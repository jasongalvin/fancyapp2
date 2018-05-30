My notes/steps for getting the app running from this excellent tutorial:  https://hovancik.net/blog/2017/07/02/creating-new-rails-and-vue-js-app-with-docker/


Clone this repo, then run these commands:

docker-compose run web rails new . --force --database=postgresql --webpack=vue

docker-compose build

update config/database.yml, making sure it matches file in this repo (because it got overwritten when we did "rails new ...")

docker-compose up -d

docker-compose exec web rails db:create db:migrate

The app should be running at:  http://localhost:3000

