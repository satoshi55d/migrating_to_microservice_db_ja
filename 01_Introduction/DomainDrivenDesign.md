## ドメイン駆動設計

It’s interesting how some methodologies and techniques take years to “mature” or to gain awareness among the general public.
And Domain-Driven Design (DDD) is one of these very useful techniques that is becoming almost essential in any discussion about microservices.
Why now?
Historically we’ve always been trying to achieve two synergic properties in software design: high cohesion and low coupling.
We aim for the ability to create boundaries between entities in our model so that they work well together and don’t propagate changes to other entities beyond the boundary.
Unfortunately, we’re usually especially bad at that.

DDD is an approach to software development that tackles complex systems by mapping activities, tasks, events, and data from a business domain to software artifacts.
One of the most important con‐ cepts of DDD is the bounded context, which is a cohesive and well- defined unit within the business model in which you define the boundaries of your software artifacts.

From a domain model perspective, microservices are all about boundaries: we’re splitting a specific piece of our domain model that can be turned into an independently releasable artifact.
With a badly defined boundary, we will create an artifact that depends too much on information confined in another microservice.
We will also create another operational pain: whenever we make modifications in one artifact, we will need to synchronize these changes with another artifact.

We advocate for the monolith-first approach because it allows you to mature your knowledge around your business domain model first.
DDD is such a useful technique for identifying the bounded contexts of your domain model: things that are grouped together and achieve high cohesion and low coupling.
From the beginning, it’s very difficult to guess which parts of the system change together and which ones change separately.
However, after months, or more likely years, developers and business analysts should have a better picture of the evolution cycle of each one of the bounded contexts.

These are the ideal candidates for microservices extraction, and that will be the starting point for the strangling of our monolith.

NOTE
To learn more about DDD, check out Eric Evan’s book,
Domain-Driven Design: Tackling Complexity in the Heart of So ware, and Vaughn Vernon’s book, Implementing Domain-Driven Design.