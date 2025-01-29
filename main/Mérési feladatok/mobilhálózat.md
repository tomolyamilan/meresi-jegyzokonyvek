## Jegyzőkönyv

**Téma:** Komplex Távközlési Hálózat Tervezése, Telepítése és Mérése  
**Dátum:** [2025.01.29]  
**Helyszín:** [V3 Labor]  
**Résztvevők:** [Vad Levente]  

---

### 1. Bevezetés
- A jegyzőkönyv célja a komplex távközlési hálózat tervezésével, telepítésével és mérésével kapcsolatos megbeszélés dokumentálása.
- A projekt célkitűzéseinek és követelményeinek áttekintése.

### 2. Hálózattervezés
- A szükséges infrastruktúra és technológiák kiválasztása.
- A hálózati topológia meghatározása.
- Kapcsolódási pontok és csomópontok tervezése.

### 3. Telepítési Fázis
- Hardver- és szoftverkomponensek beüzemelése.
- Hálózat fizikai összekötése.
- Hálózati eszközök konfigurálása.
- Üzembe helyezési és tesztelési lépések.

### 4. Használt Eszközök és Hálózati Struktúra
- **Mikrotik LHG18 LTE antenna** (192.168.88.1) – Internetkapcsolat biztosítása
- **DHCP Server**: 192.168.88.100 - 192.168.88.250 (Subnet: 255.255.255.0)
- **Mikrotik nRay60 MASTER** (192.168.88.2) – Mikroháullámú adatkapcsolat főpontja
- **Mikrotik nRay60 SLAVE** (192.168.88.3) – Mikroháullámú adatkapcsolat végpontja
- **ASUS RT-AX58 Router** (192.168.88.4) – Helyi hálózat biztosítása
- **PC / Laptop 1** (DHCP tartományból)
- **PC / Laptop 2** (DHCP tartományból)

### 5. Topológia

  <img src="https://github.com/VLevente0/meresi-jegyzokonyvek/blob/add4f824a8f5d14e6b031365f025095937d17a66/main/kepek/mobilh%C3%A1l%C3%B3zat/Megnevezetlen%20diagram.drawio.png" alt="Topológia" />


### 6. Routing Tábla
| Célhálózat       | Maszk         |  Interface          | Eszköz |
|------------------|--------------|--------------------|--------|
| ISP-tol DHCP    |              |  Mikrotik LHG18 LTE | Mikrotik LHG18 LTE |
| DHCP 192.168.88.100-250/24 | 255.255.255.0      |   Ethernet     | Laptop   |
| DHCP 192.168.88.100-250/24 | 255.255.255.0      |   Wi-Fi      | Laptop   |
| 192.168.88.2    | 255.255.255.0 |  Mikrotik nRay60 MASTER | Mikrotik nRay60 MASTER |
| 192.168.88.3    | 255.255.255.0 |  Mikrotik nRay60 SLAVE | Mikrotik nRay60 SLAVE |
| 192.168.88.4    | 255.255.255.0 |  ASUS RT-AX58       | ASUS RT-AX58 Router |


### 7. Mérések és Tesztelés
- Hálózati teljesítmény és adatátviteli sebesség vizsgálata.
- Jelkésleltetés és csomagvesztési arány elemzése.
- Hibakeresési és diagnosztikai eljárások alkalmazása.
- Minőségbiztosítási tesztek végrehajtása.



### 8. Összegzés és Következő Lépések
- Az elvégzett munka összefoglalása.
- Kiemelt problémák és megoldási javaslatok.
- Következő megbeszélés időpontjának és témájának meghatározása.

---

**Aláírások:**  
[Készítette: Vad Levente]
