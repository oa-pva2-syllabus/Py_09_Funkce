# PVA2 - Programování a vývoj aplikací
## Cvičení 09: Funkce

### Jak řešit
- Všechny úkoly řešte v souboru `reseni.py`, každou funkci pod komentář s číslem úkolu.
- **Název funkce, parametry i jejich datové typy opište přesně ze zadání.** Podle nich se řešení automaticky vyhodnocuje.
- Každá funkce má typové anotace parametrů i návratové hodnoty, funkce bez `return` má `-> None`.
- Funkce, která počítá, výsledek **vrací** přes `return`. Vypisuje jen tam, kde to zadání výslovně chce.
- Pod funkci si napište volání a výsledek vypište, ať funkci vyzkoušíte.
- Po každém `git push` se řešení vyhodnotí a výsledek najdete v pull requestu **Feedback**.
  Čísla požadavků 1–12 odpovídají číslům úkolů, požadavek 13 kontroluje typové anotace a 14 docstring.

### Definice a volání funkce

#### 1
`pozdrav() -> None`

Funkce vypíše text `Hello world` a nic nevrací.

#### 2
`pozdravKrat(pocet: int) -> None`

Funkce vypíše `Hello world` tolikrát, kolik určuje parametr `pocet`. Uvnitř volejte funkci `pozdrav()` v cyklu.

### Návratová hodnota

#### 3
`druhaMocnina(cislo: int) -> int`

Funkce vrátí druhou mocninu čísla. Vyzkoušejte ji pro čísla 4, 8, 15, 23 a -1.

#### 4
`soucetDvou(a: float, b: float) -> float`

Funkce vrátí součet dvou čísel. Zavolejte ji dvakrát s různými argumenty, oba výsledky sečtěte a součet vypište.

#### 5
`vypocet(a: int, b: int = 2, c: int = 10) -> int`

Funkce vrátí výsledek `a * b + c`. Parametry `b` a `c` jsou nepovinné s výchozími hodnotami 2 a 10.
Například `vypocet(3, 5, 20)` vrátí 35, `vypocet(3, 5)` vrátí 25 a `vypocet(3)` vrátí 16.

#### 6
`jeSude(cislo: int) -> bool`

Funkce vrátí `True`, když je číslo sudé, jinak `False`.

#### 7
`minMax(cisla: list[int]) -> tuple[int, int]`

Funkce vrátí dvojici: nejmenší a největší číslo ze seznamu. Například `minMax([3, 1, 2])` vrátí `(1, 3)`.

### Seznam jako argument

#### 8
`pridejUnikatni(seznam: list[str], prvek: str) -> None`

Funkce přidá prvek do **předaného** seznamu, ale jen pokud v něm ještě není. Nic nevrací.
Vyzkoušejte ji na seznamu `barvy` z `reseni.py`.

#### 9
`bezDuplicit(seznam: list[str]) -> list[str]`

Funkce vrátí **nový** seznam, ve kterém je každý prvek jen jednou, v pořadí prvního výskytu.
Předaný seznam nemění. Například pro `["red", "green", "red", "black"]` vrátí `["red", "green", "black"]`.
Vyzkoušejte ji na seznamu `barvySOpakovanim` z `reseni.py`.

#### 10
`soucetVybranych(cisla: list[int]) -> int`

Funkce vrátí součet čísel ze seznamu, která jsou kladná nebo menší než -10.
Například pro seznam `[-12, -11, -10, -9, 0, 1, 2, 3]` vrátí -17.

Funkci zavolejte pro seznamy `cisla1` a `cisla2` z `reseni.py` a výsledky vypište ve tvaru:

```text
Součet čísel, která jsou kladná, nebo jsou menší než -10 je -17
```

### Rekurze a dokumentace

#### 11
`faktorial(n: int) -> int`

Funkce vrátí faktoriál čísla `n` (`5! = 5 * 4 * 3 * 2 * 1 = 120`). Faktoriál 0 je 1.
Řešit můžete cyklem i rekurzí. Funkci napište i docstring.

#### 12
`hodnotaSlova(slovo: str) -> int`

Funkce vrátí bodovou hodnotu slova podle pravidel:
- písmeno `x` má hodnotu 10 bodů,
- samohlásky (`a e i o u y` i s diakritikou, např. `á é ě í ó ú ů ý`) mají hodnotu 3 body,
- ostatní písmena (souhlásky) mají hodnotu 1 bod,
- ostatní znaky (mezery, číslice, interpunkce) mají hodnotu 0 bodů,
- na velikosti písmen nezáleží.

Například `hodnotaSlova("python")` vrátí 10 a `hodnotaSlova("Xena")` vrátí 17.
