# springboot basics 

What is JDBC?

* JDBC (Java Database Connectivity) is an API in Java that facilitates communication between Java applications and relational databases. It enables Java programs to connect to databases, execute SQL queries, retrieve results, and manipulate data.

* JDBC supports various databases like MySQL, Oracle, and PostgreSQL, making it a versatile tool for database operations.

# Key Components of JDBC

JDBC consists of several essential components:

1. JDBC API: Provides interfaces and classes to interact with databases. Key interfaces include Connection, Statement, PreparedStatement, ResultSet, and CallableStatement. Classes like DriverManager and Types help manage database connections and data types.

2. DriverManager: Manages database drivers and establishes connections between Java applications and databases.

3. JDBC Drivers: These are client-side adapters that convert Java program requests into a protocol that the database management system (DBMS) understands. There are four types of JDBC drivers: Type-1: JDBC-ODBC Bridge Driver (deprecated in modern Java versions). Type-2: Native-API Driver. Type-3: Network Protocol Driver. Type-4: Thin Driver (widely used and fully Java-based).


**JDBC Architectures**

JDBC supports two main processing models:

1. Two-Tier Architecture: The Java application communicates directly with the database using a JDBC driver. This is common in client-server setups.

2. Three-Tier Architecture: The application interacts with a middle-tier service (e.g., an application server), which then communicates with the database. This model is often used in enterprise applications.


**Standard Steps followed for developing JDBC(JDBC4.X) Application**
1. Load and register the Driver
2. Establish the Connection b/w java application and database
3. Create a Statement Object
4. Send and execute the Query
5. Process the result from ResultSet
6. Close the Connection

**The Four Types of JDBC Drivers**

Java Database Connectivity (JDBC) drivers are essential components that enable Java applications to interact with databases. Sun Microsystems (now Oracle) defined four types of JDBC drivers, each with unique characteristics and use cases.

1. Type-1 Driver (JDBC-ODBC Bridge Driver)

This driver uses an ODBC driver to connect to the database. It translates JDBC method calls into ODBC function calls.

-- Advantages: Built into JDK, database-independent, and easy to use for testing.

-- Disadvantages: Requires ODBC installation on client machines, lacks portability, and is not secure. It is typically used for development and testing purposes only.

2. Type-2 Driver (Native-API Driver)

This driver converts JDBC calls into native database API calls using client-side libraries provided by the database vendor.

-- Advantages: Offers better performance and security compared to Type-1 drivers.

-- Disadvantages: Requires installation of vendor-specific libraries on client machines, is database-dependent, and lacks portability as it is not fully written in Java.

3. Type-3 Driver (Network Protocol Driver)

This driver uses middleware (application server) to convert JDBC calls into database-specific protocol calls.

-- Advantages: Fully written in Java, portable, and does not require client-side libraries. It supports switching between databases and provides features like load balancing and logging.

-- Disadvantages: Requires network support on the client machine and can be costly to maintain due to middleware configuration.

4. Type-4 Driver (Thin Driver)

This driver directly communicates with the database using the database's native protocol, without requiring middleware or native libraries.

-- Advantages: Fully written in Java, portable, and does not require client-side or server-side installations. It is the most efficient and commonly used driver.

-- Disadvantages: A new driver may be required if the database changes.

* Choosing the Right Driver

@ Use Type-4 for single-database access (e.g., Oracle, MySQL).

@ Use Type-3 for applications accessing multiple databases.

@ Use Type-2 when Type-3 or Type-4 drivers are unavailable.

@ Avoid Type-1 for production; it is suitable only for testing and development.

