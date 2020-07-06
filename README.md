# k8s redis 6 statefullset in-memory with io-threads

## create redis k8s
```
kubectl apply -f redis.yaml
```
## test benchmark
```
redis-benchmark -h redis -t get,set -n 1000000 -q
SET: 50231.06 requests per second
GET: 50035.02 requests per second
```
