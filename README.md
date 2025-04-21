## 🎥 Demo Video

※Zenn記事も書きました！ 
[「はじめまして！ブログを始めます」](https://zenn.dev/satoshiichiban/articles/8ba5073a299db7)
<br>
<br>
<br>
このツールのデモ動画はこちらです！  
実際の動作を確認できます。  
**画像をクリック**して再生してみてください。


<p align="center">
    <img src="https://github.com/satoshiichiban/NearbyFinder/blob/main/images/flashing-hand2.gif" width="40">
</p>

[![サムネイル画像](https://github.com/satoshiichiban/NearbyFinder/blob/main/images/nearbyfinderthumbnail.png?raw=true)](https://youtu.be/UyWmTlI-kr4)


## プロジェクト概要
<br>
場所検索の為の、3kmと5kmの距離スイッチ機能を追加しました。
コードの構造とロジックを改善しました。

Node.js・Expressを使用して施設検索ツールを作成したプロジェクトです。
<br><br>
4つのAPIを活用、特定のキーワード／条件で施設を検索できる機能を提供します。
<br>
Maps JavaScript API<br>
Geolocation API<br>
Directions API<br>
Places API

---

## ローカルでの実行環境
- URL: `http://localhost:3000`

---

## 主なファイル
- **server.js**: バックエンドロジック。外部API（Google Places API）通信・エラーハンドリング部。
- **script.js**: フロントエンドロジック。ユーザー入力処理と検索結果のfetchを担っています。
- **index.html**: ユーザーインターフェース（検索フォームと結果表示デザイン）。レスポンシブデザインを採用しています。

　　※機密情報は環境変数で管理しています。

---

## 設計方針
- **コードの可読性向上**: フロントエンド／バックエンドで分割、整理しています。
- **機能の追加・修正のしやすさ**: 各ファイルが明確な役割を持つ為、影響範囲を最小化しました。
- **拡張性**: 将来的な機能追加や変更を考慮した構造。
- **レスポンシブデザイン**: スマホ、タブレット、PCなど多様な画面サイズに最適表示で拡大縮小対応。
- **静的コンテンツ／動的処理に対応**:-
  静的コンテンツは `public` フォルダ内の HTML や JavaScript をブラウザに直接提供します。
  動的処理は、キーワードや現在地をサーバーに送信→Google Places APIで検索結果を生成します。


## デプロイ環境とCI/CD構成

以下の構成で自動デプロイを行っています。

- **GitHub Actions**  
　※フロントエンドのみのため、リポジトリでは非公開です。

- **Render**  
　https://nearbyfinder.onrender.com/  
　※無料プランで稼働中のため、初回アクセス時に起動待ち時間が発生します。  
　今後、別のホスティングサービスへの移行も検討中です。

CI/CDにより、デプロイ作業を省力化し、継続的な改善・運用を実現しています。


★★動作確認環境  
以下のOSで動作確認済みです：
- macOS（Safari / Google Chrome）
- Windows 11 Home（24H2）  
  Microsoft Edge / Google Chrome にて動作確認

クロスブラウザ・クロスプラットフォームに配慮して設計をしています。


---

## 主な機能
1. **施設検索**:
   - ユーザーがキーワードと条件（距離、最大件数）を入力し、指定範囲内の施設を検索。
   - 例: 「カフェ」と入力すると、近隣のカフェを一覧表示。
2. **検索結果表示**:
   - 施設名、住所、距離、評価、口コミ数をカード形式で表示。
   - 例: 「スターバックス」「住所: ◯◯」「距離: 1.2km」など。
3. **エラーハンドリング**:
   - キーワード未入力時やAPIエラー時に、適切なエラーメッセージを表示。
     
---

## 使用アイコンについて

経路表示のホームピンは、Google Fonts の「Material Symbols」から提供されている  
「Home Pin」アイコンを使用しています。

![Home Pin icon](images/home-pin.png)

※出典：  
[Google Fonts - Home Pin (Material Symbols)](https://fonts.google.com/icons?selected=Material+Symbols+Outlined:home_pin)

ライセンス：Apache License 2.0（商用利用・改変可能）

---

## 使用方法
1. このリポジトリをクローンします。
   ```bash
   git clone https://github.com/satoshiichiban/NearbyFinder.git
2. 必要な依存関係をインストールします:
   ```bash
   npm install
3. サーバーを起動します。
   ```bash
   node server.js
4. ブラウザで以下にアクセス  
   [http://localhost:3000/](http://localhost:3000/)

---
## 🌟 開発を支援する
このツールが役に立ったと感じたら、サポートしていただけると嬉しいです！  
[Buy Me a Coffee](https://www.buymeacoffee.com/satoshiichiban)
