# usage
## create container
```bash
docker build -t python-dev .
```

## run container
```bash
docker run --rm -p 8888:8888 python-dev
```

## connect to jupyter lab
access to `localhost:8888/token=<specified at log>`