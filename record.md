
## XML: `<Record>`
The Record verb allows call recording. At the end of the call, a call recording event containing the media with recorded audio URL is generated. Note that this event will be sent after the call is completed. 


### Attributes
| ATTRIBUTE             | DESCRIPTION                                                                                                    |
|:----------------------|:---------------------------------------------------------------------------------------------------------------|
| requestUrl            | (optional) Absolute URL to send the recording event                                                            |
| requestUrlTimeout     | (optional) The time in milliseconds to wait for requestUrl response. Default:30000; Range: 100-120000                                          |
| requestUrlMethod     | (optional) HTTP method to be used. Could be GET or POST. Default: POST                                           |
| fileFormat            | (optional) The format that the recording will be saved - mp3 or wav. Default: wav                                          |
| transcribe            | (optional) A boolean value to indicate that recording must be transcribed. Default is ‘false’.  *Note: Only wav files supported for transcription.*   |       
| transcribeUrl | Absolute URL to send transcribed event. Required if transcribe=true                                                    |
| transcribeUrlMethod     | (optional) HTTP method to be used. Could be GET or POST. Default: POST                                       |
|numChannels            | (optional) Number of channels to record the call. Allowed values:1,2. Default 1. When numChannels = 2, the caller and callee voices are recorded in separate channels in the same file. |

##### Tip:

<aside class="alert general small">
<p>
Transcription will not work with mp3 file format.
</p>
<p>
Any BXML returned to the recording or transcribe events will be ignored. 
</aside>

### Events Recevied

| Event                              | Can reply with more BXML |
|:-----------------------------------|:-------------------------|
| [Record](events/recording.md)      | No                      |
| [Transcribe](events/transcribe.md) | No                       |


#### Example: Recording Verb
This shows how to use Bandwidth XML record a phone call.

```XML
<?xml version="1.0" encoding="UTF-8"?>

<Response>
<SpeakSentence voice="paul" gender="male" locale="en_US">Recording your call</SpeakSentence>
<Record requestUrl="http://my.server/myrecording" transcribe="true" transcribeCallbackUrl="https://transcribe.url/result"/ >
<PlayAudio>https://audio.url/audio.mp3</PlayAudio>
</Response>
```
