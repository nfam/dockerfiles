# redir

`redir` redirects tcp connections coming in to a local port to a specified address/port combination.

* http://sammy.net/~sammy/hacks/

## Example

Redirect `10.0.0.2:80` to `10.1.0.3:8080`

```sh
docker run -d \
    --name=redir \
    -p 10.0.0.2:80:3000 \
    -e CADDR=10.1.0.3 \
    -e CPORT=8080 \
    nfam/redir
```
