# rabbitmq-cluster-haproxy

## TO BUILD IMAGES 

```
cd /home/stgappser/App/rabbitmq/clusters/docker-images/config 
docker build -t rabbitmq-node -f ../rabbitmq/Dockerfile . 
docker build -t haproxy-rabbitmq-cluster -f ../haproxy-ssl/Dockerfile . 
```

## TO SPIN OFF HAPROXY-RABBITMQ-CLUSTER 

```
cd /home/stgappser/App/rabbitmq/clusters/docker-compose 
docker-compose up -d 
```

## FOR REF 
### (FULL CHAIN) PEM 

```
openssl rsa -in client_key.pem -out client.key 
openssl rsa -in ca_key.pem -out ca.key 
openssl rsa -in server_key.pem -out server.key 

cat chained_ca_certificate.pem ca.key > ca_fullchain.pem 
cat chained_ca_certificate.pem client.key > client_fullchain.pem 
cat chained_ca_certificate.pem server.key > server_fullchain.pem 
```

### TLS-GET SETUP 

```
apt update 
apt install software-properties-common 
apt-get install python3.7 
python3.7 --version 
apt install git -y 
git --version 
apt-get install build-essential -y 
git clone https://github.com/michaelklishin/tls-gen.git 
docker cp 06d5e9468935:/tls-gen/ ./ 
```