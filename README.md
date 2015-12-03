# iptables
Basic IPTABLES Configuration

Both files are of exact content.
Any changes to be tested in rules.temp.fw prior to saving.

- Deploy by the following
iptables-restore < /path/to/iptables/rules.temp.fw

If all is well save to persist and set up persistence... If not reboot!
iptables-save > /path/to/iptables/rules.persist.fw

To make sure iptables are restored upon reboot
(1) nano /etc/network/if-pre-up.d/iptables
(2) #!/bin/sh
    /sbin/iptables-restore < /path/to/iptables/rules.persist.fw
(3) chmod +x /etc/network/if-pre-up.d/iptables


