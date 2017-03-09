
## XML: `<Pause>`
Pause is a verb to specify the length of seconds to wait before executing the next verb.

<aside class="alert general small">
<p>
This feature is coming soon.
</p>
</aside>

### Attributes

| Attribute | Description                                                         |
|:----------|:--------------------------------------------------------------------|
| duration  | (required) Seconds to wait before continuing the execution of BXML. |

### Events Recevied

| Event | Can reply with more BXML |
|:------|:-------------------------|
| None  | No                       |



#### Example: Pause

```XML
<?xml version="1.0" encoding="UTF-8"?>
<Response>
	<Pause duration="4"></Pause>
</Response>
```


