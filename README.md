Api Platform + ReactJs Proof of Concept
=======================================

This repository contains a proof of concept for projet-aaa development. It aims at creating
a double channel using on the one hand Api Platform for REST API calls and on the other hand a websocket with NodeJs.

To run that repository, you need :

- [docker](https://docs.docker.com/engine/installation/)
- [docker-compose](https://docs.docker.com/compose/install/)

## Install

To begin with, clone the project :

```sh
git clone https://github.com/projet-aaa/Api-Poc.git
cd Api-Poc
```

## Usage

To make the containers run, you can use the following commands :

```sh
docker-compose build
docker-compose up -d
```

The shortcut command for this is :

```sh
make install
```

To stop the containers, use ```docker-compose stop``` or ```make stop```.

To remove the containers (you would need to do it in case of strange problems or build new versions), use ```docker-compose rm``` or ```make rm```.

To see the containers status, use ```docker-compose ps``` or ```make status``` shortcut command.


### Application

Once you have build your images and run you containers, you can browse [http://localhost/app_dev.php](http://localhost/app_dev.php).

You can run commands in web docker container using 
```
docker-compose exec web <your_command>
docker exec -ti --user root <your_apiplatform_web_container_id> /bin/bash
```

### Tests

You can test your project with Behat. To do so, just type ```make test_behat```

You can also use :

``` 
	docker-compose run --rm web vendor/bin/behat .

```

### Licence and so on : Refer to [Api Platform](https://github.com/api-platform/api-platform) great stuff.
