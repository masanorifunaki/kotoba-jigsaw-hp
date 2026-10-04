# kotoba-jigsaw-hp

iOS アプリ「言葉ジグソー」の公開ページです。GitHub Pages で配信します。

| ページ | URL |
| --- | --- |
| アプリの紹介・サポート（お問い合わせ） | https://masanorifunaki.github.io/kotoba-jigsaw-hp/ |
| プライバシーポリシー | https://masanorifunaki.github.io/kotoba-jigsaw-hp/privacy.html |

アプリの中と App Store Connect から、この URL を参照します。URL を変えると両方が壊れるため、ファイル名は変えません。

## ファイル

| ファイル | 中身 |
| --- | --- |
| `index.html`・`home.css` | アプリの紹介とサポート。色と書体はアプリの `docs/DESIGN.md` に合わせる |
| `privacy.html`・`style.css` | プライバシーポリシー。`style.css` は要素に直接かかる書き方のため、`index.html` では読み込まない |
| `images/` | 猫とアイコンの絵。kotoba-jigsaw の `docs/design/`（`start-cats/`・`hanamaru-cats/CatStart-Hug.svg`・`AppIcon.svg`）の写し。元の絵を変えたら、ここにも写し直す |

`sitemap.xml` には、公開する 2 ページの URL を並べます。ページを足したら、ここにも足します。

## 検索への対策

Google の「SEO スターター ガイド」に沿って、各ページに固有の `title` と `description`、`canonical`、画像の `alt` を付けています。`index.html` には、アプリの構造化データ（`MobileApplication`）を JSON-LD で入れています。

- Google Search Console で、URL プレフィックス `https://masanorifunaki.github.io/kotoba-jigsaw-hp/` のプロパティを登録し、`sitemap.xml` を送信します
- 構造化データのリッチリザルトは、評価（`aggregateRating`）かレビューがないと表示されません。評価の値は作らず、実際の評価を載せられるようになってから足します
- `robots.txt` とファビコンの検索結果での表示は、ホスト（`masanorifunaki.github.io`）の単位で決まるため、このリポジトリでは変えられません

App Store へのリンクは、どこから入れられたかを数えるため、キャンペーンリンク（`ct=hp`）にしています。リンクの一覧は kotoba-jigsaw の `docs/store/campaign-links.md` にあります。

## 公開の設定

Settings → Pages で、Source を「Deploy from a branch」、Branch を `main` の `/ (root)` にします。`main` へのマージから数分で反映されます。
