# Getting Started
### Table of Contents
- [How Does Arken Work?](#how-does-arken-work)
- [Contribute Free Disk Space to Arken](/contributing/contributing.md)
  - [Installation](/contribute/installation.md)
  - [Configuration](/contribute/configuration.md)
  - [(Optional) Node Stats & Alerts](/contribute/stats-and-alerts.md)
- [Upload Data to Arken](/upload/upload.md)
  - [Signing up for GitHub](/upload/github.md)
  - [Install Ark (the Arken Command-line Client)](/upload/installation.md)
  - [Tutorial](/upload/tutorial.md)
  - [Usage](/upload/usage.md)
  - [Configuration](/upload/configuration.md)
- [Frequently Asked Questions (FAQ)](frequently-asked-questions.md)
- [Support](support.md)

## How does Arken Work?
Arken makes use of the Interplanetary Filesystem ([IPFS](//ipfs.io)) to construct a peer-to-peer [mesh network](https://en.wikipedia.org/wiki/Mesh_networking) between nodes. Utilizing this network along with a [cluster manifest](https://github.com/arken/core-manifest) each Arken node builds up an internal database of files and the number of times they are replicated across the cluster. When a node encounters a file with fewer replications than the minimum cluster threshold (e.g. the Core Cluster makes 5 replications) it copies the file to itself and begins providing the file to the cluster.

Since Arken nodes are able to distribute files directly between each other they are able to minimize network costs and remove a central point of failure/attack. Moreover, Arken clusters aren't dependent on any one organization. Even if the Arken project is forced to shutdown, the cluster (and data within it) will remain online through nodes hosted by the community.

## Exploring Data Already in the Archive
You can download data from the Core Cluster either by using [Ark: the Arken Command-line Client](/upload) or by going to [files.arken.io](https://files.arken.io).
