# RBDB
### Formatting
The structure of a card is
```json
{
  "nickname": "",
  "id": "",
  "tags": [],
  "note": "",
  "refs": []
}
```
Tags, Notes and References are optional and don't have to be included but it's good practice to include them.
When outputting to the API, the card structure will be
```json
{
  "nickname": "Astroghost",
  "id": "1208128286471880807",
  "tags": [],
  "note": "",
  "refs": [],
  "username": "",
  "created": "",
  "avatar": ""
},
```
When an ID is invalid, it will replace Username, Created, and Avatar marked as "Unknown Account"
