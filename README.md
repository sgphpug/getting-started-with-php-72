# Getting Started with PHP 7.2

## Pre-Requisite

Download and install Docker ([https://www.docker.com/community-edition#/download](https://www.docker.com/community-edition#/download)).

## Running the examples

### Interactive Shell

```
docker build --rm -t phpgettingstarted/cli -f Dockerfile.cli .
docker run --rm -it --name my-php-cli phpgettingstarted/cli
```

**Pro Tip:** Type `exit` to get out of the CLI. Or just press `ctrl` + `d`.

### Running with Apache

```
docker build -t phpgettingstarted/php-apache -f Dockerfile.apache .
docker run --rm -d --name my-php-apache -p 8080:80 -v "$PWD/src":/var/www/html phpgettingstarted/php-apache
```

Edit the `index.php` file in the `/src` folder to see the changes.

To stop the container:

```
docker stop my-php-apache
```

## Sample Codes

- [https://kinsta.com/blog/php-7-2/](https://kinsta.com/blog/php-7-2/)
- [http://devpark.pl/what-changed-in-php-7-2/](http://devpark.pl/what-changed-in-php-7-2/)
