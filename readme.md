# Local ENV Setup
A simple way to install local env use docker for PHP

## Technology Using
| Name | version  |
| ------- | --- | 
| Docker | latest | 
| PHP | 8.0.8 |
| Nginx | Latest stable |
| mysql | 8.0.8 | 
| redis | 6.2.4 |
| kibana | 7.13.3 |
| elasticsearch | 7.13.3 |
| composer | 2 | 
| artisan | latest stable |
| npm | 13.7 |

## Requirements 
Before you get started, the following needs to be installed on your machine:
* Git 
> if your local doesn't have git
> ```s
> git --version 
> sh: git: not found
> ```
> Flow [this link](https://www.atlassian.com/git/tutorials/install-git) to install git for any env(Mac, Win or Linux) 
* Docker
> Install docker by [this URL](https://www.docker.com/products/docker-desktop)

## Project setup 
* put your project located /src/project_name
* modify docker/nginx/conf/defaults.conf

## Xdebug setup 
Xdebug is integrate to docker, so we just setup the IDE server debug to enable this feature 
* Port: 9030 
* remote_host: host.docker.internal
* idekey: PHPSTORM

Flow [this url](https://thecodingmachine.io/configuring-xdebug-phpstorm-docker) for PHP STORM setup (ONLY SETUP FOR IDE)

Have a great first work day and Good luck!





