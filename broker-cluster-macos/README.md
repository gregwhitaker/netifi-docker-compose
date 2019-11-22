# broker-cluster-macos
Deploys three clustered instances of the Netifi Broker on MacOS.

Because Docker networking works differently on Docker for Mac you need to use this configuration when clustering local Netifi Broker instances on MacOS.

## Configuring the Brokers
Configuration options for the brokers can be found in the [environment configuration](.env) file.

### Default Configuration

#### Access Keys
The brokers will start with the following preconfigured access key:

- Access Key: `8833333111127534`
- Access Token: `Ih+hNsSdxLxAtHceTeEia2MGXSc=`

The brokers will start with the following preconfigured admin access key:

- Access Key: `9007199254740991`
- Access Token: `kTBDVtfRBO4tHOnZzSyY5ym2kfY=`

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
