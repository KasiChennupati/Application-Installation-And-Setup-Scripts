# PgAdmin

[PgAdmin Website](https://www.pgadmin.org/)

The docker compose file is using an image from registry so we dont need to build.

```bash
docker-compose up
```

Add the required environment variables to the ```pgadmin4_prod_env.env``` file.

```bash
PGADMIN_DEFAULT_EMAIL=admin@pgadmin.com
PGADMIN_DEFAULT_PASSWORD=adminsecretpassword
PGADMIN_LISTEN_PORT=5050 
```

with the current setup of using dpage pgadmin docker image we cannot create multiple users on the fly.
Need to create a custome image for this and have to rebuild the docker image for every user.
Alternatives to this are to be explored.
