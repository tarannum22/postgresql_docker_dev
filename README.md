# postgresql_docker_dev
A quick setup of PostgreSQL for development environment along with PgAdmin using Docker. 
It also includes persistent data and a docker network setup for consistent IP assignment.

Creates 2 services 
- db - PostgreSQL Service (Database Service)
- pgadmin - PgAdmin Service (UI webapp to connect to a PostgreSQL Database)

Create a network 
- postgresql_net
  - db IP - 192.168.0.2
  - pgadmin IP - 192.168.0.3
  
Ports for Host machine 
  - db - 5432
  - pgadmin IP - 5050

To use this script you need :
  - Docker Engine
  - Docker Compose
Docker Desktop installation usually takes care of both

## To start run in the project folder
docker-compose up

## For linux systems 
The first run will fail. 
Please change the file permission for the data folder created.
sudo chown -R 5050:5050 data

More details here. pgAdmin needs the data folder to have UID and GID as 5050:5050
https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html#mapped-files-and-directories

For making the pgadmin service publicly available, change port exposed from 5050 to 80
