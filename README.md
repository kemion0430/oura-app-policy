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

**現在このページは配信していない。** GitHub Pages を有効にすれば
`https://kemion0430.github.io/oura-app-policy/callback.html` で使えるが、
2026-09-06 時点で有効化できていない。

- スマホの GitHub アプリにはリポジトリの Settings が無い
- ブラウザの Settings → Pages でブランチを選んで保存しても反映されなかった
- ワークフローからの有効化（`actions/configure-pages` の `enablement`）は
  `Resource not accessible by integration` で失敗する。**`GITHUB_TOKEN` は
  Pages サイトを新規作成できない**（デプロイはできるが作成には管理者権限が要る）

PCから Settings → Pages を操作できるときに有効化すれば、このページはそのまま使える。
それまでの戻り先は `https://httpbin.org/get`。

連絡先: mr.meganen@gmail.com
