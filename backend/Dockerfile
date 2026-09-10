FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN apk update && apk upgrade \
    && npm install -g npm@latest \
    && npm ci --omit=dev

COPY . .

EXPOSE 3000

CMD ["npm", "start"]