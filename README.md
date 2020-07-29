# k8s statefullset redis v6 in-memory with io-threads
Tips for high load production: use type vm with high cpu speed for gke node-pool,redis better use high cpu speed, not more core cpu,
for example N2 machine types base frequency 2.8 GHz and a sustained all core turbo 3.4 GHz
![alt text](https://i.imgur.com/4QF2Aq6.png)

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
