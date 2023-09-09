FROM node:16

RUN npm install -g http-server
# 作業ディレクトリ
WORKDIR /app
# Docker側にpackageファイルをコピーする
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 8080
# web serverを起動する
CMD ["http-server", "dist"]