# iptables
Basic IPTABLES Configuration

Both files are of exact content.  
Any changes to be tested in rules.temp.fw prior to saving.  
Make sure all paths are changed according to your clone location.  

Deploy by the following  
    iptables-restore < /path/to/iptables/rules.temp.fw  

If all is well save to persist and set up persistence... If not reboot!  
    iptables-save > /path/to/iptables/rules.persist.fw  

To make sure iptables are restored upon reboot  
    mv /path/to/iptables/iptables /etc/network/if-pre-up.d/iptables  
    chmod +x /etc/network/if-pre-up.d/iptables
