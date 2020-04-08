# Nuxt.js Docker Template

This is a Docker template that provides an environment with Nuxt.js.

## Requirement

- [Docker](https://www.docker.com/)
  - docker-compose

## Usage

Run Server:

```console
$ docker-compose up
```

Go to http://localhost:3000 and you'll see the website.

## Install

Clone repository:

```console
$ git clone https://github.com/PiroHiroPiro/docker_template_nuxt.git
$ cd docker_template_nuxt
```

Build image:

```console
$ docker-compose build
```

Create new Nuxt.js application:

```console
$ docker-compose up -d
$ docker-compose exec node npm install create-nuxt-app
$ docker-compose exec node npx create-nuxt-app <project-name>
```

Change Dockerfile:

```./docker/node/Dockerfile
...
WORKDIR /src/app/<project-name>

# install packages.
RUN npm install

EXPOSE 3000
CMD ["npm", "run", "dev"]
```

Stop docker container:

```console
$ docker-compose down
```

Rebuild docker image:

```console
$ docker-compose build
```

## Licence

This software is released under the MIT License, see [LICENSE](https://github.com/PiroHiroPiro/docker_template_nuxt/blob/master/LICENSE).

## Author

[Hiroyuki Nishizawa](https://github.com/PiroHiroPiro)
