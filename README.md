# lemp-docker
dockerised lemp for php application

## Getting Starting
1. Create a new `.env` file from `env.example`

2. Start up the docker composer and pull the requirement
```
docker copmose up -d --build
```

3. SSH into the docker php container
```
docker compose exec php_app bash
```

4. Create the drupal cms application
```
composer create drupal/cms cms
```

5. Copy the project folder into the html folder
```
cp -r cms/* ./ && rm -r cms
```
6. Exit the php containter

7. Create a settings.php file in `web/sites/default` folder . Ensure that the file is writeable