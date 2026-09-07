# DesktopStream

Windows PC の画面を、スマホや別の PC から **見る / 操作する** ソフトです。

- **UAC の確認画面やロック画面も表示・操作できます** — 管理者の確認が出ても、外出先から先に進めます
- **同じ Wi-Fi でも、外出先からでも使えます**（外出先からは P2P で直接つなぎます）
- 受け取った映像を、**コメント付きで他の人に見せる**こともできます

動作条件: Windows 10 / 11（64bit）

---

## 使ってみる

### 1. ダウンロード

**[最新版をダウンロード](https://github.com/brad-55/DesktopStream/releases/latest)**

| ファイル | どちらを選ぶか |
|---|---|
| `DesktopStream-...-setup.exe` | ふつうはこちら（インストーラ） |
| `DesktopStream-...-portable.zip` | 展開して置くだけ。インストールしたくない場合 |

### 2. はじめる

**[クイックガイド](https://brad-55.github.io/DesktopStream/quickstart.html)** — 5分で画面が映るまで

もっと詳しく知りたくなったら **[使いかたガイド](https://brad-55.github.io/DesktopStream/guide.html)** をどうぞ。

### 操作する側の画面

| | |
|---|---|
| 外出先から操作する | https://brad-55.github.io/DesktopStream/client.html |
| 再配信を見る（視聴専用） | https://brad-55.github.io/DesktopStream/secondclient.html |

同じ Wi-Fi にいるときは、パソコン自身が配信する `https://パソコンのIP:8080` を開くこともできます（ルームID は要りません）。

---

## ⚠️ このソフトは署名されていません

コードサイニング証明書を取得していないため、**Windows SmartScreen やウイルス対策ソフトが警告を出します。**

「SYSTEM 権限のサービス + 画面キャプチャ + 入力注入 + 外部通信」という構成は、遠隔操作型マルウェアとまったく同じ特徴を持つためです。ソフトの性質上これは避けられません。

ダウンロードしたファイルが改ざんされていないことは、各リリースに記載の SHA256 で確認できます。

```powershell
Get-FileHash .\DesktopStream-setup.exe -Algorithm SHA256
```

## 安全に使うために

- **ルームID は実質的なパスワードです。** 知っている人は誰でもあなたの画面に接続でき、操作もできます。人に見せないでください
- 接続してくる端末は、初回に**パソコン側での承認**が必要です
- 使い終わったら Stop を押すか、コンソールから切断してください

## ライセンス

GStreamer / GLib（LGPL-2.1-or-later）を同梱しています。全文は配布物の `licenses/` に収録しています。GPL の x264 / x265 は同梱していません。
