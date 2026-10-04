# 作成
## テーブル一覧
### posts_table(投稿)
| カラム名 | データ型  | 制約  | 説明  |
|:-----|:-------|:-----|:-----------|
|id | BIGINT |PRIMARY KEY, <br>AUTO_INCREMENT | 投稿を一つずつ区別する番号|
|user_id | BIGINT | FOREIGN KEY | 投稿したユーザーid|
|category_id | BIGINT | FOREIGN KEY | 選択されたカテゴリid |
|title | VARCHAR(255) | Not Null | 投稿のタイトル|
|content | TEXT | Not Null | 投稿の内容 |
|created_at | TIMESTAMP | - | 登録した日時 |
|updated_at | TIMESTAMP | - | 更新した日時 |



&nbsp;
&nbsp;


# 参考
## テーブル一覧
### posts(投稿)
| カラム名 | データ型 | 制約 | 説明 |
|---|---|---|---|
| id | BIGINT | PRIMARY KEY, AUTO_INCREMENT | 投稿を1件ずつ区別する番号 |
| user_id | BIGINT | NOT NULL, FOREIGN KEY | 誰が書いた投稿か |
| category_id | BIGINT | NOT NULL, FOREIGN KEY | どのカテゴリに属する投稿か |
| title | VARCHAR(255) | NOT NULL | 投稿のタイトル |
| content | TEXT | NOT NULL | 投稿の本文 |
| created_at | TIMESTAMP | - | 登録した日時 |
| updated_at | TIMESTAMP | - | 最後に書き換えた日時 |