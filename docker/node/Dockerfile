FROM node:12.5

# locale & timezone (Asia/Tokyo)
# https://github.com/moby/moby/issues/12084
ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

# https://stackoverflow.com/questions/43746782/running-nuxt-js-application-in-docker
ENV HOST 0.0.0.0

# system update
RUN apt-get update \
    && apt-get install -y vim less

WORKDIR /root

# copy application code from host.
ADD ./src /src
WORKDIR /src/app

## install packages.
# RUN npm install

# EXPOSE 3000
# CMD ["npm", "run", "dev"]
