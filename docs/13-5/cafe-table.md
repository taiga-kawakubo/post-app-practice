# 作成
## テーブル一覧
### products_table(商品)
| カラム名 | データ型  | 制約  | 説明  |
|:-----|:-------|:-----|:-----------|
|id|BIGINT|PRIMARY KEY, AUTO_INCREMENT|商品ごとの番号|
|name|VARCHAR(50)|NOT NULL|商品名|
|price|INT|NOT NULL|商品の値段
|description|VARCHAR(100)|-|説明|
|is_available|BOOLEAN|NOT NULL|売り切れはfalse|
|created_at|TIMESTAMP|-|登録した日時|
|updated_at|TIMESTAMP|-|更新した日時|



### orders_table(注文)
| カラム名 | データ型  | 制約  | 説明  |
|:-----|:-------|:-----|:-----------|
|id|BIGINT|PRIMARY KEY, AUTO_INCREMENT|注文ごとの番号|
|order_number|VARCHAR(6)|NOT NULL, UNIQUE|お客様に伝える注文番号|
|total_amount|INT|NOT NULL|合計金額|
|status|VARCHAR(20)|NOT NULL|受けとり状態|
|ordered_at|DATETIME|NOT NULL|注文日時|
|created_at|TIMESTAMP|-|登録した日時|
|updated_at|TIMESTAMP|-|更新した日時|



### order_items_table(注文詳細)
| カラム名 | データ型  | 制約  | 説明  |
|:-----|:-------|:-----|:-----------|
|id|BIGINT|PRIMARY KEY, AUTO_INCREMENT|注文詳細ごとの番号|
|ordere_id|BIGINT|NOT NULL, FOREIGN KEY|どの注文の詳細か|
|product_id|BIGINT|NOT NULL, FOREIGN KEY|どの商品か|
|quantity|INT|NOT NULL|個数|
|price|INT|NOT NULL|注文した時の商品の１つ文の値段|
|created_at|TIMESTAMP|-|登録した日時|
|updated_at|TIMESTAMP|-|更新した日時|