# BXML Verb Clarity

## Verbs

| Verb                                  | Description                                                                                                                                     | Comments |
|:--------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|:--------:|
| [`<Gather>`](gather.md)               | The Gather verb is used to collect digits for some period of time.                                                                              ||
| [`<Hangup>`](hangup.md)               | The Hangup verb is used to hangup current call.                                                                                                 || 
| [`<PlayAudio>`](playAudio.md)         | The PlayAudio verb is used to play an audio file in the call.                                                                                   ||
| [`<Record>`](record.md)               | The Record verb allows call recording. At the end of the call, a call recording event containing the media with recorded audio URL is generated ||
| [`<Redirect>`](redirect.md)           | The Redirect verb is used to redirect the current XML execution to another URL.                                                                 ||
| [`<SpeakSentence>`](speakSentence.md) | The SpeakSentence verb is used to convert any text into speak for the caller.                                                                   ||
| [`<Transfer>`](transfer.md)           | The Transfer verb is used to transfer the call to another number.                                                                               ||


## Events/Callbacks

| Event                                         | Description                                                                                                                                                                                    |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Answer Event](events/answer.md)              | Bandwidth API sends this message to the application when the call is answered.                                                                                                                 |
| [Gather event](events/gather.md)              | Bandwidth API generates a gather event when the gather command completes in a call.                                                                                                            |
| [Hangup Event](events/hangup.md)              | Bandwidth API sends this message to the application when the call ends.                                                                                                                        |
| [Recording event](events/recording.md)        | Bandwidth API sends this event to the application when the recording media file is saved or an error occurs while saving it.                                                                |
| [Transcription event](events/transcription.md)        | Bandwidth API sends this event to the application when the recording media file is transcribed if requested. |
| [Redirect event](events/redirect.md)          | Bandwidth API sends this event to the application when a `<Redirect>` is requested                                                                                                             |
| [Transfer Complete Event](events/transfer.md) | Bandwidth API sends this event to the application when the `<Transfer>`is complete                                                                                                             |
