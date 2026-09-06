# oura-app-policy

Oura API を使う個人用アプリ **run log oura** のポリシー文書です。

- [プライバシーポリシー / Privacy Policy](PRIVACY.md)
- [利用規約 / Terms of Service](TERMS.md)

このアプリは開発者本人が自分の睡眠・トレーニングを分析するためのもので、
一般には提供していません。実装は非公開リポジトリにあります。

## `callback.html`

OAuth2 の戻り先ページ。URLに付いてきた `?code=` を画面に表示するだけの静的ページで、
値をどこにも送信しない。

**戻り先を `github.com/...` にすると、スマホでは GitHub アプリが横取りして開く。**
アプリにはアドレス欄が無いので `?code=` を読む手段がなくなる。`github.io` は
アプリの対象外なので必ずブラウザで開き、このページがコードを表示できる。

配信は GitHub Pages（Settings → Pages → main / root）。URLは
`https://kemion0430.github.io/oura-app-policy/callback.html`。

連絡先: mr.meganen@gmail.com
