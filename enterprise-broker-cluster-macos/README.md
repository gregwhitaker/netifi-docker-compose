# enterprise-broker-cluster-macos
Deploys three clustered instances of the Netifi Enterprise Broker on MacOS.

Because Docker networking works differently on Docker for Mac you need to use this configuration when clustering local Netifi Enterprise Broker instances on MacOS.

## Configuring the Brokers
You must add values for the following configuration properties in the [environment configuration](.env) file in order for the Netifi Enterprise Brokers to start:

- `NETIFI_ENTERPRISE_ACCESSKEY` - Access key used to authenticate with the Netifi Enterprise Platform.
- `NETIFI_ENTERPRISE_ACCESSTOKEN` - Access token used to authenticate with the Netifi Enterprise Platform.
- `NETIFI_ENTERPRISE_ADDRESS` - Hostname of your Netifi Enterprise Platform endpoint.
- `NETIFI_ENTERPRISE_PORT` - Port of your Netifi Enterprise Platform endpoint.

These values will be given to you by your Netifi customer service representative. If you are not currently a Netifi customer, feel free to reach out to us by email at info@netifi.com or via our [website](https://www.netifi.com) to get started with your Netifi Enterprise trial today.

### Default Configuration

#### Access Keys
The brokers will not start with any preconfigured access keys. All access keys will be retrieved from the Netifi Enterprise Platform at startup.

#### Port Mappings
The brokers will start with the following port mappings:

##### Broker 1
| Host | Container | Description |
|------|-----------|-------------|
| 6001 | 6001 | Admin |
| 7001 | 7001 | Clustering |
| 8001 | 8001 | TCP |
| 8101 | 8101 | Websockets |

##### Broker 2
| Host | Container | Description |
|------|-----------|-------------|
| 6002 | 6002 | Admin |
| 7002 | 7002 | Clustering |
| 8002 | 8002 | TCP |
| 8102 | 8102 | Websockets |

##### Broker 3
| Host | Container | Description |
|------|-----------|-------------|
| 6003 | 6003 | Admin |
| 7003 | 7003 | Clustering |
| 8003 | 8003 | TCP |
| 8103 | 8103 | Websockets |

## Starting the Brokers
In the current directory, run the following command to deploy the broker cluster:

    docker-compose up

## Stopping the Brokers
In the current directory, run the following command to stop the running broker cluster:

    docker-compose kill

## Removing the Broker Containers
In the current directory, run the following command to remove the broker containers:

    docker-compose rm
