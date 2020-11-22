## STEPS

```sh
heroku pg:psql --app desolate-oasis-69811

create table users(id serial primary key, username text, user_password text);
create table access_tokens(id serial primary key, access_token text, user_id integer);

http://localhost:3000/auth/register
Content-Type: application/x-www-form-urlencoded
username: test
password: test
grant_type: password
client_id: null
client_secret: null
---
OAuth2
Authorization Code
Header
Access Token
```