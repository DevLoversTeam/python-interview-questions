**Read in other languages: [English 🇺🇸](README.en.md),
[Polski 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Ukraiński 🇺🇦](README.md).**

# Python <img src="./assets/python.svg" width="40" height="40" alt="Python logo"/>

## Najpopularniejsze pytania i odpowiedzi rekrutacyjne z Pythona

<details>
<summary>1. Czym jest Python i jakie są jego główne cechy?</summary>

#### Python

**Python** to wysokopoziomowy język ogólnego przeznaczenia, nastawiony na
czytelność, szybki rozwój i rozbudowany standardowy zestaw narzędzi.

Główne cechy:

- **Prosta składnia**: kod łatwo czytać i utrzymywać.
- **Interpretowany model wykonania**: szybki cykl zmian bez ręcznego etapu
  kompilacji.
- **Wieloplatformowość**: ten sam kod działa na Linuxie, macOS i Windowsie.
- **Wieloparadygmatowość**: podejścia proceduralne, OOP i funkcyjne w jednym
  projekcie.
- **Silny ekosystem**: `pip`, `venv`, `pyproject.toml`, tysiące gotowych
  bibliotek.
- **Nowoczesne możliwości Pythona 3.10+**: type hints, `dataclass`,
  `async/await`, `match/case`, generatory, menedżery kontekstu.

Przykład funkcji w stylu production:

```python
from dataclasses import dataclass

@dataclass(slots=True)
class User:
    name: str
    active: bool

def process_users(users: list[User]) -> list[str]:
    return [user.name for user in users if user.active]
```

**W skrócie:**

- Python przyspiesza rozwój dzięki prostej składni i dużej bibliotece
  standardowej.
- Język nadaje się do backendu, automatyzacji, data/ML, testowania i DevOps.
- W Pythonie 3.10+ kluczowe praktyki to adnotacje typów, async I/O i nowoczesna
  biblioteka standardowa.

</details>

<details>
<summary>2. Jakie są kluczowe zalety Pythona?</summary>

#### Python

Kluczowe zalety Pythona w production:

- wysoka szybkość rozwoju dzięki zwięzłej składni;
- duża biblioteka standardowa (`pathlib`, `itertools`, `collections`,
  `asyncio`);
- dojrzały ekosystem pakietów dla backendu, data, automatyzacji i testowania;
- przenośność kodu między systemami operacyjnymi;
- dobre wsparcie dla typowania (`typing`, `mypy`, `pyright`) i nowoczesnych
  praktyk.

**W skrócie:**

- Python skraca time-to-market.
- Daje wiele gotowych narzędzi bez dodatkowych zależności.
- Nadaje się zarówno do MVP, jak i do skalowalnych serwisów.

</details>

<details>
<summary>3. Czym Python różni się od języków kompilowanych?</summary>

#### Python

Python zwykle jest wykonywany przez interpreter: kod jest kompilowany do
bajtkodu i uruchamiany w czasie wykonania (CPython VM). W językach kompilowanych
(C/C++, Rust) zazwyczaj występuje wcześniejsza kompilacja do kodu maszynowego.

Praktyczne konsekwencje:

- Python jest szybszy w rozwoju i prototypowaniu.
- Natywnie kompilowane języki są zwykle szybsze w zadaniach CPU-bound.
- W Pythonie wydajność często poprawia się algorytmami, profilowaniem i
  rozszerzeniami C.

**W skrócie:**

- Python optymalizuje szybkość rozwoju.
- Kompilacja do kodu maszynowego zwykle daje lepszą surową wydajność.
- Wybór zależy od domeny i wymagań dotyczących opóźnień oraz przepustowości.

</details>

<details>
<summary>4. Co oznacza dynamiczne typowanie w Pythonie?</summary>

#### Python

Dynamiczne typowanie oznacza, że typ jest przypisany do obiektu, a nie do nazwy
zmiennej. Nazwa może wskazywać na wartości różnych typów w różnym czasie
wykonania.

```python
value = 10        # int
value = "10"      # str
```

Typy są sprawdzane podczas wykonania, dlatego błędy typów pojawiają się w
w czasie wykonania, jeśli nie używa się statycznego analizatora typów.

**W skrócie:**

- W Pythonie typ ma obiekt, a nie zmienna.
- Typ może się zmieniać przy ponownym przypisaniu nazwy.
- Type hints dodają kontrolę przed uruchomieniem kodu.

</details>

<details>
<summary>5. Co oznacza strong typing w Pythonie?</summary>

#### Python

Strong typing w Pythonie oznacza, że interpreter nie wykonuje niebezpiecznych,
niejawnych konwersji między niezgodnymi typami.

```python
1 + "2"  # TypeError
```

Dla operacji na różnych typach potrzebne jest jawne rzutowanie:

```python
1 + int("2")  # 3
```

**W skrócie:**

- Python jest dynamicznie typowany, ale rygorystyczny pod względem zgodności
  typów.
- Niebezpieczne niejawne konwersje są blokowane błędem.
- Jawne rzutowanie czyni zachowanie przewidywalnym.

</details>

<details>
<summary>6. Czym jest REPL i kiedy się go używa?</summary>

#### Python

REPL (Read-Eval-Print Loop) to tryb interaktywny, w którym wpisujesz wyrażenie,
natychmiast otrzymujesz wynik i szybko weryfikujesz hipotezy.

Zastosowania:

- sprawdzenie API biblioteki;
- szybkie przetestowanie wyrażenia lub algorytmu;
- zbadanie danych przed implementacją w module.

Narzędzia: standardowy `python`, `ipython`, `ptpython`.

**W skrócie:**

- REPL daje najszybszą pętlę feedbacku.
- Jest wygodny do eksperymentów i debugowania.
- Nie zastępuje testów, ale skraca czas sprawdzania pomysłów.

</details>

<details>
<summary>7. Czym są literały w Pythonie? Podaj przykłady różnych typów literałów.</summary>

#### Python

Literał to stała wartość zapisana bezpośrednio w kodzie.

```python
name = "Ada"                  # str literal
count = 42                    # int literal
ratio = 3.14                  # float literal
enabled = True                # bool literal
items = [1, 2, 3]             # list literal
config = {"retries": 3}       # dict literal
flags = {"a", "b"}            # set literal
point = (10, 20)              # tuple literal
raw = b"abc"                  # bytes literal
```

**W skrócie:**

- Literały to wbudowane stałe wartości w kodzie.
- Każdy podstawowy typ ma własną składnię literału.
- Są często używane do inicjalizacji danych.

</details>

<details>
<summary>8. Czym są keywords w Pythonie?</summary>

#### Python

Keywords to zarezerwowane słowa języka, które mają specjalne znaczenie
składniowe i nie mogą być nazwami zmiennych.

Przykłady: `if`, `for`, `class`, `def`, `match`, `case`, `try`, `except`,
`async`, `await`.

Listę można sprawdzić:

```python
import keyword
print(keyword.kwlist)
```

**W skrócie:**

- Keywords tworzą składnię Pythona.
- Nie można ich używać jako identyfikatorów.
- Lista jest dostępna przez moduł `keyword`.

</details>

<details>
<summary>9. Czym jest zmienna w Pythonie?</summary>

#### Python

Zmienna w Pythonie to nazwa (reference), która wskazuje na obiekt w pamięci.
Przypisanie wiąże nazwę z obiektem, a nie „wkłada wartość do pudełka”.

```python
x = [1, 2]
y = x
y.append(3)
# x i y wskazują na tę samą listę
```

**W skrócie:**

- Zmienna jest referencją do obiektu.
- Kilka nazw może wskazywać na ten sam mutable object.
- To ważne dla zrozumienia kopiowania i efektów ubocznych.

</details>

<details>
<summary>10. Czym są `pass` i `...` (Ellipsis) w Pythonie?</summary>

#### Python

`pass` to instrukcja-zagłuszka: nic nie robi, ale pozwala zapisać poprawny
składniowo pusty blok.

`...` (Ellipsis) to osobny obiekt `Ellipsis`. Często jest używany jako znacznik
„jeszcze niezaimplementowane”, w type hints i bibliotekach, na przykład NumPy.

```python
def feature() -> None:
    pass

PLACEHOLDER = ...
```

**W skrócie:**

- `pass` jest przydatny w pustych blokach kodu.
- `...` jest wartością-obiektem, a nie słowem kluczowym.
- Oba są używane jako tymczasowe zagłuszki, ale mają różną semantykę.

</details>

<details>
<summary>11. Czym jest PEP i jak wpływa na rozwój Pythona?</summary>

#### Python

PEP (Python Enhancement Proposal) to oficjalny dokument opisujący nową funkcję,
standard lub proces w ekosystemie Pythona.

Przez PEP przechodzą:

- dyskusja nad projektem;
- argumentacja techniczna;
- decyzja o przyjęciu lub odrzuceniu;
- standaryzacja praktyk.

Przykłady: PEP 8 (styl), PEP 484 (type hints), PEP 634 (pattern matching).

**W skrócie:**

- PEP to mechanizm ewolucji języka i narzędzi.
- Sprawia, że zmiany są przejrzyste i sformalizowane.
- Wiele współczesnych praktyk w Pythonie zostało utrwalonych właśnie przez PEP.

</details>

<details>
<summary>12. Czym jest PEP 8 i po co jest potrzebny?</summary>

#### Python

PEP 8 to oficjalny przewodnik po stylu kodu Pythona: nazewnictwo,
formatowanie, wcięcia, importy, długość linii i czytelność konstrukcji.

Dlaczego jest potrzebny:

- kod ma jednolity styl w zespole;
- code review przebiega szybciej;
- jest mniej szumu w diffie;
- rośnie maintainability.

W praktyce styl automatyzuje się przez `ruff format` albo `black` + `ruff`.

**W skrócie:**

- PEP 8 standaryzuje styl kodu Pythona.
- Chodzi o czytelność i utrzymanie, a nie o wydajność.
- Przestrzeganie zasad najlepiej automatyzować narzędziami.

</details>

<details>
<summary>13. Jakie nowe możliwości pojawiły się we współczesnych wersjach Pythona (3.10+)?</summary>

#### Python

Kluczowe możliwości współczesnego Pythona:

- `match/case` (structural pattern matching);
- ulepszona składnia i komunikaty o błędach;
- typy union przez `|` (`int | None`);
- `typing.Self`, `typing.TypeAlias`, `typing.override`;
- generics w stylu PEP 695 (`class Box[T]: ...`, `def f[T](...) -> ...`);
- `tomllib` w bibliotece standardowej.

W praktyce zmniejsza to boilerplate i poprawia niezawodność typowanego kodu.

**W skrócie:**

- Python 3.10+ znacząco poprawił składnię i typing.
- `match/case` i nowoczesny `typing` mają najbardziej zauważalny wpływ na kod.
- Nowych funkcji warto domyślnie używać w nowym kodzie.

</details>

<details>
<summary>14. Czym jest docstring w Pythonie?</summary>

#### Python

Docstring to łańcuch dokumentacyjny, pierwszy wyrażenie w module, klasie lub
funkcji. Jest dostępny przez `__doc__` i używany przez IDE, `help()` oraz
generatory dokumentacji.

```python
def normalize_email(email: str) -> str:
    """Return lowercase email without surrounding spaces."""
    return email.strip().lower()
```

Zaleca się opisywać: co robi funkcja, argumenty, wartość zwracaną i wyjątki.

**W skrócie:**

- Docstring to wbudowana dokumentacja w kodzie.
- Działa jako źródło dla `help()` i automatycznego generowania dokumentacji.
- Dobry docstring zmniejsza potrzebę czytania implementacji.

</details>

<details>
<summary>15. Jak działają wcięcia (indentation) w Pythonie?</summary>

#### Python

W Pythonie wcięcia definiują bloki kodu (ciało `if`, `for`, `def`, `class`).
Oznacza to, że wcięcie jest częścią składni, a nie tylko stylem.

```python
if is_ready:
    run_task()
else:
    stop_task()
```

Mieszanie tabów i spacji może prowadzić do `IndentationError` albo niepoprawnej
struktury bloku.

**W skrócie:**

- Wcięcie w Pythonie definiuje strukturę programu.
- Nieprawidłowe wcięcie psuje wykonanie.
- Używaj spójnego stylu, najlepiej 4 spacji.

</details>

<details>
<summary>16. Ile spacji należy stosować do wcięcia zgodnie z PEP 8 i dlaczego ważne jest zachowanie jednolitych wcięć?</summary>

#### Python

PEP 8 zaleca **4 spacje** na jeden poziom wcięcia.

Dlaczego to istotne:

- jednolita struktura bloków w całym projekcie;
- przewidywalny wygląd w różnych edytorach;
- mniej błędów przez konflikty tab/spacja;
- czytelniejszy diff w Git.

**W skrócie:**

- Standardowe wcięcie to 4 spacje.
- Jeden styl eliminuje całą klasę błędów formatowania.
- Bezpośrednio poprawia to czytelność i utrzymanie kodu.

</details>

<details>
<summary>17. Jaka jest różnica między `ruff` a `black` pod względem funkcjonalności i użycia?</summary>

#### Python

`black` to formatter kodu o stałych regułach.

`ruff` to szybki linter, a także formatter i auto-fixer wielu reguł (PEP 8,
importy, potencjalne bugi, uproszczenia składni).

Praktyczne podejścia:

- albo `ruff check --fix` + `ruff format`;
- albo `ruff` do lintu + `black` do formatowania.

**W skrócie:**

- `black` koncentruje się na formatowaniu.
- `ruff` pokrywa linting i część automatycznych poprawek.
- W nowoczesnych projektach często wystarcza sam `ruff`.

</details>

<details>
<summary>18. Wyjaśnij przeznaczenie type annotations w Pythonie i podaj przykład funkcji z type annotations.</summary>

#### Python

Type annotations opisują oczekiwane typy argumentów i wartości zwracanej.
Poprawiają autouzupełnianie, analizę statyczną i czytelność API.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Adnotacje same w sobie nie wykonują walidacji w czasie działania, ale pomagają wykrywać
błędy na etapie CI przez `mypy` lub `pyright`.

**W skrócie:**

- Type hints dokumentują kontrakt funkcji.
- Dają wczesne wykrywanie błędów przez static checking.
- Podnoszą jakość API w dużych codebase'ach.

</details>

<details>
<summary>19. Czym jest debugging i dlaczego to ważna umiejętność dla programistów?</summary>

#### Python

Debugging to systematyczne szukanie przyczyny niepoprawnego zachowania kodu i
jej usuwanie. To nie tylko „znaleźć buga”, ale odtworzyć go, zlokalizować i
zweryfikować fix.

Podstawowy cykl:

- odtworzyć problem;
- zawęzić obszar kodu;
- sprawdzić hipotezę logami lub debuggerem;
- dodać test, który utrwala scenariusz.

**W skrócie:**

- Debugging zmniejsza MTTR i liczbę regresji.
- Działa najlepiej jako proces, a nie chaotyczne szukanie.
- Zakończenie debugowania to: fix + test + dodatkowa weryfikacja.

</details>

<details>
<summary>20. Wyjaśnij, do czego służy używanie funkcji `print` do debugowania. Podaj przykład sytuacji, w której to podejście jest przydatne.</summary>

#### Python

`print`-debugging to szybki sposób na sprawdzenie wartości zmiennych i
kolejności wykonania bez uruchamiania bardziej złożonych narzędzi.

Jest przydatny, gdy trzeba szybko sprawdzić hipotezę w lokalnym skrypcie:

```python
def parse_port(raw: str) -> int:
    value = raw.strip()
    print(f"raw={raw!r} value={value!r}")
    return int(value)
```

Dla kodu produkcyjnego lepiej przejść na `logging`, aby mieć poziomy logów i
kontrolowane wyjście.

**W skrócie:**

- `print` nadaje się do krótkiej, lokalnej diagnostyki.
- Szybko pokazuje stan zmiennych w problematycznym miejscu.
- Do stabilnej diagnostyki w serwisie używaj `logging`.

</details>

<details>
<summary>21. Opisz, jak można używać Python Debugger (PDB) do debugowania. Jakie zalety ma PDB w porównaniu z `print`?</summary>

#### Python

`pdb` pozwala zatrzymywać wykonanie programu, przechodzić po liniach,
sprawdzać stan zmiennych i stos wywołań.

Podstawowe użycie:

```python
import pdb

def compute(x: int) -> int:
    pdb.set_trace()
    return x * 2
```

Kluczowe komendy: `n` (next), `s` (step), `c` (continue), `p expr`
(print expr), `l` (list), `bt` (backtrace).

**W skrócie:**

- `pdb` daje interaktywną kontrolę nad wykonaniem.
- Jest skuteczniejszy niż `print` w bardziej złożonych scenariuszach.
- Pozwala diagnozować stan bez zaśmiecania kodu logami.

</details>

<details>
<summary>22. Jakie strategie można stosować do debugowania pętli i funkcji w Pythonie?</summary>

#### Python

Praktyczne strategie:

- zlokalizować błąd przez minimalny odtwarzalny przykład;
- logować niezmienniki podczas iteracji pętli;
- ustawiać breakpoint na wejściu i wyjściu z funkcji;
- sprawdzać przypadki brzegowe (puste dane, `None`, duże wolumeny);
- pokrywać problematyczną ścieżkę testem.

Dla pętli warto logować indeks i kluczowe stany pośrednie.

**W skrócie:**

- Zaczynaj od odtworzenia i zawężenia problemu.
- Sprawdzaj niezmienniki i warunki brzegowe.
- Kończ fixem i testem, który łapie regresję.

</details>

<details>
<summary>23. Jaki wpływ mają długotrwałe funkcje na wydajność programu?</summary>

#### Python

Długotrwałe funkcje zwiększają latency, blokują workery lub wątki i pogarszają
przepustowość serwisu.

Ryzyka:

- wolne odpowiedzi API;
- timeouty;
- wzrost kolejek zadań;
- gorsze wykorzystanie CPU i I/O.

Podejście: profilować (`cProfile`), rozbijać na mniejsze kroki, używać
generatorów i przetwarzania strumieniowego, wynosić ciężkie obliczenia do `multiprocessing` albo
do tła.

**W skrócie:**

- Długie funkcje bezpośrednio uderzają w latency.
- Optymalizację opiera się na profilowaniu, a nie na intuicji.
- Architektonicznie lepiej rozdzielać pracę CPU-bound i I/O-bound.

</details>

<details>
<summary>24. Czym jest logging i dlaczego lepiej używać go zamiast `print`?</summary>

#### Python

`logging` to standardowy mechanizm rejestrowania zdarzeń z poziomami
(`DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL`), formatami i handlerami
(console, file).

Dlaczego jest lepszy od `print`:

- kontrolowane poziomy szczegółowości;
- ustrukturyzowany format;
- scentralizowana konfiguracja;
- możliwość integracji ze stackiem observability.

**W skrócie:**

- `logging` nadaje się do produkcji, `print` nie.
- Poziomy logów dają kontrolę nad szumem.
- Logi powinny być ustrukturyzowane i spójne.

</details>

<details>
<summary>25. Czym jest traceback?</summary>

#### Python

Traceback to stos wywołań, który Python pokazuje przy wyjątku: gdzie wykonanie
się zaczęło, przez jakie funkcje przeszedł kod i gdzie dokładnie wystąpił błąd.

Zastosowanie:

- szybko znaleźć plik i linię źródła błędu;
- zrozumieć ścieżkę wykonania do awarii;
- zbudować dokładny test odtwarzający problem.

**W skrócie:**

- Traceback to „trasa” do błędu.
- Najcenniejsza część to ostatnie klatki stosu i typ wyjątku.
- Analiza tracebacku przyspiesza znalezienie root cause.

</details>

<details>
<summary>26. Jakie podstawowe typy danych istnieją w Pythonie?</summary>

#### Python

Podstawowe typy built-in:

- liczbowe: `int`, `float`, `complex`;
- logiczny: `bool`;
- tekstowe i bajtowe: `str`, `bytes`, `bytearray`;
- kolekcje: `list`, `tuple`, `set`, `dict`, `frozenset`;
- specjalne: `NoneType` (`None`).

Ważne jest rozumienie mutability:

- mutable: `list`, `dict`, `set`, `bytearray`;
- immutable: `int`, `str`, `tuple`, `frozenset`.

**W skrócie:**

- Python ma bogaty zestaw podstawowych typów „out of the box”.
- Wybór struktury danych wpływa na złożoność operacji.
- Mutability określa zachowanie kopiowania i efekty uboczne.

</details>

<details>
<summary>27. Jaka jest różnica między zwykłym dzieleniem (`/`) a dzieleniem całkowitym (`//`) w Pythonie?</summary>

#### Python

`/` wykonuje zwykłe dzielenie i zawsze zwraca `float`.

`//` wykonuje dzielenie floor: zwraca część całkowitą zaokrągloną w dół
(do `-∞`), a typem przy całkowitych operandach jest zwykle `int`.

```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

**W skrócie:**

- `/` -> wynik rzeczywisty.
- `//` -> zaokrąglenie w dół do liczby całkowitej.
- Dla liczb ujemnych `//` nie jest równoważne „ucięciu do zera”.

</details>

<details>
<summary>28. Wyjaśnij użycie operatora modulo (`%`) w Pythonie. Jak można go użyć, aby określić, czy liczba jest parzysta czy nieparzysta?</summary>

#### Python

Operator `%` zwraca resztę z dzielenia.

Sprawdzenie parzystości:

```python
def is_even(n: int) -> bool:
    return n % 2 == 0
```

Jeśli `n % 2 == 0`, liczba jest parzysta, w przeciwnym razie nieparzysta.

Typowe zadania: indeksy cykliczne, podział na grupy, obliczenia kalendarzowe.

**W skrócie:**

- `%` zwraca remainder.
- `n % 2` to standardowy test parzystości.
- Często jest używany do logiki cyklicznej.

</details>

<details>
<summary>29. Jak Python pracuje z dużymi liczbami całkowitymi i jakie są ograniczenia przy pracy z bardzo dużymi liczbami?</summary>

#### Python

`int` w Pythonie ma dowolną precyzję (arbitrary precision), czyli nie jest
ograniczony do 32 lub 64 bitów jak w wielu innych językach.

Ograniczenia są praktyczne:

- pamięć procesu;
- czas obliczeń dla bardzo dużych wartości;
- koszt operacji rośnie wraz ze wzrostem liczby cyfr.

**W skrócie:**

- Nie ma klasycznego przepełnienia `int`.
- Ograniczeniem są zasoby maszyny, a nie stały rozmiar bitowy.
- Przy dużych obliczeniach kluczowe są algorytmy i profilowanie.

</details>

<details>
<summary>30. Jakie znaczenie ma obsługa dzielenia przez zero w Pythonie i jak zapobiec `ZeroDivisionError` w kodzie?</summary>

#### Python

Dzielenie przez zero powoduje `ZeroDivisionError`. Trzeba to obsługiwać jawnie,
jeśli dzielnik pochodzi z wejścia zewnętrznego albo jest obliczany dynamicznie.

```python
def safe_div(a: float, b: float) -> float | None:
    if b == 0:
        return None
    return a / b
```

W krytycznych scenariuszach używaj `try/except` oraz logowania kontekstu.

**W skrócie:**

- Dzielenie przez zero to kontrolowany błąd czasu wykonania.
- Najprostsza ochrona to sprawdzenie dzielnika przed operacją.
- Dla danych zewnętrznych dodawaj zabezpieczenia i diagnostykę.

</details>

<details>
<summary>31. Opisz użycie modułu `random` w Pythonie. Jakie są najczęściej używane funkcje tego modułu?</summary>

#### Python

`random` jest używany do pseudolosowych wartości w symulacjach, danych
testowych i zadaniach non-crypto.

Popularne funkcje:

- `random()` — liczba z przedziału `[0.0, 1.0)`;
- `randint(a, b)` — liczba całkowita z zakresu;
- `randrange(start, stop, step)` — jak range, ale losowy element;
- `choice(seq)` / `choices(seq, k=...)`;
- `shuffle(list_)` — tasuje listę in-place;
- `sample(population, k)` — unikalna próbka.

Dla kryptografii używaj `secrets`, a nie `random`.

**W skrócie:**

- `random` nadaje się do zwykłej, aplikacyjnej losowości.
- Najczęściej używa się `randint`, `choice`, `shuffle`, `sample`.
- Do zadań security-sensitive potrzebny jest `secrets`.

</details>

<details>
<summary>32. Jak pracować w Pythonie z liczbami o lepszej precyzji?</summary>

#### Python

Dla finansowych i dokładnych obliczeń dziesiętnych używaj `decimal.Decimal`,
a nie `float`.

```python
from decimal import Decimal

total = Decimal("0.1") + Decimal("0.2")  # Decimal('0.3')
```

Dla liczb wymiernych przydatny jest `fractions.Fraction`.

**W skrócie:**

- `float` jest wygodny, ale ma błędy reprezentacji binarnej.
- Do dokładnej arytmetyki dziesiętnej wybieraj `Decimal`.
- Typ liczby powinien odpowiadać domenie problemu.

</details>

<details>
<summary>33. Czym są znaki escape w stringach Pythona i jak się ich używa? Podaj przykłady dla `\n`, `\t`, `\r`, `\"` i `\'`.</summary>

#### Python

Sekwencje escape to specjalne kombinacje z `\`, które kodują znaki specjalne
wewnątrz stringa.

- `\n` — nowa linia
- `\t` — tabulacja
- `\r` — powrót karetki
- `\"` — cudzysłów w stringu z `"`
- `\'` — apostrof w stringu z `'`

```python
text = "A\tB\n\"quoted\"\nI\'m here\rX"
```

**W skrócie:**

- Znaki escape sterują formatowaniem stringa.
- Pozwalają wstawiać cudzysłowy bez łamania składni.
- Dla ścieżek i regexów często wygodnie używać raw stringów `r"..."`.

</details>

<details>
<summary>34. Wyjaśnij użycie metod `strip`, `lstrip` i `rstrip` w Pythonie. Czym się różnią?</summary>

#### Python

Metody działają na brzegach stringa:

- `strip()` — usuwa znaki z obu stron;
- `lstrip()` — tylko z lewej;
- `rstrip()` — tylko z prawej.

Domyślnie usuwają whitespace albo konkretny zestaw znaków:

```python
"  hello  ".strip()      # "hello"
"--id--".strip("-")      # "id"
```

**W skrócie:**

- Rodzina `strip` nie zmienia stringa in-place, tylko zwraca nowy.
- Różnica dotyczy wyłącznie strony czyszczenia.
- Często jest używana na danych wejściowych.

</details>

<details>
<summary>35. Opisz przeznaczenie metody `count` w stringach. Jak działa?</summary>

#### Python

`str.count(sub[, start[, end]])` liczy liczbę niepokrywających się wystąpień
podciągu `sub` w wybranym zakresie.

```python
"banana".count("an")      # 2
"banana".count("a", 2)    # 2
```

Zwraca `0`, jeśli nie ma żadnych wystąpień.

**W skrócie:**

- `count` szybko zwraca liczbę wystąpień podciągu.
- Obsługuje ograniczenie wyszukiwania przez `start/end`.
- Liczy niepokrywające się wystąpienia.

</details>

<details>
<summary>36. Jak działa metoda `join` w Pythonie i do czego najczęściej się jej używa?</summary>

#### Python

`sep.join(iterable)` łączy sekwencję stringów w jeden string przy użyciu
separatora `sep`.

```python
names = ["Ada", "Linus", "Guido"]
result = ", ".join(names)  # "Ada, Linus, Guido"
```

Typowe zastosowania: tworzenie linii podobnych do CSV, logów, fragmentów SQL,
ścieżek URL i komunikatów.

**W skrócie:**

- `join` to standardowy i szybki sposób łączenia stringów.
- Wywołuje się go na separatorze, a nie na liście.
- Jest wydajniejszy niż wielokrotne `+=` w pętli.

</details>

<details>
<summary>37. Czym jest slicing w Pythonie i jak za jego pomocą pobierać podciągi? Podaj przykłady z dodatnimi i ujemnymi indeksami.</summary>

#### Python

Slicing to wybór fragmentu sekwencji przez `[start:stop:step]`.

```python
s = "python"
s[1:4]     # "yth"
s[:2]      # "py"
s[-3:]     # "hon"
s[::-1]    # "nohtyp"
```

`start` jest włączony, `stop` nie jest włączony.

**W skrócie:**

- Slicing działa dla stringów, list i krotek.
- Ujemne indeksy są liczone od końca.
- To podstawowe narzędzie obróbki sekwencji bez pętli.

</details>

<details>
<summary>38. Wyjaśnij metodę `replace` dla stringów. Jak za jej pomocą zamienić kilka wystąpień podciągu?</summary>

#### Python

`str.replace(old, new, count=-1)` zwraca nowy string, w którym `old` został
zamieniony na `new`. Domyślnie zamieniane są wszystkie wystąpienia.

```python
"foo bar foo".replace("foo", "baz")      # "baz bar baz"
"foo bar foo".replace("foo", "baz", 1)   # "baz bar foo"
```

**W skrócie:**

- `replace` nie zmienia stringa in-place.
- Bez `count` zamienia wszystkie wystąpienia.
- `count` pozwala kontrolować liczbę zamian.

</details>

<details>
<summary>39. Jak działa metoda `split` w stringach?</summary>

#### Python

`split(sep=None, maxsplit=-1)` dzieli string na listę podciągów.

- bez `sep` dzieli po dowolnych białych znakach;
- z `sep` dzieli po konkretnym separatorze;
- `maxsplit` ogranicza liczbę podziałów.

```python
"a,b,c".split(",")         # ["a", "b", "c"]
"a b   c".split()          # ["a", "b", "c"]
"k=v=x".split("=", 1)      # ["k", "v=x"]
```

**W skrócie:**

- `split` zamienia string na listę tokenów.
- `sep=None` ma specjalne zachowanie dla whitespace.
- `maxsplit` jest przydatny przy parsowaniu formatów key/value.

</details>

<details>
<summary>40. Jak działa konwersja typów (type casting)?</summary>

#### Python

Type casting to jawna konwersja wartości między typami przez konstruktory:
`int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`, `set()`, `dict()`.

```python
age = int("42")
price = float("19.99")
text = str(10)
```

Niepoprawne dane powodują wyjątek (`ValueError`, `TypeError`), dlatego dla
wejścia zewnętrznego potrzebna jest walidacja.

**W skrócie:**

- Python udostępnia jawne funkcje konwersji typów.
- Nie wszystkie wartości można bezpiecznie skonwertować.
- Dla user input potrzebne są walidacja i obsługa wyjątków.

</details>

<details>
<summary>41. Jak Python automatycznie konwertuje różne typy danych na wartości boolean?</summary>

#### Python

W kontekście boolean Python stosuje reguły truthiness.

Wartości podobne do `False`:

- `False`, `None`;
- liczby zerowe: `0`, `0.0`, `0j`;
- puste kolekcje: `""`, `[]`, `{}`, `set()`, `tuple()`, `range(0)`.

Wszystko inne jest zwykle `True`.

```python
bool([])      # False
bool("0")     # True
```

**W skrócie:**

- Konwersja boolean opiera się na regułach truthy/falsy.
- Puste i zerowe -> `False`.
- Niepusty string `"0"` nadal jest `True`.

</details>

<details>
<summary>42. Wyjaśnij, jak zamienić string na liczbę całkowitą albo zmiennoprzecinkową w Pythonie. Co się stanie, jeśli stringa nie da się przekonwertować na liczbę?</summary>

#### Python

Do konwersji używaj `int()` i `float()`:

```python
count = int("42")
ratio = float("3.14")
```

Jeśli string jest niepoprawny, Python zgłasza `ValueError`.

```python
def parse_int(value: str) -> int | None:
    try:
        return int(value)
    except ValueError:
        return None
```

**W skrócie:**

- `int()` i `float()` wykonują jawną konwersję ze stringa.
- Nieprawidłowy format -> `ValueError`.
- Dla danych zewnętrznych potrzebny jest `try/except`.

</details>

<details>
<summary>43. Co robi Python przy porównywaniu różnych typów danych, takich jak liczby całkowite i zmiennoprzecinkowe albo liczby całkowite i boolean?</summary>

#### Python

Python pozwala na porównania liczbowe zgodnych typów numeric.

- `int` i `float` są porównywane według wartości.
- `bool` jest podklasą `int`: `False == 0`, `True == 1`.

```python
1 == 1.0      # True
True == 1     # True
False < 1     # True
```

Dla niezgodnych typów, na przykład `int` i `str`, porównanie porządku (`<`,
`>`) powoduje `TypeError`.

**W skrócie:**

- `int`, `float` i `bool` mają wspólną semantykę numeric.
- `bool` zachowuje się jak `0/1` w porównaniach.
- Niezgodne typy nie są porównywane operatorami porządku.

</details>

<details>
<summary>44. Jak Python obsługuje porównania między listami a set?</summary>

#### Python

`list` i `set` to różne typy o różnej semantyce, dlatego bezpośrednie
porównanie porządku między nimi nie jest wspierane.

```python
[1, 2] == {1, 2}   # False
[1, 2] < {1, 2}    # TypeError
```

Jeśli trzeba porównać skład elementów, najpierw ujednolić typ:

```python
set([1, 2]) == {1, 2}  # True
```

**W skrócie:**

- `list` i `set` są porównywane jako różne struktury danych.
- `==` między nimi zwykle daje `False`.
- Aby porównać sensownie zawartość, najpierw sprowadź do jednego typu.

</details>

<details>
<summary>45. Opisz użycie funkcji `bool()` w Pythonie.</summary>

#### Python

`bool(x)` zwraca wartość boolean dla `x` zgodnie z regułami truthiness.

Typowe scenariusze:

- jawna konwersja wartości do `True/False`;
- czytelne warunki;
- budowanie filtrów.

```python
bool("text")   # True
bool("")       # False
bool(0)        # False
```

**W skrócie:**

- `bool()` ujednolica sprawdzenie „puste/niepuste”.
- Opiera się na wbudowanych regułach truthy/falsy.
- Jest przydatne w walidacji i logice warunkowej.

</details>

<details>
<summary>46. Jaka jest różnica między `list` a `tuple`?</summary>

#### Python

Główna różnica: `list` jest mutable, a `tuple` immutable.

Praktyczne konsekwencje:

- `list` nadaje się do danych, które się zmieniają;
- `tuple` nadaje się do stałych rekordów;
- `tuple` można używać jako klucza słownika, jeśli jego elementy są hashowalne.

```python
coords: tuple[float, float] = (50.45, 30.52)
queue: list[str] = ["task-1", "task-2"]
```

**W skrócie:**

- `list` służy do zmiennych kolekcji.
- `tuple` służy do niezmiennych struktur danych.
- Wybór wpływa na bezpieczeństwo API i użycie w `dict/set`.

</details>

<details>
<summary>47. Jak można utworzyć `tuple`?</summary>

#### Python

Podstawowe sposoby:

```python
t1 = (1, 2, 3)
t2 = 1, 2, 3
t3 = tuple([1, 2, 3])
single = (42,)     # ważny przecinek
empty = ()
```

Dla jednego elementu przecinek jest obowiązkowy, inaczej to tylko wyrażenie w
nawiasach.

**W skrócie:**

- `tuple` tworzy się przez literał albo `tuple(iterable)`.
- `single = (x,)` to poprawny jednoelementowy tuple.
- Pusty tuple: `()`.

</details>

<details>
<summary>48. Jaka jest różnica między metodą `reverse` a slicingiem `[::-1]` przy odwracaniu listy?</summary>

#### Python

`list.reverse()` zmienia istniejącą listę in-place i zwraca `None`.

`lst[::-1]` tworzy nową odwróconą listę, czyli kopię.

```python
values = [1, 2, 3]
values.reverse()      # values -> [3, 2, 1]

other = values[::-1]  # nowa lista
```

**W skrócie:**

- `reverse()` zmienia oryginał.
- `[::-1]` zwraca nowy obiekt.
- Wybór zależy od potrzeby zachowania danych wejściowych.

</details>

<details>
<summary>49. Wyjaśnij przeznaczenie i użycie metody `sort` dla list. Jak posortować listę w porządku malejącym?</summary>

#### Python

`list.sort()` sortuje listę in-place. Obsługuje parametry:

- `key` — funkcja klucza sortowania;
- `reverse=True` — porządek malejący.

```python
nums = [5, 1, 7]
nums.sort(reverse=True)  # [7, 5, 1]
```

Jeśli potrzebna jest nowa, posortowana kopia, użyj `sorted(iterable)`.

**W skrócie:**

- `sort()` zmienia listę na miejscu.
- Dla porządku malejącego użyj `reverse=True`.
- `sorted()` jest wygodne, gdy trzeba zachować oryginał.

</details>

<details>
<summary>50. Jaka jest różnica między metodą `copy` a bezpośrednim przypisaniem jednej listy do drugiej? Dlaczego czasem ważne jest użycie `copy`?</summary>

#### Python

Przypisanie kopiuje tylko referencję:

```python
a = [1, 2]
b = a
b.append(3)   # a też się zmieni
```

`a.copy()` tworzy nową, płytką listę:

```python
a = [1, 2]
b = a.copy()
b.append(3)   # a się nie zmieni
```

Dla struktur zagnieżdżonych może być potrzebne `copy.deepcopy`.

**W skrócie:**

- `=` nie kopiuje danych, tylko współdzieli jeden obiekt między zmiennymi.
- `copy()` izoluje zmiany na poziomie listy zewnętrznej.
- Dla obiektów zagnieżdżonych używaj `deepcopy`.

</details>

<details>
<summary>51. Co robi metoda `pop` w liście? Czym różni się jej zachowanie, jeśli podać indeks, a jeśli nie?</summary>

#### Python

`pop()` usuwa i zwraca element z listy.

- `pop()` bez argumentów usuwa ostatni element;
- `pop(i)` usuwa element o indeksie `i`.

```python
items = ["a", "b", "c"]
last = items.pop()     # "c"
first = items.pop(0)   # "a"
```

Błędny indeks powoduje `IndexError`.

**W skrócie:**

- `pop` łączy usunięcie elementu z jego zwróceniem.
- Bez indeksu działa na końcu listy.
- Z indeksem usuwa konkretną pozycję.

</details>

<details>
<summary>52. Jak połączyć dwie listy w Pythonie za pomocą operatora `+` i metody `extend`? Jaka jest kluczowa różnica między tymi dwoma sposobami?</summary>

#### Python

`a + b` tworzy **nową** listę, a `a.extend(b)` modyfikuje listę `a`
**in-place**.

```python
a = [1, 2]
b = [3, 4]

c = a + b         # [1, 2, 3, 4], a się nie zmieniło
a.extend(b)       # a -> [1, 2, 3, 4]
```

**W skrócie:**

- `+` zwraca nowy obiekt.
- `extend()` mutuje istniejącą listę.
- Wybór zależy od tego, czy trzeba zachować oryginał.

</details>

<details>
<summary>53. Do czego służą funkcje `min`, `max`, `sum`, `all`, `any` w kontekście list?</summary>

#### Python

To podstawowe agregatory dla iterowalnych kolekcji:

- `min()` / `max()` — minimum i maksimum;
- `sum()` — suma liczb;
- `all()` — `True`, jeśli wszystkie elementy są truthy;
- `any()` — `True`, jeśli przynajmniej jeden element jest truthy.

```python
nums = [3, 10, 1]
min(nums), max(nums), sum(nums)  # (1, 10, 14)
all([True, 1, "x"])              # True
any([0, "", None, 5])            # True
```

**W skrócie:**

- Funkcje zmniejszają ilość boilerplate w pętlach.
- Działają z dowolnym iterable.
- Dobrze łączą się z generatorami do leniwego przetwarzania.

</details>

<details>
<summary>54. Czym jest słownik (`dict`) w Pythonie i czym różni się od innych struktur danych?</summary>

#### Python

`dict` to tablica asocjacyjna: przechowuje pary `klucz -> wartość`. Klucze muszą być
hashable, a wartości mogą mieć dowolny typ.

Różnice:

- dostęp odbywa się po kluczu, a nie po indeksie;
- średnia złożoność wyszukiwania/wstawiania/usuwania jest bliska `O(1)`;
- od Pythona 3.7+ zachowuje kolejność wstawiania kluczy.

**W skrócie:**

- `dict` jest optymalny do szybkiego dostępu po kluczu.
- To podstawowa struktura dla konfiguracji i mapowań.
- Klucze muszą być niemutowalne (hashable).

</details>

<details>
<summary>55. Jaka jest różnica między pobieraniem wartości ze słownika przez nawiasy kwadratowe `[]` a metodą `get`?</summary>

#### Python

`d[key]` zwraca wartość albo zgłasza `KeyError`, jeśli klucza nie ma.

`d.get(key, default)` zwraca wartość albo `default` (lub `None`) bez wyjątku.

```python
config = {"timeout": 30}
config["timeout"]         # 30
config.get("retries", 3)  # 3
```

**W skrócie:**

- `[]` służy do obowiązkowych kluczy.
- `get()` nadaje się do opcjonalnych pól.
- `get()` zmniejsza liczbę `try/except` przy odczycie danych.

</details>

<details>
<summary>56. Opisz, jak można aktualizować i usuwać elementy ze słownika.</summary>

#### Python

Aktualizacja:

- `d[key] = value` — wstawić/zaktualizować jeden klucz;
- `d.update({...})` — aktualizacja zbiorcza.

Usuwanie:

- `del d[key]` — usunąć klucz (błąd, jeśli go nie ma);
- `d.pop(key, default)` — usunąć i zwrócić wartość;
- `d.popitem()` — usunąć ostatnią parę;
- `d.clear()` — wyczyścić cały słownik.

**W skrócie:**

- Do upsertu nadają się `[]` i `update()`.
- Do bezpiecznego usuwania częściej używa się `pop()`.
- API warto dobierać zależnie od oczekiwanego zachowania przy braku klucza.

</details>

<details>
<summary>57. Do czego służą metody `keys`, `values` oraz `items` w słownikach?</summary>

#### Python

Te metody zwracają obiekty view słownika:

- `keys()` — wszystkie klucze;
- `values()` — wszystkie wartości;
- `items()` — pary `(key, value)`.

```python
data = {"a": 1, "b": 2}
for key, value in data.items():
    ...
```

Widoki są dynamiczne: odzwierciedlają aktualny stan słownika.

**W skrócie:**

- `keys/values/items` są potrzebne do iteracji i sprawdzeń.
- `items()` jest najwygodniejsze do pętli z kluczem i wartością.
- To nie są kopie, tylko "żywe" reprezentacje danych.

</details>

<details>
<summary>58. Jak `dict` działa w Pythonie pod maską?</summary>

#### Python

`dict` jest zaimplementowany jako hash table z optymalizacjami pamięci i szybkiego dostępu.
Klucz jest haszowany, na podstawie hasza wybierana jest komórka, a kolizje są rozwiązywane
wewnętrznym algorytmem probing.

Praktyczne konsekwencje:

- średni czas dostępu jest bliski `O(1)`;
- jakość `__hash__` i `__eq__` wpływa na zachowanie;
- obiektów mutable nie można używać jako kluczy.

**W skrócie:**

- `dict` to wysokowydajna struktura hashująca.
- Szybkość osiąga dzięki haszowaniu.
- Klucze muszą być hashable i stabilne.

</details>

<details>
<summary>59. Czym jest hash function?</summary>

#### Python

Hash function przekształca obiekt w liczbę całkowitą (hash), która jest używana do
szybkiego umieszczania/wyszukiwania w `dict` i `set`.

Warunki poprawności:

- jeśli `a == b`, to `hash(a) == hash(b)`;
- wartość hasza musi być stabilna przez cały czas życia obiektu.

**W skrócie:**

- Funkcja haszująca jest podstawą szybkiego działania `dict/set`.
- Nie gwarantuje unikalności, bo kolizje są możliwe.
- Dla klas custom ważna jest spójność `__eq__` i `__hash__`.

</details>

<details>
<summary>60. Czym jest `set` w Pythonie i czym różni się od innych struktur danych?</summary>

#### Python

`set` to nieuporządkowana kolekcja **unikalnych** elementów.

Różnice:

- automatycznie usuwa duplikaty;
- oferuje szybkie operacje sprawdzania przynależności (`x in s`);
- wspiera operacje zbiorowe: union/intersection/difference.

**W skrócie:**

- `set` jest optymalny do zapewniania unikalności i membership-check.
- Kolejność elementów nie jest gwarantowana.
- Elementy muszą być hashable.

</details>

<details>
<summary>61. Jak utworzyć `set` w Pythonie i jakie ograniczenia dotyczą elementów set?</summary>

#### Python

Tworzenie:

```python
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # {1, 2, 3}
empty = set()            # nie {}
```

Ograniczenia:

- elementy muszą być hashable, na przykład `int`, `str`, `tuple`;
- `list`, `dict`, `set` nie można dodać bezpośrednio.

**W skrócie:**

- `set()` tworzy pusty zbiór.
- Duplikaty są usuwane automatycznie.
- Dozwolone są tylko elementy hashable.

</details>

<details>
<summary>62. Do czego służy metoda `intersection()` w Python set i czym różni się od `union()`?</summary>

#### Python

`intersection()` zwraca wspólne elementy zbiorów, a `union()` łączy wszystkie
unikalne elementy z obu zbiorów.

```python
a = {1, 2, 3}
b = {3, 4}

a.intersection(b)  # {3}
a.union(b)         # {1, 2, 3, 4}
```

**W skrócie:**

- `intersection` = część wspólna.
- `union` = suma zbiorów, czyli wszystko unikalne.
- Obie metody są podstawowe przy porównywaniu zestawów danych.

</details>

<details>
<summary>63. Jakie typy danych są immutable?</summary>

#### Python

Popularne typy immutable:

- `int`, `float`, `bool`, `complex`;
- `str`, `bytes`;
- `tuple` jeśli jego elementy też są immutable;
- `frozenset`;
- `NoneType`.

**W skrócie:**

- Obiektu immutable nie można zmienić po utworzeniu.
- Zamiast mutacji powstaje nowy obiekt.
- Takie typy są bezpieczniejsze jako klucze `dict` i elementy `set`.

</details>

<details>
<summary>64. Jakie typy danych są mutable?</summary>

#### Python

Popularne typy mutable:

- `list`;
- `dict`;
- `set`;
- `bytearray`;
- większość obiektów klas zdefiniowanych przez użytkownika.

**W skrócie:**

- Obiekty mutable zmieniają się in-place.
- Mutacje mogą powodować efekty uboczne przez współdzielone referencje.
- Z kopiowaniem trzeba pracować ostrożnie.

</details>

<details>
<summary>65. Dlaczego ważne jest rozumienie mutowalności podczas pracy ze słownikami albo set?</summary>

#### Python

`dict` i `set` opierają się na haszowaniu, dlatego ich elementy i klucze muszą być
stabilne (hashable). Obiektów mutable nie da się bezpiecznie używać jako kluczy
ani elementów set.

Dodatkowo mutacja wartości przez współdzielone referencje często prowadzi do trudnych do przewidzenia błędów.

**W skrócie:**

- Mutowalność wpływa na poprawność kluczy w `dict/set`.
- Współdzielone obiekty mutable często powodują efekty uboczne.
- Jawne kopie i kontrola mutacji zmniejszają liczbę błędów.

</details>

<details>
<summary>66. Czym jest `None`?</summary>

#### Python

`None` to specjalna wartość singleton typu `NoneType`, która oznacza
"brak wartości".

Typowe scenariusze:

- funkcja niczego jawnie nie zwraca;
- opcjonalne parametry;
- znacznik "dane nie są jeszcze ustawione".

Sprawdzenie wykonuje się przez `is`:

```python
if value is None:
    ...
```

**W skrócie:**

- `None` oznacza brak wartości.
- To singleton, więc porównuje się go przez `is`.
- Często jest używany w API jako stan opcjonalny.

</details>

<details>
<summary>67. Czym jest `id` w Pythonie, jak go używać i dlaczego to ważne?</summary>

#### Python

`id(obj)` zwraca identyfikator obiektu, unikalny w ramach cyklu życia
obiektu w bieżącym procesie.

To przydaje się w diagnostyce:

- czy to ten sam obiekt;
- czy została utworzona kopia;
- czy nastąpiła mutacja współdzielonej referencji.

**W skrócie:**

- `id` pomaga analizować tożsamość obiektów.
- Jest przydatny przy debugowaniu kopiowania i mutacji.
- Nie używa się go jako identyfikatora biznesowego.

</details>

<details>
<summary>68. Jaka jest różnica między operatorami `is` i `==`?</summary>

#### Python

`==` porównuje **wartości** czyli równoważność, a `is` porównuje **tożsamość**,
czyli czy to dokładnie ten sam obiekt w pamięci.

```python
a = [1, 2]
b = [1, 2]
a == b   # True
a is b   # False
```

**Ważne o optymalizacjach (interning):** CPython buforuje małe liczby całkowite
od `-5` do `256` oraz krótkie napisy na etapie kompilacji lub ładowania. Dlatego
dla nich `is` może zwracać `True`, nawet jeśli zostały utworzone osobno. To jednak
szczegół implementacyjny, na którym nie należy opierać logiki biznesowej.

Dla `None` zawsze używaj `is`.

**W skrócie:**

- `==` dotyczy równości wartości.
- `is` dotyczy dokładnie tego samego obiektu w pamięci.
- Interning może dawać nieoczywiste `is True` dla małych `int` i `str`.
- `value is None` to jedyny poprawny styl sprawdzania `None`.

</details>

<details>
<summary>69. Jak stosuje się Singleton pattern w Pythonie? Podaj przykłady obiektów typu Singleton w Pythonie.</summary>

#### Python

Singleton oznacza jedną globalną instancję obiektu w procesie. W Pythonie często
zastępuje się go poziomem modułu, ponieważ moduły są importowane tylko raz.

Przykłady singletonów w języku:

- `None`;
- `True` i `False`;
- `Ellipsis`.

W kodzie aplikacyjnym zamiast sztywnego Singletonu częściej używa się
kontenera DI albo fabryk, żeby poprawić testowalność.

**W skrócie:**

- Python ma już wbudowane obiekty typu singleton.
- Często wystarcza zakres modułu bez osobnego wzorca.
- Nadużywanie Singletonu pogarsza testowalność.

</details>

<details>
<summary>70. Do czego służą operatory `break` i `continue` w pętlach Pythona?</summary>

#### Python

`break` przedwcześnie kończy pętlę, a `continue` pomija bieżącą iterację
i przechodzi do następnej.

```python
for n in range(10):
    if n == 5:
        break
    if n % 2 == 0:
        continue
```

**W skrócie:**

- `break` zatrzymuje całą pętlę.
- `continue` pomija tylko bieżący krok.
- Dzięki nim sterowanie pętlą jest jawne i czytelne.

</details>

<details>
<summary>71. Wyjaśnij pojęcie pętli nieskończonej. W jakich przypadkach warto jej używać i jak zapewnić jej poprawne zakończenie?</summary>

#### Python

Pętla nieskończona to pętla bez naturalnego warunku zakończenia, na przykład
`while True`. Jest używana w procesach usługowych, workerach, pollingu i logice pętli zdarzeń.

Poprawne zakończenie:

- wyraźny warunek `break`;
- obsługa sygnałów zakończenia;
- timeouty i `try/finally` do czyszczenia zasobów.

```python
while True:
    task = queue.get()
    if task is None:
        break
    handle(task)
```

**W skrócie:**

- `while True` jest uzasadnione w długowiecznych pętlach usługowych.
- Potrzebny jest kontrolowany mechanizm zatrzymania.
- Zawsze trzeba przewidzieć zwalnianie zasobów.

</details>

<details>
<summary>72. Opisz, jak działają zagnieżdżone pętle w Pythonie. Jakie problemy z wydajnością mogą się pojawić i jak ich unikać?</summary>

#### Python

Pętla zagnieżdżona to pętla wewnątrz innej pętli. Złożoność często rośnie do `O(n*m)`
albo gorzej, co jest krytyczne przy dużych zbiorach danych.

Optymalizacje:

- zamieniać wyszukiwanie w listach na `set` lub `dict`;
- wynosić niezmienniki poza pętlę wewnętrzną;
- używać generatorów, `itertools` i wektoryzacji;
- profilować "gorące" miejsca.

**W skrócie:**

- Zagnieżdżone pętle szybko zwiększają koszt obliczeń.
- Struktury danych są często ważniejsze niż mikrooptymalizacje.
- Profilowanie pokazuje, co naprawdę trzeba optymalizować.

</details>

<details>
<summary>73. Czym jest structural pattern matching (`match`/`case`)?</summary>

#### Python

`match/case` w Pythonie 3.10+ to mechanizm dopasowywania struktury danych do wzorców.
Działa z literałami, typami, sekwencjami, słownikami i klasami.

```python
def handle(message: dict[str, object]) -> str:
    match message:
        case {"type": "ping"}:
            return "pong"
        case {"type": "user", "id": int(user_id)}:
            return f"user:{user_id}"
        case _:
            return "unknown"
```

**W skrócie:**

- `match/case` jest czytelniejsze przy złożonym rozgałęzieniu.
- Pozwala jednocześnie sprawdzać kształt danych i wyciągać wartości.
- Jest szczególnie przydatne przy protokołach, zdarzeniach i parsowaniu struktur.

</details>

<details>
<summary>74. W jakich przypadkach pattern matching jest lepszy niż `if`/`elif`?</summary>

#### Python

`match/case` jest lepszy, gdy trzeba:

- sprawdzać wiele wzajemnie wykluczających się form danych;
- rozpakowywać zagnieżdżone struktury;
- unikać długich łańcuchów `if/elif`.

`if/elif` jest lepsze dla prostych warunków logicznych i krótkiej logiki.

**W skrócie:**

- Dla scenariuszy strukturalnych lepszy jest `match/case`.
- Dla prostych warunków wystarczy `if/elif`.
- Kryterium wyboru to czytelność i łatwość utrzymania.

</details>

<details>
<summary>75. Czym jest funkcja w Pythonie?</summary>

#### Python

Funkcja to nazwany blok kodu typu callable, który przyjmuje argumenty, zwraca
wynik i pozwala enkapsulować logikę.

```python
def normalize_name(name: str) -> str:
    return name.strip().title()
```

Funkcje wspierają wartości domyślne, argumenty nazwane, `*args/**kwargs`,
adnotacje typów i dekoratory.

**W skrócie:**

- Funkcja jest podstawową jednostką ponownego użycia kodu.
- Tworzy wyraźny kontrakt przez parametry i wartość return.
- Type hints czynią ten kontrakt bardziej jawnym.

</details>

<details>
<summary>76. Jakie istnieją typy argumentów funkcji?</summary>

#### Python

We współczesnym Pythonie:

- positional-only (`/`);
- positional-or-keyword;
- keyword-only (`*`);
- variadic positional (`*args`);
- variadic keyword (`**kwargs`).

```python
def f(a, /, b, *, c, **kwargs):
    ...
```

**W skrócie:**

- Python daje elastyczną kontrolę nad sposobem wywołania funkcji.
- `/` i `*` formalizują kontrakt API.
- `*args/**kwargs` są przydatne w rozszerzalnych interfejsach.

</details>

<details>
<summary>77. Czym są argumenty pozycyjne i nazwane?</summary>

#### Python

Argumenty pozycyjne są przekazywane według kolejności, a nazwane (`keyword`)
według nazwy parametru.

```python
def connect(host: str, port: int) -> str:
    return f"{host}:{port}"

connect("localhost", 5432)           # pozycyjnie
connect(host="localhost", port=5432) # nazwane
```

**W skrócie:**

- Pozycyjne zależą od kolejności parametrów.
- Nazwane zwiększają czytelność wywołania.
- Można je łączyć z zachowaniem zasad sygnatury.

</details>

<details>
<summary>78. Czym są argumenty domyślne i jakie problemy mogą z nimi występować?</summary>

#### Python

Argumenty domyślne są używane, jeśli wartość nie została przekazana przy wywołaniu.
Są obliczane **tylko raz** w momencie definiowania funkcji.

Problem: mutable default.

```python
def add_item(item: int, bucket: list[int] | None = None) -> list[int]:
    if bucket is None:
        bucket = []
    bucket.append(item)
    return bucket
```

**W skrócie:**

- Wartości domyślne są wygodne dla stabilnych danych.
- Mutable default może kumulować stan między wywołaniami.
- Bezpieczny wzorzec to `None` + inicjalizacja wewnątrz funkcji.

</details>

<details>
<summary>79. Wyjaśnij przeznaczenie i użycie `*args` oraz `**kwargs` w funkcjach Pythona. Czym się różnią?</summary>

#### Python

`*args` zbiera dodatkowe argumenty pozycyjne do `tuple`. `**kwargs` zbiera
dodatkowe argumenty nazwane do `dict`.

```python
def log_event(event: str, *args: object, **kwargs: object) -> None:
    ...
```

Zastosowania: wrappery, adaptery API, dekoratory i przekazywanie parametrów dalej.

**W skrócie:**

- `*args` = dodatkowe argumenty pozycyjne.
- `**kwargs` = dodatkowe argumenty nazwane.
- Dają funkcjom elastyczność, ale wymagają jasnej walidacji.

</details>

<details>
<summary>80. Jak zdefiniować funkcję z type annotations w Pythonie? Podaj przykład i wyjaśnij zalety tego podejścia.</summary>

#### Python

Typy zapisuje się w sygnaturze parametrów i wartości return.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Zalety:

- lepszy DX, czyli autocomplete i nawigacja;
- statyczne sprawdzanie w CI;
- jawny kontrakt dla innych programistów.

**W skrócie:**

- Adnotacje typów dokumentują API.
- Zmniejszają ryzyko błędów integracyjnych.
- Najwięcej dają w średnich i dużych bazach kodu.

</details>

<details>
<summary>81. Czym są funkcje lambda?</summary>

#### Python

`lambda` to anonimowa funkcja jedno-wyrażeniowa. Zwykle jest używana do
krótkich callbacków w `sorted`, `map`, `filter`.

```python
users = [{"name": "Ada"}, {"name": "Bob"}]
users_sorted = sorted(users, key=lambda u: u["name"])
```

Dla bardziej złożonej logiki lepsza jest zwykła funkcja `def`.

**W skrócie:**

- `lambda` jest wygodna do krótkich lokalnych wyrażeń.
- Jest ograniczona do jednego wyrażenia.
- Dla czytelności bardziej złożony kod lepiej wynieść do `def`.

</details>

<details>
<summary>82. Jaki jest zakres widoczności zmiennych w funkcji?</summary>

#### Python

Python używa reguły LEGB do wyszukiwania nazw:

- `L`ocal;
- `E`nclosing, czyli funkcje zewnętrzne;
- `G`lobal, czyli moduł;
- `B`uiltins.

Wewnątrz funkcji przypisanie tworzy zmienną lokalną, jeśli nie użyto `global`
albo `nonlocal`.

**W skrócie:**

- Scope określa, gdzie nazwa jest dostępna i może być zmieniana.
- LEGB wyjaśnia kolejność wyszukiwania zmiennych.
- Błędne rozumienie zasięgu często prowadzi do `UnboundLocalError`.

</details>

<details>
<summary>83. Czym są zmienne lokalne i globalne w Pythonie?</summary>

#### Python

Zmienne lokalne istnieją w ciele funkcji. Zmienne globalne są zdefiniowane na
poziomie modułu.

Aby zmienić zmienną globalną z poziomu funkcji, potrzebny jest `global`, ale zwykle
warto tego unikać przez niejawne zależności.

**W skrócie:**

- Zmienne lokalne są bezpieczniejsze dla utrzymania i testowania.
- Globalne upraszczają dostęp, ale utrudniają kontrolę stanu.
- Lepiej przekazywać zależności przez parametry.

</details>

<details>
<summary>84. Jaka jest różnica między zmiennymi lokalnymi a `nonlocal` w Pythonie?</summary>

#### Python

`nonlocal` jest używane w funkcji zagnieżdżonej do zmiany zmiennej z najbliższego
zewnętrznego zasięgu, czyli nie globalnego.

```python
from collections.abc import Callable


def counter() -> Callable:
    value = 0

    def inc() -> int:
        nonlocal value
        value += 1
        return value

    return inc
```

**W skrócie:**

- Zmienna lokalna należy do bieżącej funkcji.
- `nonlocal` zmienia stan funkcji zewnętrznej.
- To kluczowy mechanizm dla closure ze stanem.

</details>

<details>
<summary>85. Czym jest unpacking w Pythonie i jak stosuje się go przy przypisaniu?</summary>

#### Python

Unpacking to rozkładanie elementów sekwencji lub struktury na osobne zmienne.

```python
x, y = (10, 20)
first, *middle, last = [1, 2, 3, 4]
```

Działa też ze słownikami w `match/case`, przy wywołaniach funkcji i w pętlach.

**W skrócie:**

- Unpacking sprawia, że kod jest bardziej zwięzły i czytelny.
- Wspiera "gwiazdkowe" przechwycenie pozostałych wartości.
- Często jest używany przy parsowaniu struktur danych.

</details>

<details>
<summary>86. Wyjaśnij pojęcie packing wartości w Pythonie i podaj przykłady.</summary>

#### Python

Packing to zbieranie kilku wartości do jednej struktury, na przykład `tuple`, `list`, `dict`.

```python
point = 10, 20                 # tuple packing

def collect(*args: int) -> tuple[int, ...]:
    return args
```

`*args` i `**kwargs` to typowy przykład packingu argumentów.

**W skrócie:**

- Packing zbiera wiele wartości do jednego kontenera.
- Najczęściej jest używany w sygnaturach funkcji.
- Dobrze łączy się z unpackingiem po stronie wywołania.

</details>

<details>
<summary>87. Do czego używa się operatora `*` przy packingu i unpackingu?</summary>

#### Python

`*` w parametrach funkcji pakuje argumenty pozycyjne do `*args`, a przy wywołaniu
rozpakowuje iterable do argumentów pozycyjnych.

```python
def add(a: int, b: int) -> int:
    return a + b

nums = [2, 3]
add(*nums)  # 5
```

`*` jest też używane w przypisaniu do przechwycenia "reszty" elementów.

**W skrócie:**

- `*` to uniwersalny operator do pracy z varargs.
- W sygnaturze pakuje, przy wywołaniu rozpakowuje.
- Zmniejsza ilość szablonowego kodu przy przekazywaniu danych.

</details>

<details>
<summary>88. Czym jest closure i jaki ma związek z decoratorami?</summary>

#### Python

Closure to funkcja wewnętrzna, która "pamięta" zmienne z zewnętrznego zakresu nawet po
zakończeniu działania funkcji zewnętrznej.

Decorator zwykle implementuje się właśnie przez closure: wrapper przechowuje
odwołanie do oryginalnej funkcji i dodatkowych parametrów.

**W skrócie:**

- Closure to funkcja plus przechwycony kontekst.
- Decorator jest często praktycznym zastosowaniem closure.
- Daje możliwość dodania zachowania bez zmiany ciała funkcji.

</details>

<details>
<summary>89. Czym jest decorator w Pythonie i jak działa?</summary>

#### Python

Decorator to obiekt callable, który przyjmuje funkcję albo klasę i zwraca zmodyfikowaną
wersję, czyli wrapper.

```python
from functools import wraps

def log_calls(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Zastosowania: logowanie, cache'owanie, autoryzacja, retry i metryki.

**W skrócie:**

- Decorator dodaje zachowanie cross-cutting.
- Działa przez opakowanie callable.
- Pozwala nie duplikować technicznej logiki w kodzie biznesowym.

</details>

<details>
<summary>90. Czy można używać kilku decoratorów dla jednej funkcji?</summary>

#### Python

Tak, można układać kilka decoratorów w stos. Są stosowane od dołu do góry,
czyli ten bliżej `def` opakowuje funkcję jako pierwszy.

```python
@decorator_a
@decorator_b
def handler() -> None:
    ...
```

Równoważny zapis: `handler = decorator_a(decorator_b(handler))`.

**W skrócie:**

- Kilka decoratorów jest dopuszczalne i powszechne.
- Kolejność zastosowania ma znaczenie.
- Stos decoratorów warto dokumentować dla przejrzystości.

</details>

<details>
<summary>91. Opisz możliwy problem z kolejnością decoratorów przy ich stosowaniu do funkcji.</summary>

#### Python

Nieprawidłowa kolejność może zmienić semantykę. Na przykład cache'owanie przed
sprawdzeniem dostępu może zachować niepożądany wynik albo ominąć oczekiwaną logikę.

Typowe ryzyka:

- logowanie widzi już zmienione argumenty;
- retry opakowują nie ten wyjątek;
- cache jest nakładany przed lub po walidacji w złym miejscu.

**W skrócie:**

- Kolejność decoratorów wpływa na zachowanie funkcji.
- To częsta przyczyna ukrytych błędów.
- Dla krytycznych łańcuchów potrzebne są testy kolejności wykonania.

</details>

<details>
<summary>92. Czy można utworzyć decorator za pomocą klasy?</summary>

#### Python

Tak. Klasa-decorator implementuje `__call__`, aby instancja zachowywała się jak funkcja.

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.calls = 0

    def __call__(self, *args, **kwargs):
        self.calls += 1
        return self.func(*args, **kwargs)
```

**W skrócie:**

- Decorator można zaimplementować nie tylko jako funkcję, ale też jako klasę.
- Klasa jest wygodna, gdy potrzebny jest wewnętrzny stan.
- Kluczowy mechanizm to `__call__`.

</details>

<details>
<summary>93. Jak zdefiniować decorator przyjmujący parametry?</summary>

#### Python

Potrzebna jest trójpoziomowa struktura: fabryka dekoratora -> decorator -> wrapper.

```python
from functools import wraps

def retry(times: int):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            for _ in range(times - 1):
                try:
                    return func(*args, **kwargs)
                except Exception:
                    pass
            return func(*args, **kwargs)
        return wrapper
    return decorator
```

**W skrócie:**

- Parametryzowany decorator to funkcja, która zwraca decorator.
- Do zachowania parametrów często używa się closure.
- To podejście jest wygodne przy konfigurowalnym zachowaniu.

</details>

<details>
<summary>94. Do czego używa się `functools.wraps` w funkcjach-decoratorach?</summary>

#### Python

`functools.wraps` kopiuje metadane oryginalnej funkcji do wrappera: nazwę,
docstring, moduł oraz `__wrapped__`.

To ważne dla:

- poprawnego debugowania i logów;
- introspekcji i dokumentacji;
- zgodności z narzędziami, które odczytują sygnaturę.

**W skrócie:**

- `wraps` zachowuje "tożsamość" oryginalnej funkcji.
- Bez niego dekorowane funkcje tracą przydatne metadane.
- To best practice dla wszystkich decoratorów opartych na wrapperze.

</details>

<details>
<summary>95. Jak działają dict comprehension, list comprehension i set comprehension?</summary>

#### Python

Comprehension tworzy kolekcję na podstawie wyrażenia i pętli, opcjonalnie z filtrem.

```python
squares = [x * x for x in range(6)]
mapping = {x: x * x for x in range(6)}
unique = {x % 3 for x in range(10)}
```

Format:

- list: `[expr for x in it if cond]`
- set: `{expr for x in it if cond}`
- dict: `{k_expr: v_expr for x in it if cond}`

**W skrócie:**

- Comprehension w zwięzły sposób wyraża transformację danych.
- Działa dla `list`, `set` i `dict`.
- Daje czystszy kod niż ręczne dodawanie elementów w pętli.

</details>

<details>
<summary>96. Jakie są zalety używania list comprehension w porównaniu ze zwykłymi pętlami?</summary>

#### Python

Zalety:

- krótszy i bardziej deklaratywny kod;
- mniej zmiennych pomocniczych;
- zwykle trochę lepsza wydajność w CPythonie;
- mniejsze ryzyko, że zapomnisz o `append`.

Wada: przy bardzo złożonej logice comprehension pogarsza czytelność.

**W skrócie:**

- List comprehension dobrze nadaje się do prostych transformacji.
- Często jest szybsze i czystsze niż ręczna pętla.
- Dla złożonych gałęzi lepszy jest zwykły `for`.

</details>

<details>
<summary>97. Czy możesz podać przykład zagnieżdżonej list comprehension?</summary>

#### Python

Przykład spłaszczenia macierzy:

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for row in matrix for item in row]  # [1, 2, 3, 4, 5, 6]
```

Przykład z warunkiem:

```python
pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
```

**W skrócie:**

- Zagnieżdżona comprehension to kilka `for` w jednym wyrażeniu.
- Kolejność `for` odpowiada zagnieżdżonym pętlom.
- Używaj jej wtedy, gdy wyrażenie pozostaje czytelne.

</details>

<details>
<summary>98. Co jest szybsze w Pythonie: list comprehension czy tworzenie listy za pomocą pętli?</summary>

#### Python

W typowych scenariuszach list comprehension jest trochę szybsze niż pętla z `append`,
bo ma zoptymalizowany bajtkod i mniej narzutu.

Ważne: realny zysk zależy od samej operacji, dlatego w krytycznych miejscach
warto mierzyć wydajność za pomocą `timeit` lub `pyperf`.

**W skrócie:**

- Często szybsze jest list comprehension.
- Różnica może być niewielka.
- W rozwiązaniach produkcyjnych trzeba opierać się na pomiarach.

</details>

<details>
<summary>99. Czym jest iterator w Pythonie?</summary>

#### Python

Iterator to obiekt, który zwraca elementy sekwencyjnie i pamięta bieżący stan.
Implementuje protokół:

- `__iter__()` zwraca siebie;
- `__next__()` zwraca następny element albo zgłasza `StopIteration`.

**W skrócie:**

- Iterator daje dostęp element po elemencie bez pełnego wczytywania danych.
- To podstawa dla `for`, generatorów i leniwego przetwarzania.
- Po wyczerpaniu iterator nie "przewija się" sam.

</details>

<details>
<summary>100. Jak utworzyć iterator z obiektu iterowalnego za pomocą funkcji `iter()`?</summary>

#### Python

Wywołaj `iter(iterable)`, aby otrzymać iterator.

```python
items = [10, 20, 30]
it = iter(items)
```

Potem wartości odczytuje się przez `next(it)`.

**W skrócie:**

- `iter()` zamienia iterable na iterator.
- To jawny sposób ręcznego sterowania iteracją.
- Używa się go w niskopoziomowym przetwarzaniu strumienia danych.

</details>

<details>
<summary>101. Do czego służy funkcja `next()` przy pracy z iteratorami?</summary>

#### Python

`next(iterator[, default])` zwraca następny element iteratora. Gdy elementy się
skończą, zgłasza `StopIteration` albo zwraca `default`, jeśli został podany.

```python
it = iter([1, 2])
next(it)        # 1
next(it)        # 2
next(it, None)  # None
```

**W skrócie:**

- `next()` daje ręczną kontrolę nad krokiem iteracji.
- Bez `default` koniec strumienia oznacza `StopIteration`.
- Z `default` można wygodnie i bezpiecznie czytać strumień.

</details>

<details>
<summary>102. Czy można zamiennie używać metod `__next__()` i `__iter__()` z funkcjami `next()` oraz `iter()`?</summary>

#### Python

Tak, ale z uwzględnieniem protokołu:

- `iter(obj)` wywołuje `obj.__iter__()`;
- `next(it)` wywołuje `it.__next__()`.

Funkcje są więc standardowym interfejsem do metod dunder i zwykle
używa się ich zamiast bezpośrednich wywołań.

**W skrócie:**

- `iter()` odpowiada `__iter__()`.
- `next()` odpowiada `__next__()`.
- W kodzie aplikacyjnym lepiej wywoływać funkcje wbudowane.

</details>

<details>
<summary>103. Jaka jest rola `StopIteration` w projektowaniu iteratorów i kiedy zwykle się pojawia?</summary>

#### Python

`StopIteration` sygnalizuje, że iterator został wyczerpany. Pętla `for`
automatycznie go przechwytuje i kończy iterację.

Zwykle pojawia się:

- przy wywołaniu `next(it)` po ostatnim elemencie;
- we własnych iteratorach, gdy dane się skończyły.

**W skrócie:**

- `StopIteration` to normalny koniec strumienia.
- Nie trzeba go logować jako "błędu" w normalnym przepływie.
- We własnych iteratorach trzeba zgłaszać go poprawnie.

</details>

<details>
<summary>104. Czym jest generator i czym różni się od iteratora albo zwykłej funkcji?</summary>

#### Python

Generator to specjalny iterator tworzony przez funkcję z `yield`. Zwraca
wartości po jednej i zachowuje wewnętrzny stan między wywołaniami.

Różnice:

- od zwykłej funkcji: nie kończy się jednym `return`, tylko działa w trybie "pauza/wznowienie";
- od ręcznego iteratora: ma prostszą implementację bez jawnej klasy z `__next__`.

**W skrócie:**

- Generator to najwygodniejszy sposób leniwej iteracji.
- Wymaga mniej kodu niż własna klasa iteratora.
- Jest szczególnie przydatny dla dużych strumieni danych.

</details>

<details>
<summary>105. Jak utworzyć funkcję generatora?</summary>

#### Python

Trzeba zdefiniować funkcję z `yield`.

```python
def countdown(start: int):
    current = start
    while current > 0:
        yield current
        current -= 1
```

Wywołanie `countdown(3)` zwraca obiekt generatora, po którym można iterować.

**W skrócie:**

- Obecność `yield` sprawia, że funkcja staje się generatorem.
- Generator zwraca wartości etapami.
- Stan funkcji jest zachowywany między iteracjami.

</details>

<details>
<summary>106. Jak słowo kluczowe `yield` zapewnia działanie generatorów i dlaczego oszczędzają one pamięć?</summary>

#### Python

`yield` zwraca kolejną wartość i "zamraża" kontekst funkcji, czyli zmienne
lokalne oraz miejsce wykonania. Następne `next()` wznawia działanie od tego punktu.

Oszczędność pamięci wynika z tego, że dane nie są tworzone w całości z góry,
tylko obliczane na żądanie.

**W skrócie:**

- `yield` realizuje mechanizm pauzy i wznowienia wykonania.
- Generator wspiera leniwe obliczanie.
- To zmniejsza zużycie pamięci dla dużych zbiorów danych.

</details>

<details>
<summary>107. Jaka jest różnica między `return` a `yield`?</summary>

#### Python

`return` kończy funkcję i zwraca jedną końcową wartość. `yield` zwraca
wartość pośrednią i zachowuje stan do dalszego wznowienia.

W generatorze `return` oznacza koniec iteracji, czyli `StopIteration`.

**W skrócie:**

- `return` oznacza zakończenie funkcji.
- `yield` oznacza etapowe zwracanie wartości.
- `yield` jest używane przy przetwarzaniu strumieniowym.

</details>

<details>
<summary>108. Czym jest Object-Oriented Programming (OOP) i jakie są jego główne zasady w Pythonie?</summary>

#### Python

OOP to podejście, w którym dane i zachowanie są połączone w obiektach.

Główne zasady:

- enkapsulacja;
- dziedziczenie;
- polimorfizm;
- abstrakcja.

W Pythonie OOP zwykle łączy się z kompozycją i duck typing.

**W skrócie:**

- OOP strukturyzuje domenę przez klasy i obiekty.
- Python wspiera OOP elastycznie, bez nadmiaru szablonowego kodu.
- W praktyce kompozycja często bywa lepsza niż głębokie dziedziczenie.

</details>

<details>
<summary>109. Czym jest `class` w Pythonie?</summary>

#### Python

`class` to szablon do tworzenia obiektów z atrybutami i metodami.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name
```

Klasa określa strukturę i zachowanie przyszłych instancji.

**W skrócie:**

- Klasa opisuje dane i operacje na nich.
- Na podstawie klasy tworzone są obiekty, czyli instancje.
- To podstawowa jednostka modelowania w OOP.

</details>

<details>
<summary>110. Jak utworzyć obiekt w Pythonie?</summary>

#### Python

Obiekt tworzy się przez wywołanie klasy:

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

user = User("Ada")
```

Podczas tworzenia wykonywane jest `__init__`, aby zainicjalizować stan.

**W skrócie:**

- Obiekt to instancja klasy.
- Tworzenie wygląda tak: `instance = ClassName(...)`.
- `__init__` ustawia początkowe atrybuty.

</details>

<details>
<summary>111. Czym są obiekty i atrybuty?</summary>

#### Python

Obiekt to konkretna instancja typu albo klasy. Atrybut to powiązana z obiektem
para nazwa-wartość, czyli dane albo metoda.

```python
user.name       # atrybut-dane
user.save()     # atrybut-metoda
```

**W skrócie:**

- Obiekt przechowuje stan i zachowanie.
- Atrybuty opisują ten stan i zachowanie.
- Dostęp do atrybutów odbywa się przez notację kropkową.

</details>

<details>
<summary>112. Jaką rolę pełni metoda `__init__()` w klasie?</summary>

#### Python

`__init__` to inicjalizator instancji: jest wywoływany po utworzeniu obiektu i
ustawia stan początkowy.

```python
class Account:
    def __init__(self, owner: str, balance: float = 0.0) -> None:
        self.owner = owner
        self.balance = balance
```

**W skrócie:**

- `__init__` ustawia początkowe atrybuty obiektu.
- Działa jako punkt wejścia konfiguracji instancji.
- Nie tworzy obiektu, tylko go inicjalizuje.

</details>

<details>
<summary>113. Do czego służy parametr `self` w metodach klas Pythona?</summary>

#### Python

`self` to referencja do bieżącej instancji. Przez `self` metoda odczytuje i zmienia
atrybuty instancji.

```python
def deposit(self, amount: float) -> None:
    self.balance += amount
```

Nazwa `self` nie jest zarezerwowana składniowo, ale jest powszechnie przyjętym standardem.

**W skrócie:**

- `self` wiąże metodę z konkretnym obiektem.
- Przez `self` dostępne są dane instancji.
- To obowiązkowy pierwszy parametr metody instancji.

</details>

<details>
<summary>114. Jak definiować metody w klasie?</summary>

#### Python

Metody definiuje się jako funkcje wewnątrz `class`.

```python
class Calculator:
    def add(self, a: int, b: int) -> int:
        return a + b
```

Typowe rodzaje to metody instancji (`self`), klasy (`@classmethod`, `cls`) i statyczne
(`@staticmethod`, bez `self/cls`).

**W skrócie:**

- Metoda to funkcja wewnątrz ciała klasy.
- Typ metody określają dekorator i sygnatura.
- Najczęściej używana jest metoda instancji.

</details>

<details>
<summary>115. Wyjaśnij koncepcję "wszystko jest obiektem" w Pythonie i podaj przykłady.</summary>

#### Python

W Pythonie prawie wszystko jest obiektem: liczby, napisy, funkcje, klasy i moduły.
Dlatego wszystko ma typ, atrybuty i zachowanie.

```python
type(10)          # <class 'int'>
type(len)         # <class 'builtin_function_or_method'>
type(str)         # <class 'type'>
```

**W skrócie:**

- Jednolity model obiektowy upraszcza język.
- Funkcje i klasy też są obiektami pierwszej kategorii.
- To sprawia, że Python jest elastyczny w metaprogramowaniu.

</details>

<details>
<summary>116. Podaj przykład klasy z metodami, które wykonują obliczenia na podstawie atrybutów.</summary>

#### Python

```python
class Rectangle:
    def __init__(self, width: float, height: float) -> None:
        self.width = width
        self.height = height

    def area(self) -> float:
        return self.width * self.height

    def perimeter(self) -> float:
        return 2 * (self.width + self.height)
```

**W skrócie:**

- Metody mogą obliczać wartości na podstawie atrybutów instancji.
- To enkapsuluje logikę domenową w obiekcie.
- API klasy staje się samoopisowe.

</details>

<details>
<summary>117. Opisz sytuację, w której może być potrzebne użycie kilku klas w programie Pythona.</summary>

#### Python

Gdy domena ma kilka odpowiedzialności, rozdziela się je między klasy. Na przykład
w systemie e-commerce: `Order`, `OrderItem`, `PaymentService`, `InventoryService`.

To daje:

- wyraźny podział odpowiedzialności;
- słabsze sprzężenie;
- łatwiejszą wymianę i testowanie komponentów.

**W skrócie:**

- Kilka klas jest potrzebnych do modelowania złożonej domeny.
- Podział odpowiedzialności zwiększa utrzymywalność.
- Kompozycja klas zwykle jest lepsza niż "obiekt-bóg".

</details>

<details>
<summary>118. Jaka jest różnica między metodą instancji, metodą klasy i metodą statyczną?</summary>

#### Python

- Metoda instancji ma `self` i działa na konkretnej instancji.
- Metoda klasy ma `cls` i działa na klasie jako całości.
- Metoda statyczna nie ma `self/cls`; to funkcja pomocnicza w przestrzeni nazw klasy.

**W skrócie:**

- Metoda instancji to logika instancji.
- Metoda klasy to logika klasy i alternatywne konstruktory.
- Metoda statyczna to logika pomocnicza bez dostępu do stanu.

</details>

<details>
<summary>119. Czym jest `@classmethod` w Pythonie i czym różni się od zwykłych metod?</summary>

#### Python

`@classmethod` przekazuje jako pierwszy argument klasę `cls`, a nie instancję.
Często używa się go do metod fabrykujących.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

    @classmethod
    def from_email(cls, email: str) -> User:
        return cls(email.split("@")[0])
```

**W skrócie:**

- `classmethod` działa na poziomie klasy.
- Jest wygodny dla alternatywnych konstruktorów.
- Nie wymaga już utworzonej instancji.

</details>

<details>
<summary>120. Czym jest `@staticmethod` w klasach Pythona i kiedy warto go stosować?</summary>

#### Python

`@staticmethod` definiuje metodę bez automatycznego `self` ani `cls`. Logicznie
należy do klasy, ale nie zależy od jej stanu.

```python
class Math:
    @staticmethod
    def clamp(value: int, min_v: int, max_v: int) -> int:
        return max(min_v, min(value, max_v))
```

**W skrócie:**

- `staticmethod` to funkcja w namespace klasy.
- Używaj go do logiki pomocniczej bez dostępu do atrybutów.
- Nie nadaje się tam, gdzie potrzebny jest stan instancji albo klasy.

</details>

<details>
<summary>121. Jaka jest różnica między `@classmethod` a `@staticmethod` w klasach Pythona?</summary>

#### Python

Różnica dotyczy pierwszego argumentu i poziomu dostępu:

- `@classmethod` otrzymuje `cls` i może pracować ze stanem klasy;
- `@staticmethod` nie otrzymuje nic automatycznie.

Metoda klasowa częściej służy do metod fabrykujących i polimorficznych konstruktorów,
a metoda statyczna do funkcji pomocniczych.

**W skrócie:**

- Metoda klasowa "wie" o klasie.
- Metoda statyczna jest odizolowana od stanu klasy i instancji.
- Wybór zależy od tego, czy potrzebny jest dostęp do `cls`.

</details>

<details>
<summary>122. Czym są atrybuty instancji w klasach Pythona i czym różnią się od atrybutów klasowych?</summary>

#### Python

Atrybuty instancji należą do konkretnego obiektu, na przykład `self.x`. Atrybuty klasowe
należą do klasy i są współdzielone przez wszystkie instancje.

```python
class User:
    role = "member"           # atrybut klasowy
    def __init__(self, name: str) -> None:
        self.name = name      # atrybut instancji
```

**W skrócie:**

- Atrybuty instancji przechowują indywidualny stan.
- Atrybuty klasowe przechowują wspólną konfigurację.
- Zmiany atrybutów klasowych wpływają na wszystkie instancje.

</details>

<details>
<summary>123. Czym jest `__slots__` w Pythonie?</summary>

#### Python

`__slots__` ogranicza zestaw dozwolonych atrybutów w klasie i może zmniejszyć
zużycie pamięci, usuwając `__dict__` z instancji.

```python
class Point:
    __slots__ = ("x", "y")
    def __init__(self, x: int, y: int) -> None:
        self.x = x
        self.y = y
```

**Niuanse użycia:**

- **Oszczędność pamięci:** obiekty zajmują znacznie mniej miejsca, bo atrybuty
  są przechowywane w stałej strukturze zamiast w tablicy haszującej `__dict__`.
- **Szybkość:** dostęp do atrybutów w `__slots__` bywa zwykle trochę szybszy.
- **Brak `__dict__`:** nie da się dynamicznie dodawać nowych atrybutów,
  których nie ma na liście `__slots__`, chyba że doda się tam `"__dict__"`.
- **Słabe referencje:** jeśli chcesz używać `weakref`, trzeba jawnie
  dodać `"__weakref__"` do `__slots__`.

**W skrócie:**

- `__slots__` jest przydatny dla milionów lekkich obiektów, na przykład węzłów grafu.
- Domyślnie usuwa `__dict__` i `__weakref__`.
- Zmniejsza elastyczność na rzecz wydajności i kontroli.

</details>

<details>
<summary>124. Czym są magic methods, czyli metody dunder, w klasach Pythona i dlaczego nazywa się je "magicznymi"?</summary>

#### Python

Metody dunder, takie jak `__init__`, `__str__`, `__len__`, `__eq__`, to specjalne
punkty zaczepienia, które Python wywołuje automatycznie w odpowiedzi na operatory i funkcje wbudowane.

Nazywa się je "magicznymi", ponieważ integrują klasę z zachowaniem samego języka.

**W skrócie:**

- Metody dunder definiują protokołowe zachowanie obiektu.
- Pozwalają klasom zachowywać się "jak typy wbudowane".
- Używaj ich tylko wtedy, gdy istnieje wyraźna potrzeba semantyczna.

</details>

<details>
<summary>125. Do czego służy metoda `__del__`?</summary>

#### Python

`__del__` to finalizator, który może zostać wywołany przed zniszczeniem obiektu przez GC.
Jego działanie nie jest deterministyczne, dlatego do zarządzania zasobami lepiej
używać menedżerów kontekstu, czyli `with`, oraz jawnego zamykania.

**W skrócie:**

- `__del__` nie gwarantuje terminowego wykonania.
- Nie opieraj krytycznego czyszczenia wyłącznie na nim.
- Zalecane podejście to `with` lub `try/finally`.

</details>

<details>
<summary>126. Podaj przykład użycia magicznej metody `__str__` do zdefiniowania tekstowej reprezentacji własnej klasy w Pythonie.</summary>

#### Python

```python
class User:
    def __init__(self, name: str, active: bool) -> None:
        self.name = name
        self.active = active

    def __str__(self) -> str:
        status = "active" if self.active else "inactive"
        return f"User(name={self.name}, status={status})"
```

`str(user)` i `print(user)` użyją `__str__`.

**W skrócie:**

- `__str__` daje reprezentację obiektu zrozumiałą dla człowieka.
- Jest przydatny w logach i wyjściu CLI.
- Powinien być krótki i czytelny.

</details>

<details>
<summary>127. Do czego używa się `__str__` i `__repr__`?</summary>

#### Python

`__str__` jest skierowany do końcowego odbiorcy. `__repr__` jest skierowany do
programisty i debugowania, dlatego najlepiej, by był jednoznaczny.

`print(obj)` zwykle używa `__str__`, a REPL oraz `repr(obj)` używają `__repr__`.

**W skrócie:**

- `__str__` służy do przyjaznego wyjścia.
- `__repr__` służy do technicznej reprezentacji.
- Dobrą praktyką jest posiadanie obu, jeśli klasa jest domenowa.

</details>

<details>
<summary>128. Jak działa przeciążanie operatorów w Pythonie i dlaczego jest to przydatne?</summary>

#### Python

Przeciążanie operatorów polega na implementacji metod dunder operatorów, takich jak
`__add__`, `__sub__`, `__eq__`, aby obiekty własnej klasy obsługiwały operatory.

```python
class Vector2:
    def __init__(self, x: float, y: float) -> None:
        self.x = x
        self.y = y

    def __add__(self, other: "Vector2") -> "Vector2":
        return Vector2(self.x + other.x, self.y + other.y)
```

**W skrócie:**

- Daje naturalną składnię dla typów domenowych.
- Zwiększa wyrazistość API.
- Ważne jest zachowanie matematycznie oczekiwanej semantyki.

</details>

<details>
<summary>129. Czym jest dziedziczenie?</summary>

#### Python

Dziedziczenie pozwala utworzyć klasę pochodną, która odziedzicza atrybuty i metody
klasy bazowej oraz może rozszerzać albo nadpisywać jej zachowanie.

**W skrócie:**

- Dziedziczenie sprzyja ponownemu użyciu kodu.
- Klasa pochodna może nadpisywać metody klasy bazowej.
- Nadmierna hierarchia utrudnia utrzymanie, więc często lepsza jest kompozycja.

</details>

<details>
<summary>130. Czym jest pojedyncze dziedziczenie w Pythonie?</summary>

#### Python

Pojedyncze dziedziczenie oznacza, że klasa ma tylko jednego bezpośredniego rodzica.

```python
class Animal:
    ...

class Dog(Animal):
    ...
```

To najprostsza i zwykle najbardziej czytelna forma dziedziczenia.

**W skrócie:**

- Jedna klasa pochodna oznacza jedną klasę bazową.
- To prosty model rozwiązywania metod.
- Często wystarcza dla większości modeli biznesowych.

</details>

<details>
<summary>131. Jak zaimplementować dziedziczenie w klasach Pythona i jaka składnia jest do tego używana?</summary>

#### Python

Składnia: `class Child(Base):`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return "hi"
```

Jeśli trzeba wywołać logikę klasy bazowej, użyj `super()`.

**W skrócie:**

- Dziedziczenie zapisuje się w nawiasach po nazwie klasy.
- Klasa pochodna otrzymuje API klasy bazowej.
- Nadpisywanie pozwala dostosować zachowanie.

</details>

<details>
<summary>132. Jak uzyskać dostęp do składowych klasy bazowej w klasie pochodnej?</summary>

#### Python

Dostęp jest możliwy bezpośrednio przez odziedziczone atrybuty i metody albo przez `super()`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return super().greet() + " world"
```

**W skrócie:**

- Odziedziczone składowe są dostępne w klasie pochodnej automatycznie.
- `super()` poprawnie wywołuje logikę klasy bazowej.
- To ważne przy rozszerzaniu, a nie duplikowaniu zachowania.

</details>

<details>
<summary>133. Do czego służy funkcja `super()` w dziedziczeniu w Pythonie i jak się jej używa?</summary>

#### Python

`super()` zwraca obiekt pośredniczący do następnej klasy zgodnie z MRO, aby wywołać jej metody.
Typowo używa się jej w `__init__` oraz przy kooperatywnym wielokrotnym dziedziczeniu.

```python
class Child(Base):
    def __init__(self, value: int) -> None:
        super().__init__()
        self.value = value
```

**W skrócie:**

- `super()` wywołuje implementację klasy bazowej bez twardego wskazywania jej nazwy.
- Pomaga zachować poprawność względem MRO.
- To zalecany sposób pracy z dziedziczeniem.

</details>

<details>
<summary>134. Opisz funkcję `isinstance()` w Pythonie i podaj przykład jej użycia.</summary>

#### Python

`isinstance(obj, cls_or_tuple)` sprawdza, czy obiekt należy do danego typu albo jego
podklasy.

```python
isinstance(10, int)                 # True
isinstance(True, int)               # True
isinstance("x", (str, bytes))       # True
```

**W skrócie:**

- `isinstance` jest bezpieczniejsze niż `type(obj) is ...` w kodzie polimorficznym.
- Uwzględnia hierarchię dziedziczenia.
- Obsługuje krotkę typów.

</details>

<details>
<summary>135. Wyjaśnij funkcję `issubclass()` w Pythonie i podaj przykład jej zastosowania.</summary>

#### Python

`issubclass(Sub, Base)` sprawdza, czy klasa `Sub` jest podklasą `Base`.

```python
class Animal: ...
class Dog(Animal): ...

issubclass(Dog, Animal)  # True
```

**W skrócie:**

- Działa na klasach, a nie na instancjach.
- Jest wygodna do walidacji API na poziomie typów.
- Uwzględnia dziedziczenie tranzytywne.

</details>

<details>
<summary>136. Czym jest wielokrotne dziedziczenie?</summary>

#### Python

Wielokrotne dziedziczenie oznacza dziedziczenie jednej klasy po kilku klasach bazowych.

```python
class A: ...
class B: ...
class C(A, B): ...
```

Daje elastyczność, ale wymaga dyscypliny w projektowaniu metod i używaniu `super()`.

**W skrócie:**

- Jedna klasa może dziedziczyć zachowanie z kilku źródeł.
- Jest przydatne w podejściu opartym na mixinach.
- Może utrudniać zrozumienie MRO.

</details>

<details>
<summary>137. Jak działa MRO (Method Resolution Order) przy wielokrotnym dziedziczeniu?</summary>

#### Python

MRO określa kolejność wyszukiwania metod w hierarchii klas. W Pythonie używany jest
algorytm linearyzacji C3.

**Problem diamentu:** To klasyczny przypadek, gdy klasa `D`
dziedziczy po `B` i `C`, a obie te klasy dziedziczą po `A`. MRO gwarantuje,
że `A` zostanie rozpatrzona dopiero po wszystkich jej potomkach, czyli
`B` i `C`.

```python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass

print(D.mro())
# [D, B, C, A, object]
```

Kolejność można sprawdzić przez `ClassName.__mro__` albo `ClassName.mro()`.

**W skrócie:**

- MRO decyduje, z której klasy bazowej pobrać metodę.
- Kolejność jest przewidywalna i formalnie określona przez C3.
- Dzięki MRO Python poprawnie obsługuje problem diamentu.
- Przy kooperatywnym dziedziczeniu wszystkie klasy powinny wywoływać `super()`.

</details>

<details>
<summary>138. Jakie są zalety i wady używania wielokrotnego dziedziczenia?</summary>

#### Python

Zalety:

- ponowne użycie zachowania z kilku źródeł;
- wygodne mixiny do "dodawania" możliwości.

Wady:

- bardziej złożone MRO;
- ryzyko konfliktów nazw i zachowań;
- trudniejsze debugowanie i wdrożenie w temat.

**W skrócie:**

- Wielokrotne dziedziczenie jest potężne, ale wymaga ścisłych zasad projektowych.
- W większości przypadków kompozycja jest prostsza.
- Używaj go głównie dla niewielkich mixinów.

</details>

<details>
<summary>139. Czym są mixiny?</summary>

#### Python

Mixin to niewielka klasa z wąskim dodatkowym zachowaniem, przeznaczona do
łączenia przez dziedziczenie, a nie do samodzielnego użycia.

Przykłady: `TimestampMixin`, `JsonSerializableMixin`.

**W skrócie:**

- Mixin dodaje jedną konkretną możliwość.
- Zwykle nie ma własnego pełnego cyklu życia.
- Dobrze łączy się z wielokrotnym dziedziczeniem.

</details>

<details>
<summary>140. Czym jest enkapsulacja w Pythonie?</summary>

#### Python

Enkapsulacja to ukrywanie wewnętrznej implementacji za stabilnym publicznym API.
W Pythonie realizuje się to głównie przez konwencje i `property`, a nie przez
sztywne modyfikatory dostępu.

**W skrócie:**

- Kod kliencki pracuje z interfejsem, a nie z detalami.
- Enkapsulacja zmniejsza sprzężenie między komponentami.
- Ułatwia zmianę wewnętrznej implementacji bez psucia API.

</details>

<details>
<summary>141. Jaka jest różnica między dostępem publicznym, prywatnym i chronionym?</summary>

#### Python

W Pythonie są to głównie konwencje nazewnicze:

- `public`: `name` — dostępny wszędzie;
- `protected`: `_name` — do użytku wewnętrznego zgodnie z konwencją;
- `private`: `__name` — powoduje zmianę nazwy, czyli `_ClassName__name`, ale nie daje
  absolutnej ochrony.

**W skrócie:**

- Python nie ma ścisłych modyfikatorów dostępu jak Java czy C#.
- `_name` i `__name` są sygnałami intencji dla programistów.
- Realna kontrola dostępu wynika z projektu API.

</details>

<details>
<summary>142. Czym jest polimorfizm i jak jest realizowany w Pythonie?</summary>

#### Python

Polimorfizm to możliwość pracy z różnymi obiektami przez wspólny interfejs.
W Pythonie często realizuje się go przez typowanie oparte na zachowaniu i protokoły.

```python
def render(obj) -> str:
    return obj.to_text()
```

Każdy obiekt z metodą `to_text` będzie odpowiedni.

**W skrócie:**

- Jeden interfejs, wiele implementacji.
- W Pythonie polimorfizm jest często "behawioralny", a nie hierarchiczny.
- To upraszcza rozszerzanie systemu o nowe typy.

</details>

<details>
<summary>143. Czym jest abstrakcja w Pythonie?</summary>

#### Python

Abstrakcja to wyodrębnienie istotnego API i ukrycie zbędnych szczegółów implementacji.
Klient pracuje z kontraktem, a nie z wewnętrznymi krokami.

**W skrócie:**

- Abstrakcja zmniejsza obciążenie poznawcze.
- Ułatwia wymianę implementacji bez zmian w kodzie klienckim.
- Jest realizowana przez interfejsy, ABC, protokoły i fasady.

</details>

<details>
<summary>144. Jak zaimplementować abstrakcję danych?</summary>

#### Python

Podejście:

- ukryć bezpośredni dostęp do pól wewnętrznych, na przykład `_field`;
- udostępnić kontrolowane API przez metody albo `@property`;
- walidować inwarianty w logice settera.

```python
class Temperature:
    def __init__(self, celsius: float) -> None:
        self.celsius = celsius

    @property
    def celsius(self) -> float:
        return self._celsius

    @celsius.setter
    def celsius(self, value: float) -> None:
        if value < -273.15:
            raise ValueError("invalid temperature")
        self._celsius = value
```

**W skrócie:**

- Abstrakcja danych chroni inwarianty obiektu.
- `property` daje kontrolowany dostęp do stanu.
- Szczegóły wewnętrzne można zmieniać bez zmiany API.

</details>

<details>
<summary>145. Czym są ABC i `@abstractmethod`?</summary>

#### Python

ABC, czyli Abstract Base Class, to abstrakcyjna klasa bazowa z modułu `abc`.
`@abstractmethod` oznacza metodę, którą podklasa musi obowiązkowo zaimplementować.

```python
from abc import ABC, abstractmethod

class Storage(ABC):
    @abstractmethod
    def save(self, data: bytes) -> None:
        ...
```

**W skrócie:**

- ABC formalizuje kontrakt hierarchii.
- `@abstractmethod` uniemożliwia utworzenie instancji niepełnej implementacji.
- To przydatne w architekturach wtyczkowych i rozszerzalnych.

</details>

<details>
<summary>146. Czym jest property w Pythonie i jak się go używa?</summary>

#### Python

`property` zamienia metody dostępowe w API przypominające atrybut, z możliwością
walidacji, obliczeń albo logiki leniwej.

```python
class User:
    def __init__(self, name: str) -> None:
        self._name = name

    @property
    def name(self) -> str:
        return self._name
```

**W skrócie:**

- `property` daje kontrolę dostępu bez zmiany zewnętrznej składni.
- Nadaje się do walidacji i wartości pochodnych.
- Pozwala rozwijać API bez psucia kodu klientów.

</details>

<details>
<summary>147. Czym jest `@property`?</summary>

#### Python

`@property` to dekorator dla metody getter. Razem z `@x.setter` i `@x.deleter`
tworzy kontrolowany atrybut.

**W skrócie:**

- `@property` pozwala odczytywać metodę jak pole.
- Pomaga enkapsulować wewnętrzną implementację.
- Często jest używane dla API zachowującego kompatybilność wsteczną.

</details>

<details>
<summary>148. Czym jest deskryptor w Pythonie?</summary>

#### Python

Deskryptor to obiekt, który implementuje `__get__`, `__set__` albo `__delete__`
i steruje dostępem do atrybutów innej klasy.

Na deskryptorach opierają się `property`, `classmethod` i `staticmethod`.

**W skrócie:**

- Deskryptor to niskopoziomowy mechanizm dostępu do atrybutów.
- Pozwala wielokrotnie używać logiki walidacji i pośredniczenia pól.
- To podstawa wielu technik metaprogramistycznych w Pythonie.

</details>

<details>
<summary>149. Czym różnią się property i deskryptor?</summary>

#### Python

`property` to gotowy wysokopoziomowy deskryptor dla jednego atrybutu. Własny
deskryptor to bardziej ogólny mechanizm, który można wielokrotnie wykorzystać
w wielu polach i klasach.

**W skrócie:**

- `property` jest prostsze i lokalne.
- Deskryptor jest bardziej elastyczny i skalowalny.
- `property` jest faktycznie zbudowane na protokole deskryptora.

</details>

<details>
<summary>150. Kiedy lepiej używać property, a kiedy deskryptora?</summary>

#### Python

Używaj `property`, gdy logika dotyczy jednego lub dwóch pól konkretnej klasy.
Używaj deskryptora, gdy tę samą logikę, na przykład walidację, rzutowanie czy
leniwą inicjalizację, trzeba wielokrotnie zastosować w wielu klasach.

**W skrócie:**

- Lokalna logika pola oznacza `property`.
- Wielokrotne użycie polityki dostępu oznacza deskryptor.
- Deskryptor opłaca się w dużych modelach domenowych.

</details>

<details>
<summary>151. Do czego używa się `setattr()`, `getattr()` i `hasattr()`? Jaka jest między nimi różnica?</summary>

#### Python

To funkcje dynamicznego dostępu do atrybutów:

- `getattr(obj, name[, default])` — odczytać atrybut;
- `setattr(obj, name, value)` — ustawić atrybut;
- `hasattr(obj, name)` — sprawdzić, czy istnieje.

```python
value = getattr(user, "email", None)
if not hasattr(user, "active"):
    setattr(user, "active", True)
```

**W skrócie:**

- `getattr/setattr/hasattr` służą do dynamicznej pracy z obiektami.
- Są przydatne w kodzie generycznym, serializacji i adapterach.
- Nie warto ich nadużywać, żeby nie stracić czytelności.

</details>

<details>
<summary>152. Wyjaśnij znaczenie metody `__set_name__` w deskryptorach Pythona i podaj przykład jej zastosowania.</summary>

#### Python

`__set_name__(self, owner, name)` jest wywoływana podczas tworzenia klasy i
przekazuje deskryptorowi nazwę atrybutu, do którego został przypisany.

```python
class Field:
    def __set_name__(self, owner, name): self.name = name
```

**W skrócie:**

- `__set_name__` inicjalizuje deskryptor kontekstem klasy.
- Pozwala tworzyć wielokrotnie używalne walidatory pól.
- Uruchamia się raz na etapie tworzenia klasy.

</details>

<details>
<summary>153. Czym jest `dataclass` i kiedy warto go używać?</summary>

#### Python

`@dataclass` automatycznie generuje powtarzalny kod, taki jak `__init__`, `__repr__`, `__eq__`.
Nadaje się do modeli danych bez złożonego zachowania.

```python
from dataclasses import dataclass
@dataclass(slots=True)
class User:
    name: str
    active: bool = True
```

**W skrócie:**

- `dataclass` skraca kod dla modeli danych.
- To dobry wybór dla DTO i konfiguracji.
- Przy złożonej walidacji często potrzebne są inne narzędzia.

</details>

<details>
<summary>154. Jaka jest różnica między `dataclass` a Pydantic?</summary>

#### Python

`dataclass` koncentruje się na wygodnym opisie struktury. Pydantic dodaje
walidację w czasie działania, parsowanie i serializację danych.

**W skrócie:**

- `dataclass` jest lżejszy i szybszy dla modeli wewnętrznych.
- Pydantic lepiej nadaje się do danych wejściowych i API.
- Wybór zależy od potrzeby walidacji podczas działania programu.

</details>

<details>
<summary>155. Czym są podpowiedzi typów i po co są potrzebne?</summary>

#### Python

Podpowiedzi typów to adnotacje typów w sygnaturach i zmiennych, które tworzą jawny kontrakt.
Poprawiają podpowiedzi IDE i analizę statyczną.

**W skrócie:**

- Podpowiedzi typów zwiększają zrozumiałość API.
- Pozwalają wcześniej wykrywać pewną klasę błędów.
- Są przydatne nawet w języku dynamicznym.

</details>

<details>
<summary>156. Jak działa statyczne sprawdzanie typów w `mypy`?</summary>

#### Python

`mypy` odczytuje adnotacje typów i analizuje kod bez uruchamiania, sprawdzając zgodność
typów. Dzięki temu wychwytuje błędy integracyjne przed wykonaniem programu.

**W skrócie:**

- `mypy` wykonuje sprawdzanie podobne do kompilacji dla Pythona.
- Najlepiej sprawdza się w CI.
- Tryby ścisłe zmniejszają liczbę błędów produkcyjnych.

</details>

<details>
<summary>157. Jak zapewnić bezpieczeństwo typów w projekcie Pythona?</summary>

#### Python

- konsekwentnie dodawać adnotacje typów do publicznego API;
- włączyć `mypy` albo `pyright` w CI;
- używać `TypedDict`, `Protocol` i generyków;
- minimalizować `Any` i niejawne rzutowania.

**W skrócie:**

- Bezpieczeństwo typów to proces, a nie jednorazowe działanie.
- Największy efekt daje bramka CI dla typów.
- Stopniowe zwiększanie rygoru działa lepiej niż podejście "big bang".

</details>

<details>
<summary>158. Czym jest `TypedDict`?</summary>

#### Python

`TypedDict` opisuje typowaną formę słownika: jakie klucze są oczekiwane i jakich
typów są ich wartości.

```python
from typing import TypedDict
class UserPayload(TypedDict): name: str; active: bool
```

**W skrócie:**

- `TypedDict` typuje `dict` o stałych kluczach.
- Jest wygodny dla struktur podobnych do JSON.
- Jest sprawdzany przez analizator statyczny.

</details>

<details>
<summary>159. Czym jest `Protocol` w typowaniu?</summary>

#### Python

`Protocol` opisuje kontrakt behawioralny, czyli typowanie strukturalne: typ jest zgodny,
jeśli ma wymagane metody i atrybuty, niezależnie od dziedziczenia.

**W skrócie:**

- `Protocol` realizuje typowanie oparte na zachowaniu w statycznym typowaniu.
- Zmniejsza silne powiązanie z konkretnymi klasami.
- Jest przydatny dla testowalnych i rozszerzalnych API.

</details>

<details>
<summary>160. Czym są generyki w Pythonie?</summary>

#### Python

Generyki pozwalają pisać typy i funkcje parametryzowane innymi typami. We
współczesnej składni: `class Box[T]: ...`, `def first[T](...) -> T`.

**W skrócie:**

- Generyki sprawiają, że typy stają się wielokrotnego użytku.
- Wzmacniają bezpieczeństwo typów kolekcji i kontenerów.
- Zmniejszają duplikację typowanego kodu.

</details>

<details>
<summary>161. Czym jest Pydantic i do czego jest używany?</summary>

#### Python

Pydantic to biblioteka do opisywania schematów danych z walidacją w czasie działania,
konwersją typów i wygodną serializacją.

Typowe zastosowania to modele żądania i odpowiedzi w FastAPI oraz konfiguracja aplikacji.

**W skrócie:**

- Pydantic waliduje dane zewnętrzne podczas działania programu.
- Jest wygodny dla API i integracji.
- Daje czytelne błędy walidacji i schematy danych.

</details>

<details>
<summary>162. Czym są wyjątki w Pythonie?</summary>

#### Python

Wyjątek to obiekt sygnalizujący błędną albo wyjątkową sytuację podczas wykonywania kodu.

**W skrócie:**

- Wyjątki przerywają normalny przepływ wykonania.
- Należy je obsługiwać tam, gdzie można podjąć decyzję.
- Poprawny model błędów zwiększa niezawodność systemu.

</details>

<details>
<summary>163. Jakie są trzy typy błędów w Pythonie i czym się różnią?</summary>

#### Python

- błędy składniowe: pojawiają się przed uruchomieniem;
- wyjątki czasu wykonania: pojawiają się w trakcie działania;
- błędy logiczne: kod działa, ale zwraca niepoprawny wynik.

**W skrócie:**

- Błędy składniowe i część błędów wykonania wychwytuje interpreter.
- Błędy logiczne wykrywa się testami i przeglądem kodu.
- Każdy typ wymaga innego podejścia diagnostycznego.

</details>

<details>
<summary>164. Jak używać `try`, `except`, `else` i `finally`?</summary>

#### Python

`try` zawiera ryzykowną operację, `except` obsługuje błąd, `else` wykonuje się,
gdy błędu nie było, a `finally` wykonuje się zawsze, zwykle przy czyszczeniu zasobów.

```python
try: data = load()
except FileNotFoundError: data = {}
else: validate(data)
finally: close_connections()
```

**W skrócie:**

- `else` warto zostawić dla kodu "ścieżki sukcesu".
- `finally` służy do zasobów i czyszczenia.
- Łap konkretne wyjątki, a nie "wszystko po kolei".

</details>

<details>
<summary>165. Co oznacza kolejność bloków `except`?</summary>

#### Python

Bloki `except` są sprawdzane od góry do dołu, dlatego najpierw umieszcza się
najbardziej konkretne wyjątki, a ogólne, takie jak `Exception`, na końcu.

**W skrócie:**

- Kolejność `except` wpływa na to, który obsługujący blok zostanie uruchomiony.
- Szeroki `except` na górze "połyka" przypadki specyficzne.
- To krytyczne dla poprawnego przepływu odzyskiwania po błędzie.

</details>

<details>
<summary>166. Jakie jest przeznaczenie słowa kluczowego `assert` w kodzie Pythona?</summary>

#### Python

`assert` sprawdza inwariant i zgłasza `AssertionError`, jeśli warunek jest fałszywy.
Nadaje się do wewnętrznych kontroli deweloperskich, a nie do walidacji danych wejściowych użytkownika.

**W skrócie:**

- `assert` dokumentuje, że "to powinno być prawdziwe".
- Nie zastępuje produkcyjnej obsługi błędów.
- Używaj go do kontraktów w logice wewnętrznej.

</details>

<details>
<summary>167. Czym `raise` różni się od zwykłego wypisania komunikatu o błędzie w Pythonie?</summary>

#### Python

`raise` zmienia przepływ sterowania i sygnalizuje błąd kodowi wywołującemu.
`print` tylko wypisuje tekst i nie zatrzymuje błędnego scenariusza.

**W skrócie:**

- `raise` jest mechanizmem obsługi błędów, a `print` nie.
- Wyjątki można centralnie przechwytywać i logować.
- `print` służy do diagnostyki, a nie do kontraktu błędów.

</details>

<details>
<summary>168. Jak utworzyć własny wyjątek?</summary>

#### Python

Utwórz klasę dziedziczącą po `Exception` albo po bardziej konkretnym wyjątku bazowym.

```python
class InvalidOrderError(Exception):
    pass
```

**W skrócie:**

- Własny wyjątek czyni błędy bardziej wyrazistymi domenowo.
- Pozwala precyzyjnie przechwytywać potrzebne przypadki.
- Często jest lepszy niż używanie wszędzie ogólnego `ValueError`.

</details>

<details>
<summary>169. Jakie znaczenie ma tworzenie własnych wyjątków w Pythonie i jak poprawiają one obsługę błędów?</summary>

#### Python

Własne wyjątki budują jawny model błędów domeny i oddzielają problemy techniczne
od reguł biznesowych.

**W skrócie:**

- Poprawiają czytelność i utrzymanie obsługi błędów.
- Dają precyzyjniejszą semantykę w logach i API.
- Ułatwiają testowanie scenariuszy negatywnych.

</details>

<details>
<summary>170. Jak są zorganizowane wyjątki w Pythonie i jaka jest hierarchia klas wyjątków?</summary>

#### Python

Hierarchia jest zbudowana od `BaseException`. W kodzie aplikacyjnym prawie zawsze
pracuje się z potomkami `Exception`.

Kluczowe gałęzie to `ValueError`, `TypeError`, `KeyError`, `OSError`, `RuntimeError`.

**W skrócie:**

- Wyjątki tworzą drzewo klas.
- Lepiej przechwytywać konkretne podklasy.
- `BaseException` zwykle nie jest przechwytywany w logice biznesowej.

</details>

<details>
<summary>171. Jakie są podejścia do obsługi kilku różnych wyjątków w Pythonie i dlaczego warto obsługiwać je osobno?</summary>

#### Python

Podejścia:

- osobne `except` dla każdego typu;
- grupowanie logicznie podobnych przypadków: `except (A, B):`;
- osobne strategie odzyskiwania dla każdej kategorii.

**W skrócie:**

- Różne wyjątki często wymagają różnych działań.
- Osobna obsługa zmniejsza ryzyko ukrytych defektów.
- Logi stają się dokładniejsze i bardziej użyteczne.

</details>

<details>
<summary>172. Po co ponownie zgłaszać wyjątek w Pythonie i kiedy jest to przydatne?</summary>

#### Python

Ponowne zgłoszenie wyjątku, czyli `raise` bez argumentów w `except`, pozwala dodać
kontekst, na przykład logi, metryki albo czyszczenie, i przekazać ten sam błąd wyżej.

**W skrócie:**

- Ponowne zgłoszenie zachowuje pierwotny ślad stosu.
- Jest przydatne przy scentralizowanej obsłudze na wyższym poziomie.
- Nie "połykaj" krytycznych błędów bez potrzeby.

</details>

<details>
<summary>173. Dlaczego użycie bloku try-except warto ograniczać w programach Pythona i jak wpływa to na wydajność?</summary>

#### Python

`try/except` jest potrzebne, ale nie powinno obejmować dużych bloków "na wszelki wypadek".
Jest to szczególnie kosztowne, gdy wyjątki pojawiają się często i sterują przepływem programu.

**W skrócie:**

- Przechwytuj tylko oczekiwane błędy w możliwie wąskim miejscu.
- Częste wyjątki pogarszają wydajność i czytelność.
- Tam, gdzie to ma sens, lepsze są jawne sprawdzenia.

</details>

<details>
<summary>174. Jak obsługiwać błędy podczas pracy z plikami?</summary>

#### Python

Używaj `with` i przechwytuj konkretne wyjątki, takie jak `FileNotFoundError`,
`PermissionError`, `UnicodeDecodeError` i `OSError`.

```python
try:
    with open(path, "r", encoding="utf-8") as f:
        content = f.read()
except FileNotFoundError:
    ...
```

**W skrócie:**

- `with` gwarantuje zamknięcie pliku.
- Obsługuj konkretne błędy wejścia i wyjścia.
- Loguj kontekst, taki jak ścieżka, tryb i kodowanie.

</details>

<details>
<summary>175. Jakie są tryby pracy z plikami w Pythonie?</summary>

#### Python

Podstawowe tryby:

- `r` odczyt;
- `w` nadpisanie;
- `a` dopisywanie na końcu;
- `x` utworzenie nowego pliku;
- `b` tryb binarny;
- `t` tryb tekstowy, domyślny;
- `+` odczyt i zapis.

**W skrócie:**

- Tryb określa semantykę bezpieczeństwa i zmian w pliku.
- `w` usuwa poprzednią zawartość, a `a` ją zachowuje.
- Dla danych bajtowych używaj `b`.

</details>

<details>
<summary>176. Dlaczego ważne jest zamykanie plików po operacjach i co może się stać, jeśli plik pozostanie otwarty?</summary>

#### Python

Otwarty plik utrzymuje deskryptor systemu operacyjnego. Jeśli go nie zamknąć, mogą wystąpić:

- wyciek deskryptorów plików;
- blokady plików lub niepełne opróżnienie bufora;
- niestabilność w długotrwałych procesach.

**W skrócie:**

- Zamknięcie pliku zwalnia zasoby systemu operacyjnego.
- `with` automatyzuje bezpieczne zamykanie.
- To krytyczne dla usług i skryptów wsadowych.

</details>

<details>
<summary>177. Jaka jest różnica między metodami `read()`, `readline()` i `readlines()` przy odczycie plików?</summary>

#### Python

- `read()` czyta cały plik albo `n` bajtów lub znaków;
- `readline()` czyta jeden wiersz;
- `readlines()` czyta wszystkie wiersze do listy.

**W skrócie:**

- `read()` i `readlines()` mogą być kosztowne pamięciowo.
- Dla dużych plików lepsza jest iteracja `for line in file`.
- Wybór zależy od rozmiaru i scenariusza przetwarzania.

</details>

<details>
<summary>178. Jak zapisać dane do pliku w Pythonie i jaka jest różnica między trybem `w` a `a`?</summary>

#### Python

Zapis:

```python
with open("out.txt", "w", encoding="utf-8") as f:
    f.write("hello\n")
```

`w` nadpisuje plik od początku, a `a` dopisuje nową treść na końcu.

**W skrócie:**

- `w` usuwa stare dane.
- `a` zachowuje istniejącą zawartość.
- Do logów zwykle używa się `a`.

</details>

<details>
<summary>179. Jak efektywnie pracować z dużymi plikami?</summary>

#### Python

- czytać strumieniowo, po wierszach albo blokach;
- unikać ładowania całego pliku do pamięci;
- używać buforowania i generatorów;
- dla danych kolumnowych i tabelarycznych dobierać odpowiednie formaty i parsery.

**W skrócie:**

- Klucz to przetwarzanie strumieniowe zamiast pełnego odczytu.
- Generatory zmniejszają zużycie pamięci.
- Algorytm przetwarzania jest ważniejszy niż mikrooptymalizacje.

</details>

<details>
<summary>180. Czym są menedżery kontekstu?</summary>

#### Python

Menedżer kontekstu zarządza zasobem przez protokół `__enter__/__exit__`:
otwarcie lub inicjalizację oraz gwarantowane zakończenie i czyszczenie.

**W skrócie:**

- Zapewnia bezpieczny cykl życia zasobu.
- Działa przez `with`.
- Zmniejsza liczbę wycieków zasobów.

</details>

<details>
<summary>181. Jak działa konstrukcja `with`?</summary>

#### Python

`with` wywołuje `__enter__` przy wejściu do bloku i `__exit__` przy wyjściu,
nawet jeśli wystąpił błąd.

```python
with open("data.txt", "r", encoding="utf-8") as f:
    data = f.read()
```

**W skrócie:**

- `with` gwarantuje czyszczenie zasobów.
- Sprawia, że praca z zasobami jest deklaratywna.
- Jest zalecany dla plików, blokad, transakcji i sesji.

</details>

<details>
<summary>182. Jak utworzyć własny menedżer kontekstu?</summary>

#### Python

Dwa podejścia:

- klasa z `__enter__` i `__exit__`;
- funkcja z dekoratorem `contextlib.contextmanager`.

```python
from contextlib import contextmanager

@contextmanager
def temp_flag():
    yield
```

**W skrócie:**

- Klasa nadaje się do złożonego stanu.
- `contextmanager` jest wygodny dla krótkich scenariuszy.
- Oba podejścia dają gwarantowane czyszczenie.

</details>

<details>
<summary>183. Jak Python zarządza pamięcią?</summary>

#### Python

CPython używa zliczania referencji i cyklicznego mechanizmu odśmiecania pamięci. Dodatkowo
ma wewnętrzny alokator `pymalloc` dla małych obiektów.

**W skrócie:**

- Podstawowy mechanizm to licznik referencji.
- GC usuwa cykliczne referencje.
- Pamięć nie zawsze jest zwalniana natychmiast na poziomie systemu operacyjnego.

</details>

<details>
<summary>184. Czym jest zliczanie referencji w Pythonie i dlaczego jest ważne dla zarządzania pamięcią?</summary>

#### Python

Każdy obiekt ma licznik referencji. Gdy spada on do zera, obiekt można
zwolnić. Zapewnia to szybkie usuwanie większości krótkotrwałych obiektów.

**W skrócie:**

- Zliczanie referencji daje przewidywalny cykl życia obiektów.
- Samodzielnie nie rozwiązuje problemu cyklicznych referencji.
- Razem z GC tworzy pełny model zarządzania pamięcią.

</details>

<details>
<summary>185. Czym jest odśmiecanie pamięci w Pythonie?</summary>

#### Python

Odśmiecanie pamięci w CPython znajduje i usuwa nieosiągalne cykle obiektów, których
nie da się wyczyścić wyłącznie przez zliczanie referencji.

**W skrócie:**

- GC uzupełnia zliczanie referencji.
- Jest szczególnie ważny dla cyklicznych grafów referencji.
- Można nim sterować przez moduł `gc`.

</details>

<details>
<summary>186. Jak uzyskać adres pamięci obiektu w Pythonie?</summary>

#### Python

W CPython `id(obj)` często odpowiada adresowi obiektu w pamięci jako liczba całkowita.
To narzędzie diagnostyczne, a nie stabilny identyfikator zewnętrzny.

**W skrócie:**

- `id()` daje tożsamość obiektu.
- W CPython zwykle jest to adres pamięci.
- Nie używaj tego w logice biznesowej.

</details>

<details>
<summary>187. Do czego służy funkcja `getrefcount()` z modułu `sys` i jak działa w Pythonie?</summary>

#### Python

`sys.getrefcount(obj)` zwraca bieżący licznik referencji do obiektu w CPython.
Wartość jest zwykle o 1 większa przez tymczasową referencję argumentu.

**W skrócie:**

- To narzędzie diagnostyki zachowania pamięci.
- Jest przydatne do analizy wycieków referencji.
- Nie należy na nim polegać w logice aplikacyjnej.

</details>

<details>
<summary>188. Wyjaśnij na przykładach różnicę między obiektami mutable i immutable w kontekście zliczania referencji i zarządzania pamięcią.</summary>

#### Python

Obiekty immutable się nie zmieniają, więc ich "zmiana" tworzy nowy obiekt.
Obiekty mutable zmieniają się in-place i wszystkie referencje widzą tę zmianę.

```python
a = "x"; b = a; a += "y"    # nowy obiekt
x = [1]; y = x; y.append(2) # zmiana tego samego obiektu
```

**W skrócie:**

- Obiekty immutable zmniejszają liczbę efektów ubocznych.
- Obiekty mutable są bardziej efektywne przy modyfikacjach in-place.
- Ta różnica jest krytyczna przy kopiowaniu i współdzielonych referencjach.

</details>

<details>
<summary>189. Jaka jest różnica między kopią płytką a kopią głęboką w Pythonie i kiedy używać każdego z tych podejść?</summary>

#### Python

Kopia płytka kopiuje tylko zewnętrzny kontener, a zagnieżdżone obiekty pozostają
współdzielone. Kopia głęboka rekurencyjnie kopiuje całą strukturę.

```python
import copy
copy.copy(obj)
copy.deepcopy(obj)
```

**W skrócie:**

- Kopia płytka wystarcza dla "płaskich" struktur.
- Kopia głęboka jest potrzebna do izolowanej pracy z zagnieżdżonymi danymi mutable.
- Kopia głęboka jest droższa czasowo i pamięciowo.

</details>

<details>
<summary>190. Czym są moduły i pakiety w Pythonie?</summary>

#### Python

Moduł to osobny plik `.py` z kodem. Pakiet to katalog modułów, czyli przestrzeń nazw,
która organizuje kod w większe bloki.

**W skrócie:**

- Moduł to jednostka kodu.
- Pakiet to struktura do skalowania modułów.
- Podział na moduły i pakiety poprawia utrzymywalność.

</details>

<details>
<summary>191. Jak importować moduł w Pythonie?</summary>

#### Python

Podstawowe formy:

- `import module`;
- `import module as m`;
- `from module import name`;
- `from package import submodule`.

**W skrócie:**

- Import ładuje moduł i udostępnia go w przestrzeni nazw.
- Alias `as` poprawia czytelność i pomaga unikać konfliktów.
- Warto preferować jawne importy.

</details>

<details>
<summary>192. Jakie są typy importów?</summary>

#### Python

Popularne typy:

- bezwzględne;
- względne;
- wybiórcze, jak `from x import y`;
- importy z aliasem przez `as`;
- dynamiczne, z użyciem `importlib`.

**W skrócie:**

- Typ importu wpływa na czytelność i utrzymanie.
- W kodzie produkcyjnym najczęściej używa się importów bezwzględnych.
- Importy dynamiczne stosuje się punktowo.

</details>

<details>
<summary>193. Jak działa system importów?</summary>

#### Python

Interpreter szuka modułu według `sys.path`, ładuje go tylko raz i zapisuje w
`sys.modules`. Ponowny import korzysta z pamięci podręcznej.

**W skrócie:**

- Import to wyszukiwanie, wykonanie modułu i zapisanie go w pamięci podręcznej.
- To wyjaśnia, dlaczego kod modułu uruchamia się przy pierwszym imporcie.
- Cykliczne importy wynikają z kolejności inicjalizacji modułów.

</details>

<details>
<summary>194. Jaka jest różnica między importem bezwzględnym a względnym?</summary>

#### Python

Import bezwzględny zaczyna się od korzenia pakietu, na przykład `from app.utils import x`.
Import względny używa kropek, na przykład `from .utils import x`.

**W skrócie:**

- Importy bezwzględne są czytelniejsze i stabilniejsze.
- Względne bywają wygodne wewnątrz pakietu, ale gorzej znoszą refaktoryzację.
- W dużych projektach lepiej standardowo trzymać się importów bezwzględnych.

</details>

<details>
<summary>195. Co robi funkcja `dir()` i jak można jej używać względem modułów?</summary>

#### Python

`dir(obj)` zwraca listę dostępnych atrybutów i nazw obiektu. W przypadku modułów
to szybki sposób na podejrzenie API.

```python
import math
dir(math)
```

**W skrócie:**

- `dir()` pomaga w interaktywnym poznawaniu modułów.
- Jest przydatne w REPL i podczas debugowania.
- Nie zastępuje oficjalnej dokumentacji.

</details>

<details>
<summary>196. Wyjaśnij rolę konstrukcji `if __name__ == "__main__":` w skryptach Pythona.</summary>

#### Python

Ten blok wykonuje się tylko wtedy, gdy plik jest uruchamiany jako skrypt, a nie importowany
jako moduł. Rozdziela to kod wielokrotnego użytku od punktu wejścia CLI.

**W skrócie:**

- Pozwala moduł zarówno uruchamiać, jak i importować.
- Zapobiega niechcianemu wykonaniu podczas importu.
- To standardowy wzorzec dla skryptów.

</details>

<details>
<summary>197. Co oznacza plik `__init__.py` w pakiecie Pythona?</summary>

#### Python

`__init__.py` oznacza katalog jako pakiet i może inicjalizować API na poziomie pakietu,
na przykład przez ponowny eksport klas i funkcji.

**W skrócie:**

- Tworzy publiczny interfejs pakietu.
- Może zawierać minimalną inicjalizację.
- Nie warto przeciążać go ciężką logiką.

</details>

<details>
<summary>198. Jakie są najlepsze praktyki dotyczące stylu importów w kodzie Pythona?</summary>

#### Python

- grupować importy: biblioteka standardowa, zewnętrzne i lokalne;
- unikać `from x import *`;
- trzymać importy na początku pliku, poza uzasadnionymi przypadkami leniwego importu;
- używać sortowania i formatowania, na przykład `ruff` oraz `isort`.

**W skrócie:**

- Spójne importy poprawiają czytelność.
- Jawne importy zmniejszają konflikty nazw.
- Automatyzacja narzędziami eliminuje ręczne błędy.

</details>

<details>
<summary>199. Jakie popularne moduły wbudowane istnieją w Pythonie?</summary>

#### Python

Przykłady popularnych modułów biblioteki standardowej:

- `os`, `sys`, `pathlib`, `json`, `datetime`, `re`,
- `collections`, `itertools`, `functools`, `typing`,
- `asyncio`, `subprocess`, `logging`, `argparse`.

**W skrócie:**

- Biblioteka standardowa pokrywa większość podstawowych zadań.
- To zmniejsza liczbę zależności zewnętrznych.
- Warto dobrze znać bibliotekę standardową przed dodawaniem pakietów zewnętrznych.

</details>
<details>
<summary>200. Co wiesz o pakiecie `collections` i jakie inne moduły wbudowane były używane?</summary>

#### Python

`collections` udostępnia wysokopoziomowe struktury:

- `Counter`, `defaultdict`, `deque`, `namedtuple`, `ChainMap`.

Typowo łączy się go z:

- `itertools` do potoków iteracyjnych;
- `functools` do buforowania wyników i narzędzi funkcyjnych;
- `pathlib`, `json`, `datetime` w zadaniach praktycznych.

**W skrócie:**

- `collections` rozszerza podstawowe kontenery o praktyczne struktury.
- Często zwiększa prostotę i wydajność kodu.
- Dobrze współpracuje z `itertools` i `functools`.

</details>

<details>
<summary>201. Co zwraca `sys.argv`?</summary>

#### Python

`sys.argv` zwraca listę argumentów wiersza poleceń:

- `sys.argv[0]` to nazwa skryptu;
- pozostałe elementy to przekazane argumenty.

**W skrócie:**

- `sys.argv` to podstawowy interfejs argumentów CLI.
- Wartości przychodzą jako napisy.
- Dla bardziej złożonych CLI lepsze jest `argparse`.

</details>

<details>
<summary>202. Jaki jest główny moduł do pracy z systemem operacyjnym w Pythonie?</summary>

#### Python

Podstawowym modułem jest `os`, razem z `os.path`, a dla nowoczesnego API ścieżek
zalecany jest `pathlib`.

**W skrócie:**

- `os` daje dostęp do API procesów, środowiska i systemu plików.
- `pathlib` jest wygodniejszy do pracy ze ścieżkami.
- W realnych projektach często używa się obu.

</details>

<details>
<summary>203. Jak przetasować elementy listy za pomocą modułu `random`?</summary>

#### Python

Użyj `random.shuffle(list_)` do tasowania in-place.

```python
import random
items = [1, 2, 3, 4]
random.shuffle(items)
```

**W skrócie:**

- `shuffle` zmienia oryginalną listę.
- Działa tylko z mutowalnymi sekwencjami, na przykład listami.
- Aby otrzymać nową kopię, użyj `random.sample(items, k=len(items))`.

</details>

<details>
<summary>204. Czym jest środowisko wirtualne?</summary>

#### Python

Środowisko wirtualne to izolowane środowisko Pythona z własnymi pakietami i
wersjami zależności dla konkretnego projektu.

**W skrócie:**

- Izolacja usuwa konflikty zależności między projektami.
- Standardowym narzędziem jest `venv`.
- To podstawowa praktyka dla odtwarzalnego rozwoju projektu.

</details>

<details>
<summary>205. Jak działa `pip`?</summary>

#### Python

`pip` instaluje, aktualizuje i usuwa pakiety z indeksów, najczęściej z PyPI,
rozwiązuje zależności i instaluje je w bieżącym środowisku.

**W skrócie:**

- `pip` to standardowy menedżer pakietów Pythona.
- Działa w obrębie aktywnego venv i interpretera.
- Dla stabilności ważne są przypięte wersje.

</details>

<details>
<summary>206. Czym jest `requirements.txt`?</summary>

#### Python

`requirements.txt` to plik z listą zależności, często z dokładnymi wersjami,
używany do odtwarzalnej instalacji.

**W skrócie:**

- Format jest prosty i zgodny z `pip install -r`.
- W środowisku produkcyjnym najlepiej przypinać dokładne wersje.
- Często jest generowany narzędziami, na przykład `pip-tools` albo `poetry export`,
  na podstawie deklaratywnej listy zależności lub plików lock.

</details>

<details>
<summary>207. Czym jest `pyproject.toml` i dlaczego stał się standardem?</summary>

#### Python

`pyproject.toml` to ustandaryzowany plik konfiguracji projektu: metadane pakietu,
system budowania i ustawienia narzędzi, takich jak `ruff`, `pytest`, `mypy`.

**W skrócie:**

- Centralizuje konfigurację projektu Python.
- Jest wspierany przez nowoczesne narzędzia pakowania.
- Zmniejsza liczbę rozproszonych plików konfiguracyjnych.

</details>

<details>
<summary>208. Jak zarządzać zależnościami w nowoczesnym projekcie Pythona?</summary>

#### Python

- izolować środowisko przez `venv`;
- definiować zależności w `pyproject.toml`;
- przypinać pliki lock albo constraints dla odtwarzalności;
- regularnie aktualizować z kontrolą przez CI.

**W skrócie:**

- Zarządzanie zależnościami powinno być odtwarzalne.
- Nie mieszaj pakietów globalnych i projektowych.
- Aktualizacje wykonuj w kontrolowany sposób, przez testy.

</details>

<details>
<summary>209. Jak poprawnie zorganizować strukturę dużego projektu Pythona?</summary>

#### Python

- podzielić kod na pakiety domenowe;
- mieć osobne warstwy, takie jak `api`, `services`, `domain`, `infrastructure`;
- wydzielić `tests/`, `scripts/`, `configs/`;
- utrzymywać jawne granice modułów i publiczne API.

**W skrócie:**

- Struktura powinna odzwierciedlać domenę, a nie przypadkowe szczegóły techniczne.
- Wyraźne granice zmniejszają liczbę cyklicznych zależności.
- Testy i narzędzia powinny być pełnoprawną częścią drzewa projektu.

</details>

<details>
<summary>210. Jaka jest różnica między testowaniem automatycznym a ręcznym i jakie są zalety testowania automatycznego?</summary>

#### Python

Testowanie ręczne wykonuje człowiek krok po kroku. Testowanie automatyczne
jest wykonywane przez skrypty albo struktury testowe.

**W skrócie:**

- Testy automatyczne są szybkie, powtarzalne i nadają się do CI.
- Testowanie ręczne jest przydatne dla eksploracyjnych scenariuszy UX.
- W praktyce produkcyjnej potrzebne jest połączenie obu podejść.

</details>

<details>
<summary>211. Czym jest TDD (Test-Driven Development)?</summary>

#### Python

TDD to cykl: napisać nieprzechodzący test -> minimalna implementacja -> refaktoryzacja.

**W skrócie:**

- TDD kształtuje API przez testy.
- Daje szybki sygnał zwrotny o regresjach.
- Najlepiej sprawdza się w modułowej logice biznesowej.

</details>

<details>
<summary>212. Jakie są popularne narzędzia testowe w Pythonie?</summary>

#### Python

Najpopularniejsze to `pytest`, `unittest` z biblioteki standardowej oraz `hypothesis`
do testów opartych na właściwościach.

**W skrócie:**

- `pytest` jest najczęściej wybierany do nowych projektów.
- `unittest` jest przydatny jako standardowe podstawowe narzędzie.
- `hypothesis` wzmacnia pokrycie przypadków brzegowych.

</details>

<details>
<summary>213. Czym jest `unittest` w Pythonie?</summary>

#### Python

`unittest` to wbudowane narzędzie w stylu xUnit do testów: klasy przypadków testowych,
metody asercji, przygotowanie i sprzątanie oraz uruchamianie testów.

**W skrócie:**

- Jest częścią biblioteki standardowej.
- Nadaje się do konserwatywnych środowisk bez zależności zewnętrznych.
- Ma bardziej rozbudowaną składnię niż `pytest`.

</details>

<details>
<summary>214. Czym jest `pytest` i czym różni się od `unittest` pod względem składni i funkcjonalności?</summary>

#### Python

`pytest` to narzędzie z prostą składnią testów funkcyjnych, rozbudowanymi
fixture'ami, parametryzacją i ekosystemem wtyczek.

**W skrócie:**

- `pytest` ma mniej szablonowy styl i jest wygodniejszy dla dużych zestawów testów.
- `unittest` jest oparty na klasach i standardowy w bibliotece standardowej.
- W nowoczesnych projektach dominuje `pytest`.

</details>

<details>
<summary>215. Opisz, jak metoda `pytest.raises` jest używana do testowania wystąpienia konkretnych wyjątków w kodzie Pythona.</summary>

#### Python

`pytest.raises(ExpectedError)` sprawdza, czy blok kodu zgłasza dokładnie oczekiwany
wyjątek.

```python
import pytest
with pytest.raises(ValueError):
    int("abc")
```

**W skrócie:**

- Jawnie testuje scenariusze negatywne.
- Chroni przed "cichym" przechodzeniem błędów.
- Może też sprawdzać komunikat lub atrybuty wyjątku.

</details>

<details>
<summary>216. Czym jest parametryzacja w testach i jak pytest wspiera ją przez `@pytest.mark.parametrize`?</summary>

#### Python

Parametryzacja uruchamia jeden test dla kilku zestawów danych wejściowych. W pytest
robi się to dekoratorem `@pytest.mark.parametrize`.

**W skrócie:**

- Daje mniej duplikacji kodu testowego.
- Łatwo skalować przypadki.
- Zwiększa przejrzystość pokrycia scenariuszy wejściowych.

</details>

<details>
<summary>217. Jak w pytest nadać własne nazwy testom w parametryzacji dla lepszej czytelności?</summary>

#### Python

Użyj parametru `ids` w `parametrize`.

```python
@pytest.mark.parametrize("value,expected", [(2, True), (3, False)], ids=["even", "odd"])
```

**W skrócie:**

- `ids` czyni wynik uruchomienia testów bardziej zrozumiałym.
- Ułatwia diagnozowanie niepowodzeń.
- Jest szczególnie przydatny przy dużej liczbie przypadków.

</details>

<details>
<summary>218. Czym jest etap przygotowania testu i dlaczego to ważne?</summary>

#### Python

Etap przygotowania testu to ustawienie stanu testowego: danych, obiektów, mocków i środowiska.
Dobrze przygotowane środowisko sprawia, że test jest deterministyczny.

**W skrócie:**

- Niestabilne przygotowanie oznacza niestabilne testy.
- Dobre przygotowanie izoluje test od efektów zewnętrznych.
- Jasny etap przygotowania poprawia czytelność scenariusza.

</details>

<details>
<summary>219. Jakie etapy obejmuje sprzątanie po teście i dlaczego to ważne?</summary>

#### Python

Sprzątanie po teście usuwa wszystko, co utworzył test: pliki tymczasowe, połączenia, mocki
i testowe rekordy w bazie danych.

**W skrócie:**

- Sprzątanie zapewnia izolację między testami.
- Zmniejsza efekty uboczne i niestabilność testów.
- W pytest wygodnie robi się to przez finalizery fixture i fixture oparte na `yield`.

</details>

<details>
<summary>220. Jaka jest różnica między metodami `setUp()` i `setUpClass()` w unittest?</summary>

#### Python

`setUp()` wykonuje się przed **każdą** metodą testową. `setUpClass()`
jako metoda klasowa wykonuje się **jeden raz** przed wszystkimi testami klasy.

**W skrócie:**

- `setUp` służy do izolacji na poziomie pojedynczego testu.
- `setUpClass` służy do kosztownych współdzielonych zasobów.
- Nadmierny współdzielony stan przez `setUpClass` może komplikować testy.

</details>

<details>
<summary>221. Czym jest obiekt pozorowany i jak pomaga podnieść jakość testów?</summary>

#### Python

Obiekt pozorowany to obiekt zastępczy, który imituje zależność i pozwala kontrolować
zachowanie oraz sprawdzać wywołania.

**W skrócie:**

- Mocki izolują testowaną jednostkę od usług zewnętrznych.
- Sprawiają, że testy są szybsze i stabilniejsze.
- Pozwalają sprawdzać interakcje, a nie tylko wynik.

</details>

<details>
<summary>222. Jaka jest różnica między użyciem `mock.patch` w unittest a `monkeypatch` w pytest do mockowania obiektów?</summary>

#### Python

`mock.patch` z `unittest.mock` podmienia obiekty według ścieżki importu i ma rozbudowane
API do sprawdzania wywołań. `monkeypatch` w pytest w prostszy sposób zmienia
atrybuty, zmienne środowiskowe i słowniki na czas testu.

**W skrócie:**

- `patch` jest potężniejszy w scenariuszach z asercjami na mockach.
- `monkeypatch` jest wygodny do szybkich testowych podmian.
- Często używa się ich łącznie, zależnie od przypadku.

</details>

<details>
<summary>223. Jakie jest przeznaczenie parametru `scope` w fixture'ach pytest?</summary>

#### Python

`scope` określa cykl życia fixture'a: `function`, `class`, `module`,
`package`, `session`.

**W skrócie:**

- Mniejszy scope oznacza lepszą izolację.
- Większy scope oznacza szybsze uruchamianie dużych zestawów testów.
- Wybór zasięgu to balans między szybkością a niezależnością.

</details>

<details>
<summary>224. Czym jest złożoność algorytmu i jak się ją określa?</summary>

#### Python

Złożoność algorytmu ocenia, jak rosną koszty czasu i pamięci wraz ze wzrostem
rozmiaru danych wejściowych `n`.

**W skrócie:**

- Mierzy się złożoność czasową i pamięciową.
- Ocena jest zwykle asymptotyczna.
- Pomaga wybierać algorytm i struktury danych.

</details>

<details>
<summary>225. Wyjaśnij pojęcie notacji Big O i jej znaczenie w ocenie złożoności algorytmów.</summary>

#### Python

Big O opisuje górną granicę wzrostu kosztu algorytmu przy dużym `n`,
pomijając stałe i składniki niższego rzędu.

**W skrócie:**

- Big O pokazuje skalowalność, a nie dokładny czas.
- Daje wspólny język do porównywania algorytmów.
- Jest krytycznie ważna dla wydajności przy dużych wolumenach danych.

</details>

<details>
<summary>226. Jakie rodzaje złożoności algorytmicznej występują najczęściej?</summary>

#### Python

Najczęstsze to `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`, `O(n^2)`.

**W skrócie:**

- `O(n)` i `O(n log n)` są najtypowsze w zadaniach praktycznych.
- `O(n^2)` i więcej często staje się wąskim gardłem.
- Trzeba brać pod uwagę także pamięć, a nie tylko czas.

</details>

<details>
<summary>227. Podaj przykłady zadań, które są efektywnie rozwiązywane przez algorytmy liniowe `O(n)`.</summary>

#### Python

Przykłady:

- szukanie maksimum i minimum;
- filtrowanie elementów;
- zliczanie częstotliwości przez `Counter`;
- sprawdzanie warunków dla każdego elementu.

**W skrócie:**

- `O(n)` oznacza jedno przejście po danych.
- To rozwiązanie optymalne dla wielu agregacji.
- Algorytmy liniowe dobrze się skalują.

</details>

<details>
<summary>228. Jak działa `lru_cache` i kiedy go używać?</summary>

#### Python

`functools.lru_cache` buforuje wyniki funkcji według argumentów i zwraca gotową
wartość przy kolejnych wywołaniach.

**W skrócie:**

- Jest skuteczny dla funkcji czystych z powtarzającymi się danymi wejściowymi.
- Nie nadaje się do funkcji z efektami ubocznymi.
- `maxsize` kontroluje rozmiar bufora w pamięci.

</details>

<details>
<summary>229. Jak profilować wydajność kodu Pythona?</summary>

#### Python

Podstawowe narzędzia:

- `timeit` do mikrobenchmarków;
- `cProfile` i `pstats` do profilowania na poziomie wywołań;
- `py-spy` i `scalene` do analizy zbliżonej do warunków produkcyjnych.

**W skrócie:**

- Optymalizuj dopiero po pomiarach.
- Profiluj realistyczne scenariusze obciążenia.
- Ustalaj punkt odniesienia przed i po zmianach.

</details>

<details>
<summary>230. Jakie są podstawowe sposoby optymalizacji kodu Pythona?</summary>

#### Python

- dobrać właściwe struktury danych;
- zmniejszyć złożoność asymptotyczną;
- unikać zbędnych kopii;
- używać generatorów i leniwych potoków;
- buforować kosztowne obliczenia;
- przenosić najbardziej gorące ścieżki do C, Rust lub NumPy, jeśli to potrzebne.

**W skrócie:**

- Największy zysk daje algorytm, a nie składniowa sztuczka.
- Optymalizacja musi opierać się na profilowaniu.
- Nie warto poświęcać czytelności bez zmierzonej korzyści.

</details>

<details>
<summary>231. Kiedy warto używać rozszerzeń C albo PyPy?</summary>

#### Python

Rozszerzenia C są zasadne dla wąskich gardeł CPU i integracji z bibliotekami
natywnymi. PyPy jest zasadne wtedy, gdy długowieczny czysty kod Pythona korzysta z kompilacji JIT.

**W skrócie:**

- Rozszerzenie C daje maksymalną wydajność kosztem złożoności budowania.
- PyPy daje potencjalny wzrost wydajności bez przepisywania kodu na C.
- Wybór powinien wynikać z pomiarów wydajności dla rzeczywistego obciążenia.

</details>

<details>
<summary>232. Czym jest profilowanie pamięci?</summary>

#### Python

Profilowanie pamięci to mierzenie, gdzie i ile pamięci zużywa kod w czasie, aby
znaleźć wycieki i kosztowne miejsca.

**W skrócie:**

- Pokazuje gorące miejsca pamięci i piki zużycia.
- Jest przydatne dla obciążeń wsadowych i przetwarzania danych.
- Narzędzia: `tracemalloc`, `memory_profiler`, `scalene`.

</details>

<details>
<summary>233. Czym jest GIL (globalna blokada interpretera)?</summary>

#### Python

GIL to mechanizm w CPython, który pozwala tylko jednemu wątkowi jednocześnie
wykonywać kod bajtowy Pythona w obrębie procesu.

**W skrócie:**

- GIL wpływa na wielowątkowość w zadaniach CPU-bound.
- W zadaniach I/O-bound wątki nadal są użyteczne.
- Do równoległości CPU częściej używa się multiprocessing.

</details>

<details>
<summary>234. Jak globalna blokada interpretera Pythona wpływa na współbieżność w CPython i jakie ma to konsekwencje dla wielowątkowości?</summary>

#### Python

Przez GIL wątki w CPython nie wykonują kodu bajtowego Pythona naprawdę równolegle
dla kodu CPU-bound. Przełączają się współbieżnie.

Konsekwencje:

- dla wątków I/O-bound efekt jest dobry, bo oczekiwanie na I/O może się nakładać;
- dla zadań CPU-bound zysk z wątków jest zwykle ograniczony.

**W skrócie:**

- GIL ogranicza równoległość wątków w scenariuszach CPU-bound.
- Wątki pozostają użyteczne dla sieci i dysku.
- Dla CPU lepiej używać procesów albo obliczeń natywnych.

</details>

<details>
<summary>235. Jak GIL wpływa na wydajność?</summary>

#### Python

GIL prawie nie przeszkadza w zadaniach I/O-bound, ale ogranicza przepustowość
wielowątkowego kodu Pythona CPU-bound w jednym procesie.

**W skrócie:**

- Wpływ GIL zależy od rodzaju obciążenia.
- CPU-bound plus wątki w CPython często się nie skaluje.
- Architekturę należy dobierać do profilu zadań.

</details>

<details>
<summary>236. Wyjaśnij koncepcję wielowątkowości w Pythonie i czym różni się od multiprocessing.</summary>

#### Python

`threading` uruchamia kilka wątków w jednym procesie ze współdzieloną pamięcią.
`multiprocessing` uruchamia osobne procesy z odrębną pamięcią.

**W skrócie:**

- Wątki są lżejsze i wygodne dla zadań I/O-bound.
- Procesy dają rzeczywistą równoległość CPU.
- Procesy mają większy narzut IPC i uruchamiania.

</details>

<details>
<summary>237. Kiedy używać multiprocessing zamiast threading?</summary>

#### Python

Gdy zadanie jest CPU-bound i wymaga użycia wielu rdzeni w CPython. Przykłady:
ciężkie parsowanie, przetwarzanie obrazu i wideo, obliczenia numeryczne.

**W skrócie:**

- CPU-bound zwykle oznacza `multiprocessing`.
- I/O-bound zwykle oznacza `threading` albo `asyncio`.
- Trzeba uwzględniać koszt serializacji między procesami.

</details>

<details>
<summary>238. Jaka jest różnica między współbieżnością a równoległością w programowaniu i kiedy której z nich używać?</summary>

#### Python

Współbieżność oznacza nakładanie się zadań w czasie. Równoległość oznacza
fizyczne wykonywanie zadań jednocześnie na kilku rdzeniach.

**W skrócie:**

- Współbieżność jest przydatna przy opóźnieniach I/O.
- Równoległość jest potrzebna dla obliczeń intensywnie obciążających CPU.
- W Pythonie wybór narzędzia zależy od rodzaju wąskiego gardła.

</details>

<details>
<summary>239. Czym jest współbieżność w Pythonie?</summary>

#### Python

Współbieżność w Pythonie to organizacja wykonywania wielu zadań tak, aby
postępowały współbieżnie: przez wątki, `asyncio` albo procesy.

**W skrócie:**

- Chodzi o zarządzanie wieloma zadaniami, niekoniecznie równolegle.
- Pozwala zwiększyć przepustowość scenariuszy I/O.
- Wymaga starannego projektowania synchronizacji i anulowania.

</details>

<details>
<summary>240. Jaka jest różnica między zadaniami I/O-bound a CPU-bound?</summary>

#### Python

Zadania I/O-bound głównie czekają na sieć, dysk albo bazę danych. Zadania CPU-bound
spędzają większość czasu na obliczeniach procesora.

**W skrócie:**

- I/O-bound dobrze skaluje się przez `asyncio` i wątki.
- CPU-bound lepiej skaluje się przez `multiprocessing` i kod natywny.
- Najpierw określ wąskie gardło przez profilowanie.

</details>

<details>
<summary>241. Do czego służy moduł `asyncio` w Pythonie i jak pozwala realizować programowanie asynchroniczne?</summary>

#### Python

`asyncio` udostępnia pętlę zdarzeń, planowanie zadań i asynchroniczne prymitywy
do współbieżności kooperatywnej w zadaniach I/O-bound.

**W skrócie:**

- Pozwala efektywnie obsługiwać wiele operacji I/O.
- Opiera się na `async` i `await`.
- Dobrze nadaje się do usług i klientów sieciowych.

</details>

<details>
<summary>242. Czym różni się programowanie synchroniczne od asynchronicznego w Pythonie?</summary>

#### Python

Programowanie synchroniczne oznacza, że wywołanie blokuje bieżący wątek do zakończenia.
Programowanie asynchroniczne oznacza, że `await` oddaje sterowanie pętli zdarzeń,
gdy operacja czeka na I/O.

**W skrócie:**

- Async zmniejsza czas bezczynności podczas I/O.
- Sync jest prostszy dla logiki liniowej.
- Async dodaje złożoność zarządzania zadaniami i anulowaniem.

</details>

<details>
<summary>243. Czym są `async` i `await`?</summary>

#### Python

`async def` definiuje funkcję typu coroutine. `await` wstrzymuje coroutine do
gotowości obiektu awaitable i oddaje sterowanie pętli.

**W skrócie:**

- To składnia asynchronicznego modelu kooperatywnego.
- Używa się jej razem z `asyncio` i bibliotekami asynchronicznymi.
- `await` można stosować tylko wewnątrz `async def`.

</details>

<details>
<summary>244. Jak działa `asyncio`?</summary>

#### Python

`asyncio` uruchamia pętlę zdarzeń, która wykonuje zadania, czyli coroutines,
przełączając się w punktach `await` i planując gotowe operacje I/O.

**Krytyczna zasada:** Pętla zdarzeń działa w jednym wątku. Każda blokująca
operacja, taka jak `time.sleep()`, synchroniczne żądania `requests` albo ciężkie obliczenia,
zatrzymuje **całą** pętlę i wszystkie inne zadania.

**W skrócie:**

- Jeden wątek może obsługiwać wiele zadań I/O dzięki kooperatywności.
- Planowanie nie wywłaszcza zadań, czyli jest niewywłaszczające.
- Blokujące wywołania niszczą wydajność `asyncio`.

</details>

<details>
<summary>245. Czym jest pętla zdarzeń?</summary>

#### Python

Pętla zdarzeń to planista, który śledzi zdarzenia oraz gotowość I/O i uruchamia
odpowiednie funkcje zwrotne oraz coroutines.

**W skrócie:**

- To centralny komponent modelu `asyncio`.
- Zarządza cyklem życia zadań asynchronicznych.
- Określa, kiedy dana coroutine ma wznowić wykonanie.

</details>

<details>
<summary>246. Jak `asyncio` pozwala realizować programowanie asynchroniczne i jakie główne komponenty biorą udział w kodzie `asyncio`?</summary>

#### Python

Kluczowe komponenty:

- pętla zdarzeń;
- coroutine, czyli `async def`;
- task, czyli `asyncio.create_task`;
- awaitables, czyli futures, tasks i coroutines;
- prymitywy synchronizacji, takie jak `Lock`, `Queue`, `Semaphore`.

**W skrócie:**

- `asyncio` łączy planowanie i asynchroniczne API w jeden model.
- Zadania kooperatywnie współdzielą jeden wątek wykonania.
- Architektura powinna uwzględniać timeouty, ponawianie i anulowanie.

</details>

<details>
<summary>247. Kiedy `asyncio` nie daje korzyści?</summary>

#### Python

Gdy obciążenie jest CPU-bound albo główne biblioteki są blokujące i nie mają API asynchronicznego.
Nie opłaca się też w prostych krótkich skryptach.

**Rozwiązanie dla blokującego kodu:** Jeśli trzeba użyć biblioteki blokującej
w środowisku asynchronicznym, można użyć `loop.run_in_executor(None, sync_func)`,
aby uruchomić ją w osobnym wątku i nie blokować pętli zdarzeń.

**W skrócie:**

- Async nie przyspiesza czystych obliczeń.
- Bez nieblokujących bibliotek I/O korzyść jest minimalna.
- `run_in_executor` pomaga integrować starszy kod synchroniczny.
- Złożoność podejścia asynchronicznego powinna być uzasadniona obciążeniem.

</details>

<details>
<summary>248. Jak działa anulowanie w `asyncio`?</summary>

#### Python

Anulowanie zadania przez `task.cancel()` podnosi `CancelledError` w coroutine. Kod
powinien poprawnie obsługiwać czyszczenie w `try/finally`.

**W skrócie:**

- Anulowanie jest zwykłym przepływem sterowania w async.
- Obsługę anulowania trzeba uwzględniać w projekcie coroutine.
- Ignorowanie anulowania prowadzi do "zawieszonych" zadań.

</details>

<details>
<summary>249. Czym jest `contextvars`?</summary>

#### Python

`contextvars` daje zmienne lokalne dla kontekstu, bezpieczne w scenariuszach
asynchronicznych i wielowątkowych. Przydaje się dla request-id, correlation-id
i kontekstu tenantów.

**W skrócie:**

- To alternatywa dla globalnego stanu w kodzie współbieżnym.
- Wartość jest izolowana w ramach kontekstu.
- Poprawia śledzenie i obserwowalność.

</details>

<details>
<summary>250. Jakie najlepsze praktyki warto stosować przy pisaniu kodu w Pythonie?</summary>

#### Python

- przestrzegać PEP 8 i automatyzować formatowanie;
- pisać jawne adnotacje typów dla publicznego API;
- używać `with` do pracy z zasobami;
- pokrywać logikę biznesową testami;
- unikać przedwczesnej optymalizacji i profilować;
- trzymać moduły niewielkie i o jasnej odpowiedzialności;
- zarządzać zależnościami przez `pyproject.toml` i strategię lock.

**W skrócie:**

- Czytelność i przewidywalność są ważniejsze niż "sztuczki".
- Jakość opiera się na automatyzacji: lint, typy, testy i CI.
- Prostota architektury zmniejsza koszt utrzymania.

</details>
