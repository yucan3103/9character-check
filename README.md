# 今のあなた どのキャラが前に出てる？（9キャラ心理学 今の状態チェック）

6問で「今、強く出ているキャラ」を診断する簡易チェックサイトです。
HTML / CSS / JavaScript のみで動作し、外部サービスは使用していません。

## 構成

```
9chara-check-site/
├── index.html        … サイト本体（CSS・JSはこの中にすべて内蔵）
├── images/           … 画像素材
│   ├── kishi.png      (騎士)
│   ├── kamisama.png   (神様)
│   ├── tankenka.png   (探検家)
│   ├── mahotsukai.png (魔法使い)
│   ├── hakase.png     (博士)
│   ├── tantei.png     (探偵)
│   ├── yosei.png      (妖精)
│   ├── osama.png      (王様)
│   ├── soryo.png      (僧侶)
│   └── session-book.png (診断ブックのイメージ)
├── README.md
└── .gitignore
```

## Cloudflare Pages での公開手順（GitHub連携）

1. このフォルダの中身を GitHub リポジトリにアップロード
   （`index.html` がリポジトリの一番上の階層にくるようにします）
2. Cloudflare の「Workers & Pages」→「Pages」→「Create application」→
   「Connect to Git」で対象リポジトリを選択
3. ビルド設定は以下（ビルド不要の静的サイト）
   - Framework preset: `None`
   - Build command: （空欄）
   - Build output directory: `/`
4. 「Save and Deploy」で公開完了

## 修正のしかた

- 色を変える　　→ `index.html` の `<style>` 冒頭 `:root{ --xxx }`
- 質問を変える　→ `index.html` の `<script>` 内 `QUESTIONS`
- 結果文章　　　→ `index.html` の `<script>` 内 `CHARACTERS`
- キャラ画像　　→ `images/` を差し替え（同名 or `CHARACTERS` の `image:` を編集）
- セッションのリンク → `RESULT_LINK`
