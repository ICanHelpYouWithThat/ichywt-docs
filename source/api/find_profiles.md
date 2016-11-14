# Profile 
This service retrieves a profile

---
## Preconditions
 - Profile ID
 - Logged in user

### Request

A profile ID

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| ProfileID     | String                 |    the unique ID of a profile                                                  |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "profileid" : "123456"
}
```

---
## Post-Conditions
The details of a profile are returned

### Response

The details of a profile

#### Parameters

```eval_rst
+--------------------------+------------------------+-----------------------------------------------------+
| Parameter                | Allowed Values/Datatype| Description                                         |
+==========================+========================+=====================================================+
| status                   | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| message                  | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:id               | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:name             | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:karma            | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:email            | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:phone            | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:geolocation      | string                 |    lat,long                                         |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:zipcode          | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:type             | string                 |    type of profile: 1 individual, 2 organization    |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:mission          | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:admin            | string                 |    Admin: 0 No, 1, yes                              |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:likes            | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:invites          | string                 |    count of invites left                            |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:status           | string                 |    Invited, New, Active, Deleted                    |
+--------------------------+------------------------+-----------------------------------------------------+
| Profile:linked_acct      | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
```

#### Sample Response

```json
{
  "status" : "0000",
  "message" : "looks good bro",
  {
  	"Profile" :
  	{
  		"id" : "12345",
  		"name" : "bob smith",
  		"karma" : "5",
  		"email" : "bob@smith.com",
  		"phone" : "123-123-1234",
  		"geolocation" : "37.4211274197085,-122.0855988802915",
  		"zipcode" : "12345",
  		"type" : "1",
  		"mission"  : "This is the mission of the user - individual mission or organizations mission.",
  		"admin" : "1",
  		"likes" : "52",
  		"invites" : "50",
  		"status" : "New",
  		"linked_acct" : "test"	
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
