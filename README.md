# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Output:
# ping:
```
C:\Users\Priyadharshini>ping google.com

Pinging google.com [2404:6800:4007:83f::200e] with 32 bytes of data:
Reply from 2404:6800:4007:83f::200e: time=4ms
Reply from 2404:6800:4007:83f::200e: time=8ms
Reply from 2404:6800:4007:83f::200e: time=31ms
Reply from 2404:6800:4007:83f::200e: time=16ms

Ping statistics for 2404:6800:4007:83f::200e:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 4ms, Maximum = 31ms, Average = 14ms
```
# ipconfig:
```
C:\Users\Priyadharshini>ipconfig

Windows IP Configuration


Ethernet adapter Ethernet 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : 2403:8600:c090:51:4899:aae8:e8a6:209e
   Temporary IPv6 Address. . . . . . : 2403:8600:c090:51:fc8b:536:11fa:6b69
   Link-local IPv6 Address . . . . . : fe80::18bc:df45:8a60:ef6e%2
   Autoconfiguration IPv4 Address. . : 169.254.251.0
   Subnet Mask . . . . . . . . . . . : 255.255.0.0
   Default Gateway . . . . . . . . . : fe80::eedd:24ff:fe3d:ced5%2
```
# tracert:
```
C:\Users\Priyadharshini>tracert google.com

Tracing route to google.com [2404:6800:4007:83f::200e]
over a maximum of 30 hops:

  1     2 ms     4 ms     3 ms  2403:8600:c090:51::1
  2     *        *        *     Request timed out.
  3     *        *        *     Request timed out.
  4     6 ms     4 ms     4 ms  pnmaaa-at-in-x0e.1e100.net [2404:6800:4007:83f::200e]

Trace complete.
```
# netstat:
```
C:\Users\Priyadharshini>netstat -an

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    0.0.0.0:135            0.0.0.0:0              LISTENING
  TCP    0.0.0.0:445            0.0.0.0:0              LISTENING
  TCP    0.0.0.0:2869           0.0.0.0:0              LISTENING
  TCP    0.0.0.0:5040           0.0.0.0:0              LISTENING
  TCP    0.0.0.0:6646           0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49664          0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49665          0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49666          0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49667          0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49668          0.0.0.0:0              LISTENING
  TCP    0.0.0.0:49673          0.0.0.0:0              LISTENING
  TCP    127.0.0.1:2015         0.0.0.0:0              LISTENING
  TCP    169.254.251.0:139      0.0.0.0:0              LISTENING
  TCP    [::]:135               [::]:0                 LISTENING
  TCP    [::]:445               [::]:0                 LISTENING
  TCP    [::]:2869              [::]:0                 LISTENING
  TCP    [::]:49664             [::]:0                 LISTENING
  TCP    [::]:49665             [::]:0                 LISTENING
  TCP    [::]:49666             [::]:0                 LISTENING
  TCP    [::]:49667             [::]:0                 LISTENING
  TCP    [::]:49668             [::]:0                 LISTENING
  TCP    [::]:49673             [::]:0                 LISTENING
  TCP    [::1]:49669            [::]:0                 LISTENING
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:49739  [2603:1040:a06:6::]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:49893  [2600:140f:5e00:83::17d3:8e65]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:51212  [2603:1047:1:98::80]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:52862  [2a04:4e42:400::347]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:53430  [2403:8600:80c0:4a::e62:100a]:443  CLOSE_WAIT
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:54481  [64:ff9b::142a:4883]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:54736  [64:ff9b::142a:4883]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:54830  [2600:1901:1:7c5::]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:54831  [2600:140f:6::17c7:4553]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:55054  [64:ff9b::8c52:7115]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:56822  [64:ff9b::2268:8000]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:58430  [64:ff9b::b9c7:6f85]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:60718  [64:ff9b::8c52:701a]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:60751  [2a06:98c1:3108::ac40:94eb]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:60899  [64:ff9b::17dc:e840]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:61345  [2606:50c0:8003::154]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:61910  [2404:6800:4003:c06::bc]:5228  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:64423  [2603:1063:2001:193c::365:ff1]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:64424  [2603:1063:2001:1902::365:ff1]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:64452  [2600:140f:6::17c7:4568]:443  ESTABLISHED
  TCP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:65238  [2600:140f:5e00:14::17d3:3c24]:443  CLOSE_WAIT
  UDP    0.0.0.0:123            *:*
  UDP    0.0.0.0:5050           *:*
  UDP    0.0.0.0:5353           *:*
  UDP    0.0.0.0:5353           *:*
  UDP    0.0.0.0:5353           *:*
  UDP    0.0.0.0:5353           *:*
  UDP    0.0.0.0:5353           *:*
  UDP    0.0.0.0:5355           *:*
  UDP    0.0.0.0:6646           *:*
  UDP    0.0.0.0:51154          23.211.60.36:443
  UDP    0.0.0.0:54395          14.98.16.10:443
  UDP    0.0.0.0:55499          0.0.0.94:443
  UDP    0.0.0.0:56388          *:*
  UDP    0.0.0.0:57330          0.0.100.100:443
  UDP    0.0.0.0:58183          0.0.100.100:443
  UDP    0.0.0.0:61329          23.211.60.20:443
  UDP    0.0.0.0:65317          *:*
  UDP    127.0.0.1:1900         *:*
  UDP    127.0.0.1:49664        127.0.0.1:49664
  UDP    127.0.0.1:58340        *:*
  UDP    169.254.251.0:137      *:*
  UDP    169.254.251.0:138      *:*
  UDP    169.254.251.0:1900     *:*
  UDP    169.254.251.0:2177     *:*
  UDP    169.254.251.0:58339    *:*
  UDP    172.16.186.45:57111    172.16.186.144:53
  UDP    [::]:123               *:*
  UDP    [::]:5353              *:*
  UDP    [::]:5353              *:*
  UDP    [::]:5353              *:*
  UDP    [::]:5355              *:*
  UDP    [::]:51154             [2600:140f:5e00:14::17d3:3c24]:443
  UDP    [::]:54395             [2403:8600:80c0:4a::e62:100a]:443
  UDP    [::]:55499             [2404:6800:4000:1010::5e]:443
  UDP    [::]:56388             [2001:4860:482b:7700::]:443
  UDP    [::]:57330             [2001:4860:4860::6464]:443
  UDP    [::]:58183             [2001:4860:4860::6464]:443
  UDP    [::]:61329             [2600:140f:5e00:14::17d3:3c14]:443
  UDP    [::]:65317             *:*
  UDP    [::1]:1900             *:*
  UDP    [::1]:58338            *:*
  UDP    [2403:8600:c090:51:4899:aae8:e8a6:209e]:2177  *:*
  UDP    [2403:8600:c090:51:fc8b:536:11fa:6b69]:2177  *:*
  UDP    [fe80::18bc:df45:8a60:ef6e%2]:1900  *:*
  UDP    [fe80::18bc:df45:8a60:ef6e%2]:2177  *:*
  UDP    [fe80::18bc:df45:8a60:ef6e%2]:58337  *:*
```
# nslookup:
```
C:\Users\Priyadharshini>nslookup google.com
Server:  dns64.dns.google
Address:  2001:4860:4860::6464

Non-authoritative answer:
Name:    google.com
Addresses:  2404:6800:4007:83f::200e
          172.217.24.206
```
# hostname:
```
C:\Users\Priyadharshini>hostname
piruthivi
```
# arp -a:
```
C:\Users\Priyadharshini>arp -a                                                                                                                                          Interface: 169.254.251.0 --- 0x2                                                      Internet Address      Physical Address      Type                                    169.254.23.250        a8-59-5f-3f-d6-0d     dynamic                                 169.254.164.247       14-ac-60-fa-07-37     dynamic                                 169.254.172.74        50-bb-b5-47-09-06     dynamic                                 169.254.172.205       68-34-21-81-83-0f     dynamic                                 169.254.233.99        68-34-21-81-86-3e     dynamic                                 169.254.236.110       68-34-21-94-13-94     dynamic                                 169.254.239.111       e0-2e-0b-30-1a-c9     dynamic                                 169.254.255.255       ff-ff-ff-ff-ff-ff     static                                  224.0.0.2             01-00-5e-00-00-02     static                                  224.0.0.22            01-00-5e-00-00-16     static                                  224.0.0.251           01-00-5e-00-00-fb     static                                  224.0.0.252           01-00-5e-00-00-fc     static                                  239.255.102.18        01-00-5e-7f-66-12     static                                  239.255.255.250       01-00-5e-7f-ff-fa     static                                  255.255.255.255       ff-ff-ff-ff-ff-ff     static                      
```
# route print:
```
C:\Users\Priyadharshini>route print
===========================================================================
Interface List
 16...00 ff ce a2 ee 58 ......ExpressVPN TAP Adapter
 14...b0 60 88 53 fb 48 ......Microsoft Wi-Fi Direct Virtual Adapter
 11...b2 60 88 53 fb 47 ......Microsoft Wi-Fi Direct Virtual Adapter #2
  2...b0 60 88 53 fb 47 ......Intel(R) Wi-Fi 6 AX201 160MHz
  1...........................Software Loopback Interface 1
===========================================================================

IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    331
        127.0.0.1  255.255.255.255         On-link         127.0.0.1    331
  127.255.255.255  255.255.255.255         On-link         127.0.0.1    331
      169.254.0.0      255.255.0.0         On-link     169.254.251.0    301
    169.254.251.0  255.255.255.255         On-link     169.254.251.0    301
  169.254.255.255  255.255.255.255         On-link     169.254.251.0    301
        224.0.0.0        240.0.0.0         On-link         127.0.0.1    331
        224.0.0.0        240.0.0.0         On-link     169.254.251.0    301
  255.255.255.255  255.255.255.255         On-link         127.0.0.1    331
  255.255.255.255  255.255.255.255         On-link     169.254.251.0    301
===========================================================================
Persistent Routes:
  None

IPv6 Route Table
===========================================================================
Active Routes:
 If Metric Network Destination      Gateway
  2    301 ::/0                     fe80::eedd:24ff:fe3d:ced5
  1    331 ::1/128                  On-link
  2    301 2403:8600:c090:51::/64   On-link
  2    301 2403:8600:c090:51:4899:aae8:e8a6:209e/128
                                    On-link
  2    301 2403:8600:c090:51:fc8b:536:11fa:6b69/128
                                    On-link
  2    301 fe80::/64                On-link
  2    301 fe80::18bc:df45:8a60:ef6e/128
                                    On-link
  1    331 ff00::/8                 On-link
  2    301 ff00::/8                 On-link
===========================================================================
Persistent Routes:
  None
```
# getmac:
```

C:\Users\Priyadharshini>getmac

Physical Address    Transport Name
=================== ==========================================================
00-FF-CE-A2-EE-58   Media disconnected
B0-60-88-53-FB-47   \Device\Tcpip_{02B2711F-C81F-4814-BB3B-250CB9EB0D07}
```
# curl:
```

C:\Users\Priyadharshini>curl google.com
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
```


## Result
Thus Execution of Network commands Performed 
