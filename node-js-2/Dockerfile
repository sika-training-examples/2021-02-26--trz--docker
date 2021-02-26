FROM node:15-slim as build
WORKDIR /build
COPY package.json .
COPY yarn.lock .
RUN yarn install
COPY . .
RUN yarn run static-build

FROM nginx:alpine
COPY --from=build /build/out /usr/share/nginx/html