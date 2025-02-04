# Vezeték nélküli hálózat

**Dátum:** 2025.02.04 <br>
**Helyszín:** Degem Labor <br>
**Készítette:** Tomolya Milán <br>

## Hálózati Eszközök

- **SOHO router** – Linksys WRT54GL<br>
- **Switch** – cisco catalyst 2950 switch<br>
- **Laptop** – Levono thinkpad, teszteléshez<br>
- **Telefon** – realme gt2 pro, teszteléshez<br>


## Hálózati Topológia
 
![Topológia](https://github.com/VLevente0/meresi-jegyzokonyvek/blob/bd62f13a4b8a0b66d23d1d3a7289ae72309e2e7a/main/kepek/vezeteknelkuli/topologia.png)

## Hálózat kiépítsének lépései

- 1.A topológia alapján kialakítáni a hálózatot
- 2.A soho router megfelelő beállítása, konfigurálása
- 3.Az eszközök csatlakoztatása a vezeték nélküli hálózathoz
- 4.Tesztelés


## Tesztelés

1.IP beállítások lekérése<br>
C:\Users\tanulo>ipconfig /all

Windows IP Configuration

   Host Name . . . . . . . . . . . . : Degem-10
   Primary Dns Suffix  . . . . . . . : kkszki.local
   Node Type . . . . . . . . . . . . : Mixed
   IP Routing Enabled. . . . . . . . : No
   WINS Proxy Enabled. . . . . . . . : No
   DNS Suffix Search List. . . . . . : kkszki.local

Wireless LAN adapter Helyi kapcsolat* 9:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :
   Description . . . . . . . . . . . : Microsoft Wi-Fi Direct Virtual Adapter
   Physical Address. . . . . . . . . : E2-0A-F6-3B-3A-B5
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes

Wireless LAN adapter Helyi kapcsolat* 10:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :
   Description . . . . . . . . . . . : Microsoft Wi-Fi Direct Virtual Adapter #2
   Physical Address. . . . . . . . . : F2-0A-F6-3B-3A-B5
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Description . . . . . . . . . . . : Intel(R) Ethernet Connection (13) I219-V
   Physical Address. . . . . . . . . : 84-A9-38-56-C3-91
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes
   Link-local IPv6 Address . . . . . : fe80::86a8:f53c:b110:f8e6%11(Preferred)
   IPv4 Address. . . . . . . . . . . : 192.168.6.193(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.192
   Lease Obtained. . . . . . . . . . : 2025. február 4., kedd 11:22:42
   Lease Expires . . . . . . . . . . : 2025. február 5., szerda 11:22:42
   Default Gateway . . . . . . . . . : 192.168.6.254
   DHCP Server . . . . . . . . . . . : 192.168.6.254
   DHCPv6 IAID . . . . . . . . . . . : 361015608
   DHCPv6 Client DUID. . . . . . . . : 00-01-00-01-2B-F6-B3-0D-84-A9-38-56-C3-91
   DNS Servers . . . . . . . . . . . : 10.224.55.253
                                       10.224.55.252
   NetBIOS over Tcpip. . . . . . . . : Enabled

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   Description . . . . . . . . . . . : Realtek RTL8852AE WiFi 6 802.11ax PCIe Adapter
   Physical Address. . . . . . . . . : E0-0A-F6-3B-3A-B5
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes
   Link-local IPv6 Address . . . . . : fe80::54af:7a3f:42a2:39e9%6(Preferred)
   IPv4 Address. . . . . . . . . . . : 192.168.6.195(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.192
   Lease Obtained. . . . . . . . . . : 2025. február 4., kedd 11:47:39
   Lease Expires . . . . . . . . . . : 2025. február 5., szerda 11:47:40
   Default Gateway . . . . . . . . . : 192.168.6.254
   DHCP Server . . . . . . . . . . . : 192.168.6.254
   DHCPv6 IAID . . . . . . . . . . . : 132123382
   DHCPv6 Client DUID. . . . . . . . : 00-01-00-01-2B-F6-B3-0D-84-A9-38-56-C3-91
   DNS Servers . . . . . . . . . . . : 10.224.55.253
                                       10.224.55.252
   NetBIOS over Tcpip. . . . . . . . : Enabled

C:\Users\tanulo>  
2.IP eldobása<br>
  C:\Users\tanulo>ipconfig /release

Windows IP Configuration

No operation can be performed on Helyi kapcsolat* 9 while it has its media disconnected.
No operation can be performed on Helyi kapcsolat* 10 while it has its media disconnected.

Wireless LAN adapter Helyi kapcsolat* 9:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Helyi kapcsolat* 10:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::86a8:f53c:b110:f8e6%11
   Default Gateway . . . . . . . . . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::54af:7a3f:42a2:39e9%6
   Default Gateway . . . . . . . . . :

C:\Users\tanulo> 
3. Új IP kérés <br>
   C:\Users\tanulo>ipconfig /renew

Windows IP Configuration

No operation can be performed on Helyi kapcsolat* 9 while it has its media disconnected.
No operation can be performed on Helyi kapcsolat* 10 while it has its media disconnected.

Wireless LAN adapter Helyi kapcsolat* 9:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Helyi kapcsolat* 10:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::86a8:f53c:b110:f8e6%11
   IPv4 Address. . . . . . . . . . . : 192.168.6.193
   Subnet Mask . . . . . . . . . . . : 255.255.255.192
   Default Gateway . . . . . . . . . : 192.168.6.254

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::54af:7a3f:42a2:39e9%6
   IPv4 Address. . . . . . . . . . . : 192.168.6.195
   Subnet Mask . . . . . . . . . . . : 255.255.255.192
   Default Gateway . . . . . . . . . : 192.168.6.254

C:\Users\tanulo>  
4. Routing tábla megjelenítése  <br>
   C:\Users\tanulo>netstat -r
===========================================================================
Interface List
 18...e2 0a f6 3b 3a b5 ......Microsoft Wi-Fi Direct Virtual Adapter
 17...f2 0a f6 3b 3a b5 ......Microsoft Wi-Fi Direct Virtual Adapter #2
 11...84 a9 38 56 c3 91 ......Intel(R) Ethernet Connection (13) I219-V
  6...e0 0a f6 3b 3a b5 ......Realtek RTL8852AE WiFi 6 802.11ax PCIe Adapter
  1...........................Software Loopback Interface 1
===========================================================================

IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
          0.0.0.0          0.0.0.0    192.168.6.254    192.168.6.193     35
          0.0.0.0          0.0.0.0    192.168.6.254    192.168.6.195     55
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    331
        127.0.0.1  255.255.255.255         On-link         127.0.0.1    331
  127.255.255.255  255.255.255.255         On-link         127.0.0.1    331
    192.168.6.192  255.255.255.192         On-link     192.168.6.193    291
    192.168.6.192  255.255.255.192         On-link     192.168.6.195    311
    192.168.6.193  255.255.255.255         On-link     192.168.6.193    291
    192.168.6.195  255.255.255.255         On-link     192.168.6.195    311
    192.168.6.255  255.255.255.255         On-link     192.168.6.193    291
    192.168.6.255  255.255.255.255         On-link     192.168.6.195    311
        224.0.0.0        240.0.0.0         On-link         127.0.0.1    331
        224.0.0.0        240.0.0.0         On-link     192.168.6.193    291
        224.0.0.0        240.0.0.0         On-link     192.168.6.195    311
  255.255.255.255  255.255.255.255         On-link         127.0.0.1    331
  255.255.255.255  255.255.255.255         On-link     192.168.6.193    291
  255.255.255.255  255.255.255.255         On-link     192.168.6.195    311
===========================================================================
Persistent Routes:
  None

IPv6 Route Table
===========================================================================
Active Routes:
 If Metric Network Destination      Gateway
  1    331 ::1/128                  On-link
 11    291 fe80::/64                On-link
  6    311 fe80::/64                On-link
  6    311 fe80::54af:7a3f:42a2:39e9/128
                                    On-link
 11    291 fe80::86a8:f53c:b110:f8e6/128
                                    On-link
  1    331 ff00::/8                 On-link
 11    291 ff00::/8                 On-link
  6    311 ff00::/8                 On-link
===========================================================================
Persistent Routes:
  None

C:\Users\tanulo>  
5. Microsoft elérhetőség teszt <br>
   ![microsoft](https://github.com/user-attachments/assets/d5ef8e26-4306-435f-b7a3-978d898afad7)
  
6. www.ipon.hu server felé vezető útvonal lekövetése <br>
  C:\Users\tanulo>tracert ipon.hu

Tracing route to ipon.hu [94.125.179.179]
over a maximum of 30 hops:

  1     1 ms    <1 ms    <1 ms  192.168.6.254
  2     1 ms     *        1 ms  FOREFRONT.kkszki.local [10.224.55.250]
  3     2 ms     1 ms     1 ms  gw.barsonyj-miskolc.edu.hu [195.199.195.22]
  4     6 ms     8 ms     6 ms  10.0.0.1
  5     6 ms     6 ms     7 ms  hge0-0-0-8.rtr.dataplex.hbone.hu [195.111.111.54]
  6     6 ms     6 ms     6 ms  hge0-0-0-6.core2.vh.hbone.hu [195.111.113.55]
  7    59 ms     8 ms     7 ms  193.224.231.129
  8     6 ms     6 ms     6 ms  vhg-sul-sw-ci-0.wifi.hbone.hu [193.224.231.130]
  9     6 ms     6 ms     6 ms  193.224.231.185
 10     *        *        8 ms  193.224.231.218
 11     *        7 ms     *     bix.deninet.hu [193.188.137.122]
 12     6 ms     6 ms     7 ms  bix.deninet.hu [193.188.137.122]
 13     7 ms     6 ms     6 ms  100.64.5.254
 14     7 ms     7 ms     6 ms  100.64.5.253
 15     6 ms     7 ms     6 ms  94.125.179.179

Trace complete.

C:\Users\tanulo>  
7. Portok listázása  <br>
  C:\Users\tanulo>netstat -anob
A kért művelethez magasabb felhasználói szint szükséges. 
8. Hálózati kapcsolatok <br>
   C:\Users\tanulo>netsh interface show interface

Admin State    State          Type             Interface Name
-------------------------------------------------------------------------
Enabled        Connected      Dedicated        Ethernet
Enabled        Connected      Dedicated        Wi-Fi


C:\Users\tanulo>
9. DNS beállítások aktualizálása <br>
   C:\Users\tanulo>ipconfig /flushdns

Windows IP Configuration

Successfully flushed the DNS Resolver Cache.

C:\Users\tanulo>  
10. Hálózati meghajtók <br>
    C:\Users\tanulo>net use
A rendszer tárolja az új kapcsolatokat.

A listában nincsenek bejegyzések.


C:\Users\tanulo>  
11.www.ipon.hu server tartománynév és IP cím megjelenítése<br>
    C:\Users\tanulo>nslookup ipon.hu
Server:  FujitsuSRV.kkszki.local
Address:  10.224.55.253

Non-authoritative answer:
Name:    ipon.hu
Address:  94.125.179.179


C:\Users\tanulo>
  
12. FQDN megjelenítése<br>
    C:\Users\tanulo>netstat -f

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    192.168.6.193:49418    20.199.120.151:https   ESTABLISHED
  TCP    192.168.6.193:64595    wf-in-f188.1e100.net:5228  ESTABLISHED
  TCP    192.168.6.193:64599    bud02s41-in-f10.1e100.net:https  ESTABLISHED
  TCP    192.168.6.193:64601    bud02s41-in-f10.1e100.net:https  ESTABLISHED
  TCP    192.168.6.193:64676    bud02s37-in-f14.1e100.net:https  TIME_WAIT
  TCP    192.168.6.193:64682    bud02s33-in-f14.1e100.net:https  TIME_WAIT
  TCP    192.168.6.193:64688    bud02s43-in-f14.1e100.net:https  ESTABLISHED
  TCP    192.168.6.193:65435    LenovoSRV.kkszki.local:epmap  TIME_WAIT
  TCP    192.168.6.193:65436    LenovoSRV.kkszki.local:49668  TIME_WAIT
  TCP    192.168.6.193:65437    52.168.117.170:https   TIME_WAIT
  TCP    192.168.6.193:65442    LenovoSRV.kkszki.local:epmap  TIME_WAIT
  TCP    192.168.6.193:65443    LenovoSRV.kkszki.local:49668  TIME_WAIT
  TCP    192.168.6.193:65447    bud02s43-in-f3.1e100.net:http  ESTABLISHED
  TCP    192.168.6.193:65448    199.232.18.172:http    ESTABLISHED
  TCP    192.168.6.193:65449    bud02s42-in-f4.1e100.net:https  ESTABLISHED

C:\Users\tanulo>
13. Ping a kliensek között <br>
   ![ping1](https://github.com/user-attachments/assets/e71777fa-0c32-43e7-87af-39135e946df0)
   
  
