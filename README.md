# History-of-HTTP

HTTP - Hypertext Transfer Protocol

Invented by Tim Berners-Lee at CERN in the year 1989-1991,The Hypertext Transfer Protocol (HTTP) is one of the most ubiquitous and 
widely adopted application protocols on the Internet:it is the common language between clients and servers, enabling the modern web.
From its simple beginnings as a single keyword and document path, it has become the protocol of choice not just for browsers, but for virtually every 
Internet-connected software and hardware application.

We will take a brief historical tour of the evolution of the HTTP protocol. A full discussion of the varying HTTP semantics is outside the scope of this lesson, 
but an understanding of the key design changes of HTTP, and the motivations behind each, will give us the necessary background for our discussions on HTTP performance, 
especially in the context of the many upcoming improvements in HTTP/2.

      1) HTTP 0.9: The One-Line Protocol
      
   In 1991, Berners-Lee outlined the motivation for the new protocol and listed several high-level design goals: file transfer functionality, 
   ability to request an index search of a hypertext archive, format negotiation, and an ability to refer the client to another server. To prove the theory in action, 
   a simple prototype was built, which implemented a small subset of the proposed functionality 
    
   HTTP took on a life of its own and evolved rapidly over the coming years. Let us quickly recap the features of HTTP 0.9:
   

                a) Client-server, request-response protocol.

                b) ASCII protocol, running over a TCP/IP link.

                c) Designed to transfer hypertext documents (HTML).

                d) The connection between server and client is closed after every request.
                
   
     2) HTTP/1.0: Rapid Growth and Informational RFC
     
   The period from 1991 to 1995 is one of rapid coevolution of the HTML specification, a new breed of software known as a “web browser,” 
   and the emergence and quick growth of the consumer-oriented public Internet infrastructure.

   The growing list of desired capabilities of the nascent Web and their use cases on the public Web quickly exposed many of the fundamental limitations of HTTP 0.9:
   we needed a protocol that could serve more than just hypertext documents, provide richer metadata about the request and the response, enable content negotiation, 
   and more. In turn, the nascent community of web developers responded by producing a large number of experimental HTTP server and client implementations through 
   an ad hoc process: implement, deploy, and see if other people adopt it.

  From this period of rapid experimentation, a set of best practices and common patterns began to emerge, and in May 1996 the HTTP Working Group (HTTP-WG) 
  published RFC 1945, which documented the “common usage” of the many HTTP/1.0 implementations found in the wild. Note that this was only an informational RFC: 
  HTTP/1.0 as we know it is not a formal specification or an Internet standard!


                 a) Request may consist of multiple newline separated header fields.

                 b) Response object is prefixed with a response status line.

                 c) Response object has its own set of newline separated header fields.

                 d) Response object is not limited to hypertext.

                 e) The connection between server and client is closed after every request.

    3) HTTP/1.1: Internet Standard

  The work on turning HTTP into an official IETF Internet standard proceeded in parallel with the documentation effort around HTTP/1.0 and happened over a period 
  of roughly four years: between 1995 and 1999. In fact, the first official HTTP/1.1 standard is defined in RFC 2068, which was officially released in January 1997, 
  roughly six months after the publication of HTTP/1.0. Then, two and a half years later, in June of 1999, a number of improvements and updates were incorporated 
  into the standard and were released as RFC 2616.

  The HTTP/1.1 standard resolved a lot of the protocol ambiguities found in earlier versions and introduced a number of critical performance optimizations: keepalive 
  connections, chunked encoding transfers, byte-range requests, additional caching mechanisms, transfer encodings, and request pipelining.

                a) Request for HTML file, with encoding, charset, and cookie metadata

                b) Chunked response for original HTML request

                c) Number of octets in the chunk expressed as an ASCII hexadecimal number (256 bytes)

                d) End of chunked stream response

                e) Request for an icon file made on same TCP connection

                f) Inform server that the connection will not be reused

                g) Icon response, followed by connection close
                
   4) HTTP/2: Improving Transport Performance
   
 HTTP/2 changes to improve the internet experience.The primary goal with research and development for a new version of HTTP centers around three qualities rarely 
 associated with a single network protocol without necessitating additional networking technologies – simplicity, high performance and robustness. These goals are 
 achieved by introducing capabilities that reduce latency in processing browser requests with techniques such as multiplexing, compression, request prioritization 
 and server push.
 
 Mechanisms such as flow control, upgrade and error handling work as enhancements to the HTTP protocol for developers to ensure high performance and resilience of 
 web-based applications.

 The collective system allows servers to respond efficiently with more content than originally requested by clients, eliminating user intervention to continuously 
 request for information until the website is fully loaded onto the web browser. For instance, the Server Push capability with HTTP/2 allows servers to respond with 
 a page’s full contents other than the information already available in the browser cache. Efficient compression of HTTP header files minimizes protocol overhead to 
 improve performance with each browser request and server response.

 HTTP/2 changes are designed to maintain interoperability and compatibility with HTTP1.1. HTTP/2 advantages are expected to increase over time based on real-world 
 experiments and its ability to address performance related issues in real-world comparison with HTTP1.1 will greatly impact its evolution over the long term
 
              Features are:-  
              a) Header Compression  
              b) Server Push 
              c) Stream Dependencies 
              d) Multiplexing 
              all contribute toward improved network utilization as a key HTTP/2 advantage
