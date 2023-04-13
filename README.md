# What is Telprotocol?

Telprotocol is a decentralized communication network based on SIP-Protocol. It can be used for dialing telephone, text message service, video calling .

The architecture of telprotocol is a peer-to-peer protocol architecture. The core data is stored in the chain as NFT. Telprotocol supports multiple chains and cross-chain transfers, and users can also use it on ethereum, arbitrum, optimism, zksync, etc .

# What problems does Telprotocol solve?

Most of the calls in the current market run as centralized services, such as AT&T, T-Mobile, and Skype.
Telprotocol is built on blockchain and is explored in the direction of decentralization. It has the following advantages:

1. The user's core data is stored in the chain.
2. Communication data, is a point-to-point connection, there is no intermediate server.
3. Encrypt communication data to ensure data security.
4. Transmission of core data is real-time, after receiving immediately destroyed, to ensure the safety of calls.


# What does Telprotocol consist of ?

![avatar](/tel.png)

1. 
CoreData consists of two parts, the NFT (such as the ENS domain name) and the data for the direction setting.
Users can set blacklist

3. 
UA, which is a client that users can use to communicate with other users. UA is usually implemented on multiple platforms, mobile, PC, and Web.
UA is divided into two categories, one is to support deep login (need to import the Ethernet account way of login) , the other is to support light login (use password, direct login) .
Deep login fully controls light login. 

4. 
The node is mainly responsible for the establishment of signaling channel.


# How Telprotocol is implemented？

Telprotocol is a layer of point-to-point communication network built on a user's core data. The data interaction between the UA and Node satisfies the Sip Protocol.

The user's core data is the basis of telprotocol, UA loads the user's core data, the user needs signature verification.

Node verifies the authenticity of UA data by loading the user's core data. Node builds a signaling channel for the authenticated user.

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


# Business scene

Telephone/Voip
![avatar](/telephone.png)


Sms
![avatar](/sms.png)


# How to ensure the security of the account?

Deep Login and Light Login
Deep Login： In the UA end, you must import the account of Ethereum to verify the authenticity of the data.

Light Login:  In the UA side, you don't need to import your account, but use a password to log in.

The password must be set in Deep Login mode.


# Telprotocol Demo


Telprotocol, how to use ENS-Domains to make a call ?  
https://www.youtube.com/watch?v=BQLZ51Gm5lk


PC Slide  
https://youtu.be/7Kk0W4Zxly4


Mobile Slide  
https://youtube.com/shorts/wedcUmf_yrY?feature=share



# How should I get involved?

you can contact me here to participate in the test.  
Twitter https://twitter.com/telprotocol

# Donations

If you want to support the project, here  
https://etherscan.io/address/0xe348A8497A00aE9674CeA417119a594b1706cF52  


# Note

In the early stages of development, the documentation will be continuously updated.