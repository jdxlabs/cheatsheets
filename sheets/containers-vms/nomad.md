# Hashicorp Nomad commands

## Show consul agents (for dynamic clusters)
```bash
consul members
consul operator raft list-peers
```

## Show servers
```bash
nomad server members
```

## Show nodes
```bash
nomad node status
nomad node status -stats <node_id>
```

## Show running jobs
```bash
nomad status
nomad status example
```

## Show logs of an allocation
```bash
nomad logs -f -tail -n 10 <alloc_id>
nomad logs -f -tail -n 10 -stderr <alloc_id>
```

## Show allocations
```bash
curl -XGET http://127.0.0.1:4646/v1/allocations
curl -XGET "http://127.0.0.1:4646/v1/allocations?prefix=<prefix>"
curl -XGET http://127.0.0.1:4646/v1/allocation/<id>
```

## Extract all current allocations in a file
```bash
curl -s -XGET http://127.0.0.1:4646/v1/allocations | python -mjson.tool > extract.json
# inside vim, to know the nb of allocs in a state: :%s/ClientStatus": "running//gn
# or, if you want to list all current states : cat extract.json | grep '"State'
```

## Trigger garbage collector
```bash
curl -XPUT http://127.0.0.1:4646/v1/system/gc
```
