# Gitlab CI image

## Inside

- PHP-FPM 7.1 (php:7.1-fpm-jessie)
- Nginx
- Node JS 10
- Composer
- Chrome-headless

## From

php:7.1-fpm-jessie

## Usage

- Config server in nginx, ex:
`cp /nginx/server.conf /etc/nginx/sites-enabled/default`
then `service nginx start`

- Increase memory limit:
`cp php7-fpm/memory-limit-php.ini /usr/local/etc/php/conf.d/memory-limit-php.ini`

- You have availabe `npm i` and `composer install`

- php app/console cache:clear

Start chrome headless host

- /usr/bin/google-chrome --disable-gpu --headless --remote-debugging-address=0.0.0.0 --remote-debugging-port=9222 --no-sandbox --window-size="1920,1080" --disable-dev-shm-usage --no-startup-window --no-first-run --no-pings &

> Enjoy
