## STEPS

```sh
heroku pg:psql --app desolate-oasis-69811

create table users(id serial primary key, username text, user_password text);
create table access_tokens(id serial primary key, access_token text, user_id integer);


##
POST
https://oauth2.fy1m.net/auth/register
[Header]
Content-Type: application/x-www-form-urlencoded
[Form]
username: test
password: test
grant_type: password
client_id: null
client_secret: null

POST
https://oauth2.fy1m.net/auth/login
[Header]
Content-Type: application/x-www-form-urlencoded
[Form]
username: test
password: test
grant_type: password
client_id: null
client_secret: null

POST
https://oauth2.fy1m.net/test/hello
[OAuth 2]
GRANT TYPE: Authorization Code
[Advanced Options]
ACCESS TOKEN
{***}

---
OAuth2

Header
Access Token
```