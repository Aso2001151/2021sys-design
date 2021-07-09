# DB定義書
## ER図
[ER図はこちら](http://www.plantuml.com/plantuml/png/fPLVJnj74C3VxrDidGTIDQwnbFv9XA8Gb5OeDLHWgQggwhJrBURA_N7tpW8BaBYzba00DGq2cj9IqePY81XKqvOeBlqmmzdk4r-XUtjcEHAZ87KVrZixixFpcvbRttPSJDsYQIYf3WMXOBKANkNuS1UypSPgfR4p1zxFuAsA-MjWPV2hu4y3-xKrUpkDdwQQix-3znYOC6OUzy1TYSrAy70Xc5qugSq4bH_gI_idjLbWZ_YwSRJ5hm1l0RoZyEmKuqU6NRVWt4ob2WQsmfZUpjbcwakSSaPqgu0fDfMEbAAyeP4XtI8eqpsOlJkWPhe7xgaz_H_r3w0FAIuXgSyETFSDTlTaU_lxuaQV3EikKPGEOFlWRu5_7_mQiB_0tmpPl2LEoqc2zOFWuGowCZQM71kBNTdRfzxjo_PcFqLNChhbzb22pMH6TzpIWEqG9SgYSBe4Z7lV0N-6Pu939oG5oXdOSHASlrdUvRa0RqLc8IHyoH2DAuYFZgWsJN--_dXFxDp1kP4yjOkMrcCRDaM3bZqQDwslhKTsDjK8ZMpk6FnGP0J-DlZFpjDNUAn2sqsfFHe_Cgae1VwBymGbxlO0-mFOKywMGDX1BgPvugfEoN69sGfN928SuAy1Umxid_0cVrhCos5Ys2EKWIcFEn5rg0Bx4zYU32RKPn5us-25hT9yKcwMls_vFAbzLr--7-okX6esYnB7XoyItBOCtXnA14UBeN343zPNDke_FcjkhuNDnXZtqApD1j_kDVs_8rSytM91B5TtIoZnxvFDeFABZ5dWvOgEQvk4eYvJFLqxjr1NL-RQApruwvRWZyPRygYQipM2FllutkTIcKpAPO5NMGeMDeaKiAPH4bEwn91h4-jdWaOCTSZ0URb1ILxLi1kvcZmFsQpMWcysuiKGdA9DK9Uc5eeqDumT4Z9chxNxZWHe_6k8Gmi_ggvTo7lbvRny4BCxlLn67u7RBZRK0jLpagWDKdEhsZZORm-cQiJb6OlpjRR-BoQAWGfDv5QeBaw1xXAp3Rv45CCgccrnWwNfOD4xrwR2eHFsg5XShZzb41S6AYnaJye8uxN4BidRjCHvpwFe9ivBGv6KopLi6rvWE-8Fvq0yMZ5gUNi8Vhg-77iyxele9NZR22VbUnzxrhmAU4_5ipKFx04NeqUdlloyNbsA_SbzfUik5lzmPf7Y4MpgITDCYTgbhkVUwTJIDwxVmEz_aUxiJBzBXjwB4f8KWozkfgKyCI5aX2qDsPPHGcSgMwWwaKrZcydnSDF4LkdCXTXAXtQcJGcwcZv-iN5y-E3DCq_ZqbDu4btjFBLGm5i4DW_UEdZbnk5luEt4CZ2doESp6XDsoncAlY15p4YEYObMEEZSTwl41L6045osgAE86SanQKlzQQ5v1Wqov8PR1b4GrVF3eK1r1HKBmfB_AaYpHotHeJOlSKUgJVnKVnq1rI_9eDclep38AnotYQKLJUC_)

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



### カテゴリマスタ(m_category)
|和名|属性名（カラム）|型|PK|NN|FK|
|:---|:---|:---|:---:|:---:|:---:|
|カテゴリID|category_id|int(11)|〇|〇||
|氏名|name|varchar(20)||〇||
|登録日|reg_date|date||〇||



### 商品マスタ(m_items)
|和名|属性名（カラム）|型|PK|NN|FK|
|:---|:---|:---|:---:|:---:|:---:|
|商品コード|item_code|int(11)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|カテゴリID|category_id|int(11)||〇||
|画像ファイル名|image|carchar(200)||〇||
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||
