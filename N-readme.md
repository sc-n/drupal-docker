if drupal is inside subdirectory use "-r ./{DIRECTORY NAME}":
web/{drupal-folders-and-files}

docker-compose exec --user 82 php drush -r ./web cc all


"web" is site folder.
There should be index.php

Bash aliases for Docker compose:
alias d-drush="docker-compose exec --user 82 php drush --root=./web"
alias d-composer="docker-compose exec --user 82 php composer"
