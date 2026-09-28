# DesktopStream

日本語 | [English](README.en.md)

Windows PC の画面を、スマホや別の PC から見たり操作したりするソフトです。

- UAC の確認画面やロック画面も表示・操作できます。管理者の確認が出ても、外出先から先へ進められます
- 同じ Wi-Fi の中からも、外出先からも使えます(外出先からは P2P で直接つなぎます)
- 受け取った映像を、コメント付きでほかの人に見せることもできます

動作条件: Windows 10 / 11(64bit)

---

## 使ってみる

### 1. ダウンロード

**[最新版をダウンロード](https://github.com/brad-55/DesktopStream/releases/latest)**

| ファイル | どちらを選ぶか |
|---|---|
| `DesktopStream-...-setup.exe` | インストーラ。ふつうはこちらを選んでください |
| `DesktopStream-...-portable.zip` | 展開して置くだけの版。インストーラを使いたくない場合に選んでください |

### 2. はじめる

[クイックガイド](https://brad-55.github.io/DesktopStream/quickstart.html)に、画面が映るまでの手順(5分ほど)をまとめています。
機能の詳しい説明と困ったときの対処は、[詳細ガイド](https://brad-55.github.io/DesktopStream/guide.html)にあります。

### 操作する側の画面

| 用途 | URL |
|---|---|
| 外出先から操作する | https://brad-55.github.io/DesktopStream/client.html |
| 再配信を見る(視聴専用) | https://brad-55.github.io/DesktopStream/secondclient.html |

同じ Wi-Fi にいるときは、パソコン自身が配信する `https://パソコンのIP:8080` を開くこともできます(ルームID は要りません)。

---

## ⚠️ このソフトは署名されていません

コードサイニング証明書を取得していないため、Windows SmartScreen やウイルス対策ソフトが警告を出します。
加えて、このソフトは「SYSTEM 権限のサービス + 画面キャプチャ + 入力注入 + 外部通信」という構成で、遠隔操作型マルウェアと同じ特徴を持つため、警告の対象になりやすくなっています。

ダウンロードしたファイルが改ざんされていないことは、SHA256 で確かめられます。
正しい値は、各リリースのリリースノートに載せています。

```powershell
Get-FileHash .\DesktopStream-v0.8.1-setup.exe -Algorithm SHA256
```

ファイル名は、ダウンロードした版に合わせて変えてください。

## 安全に使うために

- **ルームID は実質的なパスワードです。** 知っている人は誰でもあなたの画面に接続し、操作できます。人に見せないでください
- 接続してくる端末は、初回にパソコン側で承認する必要があります
- 使い終わったら、Stop を押すか、コンソールから切断してください

## ライセンス

GStreamer / GLib(LGPL-2.1-or-later)を同梱しています。ライセンスの全文は、配布物の `licenses/` に収録しています。GPL の x264 / x265 は同梱していません。
