# Laboratory 05 – The Cloud Data Engineer

## Mission Overview
CloudNova Technologies needs a proof-of-concept object storage environment for a client's photo-sharing application. In this mission I deployed **MinIO**, an S3-compatible object storage server, using Docker on a KillerCoda Playground. I then accessed its web console, created a bucket named `client-photos`, and uploaded a test file.

## Objectives
- Differentiate between Block, File, and Object Storage.
- Deploy an S3-compatible object storage server (MinIO) using Docker.
- Access a cloud service through a web interface using port forwarding.
- Create a storage bucket and upload objects (files) to the cloud.
- Document cloud storage operations using Markdown.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Tools Used
- KillerCoda Playground (Ubuntu/Docker environment)
- Docker
- MinIO (`minio/minio` image) and the MinIO Web Console
- GitHub and Git
- Markdown
- Web browser

## Skills Learned
- Explaining the differences between block, file, and object storage
- Deploying a containerized service with `docker run` and environment variables
- Mapping container ports (9000 for the API, 9001 for the console) to the host
- Accessing a cloud service through a browser using port forwarding
- Creating a bucket and uploading objects in an S3-compatible service
- Documenting technical work in Markdown and maintaining a GitHub portfolio

## Screenshots
| File | Shows |
|---|---|
| `screenshots/minio-deployed.png` | MinIO container deployed and running |
| `screenshots/minio-bucket-upload.png` | `client-photos` bucket with the uploaded file |

## Related Files
- [storage-types-research.md](storage-types-research.md)
- [minio-deployment.md](minio-deployment.md)
- [reflection.md](reflection.md)
