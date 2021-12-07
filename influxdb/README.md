#### Start
sudo systemctl stop influxdb && sudo systemctl start influxdb

curl -XPOST "http://localhost:8086/query" --data-urlencode "q=CREATE USER root WITH PASSWORD 'root' WITH ALL PRIVILEGES"


#### Install Client
sudo apt install influxdb-client