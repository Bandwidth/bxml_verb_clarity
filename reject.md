
## XML: `<Reject>`
The Reject verb is used to reject incoming calls.



### Attributes
| ATTRIBUTE | DESCRIPTION                                                                                                     |
|:----------|:----------------------------------------------------------------------------------------------------------------|
| reason    | (optional) Describe the reason for rejecting the call (busy or rejected to play different tones to the caller). |


### Events Recevied

| Event | Can reply with more BXML |
|:------|:-------------------------|
| None  | No                       |


#### Example: Reject Verb
This shows how to use Bandwidth XML to reject an incoming call.

```XML
<?xml version="1.0" encoding="UTF-8"?>

<Response>
     <Reject></Reject>
</Response>
```


