# docker-laravel-postgis-geoserver
after clone 
sudo chown -R 33:33 .
sudo chmod -R 777 .
docker volume create postgres-data
docker volume create redis-data
docker volume create geoserver-data
Membuat alias untuk docker menjalankan script php
alias dr="docker exec -it laravel-gis_php_1"
docker-compose build
docker-compose up -d
dr composer update
dr composer install
dr php artisan migrate
Jika ada depedensi yg di perlukan bisa melakukan dr kembali 
