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
  

To use this script you need :
Docker Engine
Docker Compose
*Docker Desktop installation usually takes care of both

To start run
docker-compose up
