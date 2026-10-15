# Mission Reflection

**1. Why is object storage better suited for storing millions of photos than a traditional block storage hard drive?**
Object storage keeps each photo as an independent object with its own metadata and unique ID in a flat structure, so it can scale almost without limit by adding more servers. A block storage drive is attached to one machine, has a fixed capacity, and needs a file system, which becomes costly and hard to manage at millions of files. Object storage is also reachable over HTTP, so a web application can serve images directly, and it is usually cheaper per gigabyte.

**2. How did using Docker make it easier to deploy MinIO?**
One `docker run` command downloaded the MinIO image, started the server, mapped ports 9000 and 9001, and set the admin credentials. I did not have to install dependencies or configure the operating system by hand. The same command would work on any machine with Docker, which makes the deployment fast and repeatable.

**3. What is a "bucket"?**
A bucket is a top-level container in object storage that holds objects. It is like a folder, but with its own unique name, access permissions, and policies. In this lab, the `client-photos` bucket held the file I uploaded.

**4. How do large enterprises keep object storage data from being lost if a server crashes?**
They replicate data across multiple drives, servers, and data centers or availability zones, so another copy is always available. Many systems also use erasure coding, which splits objects into fragments with parity data so they can be rebuilt after a disk or server failure. Versioning and backups add further protection against accidental deletion.

**5. How is my confidence in the Linux command line growing?**
My confidence grows with every mission. Commands like `docker run` and `docker ps` feel more natural, and I now understand what flags such as `-d`, `-p`, `-e`, and `--name` do instead of just copying them. I am more comfortable troubleshooting and reading terminal output.

---
*Note: Review and rewrite any answers, especially Question 5, in your own words. The total must be 250–350 words. Disclose AI assistance if your instructor requires it.*
