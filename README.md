# telprotocol
This paper aims to explore a new type of network transmission structure. A decentralized communication protocol based on SIP protocol combined with block chain technology.


# Several popular architectures:
C/S architecture is a typical two-tier architecture, the full name is Client/Server, that is, Client/Server-side architecture.  
  
B/S (Browser/Server) architecture, that is, Browser and Server architecture pattern, is a change or improvement of C/S architecture with the rise of Internet technology.  
  
P2P networks, which are peer-to-peer networks, rely on the computing power and bandwidth of the participants in the network, rather than concentrating the dependencies on fewer servers.  
  
In 2009, Bitcoin, the first open-source, decentralized cryptocurrency to be run by non-government, Internet users, became available to more people to learn about the power of the blockchain.  
Decentralization and exclusive ownership are the biggest features of bitcoin. The popularity of bitcoin, but also from the side of the People's desire for freedom, no borders, exclusive rights. My is my, others can not interfere, I do not like others to pry into my privacy, do their own things.
A borderless, free, user-friendly communications network is necessary.


# How does this work?
![avatar](/tel.png)
1. The base data is stored in the chain and is under the full control of the user.
Telephone: The identity number, through which users can find other users on The chain.
In the form of NFT, store in the chain, support users to sell, once sold, and the user-related data will change.
Support for custom names, such as Alice.eth

2. UC, which is a client that users can use to communicate with other users. UC is usually implemented on multiple platforms, mobile, PC, and Web.
UC is divided into two categories, one is to support deep login (need to import the Ethernet account way of login) , the other is to support light login (use phone and password, direct login) .
Deep login fully controls light login. The implementation of UC needs to satisfy the SIP protocol partial protocol.

3. The node is mainly responsible for the establishment of signaling channel, the node will load the block chain data automatically, and the data interaction of the node supports part of the SIP protocol.
There will be a hub on the final node, and the hub will assign users to different nodes based on the current network operation status to support more users.
Each node can support about 1000 users at the same time, and there will be differences in different environments.

4. The user-generated data mainly exists in the UC end, and the node does not store the data. Users can choose to use deep login, upload to the decentralized storage side, if the UC is deleted, users can download other UC side, and then in the way of deep login, can be repulled from the decentralized storage side. Data will be shared between different UC.

5. Data support encryption, to ensure the security of user's important data.


# How to communicate?
The architecture of telprotocol is a peer-to-peer protocol architecture, similar to the P2P architecture, and the data form of request and response between node and UC of telprotocol satisfies SIP protocol.

Alice "calls" Bob using his identity alice.eth, a type of Uniform Resource
   Identifier (URI) called a URI,such as alice.eth@telprotocol.
    It has a similar form to an email address.
    Bob's identity URI,such as bob.eth@telprotocol

    INVITE:
     alice.eth@telprotocol  ->   bob.eth@telprotocol
    Alice's  . . . . . . . . . . . . . . . . . . . .  Bob's
        |                |                |                |
        |    INVITE F1   |                |                |
        |--------------->|    INVITE F2   |                |
        |  100 Trying F3 |--------------->|    INVITE F4   |
        |<---------------|  100 Trying F5 |--------------->|
        |                |<-------------- | 180 Ringing F6 |
        |                | 180 Ringing F7 |<---------------|
        | 180 Ringing F8 |<---------------|     200 OK F9  |
        |<---------------|    200 OK F10  |<---------------|
        |    200 OK F11  |<---------------|                |
        |<---------------|                |                |
        |                       ACK F12                    |
        |------------------------------------------------->|
        |                   Media Session                  |
        |<================================================>|
        |                       BYE F13                    |
        |<-------------------------------------------------|
        |                     200 OK F14                   |
        |------------------------------------------------->|
        |                                                  |

     INVITE sip:bob.eth@telprotocol SIP/2.0
      Via: SIP/2.0/UDP telprotocol.com;branch=z9hG4bK776asdhds
      Max-Forwards: 70
      To: bob.eth@telprotocol
      From: alice.eth@telprotocol;tag=1928301774
      Call-ID: a84b4c76e66710@telprotocol
      CSeq: 314159 INVITE
      Contact: alice.eth@telprotocol
      Content-Type: application/sdp
      Content-Length: 142
      (Alice's SDP not shown)

 The first line of the text-encoded message contains the method name
   (INVITE).  The lines that follow are a list of header fields.  This
   example contains a minimum required set.  The header fields are
   briefly described below:

   Via contains the address (telprotocol) at which Alice is
   expecting to receive responses to this request.  It also contains a
   branch parameter that identifies this transaction.

   To contains a display name (Bob) and a URI
   (bob.eth@telprotocol) towards which the request was originally
   directed. 

   From also contains a display name (Alice) and a URI
   (alice.eth@telprotocol) that indicate the originator of the request.
   This header field also has a tag parameter containing a random string
   (1928301774) that was added to the URI by the ua.  It is used
   for identification purposes.

   The process of signaling interaction  
     
   ![avatar](/interaction.png)


For more detailed data exchange benchmarks, see:  
https://www.rfc-editor.org/rfc/rfc3261  


# How should I get involved?
you can contact me here to participate in the test.  
Twitter https://twitter.com/telprotocol

# Donations
If you want to support the project, here  
0xe348A8497A00aE9674CeA417119a594b1706cF52  


# Note
In the early stages of development, the documentation will be continuously updated.