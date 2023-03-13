
---
cssclass:
title: Java
creation-date: 2023-02-01
aliases:
tags:
- Java
---
**[[MAINCODE]]**

---
# Java
#### Introduction
>[!DONE|alt-co no-i collapse]- Why learn Java?
> ▪ The Java programming language was originally created in 1995 by **James Gosling** from Sun Microsystems (currently a subsidiary of Oracle Corporation).
> ▪ The goal was to provide a simpler and platform-independence alternative to [[C++]]
> ▪ The Java Language is object-oriented (OO), which allows you to easily relate program constructs to objects from the real world.
- [[JavaLifeCycle|The Life Cycle of a Java Program]]
- [[JavaJDK&JRE|JDK and JRE]]
- [[JavaSE&EE|Java SE and EE]]
- [[JavaHelloWorld|Hello World Program]]

#### Object-Oriented Programming
- [[JavaClass&Object|Classes and Objects]]
- [[JavaVariables|Variables]]
	- [[JavaVariablesScope|Variable Scope]]
	- [[Javafinal#^c164c7|Constants]]
	- [[JavaWrapperClass|Wrappers, AutoBoxing, & Unboxing]]
- [[JavaVariables|Variables]]
- [[JavaFlowControl|Flow Control]]
- [[JavaInheritance|Inheritance]]

#### Class Methods
- [[JavaMethod|Method]]
	- [[JavaMethodsOverloading|Method Overloading]]
	- [[JavaMethodsOverriding|Method Overriding]]
- [[JavaConstructors|Constructors]]
- [[Javasuper|super Keyword]]
- [[Javathis|this Keyword]]
- [[JavaObjectsPassing|Passing by Value or by Reference]]
- [[JavaClass&ObjectVariableScope|Variable Scopes]]
- [[Javastatic|static Keyword]]

#### Java Basics
- [[JavaArrays|Arrays]]
- [[JavaFlowControl#^217312|Loops]]
- [[JavaDebugging|Debugging Java Programs]]
- [[JavaCommandLine|Command-Line Arguments]]

#### Packages, Interfaces, and Encapsulation
- [[JavaPackages|Java Packages]]
- [[JavaEncapsulation|Encapsulation]]
- [[JavaAccessModifiers|Access Levels]]
- [[Javafinal|final Keyword]] ^07e044
- [[JavaInterface|Interfaces]]
- Marker Interfaces ^e6542d
- Casting

#### Programming w/ Abstract Classes and Interfaces
- Abstract Classes
- Polymorphism
- Interfaces vs Abstract Classes

#### Introduction Graphical User Interface (GUI)
- Swing Basics
- Layout Managers
	- Brief Introduction
	- FlowLayout
	- GridLayout
	- BorderLayout
	- Combining Layout Managers
	- BoxLayout
	- GridBagLayout
	- CardLayout
	- Containers with Absolute Layout
	- More about Swing Widgets
- Swing GUI Builders

#### Event Handling in UI
- Introduction to Event Listeners
- Teaching the Calculator to Calculate
	- Registering Components w/ ActionListener
	- Finding the Source of an Event
	- How to Pass Data between Objects
- More Swing Listeners
- How to Use Adapters
- Inner Classes
	- Anonymous Inner Classes
	- Closures

#### Introduction to Java Applets
- An Unofficial History of Java Applets
- Restrictions of Java Applets
- Learning HTML on the Run
- Writing Applets using Swing
- **Developing a TIC-TAC-TOE Applet**
- **Developing a PING-PONG Game**

#### Error Handling
- Stack Trace
- Java Exceptions
- Exception Hierarchy
- try/catch Blocks
- throw Clause
- throws Clause
- finally Clause
- Creating Your Own Exceptions

#### Introduction to Collections
- Arrays Revisited
- Classes ArrayList and Vector
- Collection Interfaces from java.util
- Classes Hashtable and HashMap
	- Class Properties
- Enumeration and Iterator
- Class LinkedList
- Class BitSet

#### Introduction to Generics
- Generics with Classes
- Defining Generics
- [[JavaWildCard|Wild Cards]] ^406387
- Bounded Wild Cards
- Generic Methods
- What to Read Next

#### Working w/ Streams
- Byte Streams
- Buffered Streams
- Characters Streams
- Data Streams
- The Class File

#### Java Serialization
- The Class ObjectOutputStream
- The Class ObjectInputStream
- The Interface Externalizable
- Class Versioning
- Serializing into Byte Arrays

#### Network Programming
- Reading Data from the Internet
- Connecting through HTTP Proxy Servers
- How to Download Files from the Internet
- The Stock Quote Program
- Socket Programming
	- Why Use Sockets?
	- The Stock Quote Server w/ Sockets

#### Processing E-mail w/ Java
- Protocols and Servers
- **Creating Birthday Mailer**
- How to Retrieve E-Mails
- Useful Open-Source Components

#### Introduction to Multi-Threading
- The Class Thread
- The Interface Runnable
- Sleeping Threads
- How to Kill a Thread
- Thread Properties
- Thread Synchronization and Race Conditions
- Thread States
- Wait and Notify

#### Digging Deeper into ConCurrent Execution
- Joining Threads
- Goodies from java.util.concurrent
	- ReentrantLock vs Synchronized
	- Executor Framework
	- Introduction to Concurrent Collections
- SwingWorker Thread

#### Working w/ Databases using JDBC
- JDBC Driver Types
- Creating a Database w/ Derby
- Processing Result Sets
- The PreparedStatement Class
- The CallableStatement Class
- The ResultSetMetaData Class
- Scrollable Result Sets and RowSet
- Transactional Updates
- Connection Pools and DataSources

#### Swing w/ JTable
- JTable and the MVC Paradigm
- The Model
	- Mandatory Callbacks of Table Models
	- Optional Callbacks of Table Models
- Introduction to Renderers
- Summary

#### Annotations and Reflection
- Java Annotations Basics
	- @Override
	- @Deprecated
	- @Inherited
	- @Documented
- Custome Annotations
- Reflection
- Run-Time Annotation Processing
- Summary

#### Remote Method Invocation
- Developing Application w/ RMI
	- Defining Remote Interfaces
	- Implementing Remote Interfaces
	- Registering Remote Objects
	- Writing RMI Clients
	- Security Considerations
	- Finding Remote Objects

#### Java EE 6 Overview
- The Big Picture
	- JCP, JSR, and Other Acronyms
	- Tiers of Java EE Applications
	- Containers versus Application Servers
- Profiles and Pruning
- Miscellaneous Concepts

#### Programming w/ Servlets
- The Big Picture
- The Thin Client
- How to Write a Servlet
- How to Deploy a Servlet
- How to Create a Servlet
- Browser-Servlet Data Flow
- HTTP Get and Post Requests
- Session Tracking
	- Cookies
	- URL Rewriting
	- Server-Side HttpSession
	- Filters
- Event Listeners
- Asynchronous Servlets

#### Java Server Pages
- Embedding Java Code into HTML
- Implicit JSP Objects
- Overview of the JSP Tags
	- Directives
	- Declarations
	- Expressions
	- Scriptlets
	- Comments
	- Standard Actions
- Error Pages
- JavaBeans
	- Using JavaBeans in JSP
	- How Long Does a Bean Live?
- Loading JSP from Servlets
- Tag Libraries
- JSTL

#### Developing Web Application w/ JSF
- The Big Picture
- Managed Beans
- Creating a JSF Website
	- Templating
	- Page Navigation
- Converters and Validators

#### Introducing JMS and MOM
- Messaging Concepts and Terminology
- Two Modes of Message Delivery
- JSM API Overview
- Types of Messages
- How to Send a Message
- How to Receive a Message
- How to Publish a Message
- How to Subscribe for a Topic
- Message Selectors
- Administering Objects in Open MQ

#### Introducing JNDI
- Java Naming and Directory Interface
- Administering JNDI Objects in GlassFish
- Accessing the GlassFish Naming Service w/ JNDI
- Injection of JNDI Resources
- DataSource and JNDI
- Lightweight Directory Access Protocol

#### Introduction to Enterprise JavaBeans
- Who needs EJB Containers
- Types of EJBs
- Stateless Sessions Beans
	- The Bean
	- The Client's View
	- The Server
	- Asynchronous Methods
- Stateful Session Beans
- Singleton Beans
- Deploying EJB
- Message-Driven Beans
- Timer Service
- Summary

#### Introduction to the Java Persistence API
- The Big Picture
- Mapping Objects to Database Tables
- JPQL
- EntityManager
- Brief Introduction to the Criteria API
- Bean Validation

#### Working w/ Restful Web Services
- The SOAP Web Services
- The RESTful Web Services
- The RESTful Stock Server

#### Introductiong to Spring MVC Framework
- Bean Writing
- Overview of Spring MVC
- Processing HTML w/ Spring
	- Understanding w/ Spring Web MVC Workflow
	- Processing HTML Forms

#### Introduction to Hibernate Framework
- The Big Picture
- Installing and Configuring Hibernate
	- Adding Hibernate Jars to an Eclipse Project
	- Testing the Database Connection
	- Configuring Hibernate w/ a DBMS
- Retrieving Data w/ Hibernate

#### Bringing JavaFX to the Mix
- Consuming Stock Quotes w/ JavaFX
- Code Walkthrough
	- Reading JavaFX Code
	- The HTML Client

#### Java Technical Interviews
- Getting the Interview
- Doing Well at the Interview
- Considering the Offer
- Interviewing Enterprise Developers
- To Get or Not to Get Certified?
- Technical Questions and Answers
- Epilogue