# Using the php image #
## Build the image ##
Navigate to the php docker file and run:
```bash
$ docker build . -t mjovel/php-debug-alpine
```

After that run:

```bash
$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp -e XDEBUG_CONFIG=remote_host=10.0.20.73 mjovel/php-debug-alpine php helloWorld.php
```

## With docker compose ##
Run:
```bash
IP={{YOUR_IP}} docker-compose up --build
```
Replace `{{YOUR_IP}}` with your current IP.
