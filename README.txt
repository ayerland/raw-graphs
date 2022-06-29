## install heroku
https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli

heroku login

heroku container:login

heroku create --app <app-name>

heroku stack:set container --app <app-name>

heroku container:push web --app <app-name>

heroku container:release web --app <app-name>

heroku open --app <app-name>


## if want to do clean up
docker image ls -aq
docker image rm -f e406301a1b5e


## Or straight from docker cli

heroku auth:token

docker login --username=<USER> --password=<TOKEN> registry.heroku.com

docker build -t registry.heroku.com/<app-name>/web .

docker push registry.heroku.com/<app-name>/web

heroku container:release web --app <app-name>

## SAMPLE
https://raw-graphs.herokuapp.com

