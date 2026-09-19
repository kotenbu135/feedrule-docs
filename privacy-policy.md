---
layout: default
title: プライバシーポリシー / Privacy Policy
---

# プライバシーポリシー / Privacy Policy

FeedRule（Chrome 拡張）について。最終更新: 2026-09-19

---

## 日本語

### 1. FeedRule が何をするものか

FeedRule は、X と YouTube で表示された投稿を、利用者が自分で書いた条件に沿って
判定し、非表示・ぼかし・強調を行うブラウザ拡張です。

判定は、外部の判定 API である **TypeSafe Jev**（`https://api.typesafe.ai`）が行います。
FeedRule 自身はサーバーを持っておらず、**開発者が運営するサーバーは存在しません。**

### 2. 外部に送信されるもの

判定のたびに、次の 2 つが TypeSafe へ送信されます。

| 送るもの | 具体的に何か |
| --- | --- |
| 判定対象の文 | 画面に表示されている投稿の本文 |
| 利用者が書いたルールの問い | 「この投稿は他人を煽る目的で書かれているか？」など |

「判定対象の文」はサイトごとに次のとおりです。

- **X** — 投稿の本文。リンクや `@` から始まる名前も、表示されているまま含まれます。
  設定で「タイムライン以外も判定する」を有効にしている場合は、
  トレンドの見出しとおすすめユーザーの欄に表示されている文も対象になります。
- **YouTube** — 動画のタイトル、およびコメントの本文。
  タイトルを要素の文字として取り出せなかった場合に限り、代わりに動画リンクの
  `title` または `aria-label` 属性を送ります。この属性には、YouTube の作りによって
  チャンネル名や再生回数が含まれることがあります。

本文は 1,200 文字までに切り詰めてから送信されます。

**表示された投稿がすべて送られるわけではありません。** 送る前に、本文が無いもの、
リンクや記号だけのもの、2 文字に満たないものは端末内で除いています。

### 3. 外部に送信されないもの

次のものは送信しません。

- 閲覧しているページの URL
- 利用者のアカウント名、ログイン情報、Cookie
- 端末や利用者を識別する ID の類
- 画像、音声、動画（Jev はテキストのみを受け取ります）
- TypeSafe の API キー以外の、他のサービスへの一切の送信

また、**同じ文をもう一度判定するときは、送信しません**（次項のキャッシュ）。

### 4. 端末に保存されるもの

すべて `chrome.storage.local`（利用者のブラウザの中）にのみ保存されます。
**外部に同期されず、開発者はこれらを一切受け取りません。**

| 保存するもの | 中身 |
| --- | --- |
| ルール | 利用者が書いた問い、しきい値、動作 |
| 設定 | 表示言語、1 日の上限、有効・無効など |
| **TypeSafe の API キー** | 利用者が設定画面で入力したもの |
| 判定キャッシュ | **本文そのものではなく、本文から作ったハッシュ値**と、Jev が返した 0〜1 の数値。最大 20,000 件・30 日で消えます |
| 実績の記録 | 日付ごとの「判定した件数」「隠した件数」。直近 30 日ぶん。投稿の内容は含みません |

**投稿の本文が端末に保存されることはありません。** キャッシュに入るのは、
元の文に戻すことのできないハッシュ値だけです。

### 5. API キーの扱い

API キーは利用者自身が TypeSafe から取得し、設定画面で入力するものです。
`chrome.storage.local` にのみ保存され、TypeSafe への認証以外には使われません。
**拡張のソースコードにも配布物にも、開発者のキーは含まれていません。**

判定 API の利用料金は、利用者ご自身が TypeSafe に対して負担します。

### 6. 第三者への提供

FeedRule が通信する相手は **TypeSafe（`https://api.typesafe.ai`）だけ**です。
解析ツール、広告、クラッシュレポートの類は一切組み込んでいません。

送信された文を TypeSafe がどう扱うかは、TypeSafe の規約とポリシーによります。
利用の前にご確認ください: <https://docs.typesafe.ai/>

### 7. 権限を求める理由

| 権限 | 理由 |
| --- | --- |
| `https://x.com/*`, `https://twitter.com/*` | X のページで投稿を読み、表示を変えるため |
| `https://www.youtube.com/*`, `https://m.youtube.com/*` | YouTube のページで動画のタイトルとコメントを読み、表示を変えるため |
| `https://api.typesafe.ai/*` | 判定 API を呼ぶため |
| `storage` | ルール・設定・キーを端末に保存するため |

対象サイト以外のページで FeedRule が動くことはありません。

### 8. データの削除

拡張をアンインストールすると、`chrome.storage.local` に保存されたものは
ブラウザによってすべて削除されます。API キーもここに含まれます。

個別に消す場合は、設定画面からルールを削除し、API キーの欄を空にして保存してください。

### 9. 子どもの利用について

FeedRule は特に子どもに向けたものではなく、子どもから個人情報を収集することもありません。

### 10. このポリシーの変更

変更した場合は、このページの日付を更新します。
送信する内容が増える変更を行う場合は、拡張の更新時に画面でお知らせします。

### 11. 連絡先

kotenbu135@gmail.com

---

## English

### 1. What FeedRule does

FeedRule is a browser extension that judges the posts shown to you on X and
YouTube against rules you write yourself, and then hides, blurs or highlights them.

The judging is done by an external API, **TypeSafe Jev**
(`https://api.typesafe.ai`). FeedRule has no backend of its own: **there is no
server operated by the developer.**

### 2. What is sent off your device

Two things are sent to TypeSafe each time a post is judged.

| Sent | What it is |
| --- | --- |
| The text to judge | The text of a post as displayed on the page |
| Your own rule questions | e.g. "Was this post written to provoke someone?" |

"The text to judge" means, per site:

- **X** — the post's text, including links and `@` names exactly as displayed.
  If you turn on "judge more than the feed", the text shown in trends and
  suggested-account panels is included too.
- **YouTube** — video titles and comment bodies. Only when the title cannot be
  read as element text, the video link's `title` or `aria-label` attribute is
  sent instead; depending on how YouTube builds the page, that attribute can
  include the channel name and view count.

Text is truncated to 1,200 characters before being sent.

**Not every post you see is sent.** Before anything leaves your device, posts
with no text, posts that are only links or symbols, and posts shorter than two
characters are dropped locally.

### 3. What is never sent

- The URL of the page you are on
- Your account name, login credentials or cookies
- Any device or user identifier
- Images, audio or video (Jev accepts text only)
- Anything at all to any service other than TypeSafe

Judging the same text a second time sends nothing (see the cache below).

### 4. What is stored on your device

Everything is stored only in `chrome.storage.local`, inside your own browser.
**None of it is synced anywhere, and the developer never receives any of it.**

| Stored | Contents |
| --- | --- |
| Rules | The questions you wrote, thresholds, actions |
| Settings | Language, daily limit, on/off, and so on |
| **Your TypeSafe API key** | As typed into the settings page |
| Judgement cache | **Not the text itself — a hash of it**, plus the 0–1 number Jev returned. At most 20,000 entries, expiring after 30 days |
| Statistics | Per-day counts of posts judged and posts hidden, for the last 30 days. No post content |

**Post text is never written to storage.** The cache holds only hashes, which
cannot be turned back into the original text.

### 5. Your API key

You obtain the key from TypeSafe yourself and enter it on the settings page. It
is stored only in `chrome.storage.local` and is used for nothing but
authenticating to TypeSafe. **No developer key is present in the source code or
in the published build.**

You pay TypeSafe directly for your own API usage.

### 6. Third parties

The only party FeedRule talks to is **TypeSafe (`https://api.typesafe.ai`)**.
There is no analytics, advertising or crash reporting of any kind.

How TypeSafe handles the text it receives is governed by their own terms and
policy. Please read them before use: <https://docs.typesafe.ai/>

### 7. Why each permission is requested

| Permission | Reason |
| --- | --- |
| `https://x.com/*`, `https://twitter.com/*` | To read posts on X and change how they are displayed |
| `https://www.youtube.com/*`, `https://m.youtube.com/*` | To read video titles and comments on YouTube and change how they are displayed |
| `https://api.typesafe.ai/*` | To call the judging API |
| `storage` | To keep your rules, settings and key on your device |

FeedRule does not run on any other site.

### 8. Deleting your data

Uninstalling the extension makes the browser delete everything in
`chrome.storage.local`, including your API key.

To remove things individually, delete your rules on the settings page and save
an empty API key field.

### 9. Children

FeedRule is not directed at children and does not knowingly collect personal
information from them.

### 10. Changes to this policy

If this policy changes, the date at the top is updated. If a change increases
what is sent off your device, it will be announced in the extension when it updates.

### 11. Contact

kotenbu135@gmail.com
