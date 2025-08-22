# Aplikace pro objednávání krmiva

##  Přehled projektu

Toto je **Aplikace pro objednávání krmiva** vytvořená jako školní zkouškový projekt. Aplikace byla vyvinuta v **5hodinovém časovém limitu** a prokazuje znalosti webového vývoje pomocí HTML, CSS (SCSS) a JavaScriptu.

##  Účel aplikace

Aplikace slouží jako interaktivní formulář pro objednávání krmiva s výpočtem ceny v reálném čase. Uživatelé mohou vybrat různé typy krmiva, specifikovat množství, zvolit kvalitativní možnosti, vybrat způsob dopravy a ověřit svůj rozpočet proti vypočítané celkové ceně.

##  Funkce

###  Výběr krmiva
- **Psí krmivo**: 150 Kč/kg
- **Kočičí krmivo**: 120 Kč/kg  
- **Krmivo pro rybičky**: 50 Kč/kg
- **Krmivo pro tygra**: 800 Kč/kg

###  Kvalitativní možnosti
- **Bio kvalita**: +30% navýšení ceny
- **Extra premium kvalita**: +50% navýšení ceny
- **Extra nekvalita pro chudé**: -15% snížení ceny
- **Dárkové balení**: +500 Kč pevný poplatek

###  Možnosti dopravy
- **Osobní odběr**: Bez příplatku
- **Firemní kurýr**: +10% z ceny krmiva
- **Česká pošta**: +250 Kč pevný poplatek

###  Systém výpočtu ceny
- Výpočet ceny v reálném čase na základě:
  - Vybraného typu krmiva a množství
  - Zvolených kvalitativních možností
  - Způsobu dopravy
- Ověření rozpočtu proti vypočítané celkové ceně
- Interaktivní porovnání cen

###  Validace formuláře
- Validace vstupu pro emailové pole
- Zpětná vazba v reálném čase
- Zobrazení chybových hlášení pro neplatné vstupy

##  Technická implementace

### Frontend technologie
- **HTML5**: Sémantická struktura a formulářové prvky
- **CSS3/SCSS**: Stylování s integrací Bootstrap 5.3.3
- **JavaScript (ES6+)**: Interaktivní funkcionalita a výpočty
- **Bootstrap 5.3.3**: Responzivní design framework

### Klíčové JavaScript funkce

#### `vypocetCeny()`
- Počítá celkovou cenu na základě uživatelských voleb
- Aplikuje kvalitativní modifikátory a náklady na dopravu
- Aktualizuje zobrazení v reálném čase

#### `kontrolaCeny()`
- Porovnává uživatelský rozpočet s vypočítanou cenou
- Poskytuje zpětnou vazbu o finanční dostatečnosti

#### `validuj()`
- Validuje emailový vstup pomocí regex
- Dynamicky zobrazuje/skrývá chybové hlášení

### Styly
- **Responzivní design**: Funguje na různých velikostech obrazovek
- **Moderní UI**: Čistý, profesionální vzhled
- **Vizuální zpětná vazba**: Barevně kódované stavy validace
- **Integrace Bootstrap**: Konzistentní stylování komponent

##  Struktura projektu

```
PetFoodFormJS/
├── index.html          # Hlavní HTML soubor
├── script.js           # JavaScript funkcionalita
├── package.json        # Závislosti (Bootstrap)
├── scss/
│   ├── custom.scss     # SCSS zdrojový soubor
│   ├── custom.css      # Zkompilovaný CSS
│   └── custom.css.map  # Source map
└── node_modules/       # Bootstrap závislosti
```

##  Designové prvky

- **Barevné schéma**: Tyrkysové a šedé téma
- **Rozložení**: Centrovaný kontejner s zaoblenými rohy
- **Typografie**: Bootstrap výchozí s vlastními nadpisy
- **Interaktivní prvky**: Hover efekty a focus stavy

##  Instalace a použití

### Předpoklady
- Moderní webový prohlížeč
- Node.js (pro správu závislostí)

### Instalace
1. Naklonujte nebo stáhněte projekt
2. Nainstalujte závislosti:
   ```bash
   npm install
   ```
3. Otevřete `index.html` ve webovém prohlížeči

### Návod na použití
1. **Vyberte krmivo**: Zvolte z rozbalovacího menu
2. **Zadejte množství**: Specifikujte hmotnost v kilogramech
3. **Zvolte kvalitu**: Vyberte požadované kvalitativní možnosti
4. **Vyberte dopravu**: Zvolte preferovaný způsob dopravy
5. **Spočítejte cenu**: Klikněte "Spočítat cenu" pro zobrazení celkové částky
6. **Ověřte rozpočet**: Zadejte svůj rozpočet a zkontrolujte dostupnost
7. **Zadejte email**: Uveďte kontaktní informace (validace povolena)

##  Logika výpočtu ceny

Aplikace implementuje sofistikovaný cenový algoritmus:

1. **Základní cena**: Cena typu krmiva × Množství
2. **Kvalitativní modifikátory**: Aplikovány postupně
   - Bio: ×1.3
   - Extra Premium: ×1.5
   - Nekvalita: ÷1.15
   - Dárkové balení: +500 Kč
3. **Náklady na dopravu**: Přidány podle výběru
   - Kurýr: +10% z ceny krmiva
   - Pošta: +250 Kč pevný poplatek

##  Vzdělávací kontext

Tento projekt demonstruje:
- **Time management**: Vývoj v přísném 5hodinovém limitu
- **Řešení problémů**: Složitá logika výpočtu cen
- **Uživatelská zkušenost**: Intuitivní design formuláře
- **Kvalita kódu**: Čistý, čitelný JavaScript
- **Moderní webové standardy**: HTML5, CSS3, ES6+

##  Autor

**Robin Lassak** - Studentský projekt vytvořený pro školní zkoušku

##  Licence

Toto je vzdělávací projekt vytvořený jako součást školní zkoušky.

---

*Vytvořeno v 5hodinovém časovém limitu jako demonstrace dovedností webového vývoje a porozumění moderním webovým technologiím.*
