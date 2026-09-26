# MinIO Deployment Technical Documentation

## 1. Launch the KillerCoda Playground

Launch an Ubuntu or Docker-enabled KillerCoda Playground.

## 2. Deploy MinIO with Docker

The following command was provided for the laboratory activity:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
minio/minio server /data --console-address ":9001"
```

### Command Explanation

- `docker run -d` runs the container in detached/background mode.
- `-p 9000:9000` maps the MinIO API port.
- `-p 9001:9001` maps the MinIO Web Console port.
- `--name minio-server` gives the container the name `minio-server`.
- `-e "MINIO_ROOT_USER=cloudadmin"` sets the MinIO root username.
- `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` sets the MinIO root password.
- `minio/minio` is the MinIO Docker image.
- `server /data` starts MinIO using `/data` as the storage location.
- `--console-address ":9001"` configures the MinIO Web Console to use port `9001`.

The `-e` flags define environment variables inside the container. In this deployment, they provide the root login credentials used to access the MinIO service.

## 3. Verify the Container

Run:

```bash
docker ps
```

The MinIO container should appear as running.

For additional information, you may use:

```bash
docker logs minio-server
```

## 4. Access the MinIO Web Console

In KillerCoda, open the **Traffic / Ports** or **Custom Ports** feature and access port:

```text
9001
```

Log in with:

```text
Username: cloudadmin
Password: CloudNova2026!
```

## 5. Create the Storage Bucket

In the MinIO Web Console:

1. Open **Buckets**.
2. Select **Create Bucket**.
3. Enter the bucket name:

```text
client-photos
```

4. Save the bucket.

## 6. Upload an Object

Open the `client-photos` bucket and use the **Upload** button to upload a safe sample image or text file.

The uploaded file demonstrates that the object storage service is working.
