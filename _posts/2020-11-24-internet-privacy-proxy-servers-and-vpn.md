---
layout: post
title:  "Internet Privacy: Proxy Servers and VPN"
author: arvind
categories: [Privacy]
tags: [network privacy,security, internet]
image: assets/images/privacy.jpg
bannerimage: assets/images/privacy.jpg
description: "A short description about tracker without bellls and whistles"
featured: false
hidden: false
---

Privacy is a huge concern on the internet, especially when there are companies making billions by selling users data. In this article, I'll be mainly talking about Proxy servers and VPN, two of the most common ways to maintain anonymity on the internet.


## Incognito Doesn't Work

For all you out there who might think that you are completely anonymous if you use incgnito mode, well guess what, you are wrong. Incognito mode is only good at preventing anyone with access to your computer from easily finding your activities. It clears all the browsing history, all the cookies so that anyone using your computer will not be able to see what you did. But the rest of the internet can still see what you are doing. The website that you just accessed in incognito mode still knows your location and so does your internet service provider.

You can use [What is My IP Address](https://whatismyipaddress.com/) to see what others on the internet see your location as. Now the whole point is, we need something better to hide ourself and protect our privacy. Now, before we look at what proxy and VPN is, let's try to get a general understanding of how internet works.

<!-- ## How internet works


![How internet works]({{site.baseurl}}/assets/images/frcnn.png)

So, your mobile phone is connected to the wifi. Let’s say you open the browser and type https://google.com. When you enter the url on your browser and press search, your phone starts sending packets of information to the wifi access point in your house. Then it travels to the modem through the ethernet cable. Your modem would probably have fiber connection or something similar that was provided to you by your internet sevice provider. Through this channel. The packets travel to your internet service provider, in this case, airtel. Now your ISP performs an IP lookup. All the nodes in a network are identified using their IP address, the ISP gets the IP address of the server of google through a DNS lookup. THen it transmits the packets through routers to google’s server. Google’s server receives the packet, processes the request and sends back the response. This is how a one way trip to the server takes place.
 -->


### How private is internet?


Let’s say you open the browser and type https://google.com. When you enter the url on your browser and press search, your phone starts sending packets of information through the wi-fi router. These packets contain information about the source and destination in their header. This is obvious because all the nodes in the network need this information in order to route the packet from source to destination and vice versa. But this means that all the nodes in the network can see where the packet came from and where it is going to. That is why you are able to google and find information about your public IP address and your IP’s location. The only thing preventing the internet from pinpointing your exact location is the NAT setup by the ISP. 

Even the server you are communicating with has lots of information about you. Therefore, anything you do on the web can easily be traced back to you. There is absolutely zero privacy there. And as we saw, incognito doesn’t work in this case because all incognito does is delete you history and session cookies.

Now, let’s have a look at what a Proxy is and how it offers privacy.
   
## Proxy Server

Proxy here serves the exact same purpose as it’s definition, which is a substitute, or someone else who represents you.
We often hear people using the word proxy in the context of accessing blocked websites. For example, In my school computers, websites like youtube,facebook are blocked by a firewall. We often used proxies to bypass the firewall. A proxy server essentially acts as your substitute and fetches content from the internet for you. 


<img src="{{ site.baseurl }}/assets/images/proxy.png" alt="Proxy Server" height=250/>

<br />

This image shows how we can use a proxy to access the blocked facebook website. In this case, the firewall believes that you are communicating with some server and allows you to do it. But this server inturn communicates with facebook and fetches content on your behalf and sends it over to you. 

But proxies are more than just means to bypass firewalls, they also provide a certain degree of privacy.

### Proxy and Privacy

A proxy essentially acts as your gateway to the internet. Now, there are different types of proxies offering different levels of security. 

A **Transparent proxy** is the least secure. It simply forwards the request they get and they are the least secure. They don't try to hide the users IP address and just forward whatever request they get. 

**Anonymous proxy** takes your request and replaces the source IP with it’s own IP. So when you access facebook, as far as the rest of the internet is concerned, it’s just proxy accessing facebook. The facebook servers will receive the Proxy’s IP and they don’t have any clue about who is on the other side of the proxy. But the disadvantage with anonymous proxies is that they don’t hide the fact that they are proxies. If some sites choose to deny service to proxy users, you won’t be able to visit them while using an anonymous proxy. Since anonymous proxies do hide your IP address, they’re not a bad choice if you’re looking to gain a bit of control over your online privacy. 

Consider **High anonymity proxies** — also known as elite proxies — a step up from your regular anonymous proxy. The fundamentals are the same, except high anonymity proxies also disguise your use of the proxy itself. A website won’t be able to detect that you’re using a proxy if you use one of these. High anonymity proxies achieve this added protection by periodically altering your new IP address and also withholding any clues that they are serving as proxies on your behalf. They’re the most secure type of proxy.


Proxy can be further improved by caching websites, filtering content etc which provides extra speed and security. But proxy is not 100% secure. So, do proxies not maintain privacy on the internet? Well, upto a certain extent. Highly anonymous proxies do provide a high degree of privacy.  But proxies definitely aren’t 100% secure. Someone with access to the proxy server can easily get information about all the transactions and can trace back to the user. And one more important thing to remember is that a proxy can only provide privacy for the things that you do on your browser. 

## Virtual Private Network

Although Proxies provide a decent level of privacy, the only thing they are good at is hiding your IP address. VPNs are a step above Proxies as they can hide your IP address and provide an encrypted connection too!
VPNs provide “device protection” and it protects all your  traffic, including your browser, wherever you have a VPN installed and enabled. VPNs provide added security and privacy for all your online activity.

We know that the internet is a public resource, so what exactly does a private network mean here? 


### What is a Private network

According to wikipedia, a private network is any connection within a specified network wherein restrictions are established to promote a secured environment. In a more simpler term, a network can be configured in such a way that devices outside the network cannot access it. But the devices within the network can access contents outside the private network. So yes, your home wifi is a type of private network. If you check your IP, it’ll probably show something like 192.168.something.something or 172.something.something.something. These are your private IP addresses. All the devices connected to the same wi-fi network can access you through this address. But devices outside the network cannot access your system using this IP address.


A **Virtual Private Network** (VPN) extends a private network across a public network and enables users to send and receive data across shared or public networks as if their computing devices were directly connected to the private network.

So this VPN technology was actually developed to provide access to corporate applications and resources to remote or mobile users, and to branch offices. Later, for security, the private network connection started using an encrypted layered tunneling protocol, and users were required to pass various authentication methods to gain access to the VPN. Now, VPN is also used for privacy on the internet.

Let’s have a look at what VPN is and how it works.

### How do VPNs work?

One thing to note is that VPN completely removes your Internet Service Provider (ISP) out of the picture. Instead of routing the packet to the destination through your ISP, we establish a secure connection to one of the VPN nodes/servers. If you open a VPN application, you usually see different countries listed. So these are the available VPN nodes. The VPN service providers like Nord VPN etc sets up a network of servers all over the world. When you choose a server, the VPN client app that you downloaded establishes a secure tunnel connection from your device to the server bypassing ISPs or any other person who might be lurking in the network. THe VPN service provider use various algortihms like IPSec to encrypt the connection and provide protection at IP level.

Your device is now seen as being on the same local network as your VPN. So your IP address will actually be the IP address of one of your VPN Provider’s servers.


A VPN connection usually works like this. Data is transmitted from your client machine to the connected node in the VPN network through a secure tunnel. The VPN node receives the packets and all relevant information, it then encrypts your data and sends it through the internet. Another node in the VPN network decrypts your data and sends it to the appropriate internet resource, maybe a web server, an email server, or your company's intranet. Then the internet resource sends data back to a point in your VPN network, where it gets encrypted. That encrypted data is sent through the internet to another point in your VPN network, which decrypts the data and sends it back to your client machine.

That brings us to the next question.

### How secure are VPNs?

Like with any online software or service, the security of a VPN will be reliant on a number of factors. In the case of VPNs, these factors include:

1. **The kind of technology the VPN provider uses** <br />There are different protocols for establishing secure connections. IPsec is one. There are other protocols such as OpenVPN, Secure Socket Tunneling Protocol  etc. Most of these protocols are fool proof and do provide a good amount of security.
2. **The laws in your country and the VPN provider**
Throughout this connection process, your identity is only revealed to the VPN node that you get connected to. Most of the VPN providers usually keep a log of all the connections to their network. Based on the laws surrounding VPN, the VPN provider might be forced to submit the user history if forced to do so. In countries like China, VPN is completely banned and you can be put into jail for using it. VPN use is also banned completely in Belarus, North Korea and Iraq.


## VPN vs Proxy

The difference can be summed up in a single sentence *"A proxy is just a gateway whereas a VPN is a tunnel"*. Another thing to note is that a connection to proxy goes through your ISP, so it is still possible to trace back to you. In the case of a VPN, only the VPN node knows your identity, which is known to the VPN service provider. As long as the VPN provider keeps it safe, your data will be 100% private. 


## Conclusion

And this is 100% true. There is nothing that provides complete privacy. The Internet is all about connecting all the devices in the world, and if you access something over the internet it can always be traced back to you. The only thing that matters is how easy it is to trace back to you.

So a normal internet connection is like sitting in your house with a door open, if you consider the fact that HTTPS is encrypted, it’s similar to sitting in your house with your door closed, but not locked. Anyone can open it. Using proxy locks the door, but there is still a back door that can be used to get into your house. VPN locks all the doors but the person who has the key can definitely enter your house. So it depends on how safe the key is. 

In the end nothing is completely private. It's just a matter of how easy  you make it for others to dig up stuff. 



