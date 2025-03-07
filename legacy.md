過去の活動

# News
- [第1回XcalableACCチュートリアル]({{ site.baseurl }}/lectures/20190222XACC)
- 第1回目の部会を、以下の要領で開催します。
  - 日時：2018年11月22日（木曜日）13:30-17:00
  - 場所：東京大学　情報基盤センター　4F遠隔スタヂオ（405号室）
  - 議題：
    - 部会概要説明
    - 部会の活動方針
    - その他

# HPCオープンソースソフトウェア

---
## Omni Compiler
概要: 
CおよびFortran 2008を対象としたソース変換(source-to-source tranformation)のインフラストラクチャです。
内部でXcodeML-Toolsを利用しています。下記の言語に対応しています。

* XcalableMP
* OpenMP (3.0)
* OpenACC
* XcalableACC

Web site: [http://omni-compiler.org/](http://omni-compiler.org/)

github: [https://github.com/omni-compiler](https://github.com/omni-compiler)

---
## XcodeML-Tools
概要：ソースコードをXcodeMLと呼ぶXML形式の中間表現に変換するフロントエンドと、XcodeMLをソースに変換するデコンンパイラで構成されています。

Web site: [http://omni-compiler.org/xcodeml.html](http://omni-compiler.org/xcodeml.html)

github: [https://github.com/omni-compiler/xcodeml-tools](https://github.com/omni-compiler/xcodeml-tools)

---
## Process-in-Process (PiP)
概要:
これまでノード内の並列実行モデルとしては、マルチプロセス（MPIで広く使われている）とマルチスレッド（OpenMPで使われている）の２つがあります。メニーコアの普及に伴い、これら従来の並列実行モデルではいくつかの問題点が顕在化しています。マルチプロセスにおけるプロセス間通信のオーバヘッドや、マルチスレッドにおける変数のアクセス競合を回避するためのオーバヘッド、などです。そこで、マルチプロセスとマルチスレッドの両者の利点を取り入れると同時に、これらの問題点を解消するための新しいノード内並列実行モデルが望まれます。このアイデア自体は新しいものではありません。米SNLで開発されたSMARTMAP、仏CEAで開発が進められているMPC、理研で開発されたPVASなどがあります。しかしながら、これらは新規OSやOSの改造が必要であったり、新たな言語処理系の開発が必要であったり、とポータビリティに欠け、京などの多数のユーザが使う大規模なスパコンでの運用を難しくしています。Process-in-Process (PiP)の新規性は、その実装が全てユーザレベルのライブラリであることであり、その結果、ポータビリティに優れています。実際、PiPライブラリは、x86_64だけでなく、Arm64、Sparc64（京コンピュータ）上での動作が確認されています。また、米ANLと共同研究によりPiPの利点を生かしたMPICHの研究開発もPiPと同時並行で進められています。

Web site: (TBA)

github: PiP repository can be found at [https://github.com/RIKEN-SysSoft/PiP.git](https://github.com/RIKEN-SysSoft/PiP.git).

---
## McKernel
概要:

Web site:

github:

----
## ACP: Advanced Communication Primitives (ACP) Library
概要: 
エクサスケール計算環境での利用に耐えるスケーラブルな通信ライブラリです。
以下の特徴を持ちます：
- 基本通信モデルとしてRDMAモデルを提供
- 初期状態でのメモリ消費を最小限に抑制する。
- アプリケーションで頻繁に用いられる通信パターンや大域データ構造の操作をインタフェースとして定義
- 煩雑な RDMAインタフェースによるプログラミングモデルを隠蔽する。
- 各インタフェースは、使用する通信用メモリ領域を明示的に確保/解放する関数を提供
- メモリ領域の再利用によるメモリ効率の高い通信の実現を支援する。
- 通信パターンや大域データ構造毎に独立したインタフェースを用意。
- 各インタフェースについて最小限のメモリ使用量とオーバヘッドでの実装を可能とする。

Web site: [http://ace-project.kyushu-u.ac.jp/main/jp/index.html](http://ace-project.kyushu-u.ac.jp/main/jp/index.html)

github: [https://github.com/project-ace/ACP](https://github.com/project-ace/ACP)

---

