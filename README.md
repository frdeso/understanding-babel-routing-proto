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
##Basics

In order to use Babel on a meshnetwork you must start by creating a mesh. In a meshnetwork, an Ad-Hoc connection is used has the Datalink layer (layer 2) of the OSI model. Once this connection is made computers can communicate between each other.

To setup a Ad-Hoc network, the computers must be in the same Ad-Hoc cell. A cell is describe with two things : the SSID and the channel. The SSID is the name of the wireless network which is a hexadecimal string formated as a MAC address. The channel is simply the frequency of operation.
Also, be sure to set your network cards in Ad-Hoc mode and not in Infrastructure mode.

##Howto install/setup Babel on Debian
###Installation
The Babel comes in a package that is present in the Debian repository. It is under the name of `babeld` for Babel daemon.

To install this package you need to run a simple apt-get command as root.
~~~sh
apt-get update && apt-get install babeld
~~~
###Configuration
##Howto install/setup Babel on OpenWRT
###Installation
OpenWRT has a package manager with a behavior like apt-get called opkg. Once, you are logging as root on your OpenWRT platform you have to make sure that you have acess to the Interwebs.(`ping google.com` is a good way to do it). 

Now, you have to run these opkg commands :

~~~sh
opkg update && oopkg install babeld kmod-ipv6
~~~
###Configuration
