# avahi

It's a [avahi][avahi] Docker image.

## Usage

```sh
docker run -d \
    --name=avahi \
    --restart=always \
    --net=host \
    nfam/avahi
```

[avahi]: https://www.avahi.org