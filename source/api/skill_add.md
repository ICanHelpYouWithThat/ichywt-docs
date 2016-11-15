# Service Add Skill
This service will add skill 

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
| skill:name           | string                 |    skill name  - optional may need to add new skill (skill name or id required)|
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill:description    | string                 |    skill name  - optional may need to add new skill (skill name or id required)|
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "skill" : 
  {
  	"name" : "Vavoom",
  	"description" : "Can clear rocks with the sound of your voice"
  }		
}
```

---
## Post-Conditions
Skill added to skill list

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
- Note 1