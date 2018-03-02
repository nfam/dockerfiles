# freegeoip
From https://github.com/fiorix/freegeoip

Run the API in a container
~~~
docker create \
    --name=freegeoip \
    -p 8080:8080 \
    -v ~/freegeoip-data:/tmp \
    nfam/freegeoip
~~~