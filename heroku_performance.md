# Heroku Performance Workshop

- dyno is just a process listening on a port
- Procfile
  - without a procfile, heroku will use webrick -> bad for production
  - define which server to use
