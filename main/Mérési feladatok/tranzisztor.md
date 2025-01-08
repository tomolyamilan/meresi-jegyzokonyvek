**MÉRÉSI JEGYZŐKÖNYV**

**1. Mérés címe:**
Transzisztor munkapontjának vizsgálata

**2. Mérést végezte:**
Mercz Noel, Vad Levente

**3. Mérés időpontja:**
2025.01.08.

**4. Mérés helyszíne:**
Villamos 3 labor

**5. Célkitűzés:**
A transzisztor bázis-emitter feszültségének (Ube), a kollektor ellenállás (Urc) feszültségének, valamint a kollektoráram (Lc) összefüggéseinek vizsgálata. A transzisztor munkapontjának beállítása során az áramköri viszonyok részletes elemzése.

---

**5. Használt eszközök:**
- 1 db NPN transzisztor (BC639)
- Ellenállások: 1.5 kΩ és 220 Ω
- Áramforrás: +5 V (NI MyDaq)
- Multiméter (METEX M3-800)
- Csatlakozók, vezetékek
- Piros Led

---

**6. Kapcsolási rajz:**
<br />
<img src="https://noel-mercz.github.io/Meresijegyzokonyvek/tranzisztor_meres/img/almafa.PNG" />

**Kapcsolási elemek leírása:**
A bemeneti jel a bázisra érkezik egy 1.5 kΩ-ellenálláson keresztül, amely beállítja a bázis-emitter feszültséget. A kollektor-körben egy 220 Ω-os ellenállás biztosítja a kollektoráram korlátozását.

---

**7. Mérési eredmények:**

Az alábbi táblázat tartalmazza az értékeket, amelyek a mérés során lettek rögzítve:

| Ube [V] | Urc [V] | Lc [mA]      |
|---------|---------|--------------|
| 0       | 0       | 0,00         |
| 0,4     | 0       | 0,00         |
| 0,5     | 0,003   | 0,01364      |
| 0,6     | 0,111   | 0,50455      |
| 0,7     | 0,87    | 3,95455      |
| 0,8     | 2,09    | 9,50000      |
| 0,9     | 2,5     | 11,36364     |
| 1       | 2,53    | 11,50000     |
| 1,1     | 2,54    | 11,54545     |
| 1,2     | 2,55    | 11,59091     |
| 1,3     | 2,56    | 11,63636     |
| 1,4     | 2,58    | 11,72727     |
| 1,5     | 2,58    | 11,72727     |
| 1,6     | 2,58    | 11,72727     |
| 1,7     | 2,58    | 11,72727     |
| 1,8     | 2,58    | 11,72727     |
| 1,9     | 2,59    | 11,72727     |
| 2       | 2,59    | 11,72727     |
| 2,1     | 2,59    | 11,72727     |
| 2,2     | 2,59    | 11,72727     |
| 2,3     | 2,59    | 11,72727     |
| 2,4     | 2,59    | 11,72727     |
| 2,5     | 2,59    | 11,72727     |


**Grafikus ábrázolás**
<br />
<img src="https://noel-mercz.github.io/Meresijegyzokonyvek/tranzisztor_meres/img/graf.PNG" />

---

**8. Értékelés:**

1. **Mérési tapasztalatok:**
   - A transzisztor bázis-emitter feszültségének növelésével a kollektoráram kezdetben exponenciálisan nőtt, majd elérte a telítési tartományt, ahol gyakorlatilag konstans maradt.
   - A kollektor-ellenálláson mért feszültség a bázis-emitter feszültséggel nőtt, de az arányosság megszűnt a telítés után.

2. **Grafikus megjelenítés:**
   - A mért adatokat grafikonokon érdemes ábrázolni az Ube-Lc és Ube-Urc összefüggések áttekintése érdekében. (Ez nem szerepel a feltöltött anyagok között.)

3. **Következtetések:**
   - A transzisztor helyesen működött aktív tartományban, majd telítési állapotba került.
   - Az adatok igazolják az elvégzett mérés pontosságát.

---

**9. Javaslatok:**
- A mérés megismétlése nagyobb pontosságú eszközökkel az értékek validálása érdekében.
- Hőmérséklet-változás hatásainak vizsgálata a transzisztorra.