
## XML: `<PlayAudio>`
The PlayAudio verb is used to play an audio file in the call.


### Attributes
| ATTRIBUTE | Description                                                                                                     |
|:----------|:----------------------------------------------------------------------------------------------------------------|
| digits    | (optional) Allows you to play DTMF digits in the call (No default value). Allowed digits:0-9#\*,wW Max length of the DTMF digits string can be 90 digits. A , or w will insert a 500 ms (0.5 seconds) pause before sending the next digit and a W will insert a 1 second pause. |


### Events Recevied

| Event | Can reply with more BXML |
|:------|:-------------------------|
| None  | No                       |


#### Example:  PlayAudio Verb
This shows how to use Bandwidth XML to play an audio clip into a phone call.



```XML
<?xml version="1.0" encoding="UTF-8"?>

<Response>

<PlayAudio>https://audio.url/audio.mp3</PlayAudio>

</Response>
```


