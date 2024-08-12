
<p align="center">
  <img src="https://raw.githubusercontent.com/mekong-labs/NodeGuide/main/MEKONG.png" width="30%" height="30%"/>
</p>


## Who Are We
[Lavender.Fives Nodes](https://www.lavenderfive.com/) is a team dedicated to bringing secure 
infrastructure and pragmatic software solutions to over 50 proof-of-stake blockchains. With 15+ years 
in software development and system administration experience we guarantee safety for the funds of 
over **100,000 delegators**. This makes us one of the most trusted Proof of Stake validators.

Our team is able to maintain industry-leading uptime by using dedicated servers around the world, 
multiple 24/7 alerting systems, and a remote signing solution with always-ready backups. 

We differentiate ourselves through our public infrastructure like API nodes and IBC relaying while 
simultaneously dedicating ourselves to wholesome and holistic governance and community engagement. We serve the
projects we validate by authoring documentation for fellow validators, improving infrastructure security
by providing automated setups, developing new features like hardware wallet support, and helping squash
code bugs before they become an issue.

## Infrastructure

The following diagram outlines the high-level approach to our network topology which optimizes for 
highly available, redundant infrastructure for blockchain projects:

![Network Architecture drawio (1)](https://github.com/LavenderFive/.github/assets/9121234/82f476af-3be2-4159-97a4-45d2fd4aed34)

### High Level Points:
- At the most basic level we utilize bare metal servers with a minimum of 2 full nodes per network.
- Each server is with a different provider at a different geographical location.
- Secure, high bandwidth, encrypted connectivity is in place between data center networks and public nodes
  to allow for node relocation, data duplication, and encrypted communication across sites.
- Secure, out of band, multi-factor based remote management is in place for 24x7 monitoring and support by Lavender.Five team.
- All server access is gated behind hardware keys (ie. Yubikey).
- 24x7 event escalation and alarm notification provided by PagerDuty to a **globally diverse team**.
- All validator/signing keys are stored locally on an offline, encrypted hard drive in addition to encrypted cloud storage.
- Where applicable, we utilize remote MPC/RAFT signers such as [Web3Signer](https://github.com/ConsenSys/web3signer/), [SSV](https://ssv.network/),
  or [Horcrux](https://github.com/strangelove-ventures/horcrux).
- Where applicable, all operator keys are secured using a Ledger or other hardware key.

### Remote/MPC Signing Topology

![157145772-8557b4b5-a0cc-4073-8834-86afda1900fc](https://github.com/LavenderFive/.github/assets/9121234/fca0d230-9dca-4f5f-a66d-2a069184c92e)


## Monitoring
For every node we manage, we utilize both Prometheus and Zabbix to consume metrics for redundancy. Utilizing Grafana
we expose those metrics for us to review. An example of one of our dashboards can be seen 
[here](https://github.com/LavenderFive/aptos-monitoring). We also have alerts set up 
through both Zabbix and Prometheus so that if a node is having issues we will immediately be notified via Pagerduty to
Slack, Discord, and direct push notifications to our phones. 

<p align="center"><img src="https://github.com/LavenderFive/.github/assets/9121234/49fd2ed2-f674-4eb8-abdf-d33dae13bdcc" /></p>

## Our Involvement

We also contribute greatly to each ecosystem we're in. 

### Open Source Tooling

- We provide open source tooling for every network we support, using Aptos as an example:
  - Ansible Playbook for [running nodes](https://github.com/LavenderFive/aptos-ansible)
  - Complete monitoring solution using [Prometheus, Grafana, and built-in alerts](https://github.com/LavenderFive/aptos-monitoring)
- We are core maintainers of:
  - [Cosmos Chain Registry](https://github.com/cosmos/chain-registry) 
  - The best monitoring solution for Cosmos-based nodes, [Tenderduty](https://github.com/blockpane/tenderduty)
  - [Tendermint slashing refund script](https://github.com/LavenderFive/slash_refunds_tendermint)
- Other Ansible Playbooks
  - [Horcrux](https://github.com/LavenderFive/horcrux-ansible)
  - [Server Setup](https://github.com/LavenderFive/secure-server-setup-ansible)

### Services

- We provide [**public 2x daily pruned snapshots**](https://services.lavenderfive.com/) for every network in order to help other nodes spin up
- We provide **public 2x daily addrbook backups** for every network to help with peering
- We provide **public RPC, API, and gRPC endpoints** for every network we have a presence on serving over 600M queries a month
- We maintain **state sync snapshots** for every network we validate
- We provide a public **seed node** for every network we validate
- **Relaying**: 
  - We are one of the most prolific relayers in the ecosystem, and have helped many relayers get their start (see the docs below)
  - We process over 400,000 IBC transactions a per month across 30+ networks and 200+ channels. - [Data](https://relayers.smartstake.io/relayer/F87ADDB700C0CC94)

### Misc Contributions

- We have added validator ledger support to many networks, including Injective protocol
- We wrote the Gentx documentation for [Kujira](https://github.com/Team-Kujira/networks/pull/5), Defund, Odin, Chihuahua, Dig, and more
- We've either written or edited every document for [Secret Network](https://docs.scrt.network/)
- We write documentation to help other node runners:
  - [Relaying](https://docs.scrt.network/relayers/setting-up-hermes.html)
  - [Setting up TMKMS](https://gist.github.com/dylanschultzie/c7c4eed531df0f004a50c5395e1604b3)
  - [Horcrux](https://gist.github.com/dylanschultzie/0a0b10cf695749f9697197759e7b12ec)
  - [Raising the Security Floor of the Cosmos](https://medium.com/@lavenderfive/raising-the-security-floor-of-the-cosmos-2467f5e71966)
- We commonly create proposals for networks:
  - [Osmosis](https://commonwealth.im/osmosis/proposal/discussion/2487-proposal-discussion-signaling-proposal-for-scrt-incentivized-pools)
  - [Secret](https://secretnodes.com/secret/chains/secret-4/governance/proposals/93)

## A Showing of Networks
A small selection of the networks we support include:
- Aptos
- Near
- Secret Network
- Cosmos Hub 
- [and many more!](https://www.lavenderfive.com/)

---

Finally, be sure to catch members of the Lavender.Five team on [Game of Nodes](https://twitter.com/gameofnodes_)!
Broadcast live on [YouTube](https://www.youtube.com/channel/UCWsyvi27z0i2bmOyBw1MAKA/videos) and 
[Twitter](https://twitter.com/gameofnodes_) every Wednesday at 21:00 UTC.

Find [Game of Nodes](https://rss.com/podcasts/game-of-nodes/) in your favorite Podcast Player.