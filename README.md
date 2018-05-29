Clone this repo, then run these commands:

docker-compose build

docker-compose run web rails new . --force --database=postgresql --webpack=vue

docker-compose build

update config/database.yml, making sure it matches file in this repo (because it got overwritten when we did "rails new ...")

docker-compose up -d

docker-compose exec web rails db:create db:migrate

The app should be running at:  http://localhost:3000

