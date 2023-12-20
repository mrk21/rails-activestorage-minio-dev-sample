# Rails ActiveStorage MinIO dev sample

[![rails-activestorage-minio-dev-Page-2.drawio.png](docs/rails-activestorage-minio-dev-Page-2.drawio.png)](docs/rails-activestorage-minio-dev-Page-2.drawio.png)

## Dependencies

- Ruby: 3.2.2
- Rails: 7.0.x
- MySQL: 8.x
- MinIO
- Docker
- Docker Compose
- direnv

## Setup

```sh
# direnv
cp .envrc.sample .envrc
vi .envrc
direnv allow .

# dokcer build
docker compose build

# minio
docker compose run --rm mc mb minio/file
docker compose run --rm mc anonymous set public minio/file

# application
docker compose run --rm rails bundle
docker compose run --rm rails rails db:setup

# run
docker compose up
open http://localhost:3000
```
