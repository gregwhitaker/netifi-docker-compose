# enterprise-broker
Deploys a single instance of the Netifi Enterprise Broker.

## Configuring the Broker
You must add values for the following configuration properties in the [environment configuration](.env) file in order for the Netifi Enterprise Broker to start:

- `NETIFI_ENTERPRISE_ACCESSKEY` - Access key used to authenticate with the Netifi Enterprise Platform.
- `NETIFI_ENTERPRISE_ACCESSTOKEN` - Access token used to authenticate with the Netifi Enterprise Platform.
- `NETIFI_ENTERPRISE_ADDRESS` - Hostname of your Netifi Enterprise Platform endpoint.
- `NETIFI_ENTERPRISE_PORT` - Port of your Netifi Enterprise Platform endpoint.

These values will be given to you by your Netifi customer service representative. If you are not currently a Netifi customer, feel free to reach out to us by email at info@netifi.com or via our [website](https://www.netifi.com) to get started with your Netifi Enterprise trial today.

### Default Configuration

#### Access Keys
The broker will not start with any preconfigured access keys. All access keys will be retrieved from the Netifi Enterprise Platform at startup.

#### Port Mappings
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
