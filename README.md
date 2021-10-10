# fork-compose
docker-compose for chia forks

# Installation:
### This repo requires docker-compose

Clone this repo into your home directory such that ~/fork-compose is created.

Append the contents of .bash_aliases.sample to ~/.bash_aliases or symbolicly link it then run `source ~/.bashrc` to load the new commands.

Copy or rename .env.sample to ~/fork-compose/.env and edit the paths & IP within acxcording to you needs.

# Usage:
### All commands will run against all containers unless a single containername or a space seperated list of containernames is appended to the command.
- To create the stack of full nodes run `nodeup`
- To stop the stack of full nodes run `nodestop`
- To destroy the stack of full nodes run `nodedown`
- To see the full node container logs run `nodelogs`
- To recreate running full node containers run `noderec`
- To pull the latest version of the full node container use `nodepull`
- To restart the full node containers `noderestart`

- To create the stack of harvesters run `forkup`
- To stop the stack of harvesters run `forkstop`
- To destroy the stack of harvesters run `forkdown`
- To see the harvester container logs run `forklogs`
- To recreate running harvester containers run `forkrec`
- To pull the latest version of the harvester container use `forkpull`
- To restart the harvester containers `forkrestart`

# Repository Rename
### If you downlodaded this repo when it was called forkdocker you will need to runn the following commands to update the name to fork-compose
run either forkdown or nodedown depending on your setup then the following commands:
```
cd ~
sed -i 's/forkdocker/fork-compose/g' .bash_aliases
source ~/.bashrc
mv ~/forkdocker ~/fork-compose
cd ~/fork-compose
git remote set-url origin https://github.com/SparXalt/fork-compose.git
git pull
```
then run forkup or nodeup
