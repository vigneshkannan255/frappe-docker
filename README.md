<div align="center">
	<h1>
		<br>
		<a href="https://frappeframework.com">
			<img src="https://github.com/frappe/frappe/blob/9622c882a7cb4eeaf7f950a06f55492e838cdd56/.github/frappe-framework-logo.svg" height="50">
		</a>
	</h1>
	<h3>
		a web framework with <a href="https://www.youtube.com/watch?v=LOjk3m0wTwg">"batteries included"</a>
	</h3>
</div>

</div>

Full-stack web application framework that uses Python and MariaDB on the server side and a tightly integrated client side library. Built for [ERPNext](https://erpnext.com).

</div>

<div align="center">
	<h2>
		Installation with Docker
	</h2>
</div>

<h4 align="center"><b>This script is used to run Frappe on docker container.</b></h4>

## Prerequisites

`Linux packages`

```
▶ apt install docker.io docker-compose
```
`clone`

```
▶ git clone https://github.com/vigneshkannan255/frappe-docker.git
▶ cd frappe-docker
```
`Note: Before running below command please change the IP address and database credentials in docker-compose.yaml`


## Docker compose

This command is used to make the [docker compose](https://docs.docker.com/compose/) up with detached mode.

`Note: Always we need to run docker-compose command inside the directory where we place the docker-compose.yaml file`

```
▶ docker-compose up -d
```
## After running the above command 

- [x] It will pull the required docker image from the [official repository](https://hub.docker.com/search?image_filter=official&q=) and store it in local.
- [x] It will start the container with the pulled images.
- [x] It will create the required volumes to store data.
- [x] It will create the required network.


## Images and Services

- [x] [mariadb](https://hub.docker.com/_/mariadb)
- [x] [redis:](https://hub.docker.com/_/redis)
- [x] [frappe/bench:](https://hub.docker.com/r/frappe/bench)

## Docker commands

command used to check the docker process.
```
▶ docker-compose ps -a
```

command used to check the bring down the containers.
```
▶ docker-compose stop 
```

command used to down all whole docker compose.
```
▶ docker-compose down
```


commands used to check the available docker images, container, volume and network.

```
▶ docker image ls
▶ docker container ls
▶ docker volume ls
▶ docker network ls
```


commands used to login container.

```
▶ docker exec -it container_id /bin/bash
```
commands to change permission of directory after login to container.

```
▶ sudo chown -R frappe:frappe /workspace/development
```

Here After you can you can initiate frappe bench and start creating websites.
