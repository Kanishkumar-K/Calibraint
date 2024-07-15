## CDN (Content Delivery Network)

- A content delivery network (CDN) is a network of interconnected servers that speeds up webpage loading for data-heavy applications. 

- The primary purpose of a content delivery network (CDN) is to reduce latency, or reduce the delay in communication created by a network's design.


 **Benefits of CDN**
  
 - Reduces Page load time
 - Reduces Bandwith costs
 - Increase content availability
 - Improve website security

### Origin Server:
An origin server is the source server where the original version of the content is stored.

### Edge Server:
An edge server is a server in a CDN that caches content closer to the end-users based on geographical location.


### Benefits of CDN

1. Reduces load time
2. Increase content availability
3. Reduces bandwidth costs


### Anycast Network

- In CDN, anycast helps improve the delivery of content by allowing multiple edge servers to share the same IP address. 
- When you request content, the CDN routes your request to the nearest server, reducing load time and improve efficiency.


### Internet Exchange Points:
  
  Internet Exchange Points are places where different Internet providers connect to exchange data directly.
  They help make Internet connections faster and more efficient by reducing the distance data needs to travel between networks.

---

### Points of Presence (PoPs):
  POPs, or Points of Presence, in the context of content delivery networks (CDNs), refer to strategically located data centers or edge servers that are distributed geographically to  enhance the delivery of content to end-users. 

 
 ## Working of CDN:

  1. CDNs store cached copies of website content across multiple servers globally.
  2. When a user requests content, the CDN's routing system directs the request to the nearest server
  3. The requested content is delivered from the nearest server rather than the origin server where the website is hosted.
  4. This reduces the distance the data travels and improves load times.

## CDN 

1. Hardware and Software Optimization
2. Minification process
3. Load balancing

---

## CDN Metrics

## 1. Rount Trip Time

Round-trip time is the duration in milliseconds it takes for a network request to go from a starting point to a destination and back again to the starting point.

## 2. Time to live

Time to Live (TTL) refers to the lifespan of a packet within a network, specifying the maximum number of router hops it can traverse before being discarded.

## 3. Cache hit ratio

Cache hit ratio is a measurement of how many requests a cache is able to hit successfully, compared to how many requests it receives.

Cache Hit Ratio = Number of Cache Hits / ( Number of Cache Hits + Number of Cache Misses)

---

## Cache

Caching is the process of storing copies of files in a cache, or temporary storage location, so that they can be accessed more quickly.

## Static Caching

Static caching involves storing copies of files that rarely change, such as images, CSS file, and HTML documents, on edge servers.

## Dynamic Caching

Dynamic caching involves caching content that is generated dynamically based on user interactions or real-time data. 
This can include database queries, API responses, personalized content, and pages that change frequently.

---

## CDN Security 

### DDoS attack

A Distributed Denial of Service (DDoS) attack is a malicious attempt to disrupt the normal traffic of a targeted server, service, or network by overwhelming it with a flood of internet traffic.

## SSL/ TLS Security:

CDNs (Content Delivery Networks) improve SSL/TLS security for websites by:
1. **Handling Encryption**: They manage SSL/TLS encryption between users and their servers, ensuring secure data transmission.
   
2. **Certificate Management**: CDNs handle SSL/TLS certificates, making sure they are valid and up-to-date, which simplifies setup for website owners.

3. **Protecting Against Attacks**: CDNs provide security features that defend against threats like DDoS attacks, safeguarding websites' SSL/TLS connections.

## TLS protocol:

Authentication: Verifying identities to confirm they are genuine.
Encryption: Transforming data to make it unreadable to unauthorized parties.
Integrity: Ensuring data remains accurate and unchanged from its original form.

## SSL Certificate

An SSL (Secure Sockets Layer) certificate is a digital certificate that authenticates the identity of a website and enables secure encrypted connections between a web browser and a web server

---

## TCP/ IP handshake:

The TCP/IP handshake is needed to establish a reliable and secure connection between two devices or systems before they can start exchanging data. 

1. **SYN (Synchronize)**:
   Client initiates by sending a SYN packet to the server to start a connection.
   
3. **SYN-ACK (Synchronize-Acknowledge)**:
   Server responds with a SYN-ACK packet, acknowledging the client's SYN and synchronizing connection parameters.

5. **ACK (Acknowledgment)**:
   Client sends an ACK packet to confirm receipt of the server's SYN-ACK, establishing the connection for data exchange.

---

