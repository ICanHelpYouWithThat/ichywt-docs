# Invite Service
The Invite Service will be called when a user would like to invite a person to icanhelpyouwiththat.

---
## Preconditions
 - User is logged in
 - User profile has invites available
 - Email address has not been invited before
 - Email address is not in a current profile
 - Email address in a profile has not been "disabled"

### Request

User Session Token and Email Address of invitee will be passed in the body of the request

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| email address | Email Addres           |    The email address that is being invited                                     |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "emailaddress" : "emailaddress"
}
```

---
## Post-Conditions
An invite will be added to the invite table
A new profile will be created for new user - status will be "1 - new"

### Response

 - Success: There is one success response but multiple conditions which could lead to failure
 - Failure: User Session Authentication Failed.
 - Failure: Email address has been invited before
 - Failure: Email address is all ready in current profile
 - Failure: Email address is in profile that is disabled

#### Parameters

```eval_rst
+---------------+------------------------+-------------------------------+
| Parameter     | Allowed Values/Datatype| Description                   |
+===============+========================+===============================+
| status        | string                 |    Error codes                |
+---------------+------------------------+-------------------------------+
| message       | string                 |    dscription message         |
+---------------+------------------------+-------------------------------+
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
| 0401          | Unauthorized      |
+---------------+-------------------+
| 0501          | All ready invited |
+---------------+-------------------+
| 0502          | Existing Profile  |
+---------------+-------------------+
| 0504          | Profile Disabled  |
+---------------+-------------------+
```

#### Implementation details

Will need to create an invite in the invite table 
Will need to create a sequential number that is hashed
Will need to create an invite with unique invite code
Will need to identify profile id by looking at the session info

---
## Notes:
- May look at being able to timeout invites
