# RBDB
### API

**`tags`** – Filter by all specified tags (exact, case-insensitive)  
`?tags=Tag1,Tag2` → `?tags=Malware,Fraud,Asshole`

**`username`** – Partial match on `username`  
`?username=text` → `?username=astro`

**`userid`** – Exact Discord user ID  
`?userid=id` → `?userid=1208128286471880807`

**`nickname`** – Partial match on `nickname`  
`?nickname=text` → `?nickname=Vale`

**`sort`** – Sorting options:  
- `sort=tags` → Most tags first  
- `sort=tag:TagName` → Most occurrences of that tag first  
Examples: `?sort=tags`, `?sort=tag:Fraud`

**Combine parameters:**  
`?tags=Malware,Fraud&username=astro&sort=tags`


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

### Tagging
These are some standardized tags you can use to describe a user and their actions. Other tags are also accepted.
```
Red:
Malware - User has history of spreading malware, such as RATs, loggers, or other malicious software types.
Fraud - User has history of stealing accounts, money, or other products.
Exitscam - User has been involved in, or contributed to, an exitscam

Orange:
Paster - When someone is a verified skid or owns an executor using someone elses API/Injector/Source/Backend.
Althopping - When someone deliberately changes their identity or switches accounts to evade public scrutiny.

Purple:
Inactive - If the user account specified is inactive.
Owner - If the user has or is an owner of a service or product.
Staff - If the user has or is a staff member of a service or product.
```
