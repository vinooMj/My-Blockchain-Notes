Video Streaming in decentralized platform

Advantage of Decentralized video platform

Decentralized videos mean there's no simple way of removing content from the site. This could be a blessing or a curse. For some users, however, the assurance that their content is not in the hands of a large organization is a big draw, and a reason to switch to Decentralized video platform.

No central server means no single place storing all of the user's data, ready to be hacked.

Decentralization means no traditional way of censoring videos.

IPFS

IPFS is a distributed system for storing and accessing files, websites, applications, and data.

IPFS or InterPlanetary File System is an open-source protocol and network designed to create a content-addressable, peer-to-peer method of storing and sharing hypermedia in a distributed file system. It aims to make the web faster, safer, and more open.

When you add a file to IPFS, your file is split into smaller chunks, cryptographically hashed, and given a unique fingerprint called a content identifier (CID). This CID acts as an permanent record of your file as it exists at that point in time.

If you add a new version of your file to IPFS, its cryptographic hash is different, and so it gets a new CID. This means files stored on IPFS are resistant to tampering and censorship — any changes to a file don't overwrite the original, and common chunks across files can be reused in order to minimize storage costs.

Installation: https://docs.ipfs.io/install/command-line/#official-distributions

Store and play videos:

Initialize the IPFS
IPFS can be used to store and play videos. Suppose we add a video:


ipfs add -q sintel.mp4 | tail -n1



You can view the resulting hash in a few different ways.

ipfs cat $video_hash | mplayer -vo xv -



Via local gateway (note that the gateway method works with most video players and browsers)

mplayer http://localhost:8080/ipfs/$video_hash



Or open it up in a browser tab (in this example, Chrome)

chromium http://localhost:8080/ipfs/$video_hash


IPFS video: https://ipfs.video/
Ex: https://ipfs.video/ipfs/Qmcd7D6TnnzZzsk12DBwCMRYx1a8TVX4tq4eemYqspL4Rv



How can IPFS help us in Streaming?
IPFS is becoming a new major subsystem of the internet. If built right, it could complement or replace HTTP.
In IPFS streaming we don't need to push the content to every user. All you have to do is, push the content to the IPFS gateways. Anyone who wants that content can pick it up from there. IPFS gateway caches the content locally. So more number of gateways, more content sources.
IPFS provides persistence storage of those live streamed media content, so that if someone misses the live streaming, they can always come back to find a saved copy of it. The network automatically deletes duplicates and tracks version history. With our interface we also allow users to schedule the content for live streaming and broadcasting. Users can record the media and automate the system to stream that media on the given time for the specified duration.
IPFS helps to resolve congestion and overly controlling governments by distribution. Instead of locations, IPFS addresses point directly to the resources and it makes sure that this data comes from the closest sources.
This means that if a classroom full of students would watch the same video, they would fetch it from each other instead of any central location. This would make streaming a 4k video bufferless.


HLS
HTTP Live Streaming (HLS) is one of the most popular protocols used to stream video today. Over the past few years, HLS has become a standard protocol for web video, and with good reason. HLS is pretty simple to set up, it’s free to use, and it’s supported on a wide range of devices.
Anyone on the network can request the content with the help of IPNS hash and play it on the browser with HLS player. HLS player takes the ‘master.m3u8’ file and plays the chunks in defined order.





Library: ipfs-http-client

Third Party:

Pinata:
Pinata is the simplest way to upload and manage files(text and videos) on IPFS. Our friendly user interface combined with our IPFS API.


Fleek:
Fleek is everything you need to host fast, modern sites & apps on IPFS. All in one seamless workflow. Deploy your site in a few quick clicks onto IPFS with a built in CDN for blazing fast performance.
 

Decentralized Video platforms:

Live streaming - https://livepeer.org

D-tube:
Standing for decentralized tube, D.Tube uses a generalist file storage blockchain called InterPlanetary File System (IPFS). Its native token to monetize activities is DTube Coin (DTC). By being on a blockchain, all uploaded content cannot be subsequently deleted or edited.

First of all, DTube has no central servers. All of the content is stored on a blockchain. By nature, a blockchain's data is verified between all of its members.
DTube uses DTube Coin ($DTC) as its currency, there is no need for traditional advertisements. Users vote on videos to give them worth. Popular videos receive $DTC and it is paid into the creator's wallet.
Creators are free to advertise within their videos, but many users are averse to advertisements, therefore relying on $DTC seems to be the best way to monetize videos on the service.
DTube Has No Recommendation Algorithm.
Uploading is too slow. it took around 15 minutes to upload a video of 3 mins.




Working:
One of the things that differ DTube from other block chain based social media platforms are that on DTube videos are not uploaded onto the blockchain. Rather, a link to the video is stored on the blockchain. The actual video file, in the .mp4 format is stored using IPFS.
IPFS is not a blockchain technology but it is a decentralized one. It is a protocol that stores decentralized data. It works on the principle that follows “Distributed Hash Tables (DHT)”. In a similar fashion of other cryptocurrencies using asymmetric cryptography, DHT networks will have hash content to identify a file. This hash is basically the identity of the record, and it is so easy to repeat data and ensure that the hashes match to ensure that the file sent to us is the original.
 
Reference:
https://medium.com/@ranamajid007_71788/what-is-dtube-how-it-works-and-can-it-ever-replace-youtube-222b67f96556
https://www.makeuseof.com/what-is-decentralized-video-streaming/
https://steemit.com/utopian-io/@hsynterkr/ipfs-tutorial-4-upload-and-stream-videos-via-ipfs
https://dabit3.medium.com/uploading-files-to-ipfs-from-a-web-application-37d75fb326ed
https://forum.moralis.io/t/file-take-a-lot-of-time-to-upload-in-ipfs/2466/9
https://stackoverflow.com/questions/52498515/how-to-improve-download-speed-of-files-coming-from-ipfs
https://github.com/ipfs/go-ipfs/issues/2111
 
 
 
 






ipfs



