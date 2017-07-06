## マイクロサービスの特徴

James LewisとMartin Fowlerは、[ほとんどのマイクロサービスアーキテクチャに当てはまる共通の特性](https://www.martinfowler.com/articles/microservices.html)を提唱しました。

* サービスによるコンポーネント化
* ビジネスケイパビリティに基づいた組織化
* プロジェクトではなくプロダクト
* スマートエンドポイントとダムパイプ
* 分散ガバナンス
* 分散データ管理
* インフラストラクチャの自動化
* 障害設計
* 進化的設計

前述の特性は確かにすべて注目すべきです。
しかし、数年かけてマイクロサービスアーキテクチャの研究、コーディング、および議論をしてきて、最も一般的な問題は次の事項であることを認めざるを得ません。

    モノリシックなレガシーデータベースをどのように進化させるのか。

この質問によって、エンタープライズアプリケーション開発者がモノリスをより効果的に破壊する方法についていくつかの考え方が生まれました。
そのため、この本では分散データ管理について主に議論します。
一言でその考え方を表現するならば、次のように述べることができるでしょう。

    マイクロサービスごとに独立したデータベースを保有するべきである。

この発言には、課題が潜んでいます。
新規開発プロジェクトの場合でも、別のサービスによって提供される情報が必要なシナリオは数多くあります。
経験上、リモートプロシージャコール(RPC)またはREST等のリモート呼出しに依存すると、データ集約型のユースケースではスループットとレイテンシの両方で十分な性能が得られません。

この本で述べる内容はすべてリレーショナルデータベースに対処するための戦略です。
第2章ではデプロイメントに関連するアーキテクチャについて説明します。
第3章で紹介するゼロダウンタイム移行は、マイクロサービスに限った話ではありませんが、分散システムではさらに重要です。
ネットワークを介して相互接続された異なる成果物によって分断された情報を持つ分散システムを扱っているため、情報をどのように収束させるかについても対処する必要があります。
第4章では整合性モデルの違いについて説明します。作成、読み取り、更新、および削除(CRUD)と、CQRS(Command and Query Responsibility Segregation)です。
第5章で扱う最後のトピックでは、マイクロサービスアーキテクチャのノード間でどのように情報を統合できるかについて説明します。

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