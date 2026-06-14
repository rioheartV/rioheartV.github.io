# My Site

活動内容・リンク・ブラウザゲームをまとめた個人サイトです。

## ファイル構成

```
C:\HP\
├─ index.html              … トップページ（活動・ゲーム・リンク）
├─ style.css               … デザイン
├─ games\                  … ゲーム置き場（1ゲーム＝1フォルダ）
│   └─ number-rush\
│       └─ index.html      … サンプルゲーム
└─ README.md               … このファイル
```

## 編集のしかた

- **文章・活動内容**: `index.html` の各セクションを書き換える。
- **リンク**: `index.html` の「リンク」内、`href="#"` を自分のURLに変える。
- **色・デザイン**: `style.css` の上部 `:root { ... }` の色を変える。

## ゲームの追加

1. `games\` の中に新しいフォルダを作る（例: `games\my-game\`）。
2. そのフォルダに `index.html` を置く（HTML/JS製ならそのまま動く）。
3. `index.html` のゲーム欄にあるコメント例をコピーして、リンク先とタイトルを差し替える。

Unity の WebGL ビルドや、他のHTML5ゲームもフォルダごと置けばOK。

## ローカルで確認

`index.html` をダブルクリックすればブラウザで開けます。

## 無料で公開する（GitHub Pages）

1. GitHub で新しいリポジトリを作る。
   - サイトを `あなたのID.github.io` で公開したい場合 → リポジトリ名を **`あなたのID.github.io`** にする。
   - それ以外の名前でもOK（URLは `あなたのID.github.io/リポジトリ名/` になる）。
2. このフォルダ（`C:\HP` の中身）をリポジトリに push する。
   ```powershell
   cd C:\HP
   git init
   git add .
   git commit -m "first site"
   git branch -M main
   git remote add origin https://github.com/あなたのID/リポジトリ名.git
   git push -u origin main
   ```
3. GitHub のリポジトリ → **Settings → Pages** で、Branch を `main` / `/(root)` にして Save。
4. 数十秒〜数分で `https://あなたのID.github.io/...` に公開される。

更新は、ファイルを編集して再度 `git add . && git commit -m "update" && git push` するだけ。
