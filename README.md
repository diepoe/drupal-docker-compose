# drupal-docker-compose

My docker-compose configuration for the drupal content-managment-system.

## setup

1. Ensure Docker & docker-compose are installed
2. Clone the repository (or download it manually):

```sh
git clone https://github.com/haudraufhaun/drupal-docker-compose.git
```

3. Launch the setup:

```sh
docker-compose up
```

> If you want to run the server in the background, use the `docker-compose up -d` command

4. Now you can visit the drupal setup screen via the ip address of your host machine

## security note

I recommend to change the login credentials of the postgres db for more security.
