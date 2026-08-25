What is JSP?

JavaServer Pages (JSP) is a server-side technology used to create dynamic, platform-independent web applications.
It allows developers to embed Java code directly into HTML pages, making it easier to build interactive and data-driven websites.

Key Features
1. Server-Side Execution – JSP code runs on the server before sending HTML to the browser.
2. Java Integration – You can use Java classes, libraries, and APIs directly in JSP.
3. Separation of Concerns – Presentation (HTML) is separated from business logic (Java code).
4. Reusable Components – Supports JavaBeans, Custom Tags, and JSTL for modular development.
5. Automatic Compilation – JSP files are compiled into Servlets by the server.

JSP Lifecycle
1. Translation – JSP file is converted into a Servlet.
2. Compilation – The Servlet is compiled into bytecode.
3. Loading & Initialization – Servlet is loaded and jspInit() is called.
4. Request Processing – jspService() handles client requests.
5. Destruction – jspDestroy() is called before unloading.

--------------------------------------------------------------------

In JSP (JavaServer Pages), Scripting Elements allow you to embed Java code directly into your JSP file so that it executes on the server before sending the HTML response to the client.

There are three main types of scripting elements in JSP:

1. Declaration Tag (<%! ... %>)
Used to declare variables and methods that become part of the servlet class generated from the JSP.
Code inside <%! ... %> is placed outside the _jspService() method, so it can be reused across requests.

<%! 
    int counter = 0; // Instance variable
    public String greet(String name) {
        return "Hello, " + name;
    }
%>

<p><%= greet("John") %></p>

2. Scriptlet Tag (<% ... %>)
Used to write Java code logic inside the _jspService() method.
Can contain loops, conditionals, and other Java statements.
Avoids printing directly; use out.print() for output.

<%
    for (int i = 1; i <= 5; i++) {
        out.println("Number: " + i + "<br>");
    }
%>

3. Expression Tag (<%= ... %>)
Used to output the result of a Java expression directly into the HTML response.
Automatically calls toString() and does not require out.print().

<p>Current Time: <%= new java.util.Date() %></p>


