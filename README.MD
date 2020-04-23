# Overview

The image contains an astra stream server

#Installation

git clone https://github.com/domorelivelonger/docker-cesbo-astra.git

cd docker-cesbo-astra

#edit file license.txt and add license code
#change port in file docker-compose.yml]


docker-compose up -d

## Image environment variables

| Variable | Default value | Description |
| -------- | ------------- | ----------- |
| ASTRA_PORT | 8000 | Astra admin port | 
| ASTRA_CONF_FILE | /etc/astra/astra.conf | Path to config file | 
| ASTRA_SCRIPT | | Path to script (if need - see FILE option in astra cli) | 
| ASTRA_DISABLE_OUT | 1 | Disable console output if 1, otherwise enable | 

## License

Without a license file astra will not start

Add license to container on path `/etc/astra/license.txt`

Buy license or get trial:

https://cesbo.com/orders/software/astra/buy/

----
Docker and Docker-compose installation

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version
