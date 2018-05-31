PCクラスタおよび高性能並列システムの利用においては、ミドルウエアからライブラリまで多くのオープンソースのソフトウェアが利用され、我が国においてもポストペタCRESTのプロジェクトで開発されたソフトウェアなどオープンソースの関連ソフトウェアが開発されています。本部会では、
そのようなオープンソースHPCソフトウェアの普及のための活動を行います。。

* [HPCオープンソースソフトウェア普及部会の概要]({{ site.baseurl }}/overview).

# オープンソースHPCソフトウェア

---
## Omni Compiler
概要: 
CおよびFortran 2008 を対象としたソース変換(source-to-source tranformation)のインフラストラクチャです。ソースコードをXcodeMLと呼ぶXML形式の中間表現に変換するフロントエンド、XcodeMLレベルでの変換のためのライブラリ、XcodeMLをソースに変換するデコンンパイラから、構成されています。
これを用いて、以下のコンパイラが開発されています。

* XcalableMP
* OpenMP (3.0)
* OpenACC
* XcalableACC

Web site: [http://omni-compiler.org/](http://omni-compiler.org/)

github: [https://github.com/omni-compiler](https://github.com/omni-compiler)

---
## Process-in-Process (PiP)
概要:
これまでノード内の並列実行モデルとしては、マルチプロセス（MPIで広く使われている）とマルチスレッド（OpenMPで使われている）の２つがあります。メニーコアの普及に伴い、これら従来の並列実行モデルではいくつかの問題点が顕在化しています。マルチプロセスにおけるプロセス間通信のオーバヘッドや、マルチスレッドにおける変数のアクセス競合を回避するためのオーバヘッド、などです。そこで、マルチプロセスとマルチスレッドの両者の利点を取り入れると同時に、これらの問題点を解消するための新しいノード内並列実行モデルが望まれます。このアイデア自体は新しいものではありません。米SNLで開発されたSMARTMAP、仏CEAで開発が進められているMPC、理研で開発されたPVASなどがあります。しかしながら、これらは新規OSやOSの改造が必要であったり、新たな言語処理系の開発が必要であったり、とポータビリティに欠け、京などの多数のユーザが使う大規模なスパコンでの運用を難しくしています。Process-in-Process (PiP)の新規性は、その実装が全てユーザレベルのライブラリであることであり、その結果、ポータビリティに優れています。実際、PiPライブラリは、x86_64だけでなく、Arm64、Sparc64（京コンピュータ）上での動作が確認されています。また、米ANLと共同研究によりPiPの利点を生かしたMPICHの研究開発もPiPと同時並行で進められています。

Web site: (TBA)

github: PiP repository will be able to access from [https://github.com/RIKEN-SysSoft/PiP.git](https://github.com/RIKEN-SysSoft/PiP.git) (not ready yet).

---
## McKernel
概要:

Web site:

github:
----
