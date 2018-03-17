# dnsmasq

It's a [dnsmasq][dnsmasq] Docker image.

## Usage

```sh
docker run -d \
    --name=dnsmasq \
    --restart=always \
    --cap-add=NET_ADMIN \
    -p 53:53/tcp \
    -p 53:53/udp \
    nfam/dnsmasq
```

[dnsmasq]: http://www.thekelleys.org.uk/dnsmasq/doc.html