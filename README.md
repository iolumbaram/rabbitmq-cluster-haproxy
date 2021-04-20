# rabbitmq-cluster-haproxy

##TO BUILD IMAGES
'''
cd /home/stgappser/App/rabbitmq/clusters/docker-images/config
docker build -t rabbitmq-node -f ../rabbitmq/Dockerfile .
docker build -t haproxy-rabbitmq-cluster -f ../haproxy-ssl/Dockerfile .
'''

##TO SPIN OFF HAPROXY-RABBITMQ-CLUSTER
'''
cd /home/stgappser/App/rabbitmq/clusters/docker-compose
docker-compose up -d
'''
