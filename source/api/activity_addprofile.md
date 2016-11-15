# Service API Activity Add Profile
This service will record a request from an individual to work on an activity

---
## Preconditions
 - User is logged in
 - User has skill requested or could have skill requested
 - There is an open activity

### Request

User requests that they are considered for an activity.

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------------+------------------------+--------------------------------------------------------------------------------+
| Parameter           | Allowed Values/Datatype| Description                                                                    |
+=====================+========================+================================================================================+
| profile:id          | string                 |    some text                                                                   |
+---------------------+------------------------+--------------------------------------------------------------------------------+
| activity:id         | string                 |     some text                                                                  |
+---------------------+------------------------+--------------------------------------------------------------------------------+
| activity:skill:id   | string                 |     some text                                                                  |
+---------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "profile" :
  {
  	"id" : 1234
  }
  "activity" : 
  {
  	"id" : 1234, 
	"skill" : 
	{
		"id" : 1234
	}
  }
}
```

---
## Post-Conditions
User is able to know if their request was added

### Response

A simple response telling user if the users profile was added to activity skill relationship was added

#### Parameters

```eval_rst
+---------------+------------------------+-------------------+
| Parameter     | Allowed Values/Datatype| Description       |
+===============+========================+===================+
| status        | string                 |    some text      |
+---------------+------------------------+-------------------+
| message       | string                 |    some text      |
+---------------+------------------------+-------------------+

```

#### Sample Response

```json
{
  "status" : "0000",
  "message" : "looks good bro"
}
```
##### Status Codes

```eval_rst
+---------------+-------------------+
| Code          | Description       |
+===============+===================+
| 0000          | Success           |
+---------------+-------------------+
| 0500          | Error Occured     |
+---------------+-------------------+
```

#### Implementation details

Include any orchestration or implementation details here.

---
## Notes:
- Note 1, this is a Note
- Note 2, this is another note
