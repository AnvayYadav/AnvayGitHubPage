---
toc: true 
comments: true 
layout: post
title: 4.1 The Internet
description: 4.1 The Internet
type: hacks
courses: { compsci: {week: 14} } 
---



4.1 The Internet
Part 1
How did the internet come to life? It all began by these massive computers. They were isolated and very hard to work on. As a result, the idea of the internet came to life. It was to easily communicate between users and opened many gateways to digital communication.

The internet is basically a way for computers to talk to each other using networks

A packet is a small amount of data or information sent over a network that includes information about the sender and destination.

Packet

A computer network is a group of computing devices interacting with each other in some sort of way
How do computers send data to each other?
In a process called packet switching, a message(file) is broken up into packets which are reassembled by the receiver. It is often times converted into something the computer can understand like binary.

A path is between the sender and receiver and the router will help find the path. For example, If you're accessing a website, routers determine the optimal path for the data packets to traverse the internet (routing), following a series of interconnected devices (paths) to reach the web server.

Routing is a process that finds a path from the sender to receiver

Bandwidth is the maximum amount of data that can be sent in a computer network

Popcorn Hack 1
The Internet

What is the diagram showing?
Bandwidth
Computer Network
Packet Switching
Operating System
Two possible answers
Part 2
Protocols are sets of rules for the way data is transferred throughout the internet

There are two acceptable models that show the layers that data is sent by protocols

OSI
TCP/IP
TCP/IP is more widely accepted but OSI is still used
The OSI(Open Systems Interconnect) model shows the 7 layers you have to go throught to communicate between other computers

OSI Model

TCP(Transmission Control Protocol) is a protocol for how to send messages between devices
TCP Model

Waist Model

Popcorn Hack 2
A request from the frontend to the backend is being made and the response returns JSON. What layer(s) did the data go through?

Application
Transport
Internet
Network Access
All layers
What is an example of the OSI/TCP Model
Process

Network Access/Internet Layer
The process usually starts with the Internet layer where the user's computer is assigned a unique IP address so it can communicate with other computers or web servers
A DHCP(Dynamic Host Configuration Protocol) assigns the computer its unique IP address
Application/Transport Layer
The user sends a request to a server or page
If the user wants to go to a website like amazon.com, it has its unique IP address but it isn't readable by humans so a DNS(Domain Name Service), which stores the IP address inside of a database, sends it over the user
During this process, the user sent a TCP request for the IP of amazon.com to the DNS server and the DNS server sent a TCP response in the form of packets for the IP of amazon.com
Now, the user can send a request to the IP of the webpage like amazon.com
The last step is for a router to send the user to the correct destination of the IP. In this case, amazon.com.
Popcorn Hack 3
How does a user get the IP for a web page when they enter the url?

It goes through layers when the request is made to the webp
The DNS sends it to the user in the form of a TCP response
There is no need for the user to know the ip when going to the url
The user automatically knows
Commonly used protocols
HTTP - Hyper Text Transfer Protocol
HTTP is a protocol that says how data is transferred over the internet
Used for sending requests from a user and receiving a response in the form of HTML or JSON from the server.
In last trimester, you made a request to the backend from the frontend using HTTP and it sent a response in the form of JSON
HTTPS
HTTPS is HTTP with security. In last trimester's final project, the devops person used certbot to make the HTTP requests to the backend secure.
HTTP

TCP/IP - Transmission Control Protocol, Internet Protocol
TCP/IP is important because HTTP requests and responses depend on a TCP connection between the client and server
Once a TCP connection is made, HTTP requests are carried in TCP packets
IP sends the TCP packets to the correct location
When you made the HTTP request from the frontend to the backend, your request was broken up into TCP packets and sent to the correct location by IP
TCP/IP

Homework
Bandwidth:

In the context of computer networks, elaborate on the concept of bandwidth. Discuss how bandwidth influences the speed and efficiency of data transfer. Provide examples of scenarios where both high and low bandwidth can impact the performance of internet connected devices.
Computer Network: 2. Explore computer networks by detailing the key components and their interplay. Discuss the significance of scalability, security, and reliability in designing computer networks. Provide real-world examples of how different types of computer networks, such as local area networks (LANs) and wide area networks (WANs), serve distinct purposes in various settings.

Packet Switching: 3. Investigate packet switching and its role in modern communication systems. Compare and contrast packet switching with alternative methods, such as circuit switching, highlighting the advantages that packet switching brings to data transmission. Describe the journey of a data packet through a network.