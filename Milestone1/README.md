### Milestone 1

# 1. INTERNET
Internet is a global network of interconnected computers and other devices that communicate with each other using communication protocols.

Internet is called a network as it creates a network by connecting computers and servers across the world using routers, switches and other communication devices and channels.


##  Types of Network

### a. Personal Area Network (PAN)
- Connects personal devices within a short range, typically a few meters.
- Examples include Bluetooth connections and USB connections.

### b. Local Area Network (LAN)
- Connects computers and devices within a localized area such as a single building.
- Common in office networks and home Wi-Fi setups.

### c. Wireless Local Area Network (WLAN)
- Similar to LAN but uses wireless technology to connect devices.
- Found in homes, offices, and public places providing Wi-Fi access.

### d. Metropolitan Area Network (MAN)
- Covers a city or large campus, connecting multiple LANs.
- Used by city-wide networks and large university campuses.

### e. Wide Area Network (WAN)
- Spans a large geographical area, often connecting multiple LANs and MANs.
- The Internet is the largest and most well-known WAN.
---

##  Internetworking
Internetworking is the process of connecting multiple distinct networks to create an extended network. 

| Type      | Description                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------|
| Intranet  | An intranet is a private network accessible only to an organization's staff. It uses internet technologies but is isolated from the public internet. |
| Extranet  | An extranet extends an intranet to allow access to external partners, customers, or suppliers. It still restricts access to authorized users but provides broader connectivity than an intranet. |
| Internet  | The internet is a global network of interconnected computers and networks that is publicly accessible. It uses standardized communication protocols to enable worldwide communication and data exchange. |
---

## Protocols

### TCP (Transmission Control Protocol)

Transmission Control Protocol (TCP) is a connection-oriented protocol for communications that facilitates the exchange of messages between different devices over a network. It operates at the transport layer of the OSI model.

### UDP (User Datagram Protocol)
User Datagram Protocol (UDP) is a transport layer protocol in the Internet Protocol suite (UDP/IP). Unlike TCP, UDP is unreliable and connectionless, meaning it does not establish a connection before data transfer.

---

## OSI Framework
The OSI (Open Systems Interconnection) framework explains the process of transmitting data between computers. It is divided into seven layers:

| Layer               | Description                                                                                          |
|---------------------|------------------------------------------------------------------------------------------------------|
| Application Layer   | Applications create the data.                                                                         |
| Presentation Layer  | Data is formatted and encrypted.                                                                      |
| Session Layer       | Connections are established and managed.                                                              |
| Transport Layer     | Data is broken into segments for reliable delivery.                                                   |
| Network Layer       | Segments are packaged into packets and routed.                                                        |
| Data Link Layer     | Packets are framed and sent to the next device.                                                       |
| Physical Layer      | Frames are converted into bits and transmitted physically.                                             |


## TCP/IP Protocol Suite

TCP/IP (Transmission Control Protocol/Internet Protocol) is a set of protocols that enable communication and data exchange over networks, including the Internet. It is organized into four layers:

| Layer                | Description                                                                                          |
|----------------------|------------------------------------------------------------------------------------------------------|
| **Application Layer**| Handles communication between applications and the network. Examples include HTTP, FTP, SMTP.         |
| **Transport Layer**  | Provides reliable data transmission services between devices. Includes TCP (connection-oriented) and UDP (connectionless). |
| **Internet Layer**   | Manages addressing, routing, and packaging of data packets. Uses IP (Internet Protocol) for addressing and routing. |
| **Link Layer**       | Transmits data between neighboring network nodes in a local network segment. Includes Ethernet, Wi-Fi. |

---

### CORS

**Cross-origin resource sharing (CORS)** is a mechanism that allows a web page to access restricted resources from a server on a domain different than the domain that served the web page.

**Example Scenario:**
- **Backend (Django)**: Django API is served from `http://localhost:8000`.
- **Frontend (React)**: React application is served from `http://localhost:3000`.

When your React frontend tries to make an HTTP request to `http://localhost:8000/api/data/`, the browser will block the request by default due to CORS policies since it's considered a different origin (_localhost:3000_ vs _localhost:8000_).

**Solution:**
To allow the React frontend to communicate with the Django backend, we should configure CORS settings in Django (`settings.py`) using the `django-cors-headers` package, as described in the previous response.

---

### Switches

**Switches** are networking devices that operate at the data link layer (Layer 2) of the OSI model. They are used to connect multiple devices within a single local area network (LAN).

---

### Routers

**Routers** are essential networking devices that operate at the network layer (Layer 3) of the OSI model. They are responsible for forwarding data packets between computer networks. Routers can connect multiple switches together to create larger networks.

---

### Proxy

**Proxies** are intermediary servers that sit between clients (such as web browsers or applications) and the internet. They facilitate indirect connections between clients and other servers.

#### Types

- **Forward Proxy**
  *Definition:* A forward proxy, also known simply as a proxy, acts on behalf of clients to access resources from servers. It sits between the client (such as a web browser) and the internet, intercepting requests and forwarding them to the appropriate server.

- **Reverse Proxy**
  *Definition:* A reverse proxy sits between clients (typically web browsers) and servers, acting on behalf of servers to handle incoming client requests. It enhances security, performance, and scalability by providing the following functionalities:

---

### Switching

**Switching** is the technique used to decide the best route for data transmission.

- **Circuit Switching**
  *Definition:* Circuit switching is a switching technique that establishes a dedicated path between sender and receiver. In the Circuit Switching Technique, once the connection is established then the dedicated path will remain to exist until the connection is terminated.

- **Packet Switching**
  *Definition:* Packet switching is a switching technique in which the message is sent in one go, but it is divided into smaller pieces, and they are sent individually. The message splits into smaller pieces known as packets and packets are given a unique number to identify their order at the receiving end.

---

# 2. HTTP
HTTP stands for “Hypertext Transfer Protocol.” It is a set of rules for sharing data on the World Wide Web (WWW). HTTP helps web browsers and servers communicate, allowing people to access and share information over the internet.

Client-Server Model: 
HTTP works on a request-response system. 

Application Layer Protocol:
HTTP operates within the Internet Protocol Suite

---
**HTTP Request**: A client's request to a server for data exchange.

- **HTTP Version**: Specifies the HTTP protocol version (e.g., HTTP/1.1).
- **URL (Uniform Resource Locator)**: Address of the requested resource.
- **HTTP Method**: Action to be performed on the resource (e.g., GET, POST).
- **HTTP Request Headers**: Additional metadata sent with the request.
- **HTTP Body**: Optional data sent with the request (e.g., form data).

---

**HTTP Response**: Server's reply to a client's request.

- **HTTP Status Code**: Outcome of the request (e.g., 200 OK, 404 Not Found).
- **HTTP Headers**: Additional metadata sent with the response.
- **HTTP Body**: Data or content sent from server to client.

---

### HTTP Methods
They describe what kind of actions does it do 
| Method | Description                                      |
|--------|--------------------------------------------------|
| GET    | Retrieve data from a specified resource.          |
| POST   | Submit data to be processed to a specified resource. |
| PUT    | Update a specified resource with new data.       |
| DELETE | Delete a specified resource.                     |
| HEAD   | Retrieve headers for a specified resource.       |
| PATCH  | Apply partial modifications to a resource.       |
| OPTIONS| Retrieve the supported HTTP methods for a resource. |

---

### HTTP Status Codes
HTTP status codes are three-digit responses from the server to the browser-side request.
| Code | Description                                           |
|------|-------------------------------------------------------|
| 100  | Informational - Continue, Switching protocols, Early hints |
| 200  | Success - The request has succeeded.                       |
| 300  | Redirectional - The requested resource has been redirected. |
| 400  | Client Side Error - The server cannot process the request due to client error syntax. |
| 500  | Internal Server Error - The server encountered an unexpected condition that prevented it from fulfilling the request. |

---

### HTTP Authentication Types

1. **Basic Authentication**:
   - Basic authentication involves sending the username and password in an encoded base64 format with each request. It is simple to implement but less secure compared to other methods.

2. **Token-Based Authentication**:
   - Token-based authentication exchanges a token with each request instead of username and password. It is commonly used in APIs for session management.
     Example. JWT token (refresh token, access token)
        
3. **Digest Authentication**:
   - Digest authentication improves security by hashing passwords before sending them over the network.
     Example: Message Digest (MD5 algorithm)
---

### Versions of HTTP

1. **HTTP/1.0**:
   - **Description**: The initial version of HTTP. It introduced basic features for communication between clients and servers.

2. **HTTP/1.1**:
   - **Description**: HTTP/1.1 improved upon HTTP/1.0 by introducing persistent connections, chunked transfer encoding, and host headers.

3. **HTTP/2**:
   - **Description**: HTTP/2 is a major revision of the HTTP protocol designed to improve speed and efficiency of web communications.

4. **HTTP/3**:
   - **Description**: HTTP/3 is the latest version, and is based on **Google's QUIC protocol.** It aims to further optimize performance and security over HTTP/2.

---
# 3. DOMAIN NAME

### Domain Name Definition

A domain name is a human-readable address used to access websites on the Internet. It serves as a unique identifier for a specific location on the web.

### Types of Domain Names

1. **Top Level Domains (TLD)**:
   - **Description**: Highest level in the DNS hierarchy, often referred to as extensions.
   - **Types**:
     - **Country Code Top Level Domain**: Two-letter domains for specific countries (e.g., .in for India, .us for United States).
     - **Generic Top Level Domains**: Open for registration to all users, regardless of citizenship or location (e.g., .com, .net, .org, .edu).

2. **Second Level Domain**:
   - **Description**: Located directly below the TLD in the DNS hierarchy.
   - **Example**: In example.co.in, "co" is the second-level domain under ".in"

3. **Third Level Domain**:
   - **Description**: Located directly below the second-level domain.
   - **Example**: In mail.yahoo.co.in, "yahoo" is the third-level domain under "co" which is under ".in" 

4. **Sub-domain**:
   - **Description**: Part of a higher-level domain name.
   - **Example**: login.yahoo.com is a subdomain of yahoo.com.

---
# 4. HOSTING
Hosting refers to the service that allows individuals and organizations to make their website accessible via the World Wide Web. 
It involves storing website files and data on a server connected to the internet, ensuring that visitors can access the site at any time.

### Hosting Types

1. **Shared Hosting**:
   - Multiple websites **share the same server resources** (CPU, RAM, disk space).
   - Cost-effective option suitable for beginners and small websites.

2. **Virtual Private Server (VPS) Hosting**:
   - **Virtual servers created by partitioning a single physical server**, providing dedicated resources.
   - Offers more control and scalability compared to shared hosting.

3. **Cloud Hosting**:
   - Uses a network of virtual servers to deliver scalable and flexible hosting resources.
   - High reliability and performance with **pay-as-you-go pricing model and on demand delivery of IT resources**.

4. **Dedicated Hosting**:
   - **Entire physical server dedicated to a single customer**, providing full control over resources.
   - Ideal for websites requiring high performance, security, and customization.

---
# 5. DNS
   - DNS translates domain names into IP addresses that computers use to identify each other on the network.
   - It facilitates easy-to-remember domain names instead of relying on numerical IP addresses.

**Operation**:
   - When a user enters a domain name in a web browser, the DNS server translates the domain name into an IP address through a process called DNS resolution.
   - DNS operates in a hierarchical and distributed manner, with different types of DNS servers (e.g., recursive resolver, authoritative nameserver) handling various aspects of the translation process.

     DNS servers invloved are
     - Local DNS Resolver
     - Root DNS Servers
     - Top-Level Domain (TLD) DNS Servers
     - Authoritative DNS Servers

**DNS Caching**:
 - DNS caching involves temporarily storing recently accessed DNS information on a local device or DNS server.
   - It reduces DNS lookup times and improves efficiency.

**DNS Record**:
DNS records are text instructions stored on DNS servers. They indicate the IP address associated with a domain

### DNS Record Types
| Record Type | Description |
|-------------|-------------|
| A           | A record (Address record) maps a domain name to the IPv4 address of the server hosting the domain. |
| AAAA        | AAAA record (IPv6 Address record) maps a domain name to the IPv6 address of the server hosting the domain. |
| MX          | MX record (Mail Exchange record) specifies the mail server responsible for receiving email messages on behalf of the domain. |
| TXT         | TXT record (Text record) carries textual information about the domain.|


---
# 6. BROWSER:

Interprets and renders web pages written in HTML, CSS, and JavaScript, allowing users to navigate websites, interact with content, and access various online resources.

### Working of a browser:

A web browser is a software application installed on a client computer that enables users to access information across the internet. It operates on a client-server model, where the browser acts as the client and communicates with web servers to retrieve and display web pages.

The browser interacts with web servers using the **HTTP protocol**.

1. **Requesting Information**: The browser sends requests to web servers via HTTP or HTTPS protocols. 

2. **Receiving and Rendering Data**: Upon receiving a response from the server, typically in the form of HTML documents, it renders this code into a user-readable format.
   
3. **Displaying Information**: The rendered web page is displayed to the user.


