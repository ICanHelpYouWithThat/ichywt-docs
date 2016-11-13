# Profile 
This service retrieves a profile

---
## Preconditions
 - Profile ID

### Request

A profile ID

#### Authentication / Authorization
 - Notes on Authentication / Authorization

#### Parameters

```eval_rst
+---------------+------------------------+--------------------------------------------------------------------------------+
| Parameter     | Allowed Values/Datatype| Description                                                                    |
+===============+========================+================================================================================+
| ProfileID     | String                 |    some text                                                                   |
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
| Content Cell  | Content Cell      |
+---------------+-------------------+
| Content Cell  | Content Cell      |
+---------------+-------------------+

#### Implementation details

Include any orchestration or implementation details here.

---
## Notes:
- Note 1, this is a Note
- Note 2, this is another note
