
# IFJ Testovací Skript

Tento skript automatizuje proces testovania IFJ kompilátora a interpretra. Kompiluje zdrojové súbory .ifj, spúšťa vygenerovaný kód cez interpret s rôznymi vstupnými súbormi a porovnáva výsledky s referenčnými výstupmi.





## Spustenie

Skript spustíte príkazom:

```bash
./test.sh <adresár_testov> <cesta_ku_kompilátoru> <cesta_k_interpretru>
```

Parametre:
- <adresár_testov>: Adresár obsahujúci testy. 
- <cesta_ku_kompilátoru>: Cesta k spustiteľnému súboru kompilátora.
- <cesta_k_interpretru>: Cesta k spustiteľnému súboru interpretra.

### Príklad spustenia

Pre štruktúru:

```
projekt/
├── ic24int                 # Interpret
├── compiler                # Komplilátor
└── tests/                  # Adresár pre testy
    ├── in                  # Vstupné testy
    │   ├── big_test.ifj
    │   ├── test_1.ifj
    │   └── ...             # Ďalšie vstupné testy
    ├── out                 # Vystupy z interpretora
    ├── ref                 # Referenčné výstupy
    │   ├── big_test.ref1
    │   ├── test_1.ref1
    │   └── ...             # Ďalšie referenčné súbory
    └── test.sh             # Testovací skript
```

```bash
cd projekt/
./tests/test.sh ./tests compiler ic24int
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
in/custom_test.ifj
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
Kde * je číslo vstupu s ktorým chceš porovnávať výstup (len v prípade, že zadáš viac vstupov).Ak vytvoríš svoje vlastné testy, neváhaj a pošli ich cez pull request. :)
## Štruktúra Projektu


```
projekt/
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
