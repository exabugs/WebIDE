 - (85%くらいの完成度ですが)サービス開始します。
 - 興味持って頂けましたら、以下のアドレス宛にメール下さい。  
  順番にアカウントを発行させて頂きます。  
  webide@exabugs.com
 - ご意見/ご要望は[GitHub](https://github.com/exabugs/WebIDE)のIssueにお願いします

# WebIDE

### 対象
 - プログラムの勉強を始めたいけど、環境構築が面倒な人
 - 2020年プログラミング教育必修化に関わる教育関係者
 - IT勉強会の主催者
 - プログラミング塾の経営者
 - 大学/高校の情報系学科の関係者

### 概要
 - ブラウザからログインするだけで、すぐにプログラム開発が可能です。  
(対応言語: Java, Node.js, C/C++, Python, Markdown)
 - メニューはなし。アイコンによる直感的な操作。


### 仕組み
 - ユーザ毎に、エディタ、実行/デバッグ環境を含む専用のDockerコンテナが起動します。
 - ログアウト後も作成したファイル(コード)は保存されており、再ログイン時にコンテナにマウントされます。

### 注意
 - CPU/メモリの上限を制限しています
 - 経費節減のため 午前中 (00:00-12:00) はサービスを完全停止します。
 
### 料金
  - とりあえず正式リリースまでは無料
  - その先の予定は未定
     - 商用利用は有料とし、CPU/メモリ上限を高くする

### お願い
 - 画面/アイコン/Webページのデザイナー募集
 - ユーザ数が順調に増えそうならクラウドファンディング
 - 直接投資 / 寄付して頂けると助かります。
 - 別件で AWS でのシステム開発のご相談も承ります。

## 機能

 - [詳細マニュアル](https://github.com/exabugs/WebIDE) (GitHub)

### 全体
- 5つのエリアに分割されていて、タブは各エリア間で移動(D&D)できます。

![全体](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/screen.png)

### エディタ
- 各言語対応のエディタ
  - 色
  - フォールディング(折り畳み)
  - 自動フォーマット
  - 文法チェック

![エディタ](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/edit2.png)

### デバッガ
- ブレークポイント
- ステップ実行

![デバッガ](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/debugger.png)

### 変数
- デバッガ連動の変数ビュワー
- 構造化されているので、詳細を見たい場合はドリルダウン

![変数](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/variable.png)

### スタックトレース
- デバッガ連動のスタックトレース

![スタックトレース](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/stack.png)

### シェル
- zsh が使えます。
- 以下のようなコマンドが使用できます
  - wget / vi などの 一般的なOSコマンド
  - git
  - npm / pip3 などの言語特有コマンド

![シェル](https://raw.githubusercontent.com/exabugs/WebIDE/master/img/zsh.png)

### 言語別対応表

|言語|バージョン|ブレーク<br>ポイント|ステップ<br>実行|変数|スタック<br>トレース|自動<br>フォーマット|文法<br>チェック|
|:-:|:-:|:-:|:-:|:-:|:-:|:--:|:--:|
|Java|1.7.0|◯|◯|◯|◯|astyle|javac|
|Node.js|8.6.0|◯|◯|-|◯|astyle|eslint|
|C/C++|gcc<br>4.9.2|◯|◯|◯|◯|astyle|cpplint|
|Python|3.4.2|◯|◯|◯|◯|yapf|flake8|

#### Python
 - numpy
 - scipy
 - matplotlib
 - pandas
 - scikit-learn
 - yapf
 - hacking
 - tensorflow-1.4.0
