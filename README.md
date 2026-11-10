# kotoba-jigsaw-hp

「ことば猫」の入口のページです。YouTube のアニメ、Kindle の漫画、note の記事と、iPhone の 2 本のゲーム「言葉ジグソー」「ことねこ野球盤」へ案内します。アプリのサポートと、2 つのアプリのプライバシーポリシーも置きます。GitHub Pages で配信します。スマートフォンで見る前提で作り、幅 720px 以上では一覧の列を増やします。

| ページ | URL |
| --- | --- |
| 入口・アプリのサポート（お問い合わせ） | https://masanorifunaki.github.io/kotoba-jigsaw-hp/ |
| プライバシーポリシー | https://masanorifunaki.github.io/kotoba-jigsaw-hp/privacy.html |

アプリの中と App Store Connect から、この URL を参照します。URL を変えると両方が壊れるため、ファイル名は変えません。

## ファイル

| ファイル | 中身 |
| --- | --- |
| `index.html`・`home.css` | 入口の案内とサポート。白地に淡い色の帯を重ね、丸いボタンと角の丸いカードで組む。2 本のアプリは「ゲーム」の節（`#game`）に並べ、言葉ジグソーを空色の帯（`#jigsaw`）、ことねこ野球盤を緑の帯（`#baseball`）で分ける。ショートと野球盤の画面写真は、スマートフォンでは横に送る列にする |
| `privacy.html`・`style.css` | 言葉ジグソーとことねこ野球盤のプライバシーポリシー。`style.css` は要素に直接かかる書き方のため、`index.html` では読み込まない |
| `images/cats3d/` | 動画と同じフェルトの 3D の猫 9 匹。kotoba-jigsaw で猫ごとに `mise run contents cat3d-lookdev --variants <案>.json`（案は `{ "cat": "cat-01", "variants": [{ "id": "hp-cat-01", "label": "cat-01" }] }`）を流し、`~/dev/videos/lookdev/variants/hp-cat-*.jpg` を幅 480px（864×1080 を 480×600）の JPEG に縮めたもの |
| `images/app/` | 言葉ジグソーのアイコン（kotoba-jigsaw の `docs/design/AppIcon.svg` を `rsvg-convert -w 180` で書き出したもの）と、4 つの遊びの画面写真（`docs/store/screenshots/` の写真を縮めたもの） |
| `images/baseball/` | ことねこ野球盤のアイコン（`KotobaBaseball/KotobaBaseball/Assets.xcassets` の写し）と、App Store のヘッダの絵・画面写真（`docs/store/baseball/creative/header.png` と `screenshots/` を JPEG に縮めたもの） |
| `images/og-card.png`・`og/card.html` | SNS で共有したときに出る 1200×630 の絵（`og:image`・`summary_large_image`）。元は `og/card.html` で、`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --hide-scrollbars --force-device-scale-factor=1 --window-size=1200,630 --virtual-time-budget=6000 --screenshot=images/og-card.png "file://$PWD/og/card.html"` で撮り直す |
| `images/og-image.png` | 構造化データの運営元のロゴ。3D の白猫を 600×600 の正方形に切り出したもの |
| `images/` | ショートの表紙（`short-*`）・横長の回のサムネイル（`wide-*`）・漫画の表紙（`manga-*`）・note の見出し画像（`note-*`）を縮めたもの。元の絵を変えたら、ここにも写し直す |

動画と記事は自動では取り直しません。ページには投稿日を出さず、紹介として並べます。載せ替えるときは、YouTube のフィード（`https://www.youtube.com/feeds/videos.xml?channel_id=UCcCaipKKBtuiueE1to55ylg`）と note の記事一覧から新しい順に選び、`short-*`・`wide-*`・`note-*` と `index.html` の題名・リンクを差し替えます。ショートの縦長の画像は `https://i.ytimg.com/vi/<動画の ID>/oar2.jpg` から取れます。

`sitemap.xml` には、公開する 2 ページの URL を並べます。ページを足したら、ここにも足します。

## 検索への対策

Google の「SEO スターター ガイド」に沿って、各ページに固有の `title` と `description`、`canonical`、画像の `alt` を付けています。`index.html` には、サイトと運営元の構造化データ（`WebSite`・`Organization`。`sameAs` に YouTube・TikTok・note を並べる）と、アプリの構造化データ（`MobileApplication`）を JSON-LD で入れています。`sitemap.xml` の `lastmod` は、ページの中身を変えた日に書き換えます。

- Google Search Console で、URL プレフィックス `https://masanorifunaki.github.io/kotoba-jigsaw-hp/` のプロパティを登録し、`sitemap.xml` を送信します
- 構造化データのリッチリザルトは、評価（`aggregateRating`）かレビューがないと表示されません。評価の値は作らず、実際の評価を載せられるようになってから足します
- `robots.txt` とファビコンの検索結果での表示は、ホスト（`masanorifunaki.github.io`）の単位で決まるため、このリポジトリでは変えられません

App Store へのリンクは、どこから入れられたかを数えるため、キャンペーンリンク（`ct=hp`）にしています。リンクの一覧は kotoba-jigsaw の `docs/store/campaign-links.md` にあります。

## 公開の設定

Settings → Pages で、Source を「Deploy from a branch」、Branch を `main` の `/ (root)` にします。`main` へのマージから数分で反映されます。
