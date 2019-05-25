## HOW TO

### Configure

Just edit the Dockerfile and change ENV vars

### Build

```bash
docker build -t blynk .
```

### RUN

```bash
docker run -p 9443:9443 -p 8440:8440 -p 8080:8080 -v blynk-data:/data -v blynk-config:/config --name blynk-server -d silvesterhsu/blynk-server
```

Don't forget to change the port attribution if you change on the ENV vars in Dockerfile

## Visit WebUI

Open website: `https://<YOUR-IP>:9443/admin` to modify account.

## UPDATE Blynk version

## How to

Stop and remove your actual container

```bash
docker stop blynk-server && docker rm blynk-server
```

- Edit your Blynk server version on the ENV var in Dockerfile
- Build & Launch
