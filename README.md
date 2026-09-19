# feedrule-docs

Chrome 拡張 **FeedRule** の公開文書（プライバシーポリシーと利用規約）だけを置く
リポジトリです。GitHub Pages で配信し、その URL を Chrome ウェブストアに登録します。

拡張のソースコードは別のリポジトリにあります。

## Pages を有効にする

Settings → Pages → Source を `Deploy from a branch`、
Branch を `main` / `/ (root)` にして Save。数分で公開されます。

## 公開後の URL

| ファイル | URL |
| --- | --- |
| `privacy-policy.md` | https://kotenbu135.github.io/feedrule-docs/privacy-policy.html |
| `terms.md` | https://kotenbu135.github.io/feedrule-docs/terms.html |

**ストアに登録するのはプライバシーポリシーの URL です。**

## 直すとき

原本は拡張側のリポジトリの `docs/` にあります。ここのファイルを直接直すと、
次に生成したときに上書きされます。原本を直して
`python3 scripts/build-public-docs.py` を走らせ、出力をここへコピーしてください。
