# Technical Documentation #

This document records the technical deployment, configuration, and management steps for the MinIO S3-compatible object storage server.

## 1. Deployment Execution
The MinIO container was deployed using Docker with explicit network interface bindings (`0.0.0.0`) and root environment credentials:
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  pgsty/minio server /data --address "0.0.0.0:9000" --console-address "0.0.0.0:9001"
```
