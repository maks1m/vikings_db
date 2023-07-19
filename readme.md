The project contains docker compose configuration with PostgreSQl for Vikings project.
The PostgreSQl initial configuration script is located in [/init/vikings_schema.sql>](/init/vikings_schema.sql>)

- to run database simply execute `docker compose up -d` or use script file `start.sh`;
- to stop: `docker compose down`

The database service should be started first before other services because while running `start.sh` it will create a docker network.
Otherwise you will need to create it manually running command `docker network create viking_network`
This is crucial because using this network all services will communicate between each other.