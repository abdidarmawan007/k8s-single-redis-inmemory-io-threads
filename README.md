# k8s statefullset redis v6 in-memory with io-threads

## create redis k8s
```
kubectl apply -f redis.yaml
```
## test benchmark
```
redis-benchmark -h redis -t set,get -q
SET: 91827.37 requests per second
GET: 93196.65 requests per second
```
