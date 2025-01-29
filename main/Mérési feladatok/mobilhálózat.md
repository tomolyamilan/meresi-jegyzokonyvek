## Jegyzőkönyv

**Téma:** Komplex Távközlési Hálózat Tervezése, Telepítése és Mérése  
**Dátum:** [Írd be a dátumot]  
**Helyszín:** [Írd be a helyszínt]  
**Résztvevők:** [Sorold fel a résztvevőket]  

---

### 1. Bevezetés
- A jegyzőkönyv célja a komplex távközlési hálózat tervezésével, telepítésével és mérésével kapcsolatos megbeszélés dokumentálása.
- A projekt célkitűzéseinek és követelményeinek áttekintése.

### 2. Hálózattervezés
- A szükséges infrastruktúra és technológiák kiválasztása.
- A hálózati topológia meghatározása.
- Kapcsolódási pontok és csomópontok tervezése.
- Biztonsági és redundancia szempontok figyelembevétele.

### 3. Telepítési Fázis
- Hardver- és szoftverkomponensek beüzemelése.
- Kábelezési és szerelési munkák részletezése.
- Hálózati eszközök konfigurálása.
- Üzembe helyezési és tesztelési lépések.

### 4. Mérések és Tesztelés
- Hálózati teljesítmény és adatátviteli sebesség vizsgálata.
- Jelkésleltetés és csomagvesztési arány elemzése.
- Hibakeresési és diagnosztikai eljárások alkalmazása.
- Minőségbiztosítási tesztek végrehajtása.

### 5. Használt Eszközök és Hálózati Struktúra
- **Mikrotik LHG18 LTE antenna** (192.168.88.1) – Internetkapcsolat biztosítása
- **DHCP Server**: 192.168.88.100 - 192.168.88.250 (Subnet: 255.255.255.0)
- **Mikrotik nRay60 MASTER** (192.168.88.2) – Mikroháullámú adatkapcsolat főpontja
- **Mikrotik nRay60 SLAVE** (192.168.88.3) – Mikroháullámú adatkapcsolat végpontja
- **ASUS RT-AX58 Router** (192.168.88.4) – Helyi hálózat biztosítása
- **PC / Laptop 1** (DHCP tartományból)
- **PC / Laptop 2** (DHCP tartományból)

### 6. Topológia

  <img src="" alt="Topológia" />


### 7. Routing Tábla
| Célhálózat       | Maszk         | Next Hop       | Interface          | Eszköz |
|------------------|--------------|---------------|--------------------|--------|
| 0.0.0.0         | 0.0.0.0       | 192.168.88.1  | Mikrotik LHG18 LTE | Mikrotik LHG18 LTE |
| 192.168.88.0/24 | 255.255.255.0 | Direkt        | ASUS RT-AX58       | ASUS RT-AX58 Router |
| 192.168.88.2    | 255.255.255.255 | Direkt      | Mikrotik nRay60 MASTER | Mikrotik nRay60 MASTER |
| 192.168.88.3    | 255.255.255.255 | 192.168.88.2 | Mikrotik nRay60 SLAVE | Mikrotik nRay60 SLAVE |
| 192.168.88.4    | 255.255.255.255 | Direkt      | ASUS RT-AX58       | ASUS RT-AX58 Router |

### 8. Összegzés és Következő Lépések
- Az elvégzett munka összefoglalása.
- Kiemelt problémák és megoldási javaslatok.
- Következő megbeszélés időpontjának és témájának meghatározása.

---

**Aláírások:**  
[Készítette: Vad Levente]
