# Local Docker Compose support for Board18

This is a fork of the official [Board18
repo](https://github.com/richpri/board18v2) that adds support for running the
site locally under [docker-compose](https://docs.docker.com/compose/). This
might be an easier way to run the site for local game box development if you
don't want to learn how to run Apache, PHP and MySQL on your local environment.

I will try to keep this branch periodically up to date with the official branch.

## Usage

Checkout this repository and from the root folder run:

``` shell
docker-compose up
```

This will spin up the site and it should be available at http://localhost:8080

Just like normal Board18, the first account you register will be an admin on
your local site. Email might work depending on your current internet access and
how agreesive your personal email provider is about spamming emails from
localhost services.

For more information on the different features of docker-compose please [read
their documentation](https://docs.docker.com/compose/).

The database is saved in a docker volume named `b18`. You can remove this volume
with normal docker commands or by running `docker-compose down --volumes` if you
want to clear it out and start again.
