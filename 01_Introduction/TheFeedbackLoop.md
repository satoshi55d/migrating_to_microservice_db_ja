## フィードバックループ

フィードバックループは人材育成における最も重要なプロセスの1つです。
適切なプロセスを歩んでいることを確かめるために、絶えず自身の行動を評価する必要があります。
よく知られているPlan-Do-Check-Act（PDCA）プロセスでさえフィードバックループの変形です。

私たちが日々の生活で行うすべてのことと同様に、ソフトウェアにおいて、フィードバックループ間隔が長くなればなるほど、結果は悪化していきます。
これは量と期間の双方において、脳に情報を保持できる容量が限られているために起こります。

私たちがコーディングツールとして使っていたのは、黒い背景と緑色のフォントを備えたテキストエディタでした。
構文が正しいかどうかを確認するためにコードをコンパイルする必要がありました。
時々、コンパイルに数分かかっていました。そして、コンパイルが終わった時にはすでにそれまでの作業の目的を忘れてしまっていました。
この場合のリードタイム(作業の開始から終了までの時間)は長すぎたのです。
私たちが使っているIDEに即時構文ハイライトと即時コンパイル機能が追加された時にようやく上記の問題を改善することができました。

同じことがテストにおいても言えます。
私たちは手作業によるテストのための専任チームを設けていました。
何らかのコードをコミットしてから、不具合が発生していることに気づくまでのリードタイムは数日または数週間でした。
今では、単体テスト、統合テスト、受入れテストなどのための自動テストツールがあります。
それらによって上記の問題は改善されました。
自分のマシン上でビルドを実行し、アプリケーション内の別の箇所のコードに不具合が起きていないかを検証することができるようになったためです。

これらはリードタイムの短縮がソフトウェア開発プロセスにおいてより良い結果を生み出す数多くの例の一部です。
実際、過去40年間のプロセスとツールに関して私たちが行ってきた主要な改善は、何らかの方法でフィードバックループの改善を狙っていたと考えられます。

これよりフィードバックループの改善のために議論する内容は、DevOpsとマイクロサービスです。