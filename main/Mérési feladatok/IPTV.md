# Távközlési Technikus Vizsga Jegyzőkönyv

## Vizsgázó Neve:
Vad Levente

## Vizsgafeladat: DVB-T jel fejállomásba küldése és IPTV rendszeren való kiadása

---

### 1. Használt eszközök

- **Beltéri antenna**: Iskra P2845 Logper
- **Fejállomás**: Lemco SCL-824CT
- **Set-top box**: MAG IPTV
- **Hálózati ezközök**: HP 2312 Procurve switch

---

### 2. Beltéri Antenna Beállítása és Mérése

- **Antenna helyzete**: DNY 233°
- **Adótorony**: Miskolci avasi adótorony
- **Jelszint**: 52dBu
- **Jel-zaj viszony (SNR) (dB)**: 
- **Multiplex frekvencia**: _[frekvencia]_
- **Multiplex szimbólumráta**: _[szimbólumráta]_
- **Multiplex**:


---

### 3. Fejállomás Mérések

- **Fejállomás bemeneteire beérkező multiplexek**:
  - **Multiplex 1**: multiplex a
  - **Multiplex 2**: multiplex b
  - **Multiplex 7**: Miskolc városi TV
  - **Multiplex 8**: multiplex e 

**Jel bevezetés mérése:**
- **Jelszint (dBμV)**: _[érték]_
- **Jel-zaj viszony (SNR) (dB)**: _[érték]_

---

### 4. IPTV Stream és Multicast Konfigurálás

- **Multicast IP tartomány**: 239.50.50.1-239.50.50.39
- **Multicast port**: 1234

**Set-top box konfigurálása:**
- **Multicast IP címek**: _[IP címek]_
- **Csatornák listája**: _[csatornák]_

---

### 5. Hálózati Tesztek

- **Ping teszt multicast IP címre**:
  - **Válaszidő (ms)**: _[érték]_
  - **Csomagvesztés (%)**: 0

- **Traceroute eredmény**:
  - **Útvonal**: _[útvonal adatok]_

- **iPerf3 hálózati teljesítmény**:
  - **Sávszélesség**: _[sávszélesség]_
  - **UDP csomagvesztés**: _[csomagvesztés]_

---

### 6. IPTV Stream Elemzés (FFmpeg/Wireshark)

- **FFmpeg stream elemzés**:
  - **Bitráta**: _[bitráta]_
  - **Késleltetés**: _[késleltetés]_
  - **Csomagvesztés**: _[csomagvesztés]_

- **Wireshark csomagok elemzése**:
  - **Mentett fájl**: _[fájl neve]_
  - **Multicast csomagok száma**: _[csomagszám]_

---

### 7. Eredmények

- **Lock állapot**: [ ] Igen [ ] Nem
- **Jelszint (dBμV)**: _[mért érték]_
- **SNR (dB)**: _[mért érték]_
- **Bit Error Rate (BER)**: _[mért érték]_
- **Modulation Error Ratio (MER) (dB)**: _[mért érték]_
- **Csillapítás (dB)**: _[mért érték]_

---

### 8. Hőmérséklet és Időjárási Körülmények

- **Hőmérséklet**: _[hőmérséklet]_
- **Szélsebesség**: _[szélsebesség]_
- **Egyéb megjegyzések**: _[további megjegyzések]_

---


- **Készítette**: Vad Levente

---

**Jegyzőkönyv zárása:**

A mérések és a konfigurálás sikeresen befejeződtek, az IPTV stream és a fejállomás megfelelően beállításra került.
4