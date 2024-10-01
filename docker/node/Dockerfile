FROM node:14

# 作業ディレクトリを設定
WORKDIR /var/www

# Vue.jsの依存関係をインストール
COPY package*.json ./
RUN npm install

# ソースコードをコピー
COPY . .

# ビルド
RUN npm run build