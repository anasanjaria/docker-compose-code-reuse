# Local mongodb cluster
Set up mongodb cluster with 1 primary and 2 replicas.

## How to start local mongodb cluster?
- Run the following command
```
docker-compose up -d
```
- After 5s, run the following command to form cluster.
```
docker exec mongo-test-1 /scripts/init.sh
```
