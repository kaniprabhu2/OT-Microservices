FROM node:18-alpine

LABEL maintainer="Opstree Solutions"

WORKDIR /app
COPY . .

RUN apk add --no-cache git

# 🔥 FIX FOR NODE 18 + REACT
ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm install
RUN npm run build

RUN npm install -g serve

EXPOSE 3000

CMD ["serve", "-s", "build"]
