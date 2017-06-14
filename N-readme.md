if drupal is inside subdirectory use "-r ./{DIRECTORY NAME}":
web/{drupal-folders-and-files}

docker-compose exec --user 82 php drush -r ./web cc all
