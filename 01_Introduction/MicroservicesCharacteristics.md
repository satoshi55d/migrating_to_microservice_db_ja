## マイクロサービスの特徴

James Lewis and Martin Fowler provided a reasonable common set of characteristics that fit most of the microservices architectures:

• Componentization via services
• Organized around business capabilities
• Products not projects
• Smart endpoints and dumb pipes
• Decentralized governance
• Decentralized data management
• Infrastructure automation
• Design for failure
• Evolutionary design

All of the aforementioned characteristics certainly deserve their own careful attention.
But after researching, coding, and talking about microservices architectures for a couple of years, I have to admit that the most common question that arises is this:

How do I evolve my monolithic legacy database?

This question provoked some thoughts with respect to how enterprise application developers could break their monoliths more effectively.
So the main characteristic that we’ll be discussing throughout this book is Decentralized Data Management.
Trying to simplify it to a single-sentence concept, we might be able to state that:

Each microservice should have its own separate database.

This statement comes with its own challenges.
Even if we think about greenfield projects, there are many different scenarios in which we require information that will be provided by another service.
Experience has taught us that relying on remote calls (either some kind of Remote Procedure Call [RPC] or REST over HTTP) usually is not performant enough for data-intensive use cases, both in terms of throughput and latency.

This book is all about strategies for dealing with your relational database.
Chapter 2 addresses the architectures associated with deployment.
The zero downtime migrations presented in Chapter 3 are not exclusive to microservices, but they’re even more important in the context of distributed systems.
Because we’re dealing with distributed systems with information scattered through different artifacts interconnected via a network, we’ll also need to deal with how this information will converge.
Chapter 4 describes the difference between consistency models: Create, Read, Update, and Delete (CRUD); and Command and Query Responsibility Segregation (CQRS).
The final topic, which is covered in Chapter 5, looks at how we can integrate the information between the nodes of a microservices architecture.

#### What About NoSQL Databases?

Discussing microservices and database types different than relational ones seems natural.
If each microservice must have is own separate database, what prevents you from choosing other types of technology?
Perhaps some kinds of data will be better handled through key-value stores, or document stores, or even flat files and git repositories.

There are many different success stories about using NoSQL databases in different contexts, and some of these contexts might fit your current enterprise context, as well.
But even if it does, we still recommend that you begin your microservices journey on the safe side: using a relational database.
First, make it work using your existing relational database.
Once you have successfully finished implementing and integrating your first microservice, you can decide whether you (or) your project will be better served by another type of database technology.

The microservices journey is difficult and as with any change, you’ll have better chances if you struggle with one problem at a time.
It doesn’t help having to simultaneously deal with a new thing such as microservices and new unexpected problems caused by a different database technology.