# Find Skills
Get a list of Skills
- Match by name
- Match by Individual Profile ID
- Match by Skill ID

---
## Preconditions
 - Logged in user who has been authenticated and has a valid session token.


### Request
Passing in different filtering criteria depending on what the user is trying to accomplish
Find Skill by name (query) and individual profile id

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+----------------------+------------------------+--------------------------------------------------------------------------------+
| Parameter            | Allowed Values/Datatype| Description                                                                    |
+======================+========================+================================================================================+
| start                | number                 |    the index to start with - optional - default is 0                           |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| limit                | number                 |    the count of how many activities to return - optional - default is 20       |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_id             | string                 |    see details about a skill                                                   |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| attendee_profile_id  | string                 |    see what skills are related to this profile is working with                 |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| name                 | string                 |    search for skills that are similar to name                                  |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| search_type          | string                 |    search type can include partial or can include synonyms     popular         |
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "start" : 0,
  "limit" : 20,
  "attendee_profile_id" : "12345",
  "skill_id" : "1234",
  "name" : "Python",
  "search_type" : "partial"
}
```

---
## Post-Conditions
A set of matching skills

### Response

A description of the Response

#### Parameters

```eval_rst
+-----------------------+------------------------+-------------------+
| Parameter             | Allowed Values/Datatype| Description       |
+=======================+========================+===================+
| status                | string                 |    some text      |
+-----------------------+------------------------+-------------------+
| message               | string                 |    some text      |
+-----------------------+------------------------+-------------------+
| skills:skill:id       | string                 |    some text      |
+-----------------------+------------------------+-------------------+
| skills:skill:name     | string                 |    some text      |
+-----------------------+------------------------+-------------------+

```

#### Sample Response

```json
{
  "status" : "0000",
  "message" : "looks good bro",
  "skills" : 
  {
  	"skill" : 
  	{
  		"id" : 1,
  		"name" : "Fire"
  	},
  	"skill" : 
  	{
  		"id" : 2,
  		"name" : "Wind"
  	}
  }
}
```
##### Status Codes

```eval_rst
+---------------+-------------------+
| Code          | Description       |
+===============+===================+
| 0000          | Success           |
+---------------+-------------------+
| 0404          | Error Not Found   |
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
