# syntax = docker/dockerfile:1.2
FROM node:15-slim as build
WORKDIR /build
COPY package.json .
COPY yarn.lock .
ENV YARN_CACHE_FOLDER /.yarn
RUN --mount=type=cache,target=/.yarn yarn install
COPY . .
RUN yarn run static-build

FROM nginx:alpine
COPY --from=build /build/out /usr/share/nginx/html