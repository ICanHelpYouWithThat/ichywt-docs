# Service Profile Add Skill
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
| profile:id           | string                 |    add activity related to this profile                                        |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_set:skill:id   | string                 |    skill id - optional (skill name or id required)                             |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_set:skill:name | string                 |    skill name  - optional may need to add new skill (skill name or id required)|
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "profile" : 
  {
  	"id" : 1234
  }
  "skill_set" :
  {
  	"skill" : 
  	{
  		"name" : "Power of Boom"
  	}
  	"skill" :
  	{
  		"id": 2
  	}
  }		
}
```

---
## Post-Conditions
Skill added to a user profile - possibly new skill added to skill list

### Response

A simple response telling us if skill was added or not

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
- Skills may be added by name and need to orchestrate lookup or create new skill
