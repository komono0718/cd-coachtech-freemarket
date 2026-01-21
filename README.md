# coachtechフリマ

## 概要
coachtechフリマは、商品を出品・購入できるフリマアプリです。  
ユーザーは会員登録後、商品の出品・購入・いいね・コメントなどの機能を利用できます。

本アプリケーションは、COACHTECHの課題要件に基づき作成しています。

---

## 使用技術

- PHP 8.x  
- Laravel 10.x  
- MySQL  
- Docker  
- GitHub  

---

## 環境構築

### 1. リポジトリをクローン

```bash
git clone https://github.com/komono0718/cd-coachtech-freemarket.git
cd cd-coachtech-freemarket
```

### 2. Dockerを起動

```bash
docker compose up -d --build
```

### 3. Laravel初期設定

```bash
cp src/.env.example src/.env
docker compose exec app php artisan key:generate
```

### 4. マイグレーション・シーディング

```bash
docker compose exec app php artisan migrate --seed
```

### 5. アプリケーション起動

ブラウザで以下にアクセスしてください。
http://localhost


## ダミーデータについて

以下の情報がシーディングにより作成されます。
	•	ユーザー情報
	•	商品情報（商品データ一覧に基づく10件）
	•	カテゴリ情報

### 主な機能

	•	会員登録 / ログイン / ログアウト
	•	商品一覧表示
	•	商品検索機能
	•	商品詳細表示
	•	いいね機能
	•	コメント機能
	•	商品出品機能
	•	商品購入機能
	•	プロフィール編集機能
