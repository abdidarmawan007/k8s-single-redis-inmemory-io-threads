# k8s redis v6 statefullset in-memory with io-threads

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

![alt text](https://i.imgur.com/kx2OYA1.png)
