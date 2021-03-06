# View Invite
This service retrieves an invite information.

---
## Preconditions
 - the user has clicked on a link that is valid and identifies a valid invite

### Request

The request will be a simple url with a querystring parameter that includes 

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| InviteID      | Encoded UniqueID       |    some text                                                                   |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request
URL with querystring parameter of InviteID


---
## Post-Conditions
The user is able to accept or decline the invite (see update invite).

### Response

Information About the Invite, Information About the Invited, Information about the Inviter


#### Parameters

```eval_rst
+--------------------------+------------------------+-------------------+
| Parameter                | Allowed Values/Datatype| Description       |
+==========================+========================+===================+
| status                   | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| message                  | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Invited:ID               | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Invited:Email            | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Invite:ID                | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Invite:Status            | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Inviter:ID               | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Inviter:Name             | string                 |    some text      |
+--------------------------+------------------------+-------------------+
| Inviter:email            | string                 |    some text      |
+--------------------------+------------------------+-------------------+

```

#### Sample Response

```json
{
  "status" : "0000",
  "message" : "looks good bro".
  { 
  			"Invited" :
  			{
  				"ID": "1234",
  				"email": "bob@bob.com"
  			}
  			"Invite" :
  			{
  				"ID" : "1234",
  				"Status" : "1"
  			}
  			"Inviter" :
  			{
  				"ID": "1234",
  				"Name" : "Bob",
  				"email": "bob2@bob.com"
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
