**Java Networking**

Java Networking is the concept of connecting two or more computing devices to exchange data and resources. It allows Java applications to communicate over the internet or local networks.

* All communications in Java networking happen at the application layer.
* The java.net package provides APIs for protocols, sockets, IP addresses, and URLs.
* Java was designed with networking in mind, making distributed computing simpler.
* In Java, networking is supported through the java.net package, which provides classes and interfaces to handle low-level communication, socket programming, and access to network resources.

Common Network Protocols 

1. TCP (Transmission Control Protocol)
TCP is a connection-oriented protocol that ensures data is delivered accurately and in the correct order. It establishes a connection before communication and verifies successful data transfer.

* Reliable and error-checked data transmission
* Maintains data order using acknowledgements
* Used for web applications, file transfer, and emails

2. UDP (User Datagram Protocol)
UDP is a connectionless protocol designed for fast data transmission without delivery guarantees. It sends data packets independently, making it suitable for real-time communication.

* Faster but unreliable compared to TCP
* No connection setup or acknowledgement
* Used in streaming, gaming, and video conferencing

**Socket Programming**
Socket programming enables communication between client and server applications over TCP or UDP.

**JDBC Tutorial**

JDBC (Java Database Connectivity) is a standard Java API that allows Java applications to connect to relational databases. It provides a set of interfaces and classes to send SQL queries, retrieve results and manage database connections. With JDBC, developers can build database-driven applications that are portable across various databases, including MySQL, PostgreSQL, Oracle and others.

**Features of JDBC**

* Platform Independent: Write once, run anywhere (Java-based).
* Database Independent: Works with any relational database using drivers.
* Standard API: Provides a standard set of interfaces (Connection, Statement, ResultSet, etc.).
* Secure: Uses Java security model and exception handling.
* Easy to Use: Simplifies database connectivity with simple method calls.
* Supports SQL: Can execute SQL queries directly from Java code.

