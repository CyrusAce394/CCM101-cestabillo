# MinIO Object Storage Deployment Documentation

## Deployment Details

### Deployment Command

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  minio/minio server /data --console-address ":9001"
```

### Port Configuration

* **Web Console Port:** `9001`
* **API Port:** `9000`

### Bucket Created

* **Bucket Name:** `client-photos`

## Environment Variables Explained

The `-e` flags are used to pass environment variables into the MinIO container when it starts.

### Root Username

```bash
-e "MINIO_ROOT_USER=cloudadmin"
```

Sets the root administrator username used to authenticate with the MinIO server and web console.

### Root Password

```bash
-e "MINIO_ROOT_PASSWORD=CloudNova2026!"
```

Sets the password associated with the MinIO root administrator account.

## Summary

MinIO was successfully deployed using Docker. The server provides an S3-compatible object storage service, with the web console available through port `9001` and the API accessible through port `9000`. A bucket named `client-photos` was created for storing objects.
