---
title: GitHub Pagesでカスタムドメインを設定するまでの奮闘記"
date: 2025-06-21
---

こんにちは、イッタケです🌿  
今回は、**GitHub Pagesで独自ドメインwww.minipei.comを設定した時の体験談**をまとめます。  
モバイルブラウザでの作業＆ドタバタの連続だったけど、最終的に**無事設定完了！**  
未来の自分や、同じことで困っている誰かのために、記録を残しておきます✍️

---

## 🔧 スタート地点

- 使っているドメイン：`www.minipei.com`（ムームードメインで取得）
- サイト本体：GitHub Pages（ittake-tech.github.io）
- スマホから設定してた（iPhone + Chrome）

---

## 🌀 最初にハマったポイント

1. **「ittake-tech.github.io.」の末尾のドット（.）**
   - GitHub Pagesの公式ドキュメントに出てくるけど、ムームーDNSに入れるとエラーになる
   - → **実はこの「.」はいらなかった！**

2. **DNS設定に必要な情報がわからない**
   - サブドメイン：`www`
   - 種別：`CNAME`
   - 内容：`ittake-tech.github.io` ←ドットなし！
   - 優先度は空白でOKだった

---

## ✅ 成功したDNSレコードの設定（ムームードメイン）

| サブドメイン | 種別  | 内容                     |
|--------------|-------|--------------------------|
| www          | CNAME | ittake-tech.github.io    |

→ この設定を入れて「設定を追加」

---

## 🕒 設定反映までの時間

- 30分〜1時間ほど待機（私の場合は40分くらいだった）
- 何度もGitHub Pagesの画面で「Check again」を押して確認した

---

## 🎉 最終確認

- `DNS check successful` の表示が出た！
- `https://www.minipei.com` にアクセスできた！
- GitHub Pages の画面にも `Your site is live at https://www.minipei.com` と表示！

---

## ✨ 感想と学び

- スマホだけでも設定できたけど、情報が少なくて大変だった…
- 「ドットいるの？いらないの？」ってところが最大の罠だった
- でも無事に設定できたときの達成感はすごい！

---

## 👋 これからの運営について

- minipei.com は、私の「整えるブログ」
- ミニマリズム・パーマカルチャー・ジャズ…静かな豊かさをここに綴っていきます

---

以上、GitHub Pagesで独自ドメインを設定した奮闘記でした！  
どこかの誰かの参考になりますように🌱

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-89D1F7DMB6"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-89D1F7DMB6');
</script>
