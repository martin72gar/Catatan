This is a simple way of importing MySQL database in Docker.

1. In you Dockerfile you must have a shared folder. 
   Shared folder is a directory in your host machine that is mounted to Docker instance.
   
2. Put the exported sql file in the shared folder.

3. Login to your Docker instance via `docker exec -it DOCKER_CONTAINER_ID bin/bash`.

4. Login to MySQL via `mysql -u USERNAME -p`.

5. While in MySQL CLI, create a database via `create database DB_NAME;`.

6. While in MySQL CLI, use the database you just created via `use DB_NAME;`.

7. While in MySQL CLI, import the sql file via `source /path/to/file.sql`.

Done

src : https://gist.github.com/geraldvillorente/4c60e7fdb5562f443f16ad2bbe4235ce