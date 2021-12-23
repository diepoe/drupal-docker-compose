# traefik

## traefik.toml

1. Install `apache-utils`

```sh
sudo apt-get install apache2-utils
```

2. Generate a secure password (replace `admin` with an username you want & `secure_password` with the password you want to use)

```sh
htpasswd -nb admin secure_password
```

3. Copy the output line into the dashboard authentications in the .toml file

4. Enter your domain name & email at the placeholders in the `traefik.toml` file

5. Create Let`s Encrypt Data storage

```sh
touch acme.json
chmod 600 acme.json
```

6. Run traefik (don't forget to enter your real domain!)

```sh
docker run -d \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v $PWD/traefik.toml:/traefik.toml \
  -v $PWD/acme.json:/acme.json \
  -p 80:80 \
  -p 443:443 \
  -l traefik.frontend.rule=Host:monitor.your_domain \
  -l traefik.port=8080 \
  --network web \
  --name traefik \
  traefik:1.7-alpine
```
