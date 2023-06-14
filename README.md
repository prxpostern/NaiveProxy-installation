- **Install go**
```
apt -y update && apt -y install wget socat && wget -c https://go.dev/dl/go1.20.5.linux-amd64.tar.gz -O - | tar -xz -C /usr/local && echo 'export PATH=$PATH:/usr/local/go/bin' > /etc/profile && source /etc/profile && go version 
```
- **Compile and install caddy**
```
go install github.com/caddyserver/xcaddy/cmd/xcaddy@latest && ~/go/bin/xcaddy build --output caddy --with github.com/mholt/caddy-l4 --with github.com/mastercactapus/caddy2-proxyprotocol --with github.com/caddyserver/forwardproxy@caddy2=github.com/klzgrad/forwardproxy@naive && setcap cap_net_bind_service=+ep ./caddy && chmod +x caddy && mv caddy /usr/bin/
```

- **Download configuration file**

 
