# Activites API
Get a list of Activities
- Match by location
- Match by skill
- Match by skill/Location
- Match by closest date
- Match by latest updated
- Match by Organization Profile ID
- Match by Individual Profile ID
- Match by Status of Activity
---
## Preconditions
 - Logged in user who has been authenticated and has a valid session token.

### Request
Passing in different filtering criteria depending on what the user is trying to accomplish
Find Activities by location, date, skill, recently updated, profile relationship, status of the activity

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
| host_profile_id      | string                 |    see what activities are related to this profile owns                        |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| attendee_profile_id  | string                 |    see what activities are related to this profile is working with             |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| geolocation          | string                 |    geo-location - lat,long                                                     |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| zipcode              | string                 |    used to find activities close by - loc of Post Office or center of  zipcode |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| radius               | number                 |    distance in miles from geo-location to find                                 |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| date_start           | number                 |    number of days since epoch to start searching for matching activities       |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| date_end             | number                 |    number of days since epoch to end searching for matching activities         |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| recent               | number                 |    number of days from today updated                                           |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| status               | string                 |    0 new, 1 open, 2 assigned, 3 completed                                      |
+----------------------+------------------------+--------------------------------------------------------------------------------+
| skill_set:id         | string                 |    list of skill_ids to find acitvities requiring a skill  (1,2,3)             |
+----------------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "start" : 0,
  "limit" : 20,
  "host_profile_id" : "12345",
  "attendee_profile_id" : "12345",
  "geolocation" : "37.4211274197085,-122.0855988802915",
  "zipcode" : "12345",
  "radius" : 1,
  "date_start" : 152,
  "date_end" : 185,
  "recent" : 1,
  "status" : "1"
  "skill_set" :
  {
  	"id": 1,
  	"id": 2
  }		
}
```

---
## Post-Conditions
Returns a set of matching activities to the search criteria passed above.

### Response

A description of the Response

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
  "message" : "looks good bro",
  "activities" : 
  {
  	"activity" : 
  	{
  		"id" : 1,
  		"org_profile_id" : 1234,
  		"status" : 0,
  		"name" : "Activity",
  		"skill" :
  		{ 
  			"id" : 1,
  			"name" : "Fire",
  			"profile_id" : 1234,
  			"status" : 0
  		}
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
