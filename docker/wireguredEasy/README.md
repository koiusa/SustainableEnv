## WireGuard is now easier to use with a GUI

- Please see the link below for more information

https://github.com/wg-easy/wg-easy

- For more information on Wire Guard please see the link below

https://www.wireguard.com

## Generate Password Hash

- Password hash generation required Please enter the results output by the script below into the ".env" file.

https://blog.programster.org/deploy-wireguard-server-with-web-ui-through-docker 

```sh
$ sudo apt install -y php
```

```
$ php
```

```sh
<?php

$randomPassword = base64_encode(random_bytes(32));
print "Random password is: " . PHP_EOL;
print $randomPassword . PHP_EOL . PHP_EOL;

$hash = password_hash($randomPassword, PASSWORD_BCRYPT);
print "Bcrypt hash is: "  . PHP_EOL;
print $hash . PHP_EOL;
```

```sh
$ cat .env
WG_EASY_PASSWORD_HASH='yourWgEasyPasswordHash'
WG_EASY_HOST=yourWANaddress
```

## Security measures

- We recommend changing the port number used from a security perspective.

```sh
 ports:
      - "51820:51820/udp"
      - "51821:51821/tcp"
```

