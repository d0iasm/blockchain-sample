# Blackchain Sample

### Start

```
HTTP_PORT=3001 P2P_PORT=6001 npm start
HTTP_PORT=3002 P2P_PORT=6002 PEERS=ws://localhost:6001 npm start
```

### Create a new block

#### From 3002 to 3001

```
curl -H "Content-type:application/json" --data '{"data" : "green"}' http://localhost:3001/mineBlock
```

#### From 3001 to 3002

```
curl -H "Content-type:application/json" --data '{"data" : "blue"}' http://localhost:3002/mineBlock
```

### Show a latest image

```
curl http://localhost:3001/blocks
```

### Add peer

```
curl -H "Content-type:application/json" --data '{"peer" : "ws://localhost:6001"}' http://localhost:3001/addPeer
```

### Query connected peers

```
curl http://localhost:3001/peers
```
