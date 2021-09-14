# TFGrid DB Architecture

- Run 9 blockchain nodes which have permission to create blocks.
- Every node actually deploys a full stack, consisting of:
  - The blockchain nodes itself
  - A graphql indexer (postgress + indexer + graphql server)
  - A digital twin proxy (+ message bus)
  - A stellar agent
  - ...

When consensus is needed, all nodes vote on the blockchain. The action is then
processes as soon as 5/9 nodes have agreed.

> more info see [consensus_mechanism](tfgrid:consensus3_principles)