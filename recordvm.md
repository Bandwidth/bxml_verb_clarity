
## XML: `<RecordVM>`
The RecordVM verb is used to record a brief message from the user like a voicemail message. At the end of the call, a call recording event containing the media with recorded audio URL is generated.


### Attributes
| ATTRIBUTE             | DESCRIPTION                                                                                                    |
|:----------------------|:---------------------------------------------------------------------------------------------------------------|
| requestUrl            | (optional) Absolute URL to send event and request new BXML.                                        |
| requestUrlTimeout     | (optional) The time in milliseconds to wait for requestUrl response. Default: 2000. Range:100-120000          |
| requestUrlMethod      | (optional) HTTP method to be used. Allowed values: GET or POST. Default: POST                                  |
| fileFormat            | (optional) The format that the recording will be saved - mp3 or wav. Default: wav                              |
| terminatingDigits     | (optional) One or more digits that will finish the recording.                                                  |
| maxDuration           | (optional) The time in second for max recording duration. Default is 300 seconds, up to 3600 seconds (1 hour). |
| transcribe            | (optional) A boolean value to indicate that recording must be transcribed. Default is ‘false’.                 |
| transcribeUrl         | Absolute URL to send transcribed event. Required if transcribe=true                                            |
| transcribeUrlMethod   | (optional) HTTP method to be used. Allowed values: GET or POST. Default: POST                                  |

##### Tip:
Any verb after <RecordVM> will not be executed. The recording event is sent to the requestUrl specified and a valid BXML response is expected to continue the call.

<aside class="alert general small">
<p>
Transcription will not work with mp3 file format.
</p>
</aside>

### Events Recevied

| Event                              | Can reply with more BXML |
|:-----------------------------------|:-------------------------|
| [Record](events/recording.md)      | Yes                      |
| [Transcribe](events/transcribe.md) | No                       |


#### Example: Recording Verb
This shows how to use Bandwidth XML record a phone call.

```XML
<?xml version="1.0" encoding="UTF-8"?>

<Response>

<SpeakSentence voice="paul" gender="male" locale="en_US">Recording your call, type 1 2 3 4 * to stop recording</SpeakSentence>

<PlayAudio>https://audio.url/audio.mp3</PlayAudio>

<Record requestUrl="/stepTransfer" terminatingDigits="1234*" maxDuration="60" transcribe="true" transcribeCallbackUrl="https://transcribe.url/result"/ >

</Response>
```
