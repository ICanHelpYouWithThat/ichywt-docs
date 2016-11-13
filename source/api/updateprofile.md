# Update Profile
This service has 2 requirements - a valid session that has access to a specific profile
That specific profile can then be updated to any of the fields that are passed in.

---
## Preconditions
 - Bulleted list
 - Bulleted list

### Request

The request can update 

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+--------------------------+------------------------+-----------------------------------------------------+
| Parameter                | Allowed Values/Datatype| Description                                         |
+==========================+========================+=====================================================+
| id                       | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| name                     | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| karma                    | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| email                    | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| phone                    | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| geolocation              | string                 |    lat,long                                         |
+--------------------------+------------------------+-----------------------------------------------------+
| zipcode                  | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| type                     | string                 |    type of  1 individual, 2 organization            |
+--------------------------+------------------------+-----------------------------------------------------+
| mission                  | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| admin                    | string                 |    Admin: 0 No, 1, yes                              |
+--------------------------+------------------------+-----------------------------------------------------+
| likes                    | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
| invites                  | string                 |    count of invites left                            |
+--------------------------+------------------------+-----------------------------------------------------+
| status                   | string                 |    Invited, New, Active, Deleted                    |
+--------------------------+------------------------+-----------------------------------------------------+
| password                 | string                 |    Password                                         |
+--------------------------+------------------------+-----------------------------------------------------+
| linked_acct              | string                 |    some text                                        |
+--------------------------+------------------------+-----------------------------------------------------+
```

#### Sample Request

```json

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
  		"password" : "thisismypassword",
  		"linked_acct" : "test"	
  	}

```

---
## Post-Conditions
A description of the post-conditions.

### Response

A description of the Response

#### Parameters

```eval_rst
+---------------+------------------------+-------------------+
| Parameter     | Allowed Values/Datatype| Description       |
+===============+========================+===================+
| Content Cell  | Content Cell           |    some text      |
+---------------+------------------------+-------------------+
| Content Cell  | Content Cell           |    some text      |
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
