#### docker-compose
git clone https://github.com/cyface/docker-saltstack.git
cd docker-saltstack
docker-compose up

docker-compose exec salt-master bash
salt '*' test.ping
docker-compose exec salt-master bashsalt '*' test.ping