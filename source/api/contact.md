# Contact Service
This service looks up data from invite table and sends a templated message to an email address or sms
This service should not be exposed externally

---
## Preconditions
 - An invite has been added to the invite table and has an email address in it
 - A shadow profile will have been created for user

### Request

A json document as a request which has the values to fill-in a template ... the template info is also passed in.

#### Authentication / Authorization
 - Notes on Authentication / Authorization
 - This should not be able to be called externally - may be orchestrated within the "invite" service.

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| InviteID      | 11234                  |     INVITE_ID from INVITE table                                                |
+---------------+------------------------+--------------------------------------------------------------------------------+
| TemplateID    | EmailInvite            |     Identifier to pull template information from                               |
+---------------+------------------------+--------------------------------------------------------------------------------+
| EmailAddress  | bob@bob.com            |     Email address to send the invite  to                                       |
+---------------+------------------------+--------------------------------------------------------------------------------+
| Unique Code   | ABCD1234DEFG1234ABCD   |     Unique Code                                                                |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "InviteID" : "1234",
  "TemplateID" : "EmailInvite",
  "EmailAddress" : "bob@bob.com",
  "EmailAddress" : "ABCD1234DEFG1234ABCD" 
}
```

---
## Post-Conditions
A message is sent out to the email address
The Invite status is updated in the INVITE table

### Response

Status of the request is returned.

#### Parameters

```eval_rst
+---------------+------------------------+------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                        |
+===============+========================+====================================+
| status        | string                 |    string of numbers               |
+---------------+------------------------+------------------------------------+
| message       | string                 |    a description of the status     |
+---------------+------------------------+------------------------------------+

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
+---------------+----------------------------------------------+
| Code          | Description                                  |
+===============+==============================================+
| 0000          | Content Cell                                 |
+---------------+----------------------------------------------+
| 0500          | Unknown Error occured during processing      |
+---------------+----------------------------------------------+
```

#### Implementation details

Include any orchestration or implementation details here.

---
## Notes:
- Note 1, this is a Note
- Note 2, this is another note
