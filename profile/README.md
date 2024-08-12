
<p align="center">
  <img src="https://raw.githubusercontent.com/mekong-labs/NodeGuide/main/MEKONG.png" width="30%" height="30%"/>
</p>


## Who Are We
[Mekong Labs](https://mekonglabs.tech/) is a team dedicated to bringing secure 
infrastructure and pragmatic software solutions to over 35 proof-of-stake blockchains. With 10+ years 
in software development and system administration experience we guarantee safety for the funds of 
over **1000 delegators**. This makes us one of the most trusted Proof of Stake validators.

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

![Network Architecture drawio (1)](https://raw.githubusercontent.com/mekong-labs/NodeGuide/main/infra.jpg)

### High Level Points:
- At the most basic level we utilize bare metal servers with a minimum of 2 full nodes per network.
- Each server is with a different provider at a different geographical location.
- Secure, high bandwidth, encrypted connectivity is in place between data center networks and public nodes
  to allow for node relocation, data duplication, and encrypted communication across sites.
- Secure, out of band, multi-factor based remote management is in place for 24x7 monitoring and support by Mekong Labs team.
- All server access is gated behind hardware keys (ie. Yubikey).
- 24x7 event escalation and alarm notification provided by PagerDuty to a **globally diverse team**.
- All validator/signing keys are stored locally on an offline, encrypted hard drive in addition to encrypted cloud storage.
- Where applicable, we utilize remote MPC/RAFT signers such as [Web3Signer](https://github.com/ConsenSys/web3signer/), [SSV](https://ssv.network/),
  or [Horcrux](https://github.com/strangelove-ventures/horcrux).
- Where applicable, all operator keys are secured using a Ledger or other hardware key.

### Remote/MPC Signing Topology

![157145772-8557b4b5-a0cc-4073-8834-86afda1900fc](https://raw.githubusercontent.com/mekong-labs/NodeGuide/main/ip.png)


## Monitoring
For every node we manage, we utilize both Prometheus and Zabbix to consume metrics for redundancy. Utilizing Grafana
we expose those metrics for us to review. We also have alerts set up 
through both Zabbix and Prometheus so that if a node is having issues we will immediately be notified via Pagerduty to
Slack, Discord, and direct push notifications to our phones. 

<p align="center"><img src="https://raw.githubusercontent.com/mekong-labs/NodeGuide/main/monitor.png" /></p>

## Our Involvement

We also contribute greatly to each ecosystem we're in. 

### Open Source Tooling

- We are core maintainers of:
  - [Cosmos Chain Registry](https://github.com/Mekong-labs/NodeGuide) 
  - The best monitoring solution for Cosmos-based nodes, [Tenderduty](https://github.com/blockpane/tenderduty)

### Services

- We provide [**public 2x daily pruned snapshots**](https://mekonglabs.tech/services/) for every network in order to help other nodes spin up
- We provide **public 2x daily addrbook backups** for every network to help with peering
- We provide **public RPC, API, and gRPC endpoints** for every network we have a presence on serving over 600M queries a month
- We maintain **state sync snapshots** for every network we validate
- We provide a public **seed node** for every network we validate
- **Relaying**: 
  - We are one of the most prolific relayers in the ecosystem, and have helped many relayers get their start (see the docs below)
  - We process over 400,000 IBC transactions a per month across 30+ networks and 200+ channels. - [Data](https://relayers.smartstake.io/relayer/F87ADDB700C0CC94)

## A Showing of Networks
A small selection of the networks we support include:
- xai
- Cosmos Hub 
- [and many more!](https://mekonglabs.tech/)