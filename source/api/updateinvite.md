# Update Invite
The ablity to update invite with either accepting invite or denying - asking to not be contacted again.

---
## Preconditions
 - A validated link has been clicked by the user
 - Successful response of view invite service
 
### Request

Invite ID, Invited Profile ID and Inviter Profile ID will be used in accepting or denying invites.


#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| Invite:ID     | String                 |    some text                                                                   |
+---------------+------------------------+--------------------------------------------------------------------------------+
| Invite:Accept | Yes or No              |    some text                                                                   |
+---------------+------------------------+--------------------------------------------------------------------------------+
| Invited:ID    | String                 |    some text                                                                   |
+---------------+------------------------+--------------------------------------------------------------------------------+
| Inviter:ID    | String                 |     some text                                                                  |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
	"Invited" :
  	{
  		"ID": "1234"
  	}
  	"Invite" :
  	{
  		"ID" : "1234",
  		"Accept" : "Yes"
  	}
  	"Inviter" :
  	{
  		"ID": "1234"
  	}
}
```


---

## Post-Conditions
The invite is accepted and status is set to complete
The invite is denied
The inviter is given more invites
The invited has a profile that is set to new

### Response

Status of the Invite Update

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

The invite is accepted and status is set to complete
The invite is denied
The inviter is given more invites
The invited has a profile that is set to new

---
## Notes:
- Note 1, this is a Note
- Note 2, this is another note
