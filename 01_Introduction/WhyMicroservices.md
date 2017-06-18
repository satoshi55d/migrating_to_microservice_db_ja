## なぜマイクロサービスなのか

マイクロサービスに関する議論はスケーラビリティに関するものだと考える人がいますが、おそらく間違っています。
確かにNetflixやAmazonなどの企業によって実装されたマイクロサービスアーキテクチャに関する素晴らしい文献を常に目にしています。
それでは、このような質問をしてみましょう。世界中で一体どのくらいの企業がNetflixやAmazonのようになることができるでしょうか。
続いて、もう1つ質問です。世界中で一体どのくらいの企業がNetflixやAmazonと同じスケーラビリティ要件に対処する必要があるでしょうか。

答えは、世界中の大多数の開発者がエンタープライズアプリケーションソフトウェアを扱っているということです。
NetflixやAmazonのドメインモデルを過小評価したくはありませんが、エンタープライズドメインモデルは完全に対処すべき野獣であると言えます。

ですから、大多数の開発者にとってマイクロサービスは通常スケーラビリティに関するものではありません。
結局のところ、リードタイムを改善し、リリースのバッチサイズを縮小することがすべてなのです。

But we have DevOps that shares the same goals, so why are we even discussing microservices to achieve this?
Maybe your development team is so big and your codebase is so huge that it’s just too difficult to change anything without messing up a dozen different points in your application.
It’s difficult to coordinate work between people in a huge, tightly coupled, and entangled codebase.

With microservices, we’re trying to split a piece of this huge monolithic codebase into a smaller, well-defined, cohesive, and loosely coupled artifact.
And we’ll call this piece a microservice.
If we can identify some pieces of our codebase that naturally change together and apart from the rest, we can separate them into another artifact that can be released independently from the other artifacts.
We’ll improve our lead time and batch size because we won’t need to wait for the other pieces to be “ready”;
thus, we can deploy our microservice into production.

#### You Need to Be This Tall to Use Microservices

Microservices architectures encompasses multiple artifacts, each of which must be deployed into production.
If you still have issues deploying one single monolith into production, what makes you think that you’ll have fewer problems with multiple artifacts?
A very mature software deployment pipeline is an absolute requirement for any microservices architecture.
Some indicators that you can use to assess pipeline maturity are the amount of manual intervention required, the amount of automated tests, the automatic provisioning of environments, and monitoring.

Distributed systems are difficult.So are people.
When we’re dealing with microservices, we must be aware that we’ll need to face an entire new set of problems that distributed systems bring to the table.
Tracing, monitoring, log aggregation, and resilience are some of problems that you don’t need to deal with when you work on a monolith.

Microservices architectures come with a high toll, which is worth paying if the problems with your monolithic approaches cost you more.
Monoliths and microservices are different architectures, and architectures are all about trade-off.