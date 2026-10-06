# Mission 6 Reflection

> **Important:** This is a reflection template. Rewrite it in your own voice and include details from your actual deployment before submitting.

Writing a `docker-compose.yml` file makes a cloud engineer's job easier because the configuration for multiple containers can be described in one place. Instead of remembering and typing many commands each time, the engineer can use the same Compose file to create the required services. This makes the deployment more repeatable and helps reduce configuration mistakes.

One important thing I learned from this activity is that YAML depends on correct indentation. If I use a Tab instead of spaces or place a line at the wrong indentation level, Docker Compose may fail to parse the file or may interpret the configuration incorrectly. This showed me why formatting is not only about appearance when working with configuration files.

We also used environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` to provide configuration values to the containers. This keeps the service configuration organized and allows the application and database to use matching settings. In a real production environment, sensitive credentials should be handled more securely rather than being committed as plain text in a public repository.

Deploying Nextcloud through Docker Compose made the process feel much more practical because a complete application stack could be started using a single deployment command. Seeing the web interface become available helped me understand how containers can be combined to provide an actual application rather than just running isolated containers.

Since Mission 1, my understanding of Cloud Computing has developed from learning individual concepts to seeing how different technologies work together. I now have a better understanding of containers, deployment, networking, Infrastructure as Code, and documentation. This mission also showed me that cloud engineering involves not only running commands but also creating repeatable configurations that other engineers can understand and use.

**Before submission:** Replace general statements above with specific details from your own experience, such as an error you encountered, how long your deployment took, or what you personally found difficult.
