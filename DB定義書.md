# DB定義書
## ER図
[ER図はこちら]

# DBテーブルカラム詳細一覧

### 購入テーブル(d_purchase)
|和名|属性名（カラム名）|型|PK|NN|FK|
|:---|:---|:---|:---:|:---:|:---:|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客コード|customer_code|varchar(50)||〇||
|購入日|purchase_date|date||〇||
|総額|total_price|int(11)||〇||



### 購入詳細テーブル(d_purchase_detail)
|和名|属性名（カラム名）|型|PK|NN|FK|
|:---|:---|:---|:---:|:---:|:---:|
|オーダー詳細ID|detail_id|bigint(20)|〇|〇||
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|商品コード|item_code|int(11)||〇||
|価格|price|int(11)||〇||
|数量|num|int(11)||〇||



### 顧客マスタ(m_customers)
|和名|属性名（カラム）|型|PK|NN|FK|
|:---|:---|:---|:---:|:---:|:---:|
|顧客コード|customer_code|varchar(50)|〇|〇||
|パスワード|pass|varchar(50)|〇|〇|〇|
|氏名|name|varchar(20)||〇||
|住所|adress|varchar(100)||〇||
|電話番号|tel|varchar(20)||〇||
|メールアドレス|mail|varchar(100)||〇||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||



### m_category
|属性|型|PK|NN|FK|
|:---|:---|:---:|:---:|:---:|
|category_id|int(11)|〇|〇||
|name|varchar(20)||〇||
|reg_date|date||〇||



### m_items
|属性|型|PK|NN|FK|
|:---|:---|:---:|:---:|:---:|
|item_code|int(11)|〇|〇||
|item_name|varchar(50)||〇||
|price|int(11)||〇||
|category_id|int(11)||〇||
|image|carchar(200)||〇||
|detail|varchar(500)||||
|del_flag|int(11)||||
|reg_date|date||〇||
