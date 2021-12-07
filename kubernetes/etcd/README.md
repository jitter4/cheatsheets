#### Standalone - Docker
sudo docker run -d -v /usr/share/ca-certificates/:/etc/ssl/certs -p 4001:4001 -p 127.0.0.1:2380:2380 -p 127.0.0.1:2379:2379 --expose 2379 \
 --name etcd quay.io/coreos/etcd:v2.3.8 \
 -name etcd0 \
 --network=host \
 -advertise-client-urls http://127.0.0.1:2379,http://127.0.0.1:4001 \
 -listen-client-urls http://0.0.0.0:2379,http://0.0.0.0:4001 \
 -initial-advertise-peer-urls http://127.0.0.1:2380 \
 -listen-peer-urls http://0.0.0.0:2380 \
 -initial-cluster-token etcd-cluster-1 \
 -initial-cluster etcd0=http://127.0.0.1:2380 \
 -initial-cluster-state new



export ETCDCTL_API=3
HOST_1=127.0.0.1
ENDPOINTS=$HOST_1:2379

etcdctl --endpoints=$ENDPOINTS member list