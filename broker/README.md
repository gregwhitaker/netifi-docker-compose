# broker
Deploys a single instance of the Netifi Broker.

The Netifi Broker will start with the following port mappings:

| Host | Container | Description |
|------|-----------|-------------|
| 6001 | 6001 | Admin |
| 7001 | 7001 | Clustering |
| 8001 | 8001 | TCP |
| 8101 | 8101 | Websockets |

## Configuring the Broker
Configuration options for the broker can be found in the [environment configuration](.env) file.

## Starting the Broker
In the current directory, run the following command to deploy the broker:

    docker-compose up

## Stopping the Broker
In the current directory, run the following command to stop the running broker:

    docker-compose kill

## Removing the Broker Container
In the current directory, run the following command to remove the broker container:

    docker-compose rm
