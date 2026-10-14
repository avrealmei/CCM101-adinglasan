# Technical Documentation #

This document records the technical deployment, configuration, and management steps for the MinIO S3-compatible object storage server.

## Deployment Execution
The MinIO container was deployed using Docker with explicit network interface bindings (`0.0.0.0`) and root environment credentials:
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  pgsty/minio server /data --address "0.0.0.0:9000" --console-address "0.0.0.0:9001"
```
## Web Management Console Access ##
- Port Number: Port 9001 (forwarded via KillerCoda Traffic Port Accessor).
- Credentials: cloudadmin / CloudNova2026!

## Bucket Creation & File Upload
- Bucket Name: client-photos
- Operation: Created the bucket using the MinIO Web Console interface and successfully uploaded a verification test asset.

 ## A brief explanation of what the -e flags (Environment Variables) did in your Docker command

 In our Docker command, the `-e` flags stand for environment variables, which serve as a clean and secure way to inject configuration settings directly into the container's isolated runtime space the moment it boots up. Since containers are self-contained and don't automatically know our custom credentials, using `-e "MINIO_ROOT_USER=cloudadmin"` and `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` tells the MinIO server exactly which master username and secure password to initialize. Without passing these flags, the container would either block administrative access or default to standard guest settings, so utilizing them ensures our custom keys are properly locked in for authenticating into the web console and handling secure cloud storage operations.
 
