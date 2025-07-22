# Networking 101

Before writing our net code we're going to have to decide on the networking protocol and topology to use. To make an informed decision we will cover the basics of networking, different protocols and topologies. Then we will look at the practicle considerations implementing networking in MonoGame.


## Crash Course


## Protocol

What protocols are avaliable and which should you use? That depends on the frequency and size of updates to other players. All the methods are built on the Internet Protocol (IP) which takes care of assigning IP addresses and routing packets.

| Use Case | Protocol |
| :---      | :---              |


## Topology

![Figure 1-1: Topologies](./images/monogame-net-topologies.png)

### Networking in MonoGame

In MonoGame we are using .NET which includes libraries for using the above networking methods in the `System.Net` namespace. There are also 3rd party .NET libraries some of which are built specifically games.

> [!NOTE]
> MonoGame does not implement the equivalent of `Microsoft.Xna.Framework.GamerServices` that existed in the XNA framework for networking becuase `GamerServices` was only for Xbox LIVE. 

> [!NOTE]
> When using a platform like Steam or consoles like PlayStation, Nintendo or Xbox there are official libraries or APIs to integrate with their identity management, further, there are libraries to assist with your multiplayer network code. For consoles you first have to have access, refer to: [About MonoGame | MonoGame](https://docs.monogame.net/articles/console_access.html), on Steam you need to be a Steamworks developer. Regardless of platform however your would still need to implement networking of updates between players which should be portable between platforms – you can still open sockets for HTTP, TCP and UDP communications on all platforms – its normally the identity management part that will be specific to each platform.

