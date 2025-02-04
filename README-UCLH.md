Installing via docker (using docker compose)
See https://opengist.io/docs/installation/docker.html

Data is stored in a SQLite database
This is in `./data` rather than the usual `~/.opengist` location
Might need moving to a volume with back up at a later date
Ignored from .gitignore

Config in `./config/config.yml`
Secrets in `./config/secrets.env`