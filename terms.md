---
layout: default
title: 利用規約と免責事項 / Terms and Disclaimer
---

# 利用規約と免責事項 / Terms and Disclaimer

FeedRule（Chrome 拡張）について。最終更新: 2026-09-19

無償で提供する拡張なので、短くしてあります。長い規約は読まれず、
読まれない規約は守られません。

---

## 日本語

### 1. これは何か

FeedRule は、X と YouTube で表示された投稿を、利用者が自分で書いた条件に沿って
判定し、非表示・ぼかし・強調を行うブラウザ拡張です。**無償で提供されます。**

インストールして使った時点で、この規約に同意したものとします。

### 2. 判定は外部の API が行い、料金は利用者の負担です

FeedRule は、表示された投稿の本文を外部の判定 API（TypeSafe Jev）へ送信し、
その結果に基づいて表示を変更します。何が送られるかは
[プライバシーポリシー](privacy-policy.md)に書いてあります。

**API の利用料金は、利用者ご自身が TypeSafe に対して負担します。**
無償なのは拡張であって、判定ではありません。

拡張には 1 日あたりの判定件数の上限があります（既定 2,000 件）。
これは請求が思わぬ額になることを防ぐためのものですが、
**上限を設けたことをもって、金額を保証するものではありません。**
実際の料金は TypeSafe の価格と利用量で決まります。

### 3. 判定は常に正しいとは限りません

判定は自動で行われるため、**常に正しいとは限りません。**
隠すべきでない投稿が隠れること、隠したい投稿が表示されることがあります。

**本拡張は、特定の情報を確実に遮断することを保証するものではありません。**
見たくないものを必ず遮断する必要がある用途には使わないでください。

判定できなかった投稿（API のエラー、通信の失敗、上限への到達など）は、
隠さずそのまま表示されます。これは仕様です。

### 4. 対象サイトの仕様変更により、予告なく動作しなくなります

FeedRule は X と YouTube の画面の構造を読んで動きます。
**これらのサイトは予告なく構造を変えます。** 変わった時点で、
FeedRule は投稿を読めなくなり、判定が止まります。

止まったことに気づけるよう、拡張は検知して知らせますが、
**復旧を約束するものではありません。**

### 5. 保証と責任

本拡張は**現状有姿**で提供されます。明示・黙示を問わず、いかなる保証もしません。

開発者は、本拡張の利用によって生じたいかなる損害
（**API の利用料金**、隠されなかった投稿を見たこと、隠された投稿を見逃したこと、
これらに起因する一切の結果を含みます）についても責任を負いません。

また、**継続的な提供、不具合の修正、問い合わせへの回答を約束するものではありません。**
個人が無償で公開しているものです。予告なく公開を取りやめることがあります。

### 6. やってはいけないこと

- 本拡張を、対象サイトの利用規約に反する形で使うこと
- 本拡張を改変して、API キーの取得や他者への配布を目的に使うこと
- 判定 API に対して、自動化された大量のリクエストを送る目的で使うこと

### 7. 他社との関係

本拡張は、**X および YouTube とは関係のない独立したソフトウェア**です。
これらの会社から承認・後援・提携を受けたものではありません。

TypeSafe についても同様で、判定 API の一利用者にすぎません。

### 8. 対価を受け取らないこと

本拡張は無償で提供され、課金・投げ銭・寄付・広告・アフィリエイトの
いずれも行いません。将来これを変える場合は、事前に公開ページで告知します。

### 9. この規約の変更

変更した場合は、このページの日付を更新します。

### 10. 連絡先

kotenbu135@gmail.com

---

## English

### 1. What this is

FeedRule is a browser extension that judges the posts shown to you on X and
YouTube against rules you write yourself, and then hides, blurs or highlights
them. **It is provided free of charge.**

By installing and using it, you agree to these terms.

### 2. An external API does the judging, and you pay for it

FeedRule sends the text of the posts you see to an external judging API
(TypeSafe Jev) and changes what you see based on the answer. What is sent is
described in the [privacy policy](privacy-policy.md).

**You pay TypeSafe for your own API usage.** The extension is free; the
judging is not.

The extension has a daily cap on how many posts it will judge (2,000 by
default). It exists to keep your bill from surprising you, but **its existence
is not a guarantee of any amount.** What you actually pay is set by TypeSafe's
pricing and your usage.

### 3. The judgement will not always be right

The judgement is automatic and **will not always be right.** Posts that should
stay may be hidden, and posts you wanted hidden may appear.

**This extension does not guarantee that any particular content will be
blocked.** Do not rely on it where content must be blocked.

Posts that could not be judged — API errors, network failures, the daily cap —
are shown unchanged. That is intended behaviour.

### 4. It will stop working without notice when the sites change

FeedRule reads the page structure of X and YouTube. **Those sites change their
structure without notice.** When they do, FeedRule can no longer read posts and
judging stops.

The extension detects this and tells you, but **no fix is promised.**

### 5. Warranty and liability

This extension is provided **as is**, without warranty of any kind, express or
implied.

The developer is not liable for any damages arising from its use, including
**API charges**, seeing a post that was not hidden, missing a post that was
hidden, and anything following from either.

The developer makes **no promise of continued availability, fixes, or support.**
This is software published free of charge by one person, and it may be withdrawn
without notice.

### 6. What you may not do

- Use it in a way that breaks the terms of the sites it runs on
- Modify it in order to harvest API keys or redistribute them
- Use it to send automated bulk traffic to the judging API

### 7. No affiliation

This extension is **independent and is not affiliated with X or YouTube**, and
is not endorsed or sponsored by them. The same applies to TypeSafe, whose API it
merely calls as one customer among others.

### 8. No payments

This extension is free and carries no purchases, tips, donations, advertising or
affiliate links. If that ever changes, it will be announced in advance on the
listing page.

### 9. Changes to these terms

If these terms change, the date at the top is updated.

### 10. Contact

kotenbu135@gmail.com
