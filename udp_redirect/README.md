# udp_redirect

`udp_redirect` redirects UDP packets coming in to a local port to a specified address/port combination.

* http://brokestream.com/udp_redirect.html

## Example

Redirect `10.0.0.2:53` to `10.1.0.3:5353`

```sh
docker run -d \
    --name=udp_redirect \
    -p 10.0.0.2:53:3000/udp \
    -e CADDR=10.1.0.3 \
    -e CPORT=5353 \
    nfam/udp_redirect
```
