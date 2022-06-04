# rails7_template
rails7,MySQL 


1. git clone
2. docker-compose run web rails new . --force --no-deps --database=mysql --css sass
3. docker-compose web bundle install
4. config > database.yml の編集(DB接続設定) https://qiita.com/croquette0212/items/7b99d9339fd773ddf20b
5. docker-compose run web rails db:create
6. Gemfile に追記：gem "cssbundling-rails"の後らへんに
   gem 'importmap-rails'
   gem 'propshaft'
7. docker-compose web bundle install
8. docker-compose build --no-cache
9. docker-compose exec web bin/rails importmap:install
10. npm install bootstrap
11. npm i bootstrap-icons
12. docker-compose run web rails css:install:bootstrap
