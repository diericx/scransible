Wireguard
=========

Sets up a basic wireguard VPN and places a client config in /etc/wireguard dir.

This is a direct translation of this script:
https://github.com/angristan/wireguard-install/blob/master/wireguard-install.sh

Role Variables
--------------

| Variable          | Default         | Comments                         |
|-------------------|-----------------|----------------------------------|
| wg_interface_name | wg0             | name of your wireguard interface |
| server_wg_ipv4    | 10.66.66.1      | Wireguard server internal IP V4  |
| server_wg_ipv6    | fd42:42:42::1   | Wireguard server internal IP V6  |
| client_ipv4       | 10.66.66.2      | internal ip for client (v4)      |
| client_ipv6       | fd42:42:42::2   | internal ip for client (v6)      |
| client_dns1       | 176.103.130.130 | dns 1 for client                 |
| client_dns2       | 176.103.130.131 | dns 2 for client                 |
| client_name       | clien1          | name for your client             |

License
-------

BSD

Dev
------------------

`molecule converge -- --skip-tags=skip_docker`
