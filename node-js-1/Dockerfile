ARG NODE_IMAGE_VERSION=15-slim
FROM node:${NODE_IMAGE_VERSION}
WORKDIR /app
COPY package.json .
COPY yarn.lock .
RUN yarn install
COPY . .
RUN yarn run build
CMD ["yarn", "run", "start"]
EXPOSE 3000