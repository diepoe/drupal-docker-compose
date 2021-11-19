# drupal-docker-compose

My docker-compose configuration for the drupal content-managment-system.

## setup

1. Ensure Docker & docker-compose are installed

### without git

2. Create a directory and `cd` into it
3. Download the compose file with

```sh
curl -o docker-compose.yml https://raw.githubusercontent.com/haudraufhaun/drupal-docker-compose/main/docker-compose.yml\?token\=ALLNLZJ3UESSGURTJSTBD2LBU
```

and the `.dockerignore` file with

```sh
curl -o .dockerignore https://raw.githubusercontent.com/haudraufhaun/drupal-docker-compose/main/.dockerignore?token=ALLNLZM3Q4TBJ45O5OAD7MDBUDOM4
```

4. Change POSTGRES_PASSWORD in the `docker-compose.yml` file

5. Launch the setup:

```sh
docker-compose up
```

> If you want to run the server in the background, use the `docker-compose up -d` command

6. Now you can visit the drupal setup screen via the ip address of your host machine

### with git

2. Clone the repository (or download it manually):

```sh
git clone https://github.com/haudraufhaun/drupal-docker-compose.git
```

3. Change POSTGRES_PASSWORD in the `docker-compose.yml` file

4. Launch the setup:

```sh
docker-compose up
```

> If you want to run the server in the background, use the `docker-compose up -d` command

5. Now you can visit the drupal setup screen via the ip address of your host machine

## security note

I recommend to change the login credentials of the postgres db for more security.
