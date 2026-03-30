# 株式秒読みカウントダウン PWA

将棋の秒読みのように株式市場の寄り・引けをカウントダウンするPWAです。

## ファイル構成

```
stock-countdown-pwa/
├── index.html      ← メインアプリ
├── manifest.json   ← PWA設定
├── sw.js           ← Service Worker（オフライン対応）
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## 公開手順（GitHub Pages）

### 1. GitHubリポジトリを作成

```bash
git init
git add .
git commit -m "初回コミット"
git remote add origin https://github.com/あなたのユーザー名/stock-countdown.git
git push -u origin main
```

### 2. GitHub Pagesを有効化

1. リポジトリの **Settings** → **Pages** を開く
2. Source: **Deploy from a branch**
3. Branch: **main** / `/ (root)` を選択
4. **Save** をクリック

数分後に `https://あなたのユーザー名.github.io/stock-countdown/` で公開されます。

### 3. スマホにインストール

**Android（Chrome）**
1. ブラウザでURLを開く
2. アドレスバー右の「インストール」アイコンをタップ
3. 「追加」でホーム画面に追加

**iPhone（Safari）**
1. Safariでアクセス
2. 共有ボタン → 「ホーム画面に追加」
3. 「追加」でホーム画面に追加

## 機能

- 東京証券取引所（前場・後場の寄り引け）
- NYSE / NASDAQ（プレマーケット〜アフターアワー）
- 残り10秒から将棋の秒読みスタイルで読み上げ
- オフライン対応（Service Workerによるキャッシュ）
- ホーム画面追加ボタン（Android Chromeで自動表示）

## 次のステップ

- **Electron化**（Windowsデスクトップアプリ）→ `main.js` + `package.json` を追加
- **Capacitor化**（App Store / Google Play）→ `capacitor.config.ts` を追加
