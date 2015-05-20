# approx - caching proxy server for Debian archive files

Point your debian or ubuntu installations to approx by modifying sources.list:

    deb http://approx:9999/debian stable main
    # or
    deb http://approx:9999/ubuntu trusty main

Or place a reverse proxy in front of approx.

## Run using the default configuration

    docker run -p 9999:9999 approx:latest

## Persist the cache

    docker run -p 9999:9999 -v /path/to/approx:/var/cache/approx approx:latest

## Use a custom approx.conf

    docker run -p 9999:9999 -v /path/to/approx.conf:/etc/approx/approx.conf approx:latest
