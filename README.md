# SonicShift

An mp4 to mp3 converter built on a microservices architecture with auth, notification, gateway, and converter services — containerized with Docker and orchestrated via Kubernetes.

## Services

- **Gateway** — handles uploads, routes requests, stores files in MongoDB GridFS
- **Auth** — JWT-based authentication backed by MySQL
- **Converter** — consumes messages from RabbitMQ and converts mp4 to mp3 using moviepy
- **Notification** — sends download links via Gmail once conversion is complete

## Docker Images

- `vaiibhavthatai/gateway:latest`
- `vaiibhavthatai/auth:latest`
- `vaiibhavthatai/converter:latest`
- `vaiibhavthatai/notification:latest`

## Stack

- Python (Flask)
- RabbitMQ
- MongoDB
- MySQL
- Kubernetes (k8s)
- Docker
