# MinIO Deployment Documentation

## Environment
KillerCoda Ubuntu Playground with Docker installed.

## Docker Command Used
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  minio/minio server /data --console-address ":9001"
```

## Verification
```bash
docker ps
```
The `minio-server` container showed a status of `Up`, with ports 9000 and 9001 mapped.

## Access Details
| Item | Value |
|---|---|
| Web Console Port | **9001** |
| API Port | 9000 |
| Container Name | `minio-server` |
| Username | `cloudadmin` |
| Bucket Created | **client-photos** |

The console was opened through the KillerCoda **Traffic / Ports** tab by entering port 9001. After logging in, I went to **Buckets → Create Bucket**, named it `client-photos`, and uploaded a sample file with the **Upload** button.

## Command Breakdown
| Part | Meaning |
|---|---|
| `-d` | Runs the container in detached (background) mode |
| `-p 9000:9000` | Maps the S3 API port to the host |
| `-p 9001:9001` | Maps the web console port to the host |
| `--name minio-server` | Names the container |
| `minio/minio` | The MinIO image |
| `server /data` | Starts MinIO and stores its data in `/data` |
| `--console-address ":9001"` | Serves the web console on port 9001 |

## What the `-e` Flags Did
The `-e` flags set environment variables inside the container when it starts. `MINIO_ROOT_USER=cloudadmin` sets the admin username and `MINIO_ROOT_PASSWORD=CloudNova2026!` sets the admin password. MinIO reads them at startup to create the root account that I used to log in to the console. Without them, MinIO would fall back to its default credentials, which are insecure.

## Screenshots
- `screenshots/minio-deployed.png`
- `screenshots/minio-bucket-upload.png`
