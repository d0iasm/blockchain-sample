# Blackchain Sample

### Start

```
HTTP_PORT=3001 P2P_PORT=6001 npm start
HTTP_PORT=3002 P2P_PORT=6002 PEERS=ws://localhost:6001 npm start
```

### Create a new block

```
curl -H "Content-type:application/json" --data '{"data" : "green"}' http://localhost:3001/mineBlock
```

### Show blocks

```
curl http://localhost:3001/blocks
```
