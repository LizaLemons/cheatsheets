
# Networking Basics for Devs

---


### What is networking?

You can think of networking in terms of tracing the path of data, both as it is prepared and packaged on your machine, and as it is transmitted to other machines.

Basically, the ways in which machines communicate with each other and how they transport data.

---


### Examples
- Sending iMessages between two Apple computers
- When a person navigates to any URL
- When you connect to a router or wifi network
- AirDrop


---


### Protocols

All of the above actions use different **protocols**, or procedures, for sending data.


---


### TCP/IP model

- TCP/IP is one method of talking about the different **layers** of network communication.

- More commonly known as the **internet protocol suite.**

- There are many models, this one is most relevant for devs & is widely used

- Another example is the OSI model, or the **Open Systems Interconnect** model.


---


### What are layers

When people discuss networking, usually it is in a horizontal fashion, meaning how data is transmitted **between hosts**.

But when we talk about **layers** of a model, we will be talking about networking in a vertical fashion, as in how data is prepared, packaged, and subsequently transmitted within a single machine.


---


### Four layers of the TCP/IP model
- Application
- Transport
- Internet
- Link


---


### Application layer

- The application layer is responsible for **creating and transmitting user data between applications.**

- This is where the HTTP protocol is implemented
  - Stands for hypertext transfer protocol
  - HTTP essentially tells the remote system what you are requesting
  - For example, GET, POST, and DELETE all interact with the requested data in a different way.


---


### Transport layer

- The transport layer is responsible for **communication between processes.**

- This level of networking utilizes **ports** to address different services.
  - A **port** is an address on a single machine that can be tied to a specific piece of software.
  - When have we used ports before?
    - `localhost:3000` - react & node
    - `localhost:27017` - mongodb
    - `localhost:8080` - http-server  

- This is where the TCP protocol is implemented. TCP is used to establish reliable connections.

---


### Internet layer

- The internet layer is used to transport data from node to node in a network

- This is where the IP protocol is implemented

- IP addresses are used in this layer as a way of reaching remote systems.
  - IP addresses look like this: `109.210.15.7`
  - IP addresses are unique on each network
  - They allow machines to address each other across a network

- DNS (domain name system) are a human-friendly naming mechanism for internet resources.

- DNS is how a domain name is tied to an IP address, and allows people to access websites using a URL in your browser.

---


### Link layer

- This layer establishes connections between neighboring nodes to send data

- Implements the actual topology of the local network that allows the Internet layer to work


---


### Resources
- [Digital Ocean: Intro to Networking](https://www.digitalocean.com/community/tutorials/an-introduction-to-networking-terminology-interfaces-and-protocols)
- YouTube - Intro to Computer Networks
  - [Part I](https://www.youtube.com/watch?v=ClPA3F_ZXds)
  - [Part II](https://www.youtube.com/watch?v=fXKLH_NkNFY)
  - [Part III](https://www.youtube.com/watch?v=xhvdQRw3sms)
- [Udacity: Networking for Web Devs](https://mena.udacity.com/course/networking-for-web-developers--ud256)




















---
