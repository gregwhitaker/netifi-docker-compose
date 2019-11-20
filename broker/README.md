# broker
Deploys a single instance of the Netifi Broker.

## Configuring the Broker
Configuration options for the broker can be found in the [environment configuration](.env) file.

## Default Configuration

### Access Keys
The broker will start with the following access keys:

- Access Key: `8833333111127534`
- Access Token: `Ih+hNsSdxLxAtHceTeEia2MGXSc=`

### Port Mappings
The broker will start with the following port mappings:

| Host | Container | Description |
|------|-----------|-------------|
| 6001 | 6001 | Admin |
| 7001 | 7001 | Clustering |
| 8001 | 8001 | TCP |
| 8101 | 8101 | Websockets |

## Starting the Broker
In the current directory, run the following command to deploy the broker:

    docker-compose up

## Stopping the Broker
In the current directory, run the following command to stop the running broker:

    docker-compose kill

## Removing the Broker Container
In the current directory, run the following command to remove the broker container:

    docker-compose rm
