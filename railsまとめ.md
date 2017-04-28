# 主に利用するサイト
* Rails チュートリアル
https://railstutorial.jp/
* Rails ガイド
https://railsguides.jp/
* API ドキュメント
http://api.rubyonrails.org/


# Rails：GitHubからコードをダウンロードして動かしてみるまでの手順
以下を参考にする
http://tyoshikawa1106.hatenablog.com/entry/2015/09/07/164134


# 1章でのまとめ
## Bundlerについて
Bundler は RubyGems と一緒に使われる、アプリケーションの依存関係を管理するためのツール
より詳細については、以下を参考にする
※ Bundler（英語）
http://bundler.io/
※ Bundler 入門（バージョンは古い）
http://ruby.studio-kingdom.com/bundler/guides/getting_started
※ Bundler の使い方（qiita）
http://qiita.com/oshou/items/6283c2315dc7dd244aef


# 2章でのまとめ
## protect_from_forgery with: :exception について
app/controllers/application_controller.rb
protect_from_forgery がコントローラーに記述されていると、CSRF対策が有効になる
Rails のセキュリティについては以下をを参考にする
https://railsguides.jp/security.html


## ルーティングについて
config/routes.rb
Rails のルーティングについては以下を参考にする
https://railsguides.jp/routing.html
$ rails routes でルーティングの一覧が出力される


## rails コマンドについて
$ rails generate scaffold User name:string email:string
rails のコマンドについては以下を参考にする（generate について記載されている）
https://railsguides.jp/command_line.html
#  !!! scaffold についてかけたら書く
※ rake コマンドは rails4 以前では使い方を覚える必要がある


## rails db:migrate について
rails のコマンドについては以下を参考にする（db について記載されている）
https://railsguides.jp/command_line.html
より詳しい、マイグレーションについては以下を参考にする
https://railsguides.jp/active_record_migrations.html


## rails server について
rails コマンドについてに記載されている URL を参考にする


## ルーティングの resources や resource について
ルーティングについてに記載されている URL を参考にする


## Rails における REST について
Rails チュートリアルの以下のコラムを参考にする
コラム 2.2 REpresentational State Transfer (REST)
https://railstutorial.jp/chapters/toy_app?version=5.0#aside-REST


## Prefix_path について（path ヘルパー）
※ Prefix は $ rails routes で表示される Prefix のこと
ルーティングについてを参考にする
以下も Rails ガイドではないが参考にする
http://qiita.com/higeaaa/items/df8feaa5b6f12e13fb6f


## Active Record について
Active Record については以下を参考にする
* Active Record の基礎
https://railsguides.jp/active_record_basics.html
* Active Record マイグレーション
https://railsguides.jp/active_record_migrations.html
* Active Record バリデーション
https://railsguides.jp/active_record_validations.html
* Active Record コールバック
https://railsguides.jp/active_record_callbacks.html
* Active Record の関連付け
https://railsguides.jp/association_basics.html
* Active Record クエリインターフェイス
https://railsguides.jp/active_record_querying.html


## バリデーションについて
バリデーションについては以下を参考にする
https://railsguides.jp/active_record_validations.html


## データモデル同士の関連付けについて（Active Record の関連付け）
Active Record の関連付けについては以下を参考にする
https://railsguides.jp/association_basics.html


## rails console について
rails コマンドについてに記載されている URL を参考にする


## コントローラーとモデルのクラス階層について
Rails チュートリアル 2.3.4 継承の階層 を参考にする
https://railstutorial.jp/chapters/toy_app?version=5.0#sec-inheritance_hierarchies
※ コントローラーもモデルも基本クラスを継承しているということを理解できれば良い。


--


# 3章でのまとめ
## コントローラーの生成
rails genetare controller については ## rails コマンドについて を参考にする


## コントローラーについて
コントローラーについては以下を参考にする
https://railsguides.jp/action_controller_overview.html


## 元に戻す方法について
コラム 3.1 元に戻す方法 を参考にする
https://railstutorial.jp/chapters/static_pages?version=5.0#aside-undoing_things
※ 最初の状態に戻したいときは、VERSION=0オプションを使う の箇所があるので参考にすると良い

より詳細については以下を参考にする
* rails destroy について
https://railsguides.jp/command_line.html#rails-destroy
* rails db:rollback （ロールバック）について
https://railsguides.jp/active_record_migrations.html#%E3%83%AD%E3%83%BC%E3%83%AB%E3%83%90%E3%83%83%E3%82%AF


## テストについて
Rails 標準のテストは Minitest らしい。
テストについては以下を参考にする
https://railsguides.jp/testing.html

Minitest で使用できるアサーション、Rails 固有のアサーションが存在している


## Prefix_url について（url ヘルパー）
※ Prefix は $ rails routes で表示される Prefix のこと
ルーティングについてを参考にする
以下も Rails ガイドではないが参考にする
http://qiita.com/higeaaa/items/df8feaa5b6f12e13fb6f


## ビューについて（ERB タグが出てきたので）
ビューについては以下を参考にする
* Action View の概要
https://railsguides.jp/action_view_overview.html
* レイアウトとレンダリング
https://railsguides.jp/layouts_and_rendering.html
* Action View フォームヘルパー
https://railsguides.jp/form_helpers.html


## Rails の provide 関数と yield 関数について
provide 関数と yield 関数については以下を参考にする（ガイドには見当たらなかった）
http://qiita.com/rentalgambler/items/3fd7c050b4ad2c424957
http://tbpgr.hatenablog.com/entry/20130716/1373989560


## レイアウトについて
レイアウトについては、ビューについて を参考にする


## Guardによるテストの自動化 について
よくわってないので後で調べる


--


# 4章でのまとめ
## Rails の組み込みヘルパーについて
以下のページの Action View が提供するヘルパーの概要 あたりを参考にする
https://railsguides.jp/action_view_overview.html#action-view%E3%81%8C%E6%8F%90%E4%BE%9B%E3%81%99%E3%82%8B%E3%83%98%E3%83%AB%E3%83%91%E3%83%BC%E3%81%AE%E6%A6%82%E8%A6%81

※ カスタムヘルパーについては、Rails ガイドになかったため Rails チュートリアルを参考にする


## モジュールについて
Rails チュートリアル 4.2.5 title ヘルパー、再び を参考にする（さわり程度は書いてある）


--


# 5章でのまとめ
## Rails のヘルパー link_to について
link_toの第1引数はリンクテキスト、第2引数はURL,第3引数はオプションハッシュ
詳細は API ドキュメント で検索


## Sass について（SCSS）
Sass については以下を参考にする
* Sass 公式（英語）
http://sass-lang.com/
* Sass（SCSS）入門
http://www.buildinsider.net/web/rubyonrails4/0903
※ 上記で記載されている CoffeeScript については、同サイト内にリンクがあるので
そちらを参考にする
* CSSのメタ言語Sass(SCSS)、LESSの完全入門
http://qiita.com/ritukiii/items/67b3c50002b48c6186d6

## パーシャル について（partial）
パーシャルについては Action View の概要 内にある以下を参考にする
* 3.2 パーシャル、
https://railsguides.jp/action_view_overview.html#%E3%83%91%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB
* 4 パーシャルレイアウト
https://railsguides.jp/action_view_overview.html#%E3%83%91%E3%83%BC%E3%82%B7%E3%83%A3%E3%83%AB%E3%83%AC%E3%82%A4%E3%82%A2%E3%82%A6%E3%83%88


## アセットパイプライン について
アセットパイプライン については以下を参考にする
https://railsguides.jp/asset_pipeline.html


## マニフェストファイル について
マニフェストファイルについては、アセットパイプライン内にある以下を参考にする
* 2.4 マニフェストファイルとディレクティブ
https://railsguides.jp/asset_pipeline.html#%E3%83%9E%E3%83%8B%E3%83%95%E3%82%A7%E3%82%B9%E3%83%88%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%A8%E3%83%87%E3%82%A3%E3%83%AC%E3%82%AF%E3%83%86%E3%82%A3%E3%83%96


## プリプロセス について（チュートリアルではプリプロセッサ）
プリプロセスについては、アセットパイプライン内にある以下を参考にする
* 2.5 プリプロセス
https://railsguides.jp/asset_pipeline.html#%E3%83%97%E3%83%AA%E3%83%97%E3%83%AD%E3%82%BB%E3%82%B9


## 本番環境での効率性 について
アセットパイプラインのメリット等があるので、参考にすること
※ 5章で 本番環境での効率性 で検索をして該当箇所を参考にする


## Rails のルートURL について
ルーティングについて を参考にする
Prefix_path について（path ヘルパー） を参考にする

チュートリアルにもあるように、以下のような一般的な規約に従う
Prefix_path書式: 基本的にはこちらを使用する
Prefix_url書式:  リダイレクトの場合のみ使用する


## リンクのテスト について（統合/結合テスト、integration test）
integration test については、Rails テスティングガイド 内にある以下を参考にする
* 5 結合テスト
https://railsguides.jp/testing.html#%E7%B5%90%E5%90%88%E3%83%86%E3%82%B9%E3%83%88

### assert_select について
assert_selectには2つの書式があります。

* 1つ目の書式
assert_select(セレクタ, [確認条件], [失敗時のメッセージ])
セレクタで指定された要素が条件に一致することを主張します。
セレクタにはCSSセレクタの式 (文字列) や代入値を持つ式を使用できます。

* 2つ目の書式
assert_select(要素, セレクタ, [確認条件], [失敗時のメッセージ])
選択されたすべての要素が条件に一致することを主張します。
選択される要素は、element (Nokogiri::XML::Node or Nokogiri::XML::NodeSetのインスタンス)
 からその子孫要素までの範囲から選択されます。
