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

# Bootstrap

Depolyed landing page site link: https://xyz-travels.netlify.app/

    <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Travel Agency Landing Page</title>
            <link rel="preconnect" href="https://fonts.googleapis.com">
            <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
            <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
            <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
            <style>
                .carousel-item {
                    height: 730px; 
                }

        .carousel-item img {
            height: 100%;
            object-fit: cover;
        }

        .carousel-caption {
            top: 50%;
            transform: translateY(-50%);
            bottom: initial;
        }

        .lead{
            text-align: justify;
            padding-left: 80px;
            padding-right: 80px;
        }

        .display-6{
            text-align: center;
            font-weight: 300;
        }

        .s2{
            background-color: antiquewhite;
        }
      
        .display-6 {
            font-family: "Dancing Script", cursive;
            font-optical-sizing: auto;
            font-weight: 400;
            font-size: 60px;
            font-style: normal;
          }

        .s1{
        padding-left: 980px;
        }

    </style>
    </head>
      <body>
    
    <!-- Bootstrap Navbar  -->

    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <a class="navbar-brand" href="#">&nbsp;&nbsp;&nbsp; XYZ Travels</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
            <div class="navbar-nav">
                <a class="nav-item nav-link active" href="#home">Home</a>
                <a class="nav-item nav-link" href="#about-us">About Us</a>
                <a class="nav-item nav-link" href="#products">Packages</a>
                <a class="nav-item nav-link" href="#contacts">Contact</a>
                <div class="s1">
                <button type="button" class="btn btn-primary">Sign Up </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Bootstrap Carousal -->

    <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="image1.jpg" class="d-block w-100" alt="...">
            <div class="carousel-caption d-none d-md-block">
              <h1 class="display-1">XYZ Travel Agency</h1>  
              <h5>We turn your travel dreams into reality. Whether you're seeking a tranquil beach escape, an adventurous mountain trek, or a cultural city tour, we offer personalized travel experiences that cater to all your desires.</h5>
            </div>
          </div>
          <div class="carousel-item">
            <img src="image3.jpg" class="d-block w-100" alt="...">
            <div class="carousel-caption d-none d-md-block">
              <h1 class="display-1">XYZ Travel Agency</h1>
              <h5>Our expert team is dedicated to crafting unique and unforgettable journeys tailored to your interests and budget.</h5>
            </div>
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
        <br />


      <!-- Bootstrap lead and display headings -->
      <section id="about-us">   
        <br />
        <br />
        <br />
        <h1 class="display-6">About us</h1>   
        <p class="lead">
            Welcome to XYZ Travel Agency, where we transform your travel dreams into reality. Whether you're seeking a serene beach escape, an adventurous mountain trek, or a vibrant cultural city tour, we specialize in crafting personalized travel experiences that cater to your unique desires. Our expert team is committed to providing you with tailored itineraries, insider tips, and seamless travel arrangements, ensuring an unforgettable journey. With exclusive deals, 24/7 support, and a passion for exceptional service, we take care of every detail, allowing you to explore the world with confidence and excitement. Discover your next adventure with us, where your perfect getaway awaits.
        </p>
        <br />
        <br />
      </section>

<!-- Bootstrap Footer -->

      <footer class="text-center text-lg-start  bg-dark text-light">
          <section class="d-flex justify-content-center justify-content-lg-between">
      <div>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-facebook-f"></i>
        </a>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-twitter"></i>
        </a>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-google"></i>
        </a>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-instagram"></i>
        </a>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-linkedin"></i>
        </a>
        <a href="" class="me-4 text-reset">
          <i class="fab fa-github"></i>
        </a>
      </div>
    </section>
  
    <section class="">
      <div class="container text-center text-md-start mt-5">
        <div class="row mt-3">
          <div class="col-md-3 col-lg-4 col-xl-3 mx-auto mb-4">            
            <h6 class="text-uppercase fw-bold mb-4">
              <i class="fas fa-gem me-3"></i>XYZ Travels
            </h6>
            <p>
                Welcome to XYZ Travel Agency, where we transform your travel dreams into reality. 
            </p>
          </div>
  
          <div class="col-md-2 col-lg-2 col-xl-2 mx-auto mb-4">
            <h6 class="text-uppercase fw-bold mb-4">
              Our Agency
            </h6>
            <p>
              <a href="#!" class="text-reset">About</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Contacts</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Our Team</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Reviews</a>
            </p>
          </div>
  
          <div class="col-md-3 col-lg-2 col-xl-2 mx-auto mb-4">

            <h6 class="text-uppercase fw-bold mb-4">
              Useful links
            </h6>
            <p>
              <a href="#!" class="text-reset">Packages</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Pricing</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Members</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Help</a>
            </p>
          </div>
  
          <div class="col-md-4 col-lg-3 col-xl-3 mx-auto mb-md-0 mb-4">
            <h6 class="text-uppercase fw-bold mb-4">Contact</h6>
            <p><i class="fas fa-home me-3"></i> Chennai 600 004, India</p>
            <p>
              <i class="fas fa-envelope me-3"></i>
              xyztravels@gmail.com
            </p>
            <p><i class="fas fa-phone me-3"></i> + 91 90234567888</p>
            <p><i class="fas fa-print me-3"></i> + 91 90234567889</p>
          </div>
        </div>
      </div>
    </section>
  
    <div class="text-center p-4" style="background-color: rgba(0, 0, 0, 0.05);">
      © 2024 Copyright:
      <a class="text-reset fw-bold" href="https://mdbootstrap.com/">xyztravels.com</a>
    </div>
    </footer>
    </body>
    </html>
 



![image](https://github.com/user-attachments/assets/abbcf264-90a3-4eab-b7f6-506c019efe47)

![image](https://github.com/user-attachments/assets/1d0aed22-ca84-46f6-870a-7d7d1d6691dd)


Utilized,

- Bootstrap Carousal
- Typography
- Navbar
- Footer
- Button
- Lead element
- Display and Heading text

  ---

  
