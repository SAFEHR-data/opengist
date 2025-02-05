Installing via docker (using docker compose)
See https://opengist.io/docs/installation/docker.html

Data is stored in a SQLite database
This is in `./data` rather than the usual `~/.opengist` location
Might need moving to a volume with back up at a later date
Ignored from .gitignore

Config in `./config/config.yml` ... derived from `./config.yml` and referenced via volumes in docker-compose.yml
Secrets in `./config/secrets.env`

When you install on a GAE
```
git clone https://github.com/SAFEHR-data/opengist/tree/steve/gae14v1
cp ./config/example.secrets.env ./config/secrets.env
docker compose up
```

And probably best to do this in tmux so it persists between logins

---
Tried and failed to get OAuth authentication working via github
Problems with the redirect URL
Times out?
https://opengist.io/docs/configuration/oauth-providers.html#github
https://github.com/organizations/SAFEHR-data/settings/applications/2870943
https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/authorizing-oauth-apps#redirect-urls
