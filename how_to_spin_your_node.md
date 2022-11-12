To launch a node on the Ethereum blockchain, there are several possibilities. 

Local or cloud: 
What are the pros and cons? 

How much space do you need? 

Choosing the approach

The first step in spinning up your node is choosing your approach. 

To start, you have to choose:
- the Ethereum client (software)
- environment
- parameters you want to start with.

Client Settings

Before starting the node, you decide:
- network to use.
- sync mode (download & validating method). 

Most important things to consider:
- disk space.
- sync time the client will need.

For testing, you can use a testnet network.
Local or cloud?

The first choice to make is whether to rely on the cloud or launch the node on your own machine.

There are various options for both cloud and local.

Eth clients don't require special hardware: they can run on consumer-grade computers.

Let's see the pros/cons:
Cloud pros/cons

✅Providers offer high server uptime, static public IP addresses
✅ Getting a dedicated or virtual server can be more comfortable than building your own

❌ You need to TRUST a third-party/server provider
❌ High price to rent a server mainly because of storage

Services for deploying nodes

If you are looking for a cloud solution, in addition to many traditional cloud computing providers, there are also services focused on deploying nodes. 

Examples:
- Alchemy
- Infura
- QuikNode

Local pros/cons

✅More trustless and sovereign approach.
✅One-time investment.
✅Buy pre-configured machines option.
❌You have to physically prepare, maintain, and troubleshoot the machine.
Preconfigured Local Nodes

A censorship-resistant, decentralized network should not rely on cloud providers. 

It's healthier for the ecosystem if you run your own node on hardware. 

Preconfigured machines options:

- DappNode

- Avado

Local option HW requirements

💿Disk space:
SSD is strongly recommended.

🖥CPU: 
Most of the clients can run on a single-board computer with ARM. 

🌐CONNECTION:
An unmetered connection is recommended.
Operating systems

All clients support:
- Windows.
- macOS.
- Linux.

You can run nodes on regular desktop or server machines with the OS you prefer.

⚠ Update your OS to avoid issues & security vulnerabilities!

Steps to spinning up the node

1. Getting the client software
2. Starting the client
3. Using the client
4. Reaching RPC
5. Operating the node

Getting the client software

The first step is to download an executable app or installation package for your OS/architecture and verify signatures and checksums.

All the clients are open source: 
- Geth
- OpenEthereum
- Nethermind
- Besu
- Erigon

⚠ OpenEthereum is deprecated

efore starting, check that:

- OS is updated.

- Memory & CPU are not halted by other programs.

- Router & Firewall accept connections on listening ports. (Default: port 30303 for TCP/UDP).

- There's enough disk space for network & sync mode.

Starting the client

Run your client on a testnet first (e.g. Geth light).
Check the docs!
Declare settings that aren't default. 

Client execution will:
- initiate core functions
- chose endpoints
- start looking for peers
- start sync

Then the blockchain data will be available

Clients RPC API endpoints

They can be used to interact with the network by:
- Manual call (curl).
- Attaching a console.
- In-app implementation.

Different implementations, but there's a standard JSON-RPC

🦊MetaMask lets you run a local blockchain instance and connect to it.

Reaching RPC

Default JSON-RPC port: 8545.

By default, the RPC interface is only reachable on 
localhost.

To make it remotely accessible, change the address to  0.0.0.0. 

⚠ This will let anyone on the internet control your node!

Don't get hacked!

Malicious actors can access:
- bring down your system
- steal your funds.

Basic Solutions:
- geth: declare modifiable methods with a flag
- host access to your RPC interface by pointing the service of the web server, to your client's local address.

Tor Onion Service

It's the most privacy-preserving way to set up a publicly reachable endpoint:
- Install tor
- Edit torrc config: enable hidden service with client RPC address/port
- Restart to get hidden service keys & hostname 

RPC will be reachable on a .onion hostname.

Operating the node

This is just the beginning!

Each node must be maintained, updated, and monitored. 

We also want to add features and services that interest us.
