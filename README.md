# Using the php image #
## Build the image ##
Navigate to the php docker file and run:
```bash
$ docker build -t mjovel/php-debug-alpine .
```

After that run in the root folder:

```bash
$ docker run -it --rm --name my-running-script -v "$PWD"/src:/usr/src/myapp -w /usr/src/myapp mjovel/php-debug-alpine php helloWorld.php
```

## With docker compose ##
Run:
```bash
$ docker-compose up --build
```

## Visual Code Config ##
1. Install php debug.
1. Create a new config file.
1. Under the port write the path for your project

```json
"pathMappings": {
    "/usr/src/myapp" : "${workspaceRoot}/src"
},
```
