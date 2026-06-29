# STAGE - 1 

FROM node:20-alpine AS builder

WORKDIR /app

COPY package*.json ./

RUN npm ci 

COPY . .

RUN npm run build 

# STAGE - 2

FROM node:20-alpine  

WORKDIR /app

COPY package*.json ./

RUN npm install -g vite@7.3.6

COPY --from=builder /app/dist ./dist

COPY vite.preview.config.js ./vite.config.js

RUN adduser -D -u 10001 app && chown -R app:app /app

USER app

EXPOSE 8000

CMD ["npm","run","preview","--","--host","0.0.0.0","--port","8000"]
