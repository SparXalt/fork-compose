# forkdocker
docker-compose for chia forks

# Installation:
### This repo requires docker-compose

Clone this repo into your home directory such that ~/forkdocker is created.

Append the contents of .bash_aliases.sample to ~/.bash_aliases or symbolicly link it then run `source ~/.bashrc` to load the new commands.

Copy or rename .env.sample to ~/forkdocker/.env and edit the paths & IP within acxcording to you needs.

# Usage:
### All commands will run against all containers unless a single containername or a space seperated list of containernames is appended to the command.
To create the stack of harvesters run `forkup`
To stop the stack of harvesters run `forkstop`
To destroy the stack of harvesters run `forkdown`
To see the container logs run `forklogs`
To recreate running containers run `forkrec`
To pull the latest version of the container use `forkpull`
To restart the containers `forkrestart`




