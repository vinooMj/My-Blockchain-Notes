Files are stored inside IPFS Object which are upto 256kb in size. IPFS object can also contain link to other ipfs objects. Files that are larger than 256 kb, an image or video. those are split up into multiple ipfs objects that are all 256 kb in size and afterward, the system will create an empty IPFS OBJECT that links to all other pieces of the file. Each object gets hashed and given a unique content identifier (CID), which serves as a fingerprint. This makes it faster and easier to store the small pieces of your data on the network quickly.

Because IPFS uses content-based addressing, once something is added cannot be changed. it is an immutable data store much like a blockchain. IPFS can help deliver content in a way that can save you considerable money.

IPFS removes duplications across the network and tracks version history for every file. IPFS also provides high performance and clustered persistence.

Since IPFS supports versioning of your files. let's say u want to share an important file with someone over the ipfs. IPFS will create a new commit object. it is very basic. it just tells ipfs which commit went before it and it links to the IPFS object of your file. let's say after a while u want to update a file. you just add updated file to the IPFS network and the software will create a new commit object for your file. this commit object now links to the previous commit. this can be done endlessly. IPFS will make sure your file plus its entire history is accessible to the other nodes on the network.

Biggest problem with IPFS is keeping files available. every node on the network keeps a cache of the files that it has downloaded and helps to share them if other people need them. But if a specific file is hosted by 4 nodes and if those nodes go offline, then those files become unavailable and no one can grab a copy of it. there are two possible solutions to this problem.

Either we incentive people to store files and make them available or we can proactively distribute files and make sure that there are always a certain amount number of copies available on the network. that is what exactly file coin intends to do. File coin is created by the same group people that have created IPFS. it is basically a blockchain built on top of IPFS that wants to create a decentralized market for storage. if you have some free space you can rent it out to others and make money from it in the process.

IPFS and the blockchain are a perfect fit. You can address large amounts of data with IPFS and place the immutable, IPFS links into a blockchain transaction. This timestamps and secures your content, without having to put the data on the chain itself.

When you upload something, the file is chunked by ipfs and stored in your cache folder (.ipfs).

If you check the file existance on another peer of the network (say the main gateway, ipfs.io) that peer requests the file from you and caches it too.

If later you switch off your daemon and you can still see the file on the gateway it's probably because the gateway or some other peer on the web still has it cached.

When a peer wants to download a file but it's out of memory (it can no longer cache), it trashes the oldest used files to free space.

If you want to dive deep into the technology, check first these fundamentals:

how git works
decentralized hash tables (DHT)
kademlia
merkle trees
The latter should give you an idea of how the mechanism works more or less.

Now, let's answer point by point
Are the blocks stored locally on my system too?
Yes

Where else is the data stored? On other peers that I am connected to? Because I'm still able to access the file if I close my ipfs daemon.
All the peers that request your file cache it

If this is true, and data is stored at several places, possibility of losing my data is still there, if all the peers disconnect from the network?
You lose the file when it's no longer possible to reconstitute your file from all the peers that had a part of it cached (including yourself)

Does every peer on the network store the entire file or just a part of the file?
One can get just a part of it, imagine you are watching a movie and you stop more, or less, at the half... that's it, you've cached just half of it.

If copy of data is being distributed across the p2p network, it means the data is being duplicated multiple times? How is this efficient in terms of storage?
When you watch a video on YouTube your browser caches it (that means a replication!)... ipfs is more efficient in terms of traffic, let's say you switch off the browser and 2 minutes later you want to watch it again. Ipfs gets it from your cache, YouTube makes you download it again. There's also an interesting matter on the delta storage (related to git) and from where you get it (could be inside your lan... that means blazing fast) but I want to stick to the questions.

We store data uploaded by other peers too?
If you get data, you cache it so...

Minimum System requirements for running IPFS? We just need abundant storage, not necessarily a powerful system?
The main daemon is written in go. Go is efficient but not as much as writing it on C++, C, Rust... Also, the tech is pretty young and it will improve with time. The more space you have the more you can cache, CPU power isn't THAT important.

If you are interested in ways to store data in a p2p manner, here some links to interesting projects.

https://filecoin.io/
https://storj.io/
https://maidsafe.net/
https://www.ethereum.org/ and it's related storage layer
https://ethersphere.github.io/swarm-home/
