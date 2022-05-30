# The Graph
The graph for SoulBound

## Subgraph Studio
1. Install the Graph CLI
```shell
# NPM
$ npm install -g @graphprotocol/graph-cli

# Yarn
$ yarn global add @graphprotocol/graph-cli
```

2. Deploy to the Subgraph Studio
``` shell
# Run these commands in the subgraph folder
$ graph codegen
$ graph build
```
``` shell
# Authenticate and deploy your subgraph. The deploy key can be found on the Subgraph page in Subgraph Studio.
$ graph auth --studio <DEPLOY_KEY>
$ graph deploy --studio <SUBGRAPH_SLUG>
```

## Example Request

### Docs
https://thegraph.com/docs/zh/developer/querying-from-your-app/

### PRODUCTION QUERY URL (RINKEBY)
https://gateway.testnet.thegraph.com/api/[api-key]/subgraphs/id/AU9Ae18M7qSzasPUAdSvECrAFkjQMCHx5wQDqBhHTTV7

### DEVELOPMENT QUERY URL
https://api.studio.thegraph.com/query/28260/soulbound/v0.0.4

```graphql
{
  souls(first: 5) {
    id
    creator
    soulId
    name
    length
  }
}
```

## Example Response

```json
{
  "data": {
    "souls": [
      {
        "id": "0x046db183639ca3db83c5e3867983139ed51daaac4aae922aa1eb54b439c44e64-32",
        "creator": "0x378f7533041249cd1806550deaa2f73a856c9889",
        "soulId": "2",
        "name": "0x48bed44d1bcd124a28c27f343a817e5f5243190d3c52bf347daf876de1dbbf77",
        "length": "6"
      },
      {
        "id": "0x1386171777b9216d1285aa7c65ba645cace7252ae944d24702ca983aad3a2659-24",
        "creator": "0x3e657631eb0c4715daee88d26dd42c2e999f3c92",
        "soulId": "1",
        "name": "0xc1ed523aa753ea126af382cd6e5d97a38e7401dd519bd4338cc2480409fe6018",
        "length": "9"
      },
      {
        "id": "0x24ccb476707f500086aa1a2befb95543464b1376a3a0993ab5cd0da69b0f082d-35",
        "creator": "0x378f7533041249cd1806550deaa2f73a856c9889",
        "soulId": "3",
        "name": "0xee07dc2598625017c68fbd0a43362728a52940989a308f8b1538307e00c54f9b",
        "length": "7"
      },
      {
        "id": "0x2e29d4718c8464df36a8164d6b5d6d6d5e20163e33034d680a219fdc4620bb9d-16",
        "creator": "0x378f7533041249cd1806550deaa2f73a856c9889",
        "soulId": "1",
        "name": "0x3b13a0e7e4762192a84755e11f97a673eaeeb474796129d6fbf89e05c6e7a8d1",
        "length": "4"
      },
      {
        "id": "0x4e91a2065c06ea5e2594c3de4fdd9e412af80bb5baeb0729de0431f35ce55f31-94",
        "creator": "0x378f7533041249cd1806550deaa2f73a856c9889",
        "soulId": "0",
        "name": "0xd23b00fcb8e0ebd93983a99e8ff85b08f8a67686540afd945aa825219b012b22",
        "length": "3"
      }
    ]
  }
}
```



