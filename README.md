# README

## Rails の雛形生成

・Rails を API モードで生成
rails new blog --api

・モデルとコントローラー生成
$ rails g model post title:string content:string
$ rails g controller posts
$ rails db:create
$ rake db:migrate

・ルーティング生成（名前空間あり）
**コントローラーのフォルダ階層を変える必要あり。**

Rails.application.routes.draw do
namespace 'api' do
namespace 'v1' do
resources :posts
end
end
end

・基本アクションをコントローラーで生成
**結果は JSON で返す**

・Advanced Rest client で動作確認
**記事の表示・削除など全てのアクションを実行できたら OK**
