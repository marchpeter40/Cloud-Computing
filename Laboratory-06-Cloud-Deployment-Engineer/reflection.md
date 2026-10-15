# Mission Reflection

**1. How does writing a docker-compose.yml file make a cloud engineer's job easier?**
Instead of typing a separate long `docker run` command for each container and remembering every flag, I describe the whole system once in a file. One command, `docker-compose up -d`, brings everything up in the right configuration, and the file can be saved in Git, reviewed, and reused. That makes deployments faster, repeatable, and much less prone to typing mistakes.

**2. What happens if you use a Tab instead of Spaces in YAML?**
YAML only allows spaces for indentation, so a Tab causes a parsing error and Compose refuses to run, usually reporting a syntax error with the line number. Even a wrong number of spaces can change the structure, such as placing a key under the wrong service, so careful indentation matters.

**3. Why use environment variables like MYSQL_PASSWORD?**
Environment variables let me configure the containers without changing the images. The database uses them to create its user and database on first start, and Nextcloud uses the same values to connect. Keeping settings in one place avoids hard-coded values inside images, and the values are easy to change per environment. In real projects, secrets would go in an `.env` file or a secrets manager rather than being committed to GitHub.

**4. How did it feel to deploy Nextcloud in a few minutes?**
Seeing the Nextcloud setup page load after only one command was satisfying. I was surprised that a full private cloud storage system with a database needed only about 20 lines of YAML, and it made the value of Infrastructure as Code very clear.

**5. How has my understanding of cloud computing evolved since Mission 1?**
In Mission 1, cloud computing was mostly a concept to me. Since then I have moved from single containers to storage services and now to multi-tier stacks defined as code. I now see the cloud as services that can be built, repeated, and torn down quickly through automation.
