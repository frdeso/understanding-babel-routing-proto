understanding-babel-routing-proto
=================================
This is a draft of my understanding on how the Babel Routing Protocol works and is used. I use this as a way to structure my knowledge of the protocol to use it in the most efficient way possible.


##What is Babel ?

The Babel routing protocol is a distance-vector routing protocol for Internet Protocol packet-switched networks that is designed to be robust and efficient on both wireless mesh networks and wired networks. [Wikipedia]

###First, what is a routing protocol?

A routing protocol is the way routers communicate with each other to spread the metrics of the network. A good routing protocol is one that find the good path from computer A to computer B. To make a good routing choice, a node must have the best information available about the cost of each link.

###Second, what is a distance-vector routing protocol?

A distance-vector routing protocol is routing protocol in which nodes store information of the direction and the distance(eg. Number of hops) to the destination. Also, each node periodicly exchange routing table with their immediate neighbor. Doing this, the node can update his routing table with the most up-to-date information and the share it with his neighbors.

###Third, what is a Mesh network?

A Mesh network is a computer network with no central point. Every node can exchange data directly with other nodes without having to acces to central point, like a router. The node must do his best the spread through the network his data AND the data of the other nodes. This type of network is a lot less vulnerable to natural disasters and cencorship since no node is essential.

##Howto install/setup Babel on Debian
###Installation
The Babel comes in a package that is present in the Debian repository. It is under the name of `babeld` for Babel daemon.

To install this package you need to run a simple apt-get command as root.

`apt-get update && apt-get install babeld`
###Configuration
##Howto install/setup Babel on OpenWRT
###Installation
###Configuration
