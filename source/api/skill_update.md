# Service Profile Update Skill
This service will add skill to a profile

---
## Preconditions
 - User is logged in


### Request

A description of the Request

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+----------------------+------------------------+--------------------------------------------------------------------------------+
| Parameter            | Allowed Values/Datatype| Description                                                                    |
+======================+========================+================================================================================+
| skill:id             | string                 |    skill id - (required)                                                       |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill:name           | string                 |    skill name                                                                  |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill:description    | string                 |    skill description                                                           |
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "skill" : 
  	{	
  		"id": 2,
  		"name" : "Power of Boom",
		"description" : "drops lyrics like Nicki Minaj"  	
  	}
}
```

---
## Post-Conditions
Skill updated

### Response

A simple response telling us if skill was updated not

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
- Note 1
