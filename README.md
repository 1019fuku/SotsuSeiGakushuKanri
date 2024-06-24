# サービス概要
このサービスは、みんなで集まって学習をする場所をオンライン上で提供し、学習進捗状況をリアルタイムで共有できるプラットフォームです。また、学習成果を個人のデータとして蓄積し、過去の実績も振り返ることができます。
勉強のタスク管理をしてリアルタイムでサービスに参加しているメンバーと共有する。
タスク管理上でのチャットのメモを共有する。
ポモドーロ機能によって、みんなで時間の管理もしながら同時に休憩も取れるようにして、その際に交流ができます。

# このサービスへの思い・作りたい理由
学習中に感じる孤独感を解消し、モチベーションを維持するためにこのサービスを作成します。リアルタイムで他の人の学習状況がわかることで、自分も頑張ろうという気持ちになりたいという思いがあります。
カリキュラムの学習をしていて躓くところがあった際に、リアルのもくもく会を開催してもらったことで、勉強を続けるには1人では厳しいと感じたからです。そこで誰かと一緒に勉強をしていると感じられるようなサービスを提供できれば、それを使うことで自分のモチベーションも保ちつつ、自分と同じように躓いてやる気がなくなっている人も救済できると感じました。勉強を誰かとする方法は他にもあるとは思いますが、このサービスを使用して各個人の学習記録も残せるようになると、今までの振り返りもしやすくなると思っています。

# ユーザー層について
このサービスはRUNTEQ生限定です。
GitHub認証を使用し、RUNTEQの組織に含まれている人のみがアクセスできるようにします。
RUNTEQ生を対象にすることで、カリキュラムに関する質問であれば、学習内容を共有しやすく、共に質問やそれに回答する経験を積む事ができます。
また、RUNTEQ卒業生との繋がりも作る事ができ、卒業生の状況も知る事ができる機会を提供します。

# サービスの利用イメージ
ユーザーはこのサービスを利用することで、以下の価値を得ることができます：

リアルタイムでの学習進捗共有：学習中に他のユーザーの進捗状況を確認でき、孤独感を解消できます。
学習成果の蓄積と振り返り：自分の学習成果をデータとして蓄積し、過去の実績を振り返ることができます。同様の学習をしている人がいれば、その人の記録を参考にすることもできます。
モチベーションの維持：他のユーザーの学習状況を見て刺激を受け、自分も学習を続けるモチベーションを保てます。サービスの使用を始める都度に、各人の学習目標を設定してから開始しそれを達成する度に、周りに報告し共有する事ができることでモチベーションを保てるようにします。
Discordでも同様に学習はできるが、学習の記録として振り返る事が難しく、このサービスではログインしている個人に記録を紐付けることで、学習の振り返りがしやすい。

# ユーザーの獲得について
このサービスはRUNTEQ生限定であり、主に以下の方法でユーザーを獲得します：

コミュニティ内のプロモーション：RUNTEQ内での積極的なプロモーションを行い、サービスの認知度を高めます。
timesでの宣伝：timesの投稿で周知してもらいます。

# サービスの差別化ポイント・推しポイント
差別化ポイント
RUNTEQ生限定：このサービスはRUNTEQ生のみが利用できるため、安心して学習状況を共有できます。
リアルタイムの進捗共有：学習進捗をリアルタイムで共有する機能は、他のサービスにはない独自の強みです。
推しポイント
コミュニティの一体感：オフラインのように共に学び、教え合う文化を育むことで、コミュニティ全体の学習意欲を向上させます。
学習データの蓄積：個人の学習データを蓄積し、成長を可視化することで、自己肯定感を高めます。

# 機能候補
MVPリリース時
認証機能：gem devise
リアルタイム進捗共有：WebSocketで学習進捗をリアルタイムで共有できる機能。

本リリース
認証機能：RUNTEQ生のみが登録できる。
学習成果の記録と表示：学習成果をデータとして記録し、表示する機能。
過去の学習実績の振り返り：過去の学習実績を振り返ることができる機能。
コミュニティフォーラム：ユーザー間で情報交換や質問ができるフォーラム機能。
ポモドーロ機能：JavaScriptでのタイマー表示。

# 機能の実装方針予定
一般的なCRUD以外の実装予定の機能
リアルタイム通信：学習進捗のリアルタイム共有には、WebSocketを使用してリアルタイム通信を実現します。
データの蓄積と分析：学習成果をデータベースに蓄積し、ユーザーが自分の成長を可視化できるようにデータ分析機能を提供します。
学習の振り返り機能：サービスを使って学習していた内容を日々蓄積することで、学習記録を付ける事ができます。

# 使用するAPIや技術について
WebSocket：リアルタイム通信
Devise：ユーザー認証
Faker：テストデータの生成
Kaminari：ページネーション

DB：PostgreSQL
デプロイ方法：Render.com
