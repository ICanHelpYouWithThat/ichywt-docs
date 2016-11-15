# Service Add Activity
This service will add activities to the database

---
## Preconditions
 - User is logged in
 - User represents an organization that is active state

### Request

An organization would like to add in an activity


#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+----------------------+------------------------+--------------------------------------------------------------------------------+
| Parameter            | Allowed Values/Datatype| Description                                                                    |
+======================+========================+================================================================================+
| host_profile_id      | string                 |    add activity related to this profile                                        |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| name                 | string                 |    name of activity                                                            |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| mission              | string                 |    description of what this activity is trying to accomplish                   |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| geolocation          | string                 |    geo-location - lat,long                                                     |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| zipcode              | string                 |    used to find activities close by - loc of Post Office or center of  zipcode |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| date_start           | number                 |    number of days since epoch to start searching for matching activities       |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| date_end             | number                 |    number of days since epoch to end searching for matching activities         |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_set:skill:id   | string                 |    skill id - optional (skill name or id required)                             |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_set:skill:name | string                 |    skill name  - optional may need to add new skill (skill name or id required)|
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "host_profile_id" : "12345",
  "name" : "
  "geolocation" : "37.4211274197085,-122.0855988802915",
  "zipcode" : "12345",
  "date_start" : 152,
  "date_end" : 185,
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
An activity is added and will be searchable

### Response

A simple response telling us if activity was added or not

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
- When adding in activities - need to understand where the activity is in relationship to map ... so when searching for activities we can make efficient lookup by region
- Skills may be added by name and need to orchestrate lookup or create new skill