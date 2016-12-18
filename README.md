## Composer
Perform composer install

## Composer
Start container

    docker-compose up -d
    
## Vendor on container
Connect to container and Move vendor to no-share folder on (performence issue)
    
    docker exec -ti symfonybaseproject_php_1 bash
    mkdir -p /dev/shm/symfony
    cp -R /var/www/symfony/vendor /dev/shm/symfony/vendmkdiror

Change location path on autoload.php

    $loader = require '/dev/shm/symfony/vendor/autoload.php';
