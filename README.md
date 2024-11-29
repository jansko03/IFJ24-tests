# ⚠️**POZOR NA TESTY test_retype_i32 A test_retype_bad**⚠️

Testy sa od **26.11.2024** riadia podľa tejto správy:
Platí to, co je v zadání a speciálně zde na fóru. https://moodle.vut.cz/mod/forum/discuss.php?d=4850
1. vždy se dá impl. převést konstantní výraz f64 s nulovou částí na i32
2. v op. +, -, * se dá impl. převést *literál* i32 -> f64
- v op. / ale jde použít jen bod 1)
3. v relačních op. platí to, co je na fóru


# IFJ Testovací Skript

Tento skript automatizuje proces testovania IFJ kompilátora a interpretu. Kompiluje zdrojové súbory .ifj, spúšťa vygenerovaný kód cez interpret s rôznymi vstupnými súbormi a porovnáva výsledky s referenčnými výstupmi.
Niektoré testy počítajú s implementácou rozšírenia FUNEXP. Tieto testy by mali byť označené FUNEXP. Ak nájdete nejaký neoznačený test, napíšte nám/pull request.





## Spustenie



Skript spustíte príkazom:

```bash
./test.sh <adresár_testov> <cesta_ku_kompilátoru> <cesta_k_interpretu>
```

Parametre:
- <adresár_testov>: Adresár obsahujúci testy. 
- <cesta_ku_kompilátoru>: Cesta k spustiteľnému súboru kompilátora.
- <cesta_k_interpretu>: Cesta k spustiteľnému súboru interpretu.

### Príklad spustenia

Pre štruktúru:

```
projekt/
├── ic24int                 # Interpret
├── compiler                # Komplilátor
└── IFJ24-tests-master/     # Adresár pre testy
    ├── in                  # Vstupné testy
    │   ├── big_test.ifj
    │   ├── test_1.ifj
    │   └── ...             # Ďalšie vstupné testy
    ├── out                 # Výstupy z interpretu
    ├── ref                 # Referenčné výstupy
    │   ├── big_test.ref1
    │   ├── test_1.ref1
    │   └── ...             # Ďalšie referenčné súbory
    └── test.sh             # Testovací skript
```

```bash
cd projekt/
```
```bash
chmod +x ./IFJ24-tests-master/test.sh
```
```bash
./IFJ24-tests-master/test.sh ./IFJ24-tests-master compiler ic24int
```
## Pridanie vlastného testu

### 1. Testovaný program
Vytvor testovací program v jazyku IFJ a vlož ho do zložky in/:

```
in/custom_test.ifj
```

### 2. Vstup pre program
Pridaj vstup pre svoj program. Ak tvoj program nevyžaduje žiadny vstup, môžeš tento krok preskočiť (programu sa automaticky pridelí prázdny súbor na vstup).

Vstupný súbor by mal byť vo formáte:
```
in/custom_test.in*
```
Kde * je číslo vstupu. Ak chceš program spustiť viac krát s rôznymi vstupmi, použiješ rôzne čísla (napr. custom_test.in1, custom_test.in2, atď.).

### 3. Referenčný súbor
Pridaj referenčný súbor podľa ktorého sa bude porovnávať výstup tvojho programu.

Referenčný súbor by mal byť vo formáte:
```
ref/custom_test.ref*
```
Kde * je číslo vstupu. Ak zadáš viac vstupov, použiješ rôzne čísla.

### 4. Kontrola exit kódu programu
Ak chceš testovať aj exit kód, ktorý vráti kompilátor alebo interpret, pridaj súbor obsahujúci požadovaný exit kód.

Ako by mal vyzerať taký súbor:
```
ref/custom_test.exit*
```
Kde * je číslo vstupu s ktorým chceš porovnávať výstup (len v prípade, že zadáš viac vstupov).
### Ak vytvoríš svoje vlastné testy, neváhaj a pošli ich cez pull request (len .ifj, .exit, .ref a prípadne .in súbory) :)
## Štruktúra Projektu


```
IFJ24-tests/
├── in/                  # Adresár so vstupnými súbormi
│   ├── *.ifj            # Zdrojové súbory kódu
│   ├── *.in*            # Vstupné súbory pre testy
│   └── empty.in         # Predvolený prázdny vstupný súbor
├── out/                 # Adresár pre vygenerované súbory
│   ├── *.ifjcode        # Vygenerovaný kód z kompilátora
│   ├── *.out*           # Výstupy z interpretra
├── ref/                 # Adresár s referenčnými výstupmi
│   ├── *.ref*           # Očakávané výstupné súbory
│   └── *.exit           # Očakávané návratové kódy
└── test.sh              # Testovací skript
```

## Prispeli
- tiquis0290
- Sigull

## Autori

- Filip Novák [@fifixsandy] (https://github.com/fifixsandy)
- Ján Skovajsa [@jansko03]
