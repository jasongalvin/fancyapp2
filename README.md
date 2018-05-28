Clone this repo, then run these commands:
docker-compose build
docker-compose run web rails new . --force --database=postgresql --webpack=vue
docker-compose build
docker-compose exec web rails db:create db:migrate
docker-compose up

The app should be running at:  http://localhost:3000

