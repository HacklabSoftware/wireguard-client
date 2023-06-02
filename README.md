# Wireguard


Client setup - 

### Ubuntu
```
sudo apt install wireguard
sudo apt install resolvconf

sudo cp <client_>.conf /etc/wireguard/wg0.conf
```

To start the wireguard tunnel
```
sudo wg-quick up wg0
```

To stop the wireguard tunnel
```
sudo wg-quick down wg0 
```

#### To make permanent setup
Add the WireGuard service to systemd:
```
  sudo systemctl enable wg-quick@wg0.service
  sudo systemctl daemon-reload
```
Start the new service immediately:

```
sudo systemctl start wg-quick@wg0
```
Reboot your computer system to verify the automatic connection on startup works as expected.



### Others
https://www.wireguard.com/install/
