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
