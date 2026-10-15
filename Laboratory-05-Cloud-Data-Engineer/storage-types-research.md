# Types of Cloud Storage

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Splits data into fixed-size blocks, each with its own address. It behaves like a raw hard drive attached to a single server, which formats it with a file system. | Operating system disks, databases, and applications that need fast, low-latency reads and writes. | AWS EBS (Elastic Block Store) |
| **File Storage** | Stores data as files in a hierarchy of folders and paths, accessed over a network using protocols such as NFS or SMB. Many machines can share it at the same time. | Shared drives, home directories, content management, and shared files across multiple servers. | AWS EFS (Elastic File System) |
| **Object Storage** | Stores each file as an object in a flat structure. Each object holds the data, its metadata, and a unique ID, and is accessed over HTTP APIs. | Massive amounts of unstructured data such as images, videos, backups, logs, and static website content. | AWS S3 (Simple Storage Service) |

## Recommendation to the Client
Object Storage is the best choice for storing user-uploaded images because it scales almost without limit to millions of files without managing disks or folder hierarchies. Each image is stored with its own metadata and unique ID and is available directly over HTTP, which suits a web application. It is also usually cheaper per gigabyte and replicates data automatically for durability, unlike containers, whose local storage is temporary.
