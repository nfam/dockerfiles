# aria2
The original aria2 without any modification.

## Usage

```sh
docker run -d \
    --name=aria2 \
    --restart=always \
    -p 6800:6800 \
    -v ~/downloads:/downloads \
    nfam/aria2 \
    --dir=/downloads \
    --enable-rpc=true \
    --max-connection-per-server=1 \
    --rpc-listen-all=true \
    --rpc-secret={{secret}}
```
