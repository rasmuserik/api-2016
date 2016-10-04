# api.solsort.com ![](https://api.solsort.com/icon-small.png)

Under development, not working yet!

Login service + couch user creation.

Will be based on https://github.com/rasmuserik/mubackend


- `/login` - redirects back to callback afte rlogin
  - `provider` = `(github|facebook|google|linkedin|wordpress|twitter)`
  - `callback` = whitelisted url to redirect back to 
  - `permissions` = whitespace separated list of permissions, later includes couchdb for access to couch.solsort.com using the login

Config via environment (initial version): 

- `URL` url for this application
- `URL_WHITELIST` whitespace separated list of valid clients
- `GITHUB_ID` `GITHUB_SECRET`
- `SESSION_SECRET` random string

Config via environment (later version): 

- `USER_HASH` random string
- `COUCH_ADMIN_USER` `COUCH_ADMIN_PASSWORD` couchdb and admin user for couch.solsort.com for creating users. 
- `TWITTER_ID` `TWITTER_SECRET`
- `WORDPRESS_ID` `WORDPRESS_SECRET`
- `FACEBOOK_ID` `FACEBOOK_SECRET`
- `GOOGLE_ID` `GOOGLE_SECRET`
- `LINKEDIN_ID` `LINKEDIN_SECRET`

Deployment via docker. https://hub.docker.com/r/solsort/api

