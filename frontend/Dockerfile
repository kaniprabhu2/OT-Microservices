FROM node:18-alpine

LABEL maintainer="Opstree Solutions"

COPY . /app
WORKDIR /app/

RUN apk add --no-cache git

RUN npm install 
RUN npm run build

RUN yarn global add serve

EXPOSE 3000

ENTRYPOINT ["serve", "-s", "build"]
