# MicroServices-concepts

What are Monolothics ?
Monolothics architecture is consider a traditional way of application development in where it is built on single and divisible unit a client site user interface , business logic , database interface  to access database . they are on same server. Monolothics architecture is present from 2 decades. 
Limited Scalability for each functionality

What are Microservices?
Microservices are suite of small services , autonomously developed, independently deployable decentralized and build and released with automated process. 
Microservices provide a solution that is unique , distinct within the eco-system.
Microservices are an architectural and organizational approach to software development where software is composed of small independent services that communicate over well-defined APIs. These services are owned by small, self-contained teams.
Microservices architectures make applications easier to scale and faster to develop, enabling innovation and accelerating time-to-market for new features.
Monolithic vs. Microservices Architecture
With monolithic architectures, all processes are tightly coupled and run as a single service. This means that if one process of the application experiences a spike in demand, the entire architecture must be scaled. Adding or improving a monolithic application’s features becomes more complex as the code base grows. This complexity limits experimentation and makes it difficult to implement new ideas. Monolithic architectures add risk for application availability because many dependent and tightly coupled processes increase the impact of a single process failure.
With a microservices architecture, an application is built as independent components that run each application process as a service. These services communicate via a well-defined interface using lightweight APIs. Services are built for business capabilities and each service performs a single function. Because they are independently run, each service can be updated, deployed, and scaled to meet demand for specific functions of an application.

https://www.freelancinggig.com/blog/2019/02/19/understanding-monolith-vs-microservices-vs-serverless/
https://thecustomizewindows.com/2019/04/serverless-functions-vs-microservices/
https://www.infoq.com/articles/serverless-microservices-flexibility/
https://www.byteant.com/blog/serverless-vs-microservices-architecture-what-does-the-future-of-business-computing-look/


https://thecustomizewindows.com/2019/04/serverless-functions-vs-microservices/

https://thecustomizewindows.com/2019/04/serverless-functions-vs-microservices/
Breaking a monolithic application into microservices
Characteristics of Microservices
 
Autonomous
Each component service in a microservices architecture can be developed, deployed, operated, and scaled without affecting the functioning of other services. Services do not need to share any of their code or implementation with other services. Any communication between individual components happens via well-defined APIs.
 
Specialized
Each service is designed for a set of capabilities and focuses on solving a specific problem. If developers contribute more code to a service over time and the service becomes complex, it can be broken into smaller services.
Benefits of Microservices
 
Agility
Microservices foster an organization of small, independent teams that take ownership of their services. Teams act within a small and well understood context, and are empowered to work more independently and more quickly. This shortens development cycle times. You benefit significantly from the aggregate throughput of the organization.
 
Flexible Scaling
Microservices allow each service to be independently scaled to meet demand for the application feature it supports. This enables teams to right-size infrastructure needs, accurately measure the cost of a feature, and maintain availability if a service experiences a spike in demand.
 
Easy Deployment
Microservices enable continuous integration and continuous delivery, making it easy to try out new ideas and to roll back if something doesn’t work. The low cost of failure enables experimentation, makes it easier to update code, and accelerates time-to-market for new features.
 
Technological Freedom
Microservices architectures don’t follow a “one size fits all” approach. Teams have the freedom to choose the best tool to solve their specific problems. As a consequence, teams building microservices can choose the best tool for each job.
 
Reusable Code
Dividing software into small, well-defined modules enables teams to use functions for multiple purposes. A service written for a certain function can be used as a building block for another feature. This allows an application to bootstrap off itself, as developers can create new capabilities without writing code from scratch.
 
Resilience
Service independence increases an application’s resistance to failure. In a monolithic architecture, if a single component fails, it can cause the entire application to fail. With microservices, applications handle total service failure by degrading functionality and not crashing the entire application.

====================================================================
Microservices and serverless are both important topics in the world of cloud-native computing. Yet, although serverless functions and microservices architectures often go hand-in-hand, they’re distinct technologies that fill different roles in modern software environments.
Here’s an overview of what microservices and serverless are, how they relate to each other, how they are different, and why you may or may not wish to deploy a serverless microservice.
What Are Microservices?
The term “microservices” refers to an architectural pattern in which applications are broken down into a series of small services (hence the term “microservice”). Microservices architectures are the opposite of so-called monoliths (meaning applications where all functionality runs as a single entity).
As a simple example of a microservices application, imagine a shopping app that lets users search for products, place them in their carts, and then complete their purchases. This app could be implemented as a series of discrete microservices:
•	A frontend application interface.
•	A search service that looks up products in a database based on user-generated search queries.
•	A product-detail service that displays additional information about products that users click on.
•	A shopping cart service to keep track of items that users place in their cart.
•	A checkout service that handles the payment process.
This is just an example. In the real world, microservices applications can be implemented in a variety of ways. There are no hard-and-fast rules regarding how application functionality should be distributed across different microservices.
Indeed, there’s not even a rule stating that you need a certain number of services for your application to count as an example of microservices. Technically, you could implement just a couple of services and call it a microservices app, although most developers include at least several microservices in each app.
Although the concepts at the core of microservices date back decades (as evidenced by the microkernel hype in the 1980s and 1990s and the SOA trend of the 2000s, for example), it has only been over the past ten years or so that microservices have become immensely popular. That’s thanks largely to the scalability and flexibility that microservices bring to applications running in distributed, cloud-based environments. When you are deploying multiple instances of an application across dozens or more servers, microservices help ensure that you can distribute the load more equitably by running different microservices on different servers.
Microservices can also improve application reliability and performance by spreading out your application’s footprint: if one microservice fails, the rest of your application keeps running, so your users don’t get completely locked out. In addition, because microservices are smaller than entire apps, it’s faster to spin up a new microservice to replace a failed instance (or to add capacity if your application load increases) than it would be to reload the entire application.
Serverless
Serverless is a model in which application code is executed on-demand in response to triggers that application developers configure ahead of time.
The code that runs in this way (which is called a serverless function) could represent an entire application. However, it is more common to use serverless functions to implement discrete units of application functionality.
For example, a typical use case for serverless is to run an application service that resizes images uploaded by users. In this scenario, developers would set up triggers that execute the serverless function whenever a user uploads a new image to the application. The serverless function would then do its job and stop running as soon as it’s complete.
The main benefit of serverless is that it offers an efficient way to execute code that doesn’t need to run on a continuous basis. Without serverless, you’d have to keep all parts of your application running constantly, which would waste resources. Serverless functions allow you to configure certain parts of your application to run only when they’re needed.
Thus, an application frontend typically wouldn’t be a good fit for a serverless function, because it needs to run all of the time to keep users logged in. But an authentication service that is only requested occasionally could be a good candidate for serverless.
Serverless also offers the benefit of simplified deployment and configuration. Instead of requiring developers to configure an entire operating system environment, serverless lets them upload the functions they want to run, configure the triggers for them, and call it a day.
Like microservices, the concepts that gave rise to serverless have been around for a long time. But serverless didn’t come into its own until the cloud-native era. Specifically, the introduction of Lambda (Amazon’s serverless framework) in 2014 touched off the modern serverless era. Today, all of the major cloud providers offer serverless platforms. Third-party serverless frameworks that can run on cloud IaaS infrastructure or on-premises, such as Kubeless and OpenFaaS, are also available.
Serverless Microservices
Thus, serverless and microservices are different sorts of technologies. Microservices is a way to design an application, while serverless is a way to run an application (or a part of an application).
Nonetheless, serverless and microservices are closely related. Not only are they both common technologies within cloud-based environments, but serverless functions are one way to host microservices.
In other words, you can create a “serverless microservice” by writing the code for a microservice and then setting it up to run as a serverless function. Any microservice that needs to run only occasionally is a good candidate for a serverless microservice deployment model, for the reasons noted above.
Serverless and microservices are also comparable in that they require similar approaches to monitoring and management. The more microservices and/or serverless functions you include in your environment, the more moving pieces you have to keep track of, and the more robust your monitoring and log management tools need to be.
Differences between Serverless and Microservices
This isn’t to say that microservices and serverless always go hand-in-hand. It’s rare to run every microservice in an application as a serverless function. Typically, as we’ve discussed, you would have microservices (like app frontends) that need to run constantly, and these would not work well within a serverless environment. You’d be better off deploying them inside containers.
 


You also don’t have to use a microservices architecture in order to take advantage of serverless functions. There’s nothing stopping you from deploying a monolithic application on a serverless platform, although it’s difficult to imagine many use cases where this would offer real benefits. You would not be able to take advantage of the efficiency that serverless offers if you have a monolith and can’t separate application units that must run all the time from those that are only needed at certain times.
It’s worth noting as well that serverless environments may include dozens of different serverless functions, some of which could be shared by multiple applications. (Again, to go back to the example of a serverless function that resizes images, you might have multiple applications running that need that functionality, so you would share the function between them.) In contrast, it would be rare (though by no means impossible) to have dozens of microservices running in a single application. It is also not common to share the same microservice across multiple applications, unless it’s a service that provides auxiliary functionality (like log collection) rather than core application functionality.
Some observers also suggest that serverless remains less mature than microservices, but this is debatable and depends to some extent on how you define serverless and microservices. Both types of technology have existed for a number of years at this point, and it would be hard to make the case that either is not yet mature enough for production deployment.
That said, you could argue that the tooling surrounding serverless functions is less mature than it is for microservices. There are plenty of solutions that can monitor and manage microservices applications. Support for serverless monitoring and log management can be more difficult to find, due especially to the fact that the serverless market remains fragmented. No two serverless platforms are identical; they all support different languages, and you can’t drag-and-drop a serverless function from, say, AWS Lambda into Azure Functions without reconfiguring it at least partially. Thus, the tooling for serverless monitoring and management remains somewhat platform-specific. In this sense, at least, serverless is a bit less developed than microservices.
Nonetheless, Sumo Logic does support log management and analysis for both microservices architectures and serverless functions. It’s easy to take logs from a serverless environment like Lambda and move them to Sumo Logic for analysis. You can also manage logs from any microservices environment using Sumo Logic, just as you could for a monolith.
Conclusion
If you like analogies, you might say that serverless is like French fries and microservices are like ketchup: they go well together, but they don’t always have to go together. You can eat French fries with mustard or pair your ketchup with a hamburger, just as you could implement microservices without serverless functions or use serverless to run functions that are not discrete microservices.
If you don’t like analogies, you can put it this way: serverless is one way to host microservices, but it’s not the only way. Nor do you deploy and manage microservices in exactly the same way as serverless functions. Both technologies offer important advantages for cloud-native computing, but they solve different sorts of problems.


 

 



 


•	SOA is focused on application service reusability while Microservices are more focused on decoupling.
•	SOA involves sharing data storage between services while in Microservices, each service can have independent data storage.
•	SOA is designed to share resources across services while Microservices is designed to host services that can function independently.
•	SOA is a less scalable architecture while Microservices is highly scalable architecture.
What is coupling and Cohesion ?
Coupling shows the relationships between modules. Coupling shows the relative independence between the modules.  Coupling is to measure of degree of interdependence class knows about another modules. Loosely coupled (modules are programming lang -package to packages
Cohesion shows the relationship within the module.  Cohesion shows the module's relative functional strength. Degree to which all elements(member functions) directed towards performing a single modules. ( within each module are programming lang -functions or methods) 

 










https://www.youtube.com/watch?v=9QTsXLB6Al8
 
MicroService Design Patterns 
Categaries into 5 patters as per their design patters
Decomposition patterns: to helps to break into small services
Integration patterns: focus on  inter communication between the services and other components.

Database patterns: to provides solution to connect with data structure
Observability patterns : helps in enabling logging and appling matrix and designing distributed traffic 
Cross-cutting Concerns patterns : can provide the solution for service discovery and handling fault tolerance . Define right architure for 0 downtime support site extra.

Important key design principles Rules and guideline for Micro services  
Domain (subject area -core area) driven design
1.	Build Around business capabilities
2.	Single responsibility principle
3.	High cohesion and low coupling
4.	Decentralized data
5.	Failure isolation
6.	Fault tolerant
7.	Hexagonal Architecture
8.	Continuous Delivery with DevOps
9.	Continuous Monitoring and Distributed tracing


Decomposition patterns – In details

2.Decompose by Sub domain
 


3.
 


4.

5.
  

5. Sidecar 
 
