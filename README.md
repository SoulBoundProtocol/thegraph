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
https://api.studio.thegraph.com/query/28260/soulbound/v0.0.1

```graphql
{
  souls(first: 5) {
    id
    creator
    soulId
    soul
    name
  }
}
```

## Example Response

```json
{
  "data": {
    "souls": [
      {
        "id": "0x4e91a2065c06ea5e2594c3de4fdd9e412af80bb5baeb0729de0431f35ce55f31-94",
        "creator": "0x378f7533041249cd1806550deaa2f73a856c9889",
        "soulId": "0",
        "soul": "0x110d83ac5380f9698e73ff68e84fd749c569e15a",
        "name": null
      },
      {
        "id": "0x999fdf9ab2395236ee008eb703a9958d4438dd4ad88835ca52639fde424154e4-25",
        "creator": "0x25df6da2f4e5c178ddff45038378c0b08e0bce54",
        "soulId": "0",
        "soul": "0xf6c92dfd6dfc87c3750971060e6206780db620e0",
        "name": null
      },
      {
        "id": "0xd61751e2aaea9314a2ca4537bb645896cefff889e43fc25ce5473f22d152ff5a-9",
        "creator": "0x3317ad9eda6942b5a7be5ba83346c0ea82c3c26c",
        "soulId": "0",
        "soul": "0xd33dbc265522003efdccf267fa6f5a4af9f9398c",
        "name": null
      }
    ]
  }
}
```



