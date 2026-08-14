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

RUN apk upgrade --no-cache

COPY package*.json ./

COPY --from=builder /app/node_modules ./node_modules

COPY --from=builder /app/dist ./dist

COPY vite.preview.config.js ./vite.config.js

RUN rm -rf /usr/local/lib/node_modules/npm \
           /usr/local/bin/npm \
           /usr/local/bin/npx

RUN adduser -D -u 10001 app && \
    chown -R app:app /app

USER app

EXPOSE 8000

CMD ["node", "node_modules/vite/bin/vite.js", "preview", "--host", "0.0.0.0", "--port", "8000"]