# Acoustic Code Challenge

This is a code challenge made for [Acoustic](https://acoustic.co/) which
consists in SPA applications that consumes Acoustic Content APIs and render the
content returned using different front-end techologies such as React and
Angular.

To be able to run these projects locally, it's highly recommended that you use
docker. If you don't have docker installed see:
https://docs.docker.com/engine/installation.

If you don't want to use docker for some reason, try and prepare your local
development environment in accordance to the technologies and versions
present in the `Dockerfile.dev` of each project and see the how to run
them on their respectives `docker-compose.yml`.

## Configuration

```
git submodule update --init
```

Follow config instructions in the README.md of each service.

## Updating the submodules

```
./update <GIT_BRANCH>
```

## Build Services Images

```
docker-compose build <SERVICE NAME>
```

## Creating Services Containers

```
docker-compose up <SERVICE_NAME_1> [<SERVICE_NAME_2> ...]
```

Use option `-d` for running on background. Ex:

```
docker-compose up -d <SERVICE_NAME_1> [<SERVICE_NAME_2> ...]
```

## Destroying Services Containers

1. find services containers names with `docker ps -a`
1. destroy them with `docker rm -f <CONTAINER NAME 1> [<CONTAINER NAME 1> ...]`

## Starting Services Containers

```
docker-compose start <SERVICE_NAME_1> [<SERVICE_NAME_2> ...]
```

## Stopping Services Containers

```
docker-compose stop <SERVICE_NAME_1> [<SERVICE_NAME_2> ...]
```

## Logs

```
docker-compose logs <SERVICE_NAME>
```

## Protips

Create some aliases to avoid writing docker-compose commands. In your `.bashrc`
file you can add the following:

```
alias dce='docker-compose exec'
alias dcl='docker-compose logs'
alias dcr='docker-compose run'
alias dcu='docker-compose up'
```
