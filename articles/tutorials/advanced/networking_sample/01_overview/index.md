# Overview

## Networking 101

Before writing our net code we're going to have to decide on the networking method and topology to use. To make an informed decision we will cover the basics of networking, different methods and topologies 


## Method

What methods are avaliable and which should you use? That depends on the frequency and size of updates to other players. All the methods are built on the Internet Protocol (IP) which takes care of assigning IP addresses and routing packets.

| Method    | Use Case |
| :---      | :---              |
| Request Response > 2s | HTTP or similar TCP based request response protocol |
| Turn-based > 1s latency | WebSockets or similar TCP based |
| Continuous Updates about 1s latency | UDP |
| Continuous Updates < 0.5s latency | UDP |


### MonoGame

In MonoGame we are using .NET which includes libraries for using the above networking methods in the `System.Net` namespace. There are also 3rd party .NET libraries some of which are built specifically games.

> [!NOTE]
> MonoGame does not implement the equivalent of `Microsoft.Xna.Framework.GamerServices` that existed in the XNA framework for networking becuase `GamerServices` was locked to Xbox LIVE. 

> [!NOTE]
> When using a platform like Steam or consoles like PlayStation, Nintendo or Xbox there are official libraries or APIs to integrate with their identity management, further, there are libraries to assist with your multiplayer network code. For consoles you first have to have access, refer to: [About MonoGame | MonoGame](https://docs.monogame.net/articles/console_access.html), on Steam you need to be a Steamworks developer.



## Topology

![Figure 1-1: Topologies](./images/monogame-net-topologies.png)

## 