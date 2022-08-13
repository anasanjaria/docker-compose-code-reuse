# Local mongodb cluster
Set up mongodb cluster with 1 primary and 2 replicas. I used this tutorial [1] for setting up local mongodb cluster.

My focus is not on setting up mongodb cluster but on code reusing in docker-compose using YAML feature called `anchors`.
As per this tutorial [2][3], under section `EXTRA YAML FEATURES`

> YAML also has a handy feature called 'anchors', which let you easily duplicate
> content across your document. Both of these keys will have the same value:

```
anchored_content: &anchor_name # This string will appear as the value of two keys.
other_anchor: *anchor_name
```

## How to start local mongodb cluster?
- Run the following command
```
docker-compose up -d
```
- After 5s, run the following command to form cluster.
```
docker exec mongo-test-1 /scripts/init.sh
```

## Resources
[1] https://blog.tericcabrel.com/mongodb-replica-set-docker-compose/

[2] https://learnxinyminutes.com/docs/yaml/

[3] https://stackoverflow.com/a/45805673