**Introduction to Java Servlets**

A Java Servlet is a server-side Java program that runs within a Servlet Container (like Apache Tomcat, Jetty, or GlassFish) to handle client requests, process them, and generate dynamic responses. Servlets are part of the Jakarta EE (formerly Java EE) specification and are widely used for building scalable, efficient web applications.

They work by extending the capabilities of a web server, enabling dynamic content generation and interaction with databases, APIs, and other resources. Unlike older technologies like CGI, servlets are more efficient because they run within the server process and reuse threads instead of creating new processes for each request.

Core Workflow

-- Client sends a request to the web server.

-- Web server forwards the request to the servlet container.

-- Servlet processes the request (via doGet() or doPost()).

-- Response is generated and sent back to the client.


A Servlet is a Java program running on a server to handle client requests and generate dynamic responses. Its life cycle is fully managed by the Servlet container, which controls creation, execution, and destruction of the servlet instance. The process ensures efficient resource management and scalability.

** Key Phases of the Servlet Life Cycle:

1. Loading and Instantiation The container loads the servlet class into memory and creates an instance using the no-argument constructor.

Loading can occur at server startup (if configured) or on the first request (lazy loading).

This happens only once in the servlet’s lifetime.

2. Initialization (init() method) After instantiation, the container calls:

@Override
public void init() throws ServletException {
// Initialization logic (e.g., DB connection setup)
}
Copy
Executed once to prepare the servlet for handling requests.

Ideal for resource setup like database connections or configuration loading.

Throwing ServletException here prevents the servlet from entering service state.

3. Request Handling (service() method) For each client request, the container invokes:

@Override
public void service(ServletRequest req, ServletResponse res)
throws ServletException, IOException {
// Process request and generate response
}
Copy
Determines HTTP method (GET, POST, PUT, DELETE) and delegates to doGet(), doPost(), etc.

Runs in multiple threads for concurrent requests, so thread safety is crucial.

4. Destruction (destroy() method) When the servlet is removed from service, the container calls:

@Override
public void destroy() {
// Cleanup logic (e.g., close DB connections)
}
Copy
Executed once before garbage collection.

Used to release resources and perform final cleanup.

------------------------------------------------------------------------------

Creating a Java servlet involves setting up a directory structure, writing the servlet class, compiling it, configuring deployment, and running it on a web server like Tomcat.

Step 1: Set Up Directory Structure
Create a structured hierarchy for your web application inside the web server’s webapps folder. Typically:

Place HTML or static files directly under the application folder.
Place compiled servlet classes in WEB-INF/classes.
Place the deployment descriptor web.xml in WEB-INF.
Include any required JAR files in WEB-INF/lib 

Step 2: Create the Servlet Class
Write a Java class that extends HttpServlet. Override either doGet() or doPost() methods depending on the type of request you want to handle. Example:

import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;
public class HelloWorldServlet extends HttpServlet {
    public void doGet(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        response.setContentType("text/html");
        PrintWriter out = response.getWriter();
        out.println("<h1>Hello, World!</h1>");
    }
}

Step 3: Compile the Servlet
Compile the Java file using the servlet API JAR (usually servlet-api.jar from Tomcat). For example:

javac -cp path_to_tomcat/lib/servlet-api.jar HelloWorldServlet.java

Step 4: Configure Deployment
You can configure the servlet in two ways:
Using web.xml:

<web-app>
    <servlet>
        <servlet-name>HelloWorld</servlet-name>
        <servlet-class>HelloWorldServlet</servlet-class>
    </servlet>
    <servlet-mapping>
        <servlet-name>HelloWorld</servlet-name>
        <url-pattern>/hello</url-pattern>
    </servlet-mapping>
</web-app>

Using Annotations (Servlet 3.0+):

@WebServlet("/hello")
public class HelloWorldServlet extends HttpServlet {
    // doGet() method
}


Step 5: Deploy and Run
Place your application folder inside Tomcat’s webapps.
Start the Tomcat server.
Access the servlet via a browser at http://localhost:8080/yourApp/hello

Step 6: Test and Verify
Ensure the servlet responds correctly to requests. You can modify the servlet to handle different request types, generate dynamic content, or interact with databases using JDBC

-----------------------------------------------------------------------------