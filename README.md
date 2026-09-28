# 茶道体験 スマホ用ページ — 公開手順（GitHub ＋ Netlify）

このフォルダ（`web/`）が公開するサイト一式です。
- `index.html` … ページ本体（1ファイル）
- `img/` … 画像（v4パワポの画像を軽量化したもの。人物写真は入れていません）

## 1. GitHub にアップロード（初回のみ）
1. https://github.com にログイン → 右上「+」→ **New repository**
2. Repository name: `tea-ceremony-guide`（任意）、**Public** を選択 → **Create repository**
3. 作成後の画面で **uploading an existing file** をクリック
4. `web` フォルダの**中身**（`index.html` と `img` フォルダ）をドラッグ＆ドロップ
   - ※ `web` フォルダごとではなく、中身を入れる（`index.html` がリポジトリ直下に来るように）
5. **Commit changes**

## 2. Netlify で公開（初回のみ）
1. https://app.netlify.com に GitHub アカウントでサインアップ／ログイン
2. **Add new site → Import an existing project → GitHub** → 手順1のリポジトリを選択
3. 設定はすべて空欄のまま（Build command なし、Publish directory は空 or `/`）→ **Deploy**
4. 公開URL（例 `https://xxxx.netlify.app`）が発行される
   - **Site configuration → Change site name** で `ef-tea-ceremony` などに変更可 → `https://ef-tea-ceremony.netlify.app`
5. URLが決まったら Claude に伝える → QRコードを作ってパワポ（表紙・最終スライド）に入れます

## 3. 更新するとき
- GitHub のリポジトリ画面で `index.html` を開き、鉛筆アイコンで編集 → Commit
  または新しいファイルをドラッグ＆ドロップで上書き → Commit
- Netlify が自動で再公開（1分程度）。URLは変わらないのでQRコードもそのまま使えます

## メモ
- 🔊 発音ボタンはブラウザの読み上げ機能（Web Speech API）を使います。iPhone / Android / PC の主要ブラウザで動作します。音声がない環境では案内文が出ます。
- Google Fonts（BIZ UDPGothic）を読み込んでいます。オフラインでも端末のフォントで表示されます。
