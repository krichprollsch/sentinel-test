# Redis Sentinel test

## Install

- install Docker & Docker compose
- `cp -fr src test`

## Run test

start containers

```
docker-compose up
```

shutdown `master` and `s1`

```
docker-compose pause master s1
```

You can see `slave` promotion to master


Restart master

```
docker-compose unpause master s1
```

`master` is now the slave of `slave`.
