FROM node:18-alpine

WORKDIR /app
COPY . .

RUN apk add --no-cache git

# fix for node 18
ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm install
RUN npm run build

RUN npm install -g serve

EXPOSE 3000

CMD ["serve", "-s", "build"]
