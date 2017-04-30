## フィードバックループ

フィードバックループは人材育成における最も重要なプロセスの1つです。
適切なプロセスを歩んでいることを確かめるために、絶えず自身の行動を評価する必要があります。
よく知られているPlan-Do-Check-Act（PDCA）プロセスでさえフィードバックループの変形です。

私たちが日々の生活で行うすべてのことと同様に、ソフトウェアにおいて、フィードバックループ間隔が長くなればなるほど、成果物は悪化していきます。
これは量と期間の双方において、脳に情報を保持できる容量が限られているために起こります。

私たちがコーディングツールとして使っていたのは、黒い背景と緑色のフォントを備えたテキストエディタでした。
構文が正しいかどうかを確認するためにコードをコンパイルする必要がありました。
時々、コンパイルに数分かかっていました。そして、コンパイルが終わった時にはすでにそれまでの作業の目的を忘れてしまっていました。
この場合のリードタイム(作業の開始から終了までの時間)は長すぎたのです。
私たちが使っているIDEに即時構文ハイライトと即時コンパイル機能が追加された時にようやく上記の問題を改善することができました。

We can say the same thing for testing.
We used to have a dedicated team for manual testing, and the lead time between committing something and knowing if we broke anything was days or weeks.
Today, we have automated testing tools for unit testing, integration testing, acceptance testing, and so on.
We improved because now we can simply run a build on our own machines and check if we broke code somewhere else in the application.

These are some of the numerous examples of how reducing the lead time generated better results in the software development process.
In fact, we might consider that all the major improvements we had with respect to process and tools over the past 40 years were targeting the improvement of the feedback loop in one way or another.

The current improvement areas that we’re discussing for the feed‐ back loop are DevOps and microservices.
