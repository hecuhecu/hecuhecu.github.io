# hecuhecu.github.io

kawamura の個人開発アプリポータル。GitHub Pages (Jekyll) で運用。

## 構造

```
.
├─ _config.yml              Jekyll 設定
├─ _layouts/
│  ├─ default.html          共通レイアウト
│  ├─ legal.html            規約系ページ用
│  └─ app.html              アプリLP用
├─ _includes/
│  ├─ header.html
│  └─ footer.html
├─ assets/css/base.css      共通CSS
├─ apps/
│  ├─ index.md              アプリ一覧
│  └─ <slug>/               各アプリのページ群（規約4種＋LP）
├─ index.html               旧トップ（TODOタイマーLP、将来移行）
└─ app-ads.txt
```

## 新規アプリページの追加手順

1. `_foundry/legal-kit/templates/` の4つの .template を `apps/<slug>/` にコピー
2. 各ファイル冒頭の Jekyll front matter（`---`）はそのまま残す
3. プレースホルダ（`{{APP_NAME}}` 等）を実値で置換
4. `git push` で自動デプロイ

詳細手順は `_foundry/legal-kit/README.md` と `_foundry/legal-kit/conventions.md` 参照。

## 既存 index.html について

現在の `index.html` は TODOタイマー の単一アプリLP状態。将来、開発者ポータルの体裁に作り変える予定（Jekyll 化後にレイアウト統一）。
