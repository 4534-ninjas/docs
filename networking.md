# On the Pi

The goal of this setup is so that we can guarnatee that we just plug
in power for a demo, and things "just work" without any manual
intervention.

The Pi has two network interfaces:

1. One not-always-present wired connection for its connection to the
   outside world (for downloading packages and whatever), configured
   with a DHCP client.

2. It also has a wireless interface in AP mode with a DHCP server for
   the WiFlys to connect to.

SSHd accepts incoming connections from either interface.

## To configure the wireless thing:

TODO: Directions here.


# On the WiFlys

TODO: Dump init sequence here.


# On an optional laptop

Set it up as a router with a DHCP server advertising leases on a wired
interface connected to the Pi.

## Directions with Ubuntu

1. ["Share the network connection"](http://askubuntu.com/questions/359856/share-wireless-internet-connection-through-ethernet)

2. Find the Pi's IP address by checking the DHCP lease:

   ```
   $ cat /var/lib/misc/dnsmasq.leases
   1445310314 b8:27:eb:78:95:4a 10.42.0.14 raspberrypi 01:b8:27:eb:78:95:4a
                                ^^^^^^^^^^
   ```

Note also that Ubuntu has some DNS magic that will resolve
*hostname*.local, so
```
$ ssh pi@raspberrypi.local
```
"*just works*<sup>TM</sup>"
