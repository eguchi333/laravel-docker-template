# Laravel Lesson レビュー②

## Todo編集機能

### @method('PUT')を記述した行に何が出力されているか
<!-- <input type="hidden" name="_method" value="PUT"> -->
### findメソッドの引数に指定しているIDは何のIDか
Todoインスタンス
### findメソッドで実行しているSQLは何か
SELECT * FROM todos WHERE id = $id;
### findメソッドで取得できる値は何か
Modelオブジェクト
### saveメソッドは何を基準にINSERTとUPDATEを切り替えているのか
saveメソッドを行うよりも前にfindメソッドを実行しルートパラメータで指定したidのレコードを取得しているかどうか
Todoインスタンス内のwasRecentlyCreatedプロパティがtrueかfalseか

## Todo論理削除

### traitとclassの違いとは
インスタンスかできるか
一つのclassに対し、複数のtraitを追加することができる
### traitを使用するメリットとは
複数のクラス間でプロパティ、メソッドを共通化し再利用できるようにするために使用する
## その他

### TodoControllerクラスのコンストラクタはどのタイミングで実行されるか
リクエストが送信されるとき
### RequestクラスからFormRequestクラスに変更した理由
バリデーション等の処理を切り離し保守性を高めるため
### $errorsのhasメソッドの引数・返り値は何か
引数: str
返り値: bool値
### $errorsのfirstメソッドの引数・返り値は何か
引数: str
返り値: str
### フレームワークとは何か
指定のディレクトリにファイルを配置し、処理を書き加えることで効率よくアプリケーションを作成することができるようにしたもの
### MVCはどういったアーキテクチャか
Model, View, Controllerに役割を分け、相互にやり取りを行うことで再利用性と可読性、保守性を上昇させることができるアーキテクチャ
### ORMとは何か、またLaravelが使用しているORMは何か
ORM: ClassとテーブルをマッピングすることでSQLを直接操作することなくDBとのやり取りを可能とするもの
LaravelのORMはEloquent
### composer.json, composer.lockとは何か
compose.json: 依存するパッケージやライブラリを定義するためのファイル

composer.lock: installコマンド実行時にcomposer.lockファイルがあるならファイル内に書かれているバージョンをダウンロードする -> チーム間でバージョンを統一することができる
### composerでインストールしたパッケージ（ライブラリ）はどのディレクトリに格納されるのか
vender/
