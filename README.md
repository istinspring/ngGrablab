# Grablab.org web application source code.

Source code for [Grablab.org](http://grablab.org) website.

Current status: NotFinished.

## Tools and frameworks used:

+ [NodeJS](http://nodejs.org/) - platform built on Chrome's JavaScript runtime
                                 for easily building fast, scalable network applications.
+ [LoopBack](http://loopback.io) - API framework based on ExpressJS.
+ [AngularJS](https://angularjs.org) - front-end framework.
+ [Docker](https://www.docker.com/) - assemble multi-container apps, run on any infrastructure.
+ [Python](http://python.org) - some additional backend things.
+ [fig.sh](http://fig.sh/) - fast, isolated development environments using Docker.


## Installation (Ubuntu 14.10)

How to install? First of all I suggest to run system update/upgrade first.

```
    sudo apt-get update && sudo apt-get upgrade
```

#### install nodejs

```
    curl -sL https://deb.nodesource.com/setup | sudo bash -
    sudo apt-get install -y nodejs
```

...Read more [install nodejs](https://github.com/joyent/node/wiki/installing-node.js-via-package-manager)


#### install Docker

```
    sudo apt-get install docker.io
```

...Read more [install docker](https://docs.docker.com/installation/)


#### Docker containers

How to login into container to check something?

```
    sudo docker run -t -i grablab/grablab-org-api /bin/bash
```

How to build own container (in case):

```
    sudo docker build -t="<image_name>" [DIR_WITH_DOCKERFILE]
```

## Gulp commands

+ **gulp lint** run few linters over js code and html/css files.
+ **gulp test** run both backend and front end tests, generate coverage report.
+ **gulp dev_server** run devserver with livereload and karma tests
+ **gulp ci** continuous integration script (make it pass before commit)

## Architecture decisions

+ [MongoDB](http://mongodb.org) as a database
+ [Prerender](http://prerender.io) render rich javascript application pages for robots
