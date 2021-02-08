# Stargazer for WordPress by mihdan
Звёзный рейтинг для WordPress

## API

* POST /v1/register
  Register a new account, you'll receive an account key and a secret.

* POST /v1/incr/key
  Increment the value of a key. Requires X-Account header.

* GET /v1/get/key1[,key2[,...]]
  Get a key, or multiple keys. Requires X-Account header.

* POST /v1/get
  Get a key or multiple keys, same syntax as /get/ but passed as the request body. Requires X-Account header.

* POST /v1/set/key1:value1[,key2:value2[,...]]
  Set one or multiple keys to their values. Require X-Account and X-Secret headers.
  
## DB

```
Column |         Type          | Modifiers 
--------+-----------------------+-----------
 key    | character varying(16) | not null
 value  | integer               | default 0
 ```
