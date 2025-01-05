# Node.jsのイメージを指定
FROM node:23.5.0

# 作業ディレクトリを設定
WORKDIR /app

# package.jsonとpackage-lock.jsonをコピー
COPY ./src/package.json ./src/package-lock.json /app/

# 依存関係をインストール
RUN npm install

# アプリケーションのソースコードをコピー
COPY ./src /app

# ポート3000を公開
EXPOSE 3000

# 開発サーバーを起動（npm run dev でソース変更時にビルドしてくれる）
CMD ["npm", "run", "dev"]