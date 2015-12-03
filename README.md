# iptables
Basic IPTABLES Configuration

Both files are of exact content.
Any changes to be tested in rules.temp.fw prior to saving.

Deploy by the following <br>
iptables-restore < /path/to/iptables/rules.temp.fw

If all is well save to persist and set up persistence... If not reboot!<br>
iptables-save > /path/to/iptables/rules.persist.fw

To make sure iptables are restored upon reboot
( 1 ) mv /path/to/iptables/iptables /etc/network/if-pre-up.d/iptables <br>
( 2 ) chmod +x /etc/network/if-pre-up.d/iptables






