# aria2
The original aria2 without any modification.

## Build container
~~~
docker create \
    --name=aria2 \
    -p 6800:6800 \
    -v ~/downloads:/downloads \
    nfam/aria2 \
    --dir=/downloads \
    --enable-rpc=true \
    --max-connection-per-server=1 \
    --rpc-listen-all=true \
    --rpc-secret={{secret}}
~~~
