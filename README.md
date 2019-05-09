# WPDWCI

## Requirements

Make sure you have the latest versions of **Docker** and **Docker Compose** installed on your machine.

Clone this repository or copy the files from this repository into a new folder. In the **docker-compose.yml** file you may change the IP address (in case you run multiple containers) or the database from MySQL to MariaDB.


## Configuration

Edit the `.env` file to change the default IP address, MySQL root password and WordPress database name.

## Installation

Open a terminal and `cd` to the folder in which `docker-compose.yml` is saved and run:

```
docker-compose up -d
```

The containers are now built and running. You should be able to access the WordPress installation with the configured IP in the browser address. By default it is `http://127.0.0.1`.

For convenience you may add a new entry into your hosts file.

### Stopping containers

```
docker-compose stop
```

### Removing containers

To stop and remove all the containers use the`down` command:

```
docker-compose down
```

Use `-v` if you need to remove the database volume which is used to persist the database:

```
docker-compose down -v
```
#### Install Wordpress using CLI 

```
docker-compose run --rm wpcli core install --url=http://localhost --title=title_here --admin_user=admin --admin_email=admin@domainname.com --admin_password=passwordhere
``````

#### Install Wordpress Plugin and Activate
```
docker-compose run --rm wpcli plugin install wpcasa --activate
````

### COMMAND To Shut down and Delete data:

```
docker-compose down -v
```
