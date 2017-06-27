## ストラングラーパターン

マーティン・ファウラーは、[モノリス・ファースト・アプローチ](https://martinfowler.com/bliki/MonolithFirst.html)についての素晴らしい記事を書いています。
彼の記事から2つの興味深いポイントを引用してみましょう。

* 成功したマイクロサービスのほとんどすべてが大きく成長したモノリスを解体させることから始まっています。
* 最初からマイクロサービスとして構築されたシステム事例のほとんどすべてが、重大なトラブルを引き起こして終わった。

すべてのエンタープライズアプリケーションソフトウェア開発者にとって、
すべて投げ捨てることなくゼロから始めることはきっとラッキーなことだと思います。（誰かがこのアプローチを考えていたとしても）
そして、重大なトラブルを引き起こす結末を迎えることでしょう。
しかし、本当にラッキーなのは本番環境で保守しているモノリスを既に保有していることなのです。

モノリスファーストの考え方は、絞め殺しの木の発達に似ていることから、絞め殺しパターンとも言われます。
絞め殺しの木は、宿主の木の一番上で小さく芽生えます。
そして、その根は地面に向かって成長し始めます。
根が地面に達するとさらに成長を続け、絞め殺しの木は宿主の木の周りにまで成長し始めます。
やがて絞め殺しの木は宿主の木よりも大きくなり、時には宿主を死滅させることさえあります。
完全にこじつけだと思いますが、私たちは皆、モノリスという獣を殺したいという深い欲望を心の中に隠しています。

Having a stable monolith is a good starting point because one of the hardest things in software is the identification of boundaries between the domain model—things that change together, and things that change apart.
Create wrong boundaries and you’ll be doomed with the consequences of cascading changes and bugs.
And boundary identification is usually something that we mature over time.
We refactor and restructure our system to accommodate the acquired boundary knowledge.
And it’s much easier to do that when you have a single codebase to deal with, for which our modern IDEs will be able to refactor and move things automatically.
Later you’ll be able to use these established boundaries for your microservices.
That’s why we really enjoy the strangler pattern: you start small with microservices and grow around a monolith.
It sounds like the wisest and safest approach for evolving enterprise application software.

The usual candidates for the first microservices in your new architecture are new features of your system or changing features that are peripheral to the application’s core.
In time, your microservices architecture will grow just like a strangler fig tree, but we believe that the reality of most companies will still be one, two, or maybe even up to half-dozen microservices coexisting around a monolith.

The challenge of choosing which piece of software is a good candidate for a microservice requires a bit of Domain-Driven Design knowledge, which we’ll cover in the next section.