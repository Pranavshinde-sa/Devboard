# STAGE - 1

FROM golang:1.24-alpine AS builder

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN CGO_ENABLED=0 go build -o devboard-backend .

# STAGE - 2

FROM golang:1.24-alpine

WORKDIR /app

RUN adduser -D -u 10001 app

COPY --from=builder /app/devboard-backend ./devboard-backend

RUN chown -R app:app /app/devboard-backend

USER app

RUN chmod +x ./devboard-backend

EXPOSE 8080
 
ENTRYPOINT ["./devboard-backend"]
