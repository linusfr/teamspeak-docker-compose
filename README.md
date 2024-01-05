# Teamspeak Docker-Compose

Simple docker-compose setup for teamspeak.

# How To

1. Copy the .env.example file to .env

```
cp .env.example .env
```

2. Ensure correct permissions on the .env file

```
chmod 660 .env
```

3. Edit the passwords in the .env file

4. Start the Services

```
docker compose up -d
```

5. Retrieve the Token and the ApiKey

```
docker compose logs teamspeak | grep -E "token=|apikey="
```

Store those away safely.
The token you need to use at your first login to gain admin privileges.

6. Open ports

Example for ufw

```
sudo ufw allow 9987/udp
sudo ufw allow 30033/tcp
sudo ufw allow 10011/tcp
```
