# 人と人のつながり可視化サービス「TSUNAGARI」

<img src="https://github.com/user-attachments/assets/821a4098-ce0d-4ee2-9801-77d03af95aa6" width="35%">

## 人、場所、イベントをつないで可視化することで、以下の課題を解決できます。
* 名刺の整理が面倒
  * → 面倒だった名刺の管理が楽しい
* 出会った人が思い出せない
  * → どうやって会えたかわかる
  * → 過去の自分の振り返りができる

### 現在、開発は途中で止まっている状況です。
#### 新潟で行われたハッカソン「DERTA Gig HACKS in Niigata」での成果物です。
* [DERTA Gig HACKS in Niigataについて](https://derta.notion.site/DERTA-Gig-HACKS-in-Niigata-1315f95e18204c18bb891e22bb5e053b)


# 開発について
* フロントエンドは/publicディレクトリです。
  * バニラJavaScriptであるためnpmなどのパッケージ管理サービス、Dockerfileは用意していません。
  * ポートはバックエンドと同じhttp://localhost:3000/ です。
* OCRはlib/ocrディレクトリです。
  * ポートはhttp://localhost:5001/ にしています。

## 開発環境のセットアップ

#### .envファイルを作成
* 以下は例です。任意の値を設定してください
```env
DATABASE_HOST=db
DATABASE_USERNAME=your_db_username
DATABASE_PASSWORD=your_db_password
DATABASE_NAME=your_db_name
DATABASE_PORT=3306
SERVICE_URL=http://ocr_service:5001
```

#### Dockerコンテナの起動
```
docker-compose build
```

```
docker-compose up
```

#### localhostにアクセス
```
http://localhost:3000/
```

#### 初期データの投入コマンド
```
docker-compose run web rails db:seed
```
