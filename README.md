# Ročníkový projekt: Renovace a kompletace PC sestavy
**Autor:** Daniel Vlasák
**Třída:** S3E
**Školní rok:** 2025/2026
**Předmět:** Mikropočítačové Systémy / Praktická cvičení

---

##  1. Cíl projektu
Cílem mého ročníkového projektu je záchrana, vyčištění a kompletní zprovoznění starší kancelářské sestavy **Lenovo ThinkCentre A58**, která byla nalezena v rozebraném stavu s neznámou funkčností. Projekt se zaměřuje na identifikaci komponent, ověření jejich vzájemné kompatibility, správnou montáž a cable management. Výstupem je funkční počítač schopný POST testu.

---

##  2. Dokumentace stavu a hardware

### Specifikace sestavy (Inventory)
Po identifikaci všech dílů se sestava skládá z následujících komponent:

| Komponenta | Model / Specifikace | Poznámka |
| :--- | :--- | :--- |
| **Základní deska** | Lenovo L-IG41M | Socket 775, Chipset G41, DDR3 support |
| **Procesor (CPU)** | Intel Core 2 Duo E7500 | 2.93 GHz, 3MB Cache, TDP 65W |
| **Chladič** | Stock Intel Cooler | Hliníkový, 4-pin PWM regulace |
| **Paměť (RAM)** | 2GB DDR3 Samsung/Lenovo | 1066 MHz (PC3-8500U) |
| **Grafická karta** | ASUS GeForce 7300 SE | Pasivní chlazení, Low Profile |
| **Pevný disk** | Seagate Barracuda 7200.11 | 320 GB, SATA II, 7200 rpm |
| **Zdroj (PSU)** | AcBel PC6001 (Lenovo OEM) | 280 W Max výkon |
| **Skříň** | Lenovo ThinkCentre A58 Tower | Pevné ocelové šasi, ATX |

*(Fotodokumentace komponent)*
![Přehled komponent](komponenty.jpg)

---

##  3. Postup realizace a řešení problémů

### Fáze 1: Vstupní diagnostika a čištění
Sestava byla kompletně rozebrána. Komponenty jsem očistil od prachu stlačeným vzduchem. Z procesoru a chladiče byla odstraněna stará ztvrdlá teplovodivá pasta pomocí isopropylalkoholu, aby bylo možné nanést novou vrstvu pro efektivní odvod tepla.

### Fáze 2: Řešení problému s kompatibilitou RAM
Během přípravy k montáži jsem narazil na zásadní problém, který pravděpodobně způsoboval nefunkčnost PC u předchozího uživatele.
* **Popis problému:** K základní desce byly přiloženy dva paměťové moduly, které vypadaly vizuálně téměř shodně.
* **Analýza:** Při detailní kontrole štítků jsem zjistil nesrovnalost:
    * Modul A: **Lenovo 2GB (DDR3 / PC3-8500U)** – Správný typ.
    * Modul B: **OCZ 1GB (DDR2 / PC2-5400)** – Nekompatibilní typ.
* **Řešení:** Základní deska L-IG41M podporuje pouze paměti DDR3. Osazení DDR2 modulu je fyzicky nemožné bez poškození slotu (jiná poloha výřezu) a elektricky nekompatibilní. Modul DDR2 jsem proto z montáže vyřadil a systém osadil pouze 2GB DDR3 modulem do slotu DIMM_1.

*(Porovnání modulů)*
![Detail problému RAM](ram_problem.jpg)

### Fáze 3: Kompletace a Cable Management
1. **CPU:** Osazení procesoru do patice LGA775 (kontrola orientace dle zlaté šipky).
2. **Chlazení:** Aplikace pasty a montáž chladiče. Důležité bylo nezapomenout zapojit 4-pin konektor ventilátoru do desky (CPU_FAN), aby nedošlo k přehřátí.
3. **Kabeláž:** Zapojení 24-pin konektoru pro desku a 4-pin 12V konektoru pro napájení procesoru.
4. **Senzory:** Zapojení specifického teplotního čidla (Thermal Sensor), které vyžadují OEM desky Lenovo pro řízení otáček.

*(Pohled na zapojenou desku ve skříni)*
![Hotová montáž](hotovo.jpg)

---

##  4. Závěr a funkčnost
Po finální kontrole zapojení byl proveden testovací start.
* **Výsledek:** Počítač úspěšně nastartoval, ventilátory se roztočily a systém detekoval základní hardware. Problém s nekompatibilní RAM byl úspěšně vyřešen.

###  Videodokumentace
Video zachycující průběh montáže, vysvětlení problému s RAM a finální start systému naleznete zde:
> **[ZDE VLOŽ ODKAZ NA SVÉ YOUTUBE VIDEO]**

---

##  5. Použité zdroje a nástroje

### Použité nástroje
(1) GITHUB, INC. *GitHub*. Online. © 2025. Dostupné z: https://github.com/. [cit. 2025-12-16].
(2) CITACE.COM, S.R.O. *Citace.com*. Online. © 2025. Dostupné z: https://www.citace.com/. [cit. 2025-12-16].
(3) OPENAI. *ChatGPT (model GPT-4o)*. Online. 2025. Nástroj využit pro konzultaci kompatibility paměťových modulů a korekturu textu.

### Literatura a zdroje informací
[1] *Intel Core 2 Duo Processor E7500 Specifications*. Online. Intel. Dostupné z: https://ark.intel.com/. [cit. 2025-12-16].
[2] *Lenovo ThinkCentre A58 Hardware Maintenance Manual*. Online. Lenovo Support. Dostupné z: https://support.lenovo.com/. [cit. 2025-12-16].

##  Poděkování
Děkuji vyučujícímu za zadání tohoto praktického projektu. Dále děkuji internetové komunitě za veřejně dostupné manuály k OEM deskám Lenovo, které pomohly při zapojení.
