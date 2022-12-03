# vpn-bypass-for-streaming


quick an dirty fix to bypass vpn for Amazon Prime and Netflix to integrate in GL-INET Routers via Policy Routing and Crontab ;) using my generated hosts lists from ... [LouCipher/vpn-bypass-for-streaming](https://github.com/Lou-Cipher/vpn-bypass-for-streaming)
 



##### Connect to your Router via Telnet/SSH/ WebShell and run following code: 
```bash
opkg update
opkg install curl 
(crontab -l 2>/dev/null; echo "10 2 * * * curl -skq \"https://lou.h4ck.me/vpn_bypass.txt\" -o /etc/route_policy/domain_name/bypass_vpn/manual-list.conf  ; reboot") | crontab -
```

##### no time to wait until cron runs at 02 at night? ... fire up the cmd manually: 
```bash
curl -skq "https://lou.h4ck.me/vpn_bypass.txt" -o /etc/route_policy/domain_name/bypass_vpn/manual-list.conf  ; reboot
```


