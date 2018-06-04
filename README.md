# Using the php image #
## Build the image ##
Navigate to the php docker file and run:
```bash
$ docker build . -t mjovel/php-debug-alpine
```

After that run:

```bash
$ docker run -it --rm --name my-running-script -v "$PWD":/usr/src/myapp -w /usr/src/myapp mjovel/php-debug-alpine php helloWorld.php
```
