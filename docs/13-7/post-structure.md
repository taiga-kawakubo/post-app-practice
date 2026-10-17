# 作成
## 構造図

| まとまり | 実物の場所 | 実物の場所 |
| :----- | :-------- | :-------- |
| ルート | routes/web.php | URLと対象のControllerを結ぶ |
| Controller | app/Http/Controllers/PostController.php | 受け取った内容に対して何を返答するかを決める |
| View | app/Policies/PostPolicy.php | 画面への表示 |
| Policy | app/Models/User.php・Post.php・Category.php | 送信元の操作の権限を確認する。|
| Model | resources/views/posts/index.blade.php・edit.blade.php | データの読み書き、テーブル同士の結びつきを決める |
| Database | users・categories・posts テーブル  |　保存する内容 |


&nbsp;
&nbsp;


# 参考
## 構造図
| まとまり | 実物の場所 | 置くもの |
|---|---|---|
| ルーティング | `routes/web.php` | どのURLが、どのコントローラーの何を呼ぶか。ログインが要るかどうか |
| コントローラー | `app/Http/Controllers/PostController.php` | 受け取った内容をどう扱い、どの画面を返すか。どんな値まで受け付けるか |
| 認可 | `app/Policies/PostPolicy.php` | 誰がその投稿を編集・削除してよいか |
| モデル | `app/Models/User.php`・`Post.php`・`Category.php` | データの読み書きと、テーブルどうしのつながり |
| ビュー | `resources/views/posts/index.blade.php`・`edit.blade.php` | 画面に並べるもの |
| データベース | `users`・`categories`・`posts` テーブル | 覚えておく中身 |