
# EDA: Rozhlasové vysílání v Česku

## Data
Základem dnešního cvičení jsou data o programu vysílání 3 rozhlasových stanic:
- Rádio Beat,
- Metal Heart Radio,
- Metal Heart Radio – Soft Channel.

Vstupem je soubor ve formátu JSONL:
https://wormscesky.cz/radiohead.jsonl
Pokud se tento soubor pokusíte načíst jako celek pomocí modulu json, nepovede se vám to.
Soubor jako celek totiž není validní JSON, validní JSON je ale každý jeho řádek, soubor
je tedy nutné načíst po řádcích.
Každý řádek obsahuje slovník s následujícími klíči:
- code: zkratka stanice
- station: název stanice
- time: datum a čas přehrání skladby
- title: interpret a název skladby


## Zadání
0) Načtěte soubor do seznamu (list). Ano, už tady uplatníte for cykly. 🙂
1) Zjistěte, kolik skladeb celkem soubor obsahuje.
2) Zjistěte, jaké je zastoupení rádií v tomto souboru (čistě podle počtu skladeb).
3) Zjistěte, kolikrát hrála na Rádiu Beat skupina Accept (pozor, je v tom drobný
    háček). 🎣 😊
4) Uložte do souboru všechna přehrání skladeb skupiny Iron Maiden (kompletní data,
    tzn. včetně stanice i času).
5) BONUS: Očistěte data o jingly a poté znovu proveďte úkoly 1 a 2.
6) 🦸‍♀️ SUPERHERO BONUS: Zjistěte pestrost programu jednotlivých stanic: kolik různých
    interpretů hrálo na jednotlivých stanicích? Doporučuji využít datové typy dict
    a set. Při ukládání interpretů za jednotlivá rádia vám množiny (set) zajistí
    jejich unikátnost. K přidávání prvků do setů slouží metoda add:
    ```
    s = set()
    s.add("a")
    s.add("a")
    s.add("b")
    s.add("a")
    # s == {'b', 'a'}  # všimněte si, že set nijak neřeší pořadí položek!
    ```
