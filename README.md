# 🧷ひっつくん

VRCの機能の「**コンタクト**」とUnityの標準機能の「**コンストレイント**」を用いて、特定のオブジェクトに追従するようにできるアバターギミックです。

<div align="center">

![sample](https://github.com/user-attachments/assets/d78faef2-2c30-49b0-8b9f-e7ac1ce7d1d4)

</div>

相手の頭や手、コンタクトが対応している箇所はすべて追従可能です。

もちろん、Tagなどを設定することによって特定のオブジェクトに追従することもできます。

使いやすいようにunitypackage化しました。
ダウンロードは [**こちら**](https://github.com/HV-Niiya/Hittukun/releases/latest)からどうぞ！

> [!WARNING]  
> 後からJoinしてきたユーザーには同期されません

改良の余地あり

# 🛠導入方法
- Assets内の「ひっつくん」のフォルダーの中に「**DummyAvatar**」プレハブがあるので、Hierarchyのなかにドラック＆ドロップする。

![sample](https://github.com/user-attachments/assets/d78faef2-2c30-49b0-8b9f-e7ac1ce7d1d4)

- Hierarchyの「**ひっつくん**」を実装したいアバターにドラック＆ドロップする。同じ親子関係になっていればOK！
- Assets内の「**ひっつくん**」のフォルダーの中の「**FX**」を実装したいアバターのFXと統合する。
> [!TIP]
> 「**Modular Avatar**」などのツールを使用すると、簡単に統合ができます。
- 「**オブジェクト**」の配下の「**Cube**」を自分が使用したいモデルに変更する
- 最後に「**DummyAavatar**」が残っているで、消去すること

> [!CAUTION]
> Unity上で動作確認する場合は、「**Gesture Manager**」などのツールを再生しないと、正常に動作しない場合があります。

# 🔗リンク
勉強するときに使ったサイト

- https://qiita.com/u_d_iix/items/806d68e1496ba6fa3acd
- https://note.com/ninado/n/nebdf295a1f98

-----

※上位互換
- https://github.com/VRLabs/Contact-Tracker
