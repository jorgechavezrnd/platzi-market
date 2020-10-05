# Commands for start postgres database
- `docker pull postgres:9.6.6-alpine`
- `docker run -d --name postgres_server -p 5432:5432 -e POSTGRES_PASSWORD=platzi postgres:9.6.6-alpine`

# Command for start pgadmin container
- `docker run -p 64374:80 -e "PGADMIN_DEFAULT_EMAIL=user@domain.com" -e "PGADMIN_DEFAULT_PASSWORD=SuperSecret" -d dpage/pgadmin4`
- Go to http://localhost:64374 for login and start

# URL for Swagger documentation
- http://localhost:8090/platzi-market/api/swagger-ui.html

# For generate jar file
- Go to Gradle in Intellij, and execute the 'build/bootJar' task

# Command for execute the jar file
- `java -jar .\build\libs\platzi-market-1.0.jar`

# Command for execute the jar with production profile
- `java -jar -Dspring.profiles.active=pdn build/libs/platzi-market-1.0.jar`

# Commands for deploy to heroku:
- `heroku login`
- `heroku create platzimarketjorge`
- `heroku addons:create heroku-postgresql`
- `heroku config`
- Now we go to PgAdmin with the credentials that the last command shows
