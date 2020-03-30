# Sarafan network

Version: 1.0

Sarafan project aimed to provide secure and safe way to publish and consume publications.
It is aimed to provide opensource client and server apps for end-user and, to build and to 
support content publishing network infrastructure.

It is based on widely used and well known technologies like Tor, BitTorrent and Ethereum,
instead of reallying hyped and untested technologies with undiscovered holes and problems.

## Abstract

Do you own the content you publishing on the web? Simple answer is "No". 

You are agree with tons of agreements and you loose your ownership: web site owner can ban you, 
delete your content, change it in unacceptable manner or try to sell it (so you will be banned 
at the court this time if you'll try to pretend on the ownership). They are telling you what you
should write and what you shouldn't.

As a reader you may face with another class of problem: fraud. There are a lot of reason even
biggest informational agencies may want to change what they said. It is more or less acceptable if 
it was unintentional mistake. But there is a chance that someone tries to hide the truth (published
by mistake) or manipulate your meaning. For example: they can tell you that company A official said
that they will buy company B in two weeks. You are buying B stocks and are waiting for the moon.
The news agency just add "never" word to "will buy" after the hour and you lose your money.
But someone from company B stock owners will raise them, you know. It is deadly simple scheme if you
are the owner of the data.

The other side of that sad story is a privacy. Even when you using tor browser over VPN your are
not safe from deanonymization. It is important in anti-human regimes like in North Korea, China,
Russia etc. There are a lot of resources involved to find the meaning source and control or isolate 
it as fast as possible. You became a target for them if you read or publish a content they didn't
accept. Or if your meaning is not match what they expecting. 

It might be dangerous for the whole world.

North Korean scientist working on another biological weapon may inform a general public about
coming disaster. He can also publish information about antidote production. If he will exactly
know that he will be not compromised. It will cost him a life in most cases. Edward Snowden was
a security IT specialist when he was trying to publish his information. In the US. What about 
North Korean biologist?

China doctor seeing emergence of a new epidemic may tell us about situation without being caught
and silenced.

Fisherman seeing explosion near Arkhangelsk or an ecologist seeing increased radioactivity or
doctors found their patients irradiated. All of them are sources of very important information
about global disaster. Their governments will do what they can to stop the spreading of such
information because they may lost the control.  

You can try to work with wikileaks, for example. But no one give you a guarantee that 
it is not an another KGB media project. They will filter out inconvenient information and will 
publish only information beneficial for them. And we met information ownership and 
mutability problem again.

Okay, you just found those guys running non-KGB wikileaks. But they could be also caught too.
It isn't the only reason to shutdown website and format hard drives.

There is a special problem with independent journalists. They facing the whole problems above. Also,
publication is their work. They need eat, wear, rent a flat. To tell you the truth. A lot of
journalists sells their opinion. We should support the right side or we will die from another 
pneumonia.

There is also a problem to find a stable knowledge source in dark web. A lot of sources disappearing
every day. Working with a content in distributed manner and providing user-friendly client app 
we may help to save us published information too.

Sarafan will help to solve this problem.

## Project goals

The main Sarafan project goal is to provide private and safe way to publish and consume content 
for all over the world.

Other goals:

* Deploy and maintain sarafan delivery network
* Publish strict Sarafan publication format specification

Open-source products delivery goals:

* Sarafan node app
* Personal app to access Sarafan network
* Community platform ("immortal web-site")

## Sarafan solution

Sarafan solution evolves multiple time-proven technologies like BitTorrent, Ethereum 
and onion routing.

Sarafan uses Tor as a private transport and Ethereum as a central content registry. Also, Sarafan
uses Ethereum as a payment system for clearing between content authors, network peers and reader.

We use some technologies from BitTorrent like DHT to search nodes with desired content but in 
a more secure way: all communication is hidden in Tor overlay.

The main product of Sarafan is Sarafan App. It is an open-source cross-platform end-user app 
to access Sarafan delivery network. User can securely read and publish content on blockchain directly 
without any intermediates. It is also possible to run it as a web-site in tor network for
personal use (it is not a high-load solution, it is standalone and minimal-dependency).

The key infrastructure component is Sarafan Node. It is an open-source software aimed to listen
Sarafan contract for events, to download and to share publications content. Node owner rewarded
for storing content matching his node id.

The big-deal of Sarafan project funding is to deliver open-source community platform.
It should allow to deploy immortal community site for flowers lovers, mini-cooper owners,
Wall-mart customers etc. Deployed first time this site will be never forgotten: whole content
will be stored on sarafan network and can be easily restored. Anyone can run replicate 
or revive site from the ground if its first owner concerned to shut it down. It is also possible 
to access community with standalone Sarafan App but without community-specific features. 

SRFN token will be issued and utilized for reader-published-storage clearing and fees.

## Sarafan token

Sarafan token will be issued and raised funds will be used for project development including 
developers salary, initial network infrastructure and marketing.

Token will be used for Sarafan content delivery network fee and clearing between nodes.

1 SRFN is equal to storing of 1Mb per month at 10 replicas: 

* publisher will pay fee according to published content size
* sarafan node owner will got tokens for publication based on content rarity and number of nodes
    serving this file same time

## Sarafan content delivery network

Sarafan content stored in fully distributed manner.

Every Publication in the network is identified with a hash called "magnet". It's like in BitTorrent
but there is no encoded content it is just a content file hash.

Each node in the network has a random ID which is in the same address space as magnets. Files
are distributed to the nodes with nearest ID to content hash. The distance is not a geographical 
term: it is just a XOR between two hashes (which are a bytes representing big integer). 

Nodes will receive fees according to a distance to a stored files hashes and their rarity.
Validation node will count 10 nearest nodes reporting files stored as fee targets and split half
of the fee between of them. The other half will be distributed against all other nodes reporting
files stored. If there are less than 20 nodes storing the same file, fee will be distributed equally
between all of them. So, the storing of rarest and nearest content is a node main goal.

The main way node receive content is to listen contract for events and search new content
matching node id using DHT. Publication can be also uploaded by client directly: node check
file hash and check if hash published using Sarafan contract, and serve it than.
   
All communications between nodes hidden in Tor overlay. But you should use VPN to ensure your
privacy: your ISP will know that you use Tor without VPN (but will not know what you see, anyway).
There is also a reason to host nodes as hidden services: there is no exit node so there is no
way to attack you by measuring transmission latency. Sarafan nodes, also, designed to be short-living 
and there will be no time to correctly identify its location.

### Publication fee

Publication fee is based on content size and measured in SRFN tokens.

1 token equal to storage of 1Mb for 1 month on 10 replicas. Publisher can increase storage time
increasing the fee proportionally.

Fee is fully transferred to peering network for clearing.

### Publications award system

There is a motivation system for content authors. User can send tokens to the publication author 
to award author and increase content storage time.

Award amount will be split between peering contract and publication author as 1:1. It will allow to
increase content storage time. So the minimal award is 2 SRFN (~0.03).

### Storage reward

Sarafan nodes owners are motivated to store publications content by storage fee.

Peers should commit their storage with minimum interval of 12 hours. Special validation peers owning 
more than 10M SRFN will validate commitment and generate `Verify` or `Reject` contract event according 
to data validity.

`Verify` event contains `value` which defines amount of committed data the network 
should pay. There is multiple reasons to not count stored content:

* content too old
* content not on chain
* content data is wrong
* content hash is too far from node hash
* node didn't passed proof of storage check
* node didn't respond in committed interval

Peer reward is based on how close stored content to its id and how many peers
reported this content piece stored. So it is a peer interest to listen content contract for 
closest publications and instead of waiting publisher to push content try to locate and 
download content package first. Peer can also listen for network topology changes and download
new payed content or remove unpayed content from storage.

### Validation node

There is special nodes in content delivery network who's main task is to verify commitments from
other nodes. Owner of such node should own at least 10M SRFN to be allowed to send verification 
or rejection.

Validation nodes are equal between. So the approval process is looks like a voting: every node
can send its own choice. Approvals and rejections are counted in amounts of SRFN tokens validation 
node owns. Every time node approve or reject commitment appropriate amounts will be added to the
accumulated value.

There is also a `value` for every verification. It express amount of data that should be payed to peer.
Validation node should calculate it based on whole content index and should take in count individual
content file rarity.

After 7 days from commitment, content author can request payout. Payout is possible only in case
of approval amount is greater than amount of rejection. Than, `averageValue` is used as ratio for
calculated payout sum. Every `Verify` have a different weight in value, based on validation node
weight.

### Proof of storage

Sarafan node store and support its own Merkle hash tree of all content. The root hash of that tree
is passed to storage commitment. Any node in network can download a small piece of any content
file and check if it is belong to root hash by requesting a solution from node (full path from chunk 
hash to root node hash).

The node can't generate full hash for limited time so it is mostly impossible to download content
and hash it on-promise (without using storage for a committed time).

Also it is possible to proxy content from single node and got network fee multiple time for single
file instance. It can be solved by building Merkle hash tree using file content encoded with node id.
So the hash tree will differ for the same file on different nodes. It will prove storage instance
identity.

### Proof of time

There is no clear way to ensure that node store and serve content for the whole committed time
except polling and evaluating checks rapidly. Validation nodes will do so in reaction to `Commmit`
event. It is why nodes should submit commitments so frequently.

## Alternative solutions

There are a number of alternatives to publish your content but most of them are a transport layer
solution. Sarafan gets some technologies from each of them to compound advantages and disadvantages
of each technology and wraps them in user-friendly app.

But lets a look at them and look at what we got from their experience. 

### Traditional web site

We are trying to create something like distributed reddit, so we should look at traditional 
web sites first.

Traditional web sites, running on modern browsers may concurrent with desktop applications.

We should use most of the tech stack for our apps from them:

* HTTP(s) as content transport
* UI (html, css, js)
* PWA as possibility to create mobile app working everywhere.

But we should limit allowed features to prevent network members to affect privacy of each other.

Advantages:

* agile UI
* easy access
* easy development (low cost)
* low storage cost (0,02 USD per GB per month)

Disadvantages:

* publisher privacy
* readers privacy
* storage owner owns content (can remove or change it)
* security

### Tor website

Migrating the site to the Tor network will solve many privacy problems. But you will face with
a void. There is a deorganized space without any fresh index of available data. Information
sources are disappearing rapidly.

We can use tor network to distribute content privately. But opening an onion site is a brave thing.
You should exactly know what you are doing. Sarafan defines a fixed and safe exchange formats and 
targeted only for specific information (publications feed), so it is safer than just using Tor.

Advantages:

* agile UI (web)
* easy access

Disadvantages:

* complicated hidden service deployment process (needs additional expertise)
* a lot of unsafe sources (js can break your privacy)
* unstable sources (few long-living sites, boards the most)
* looks like a 200x

### On-chain

The direct ideas with a blockchain is to store your data in transactions. It is possible but
it is cost too much: 76,000 USD per GB. It is for a whole blockchain life.

Sarafan stores critical data on-chain but uses a peering network to distribute content itself.

It is important that storage nodes have a strict contract with a network. Ethereum contract
used in Sarafan for content index, fees (token) and content codes clearing.

Advantages:

* no p2p network
* content will be available while Ethereum network exists

Disadvantages:

* high storage cost
* publishing privacy (can be fixed)

### BitTorrent

BitTorrent will help us with a base for peering network. We use something like DHT and magnet
links in Sarafan.

BitTorrent has lack of privacy. But it is related to its high throughput (which has no such
importance at Sarafan scale).

Advantages:

* large files
* free storage
* private trackers can be used to gather fee

Disadvantages:

* no magnet index
* no storage guaranties
* requires self-hosting first
* no UI (can be fixed with app)
* no storage/seeding guaranteed
* reader and publisher privacy problems
* can't be used with Tor (requires UDP)

## Economy

Sarafan economy is based on fact that cloud-storage of 1Gb of data will cost you around 
0.02 per month (as of Jan 2020). Target token price is $0.015. 1 SRFN is equal to storage of 1Mb
per month. It can be increased according to contract conditions but 1 is minimal value.
It is guarantee to storage peers that it will be always valuable for them.

We will store 15 copies of 1Mb content for 1 month for 1 SRFN (~$0.015). This time interval 
of guaranted storage can be extended with publication awards by the readers. But it is not the end 
of publication life. There are a lot of nodes serving Sarafan content for free. So the unused fee 
will be used to increase average content life.

Storage peer will receive reward based on distance between its random id and content hash.
10 nearest nodes will receive 1/10 of reward. Storage of merkle hash files is included.

We need less than $200,000 to finish what we want. So we are starting our ICO.

### ICO

Token emitted by sending ethereum to SRFN token contract address `0x957D0b2E4afA74A49bbEa4d7333D13c0b11af60F`.
There is no need for KYC because we are for privacy.

Initial token price will be ~$0.0001. Target price is ~$0.01-$0.02.

Next stages will be started automatically based on the tokens sold:

* before 50M sold — 1 ETH = 1000000 SRFN
* 50M - 200M sold — 1 ETH = 100000 SRFN
* 200M - 400M sold — 1 ETH = 10000 SRFN

After 400M of tokens will be sold the price will be fixed at 1 ETH for 1000 SRFN.
So the tokens should be bought on exchange instead of direct transfer to token contract.
Direct transfer will be available for emergency cases.

Developers initially receive 300,000,000 tokens for:

* controlling network (validation etc.)
* gifting to human right orgs, media etc.
* reward
* first dapp purposes (including marketing)

## Roadmap

### Q2 2020

We are currently working on node prototype and on deploying delivery network to life. It is
cost us a lot so we are starting the ICO.

* Contract deployment
* Sarafan delivery network deployment (at minimum capacity of 1Tb)
* Sarafan Node beta
* Sarafan App alpha
* Content bundle spec

### Q3 2020

We should focus on secure client app development and sarafan node stabilization.
Also we should start work with media as soon as possible (with beta of client app).

* stable p2p network and node app
* Sarafan Node 1.0 release
* Sarafan App beta
* Sarafan Community Server alpha
* Marketing

### Q4 2020

In Q4 the main point is community server: the webapp that can serve multiple (30k) users and
connecting them to the Sarafan network. So the anyone can run copy of such website if something
going wrong.

* Sarafan App 1.0 release
* Sarafan Community Server beta
* Public installation of community server

### Q1 2021

The Q1 2021 should be about stabilization and token listing.

* Community Server 1.0 release
* SRFN token listing

### Q2-Q3 2021

* Marketing
* Specification changes
* Community server and client app improvements

### Q1 2021 and next

Starting from Q1 2021 the team should disappear. All possible funds gathered from token sale
will be transferred for charity and token burning. Products will be supported by community. 
Changes in this part will be announced and discussed with token holders if needed.
