# kotoba-jigsaw-hp

「ことば猫」の入口のページです。YouTube のアニメ、Kindle の漫画、note の記事、iOS アプリ「言葉ジグソー」と、ゲーム「ことねこ野球盤」へ案内します。アプリのサポートと、2 つのアプリのプライバシーポリシーも置きます。GitHub Pages で配信します。スマートフォンで見る前提で作り、幅 720px 以上では一覧の列を増やします。

| ページ | URL |
| --- | --- |
| 入口・アプリのサポート（お問い合わせ） | https://masanorifunaki.github.io/kotoba-jigsaw-hp/ |
| プライバシーポリシー | https://masanorifunaki.github.io/kotoba-jigsaw-hp/privacy.html |

アプリの中と App Store Connect から、この URL を参照します。URL を変えると両方が壊れるため、ファイル名は変えません。

## ファイル

| ファイル | 中身 |
| --- | --- |
| `index.html`・`home.css` | 入口の案内とサポート。白地に淡い色の帯を重ね、丸いボタンと角の丸いカードで組む |
| `privacy.html`・`style.css` | 言葉ジグソーとことねこ野球盤のプライバシーポリシー。`style.css` は要素に直接かかる書き方のため、`index.html` では読み込まない |
| `images/chara/` | 9 匹の猫の設定画（kotoba-jigsaw の `KotobaJigsaw/KotobaJigsaw/Assets.xcassets` にある `CatStart*`）を幅 480px に縮めたもの。`cat-main` がしろ、`cat-01`〜`cat-08` が野球盤の `Cat.swift` の順の猫 |
| `images/app/` | 言葉ジグソーの 4 つの遊びの画面写真（kotoba-jigsaw の `docs/store/screenshots/` の写真を縮めたもの） |
| `images/baseball/` | ことねこ野球盤のアイコンと、打つ猫・投げる猫の絵（kotoba-jigsaw の `KotobaBaseball/KotobaBaseball/Assets.xcassets` の写し） |
| `images/` | ショートの表紙（`short-*`）・横長の回のサムネイル（`wide-*`）・漫画の表紙（`manga-*`）・note の見出し画像（`note-*`）を縮めたもの。元の絵を変えたら、ここにも写し直す |

新着の動画と記事は自動では取り直しません。載せ替えるときは、YouTube のフィード（`https://www.youtube.com/feeds/videos.xml?channel_id=UCcCaipKKBtuiueE1to55ylg`）と note の記事一覧から新しい順に選び、`short-*`・`wide-*`・`note-*` と `index.html` の題名・リンクを差し替えます。ショートの縦長の画像は `https://i.ytimg.com/vi/<動画の ID>/oar2.jpg` から取れます。

`sitemap.xml` には、公開する 2 ページの URL を並べます。ページを足したら、ここにも足します。

## 検索への対策

Google の「SEO スターター ガイド」に沿って、各ページに固有の `title` と `description`、`canonical`、画像の `alt` を付けています。`index.html` には、アプリの構造化データ（`MobileApplication`）を JSON-LD で入れています。

- Google Search Console で、URL プレフィックス `https://masanorifunaki.github.io/kotoba-jigsaw-hp/` のプロパティを登録し、`sitemap.xml` を送信します
- 構造化データのリッチリザルトは、評価（`aggregateRating`）かレビューがないと表示されません。評価の値は作らず、実際の評価を載せられるようになってから足します
- `robots.txt` とファビコンの検索結果での表示は、ホスト（`masanorifunaki.github.io`）の単位で決まるため、このリポジトリでは変えられません

App Store へのリンクは、どこから入れられたかを数えるため、キャンペーンリンク（`ct=hp`）にしています。リンクの一覧は kotoba-jigsaw の `docs/store/campaign-links.md` にあります。

## 公開の設定

Settings → Pages で、Source を「Deploy from a branch」、Branch を `main` の `/ (root)` にします。`main` へのマージから数分で反映されます。
