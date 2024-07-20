# 🧷ひっつくん

VRCの機能の「**コンタクト**」とUnityの標準機能の「**コンストレイント**」を用いて、特定のオブジェクトに追従するようにできるアバターギミックです。

「**VRC Contact Receiver**」で検出可能なコライダーであれば、例え他のプレイヤー（アバター）であっても追従可能です。

※上級者向けのギミックになるので、導入の難易度は高いと思います。＋ゴミ説明で難易度が超破滅級にUP!してます...

<div align="center">

![sample](https://github.com/user-attachments/assets/d78faef2-2c30-49b0-8b9f-e7ac1ce7d1d4)

</div>

> [!WARNING]  
> 後からJoinしてきたユーザーには同期されません

→使いやすいようにunitypackage化しました。ダウンロードは [**こちら**](https://github.com/HV-Niiya/Hittukun/releases/latest)からどうぞ！

# 🛠導入方法
- Assets内の「ひっつくん」のフォルダーの中に「**DummyAvatar**」プレハブがあるので、Hierarchyのなかにドラック＆ドロップする。

<!-- 
![スクリーンショット (243)](https://github.com/user-attachments/assets/950dd313-b8e5-4302-8a62-607ea2ac13aa)
-->

![スクリーンショット (246)](https://github.com/user-attachments/assets/74290cb3-210c-4d39-b0e0-53abc52a8acc)

- Hierarchyの「**ひっつくん**」を実装したいアバターにドラック＆ドロップする。同じ感じ親子関係になっていればOK！
- Assets内の「**ひっつくん**」のフォルダーの中の「**FX**」を実装したいアバターのFXと統合する。
> [!TIP]
> 「**Modular Avatar**」などのツールを使用すると、簡単に統合ができます。
- 「**オブジェクト**」の配下の「**Cube**」を自分が使用したいモデルに差し替える。
- 「**元のポジション**」を手や頭など追従させたいところに移動させる。トラッキングしているオブジェクトがLOST状態になるとそのポジションへ戻る。
- 最後に「**DummyAavatar**」が残っているで、消去すること。

※「**TestObject**」は追従される側のオブジェクトのサンプル。

> [!CAUTION]
> Unity上で動作確認する場合は、「**Gesture Manager**」などのツールを再生しないと、正常に動作しない場合があります。

# 📄仕様や説明など
- 「**Tracker**」とその配下（X+1からY+1）のコンポーネントの中に「**VRC Contact Receiver**」があります。その設定の「**Collision Tag**」を追従させたいオブジェクト「**VRC Contact Sender**」の「**Collision Tag**」と一致さてください。

![スクリーンショット (244)](https://github.com/user-attachments/assets/7c999a18-9338-4218-a72e-34357733d4d9)

- オブジェクトを見失う（**LOST状態**）と元のポジションに戻ります。

LOST状態になったらワールド固定になる挙動へ変更することもでき、その場合は、「**ひっつくん**」フォルダー内の「**Tracking**」フォルダーの中に「**Tracking**」と「**LOST**」のアニメーションの中身を無（中身無し）に書き変えることで変更可能です。

難儀でしたら、「**Tracker**」の中の「**Parent Constraint**」を消去or無効にするか、「**FX**」のLayersの中の「**isTraking**」のレイヤーを消去or無効にするか、いっそのこと「**Tracking**」と「**LOST**」のアニメーションのファイルを消去でいけます。

# 📄確認した環境
- Unity version 2022.3.22f1
- VRC SDK 3.6.1
- Gesture Manager 3.9.1

※合わせる必要はないと思います

# 🔗リンク
勉強するときに使ったサイト

- https://qiita.com/u_d_iix/items/806d68e1496ba6fa3acd
- https://note.com/ninado/n/nebdf295a1f98
-----
