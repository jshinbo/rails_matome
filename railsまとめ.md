# 主に利用するサイト
## Rails 関係
* Rails チュートリアル
https://railstutorial.jp/
* Rails ガイド
https://railsguides.jp/
* API ドキュメント
http://api.rubyonrails.org/
* 演習の解答
http://qiita.com/mochikichi321/items/ea641d218df4a3941aad
http://mochikichi.hatenablog.com/entry/2017/02/06/212658


## Ruby 関係
* Ruby リファレンスマニュアル
https://docs.ruby-lang.org/ja/
* るりまサーチ（Ruby リファレンス検索）
https://docs.ruby-lang.org/ja/search/
* Ruby Style ガイド
https://github.com/fortissimo1997/ruby-style-guide/blob/japanese/README.ja.md


--


# Rails：GitHubからコードをダウンロードして動かしてみるまでの手順
* 抜粋
  1. gem install bundler
  2. bundle install
  3. rails db:migrate
  4. rails s

詳細は以下を参考にする
http://tyoshikawa1106.hatenablog.com/entry/2015/09/07/164134


--


# Rails チュートリアル の前に
目を通すだけでもチュートリアル時の理解が違うかもしれない
* Rails ガイド の Rails をはじめよう
https://railsguides.jp/getting_started.html
* ドットインストール（バージョンが古いので雰囲気をつかむ程度なら）
http://dotinstall.com/lessons/basic_rails_v2
* Progate（有料会員向けが多いのでなんとも言えない）
https://prog-8.com/languages/rails


## Cloud9、Bitbucket、Heroku の利用について
クレジットカードの登録が必要になるが（料金は発生しない）、個人で問題がなければ
Rails チュートリアルに従って Cloud9、Bitbucket、Heroku を利用したほうが早い


--


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


--


# 6章でのまとめ
## マイグレーションについて
Active Record マイグレーション を参考にする
https://railsguides.jp/active_record_migrations.html

## 6.1.2 model ファイル について
Active Record について を参考にする
以下、URL引用
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


## 6.1.3 ユーザーオブジェクトを作成する について
Active Record の基礎 5.1 Create を参考にする
https://railsguides.jp/active_record_basics.html#create

new、save、create の違いが記載されている


## 6.1.4 ユーザーオブジェクトを検索する について
Rails ガイド の以下を参考にする
https://railsguides.jp/active_record_querying.html


## 6.1.5 ユーザーオブジェクトを更新する
reload: データベースの情報を元にオブジェクトを再読み込みする
update_attributes: 属性のハッシュを受け取り、成功時には更新と保存を続けて同時に行う
update_attribute:  同上（※特定の属性のみを更新する）

※ 詳細は API ドキュメント を参考にする


## 6.2 ユーザーを検証する について
Active Record バリデーション を参考にする
https://railsguides.jp/active_record_validations.html

※ テストは テストについて を以下を参考にする
https://railsguides.jp/testing.html


## コラム 6.2. データベースのインデックス
Rails チュートリアルを参考にする


## rails genetate migration について
Active Record マイグレーション を参考にする
https://railsguides.jp/active_record_migrations.html


## コールバック について
Active Record コールバック を参考にする
https://railsguides.jp/active_record_callbacks.html


## 6.3 セキュアなパスワードを追加する について
このあたりから、Rails のビルトイン has_secure_password を利用した
認証、認可のチュートリアルが始まるので、飛ばさずに進めることを推奨


## has_secure_password について
モデルに has_secure_password を追加することで、以下の様な機能が利用できる
ただし、モデル内にpassword_digestという属性が含まれている必要がある

* セキュアにハッシュ化したパスワードを、データベース内のpassword_digestという属性に保存できるようになる
* 2つのペアの仮想的な属性 (passwordとpassword_confirmation) が使えるようになる
  - また、存在性と値が一致するかどうかのバリデーションも追加される
* authenticateメソッドが使えるようになる
  - (引数の文字列がパスワードと一致するとUserオブジェクトを、間違っているとfalseを返すメソッド)

※ いくつか注意点について、Rails チュートリアル にあるので読むことを推奨


--


# 7章でのまとめ
## デバッグ について
Rails アプリケーションのデバッグ を参考にする
https://railsguides.jp/debugging_rails_applications.html


## Rails の環境について
Rails チュートリアル の　コラム 7.1. Railsの3つの環境 を参考にする


## 7.1.3 debuggerメソッド について（byebug gem）
※ この debugger メソッドは Rails 標準のデバック機能ではない

byebug について Rails チュートリアル で不足な場合は以下を参考にする
* printデバッグにさようなら！Ruby初心者のためのByebugチュートリアル
http://qiita.com/jnchito/items/5aaf323ab4f24b526a61
* byebugでRubyスクリプトをコマンドラインデバッグする
http://qiita.com/aosho235/items/6f988a0b5262b95ca460


## form_forヘルパー について
Action View フォームヘルパー についての詳細は以下を参考にする
https://railsguides.jp/form_helpers.html


## 7.3.2 Strong Parameters について
Action Controller の概要 の 4.5 Strong Parameters を参考にする
https://railsguides.jp/action_controller_overview.html#strong-parameters


## 7.3.3 エラーメッセージ について
Active Record バリデーション の 7 バリデーションエラーに対応する を参考にする
https://railsguides.jp/active_record_validations.html#%E3%83%90%E3%83%AA%E3%83%87%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%AB%E5%AF%BE%E5%BF%9C%E3%81%99%E3%82%8B

### shared/ ディレクトリについて
Rails全般の慣習で、パーシャルは複数のコントローラにわたるビューに対し、専用のshared/ディレクトリを使用する

### エラーメッセジをビューで表示する について
Active Record バリデーション の バリデーションエラーをビューで表示する を参考にする
https://railsguides.jp/active_record_validations.html#%E3%83%90%E3%83%AA%E3%83%87%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%A8%E3%83%A9%E3%83%BC%E3%82%92%E3%83%93%E3%83%A5%E3%83%BC%E3%81%A7%E8%A1%A8%E7%A4%BA%E3%81%99%E3%82%8B


## 7.4.2 flash について
Action Controller の概要 の 5.2 Flash を参考にする
https://railsguides.jp/action_controller_overview.html#flash


## 7.5.1 本番環境でのSSL 7.5.2 本番環境用のWebサーバー について
ローカル環境で実施のため割愛する

SSLについては
Rails セキュリティガイド 2.3 セッションハイジャック を参考にする
https://railsguides.jp/security.html#%E3%82%BB%E3%83%83%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%8F%E3%82%A4%E3%82%B8%E3%83%A3%E3%83%83%E3%82%AF

本番環境のWebサーバーについては割愛


--


# 8章でのまとめ
※ 8章は難度が高い

## 8.1 セッション 8.1.1 Sessionsコントローラ について
Rails チュートリアルより詳細は、Rails セキュリティガイド の 2 セッション を参考にする
https://railsguides.jp/security.html#%E3%82%BB%E3%83%83%E3%82%B7%E3%83%A7%E3%83%B3

Action Controller の概要 の 5 セッション を参考にする
https://railsguides.jp/action_controller_overview.html#%E3%82%BB%E3%83%83%E3%82%B7%E3%83%A7%E3%83%B3


## authenticate メソッド について
authenticate メソッドは認証に失敗したときに false を返す


## flash.now について
Action Controller の概要 の 5.2.1 flash.now を参考にする
https://railsguides.jp/action_controller_overview.html#flash


## 「||=」について
Rails チュートリアル の コラム 8.1. 「||=」とは何か？ を参考にする


## 8.2.4 レイアウトの変更をテストする
Rails チュートリアル よりも詳細については、
Rails テスティングガイド の 4.6 テンプレートとレイアウトをテストする を参考にする
https://railsguides.jp/testing.html#%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%81%A8%E3%83%AC%E3%82%A4%E3%82%A2%E3%82%A6%E3%83%88%E3%82%92%E3%83%86%E3%82%B9%E3%83%88%E3%81%99%E3%82%8B

※ Rails チュートリアル 内には、test用データについても記載があるので参考にする


## ヘルパーのテスト について
8.2.5 ユーザー登録時にログイン を参考にする
より詳細は Rails ガイド
Rails テスティングガイド の 11 ヘルパーをテストする を参考にする
https://railsguides.jp/testing.html#%E3%83%98%E3%83%AB%E3%83%91%E3%83%BC%E3%82%92%E3%83%86%E3%82%B9%E3%83%88%E3%81%99%E3%82%8B


--


# 9章でのまとめ
## 9.1.1 記憶トークンと暗号化 について
Rails チュートリアル を参考にする
より詳細については、Rails セキュリティガイド を参考にする
https://railsguides.jp/security.html


## cookiesメソッド について
cookiesメソッドは、sessionのときと同様にハッシュとして扱える
個別のcookiesは、ひとつのvalue (値) と、オプションのexpires (有効期限) からできている
有効期限は省略可能


## 9.1.4 ２つの目立たないバグ について
複数タブの問題、複数ブラウザの問題 を取り扱っているので
Rails チュートリアル 9章の 9.1.4 ２つの目立たないバグ を参考にする
https://railstutorial.jp/chapters/advanced_login?version=5.0#sec-two_subtle_bugs


## assigns メソッドについて
assigns メソッドについては、
Rails チュートリアル内の以下の演習を参考にする
https://railstutorial.jp/chapters/advanced_login?version=5.0#sec-exercises_testing_the_remember_me_box

Railsガイド Rails テスティングガイド 内の 4.3 4つのハッシュ を参考にする
https://railsguides.jp/testing.html#4%E3%81%A4%E3%81%AE%E3%83%8F%E3%83%83%E3%82%B7%E3%83%A5


--


# 10章でのまとめ
## db/seeds.rb rails db:seed について
Active Record マイグレーション の 8 マイグレーションとシードデータ を参考にする
https://railsguides.jp/active_record_migrations.html#%E3%83%9E%E3%82%A4%E3%82%B0%E3%83%AC%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%A8%E3%82%B7%E3%83%BC%E3%83%89%E3%83%87%E3%83%BC%E3%82%BF


## rails db:migrate:reset について
Active Record マイグレーション の 4.3 データベースをリセットする を参考にする
https://railsguides.jp/active_record_migrations.html#%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9%E3%82%92%E3%83%AA%E3%82%BB%E3%83%83%E3%83%88%E3%81%99%E3%82%8B


--


# 11章でのまとめ
## Mailer（メイラー） について
Mailer については、Rails ガイドの Action Mailer の基礎 を参考にする
https://railsguides.jp/action_mailer_basics.html


## 11.2.2 送信メールのプレビュー について
チュートリアルより詳細については、
Rails ガイド内に詳細が見当たらなかったので、以下のサイトを参考にする
http://y-yagi.tumblr.com/post/88746017105/rails%E3%81%AEaction-mailer-previews%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6


## CGI.escape について
Ruby のメソッドのため、以下を参考にする
https://docs.ruby-lang.org/ja/search/query:CGI.escape/


## development 環境等でアカウント有効化のURLを試すとき
サインインすると rails s のサーバーログに出力される
※ Rails チュートリアルの リスト 11.25: サーバーログに表示されたアカウント有効化メールの例 を参考にする


--


# 12章でのまとめ
## --no-test-framework について
--no-test-framework: rails generate でテストを生成されないようにするオプション


## フォームでシンボルを使う理由（オブジェクトを使う場合との違い） について
以下のサイトを参考にする
https://ja.stackoverflow.com/questions/18099/rails%E3%81%AEform-for%E3%81%AB%E3%82%B7%E3%83%B3%E3%83%9C%E3%83%AB%E3%82%92%E4%B8%8E%E3%81%88%E3%82%8B%E3%81%A8%E3%81%8D%E3%81%AF%E3%81%A9%E3%81%AE%E3%82%88%E3%81%86%E3%81%AA%E3%81%A8%E3%81%8D%E3%81%8B


## f.hidden_field と hidden_field_tag の違いについて
Rails チュートリアル以外も調べたが、分からなかったので、Rails チュートリアルを参考にする
* 抜粋
前者 : hidden_field_tag :email, @user.email
後者 : f.hidden_field :email, @user.email
前者（hidden_field_tag） ではメールアドレスがparams[:email]に保存される
後者（f.hidden_field） ではparams[:user][:email] に保存される

※ 違いについては書いていないが、以下も載せておく
http://ruby-rails.hatenadiary.com/entry/20150113/1421149061#view-helpers-hidden


--


# 13章でのまとめ
## インデックス について
Active Record マイグレーション を参考にする
https://railsguides.jp/active_record_migrations.html
※ 複合インデックスの指定については Rails チュートリアル（13章）と以下を参考にする
https://openbook4.me/sections/621
http://qiita.com/ryu-taka/items/c9045a48497c062f5595


## 13.1.3 User/Micropostの関連付け について
Rails チュートリアルの内容と合わせて
Rails ガイドの Active Record の関連付け (アソシエーション) を参考にする
https://railsguides.jp/association_basics.html


## default_scope（スコープ） について
Rails ガイド Active Record クエリインターフェイス の 14 スコープ を参考にする
https://railsguides.jp/active_record_querying.html#%E3%82%B9%E3%82%B3%E3%83%BC%E3%83%97


## dependent: :destroy について
Rails ガイド Active Record の関連付け (アソシエーション) の 4.1.2.4 :dependent を参考にする
https://railsguides.jp/association_basics.html#belongs-to%E3%81%AE%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3-dependent


## take メソッド について
Rails ガイド Active Record クエリインターフェイス の 1.1.2 take を参考にする
https://railsguides.jp/active_record_querying.html#take


## リスト 13.26: マイクロポスト用のCSS (本章で利用するCSSのすべて) について
途中で間違えたのか、崩れたので マイクロポストの li ブロックに margin-bottom: 30px; を追加してみた


## carrierwave gem, mini_magick gem, fog gem について
以下を参考にする
* carrierwave
http://qiita.com/unchiman-tojour-haraita/items/cc447237e23bf10d159e
http://morizyun.github.io/blog/carrierwave-image-uploader-rails/
* mini_magick
http://keruuweb.com/rails-minimagick%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9/
* fog (あまり参考になりそうなのがなかった)
http://qiita.com/ryo-ichikawa/items/a30dc626cba1ec909d57


## validates, validate について
validates について
Active Record バリデーション を参考にする
https://railsguides.jp/active_record_validations.html

validate については
Active Record バリデーション 6.2 カスタムメソッド を参考にする
https://railsguides.jp/active_record_validations.html#%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%A0%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89


## 13.4.4 本番環境での画像アップロード について
heroku 利用していなかったので、割愛


--


# 14章でのまとめ
## 関連付け について
何度もでているが、Active Record の関連付け を参考にする
https://railsguides.jp/association_basics.html

* class_name オプション について
https://railsguides.jp/association_basics.html#belongs-to%E3%81%AE%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3-class-name
* foreign_key オプション について
https://railsguides.jp/association_basics.html#belongs-to%E3%81%AE%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3-foreign-key


## :through 関連付けについて
以下を参考にする
* 2.4 has_many :through関連付け
https://railsguides.jp/association_basics.html#has-many-through%E9%96%A2%E9%80%A3%E4%BB%98%E3%81%91
* 2.5 has_one :through関連付け
https://railsguides.jp/association_basics.html#has-one-through%E9%96%A2%E9%80%A3%E4%BB%98%E3%81%91


## ルーティングにアクションを追加する（member ルーティングを追加する）について
2.10 RESTfulなアクションをさらに追加する 内の 2.10.1 メンバールーティングを追加する を参考にする
https://railsguides.jp/routing.html#restful%E3%81%AA%E3%82%A2%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%92%E3%81%95%E3%82%89%E3%81%AB%E8%BF%BD%E5%8A%A0%E3%81%99%E3%82%8B

※ collection メソッドとの違いは、Rails チュートリアル 14.2.2 統計と [Follow] フォーム 又は、
上記のURLを参考にする


## ajax について
ajax については、Rails で JavaScript を使用する を参考にする
https://railsguides.jp/working_with_javascript_in_rails.html


## 読み物ガイド
日本語の読み物として以下が紹介されていた
* Ruby on Railsを仕事にしていくための第一歩
http://morizyun.github.io/blog/ruby-rails-non-beginner-guide-book/
