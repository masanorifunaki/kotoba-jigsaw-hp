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

App Store へのリンクは、どこから入れられたかを数えるため、キャンペーンリンク（`ct=hp`）にしています。リンクの一覧は kotoba-jigsaw の `docs/store/campaign-links.md` にあります。

## 公開の設定

Settings → Pages で、Source を「Deploy from a branch」、Branch を `main` の `/ (root)` にします。`main` へのマージから数分で反映されます。
