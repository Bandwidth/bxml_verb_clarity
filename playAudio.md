
## XML: `<PlayAudio>`
The PlayAudio verb is used to play an audio file in the call.


### Attributes
| ATTRIBUTE | Description                                                                                                     |
|:----------|:----------------------------------------------------------------------------------------------------------------|
| None    | None|


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


