# Login Service
The Login Service will authenticate a user who has a username (email address) and password.

Will need to add in locking and unlocking accounts.

---
## Preconditions
 - A profile is in active state with email and password

### Request

The request will contain a JSON document in the body of the request - username/password.  Username/Password should be passed over HTTPS.

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| userid        | email address          |    email address all lowercase                                                 |
+---------------+------------------------+--------------------------------------------------------------------------------+
| password      | password               |    password in case that was originally entered by user                        |
+---------------+------------------------+--------------------------------------------------------------------------------+
```

#### Sample Request

```json
{
  "userid" : "zmagaw",
  "password" : "thisismypassword-noreallythisismypassword"
}
```

---
## Post-Conditions
After the username/password is validated the user will be given a session token.

### Response

A JSON document in the body of the response and an HTTP cookie that will be used across requests to ensure user is authenticated and authorized. 

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


#### Success Sample Response

```json
{
  "status" : "0000",
  "message" : "looks good bro"
}
```

#### Error Sample Response

```json
{
  "status" : "0500",
  "message" : "Error exists"
}
```

##### Status Codes
```eval_rst
+---------------+------------------------+
| Code          | Description            |
+===============+========================+
| 0000          | Success                |
+---------------+------------------------+
| 0500          | Error                  |
+---------------+------------------------+
```

#### Implementation details

Include any orchestration or implementation details here.

---
## Notes:
- Will need to add in locking and unlocking accounts.
- Note 2, this is another note
