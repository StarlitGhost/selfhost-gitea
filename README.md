[gitea](https://gitea.io/) is a self-hosted Git Repository Host.

This docker config uses [this image](https://hub.docker.com/r/gitea/gitea/)

# Setup

This relies on my [base docker services](https://github.com/StarlitGhost/selfhost-base) and 
[postgres](https://github.com/StarlitGhost/selfhost-postgres).
You'll want to symlink selfhost-base's .env file into this project's directory.

With postgres running you'll want to run the following to create an empty database:

`docker exec -it postgres createdb -U docker gitea`

Once that's done you can just spin it up with `docker-compose up -d`. The remainder of the setup is done online at `git.${DOMAIN_HOME}`
