**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

# Python <img src="./assets/python.svg" width="40" height="40" alt="Python logo"/>

## Die beliebtesten Python-Interviewfragen und Antworten

<details>
<summary>1. Was ist Python und was sind seine wichtigsten Eigenschaften?</summary>

#### Python

**Python** ist eine High-Level-Allzwecksprache mit Fokus auf Lesbarkeit, schnelle Entwicklung und eine umfangreiche Standardbibliothek.

Wichtige Eigenschaften:

- **Einfache Syntax**: Code lässt sich leicht lesen und warten.
- **Interpretierte Ausführung**: schneller Änderungszyklus ohne manuellen Kompilierungsschritt.
- **Plattformunabhängigkeit**: derselbe Code läuft unter Linux, macOS und Windows.
- **Multiparadigma**: prozedurale, OOP- und funktionale Ansätze in einem Projekt.
- **Starkes Ökosystem**: `pip`, `venv`, `pyproject.toml`, tausende fertige Bibliotheken.
- **Moderne Python-3.10+-Features**: Type Hints, `dataclass`, `async/await`, `match/case`, Generatoren, Context Manager.

Beispiel für eine production-taugliche Funktion:

```python
from dataclasses import dataclass

@dataclass(slots=True)
class User:
    name: str
    active: bool

def process_users(users: list[User]) -> list[str]:
    return [user.name for user in users if user.active]
```

**Kurz:**

- Python beschleunigt die Entwicklung durch einfache Syntax und eine große Standardbibliothek.
- Die Sprache eignet sich für Backend, Automatisierung, Data/ML, Testing und DevOps.
- In Python 3.10+ sind Type Hints, Async IO und moderne Standardbibliotheks-Patterns zentral.

</details>

<details>
<summary>2. Was sind die wichtigsten Vorteile von Python?</summary>

#### Python

Wichtige Vorteile von Python im Produktiveinsatz:

- hohe Entwicklungsgeschwindigkeit durch knappe Syntax;
- große Standardbibliothek (`pathlib`, `itertools`, `collections`, `asyncio`);
- reifes Paket-Ökosystem für Backend, Data, Automatisierung und Testing;
- portable Codebasis zwischen Betriebssystemen;
- gute Unterstützung für Typisierung (`typing`, `mypy`, `pyright`) und moderne Praktiken.

**Kurz:**

- Python verkürzt die Time-to-Market.
- Es bietet viele sofort nutzbare Werkzeuge ohne zusätzliche Abhängigkeiten.
- Es eignet sich sowohl für MVPs als auch für skalierbare Services.

</details>

<details>
<summary>3. Wodurch unterscheidet sich Python von kompilierten Programmiersprachen?</summary>

#### Python

Python wird in der Regel von einem Interpreter ausgeführt: Der Code wird in Bytecode kompiliert und
zur Laufzeit ausgeführt (CPython VM). Bei kompilierten Sprachen wie C/C++ oder Rust
erfolgt meist eine vorgelagerte Kompilierung in Maschinencode.

Praktische Folgen:

- Python ist schneller in Entwicklung und Prototyping.
- Nativ kompilierte Sprachen sind bei CPU-bound-Aufgaben meist schneller.
- In Python verbessert man Performance oft über Algorithmen, Profiling und C-Erweiterungen.

**Kurz:**

- Python optimiert Entwicklungsgeschwindigkeit.
- Die Kompilierung in Maschinencode liefert meist bessere Roh-Performance.
- Die Wahl hängt von Domäne sowie Anforderungen an Latenz und Durchsatz ab.

</details>

<details>
<summary>4. Was bedeutet dynamische Typisierung in Python?</summary>

#### Python

Dynamische Typisierung bedeutet, dass der Typ an das Objekt und nicht an den
Variablennamen gebunden ist. Ein Name kann zur Laufzeit auf Werte unterschiedlicher Typen verweisen.

```python
value = 10        # int
value = "10"      # str
```

Typen werden während der Ausführung geprüft. Deshalb treten Typfehler zur Laufzeit auf,
wenn kein statischer Typprüfer verwendet wird.

**Kurz:**

- In Python gehört der Typ zum Objekt, nicht zur Variablen.
- Der Typ kann sich ändern, wenn derselbe Name neu gebunden wird.
- Type Hints ergänzen zusätzliche Kontrolle vor der Codeausführung.

</details>

<details>
<summary>5. Was bedeutet strenge Typisierung (strong typing) in Python?</summary>

#### Python

Strong Typing in Python bedeutet, dass der Interpreter keine unsicheren impliziten
Konvertierungen zwischen inkompatiblen Typen durchführt.

```python
1 + "2"  # TypeError
```

Für Operationen zwischen verschiedenen Typen ist eine explizite Umwandlung nötig:

```python
1 + int("2")  # 3
```

**Kurz:**

- Python ist dynamisch typisiert, aber streng bei Typkompatibilität.
- Unsichere implizite Konvertierungen werden mit einem Fehler blockiert.
- Explizite Umwandlung macht das Verhalten vorhersehbar.

</details>

<details>
<summary>6. Was ist eine REPL und wann verwendet man sie?</summary>

#### Python

REPL (Read-Eval-Print Loop) ist ein interaktiver Modus, in dem man Ausdrücke eingibt,
sofort Ergebnisse erhält und Hypothesen schnell prüfen kann.

Anwendungsfälle:

- ein Bibliotheks-API prüfen;
- schnell einen Ausdruck oder Algorithmus testen;
- Daten vor der Implementierung in einem Modul explorieren.

Werkzeuge: das Standard-`python`, `ipython`, `ptpython`.

**Kurz:**

- Eine REPL liefert den schnellsten Feedback-Zyklus.
- Sie ist praktisch für Experimente und Debugging.
- Sie ersetzt keine Tests, verkürzt aber die Validierung von Ideen.

</details>

<details>
<summary>7. Was sind Literale in Python? Nennen Sie Beispiele für verschiedene Literaltypen.</summary>

#### Python

Ein Literal ist ein fester Wert, der direkt im Code geschrieben wird.

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

**Kurz:**

- Literale sind eingebaute konstante Werte im Code.
- Jeder Basistyp hat seine eigene Literal-Syntax.
- Sie werden häufig zur Initialisierung von Daten verwendet.

</details>

<details>
<summary>8. Was sind Keywords in Python?</summary>

#### Python

Keywords sind reservierte Wörter der Sprache mit spezieller syntaktischer
Bedeutung und können nicht als Variablennamen verwendet werden.

Beispiele: `if`, `for`, `class`, `def`, `match`, `case`, `try`, `except`,
`async`, `await`.

Liste anzeigen:

```python
import keyword
print(keyword.kwlist)
```

**Kurz:**

- Keywords bilden die Syntax von Python.
- Sie können nicht als Bezeichner verwendet werden.
- Die Liste ist über das Modul `keyword` verfügbar.

</details>

<details>
<summary>9. Was ist eine Variable in Python?</summary>

#### Python

Eine Variable in Python ist ein Name (eine Referenz), der auf ein Objekt im Speicher zeigt.
Eine Zuweisung bindet den Namen an ein Objekt und „legt keinen Wert in eine Box“.

```python
x = [1, 2]
y = x
y.append(3)
# x und y verweisen auf dieselbe Liste
```

**Kurz:**

- Eine Variable ist eine Referenz auf ein Objekt.
- Mehrere Namen können auf dasselbe mutable Objekt verweisen.
- Das ist wichtig für das Verständnis von Kopien und Seiteneffekten.

</details>

<details>
<summary>10. Was sind `pass` und `...` (Ellipsis) in Python?</summary>

#### Python

`pass` ist eine Platzhalter-Anweisung: Sie macht nichts, erlaubt aber einen
syntaktisch gültigen leeren Block.

`...` (Ellipsis) ist das eigenständige Objekt `Ellipsis`. Es wird oft als
Marker für „noch nicht implementiert“, in Type Hints und in Bibliotheken wie NumPy verwendet.

```python
def feature() -> None:
    pass

PLACEHOLDER = ...
```

**Kurz:**

- `pass` wird für leere Codeblöcke benötigt.
- `...` ist ein Wertobjekt und kein Schlüsselwort.
- Beide werden als temporäre Platzhalter verwendet, aber mit unterschiedlicher Semantik.

</details>

<details>
<summary>11. Was ist ein PEP und wie beeinflusst es die Entwicklung von Python?</summary>

#### Python

Ein PEP (Python Enhancement Proposal) ist ein offizielles Dokument, das ein neues
Feature, einen Standard oder einen Prozess im Python-Ökosystem beschreibt.

Durch ein PEP laufen:

- Design-Diskussionen;
- technische Begründung;
- Entscheidung über Annahme oder Ablehnung;
- Standardisierung von Praktiken.

Beispiele: PEP 8 (Style), PEP 484 (Type Hints), PEP 634 (Pattern Matching).

**Kurz:**

- PEPs sind der Mechanismus für die Weiterentwicklung von Sprache und Werkzeugen.
- Sie machen Änderungen transparent und formalisiert.
- Viele moderne Python-Praktiken wurden genau über PEPs standardisiert.

</details>

<details>
<summary>12. Was ist PEP 8 und wozu wird es benötigt?</summary>

#### Python

PEP 8 ist der offizielle Style Guide für Python-Code: Benennung, Formatierung,
Einrückung, Imports, Zeilenlänge und Lesbarkeit von Konstrukten.

Wozu es dient:

- ein einheitlicher Stil im Team;
- schnellere Code Reviews;
- weniger Rauschen im Diff;
- bessere Wartbarkeit.

In der Praxis automatisiert man den Stil mit `ruff format` oder `black` + `ruff`.

**Kurz:**

- PEP 8 standardisiert den Stil von Python-Code.
- Es geht um Lesbarkeit und Wartbarkeit, nicht um Performance.
- Die Einhaltung sollte besser mit Tools automatisiert werden.

</details>

<details>
<summary>13. Welche neuen Möglichkeiten sind in modernen Python-Versionen (3.10+) hinzugekommen?</summary>

#### Python

Wichtige Features moderner Python-Versionen:

- `match/case` (Structural Pattern Matching);
- verbesserte Syntax und Fehlermeldungen;
- Union-Typen über `|` (`int | None`);
- `typing.Self`, `typing.TypeAlias`, `typing.override`;
- Generics im Stil von PEP 695 (`class Box[T]: ...`, `def f[T](...) -> ...`);
- `tomllib` in der Standardbibliothek.

Praktisch reduziert das Boilerplate und verbessert die Zuverlässigkeit von typisiertem Code.

**Kurz:**

- Python 3.10+ hat Syntax und Typisierung deutlich verbessert.
- `match/case` und modernes `typing` wirken sich am sichtbarsten auf den Code aus.
- Neue Features sollte man in neuem Code standardmäßig nutzen.

</details>

<details>
<summary>14. Was ist ein Docstring in Python?</summary>

#### Python

Ein Docstring ist ein Dokumentationsstring, also der erste Ausdruck in einem Modul, einer Klasse oder Funktion.
Er ist über `__doc__` verfügbar und wird von IDEs, `help()` und Doku-Generatoren verwendet.

```python
def normalize_email(email: str) -> str:
    """Return lowercase email without surrounding spaces."""
    return email.strip().lower()
```

Empfohlen ist die Beschreibung von Funktion, Argumenten, Rückgabewert und Ausnahmen.

**Kurz:**

- Ein Docstring ist eingebaute Dokumentation im Code.
- Er dient als Quelle für `help()` und automatische Dokumentation.
- Ein guter Docstring reduziert die Notwendigkeit, die Implementierung zu lesen.

</details>

<details>
<summary>15. Wie funktionieren Einrückungen (Indentation) in Python?</summary>

#### Python

In Python definieren Einrückungen Codeblöcke (den Körper von `if`, `for`, `def`, `class`).
Einrückung ist also Teil der Syntax und nicht nur Stil.

```python
if is_ready:
    run_task()
else:
    stop_task()
```

Das Mischen von Tabs und Spaces kann zu `IndentationError` oder einer falschen
Blockstruktur führen.

**Kurz:**

- Einrückung definiert in Python die Programmstruktur.
- Falsche Einrückung bricht die Ausführung.
- Verwenden Sie einen konsistenten Stil mit 4 Leerzeichen.

</details>

<details>
<summary>16. Wie viele Leerzeichen empfiehlt PEP 8 für Einrückungen und warum ist ein einheitlicher Stil wichtig?</summary>

#### Python

PEP 8 empfiehlt **4 Leerzeichen** pro Einrückungsebene.

Warum das wichtig ist:

- einheitliche Blockstruktur im gesamten Projekt;
- vorhersehbare Darstellung in verschiedenen Editoren;
- weniger Fehler durch Tab-/Space-Konflikte;
- sauberere Diffs in Git.

**Kurz:**

- Standard-Einrückung: 4 Leerzeichen.
- Ein einheitlicher Stil eliminiert eine ganze Klasse von Formatierungsfehlern.
- Das verbessert direkt die Lesbarkeit und Wartbarkeit des Codes.

</details>

<details>
<summary>17. Worin unterscheiden sich `ruff` und `black` hinsichtlich Funktionalität und Einsatz?</summary>

#### Python

`black` ist ein Code-Formatter mit festen Regeln.

`ruff` ist ein schneller Linter sowie Formatter und Auto-Fixer für viele Regeln
(PEP 8, Imports, potenzielle Bugs, Syntaxvereinfachungen).

Praktische Setups:

- entweder `ruff check --fix` + `ruff format`;
- oder `ruff` für Linting und `black` für Formatierung.

**Kurz:**

- `black` fokussiert sich auf Formatierung.
- `ruff` deckt Linting und einen Teil der automatischen Korrekturen ab.
- In modernen Projekten reicht oft ein einziges `ruff`.

</details>

<details>
<summary>18. Erklären Sie den Zweck von Type Annotations in Python und geben Sie ein Beispiel für eine Funktion mit Type Annotations.</summary>

#### Python

Type Annotations beschreiben die erwarteten Typen von Argumenten und Rückgabewerten.
Sie verbessern Autovervollständigung, statische Analyse und die Lesbarkeit eines API.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Annotationen führen selbst keine Runtime-Validierung aus, helfen aber,
Fehler in CI über `mypy` oder `pyright` zu finden.

**Kurz:**

- Type Hints dokumentieren den Vertrag einer Funktion.
- Sie ermöglichen frühe Fehlererkennung durch statische Prüfung.
- Sie erhöhen die API-Qualität in großen Codebasen.

</details>

<details>
<summary>19. Was ist Debugging und warum ist es eine wichtige Fähigkeit für Entwickler?</summary>

#### Python

Debugging ist die systematische Suche nach der Ursache für fehlerhaftes Verhalten im Code
und deren Behebung. Es bedeutet nicht nur, „einen Bug zu finden“, sondern ihn zu reproduzieren, zu lokalisieren und den Fix zu verifizieren.

Typischer Ablauf:

- das Problem reproduzieren;
- den betroffenen Codebereich eingrenzen;
- eine Hypothese mit Logs oder Debugger prüfen;
- einen Test hinzufügen, der das Szenario absichert.

**Kurz:**

- Debugging reduziert MTTR und die Zahl von Regressionen.
- Es funktioniert am besten als Prozess und nicht als chaotische Suche.
- Ein Debugging-Vorgang ist erst mit Fix, Test und Nachkontrolle abgeschlossen.

</details>

<details>
<summary>20. Erklären Sie den Zweck von `print` beim Debugging. Geben Sie ein Beispiel für eine Situation, in der dieser Ansatz nützlich ist.</summary>

#### Python

`print`-Debugging ist ein schneller Weg, Variablenwerte und die Ausführungsreihenfolge
zu prüfen, ohne komplexe Werkzeuge zu starten.

Das ist nützlich, wenn man in einem lokalen Skript schnell eine Hypothese prüfen muss:

```python
def parse_port(raw: str) -> int:
    value = raw.strip()
    print(f"raw={raw!r} value={value!r}")
    return int(value)
```

Für Produktivcode sollte man zu `logging` wechseln, um Log-Level und
kontrollierte Ausgabe zu haben.

**Kurz:**

- `print` eignet sich für kurze lokale Diagnosen.
- Es zeigt schnell den Zustand von Variablen an einer problematischen Stelle.
- Für stabile Diagnose in Services sollte `logging` verwendet werden.

</details>

<details>
<summary>21. Beschreiben Sie, wie man den Python Debugger (PDB) zum Debugging verwenden kann. Welche Vorteile hat PDB gegenüber `print`?</summary>

#### Python

`pdb` ermöglicht es, die Programmausführung anzuhalten, zeilenweise zu gehen,
den Zustand von Variablen und den Call Stack zu betrachten.

Grundlegende Verwendung:

```python
import pdb

def compute(x: int) -> int:
    pdb.set_trace()
    return x * 2
```

Wichtige Befehle: `n` (next), `s` (step), `c` (continue), `p expr` (print expr),
`l` (list), `bt` (backtrace).

**Kurz:**

- `pdb` bietet interaktive Kontrolle über die Ausführung.
- Für komplexe Szenarien ist es effektiver als `print`.
- Es erlaubt die Zustandsdiagnose, ohne den Code mit Logs zu verschmutzen.

</details>

<details>
<summary>22. Welche Strategien kann man zum Debugging von Schleifen und Funktionen in Python anwenden?</summary>

#### Python

Praktische Strategien:

- den Bug mit einem minimal reproduzierbaren Beispiel eingrenzen;
- Invarianten in Schleifeniterationen loggen;
- Breakpoints am Ein- und Austritt einer Funktion setzen;
- Randfälle prüfen (leere Daten, `None`, große Datenmengen);
- den problematischen Pfad mit einem Test absichern.

Bei Schleifen ist es nützlich, Index und wichtige Zwischenzustände zu loggen.

**Kurz:**

- Beginnen Sie mit Reproduktion und Eingrenzung des Problems.
- Prüfen Sie Invarianten und Randbedingungen.
- Schließen Sie den Fix mit einem Test ab, der Regressionen erkennt.

</details>

<details>
<summary>23. Welchen Einfluss haben lang laufende Funktionen auf die Programmleistung?</summary>

#### Python

Lang laufende Funktionen erhöhen die Latenz, blockieren Worker oder Threads und verschlechtern
den Durchsatz eines Services.

Risiken:

- langsame API-Antworten;
- Timeouts;
- wachsende Task-Queues;
- schlechtere Nutzung von CPU/IO.

Ansatz: Profiling mit `cProfile`, Zerlegung in kleinere Schritte, Nutzung von
Generatoren oder Streaming, Auslagerung schwerer Berechnungen in `multiprocessing` oder Hintergrundjobs.

**Kurz:**

- Lange Funktionen schlagen direkt auf die Latenz durch.
- Optimierung basiert auf Profiling, nicht auf Intuition.
- Architektonisch sollte man CPU-bound- und IO-bound-Arbeit trennen.

</details>

<details>
<summary>24. Was ist Logging und warum sollte man es statt `print` verwenden?</summary>

#### Python

`logging` ist der Standardmechanismus zur Protokollierung von Ereignissen mit Levels (`DEBUG`,
`INFO`, `WARNING`, `ERROR`, `CRITICAL`), Formaten und Handlern (Konsole, Datei).

Warum besser als `print`:

- steuerbare Detailstufen;
- strukturiertes Format;
- zentrale Konfiguration;
- Möglichkeit zur Integration in einen Observability-Stack.

**Kurz:**

- `logging` ist für Produktion geeignet, `print` nicht.
- Log-Levels geben Kontrolle über das Rauschen.
- Logs sollten strukturiert und konsistent sein.

</details>

<details>
<summary>25. Was ist ein Traceback?</summary>

#### Python

Ein Traceback ist der Call Stack, den Python bei einer Ausnahme anzeigt: wo die
Ausführung begann, durch welche Funktionen der Code gelaufen ist und wo genau der Fehler auftrat.

Verwendung:

- die Datei und Zeile der Fehlerquelle schnell finden;
- den Ausführungspfad bis zum Fehler verstehen;
- einen präzisen Reproduktionstest bauen.

**Kurz:**

- Ein Traceback ist die „Route“ zum Fehler.
- Am wertvollsten sind die letzten Stack-Frames und der Ausnahmetyp.
- Die Analyse eines Tracebacks beschleunigt die Root-Cause-Suche.

</details>

<details>
<summary>26. Welche grundlegenden Datentypen gibt es in Python?</summary>

#### Python

Wichtige Built-in-Typen:

- numerische Typen: `int`, `float`, `complex`;
- boolesch: `bool`;
- Strings/Bytes: `str`, `bytes`, `bytearray`;
- Collections: `list`, `tuple`, `set`, `dict`, `frozenset`;
- spezielle Typen: `NoneType` (`None`).

Wichtig ist auch die Mutability:

- mutable: `list`, `dict`, `set`, `bytearray`;
- immutable: `int`, `str`, `tuple`, `frozenset`.

**Kurz:**

- Python hat von Haus aus einen reichen Satz grundlegender Typen.
- Die Wahl der Datenstruktur beeinflusst die Komplexität von Operationen.
- Mutability bestimmt das Verhalten von Kopien und Seiteneffekten.

</details>

<details>
<summary>27. Was ist der Unterschied zwischen normaler Division (`/`) und ganzzahliger Division (`//`) in Python?</summary>

#### Python

`/` führt normale Division aus und liefert immer einen `float`.

`//` führt Floor-Division aus: Es rundet nach unten (gegen `-∞`), der Typ ist bei ganzzahligen Operanden meist
`int`.

```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

**Kurz:**

- `/` -> Ergebnis als Fließkommazahl.
- `//` -> Abrundung nach unten auf einen ganzzahligen Wert.
- Für negative Zahlen ist `//` nicht dasselbe wie „Abschneiden gegen null“.

</details>

<details>
<summary>28. Erklären Sie die Verwendung des Modulo-Operators (`%`) in Python. Wie kann man damit prüfen, ob eine Zahl gerade oder ungerade ist?</summary>

#### Python

Der Operator `%` liefert den Rest einer Division.

Prüfung auf Gerade/Ungerade:

```python
def is_even(n: int) -> bool:
    return n % 2 == 0
```

Wenn `n % 2 == 0`, ist die Zahl gerade, sonst ungerade.

Typische Anwendungsfälle: zyklische Indizes, Gruppierung, Kalenderberechnungen.

**Kurz:**

- `%` liefert den Restwert.
- `n % 2` ist die Standardprüfung auf Gerade/Ungerade.
- Der Operator wird häufig für zyklische Logik verwendet.

</details>

<details>
<summary>29. Wie arbeitet Python mit großen Ganzzahlen und welche Grenzen gibt es bei sehr großen Zahlen?</summary>

#### Python

`int` in Python hat beliebige Genauigkeit (arbitrary precision), ist also nicht
auf 32 oder 64 Bit begrenzt wie in vielen anderen Sprachen.

Die Grenzen sind praktisch:

- Prozessspeicher;
- Rechenzeit bei sehr großen Werten;
- die Kosten von Operationen steigen mit der Zahl der Stellen.

**Kurz:**

- Ein `int` überläuft im üblichen Sinn nicht.
- Die Grenze sind Maschinenressourcen, nicht eine feste Bitbreite.
- Für große Berechnungen sind Algorithmen und Profiling entscheidend.

</details>

<details>
<summary>30. Welche Bedeutung hat die Behandlung von Division durch null in Python und wie verhindert man `ZeroDivisionError` im Code?</summary>

#### Python

Division durch null löst `ZeroDivisionError` aus. Das sollte explizit behandelt werden, wenn
der Divisor aus externer Eingabe kommt oder dynamisch berechnet wird.

```python
def safe_div(a: float, b: float) -> float | None:
    if b == 0:
        return None
    return a / b
```

In kritischen Szenarien sollten `try/except` und Kontext-Logging verwendet werden.

**Kurz:**

- Division durch null ist ein kontrollierbarer Laufzeitfehler.
- Die einfachste Prävention ist eine Prüfung des Divisors vor der Operation.
- Bei externen Daten sollten Schutzmechanismen und Diagnose ergänzt werden.

</details>

<details>
<summary>31. Beschreiben Sie die Verwendung des Moduls `random` in Python. Welche Funktionen daraus werden am häufigsten verwendet?</summary>

#### Python

`random` wird für pseudozufällige Werte in Simulationen, Testdaten und
nicht-kryptografischen Aufgaben verwendet.

Häufig verwendete Funktionen:

- `random()` — Zahl in `[0.0, 1.0)`;
- `randint(a, b)` — Ganzzahl in einem Bereich;
- `randrange(start, stop, step)` — wie `range`, aber mit zufälligem Element;
- `choice(seq)` / `choices(seq, k=...)`;
- `shuffle(list_)` — mischt eine Liste in-place;
- `sample(population, k)` — eindeutige Stichprobe.

Für Kryptografie sollte `secrets` statt `random` verwendet werden.

**Kurz:**

- `random` eignet sich für gewöhnliche anwendungsbezogene Zufälligkeit.
- Am häufigsten genutzt werden `randint`, `choice`, `shuffle` und `sample`.
- Für sicherheitskritische Aufgaben braucht man `secrets`.

</details>

<details>
<summary>32. Wie arbeitet man in Python mit Zahlen mit höherer Genauigkeit?</summary>

#### Python

Für finanzielle und exakt dezimale Berechnungen sollte `decimal.Decimal`
anstelle von `float` verwendet werden.

```python
from decimal import Decimal

total = Decimal("0.1") + Decimal("0.2")  # Decimal('0.3')
```

Für rationale Zahlen ist `fractions.Fraction` nützlich.

**Kurz:**

- `float` ist praktisch, hat aber Fehler durch binäre Darstellung.
- Für exakte Dezimalarithmetik sollte `Decimal` verwendet werden.
- Der Zahlentyp muss zur Domäne der Aufgabe passen.

</details>

<details>
<summary>33. Was sind Escape-Zeichen in Python-Strings und wie werden sie verwendet? Geben Sie Beispiele für `\n`, `\t`, `\r`, `\"` und `\'`.</summary>

#### Python

Escape-Sequenzen sind spezielle Kombinationen mit `\`, die Steuerzeichen
innerhalb eines Strings kodieren.

- `\n` — Zeilenumbruch
- `\t` — Tabulator
- `\r` — Wagenrücklauf
- `\"` — doppeltes Anführungszeichen in einem String mit `"`
- `\'` — einfaches Anführungszeichen in einem String mit `'`

```python
text = "A\tB\n\"quoted\"\nI\'m here\rX"
```

**Kurz:**

- Escape-Zeichen steuern die Formatierung eines Strings.
- Sie erlauben das Einfügen von Anführungszeichen, ohne die Syntax zu brechen.
- Für Pfade oder Regex sind Raw-Strings `r"..."` oft bequemer.

</details>

<details>
<summary>34. Erklären Sie die Verwendung der Methoden `strip`, `lstrip` und `rstrip` in Python. Worin unterscheiden sie sich?</summary>

#### Python

Die Methoden arbeiten mit den Rändern eines Strings:

- `strip()` — entfernt Zeichen auf beiden Seiten;
- `lstrip()` — nur links;
- `rstrip()` — nur rechts.

Standardmäßig entfernen sie Whitespace oder einen konkreten Zeichensatz:

```python
"  hello  ".strip()      # "hello"
"--id--".strip("-")      # "id"
```

**Kurz:**

- Die `strip`-Familie verändert den String nicht in-place, sondern liefert einen neuen zurück.
- Der Unterschied liegt nur auf der Seite, von der bereinigt wird.
- Sie wird häufig auf Eingabedaten angewendet.

</details>

<details>
<summary>35. Beschreiben Sie den Zweck der Methode `count` bei Strings. Wie funktioniert sie?</summary>

#### Python

`str.count(sub[, start[, end]])` zählt die Anzahl nicht überlappender Vorkommen
des Teilstrings `sub` in einem gewählten Bereich.

```python
"banana".count("an")      # 2
"banana".count("a", 2)    # 2
```

Sie gibt `0` zurück, wenn keine Vorkommen vorhanden sind.

**Kurz:**

- `count` liefert schnell die Anzahl von Teilstring-Vorkommen.
- Die Suche kann über `start/end` eingeschränkt werden.
- Gezählt werden nicht überlappende Vorkommen.

</details>

<details>
<summary>36. Wie funktioniert die Methode `join` in Python und wofür wird sie am häufigsten verwendet?</summary>

#### Python

`sep.join(iterable)` verbindet eine Folge von Strings zu einem einzigen String mit dem Trennzeichen
`sep`.

```python
names = ["Ada", "Linus", "Guido"]
result = ", ".join(names)  # "Ada, Linus, Guido"
```

Typische Anwendung: Erzeugen von CSV-ähnlichen Zeilen, Logs, SQL-Fragmenten,
URL-Pfaden oder Nachrichten.

**Kurz:**

- `join` ist der standardmäßige und schnelle Weg, Strings zusammenzufügen.
- Es wird auf dem Trennzeichen aufgerufen, nicht auf der Liste.
- Es ist effizienter als wiederholtes `+=` in einer Schleife.

</details>

<details>
<summary>37. Was ist Slicing in Python und wie erhält man damit Teilstrings? Geben Sie Beispiele mit positiven und negativen Indizes.</summary>

#### Python

Slicing ist die Auswahl eines Teils einer Sequenz über `[start:stop:step]`.

```python
s = "python"
s[1:4]     # "yth"
s[:2]      # "py"
s[-3:]     # "hon"
s[::-1]    # "nohtyp"
```

`start` ist inklusive, `stop` exklusive.

**Kurz:**

- Slicing funktioniert für Strings, Listen und Tupel.
- Negative Indizes werden vom Ende aus gezählt.
- Es ist ein grundlegendes Werkzeug zur Verarbeitung von Sequenzen ohne Schleifen.

</details>

<details>
<summary>38. Erklären Sie die Methode `replace` für Strings. Wie kann man damit mehrere Vorkommen eines Teilstrings ersetzen?</summary>

#### Python

`str.replace(old, new, count=-1)` gibt einen neuen String zurück, in dem `old` durch
`new` ersetzt wird. Standardmäßig werden alle Vorkommen ersetzt.

```python
"foo bar foo".replace("foo", "baz")      # "baz bar baz"
"foo bar foo".replace("foo", "baz", 1)   # "baz bar foo"
```

**Kurz:**

- `replace` verändert den String nicht in-place.
- Ohne `count` werden alle Vorkommen ersetzt.
- `count` erlaubt die Kontrolle über die Anzahl der Ersetzungen.

</details>

<details>
<summary>39. Wie funktioniert die Methode `split` bei Strings?</summary>

#### Python

`split(sep=None, maxsplit=-1)` teilt einen String in eine Liste von Teilstrings.

- ohne `sep` wird an beliebigen Leerraumzeichen getrennt;
- mit `sep` an einem konkreten Trennzeichen;
- `maxsplit` begrenzt die Anzahl der Trennungen.

```python
"a,b,c".split(",")         # ["a", "b", "c"]
"a b   c".split()          # ["a", "b", "c"]
"k=v=x".split("=", 1)      # ["k", "v=x"]
```

**Kurz:**

- `split` wandelt einen String in eine Liste von Token um.
- `sep=None` hat ein spezielles Verhalten für Whitespace.
- `maxsplit` ist nützlich beim Parsen von Key/Value-Formaten.

</details>

<details>
<summary>40. Wie funktioniert Type Casting?</summary>

#### Python

Type Casting ist die explizite Umwandlung eines Werts zwischen Typen über Konstruktoren:
`int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`, `set()`, `dict()`.

```python
age = int("42")
price = float("19.99")
text = str(10)
```

Ungültige Daten verursachen Ausnahmen (`ValueError`, `TypeError`), daher ist für
externe Eingaben Validierung nötig.

**Kurz:**

- Python bietet explizite Funktionen zur Typkonvertierung.
- Nicht alle Werte lassen sich sicher konvertieren.
- Für Benutzereingaben sind Prüfungen und Exception-Handling notwendig.

</details>

<details>
<summary>41. Wie konvertiert Python automatisch verschiedene Datentypen in boolesche Werte?</summary>

#### Python

Im booleschen Kontext wendet Python Truthiness-Regeln an.

`False`-ähnliche Werte:

- `False`, `None`;
- numerische Nullwerte: `0`, `0.0`, `0j`;
- leere Collections: `""`, `[]`, `{}`, `set()`, `tuple()`, `range(0)`.

Alles andere ist normalerweise `True`.

```python
bool([])      # False
bool("0")     # True
```

**Kurz:**

- Die Bool-Konvertierung basiert auf Truthy/Falsy-Regeln.
- Leere und nullartige Werte ergeben `False`.
- Der nichtleere String `"0"` ist trotzdem `True`.

</details>

<details>
<summary>42. Erklären Sie, wie man in Python einen String in eine Ganzzahl oder Fließkommazahl umwandelt. Was passiert, wenn der String nicht konvertiert werden kann?</summary>

#### Python

Zur Umwandlung verwendet man `int()` und `float()`:

```python
count = int("42")
ratio = float("3.14")
```

Wenn der String ungültig ist, löst Python `ValueError` aus.

```python
def parse_int(value: str) -> int | None:
    try:
        return int(value)
    except ValueError:
        return None
```

**Kurz:**

- `int()` und `float()` führen eine explizite Konvertierung aus Strings aus.
- Ungültiges Format führt zu `ValueError`.
- Für externe Daten ist `try/except` nötig.

</details>

<details>
<summary>43. Was macht Python beim Vergleich verschiedener Datentypen wie Ganzzahlen und Fließkommazahlen oder Ganzzahlen und Boolean-Werten?</summary>

#### Python

Python erlaubt numerische Vergleiche kompatibler numerischer Typen.

- `int` und `float` werden nach ihrem Wert verglichen.
- `bool` ist eine Unterklasse von `int`: `False == 0`, `True == 1`.

```python
1 == 1.0      # True
True == 1     # True
False < 1     # True
```

Bei inkompatiblen Typen wie `int` und `str` löst ein Ordnungsvergleich (`<`, `>`)
`TypeError` aus.

**Kurz:**

- `int`, `float` und `bool` teilen eine gemeinsame numerische Semantik.
- `bool` verhält sich in Vergleichen wie `0/1`.
- Inkompatible Typen lassen sich nicht mit Ordnungsoperatoren vergleichen.

</details>

<details>
<summary>44. Wie verarbeitet Python Vergleiche zwischen Listen und Sets?</summary>

#### Python

`list` und `set` sind unterschiedliche Typen mit unterschiedlicher Semantik, daher wird
ein direkter Ordnungsvergleich zwischen ihnen nicht unterstützt.

```python
[1, 2] == {1, 2}   # False
[1, 2] < {1, 2}    # TypeError
```

Wenn man die enthaltenen Elemente vergleichen will, sollte man den Typ vereinheitlichen:

```python
set([1, 2]) == {1, 2}  # True
```

**Kurz:**

- `list` und `set` werden als unterschiedliche Datenstrukturen verglichen.
- `==` zwischen ihnen ist meist `False`.
- Für einen sinnvollen Vergleich sollte man sie zuerst in denselben Typ überführen.

</details>

<details>
<summary>45. Beschreiben Sie die Verwendung der Funktion `bool()` in Python.</summary>

#### Python

`bool(x)` gibt den booleschen Wert von `x` nach den Truthiness-Regeln zurück.

Typische Anwendungsfälle:

- explizite Umwandlung eines Werts in `True/False`;
- besser lesbare Bedingungen;
- Aufbau von Filtern.

```python
bool("text")   # True
bool("")       # False
bool(0)        # False
```

**Kurz:**

- `bool()` vereinheitlicht die Prüfung auf „leer/nicht leer“.
- Es basiert auf eingebauten Truthy/Falsy-Regeln.
- Es ist nützlich für Validierung und bedingte Logik.

</details>

<details>
<summary>46. Was ist der Unterschied zwischen `list` und `tuple`?</summary>

#### Python

Der Hauptunterschied: `list` ist mutable, `tuple` ist immutable.

Praktische Folgen:

- `list` eignet sich für veränderliche Daten;
- `tuple` eignet sich für feste Datensätze;
- `tuple` kann als Dictionary-Key verwendet werden, wenn seine Elemente hashbar sind.

```python
coords: tuple[float, float] = (50.45, 30.52)
queue: list[str] = ["task-1", "task-2"]
```

**Kurz:**

- `list` ist für veränderliche Collections gedacht.
- `tuple` für unveränderliche Datenstrukturen.
- Die Wahl beeinflusst API-Sicherheit und die Nutzung in `dict/set`.

</details>

<details>
<summary>47. Wie kann man ein `tuple` erstellen?</summary>

#### Python

Hauptvarianten:

```python
t1 = (1, 2, 3)
t2 = 1, 2, 3
t3 = tuple([1, 2, 3])
single = (42,)     # das Komma ist wichtig
empty = ()
```

Bei einem einzelnen Element ist das Komma Pflicht, sonst ist es nur ein Ausdruck in Klammern.

**Kurz:**

- Ein `tuple` wird über ein Literal oder `tuple(iterable)` erzeugt.
- `single = (x,)` ist ein korrektes Ein-Element-Tuple.
- Ein leeres Tuple ist `()`.

</details>

<details>
<summary>48. Was ist der Unterschied zwischen der Methode `reverse` und dem Slicing `[::-1]` beim Umdrehen einer Liste?</summary>

#### Python

`list.reverse()` verändert die bestehende Liste in-place und gibt `None` zurück.

`lst[::-1]` erstellt eine neue umgekehrte Liste, also eine Kopie.

```python
values = [1, 2, 3]
values.reverse()      # values -> [3, 2, 1]

other = values[::-1]  # neue Liste
```

**Kurz:**

- `reverse()` verändert das Original.
- `[::-1]` gibt ein neues Objekt zurück.
- Die Wahl hängt davon ab, ob die Ausgangsdaten erhalten bleiben sollen.

</details>

<details>
<summary>49. Erklären Sie Zweck und Verwendung der Methode `sort` für Listen. Wie sortiert man eine Liste in absteigender Reihenfolge?</summary>

#### Python

`list.sort()` sortiert eine Liste in-place. Es unterstützt folgende Parameter:

- `key` — Funktion für den Sortierschlüssel;
- `reverse=True` — absteigende Reihenfolge.

```python
nums = [5, 1, 7]
nums.sort(reverse=True)  # [7, 5, 1]
```

Wenn eine neue sortierte Kopie benötigt wird, sollte `sorted(iterable)` verwendet werden.

**Kurz:**

- `sort()` verändert die Liste direkt.
- Für absteigende Sortierung verwendet man `reverse=True`.
- `sorted()` ist praktisch, wenn das Original erhalten bleiben soll.

</details>

<details>
<summary>50. Was ist der Unterschied zwischen der Methode `copy` und der direkten Zuweisung einer Liste an eine andere? Warum ist `copy` manchmal wichtig?</summary>

#### Python

Eine Zuweisung kopiert nur die Referenz:

```python
a = [1, 2]
b = a
b.append(3)   # a wird ebenfalls verändert
```

`a.copy()` erstellt eine neue flache Liste:

```python
a = [1, 2]
b = a.copy()
b.append(3)   # a bleibt unverändert
```

Für verschachtelte Strukturen kann `copy.deepcopy` nötig sein.

**Kurz:**

- `=` kopiert die Daten nicht, sondern teilt ein Objekt zwischen Variablen.
- `copy()` isoliert Änderungen auf Ebene der obersten Liste.
- Für verschachtelte Objekte sollte `deepcopy` verwendet werden.

</details>

<details>
<summary>51. Was macht die Methode `pop` bei einer Liste? Worin unterscheidet sich ihr Verhalten mit und ohne Index?</summary>

#### Python

`pop()` entfernt ein Element aus einer Liste und gibt es zurück.

- `pop()` ohne Argument entfernt das letzte Element;
- `pop(i)` entfernt das Element am Index `i`.

```python
items = ["a", "b", "c"]
last = items.pop()     # "c"
first = items.pop(0)   # "a"
```

Ein ungültiger Index führt zu `IndexError`.

**Kurz:**

- `pop` kombiniert Entfernen und Rückgabe eines Werts.
- Ohne Index arbeitet es am Ende der Liste.
- Mit Index entfernt es eine konkrete Position.

</details>

<details>
<summary>52. Wie kombiniert man zwei Listen in Python mit dem Operator `+` und der Methode `extend`? Was ist der zentrale Unterschied zwischen beiden Varianten?</summary>

#### Python

`a + b` erstellt eine **neue** Liste, während `a.extend(b)` die Liste `a` **in-place** verändert.

```python
a = [1, 2]
b = [3, 4]

c = a + b         # [1, 2, 3, 4], a bleibt unverändert
a.extend(b)       # a -> [1, 2, 3, 4]
```

**Kurz:**

- `+` gibt ein neues Objekt zurück.
- `extend()` mutiert die bestehende Liste.
- Die Wahl hängt davon ab, ob das Original erhalten bleiben soll.

</details>

<details>
<summary>53. Wofür werden die Funktionen `min`, `max`, `sum`, `all` und `any` im Kontext von Listen verwendet?</summary>

#### Python

Das sind grundlegende Aggregatoren für iterierbare Collections:

- `min()` / `max()` — Minimum und Maximum;
- `sum()` — Summe numerischer Werte;
- `all()` — `True`, wenn alle Elemente truthy sind;
- `any()` — `True`, wenn mindestens ein Element truthy ist.

```python
nums = [3, 10, 1]
min(nums), max(nums), sum(nums)  # (1, 10, 14)
all([True, 1, "x"])              # True
any([0, "", None, 5])            # True
```

**Kurz:**

- Die Funktionen reduzieren Boilerplate in Schleifen.
- Sie arbeiten mit jedem Iterable.
- Sie kombinieren sich gut mit Generatoren für lazy Verarbeitung.

</details>

<details>
<summary>54. Was ist ein Wörterbuch (`dict`) in Python und worin unterscheidet es sich von anderen Datenstrukturen?</summary>

#### Python

`dict` ist ein assoziatives Array: Es speichert Paare `Schlüssel -> Wert`.
Schlüssel müssen hashbar sein, Werte können jeden Typ haben.

Unterschiede:

- Zugriff per Schlüssel statt per Index;
- durchschnittliche Komplexität für Suche/Einfügen/Löschen liegt nahe bei `O(1)`;
- ab Python 3.7+ bleibt die Einfügereihenfolge der Schlüssel erhalten.

**Kurz:**

- `dict` ist optimal für schnellen Zugriff per Schlüssel.
- Es ist die zentrale Struktur für Konfigurationen und Mappings.
- Schlüssel müssen unveränderlich bzw. hashbar sein.

</details>

<details>
<summary>55. Was ist der Unterschied zwischen dem Zugriff auf einen Dictionary-Wert über eckige Klammern `[]` und die Methode `get`?</summary>

#### Python

`d[key]` gibt den Wert zurück oder löst `KeyError` aus, wenn der Schlüssel fehlt.

`d.get(key, default)` gibt den Wert oder `default` (bzw. `None`) zurück, ohne Ausnahme.

```python
config = {"timeout": 30}
config["timeout"]         # 30
config.get("retries", 3)  # 3
```

**Kurz:**

- `[]` eignet sich für Pflichtschlüssel.
- `get()` eignet sich für optionale Felder.
- `get()` reduziert die Zahl von `try/except` beim Lesen von Daten.

</details>

<details>
<summary>56. Beschreiben Sie, wie man Elemente in einem Dictionary aktualisieren und löschen kann.</summary>

#### Python

Aktualisierung:

- `d[key] = value` — einen einzelnen Schlüssel einfügen/aktualisieren;
- `d.update({...})` — Massenupdate.

Löschen:

- `del d[key]` — Schlüssel löschen (Fehler, falls er fehlt);
- `d.pop(key, default)` — Wert löschen und zurückgeben;
- `d.popitem()` — letztes Paar entfernen;
- `d.clear()` — gesamtes Dictionary leeren.

**Kurz:**

- Für Upsert eignen sich `[]` und `update()`.
- Für sicheres Löschen wird häufiger `pop()` verwendet.
- Die API sollte entsprechend dem gewünschten Verhalten bei fehlendem Schlüssel gewählt werden.

</details>

<details>
<summary>57. Wofür dienen die Methoden `keys`, `values` und `items` bei Dictionaries?</summary>

#### Python

Diese Methoden geben View-Objekte des Dictionarys zurück:

- `keys()` — alle Schlüssel;
- `values()` — alle Werte;
- `items()` — Paare `(key, value)`.

```python
data = {"a": 1, "b": 2}
for key, value in data.items():
    ...
```

Views sind dynamisch und zeigen den aktuellen Zustand des Dictionarys.

**Kurz:**

- `keys/values/items` sind für Iteration und Prüfungen nötig.
- `items()` ist am bequemsten für Schleifen mit Schlüssel und Wert.
- Das sind keine Kopien, sondern „lebende“ Ansichten der Daten.

</details>

<details>
<summary>58. Wie ist ein `dict` in Python unter der Haube aufgebaut?</summary>

#### Python

`dict` ist als Hash-Tabelle mit Optimierungen für Speicher und schnellen Zugriff implementiert.
Der Schlüssel wird gehasht, über den Hash wird ein Slot gewählt und Kollisionen werden über einen internen
Probing-Algorithmus behandelt.

Praktische Folgen:

- durchschnittlicher Zugriff nahe `O(1)`;
- die Qualität von `__hash__` und `__eq__` beeinflusst das Verhalten;
- mutable Objekte können nicht als Schlüssel verwendet werden.

**Kurz:**

- `dict` ist eine hochperformante Hash-Struktur.
- Die Geschwindigkeit wird durch Hashing erreicht.
- Schlüssel müssen hashbar und stabil sein.

</details>

<details>
<summary>59. Was ist eine Hash-Funktion?</summary>

#### Python

Eine Hash-Funktion wandelt ein Objekt in eine Ganzzahl (Hash) um, die für
schnelle Platzierung und Suche in `dict` und `set` verwendet wird.

Bedingungen für Korrektheit:

- wenn `a == b`, dann muss `hash(a) == hash(b)` gelten;
- der Hash-Wert muss während der Lebensdauer des Objekts stabil bleiben.

**Kurz:**

- Die Hash-Funktion ist die Grundlage für die schnelle Arbeit von `dict/set`.
- Sie garantiert keine Eindeutigkeit, Kollisionen sind möglich.
- Für benutzerdefinierte Klassen ist die Konsistenz von `__eq__` und `__hash__` wichtig.

</details>

<details>
<summary>60. Was ist ein `set` in Python und worin unterscheidet es sich von anderen Datenstrukturen?</summary>

#### Python

`set` ist eine ungeordnete Collection **eindeutiger** Elemente.

Unterschiede:

- entfernt Duplikate automatisch;
- schnelle Membership-Checks (`x in s`);
- unterstützt mengentheoretische Operationen: Union, Intersection, Difference.

**Kurz:**

- `set` ist optimal für Eindeutigkeit und Membership-Checks.
- Die Reihenfolge der Elemente ist nicht garantiert.
- Elemente müssen hashbar sein.

</details>

<details>
<summary>61. Wie erstellt man ein `set` in Python und welche Einschränkungen gelten für seine Elemente?</summary>

#### Python

Erstellung:

```python
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # {1, 2, 3}
empty = set()            # nicht {}
```

Einschränkungen:

- Elemente müssen hashbar sein, zum Beispiel `int`, `str`, `tuple`;
- `list`, `dict` und `set` können nicht direkt hinzugefügt werden.

**Kurz:**

- `set()` erstellt eine leere Menge.
- Duplikate werden automatisch entfernt.
- Nur hashbare Elemente sind erlaubt.

</details>

<details>
<summary>62. Wofür wird die Methode `intersection()` bei einem Python-`set` verwendet und worin unterscheidet sie sich von `union()`?</summary>

#### Python

`intersection()` gibt die gemeinsamen Elemente von Mengen zurück, während `union()` alle
eindeutigen Elemente beider Mengen zusammenführt.

```python
a = {1, 2, 3}
b = {3, 4}

a.intersection(b)  # {3}
a.union(b)         # {1, 2, 3, 4}
```

**Kurz:**

- `intersection` = Schnittmenge (Gemeinsames).
- `union` = Vereinigung (alles Eindeutige).
- Beide Methoden sind grundlegend für den Vergleich von Datensätzen.

</details>

<details>
<summary>63. Welche Datentypen sind immutable?</summary>

#### Python

Verbreitete immutable Typen:

- `int`, `float`, `bool`, `complex`;
- `str`, `bytes`;
- `tuple` (wenn auch die Elemente immutable sind);
- `frozenset`;
- `NoneType`.

**Kurz:**

- Ein immutable Objekt kann nach der Erstellung nicht verändert werden.
- Statt Mutation wird ein neues Objekt erzeugt.
- Solche Typen sind sicherer als `dict`-Schlüssel oder `set`-Elemente.

</details>

<details>
<summary>64. Welche Datentypen sind mutable?</summary>

#### Python

Verbreitete mutable Typen:

- `list`;
- `dict`;
- `set`;
- `bytearray`;
- die meisten benutzerdefinierten Klassenobjekte.

**Kurz:**

- Mutable Objekte werden in-place verändert.
- Mutationen können über geteilte Referenzen Seiteneffekte erzeugen.
- Mit Kopien muss vorsichtig gearbeitet werden.

</details>

<details>
<summary>65. Warum ist es wichtig, Mutability zu verstehen, wenn man mit Dictionaries oder Sets arbeitet?</summary>

#### Python

`dict` und `set` basieren auf Hashing, deshalb müssen ihre Elemente oder Schlüssel
stabil und hashbar sein. Mutable Objekte können nicht sicher als
Schlüssel oder Set-Elemente verwendet werden.

Außerdem erzeugt die Mutation von Werten über geteilte Referenzen häufig unerwartete Bugs.

**Kurz:**

- Mutability beeinflusst die Korrektheit von Schlüsseln in `dict/set`.
- Geteilte mutable Objekte führen oft zu Seiteneffekten.
- Explizite Kopien und kontrollierte Mutationen reduzieren Bugs.

</details>

<details>
<summary>66. Was ist `None`?</summary>

#### Python

`None` ist ein spezieller Singleton-Wert vom Typ `NoneType`, der
„kein Wert vorhanden“ bedeutet.

Typische Fälle:

- eine Funktion gibt nichts explizit zurück;
- optionale Parameter;
- Marker „Daten sind noch nicht gesetzt“.

Die Prüfung erfolgt mit `is`:

```python
if value is None:
    ...
```

**Kurz:**

- `None` bedeutet das Fehlen eines Werts.
- Es ist ein Singleton, daher vergleicht man mit `is`.
- In APIs wird es oft als optionaler Zustand verwendet.

</details>

<details>
<summary>67. Was ist `id` in Python, wie verwendet man es und warum ist es wichtig?</summary>

#### Python

`id(obj)` gibt den Objektidentifikator zurück, der innerhalb des Lebenszyklus
eines Objekts im aktuellen Prozess eindeutig ist.

Nützlich für Diagnose:

- ob es dasselbe Objekt ist;
- ob eine Kopie erstellt wurde;
- ob eine Mutation über eine geteilte Referenz stattgefunden hat.

**Kurz:**

- `id` hilft bei der Analyse der Objektidentität.
- Es ist nützlich beim Debugging von Kopien und Mutationen.
- Es sollte nicht als fachlicher Identifikator verwendet werden.

</details>

<details>
<summary>68. Was ist der Unterschied zwischen den Operatoren `is` und `==`?</summary>

#### Python

`==` vergleicht **Werte** (Äquivalenz), während `is` die **Identität** vergleicht,
also ob es dasselbe Objekt im Speicher ist.

```python
a = [1, 2]
b = [1, 2]
a == b   # True
a is b   # False
```

**Wichtig zu Optimierungen (Interning):**
CPython cached bzw. „interniert“ kleine Ganzzahlen (von -5 bis 256) und kurze Strings
beim Kompilieren oder Laden. Deshalb kann `is` für solche Werte `True` zurückgeben,
selbst wenn sie separat erzeugt wurden. Darauf sollte man sich in Business-Logik aber
nicht verlassen, weil es ein Implementierungsdetail ist.

Für `None` sollte immer `is` verwendet werden.

**Kurz:**

- `==` prüft Wertgleichheit.
- `is` prüft, ob es dasselbe Objekt im Speicher ist.
- Interning kann ein nicht offensichtliches `is True` für kleine `int` und `str` liefern.
- `value is None` ist der einzig richtige Stil für die Prüfung auf `None`.

</details>

<details>
<summary>69. Wie wird das Singleton-Pattern in Python angewendet? Nennen Sie Beispiele für Singleton-Objekte in Python.</summary>

#### Python

Singleton bedeutet eine globale Objektinstanz pro Prozess.
In Python wird es oft durch den Modul-Scope ersetzt, da Module nur einmal importiert werden.

Beispiele für eingebaute Singleton-Objekte:

- `None`;
- `True` und `False`;
- `Ellipsis`.

In Anwendungscode verwendet man statt eines harten Singletons oft eher DI-Container
oder Fabriken für bessere Testbarkeit.

**Kurz:**

- Python hat bereits eingebaute Singleton-Objekte.
- Oft reicht Modul-Scope statt eines eigenen Patterns.
- Übermäßiger Einsatz von Singleton verschlechtert die Testbarkeit.

</details>

<details>
<summary>70. Wofür werden die Operatoren `break` und `continue` in Python-Schleifen verwendet?</summary>

#### Python

`break` beendet eine Schleife vorzeitig, `continue` überspringt die aktuelle Iteration
und geht zur nächsten über.

```python
for n in range(10):
    if n == 5:
        break
    if n % 2 == 0:
        continue
```

**Kurz:**

- `break` beendet die Schleife vollständig.
- `continue` überspringt nur den aktuellen Schritt.
- Beide machen die Schleifensteuerung explizit und lesbar.

</details>

<details>
<summary>71. Erklären Sie das Konzept einer Endlosschleife. In welchen Fällen ist eine Endlosschleife sinnvoll und wie stellt man ihre korrekte Beendigung sicher?</summary>

#### Python

Eine Endlosschleife ist eine Schleife ohne natürliche Abbruchbedingung, zum Beispiel `while True`.
Sie wird für Daemon- und Worker-Prozesse, Polling und Event-Loop-Logik verwendet.

Korrekte Beendigung:

- klare `break`-Bedingung;
- Verarbeitung von Beendigungssignalen;
- Timeouts und `try/finally` für Cleanup.

```python
while True:
    task = queue.get()
    if task is None:
        break
    handle(task)
```

**Kurz:**

- `while True` ist für langlebige Service-Schleifen sinnvoll.
- Es wird ein kontrollierter Stop-Mechanismus benötigt.
- Ressourcenfreigabe sollte immer vorgesehen werden.

</details>

<details>
<summary>72. Beschreiben Sie, wie verschachtelte Schleifen in Python funktionieren. Welche Performance-Probleme können dabei entstehen und wie lassen sie sich vermeiden?</summary>

#### Python

Eine verschachtelte Schleife ist eine Schleife innerhalb einer anderen Schleife. Oft wird die Komplexität zu `O(n*m)`
oder schlechter, was bei großen Datenmengen kritisch ist.

Optimierungen:

- Suchen in Listen durch `set` oder `dict` ersetzen;
- Invarianten aus der inneren Schleife herausziehen;
- Generatoren, `itertools` oder Vektorisierung einsetzen;
- „heiße“ Stellen profilieren.

**Kurz:**

- Verschachtelte Schleifen vervielfachen schnell die Rechenkosten.
- Datenstrukturen sind oft wichtiger als Mikrooptimierungen.
- Profiling zeigt, was tatsächlich optimiert werden muss.

</details>

<details>
<summary>73. Was ist Structural Pattern Matching (`match`/`case`)?</summary>

#### Python

`match/case` (Python 3.10+) ist ein Mechanismus zum Analysieren von Datenstrukturen anhand von Mustern.
Er funktioniert mit Literalen, Typen, Sequenzen, Dictionaries und Klassen.

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

**Kurz:**

- `match/case` ist bei komplexer Verzweigung oft besser lesbar.
- Es erlaubt, gleichzeitig die Form zu prüfen und Daten zu extrahieren.
- Besonders nützlich ist es für Protokolle, Events und das Parsen von Strukturen.

</details>

<details>
<summary>74. In welchen Fällen ist Pattern Matching besser als `if`/`elif`?</summary>

#### Python

`match/case` ist besser, wenn man:

- viele gegenseitig ausschließende Datenformen prüfen muss;
- verschachtelte Strukturen entpacken muss;
- lange `if/elif`-Ketten vermeiden will.

`if/elif` ist besser für einfache boolesche Bedingungen und kurze Logik.

**Kurz:**

- Für strukturelle Szenarien ist `match/case` besser.
- Für einfache Bedingungen reicht `if/elif`.
- Das Auswahlkriterium ist Lesbarkeit und Wartbarkeit.

</details>

<details>
<summary>75. Was ist eine Funktion in Python?</summary>

#### Python

Eine Funktion ist ein benannter aufrufbarer Codeblock, der Argumente entgegennimmt,
ein Ergebnis zurückgibt und die Kapselung von Logik ermöglicht.

```python
def normalize_name(name: str) -> str:
    return name.strip().title()
```

Funktionen unterstützen Default-Werte, Keyword-Argumente, `*args/**kwargs`,
Typannotationen und Dekoratoren.

**Kurz:**

- Eine Funktion ist die grundlegende Einheit für wiederverwendbaren Code.
- Sie definiert einen klaren Vertrag über Parameter und Rückgabewert.
- Type Hints machen diesen Vertrag explizit.

</details>

<details>
<summary>76. Welche Arten von Funktionsargumenten gibt es?</summary>

#### Python

Im modernen Python:

- positional-only (`/`);
- positional-or-keyword;
- keyword-only (`*`);
- variadic positional (`*args`);
- variadic keyword (`**kwargs`).

```python
def f(a, /, b, *, c, **kwargs):
    ...
```

**Kurz:**

- Python bietet flexible Kontrolle über die Aufrufweise einer Funktion.
- `/` und `*` formalisieren den API-Vertrag.
- `*args/**kwargs` sind nützlich für erweiterbare Interfaces.

</details>

<details>
<summary>77. Was sind Positionsargumente und benannte Argumente?</summary>

#### Python

Positionsargumente werden nach Reihenfolge übergeben, benannte (`keyword`) nach dem Namen
des Parameters.

```python
def connect(host: str, port: int) -> str:
    return f"{host}:{port}"

connect("localhost", 5432)           # positional
connect(host="localhost", port=5432) # keyword
```

**Kurz:**

- Positionsargumente hängen von der Reihenfolge der Parameter ab.
- Benannte Argumente erhöhen die Lesbarkeit des Aufrufs.
- Beide lassen sich kombinieren, sofern die Signaturregeln eingehalten werden.

</details>

<details>
<summary>78. Was sind Default-Argumente und welche Probleme können mit ihnen auftreten?</summary>

#### Python

Default-Argumente werden verwendet, wenn beim Aufruf kein Wert übergeben wird.
Sie werden **einmal** bei der Definition der Funktion ausgewertet.

Problem: mutable Default-Werte.

```python
def add_item(item: int, bucket: list[int] | None = None) -> list[int]:
    if bucket is None:
        bucket = []
    bucket.append(item)
    return bucket
```

**Kurz:**

- Default-Werte sind praktisch für stabile Werte.
- Ein mutable Default kann Zustand zwischen Aufrufen ansammeln.
- Das sichere Muster ist: `None` + Initialisierung innerhalb der Funktion.

</details>

<details>
<summary>79. Erklären Sie Zweck und Verwendung von `*args` und `**kwargs` in Python-Funktionen. Worin unterscheiden sie sich?</summary>

#### Python

`*args` sammelt zusätzliche Positionsargumente in einem `tuple`.
`**kwargs` sammelt zusätzliche benannte Argumente in einem `dict`.

```python
def log_event(event: str, *args: object, **kwargs: object) -> None:
    ...
```

Verwendung: Wrapper, API-Adapter, Dekoratoren, Weiterreichen von Parametern.

**Kurz:**

- `*args` = zusätzliche Positionsargumente.
- `**kwargs` = zusätzliche benannte Argumente.
- Sie machen Funktionen flexibel, erfordern aber klare Validierung.

</details>

<details>
<summary>80. Wie definiert man eine Funktion mit Type Annotations in Python? Geben Sie ein Beispiel und erklären Sie die Vorteile dieses Ansatzes.</summary>

#### Python

Typen werden in der Signatur der Parameter und des Rückgabewerts angegeben.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Vorteile:

- bessere Developer Experience (Autocomplete, Navigation);
- statische Prüfung in CI;
- expliziter Vertrag für andere Entwickler.

**Kurz:**

- Typannotationen dokumentieren das API.
- Sie reduzieren das Risiko von Integrationsfehlern.
- Den größten Nutzen bringen sie in mittelgroßen und großen Codebasen.

</details>

<details>
<summary>81. Was sind Lambda-Funktionen?</summary>

#### Python

`lambda` ist eine anonyme Ein-Ausdruck-Funktion.
Sie wird meist für kurze Callbacks in `sorted`, `map` oder `filter` verwendet.

```python
users = [{"name": "Ada"}, {"name": "Bob"}]
users_sorted = sorted(users, key=lambda u: u["name"])
```

Für komplexere Logik ist eine normale `def`-Funktion besser geeignet.

**Kurz:**

- `lambda` ist praktisch für kurze lokale Ausdrücke.
- Sie ist auf einen einzigen Ausdruck beschränkt.
- Für bessere Lesbarkeit sollte komplexer Code in eine `def` ausgelagert werden.

</details>

<details>
<summary>82. Welchen Gültigkeitsbereich haben Variablen in einer Funktion?</summary>

#### Python

Python verwendet für die Namensauflösung die LEGB-Regel:

- `L`ocal;
- `E`nclosing (äußere Funktionen);
- `G`lobal (Modul);
- `B`uiltins.

Innerhalb einer Funktion erzeugt eine Zuweisung eine lokale Variable, sofern nicht
`global` oder `nonlocal` angegeben wurde.

**Kurz:**

- Scope bestimmt, wo ein Name verfügbar und veränderbar ist.
- LEGB erklärt die Reihenfolge der Variablensuche.
- Ein falsches Verständnis von Scope führt oft zu `UnboundLocalError`.

</details>

<details>
<summary>83. Was sind lokale und globale Variablen in Python?</summary>

#### Python

Lokale Variablen leben im Funktionskörper.
Globale Variablen sind auf Modulebene definiert.

Um eine globale Variable in einer Funktion zu ändern, braucht man `global`, aber das
sollte wegen impliziter Abhängigkeiten meist vermieden werden.

**Kurz:**

- Lokale Variablen sind sicherer für Wartung und Tests.
- Globale Variablen vereinfachen den Zugriff, erschweren aber die Zustandskontrolle.
- Abhängigkeiten sollten besser über Parameter übergeben werden.

</details>

<details>
<summary>84. Was ist der Unterschied zwischen lokalen und `nonlocal`-Variablen in Python?</summary>

#### Python

`nonlocal` wird in einer verschachtelten Funktion verwendet, um eine Variable aus dem
nächstgelegenen Enclosing-Scope zu verändern, nicht aus dem globalen.

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

**Kurz:**

- Eine lokale Variable gehört zur aktuellen Funktion.
- `nonlocal` verändert den Zustand einer äußeren Funktion.
- Das ist ein zentraler Mechanismus für Closures mit Zustand.

</details>

<details>
<summary>85. Was ist Unpacking in Python und wie wird es bei Zuweisungen verwendet?</summary>

#### Python

Unpacking ist das Zerlegen von Elementen einer Sequenz oder Struktur in einzelne Variablen.

```python
x, y = (10, 20)
first, *middle, last = [1, 2, 3, 4]
```

Es funktioniert auch mit Dictionaries in `match/case`, bei Funktionsaufrufen und in Schleifen.

**Kurz:**

- Unpacking macht Code kompakter und lesbarer.
- Es unterstützt das „Sternchen“-Sammeln der restlichen Werte.
- Es wird häufig beim Parsen von Datenstrukturen verwendet.

</details>

<details>
<summary>86. Erklären Sie das Konzept des Packings von Werten in Python und geben Sie Beispiele.</summary>

#### Python

Packing ist das Zusammenfassen mehrerer Werte in einer Struktur wie `tuple`, `list` oder `dict`.

```python
point = 10, 20                 # tuple packing

def collect(*args: int) -> tuple[int, ...]:
    return args
```

`*args` und `**kwargs` sind typische Beispiele für Argument-Packing.

**Kurz:**

- Packing sammelt viele Werte in einem Container.
- Am häufigsten wird es in Funktionssignaturen verwendet.
- Es lässt sich gut mit Unpacking auf Aufruferseite kombinieren.

</details>

<details>
<summary>87. Wofür verwendet man den Operator `*` beim Packing und Unpacking?</summary>

#### Python

`*` packt in Funktionsparametern Positionsargumente (`*args`) und entpackt bei einem Aufruf
ein Iterable in Positionsargumente.

```python
def add(a: int, b: int) -> int:
    return a + b

nums = [2, 3]
add(*nums)  # 5
```

Außerdem wird `*` bei Zuweisungen verwendet, um den „Rest“ der Elemente aufzufangen.

**Kurz:**

- `*` ist ein universeller Operator für den Umgang mit Varargs.
- In der Signatur packt er, im Aufruf entpackt er.
- Er reduziert Boilerplate bei der Datenübergabe.

</details>

<details>
<summary>88. Was ist ein Closure und welche Beziehung hat es zu Decorators?</summary>

#### Python

Ein Closure ist eine innere Funktion, die sich an Variablen aus dem Enclosing-Scope erinnert,
selbst nachdem die äußere Funktion beendet wurde.

Decoratoren werden meist genau über Closures implementiert: Der Wrapper speichert Referenzen
auf die Originalfunktion und zusätzliche Parameter.

**Kurz:**

- Ein Closure ist Funktion plus eingefangener Kontext.
- Ein Decorator ist oft eine praktische Anwendung eines Closures.
- Damit lässt sich Verhalten ergänzen, ohne den Funktionskörper zu ändern.

</details>

<details>
<summary>89. Was ist ein Decorator in Python und wie funktioniert er?</summary>

#### Python

Ein Decorator ist ein Callable, das eine Funktion oder Klasse entgegennimmt und eine modifizierte
Version, also einen Wrapper, zurückgibt.

```python
from functools import wraps

def log_calls(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Anwendungsfälle: Logging, Caching, Autorisierung, Retries, Metriken.

**Kurz:**

- Ein Decorator fügt Querschnittsverhalten hinzu.
- Er arbeitet durch das Wrappen eines Callables.
- So muss technische Logik nicht im Business-Code dupliziert werden.

</details>

<details>
<summary>90. Kann man mehrere Decorators für eine Funktion verwenden?</summary>

#### Python

Ja, mehrere Decorators können gestapelt werden.
Sie werden von unten nach oben angewendet, also wird der näher bei `def` stehende zuerst umhüllt.

```python
@decorator_a
@decorator_b
def handler() -> None:
    ...
```

Äquivalent: `handler = decorator_a(decorator_b(handler))`.

**Kurz:**

- Mehrere Decorators sind zulässig und verbreitet.
- Die Reihenfolge ihrer Anwendung ist wichtig.
- Die Kette der Decorators sollte zur besseren Nachvollziehbarkeit dokumentiert werden.

</details>

<details>
<summary>91. Beschreiben Sie ein mögliches Problem mit der Reihenfolge von Decorators bei ihrer Anwendung auf eine Funktion.</summary>

#### Python

Eine falsche Reihenfolge kann die Semantik verändern: Zum Beispiel kann Caching vor einer
Zugriffsprüfung ein unerwünschtes Ergebnis cachen oder die erwartete Logik umgehen.

Typische Risiken:

- Logging sieht bereits veränderte Argumente;
- Retries wrappen die falsche Exception;
- Caching wird vor oder nach der Validierung an der falschen Stelle angewendet.

**Kurz:**

- Die Reihenfolge von Decorators beeinflusst das Verhalten einer Funktion.
- Das ist eine häufige Ursache versteckter Bugs.
- Für kritische Chains sind Tests für die Ausführungsreihenfolge nötig.

</details>

<details>
<summary>92. Kann man einen Decorator mit Hilfe einer Klasse erstellen?</summary>

#### Python

Ja. Ein Klassen-Decorator implementiert `__call__`, damit sich die Instanz wie eine Funktion verhält.

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.calls = 0

    def __call__(self, *args, **kwargs):
        self.calls += 1
        return self.func(*args, **kwargs)
```

**Kurz:**

- Ein Decorator kann nicht nur als Funktion, sondern auch als Klasse implementiert werden.
- Eine Klasse ist praktisch, wenn interner Zustand benötigt wird.
- Der zentrale Mechanismus ist `__call__`.

</details>

<details>
<summary>93. Wie definiert man einen Decorator, der Parameter annimmt?</summary>

#### Python

Man braucht eine dreistufige Struktur: Decorator-Fabrik -> Decorator -> Wrapper.

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

**Kurz:**

- Ein parametrisierter Decorator ist eine Funktion, die einen Decorator zurückgibt.
- Oft wird ein Closure verwendet, um Parameter zu speichern.
- Dieser Ansatz ist praktisch für konfigurierbares Verhalten.

</details>

<details>
<summary>94. Wofür verwendet man `functools.wraps` in Decorator-Funktionen?</summary>

#### Python

`functools.wraps` kopiert Metadaten der Originalfunktion in den Wrapper:
Name, Docstring, Modul sowie `__wrapped__`.

Das ist wichtig für:

- korrektes Debugging und Logs;
- Introspektion und Dokumentation;
- Kompatibilität mit Werkzeugen, die die Signatur lesen.

**Kurz:**

- `wraps` bewahrt die „Identität“ der Originalfunktion.
- Ohne `wraps` verlieren dekorierte Funktionen nützliche Metadaten.
- Es ist Best Practice für alle Wrapper-Decorators.

</details>

<details>
<summary>95. Wie funktionieren Dict-, List- und Set-Comprehensions?</summary>

#### Python

Eine Comprehension erzeugt eine Collection aus einem Ausdruck und einer oder mehreren Schleifen, optional mit Filter.

```python
squares = [x * x for x in range(6)]
mapping = {x: x * x for x in range(6)}
unique = {x % 3 for x in range(10)}
```

Format:

- list: `[expr for x in it if cond]`
- set: `{expr for x in it if cond}`
- dict: `{k_expr: v_expr for x in it if cond}`

**Kurz:**

- Comprehensions drücken Datentransformation kompakt aus.
- Sie funktionieren für `list`, `set` und `dict`.
- Sie ergeben saubereren Code als manuelles Hinzufügen in einer Schleife.

</details>

<details>
<summary>96. Welche Vorteile haben List Comprehensions im Vergleich zu normalen Schleifen?</summary>

#### Python

Vorteile:

- kürzerer und deklarativerer Code;
- weniger Hilfsvariablen;
- meist etwas bessere Performance in CPython;
- geringeres Risiko, ein `append` zu vergessen.

Nachteil: Bei sehr komplexer Logik verschlechtert eine Comprehension die Lesbarkeit.

**Kurz:**

- List Comprehensions eignen sich gut für einfache Transformationen.
- Sie sind oft schneller und sauberer als eine manuelle Schleife.
- Für komplexe Verzweigungen ist ein normales `for` besser.

</details>

<details>
<summary>97. Können Sie ein Beispiel für eine verschachtelte List Comprehension geben?</summary>

#### Python

Beispiel für das Flatten einer Matrix:

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for row in matrix for item in row]  # [1, 2, 3, 4, 5, 6]
```

Beispiel mit Bedingung:

```python
pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
```

**Kurz:**

- Eine verschachtelte Comprehension enthält mehrere `for` in einem Ausdruck.
- Die Reihenfolge der `for` entspricht verschachtelten Schleifen.
- Sie sollte verwendet werden, solange der Ausdruck lesbar bleibt.

</details>

<details>
<summary>98. Was ist in Python schneller: eine List Comprehension oder das Erstellen einer Liste mit einer Schleife?</summary>

#### Python

In typischen Szenarien ist eine List Comprehension etwas schneller als eine Schleife mit `append`,
weil sie optimierten Bytecode und weniger Overhead hat.

Wichtig ist: Der reale Gewinn hängt vom Funktionskörper ab, daher sollte man kritische
Stellen mit `timeit` oder `pyperf` messen.

**Kurz:**

- Oft ist die List Comprehension schneller.
- Der Unterschied kann aber klein sein.
- Für Produktionsentscheidungen sollten Messungen ausschlaggebend sein.

</details>

<details>
<summary>99. Was ist ein Iterator in Python?</summary>

#### Python

Ein Iterator ist ein Objekt, das Elemente nacheinander liefert und seinen aktuellen Zustand speichert.
Er implementiert das Protokoll:

- `__iter__()` gibt sich selbst zurück;
- `__next__()` liefert das nächste Element oder löst `StopIteration` aus.

**Kurz:**

- Ein Iterator bietet elementweisen Zugriff ohne vollständiges Laden aller Daten.
- Er ist die Grundlage für `for`, Generatoren und lazy Verarbeitung.
- Nach dem Verbrauch wird ein Iterator nicht automatisch „zurückgespult“.

</details>

<details>
<summary>100. Wie erzeugt man mit der Funktion `iter()` einen Iterator aus einem iterierbaren Objekt?</summary>

#### Python

Rufen Sie `iter(iterable)` auf, um einen Iterator zu erhalten.

```python
items = [10, 20, 30]
it = iter(items)
```

Danach werden Werte über `next(it)` gelesen.

**Kurz:**

- `iter()` wandelt ein Iterable in einen Iterator um.
- Das ist eine explizite Methode zur manuellen Steuerung der Iteration.
- Sie wird bei Low-Level-Stream-Verarbeitung eingesetzt.

</details>

<details>
<summary>101. Wofür dient die Funktion `next()` bei der Arbeit mit Iteratoren?</summary>

#### Python

`next(iterator[, default])` gibt das nächste Element eines Iterators zurück.
Wenn keine Elemente mehr vorhanden sind, wird `StopIteration` ausgelöst oder
`default` zurückgegeben, falls es übergeben wurde.

```python
it = iter([1, 2])
next(it)        # 1
next(it)        # 2
next(it, None)  # None
```

**Kurz:**

- `next()` gibt manuelle Kontrolle über die Iterationsschritte.
- Ohne `default` führt das Ende des Streams zu `StopIteration`.
- Mit `default` kann ein Stream sicher gelesen werden.

</details>

<details>
<summary>102. Kann man die Methoden `__next__()` und `__iter__()` austauschbar mit den Funktionen `next()` und `iter()` verwenden?</summary>

#### Python

Ja, aber mit einer Protokoll-Besonderheit:

- `iter(obj)` ruft `obj.__iter__()` auf;
- `next(it)` ruft `it.__next__()` auf.

Die Funktionen sind also die Standardschnittstelle zu den Dunder-Methoden und
werden normalerweise statt direkter Aufrufe verwendet.

**Kurz:**

- `iter()` entspricht `__iter__()`.
- `next()` entspricht `__next__()`.
- Im Anwendungscode sollte man die Built-in-Funktionen bevorzugen.

</details>

<details>
<summary>103. Welche Rolle spielt `StopIteration` beim Entwurf von Iteratoren und wann tritt sie typischerweise auf?</summary>

#### Python

`StopIteration` signalisiert, dass ein Iterator erschöpft ist.
Eine `for`-Schleife fängt diese Exception automatisch ab und beendet die Iteration.

Sie tritt typischerweise auf:

- beim Aufruf von `next(it)` nach dem letzten Element;
- in benutzerdefinierten Iteratoren, wenn die Daten aufgebraucht sind.

**Kurz:**

- `StopIteration` ist das normale Ende eines Datenstroms.
- Im normalen Ablauf sollte sie nicht als "Fehler" geloggt werden.
- In eigenen Iteratoren muss sie korrekt ausgelöst werden.

</details>

<details>
<summary>104. Was ist ein Generator und wie unterscheidet er sich von einem Iterator oder einer normalen Funktion?</summary>

#### Python

Ein Generator ist ein spezieller Iterator, der durch eine Funktion mit `yield`
erzeugt wird. Er liefert Werte einzeln und behält seinen internen Zustand zwischen
den Aufrufen.

Unterschiede:

- zu einer normalen Funktion: endet nicht mit einem einzigen `return`, sondern arbeitet mit "Pause/Fortsetzung";
- zu einem manuellen Iterator: einfachere Implementierung ohne explizite Klasse mit `__next__`.

**Kurz:**

- Ein Generator ist die bequemste Form der Lazy-Iteration.
- Er benötigt weniger Code als eine eigene Iterator-Klasse.
- Besonders nützlich für große Datenströme.

</details>

<details>
<summary>105. Wie erstellt man eine Generator-Funktion?</summary>

#### Python

Dafür definiert man eine Funktion mit `yield`.

```python
def countdown(start: int):
    current = start
    while current > 0:
        yield current
        current -= 1
```

Der Aufruf `countdown(3)` gibt ein Generator-Objekt zurück, über das iteriert werden kann.

**Kurz:**

- Das Vorhandensein von `yield` macht eine Funktion zu einem Generator.
- Ein Generator liefert Werte schrittweise zurück.
- Der Funktionszustand bleibt zwischen den Iterationen erhalten.

</details>

<details>
<summary>106. Wie ermöglicht das Schlüsselwort `yield` die Funktionalität von Generatoren und warum sparen sie Speicher?</summary>

#### Python

`yield` gibt den nächsten Wert zurück und "friert" den Kontext der Funktion ein
(lokale Variablen, Ausführungsposition). Das nächste `next()` setzt die Ausführung
genau an dieser Stelle fort.

Speicherersparnis: Daten werden nicht vollständig vorab erzeugt, sondern bei Bedarf berechnet.

**Kurz:**

- `yield` implementiert Pause und Fortsetzung der Ausführung.
- Ein Generator unterstützt Lazy Evaluation.
- Das reduziert den Speicherverbrauch bei großen Datenmengen.

</details>

<details>
<summary>107. Worin besteht der Unterschied zwischen `return` und `yield`?</summary>

#### Python

`return` beendet eine Funktion und gibt einen finalen Wert zurück.
`yield` gibt einen Zwischenwert zurück und behält den Zustand für die spätere Fortsetzung.

In einem Generator bedeutet `return` das Ende der Iteration (`StopIteration`).

**Kurz:**

- `return` beendet die Funktion.
- `yield` liefert Werte schrittweise.
- `yield` wird für Stream- und Pipeline-Verarbeitung verwendet.

</details>

<details>
<summary>108. Was ist Object-Oriented Programming (OOP) und was sind seine Hauptprinzipien in Python?</summary>

#### Python

OOP ist ein Ansatz, bei dem Daten und Verhalten in Objekten gebündelt werden.

Zentrale Prinzipien:

- Kapselung;
- Vererbung;
- Polymorphismus;
- Abstraktion.

In Python wird OOP meist mit Komposition und Duck Typing kombiniert.

**Kurz:**

- OOP strukturiert die Domäne über Klassen und Objekte.
- Python unterstützt OOP flexibel, ohne übermäßigen Boilerplate-Code.
- In der Praxis ist Komposition oft besser als tiefe Vererbung.

</details>

<details>
<summary>109. Was ist eine `class` in Python?</summary>

#### Python

Eine `class` ist eine Vorlage für die Erzeugung von Objekten mit Attributen und Methoden.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name
```

Die Klasse definiert Struktur und Verhalten zukünftiger Instanzen.

**Kurz:**

- Eine Klasse beschreibt Daten und Operationen darauf.
- Auf Basis einer Klasse werden Objekte (Instanzen) erstellt.
- Sie ist die grundlegende Modellierungseinheit in OOP.

</details>

<details>
<summary>110. Wie erstellt man ein Objekt in Python?</summary>

#### Python

Ein Objekt wird durch den Aufruf einer Klasse erstellt:

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

user = User("Ada")
```

Während der Erstellung wird `__init__` zur Initialisierung des Zustands ausgeführt.

**Kurz:**

- Ein Objekt ist eine Instanz einer Klasse.
- Erstellung: `instance = ClassName(...)`.
- `__init__` richtet die Anfangsattribute ein.

</details>

<details>
<summary>111. Was sind Objekte und Attribute?</summary>

#### Python

Ein Objekt ist eine konkrete Instanz eines Typs bzw. einer Klasse.
Ein Attribut ist ein mit dem Objekt verbundenes Name-Wert-Paar (Daten oder Methode).

```python
user.name       # Datenattribut
user.save()     # Methodenattribut
```

**Kurz:**

- Ein Objekt speichert Zustand und Verhalten.
- Attribute beschreiben diesen Zustand bzw. dieses Verhalten.
- Auf Attribute wird per Punktnotation zugegriffen.

</details>

<details>
<summary>112. Welche Rolle hat die Methode `__init__()` in einer Klasse?</summary>

#### Python

`__init__` ist der Initialisierer einer Instanz: Er wird nach der Objekterzeugung
aufgerufen und setzt den Anfangszustand.

```python
class Account:
    def __init__(self, owner: str, balance: float = 0.0) -> None:
        self.owner = owner
        self.balance = balance
```

**Kurz:**

- `__init__` setzt die Startattribute eines Objekts.
- Es dient als Einstiegspunkt für die Konfiguration der Instanz.
- Es erstellt das Objekt nicht, sondern initialisiert es nur.

</details>

<details>
<summary>113. Wofür dient der Parameter `self` in Methoden einer Python-Klasse?</summary>

#### Python

`self` ist eine Referenz auf die aktuelle Instanz. Darüber liest oder verändert
eine Methode die Instanzattribute.

```python
def deposit(self, amount: float) -> None:
    self.balance += amount
```

Der Name `self` ist syntaktisch nicht reserviert, aber der allgemein anerkannte Standard.

**Kurz:**

- `self` bindet eine Methode an ein konkretes Objekt.
- Über `self` sind Instanzdaten erreichbar.
- Es ist der verpflichtende erste Parameter einer Instanzmethode.

</details>

<details>
<summary>114. Wie definiert man Methoden in einer Klasse?</summary>

#### Python

Methoden werden als Funktionen innerhalb von `class` definiert.

```python
class Calculator:
    def add(self, a: int, b: int) -> int:
        return a + b
```

Typische Arten: Instanzmethode (`self`), Klassenmethode (`@classmethod`, `cls`) und statische Methode (`@staticmethod`, ohne `self/cls`).

**Kurz:**

- Eine Methode ist eine Funktion im Klassenkörper.
- Der Methodentyp wird durch Decorator und Signatur bestimmt.
- Am häufigsten wird die Instanzmethode verwendet.

</details>

<details>
<summary>115. Erklären Sie das Konzept "Alles ist ein Objekt" in Python und nennen Sie Beispiele.</summary>

#### Python

In Python ist fast alles ein Objekt: Zahlen, Strings, Funktionen, Klassen, Module.
Deshalb hat nahezu alles einen Typ, Attribute und Verhalten.

```python
type(10)          # <class 'int'>
type(len)         # <class 'builtin_function_or_method'>
type(str)         # <class 'type'>
```

**Kurz:**

- Das einheitliche Objektmodell vereinfacht die Sprache.
- Funktionen und Klassen sind ebenfalls First-Class-Objekte.
- Das macht Python flexibel für Metaprogrammierung.

</details>

<details>
<summary>116. Geben Sie ein Beispiel für eine Klasse mit Methoden, die Berechnungen auf Basis von Attributen ausführen.</summary>

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

**Kurz:**

- Methoden können Werte aus Instanzattributen berechnen.
- Das kapselt Domänenlogik im Objekt.
- Die API der Klasse wird dadurch selbstdokumentierend.

</details>

<details>
<summary>117. Beschreiben Sie eine Situation, in der mehrere Klassen in einem Python-Programm sinnvoll sind.</summary>

#### Python

Wenn eine Domäne mehrere Verantwortlichkeiten hat, werden sie auf mehrere Klassen verteilt.
Beispiel im E-Commerce: `Order`, `OrderItem`, `PaymentService`, `InventoryService`.

Das bringt:

- eine klare Verantwortungsverteilung;
- geringere Kopplung;
- einfacheren Austausch und einfacheres Testen von Komponenten.

**Kurz:**

- Mehrere Klassen sind nötig, um eine komplexe Domäne zu modellieren.
- Die Verteilung von Verantwortlichkeiten verbessert die Wartbarkeit.
- Komposition von Klassen ist meist besser als ein "God Object".

</details>

<details>
<summary>118. Worin besteht der Unterschied zwischen Instance Method, Class Method und Static Method?</summary>

#### Python

- Instance Method: hat `self` und arbeitet mit einer konkreten Instanz.
- Class Method: hat `cls` und arbeitet mit der Klasse als Ganzes.
- Static Method: hat weder `self` noch `cls`; sie ist eine Hilfsfunktion im Namespace der Klasse.

**Kurz:**

- Instance -> Logik der Instanz.
- Class -> Logik der Klasse bzw. alternative Konstruktoren.
- Static -> Hilfslogik ohne Zugriff auf Zustand.

</details>

<details>
<summary>119. Was ist `@classmethod` in Python und worin unterscheidet es sich von normalen Methoden?</summary>

#### Python

`@classmethod` übergibt als erstes Argument die Klasse (`cls`) statt einer Instanz.
Es wird häufig für Factory-Methoden verwendet.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

    @classmethod
    def from_email(cls, email: str) -> User:
        return cls(email.split("@")[0])
```

**Kurz:**

- `classmethod` arbeitet auf Klassenebene.
- Es ist praktisch für alternative Konstruktoren.
- Es benötigt keine bereits erzeugte Instanz.

</details>

<details>
<summary>120. Was ist `@staticmethod` in Python-Klassen und wann sollte man es verwenden?</summary>

#### Python

`@staticmethod` definiert eine Methode ohne automatisches `self` oder `cls`.
Sie gehört logisch zur Klasse, hängt aber nicht von ihrem Zustand ab.

```python
class Math:
    @staticmethod
    def clamp(value: int, min_v: int, max_v: int) -> int:
        return max(min_v, min(value, max_v))
```

**Kurz:**

- `staticmethod` ist eine Funktion im Namespace der Klasse.
- Sie eignet sich für Hilfslogik ohne Zugriff auf Attribute.
- Sie ist ungeeignet, wenn Instanz- oder Klassenzustand benötigt wird.

</details>

<details>
<summary>121. Worin besteht der Unterschied zwischen `@classmethod` und `@staticmethod` in Python-Klassen?</summary>

#### Python

Der Unterschied liegt im ersten Argument und in der Zugriffsebene:

- `@classmethod` erhält `cls` und kann mit dem Klassenzustand arbeiten;
- `@staticmethod` erhält nichts automatisch.

`classmethod` wird häufiger für Fabriken bzw. polymorphe Konstruktoren verwendet,
`staticmethod` für Hilfsfunktionen.

**Kurz:**

- `classmethod` kennt die Klasse.
- `staticmethod` ist vom Klassen- und Instanzzustand isoliert.
- Die Wahl hängt davon ab, ob Zugriff auf `cls` benötigt wird.

</details>

<details>
<summary>122. Was sind Instanzattribute in Python-Klassen und worin unterscheiden sie sich von Klassenattributen?</summary>

#### Python

Instanzattribute gehören zu einem konkreten Objekt (`self.x`).
Klassenattribute gehören zur Klasse und werden von allen Instanzen gemeinsam genutzt.

```python
class User:
    role = "member"           # Klassenattribut
    def __init__(self, name: str) -> None:
        self.name = name      # Instanzattribut
```

**Kurz:**

- Instanzattribute speichern individuellen Zustand.
- Klassenattribute speichern gemeinsame Konfiguration.
- Änderungen an Klassenattributen wirken sich auf alle Instanzen aus.

</details>

<details>
<summary>123. Was ist `__slots__` in Python?</summary>

#### Python

`__slots__` begrenzt die Menge erlaubter Attribute in einer Klasse und kann den
Speicherverbrauch verringern, indem `__dict__` für Instanzen entfernt wird.

```python
class Point:
    __slots__ = ("x", "y")
    def __init__(self, x: int, y: int) -> None:
        self.x = x
        self.y = y
```

**Wichtige Details zur Verwendung:**

- **Speicherersparnis:** Objekte benötigen deutlich weniger Platz, weil Attribute
  in einem festen Array und nicht in der Hashtabelle `__dict__` gespeichert werden.
- **Geschwindigkeit:** Der Zugriff auf Attribute in `__slots__` ist meist etwas schneller.
- **Kein `__dict__`:** Neue Attribute lassen sich nicht dynamisch hinzufügen,
  sofern sie nicht in `__slots__` enthalten sind (außer man fügt `"__dict__"` explizit hinzu).
- **Schwache Referenzen:** Wenn `weakref` genutzt werden soll, muss
  `"__weakref__"` explizit in `__slots__` aufgenommen werden.

**Kurz:**

- `__slots__` ist nützlich für Millionen leichtgewichtiger Objekte, z. B. Graphknoten.
- Es entfernt standardmäßig `__dict__` und `__weakref__`.
- Es reduziert Flexibilität zugunsten von Performance und Kontrolle.

</details>

<details>
<summary>124. Was sind Magic Methods (Dunder-Methoden) in Python-Klassen und warum nennt man sie "magisch"?</summary>

#### Python

Dunder-Methoden (`__init__`, `__str__`, `__len__`, `__eq__`, ...) sind spezielle
Hooks, die Python automatisch als Reaktion auf Operatoren und Built-ins aufruft.

Sie werden "magisch" genannt, weil sie Ihre Klasse in das Verhalten der Sprache integrieren.

**Kurz:**

- Dunder-Methoden definieren das protokollbasierte Verhalten eines Objekts.
- Sie ermöglichen, dass sich eigene Klassen wie eingebaute Typen verhalten.
- Sie sollten nur verwendet werden, wenn eine klare semantische Notwendigkeit besteht.

</details>

<details>
<summary>125. Wofür ist die Methode `__del__` gedacht?</summary>

#### Python

`__del__` ist ein Finalizer, der vor der Zerstörung eines Objekts durch den GC
aufgerufen werden kann. Sein Verhalten ist nicht deterministisch, deshalb sollte
für Ressourcenverwaltung besser `with` und ein explizites Schließen verwendet werden.

**Kurz:**

- `__del__` garantiert keine rechtzeitige Ausführung.
- Kritisches Cleanup sollte nicht allein darauf aufbauen.
- Empfohlener Ansatz: `with` bzw. `try-finally`.

</details>

<details>
<summary>126. Geben Sie ein Beispiel für die Verwendung der Magic Method `__str__`, um die Textdarstellung einer eigenen Klasse in Python festzulegen.</summary>

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

`str(user)` und `print(user)` verwenden `__str__`.

**Kurz:**

- `__str__` liefert eine menschenlesbare Darstellung eines Objekts.
- Das ist nützlich für Logs und CLI-Ausgaben.
- Die Darstellung sollte kurz und gut lesbar sein.

</details>

<details>
<summary>127. Wofür werden `__str__` und `__repr__` verwendet?</summary>

#### Python

`__str__` ist auf den Endleser ausgerichtet.
`__repr__` ist für Entwickler und Debugging gedacht und sollte möglichst eindeutig sein.

`print(obj)` verwendet in der Regel `__str__`,
während REPL und `repr(obj)` `__repr__` verwenden.

**Kurz:**

- `__str__` dient der benutzerfreundlichen Ausgabe.
- `__repr__` dient der technischen Darstellung.
- Gute Praxis: Bei Domänenklassen beide implementieren.

</details>

<details>
<summary>128. Wie funktioniert Operator Overloading in Python und warum ist es nützlich?</summary>

#### Python

Operator Overloading bedeutet die Implementierung von Dunder-Methoden für Operatoren
(`__add__`, `__sub__`, `__eq__`, ...), damit Objekte einer eigenen Klasse Operatoren unterstützen.

```python
class Vector2:
    def __init__(self, x: float, y: float) -> None:
        self.x = x
        self.y = y

    def __add__(self, other: "Vector2") -> "Vector2":
        return Vector2(self.x + other.x, self.y + other.y)
```

**Kurz:**

- Es ermöglicht natürliche Syntax für Domänentypen.
- Es verbessert die Ausdruckskraft der API.
- Wichtig ist, die mathematisch erwartete Semantik beizubehalten.

</details>

<details>
<summary>129. Was ist Inheritance (Vererbung)?</summary>

#### Python

Vererbung ermöglicht es, eine abgeleitete Klasse zu erstellen, die Attribute und Methoden
einer Basisklasse erbt und Verhalten erweitern oder überschreiben kann.

**Kurz:**

- Vererbung fördert Wiederverwendung von Code.
- Eine abgeleitete Klasse kann Methoden der Basisklasse überschreiben.
- Zu tiefe Hierarchien erschweren die Wartung, daher ist Komposition oft besser.

</details>

<details>
<summary>130. Was ist Single Inheritance in Python?</summary>

#### Python

Single Inheritance bedeutet, dass eine Klasse genau eine direkte Basisklasse hat.

```python
class Animal:
    ...

class Dog(Animal):
    ...
```

Das ist die einfachste und meist auch lesbarste Form der Vererbung.

**Kurz:**

- Eine abgeleitete Klasse -> eine Basisklasse.
- Einfaches Modell der Methodenauflösung.
- Für die meisten Geschäftsmodelle oft völlig ausreichend.

</details>

<details>
<summary>131. Wie implementiert man Vererbung in Python-Klassen und welche Syntax wird dafür verwendet?</summary>

#### Python

Syntax: `class Child(Base):`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return "hi"
```

Wenn Logik der Basisklasse aufgerufen werden muss, verwenden Sie `super()`.

**Kurz:**

- Vererbung wird in Klammern nach dem Klassennamen angegeben.
- Die abgeleitete Klasse erhält die API der Basisklasse.
- Durch Überschreiben kann Verhalten angepasst werden.

</details>

<details>
<summary>132. Wie greift man in einer abgeleiteten Klasse auf Mitglieder der Basisklasse zu?</summary>

#### Python

Der Zugriff ist direkt über geerbte Attribute und Methoden oder über `super()` möglich.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return super().greet() + " world"
```

**Kurz:**

- Geerbte Mitglieder sind in der abgeleiteten Klasse automatisch verfügbar.
- `super()` ruft die Logik der Basisklasse korrekt auf.
- Das ist wichtig, um Verhalten zu erweitern statt zu duplizieren.

</details>

<details>
<summary>133. Wofür dient die Funktion `super()` bei Vererbung in Python und wie verwendet man sie?</summary>

#### Python

`super()` gibt einen Proxy auf die nächste Klasse gemäß MRO zurück, um deren Methoden aufzurufen.
Typischerweise wird es in `__init__` und bei kooperativer Mehrfachvererbung verwendet.

```python
class Child(Base):
    def __init__(self, value: int) -> None:
        super().__init__()
        self.value = value
```

**Kurz:**

- `super()` ruft die Implementierung der Elternklasse ohne hartcodierten Klassennamen auf.
- Es hilft, Korrektheit gemäß MRO zu bewahren.
- Das ist die empfohlene Arbeitsweise bei Vererbung.

</details>

<details>
<summary>134. Beschreiben Sie die Funktion `isinstance()` in Python und geben Sie ein Beispiel für ihre Verwendung.</summary>

#### Python

`isinstance(obj, cls_or_tuple)` prüft, ob ein Objekt zu einem Typ oder dessen
Unterklasse gehört.

```python
isinstance(10, int)                 # True
isinstance(True, int)               # True
isinstance("x", (str, bytes))       # True
```

**Kurz:**

- `isinstance` ist in polymorphem Code sicherer als `type(obj) is ...`.
- Es berücksichtigt die Vererbungshierarchie.
- Es unterstützt ein Tupel von Typen.

</details>

<details>
<summary>135. Erklären Sie die Funktion `issubclass()` in Python und geben Sie ein Beispiel für ihre Anwendung.</summary>

#### Python

`issubclass(Sub, Base)` prüft, ob die Klasse `Sub` eine Unterklasse von `Base` ist.

```python
class Animal: ...
class Dog(Animal): ...

issubclass(Dog, Animal)  # True
```

**Kurz:**

- Funktioniert mit Klassen, nicht mit Instanzen.
- Ist praktisch für API-Validierung auf Typebene.
- Berücksichtigt transitive Vererbung.

</details>

<details>
<summary>136. Was ist Multiple Inheritance (Mehrfachvererbung)?</summary>

#### Python

Multiple Inheritance bedeutet, dass eine Klasse von mehreren Basisklassen erbt.

```python
class A: ...
class B: ...
class C(A, B): ...
```

Das bietet Flexibilität, erfordert aber Disziplin beim Entwurf von Methoden und beim Einsatz von `super()`.

**Kurz:**

- Eine Klasse kann Verhalten aus mehreren Quellen erben.
- Das ist nützlich für den Mixin-Ansatz.
- Es kann das Verständnis der MRO erschweren.

</details>

<details>
<summary>137. Wie funktioniert die MRO (Method Resolution Order) bei Multiple Inheritance?</summary>

#### Python

Die MRO bestimmt die Reihenfolge, in der Methoden in einer Klassenhierarchie gesucht werden.
In Python wird dafür der Algorithmus der C3-Linearisierung verwendet.

**Diamond Problem (Diamantproblem):**
Das ist der klassische Fall, in dem die Klasse `D` von `B` und `C` erbt, die beide
von `A` erben. Die MRO garantiert, dass `A` erst betrachtet wird, nachdem alle
seine Nachfolger (`B` und `C`) berücksichtigt wurden.

```python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass

print(D.mro())
# [D, B, C, A, object]
```

Die Reihenfolge kann über `ClassName.__mro__` oder `ClassName.mro()` eingesehen werden.

**Kurz:**

- Die MRO entscheidet, aus welcher Basisklasse eine Methode genommen wird.
- Die Reihenfolge ist vorhersehbar und formal definiert (C3).
- Dank der MRO verarbeitet Python das Diamantproblem korrekt.
- Für kooperative Vererbung müssen alle Klassen `super()` aufrufen.

</details>

<details>
<summary>138. Welche Vor- und Nachteile hat die Verwendung von Multiple Inheritance?</summary>

#### Python

Vorteile:

- Wiederverwendung von Verhalten aus mehreren Quellen;
- praktische Mixins zum "Hinzufügen" von Fähigkeiten.

Nachteile:

- komplexere MRO;
- Risiko von Namens- und Verhaltenskonflikten;
- schwierigeres Debugging und Onboarding.

**Kurz:**

- MI ist mächtig, erfordert aber strenge Designregeln.
- Für die meisten Fälle ist Komposition einfacher.
- Verwenden Sie MI vor allem für kleine Mixins.

</details>

<details>
<summary>139. Was sind Mixins?</summary>

#### Python

Ein Mixin ist eine kleine Klasse mit engem Zusatzverhalten, die zum Kombinieren
per Vererbung gedacht ist und nicht zur eigenständigen Verwendung.

Beispiele: `TimestampMixin`, `JsonSerializableMixin`.

**Kurz:**

- Ein Mixin ergänzt genau eine konkrete Fähigkeit.
- Es hat normalerweise keinen eigenen vollständigen Lebenszyklus.
- Es passt gut zu Mehrfachvererbung.

</details>

<details>
<summary>140. Was ist Encapsulation (Kapselung) in Python?</summary>

#### Python

Kapselung bedeutet, die interne Implementierung hinter einer stabilen öffentlichen API zu verbergen.
In Python wird das vor allem über Konventionen und `property` umgesetzt, nicht über harte Zugriffsmodifikatoren.

**Kurz:**

- Der Client-Code arbeitet mit der Schnittstelle, nicht mit Details.
- Kapselung reduziert die Kopplung zwischen Komponenten.
- Sie erleichtert Änderungen der internen Implementierung, ohne die API zu brechen.

</details>

<details>
<summary>141. Worin besteht der Unterschied zwischen public, private und protected Zugriff?</summary>

#### Python

In Python sind das größtenteils Benennungskonventionen:

- `public`: `name` — überall zugänglich;
- `protected`: `_name` — für interne Nutzung per Konvention;
- `private`: `__name` — Name Mangling (`_ClassName__name`), kein absoluter Schutz.

**Kurz:**

- Python hat keine strikten Access Modifiers wie Java oder C#.
- `_name` und `__name` sind Signale der Absicht für Entwickler.
- Echte Zugriffskontrolle entsteht durch API-Design.

</details>

<details>
<summary>142. Was ist Polymorphism (Polymorphismus) und wie wird er in Python umgesetzt?</summary>

#### Python

Polymorphismus ist die Fähigkeit, mit verschiedenen Objekten über eine gemeinsame
Schnittstelle zu arbeiten. In Python wird das oft über Duck Typing und Protokolle umgesetzt.

```python
def render(obj) -> str:
    return obj.to_text()
```

Jedes Objekt mit einer Methode `to_text` passt.

**Kurz:**

- Eine Schnittstelle, viele Implementierungen.
- In Python ist Polymorphismus oft verhaltensbasiert statt hierarchiebasiert.
- Das vereinfacht die Erweiterung eines Systems um neue Typen.

</details>

<details>
<summary>143. Was ist Abstraction (Abstraktion) in Python?</summary>

#### Python

Abstraktion bedeutet, die wesentliche API hervorzuheben und unnötige
Implementierungsdetails zu verbergen. Der Client arbeitet mit dem Vertrag, nicht mit den internen Schritten.

**Kurz:**

- Abstraktion reduziert die kognitive Last.
- Sie erleichtert den Austausch einer Implementierung ohne Änderungen im Client-Code.
- Sie wird über Interfaces, ABCs, Protokolle und Fassaden umgesetzt.

</details>

<details>
<summary>144. Wie implementiert man Data Abstraction?</summary>

#### Python

Ansatz:

- direkten Zugriff auf interne Felder (`_field`) verbergen;
- eine kontrollierte API über Methoden bzw. `@property` bereitstellen;
- Invarianten in der Setter-Logik validieren.

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

**Kurz:**

- Data Abstraction schützt die Invarianten eines Objekts.
- `property` bietet kontrollierten Zugriff auf den Zustand.
- Interne Details lassen sich ändern, ohne die API zu ändern.

</details>

<details>
<summary>145. Was sind ABC und `@abstractmethod`?</summary>

#### Python

ABC (Abstract Base Class) ist eine abstrakte Basisklasse aus dem Modul `abc`.
`@abstractmethod` markiert eine Methode, die von der Unterklasse zwingend implementiert werden muss.

```python
from abc import ABC, abstractmethod

class Storage(ABC):
    @abstractmethod
    def save(self, data: bytes) -> None:
        ...
```

**Kurz:**

- Eine ABC formalisiert den Vertrag einer Hierarchie.
- `@abstractmethod` verhindert die Instanziierung einer unvollständigen Implementierung.
- Das ist nützlich für Plugin- und erweiterbare Architekturen.

</details>

<details>
<summary>146. Was ist `property` in Python und wie wird es verwendet?</summary>

#### Python

`property` verwandelt Zugriffsmethoden in eine attributähnliche API mit der Möglichkeit
für Validierung, Berechnungen oder Lazy-Logik.

```python
class User:
    def __init__(self, name: str) -> None:
        self._name = name

    @property
    def name(self) -> str:
        return self._name
```

**Kurz:**

- `property` gibt Zugriffskontrolle, ohne die äußere Syntax zu ändern.
- Es eignet sich für Validierung und abgeleitete Werte.
- Damit kann eine API weiterentwickelt werden, ohne Clients zu brechen.

</details>

<details>
<summary>147. Was ist `@property`?</summary>

#### Python

`@property` ist ein Decorator für eine Getter-Methode.
Zusammen mit `@x.setter` und `@x.deleter` bildet er ein kontrolliertes Attribut.

**Kurz:**

- `@property` erlaubt es, eine Methode wie ein Feld zu lesen.
- Es hilft, die interne Implementierung zu kapseln.
- Es wird oft für backward-compatible APIs verwendet.

</details>

<details>
<summary>148. Was ist ein Descriptor in Python?</summary>

#### Python

Ein Descriptor ist ein Objekt, das `__get__`, `__set__` oder `__delete__`
implementiert und den Zugriff auf Attribute einer anderen Klasse steuert.

Auf Descriptoren basieren `property`, `classmethod` und `staticmethod`.

**Kurz:**

- Ein Descriptor ist ein Low-Level-Mechanismus für Attributzugriff.
- Er ermöglicht die Wiederverwendung von Validierungs- oder Proxy-Logik für Felder.
- Das ist die Grundlage vieler Metaprogrammierungstechniken in Python.

</details>

<details>
<summary>149. Worin unterscheiden sich `property` und Descriptor?</summary>

#### Python

`property` ist ein fertiger High-Level-Descriptor für ein einzelnes Attribut.
Ein eigener Descriptor ist ein allgemeinerer Mechanismus, der in vielen
Feldern und Klassen wiederverwendet werden kann.

**Kurz:**

- `property` ist einfacher und lokaler.
- Ein Descriptor ist flexibler und besser skalierbar.
- `property` ist tatsächlich auf dem Descriptor-Protokoll aufgebaut.

</details>

<details>
<summary>150. Wann sollte man besser `property` und wann einen Descriptor verwenden?</summary>

#### Python

Verwenden Sie `property`, wenn sich die Logik auf ein oder zwei Felder einer
konkreten Klasse bezieht. Verwenden Sie einen Descriptor, wenn dieselbe Logik
(Validierung, Casting, Lazy-Initialisierung) in vielen Klassen wiederverwendet werden soll.

**Kurz:**

- Lokale Feldlogik -> `property`.
- Wiederverwendung einer Zugriffspolitik -> Descriptor.
- Ein Descriptor lohnt sich in großen Domänenmodellen.

</details>

<details>
<summary>151. Wofür verwendet man `setattr()`, `getattr()` und `hasattr()`? Worin besteht der Unterschied?</summary>

#### Python

Das sind Funktionen für den dynamischen Zugriff auf Attribute:

- `getattr(obj, name[, default])` — ein Attribut lesen;
- `setattr(obj, name, value)` — ein Attribut setzen;
- `hasattr(obj, name)` — prüfen, ob ein Attribut vorhanden ist.

```python
value = getattr(user, "email", None)
if not hasattr(user, "active"):
    setattr(user, "active", True)
```

**Kurz:**

- `getattr/setattr/hasattr` werden für dynamische Arbeit mit Objekten gebraucht.
- Sie sind nützlich in generischem Code, bei Serialisierung und in Adaptern.
- Man sollte sie nicht übermäßig einsetzen, damit der Code lesbar bleibt.

</details>

<details>
<summary>152. Erklären Sie die Bedeutung der Methode `__set_name__` in Python-Deskriptoren und geben Sie ein Beispiel für ihre Anwendung.</summary>

#### Python

`__set_name__(self, owner, name)` wird beim Erstellen der Klasse aufgerufen und teilt
dem Deskriptor den Namen des Attributs mit, an das er gebunden ist.

```python
class Field:
    def __set_name__(self, owner, name): self.name = name
```

**Kurz:**

- `__set_name__` initialisiert einen Deskriptor mit dem Kontext der Klasse.
- Damit lassen sich wiederverwendbare Feldvalidatoren bauen.
- Es wird einmal bei der Klassenerstellung ausgeführt.

</details>

<details>
<summary>153. Was ist eine `dataclass` und wann sollte man sie verwenden?</summary>

#### Python

`@dataclass` generiert automatisch Boilerplate wie `__init__`, `__repr__` und `__eq__`.
Es eignet sich für Datenmodelle ohne komplexes Verhalten.

```python
from dataclasses import dataclass
@dataclass(slots=True)
class User: 
    name: str
    active: bool = True
```

**Kurz:**

- `dataclass` reduziert Code für Datenmodelle.
- Sie ist eine gute Wahl für DTOs und Konfigurationen.
- Für komplexe Validierung werden oft andere Werkzeuge benötigt.

</details>

<details>
<summary>154. Worin besteht der Unterschied zwischen `dataclass` und Pydantic?</summary>

#### Python

`dataclass` konzentriert sich auf eine bequeme Beschreibung der Struktur.
Pydantic ergänzt Runtime-Validierung, Parsing und Serialisierung von Daten.

**Kurz:**

- `dataclass` ist leichter und schneller für interne Modelle.
- Pydantic ist besser für externen Input und APIs.
- Die Wahl hängt davon ab, ob Runtime-Validierung benötigt wird.

</details>

<details>
<summary>155. Was sind Type Hints und wofür werden sie benötigt?</summary>

#### Python

Type Hints sind Typannotationen in Signaturen und Variablen, die einen expliziten Vertrag bilden.
Sie verbessern IDE-Hinweise und statische Analyse.

**Kurz:**

- Type Hints erhöhen die Verständlichkeit einer API.
- Sie ermöglichen das frühe Erkennen einer Klasse von Fehlern.
- Sie sind auch in einer dynamischen Sprache nützlich.

</details>

<details>
<summary>156. Wie funktioniert statische Typprüfung mit `mypy`?</summary>

#### Python

`mypy` liest Type Hints und analysiert Code ohne ihn auszuführen, indem es die Typkompatibilität prüft.
Es findet Integrationsfehler vor der Runtime.

**Kurz:**

- `mypy` führt eine compile-time-ähnliche Prüfung für Python aus.
- Es funktioniert am besten in CI.
- Strenge Modi reduzieren die Zahl von Produktionsfehlern.

</details>

<details>
<summary>157. Wie stellt man Type Safety in einem Python-Projekt sicher?</summary>

#### Python

- Type Hints konsequent im öffentlichen API ergänzen;
- `mypy` oder `pyright` in CI aktivieren;
- `TypedDict`, `Protocol` und Generics verwenden;
- `Any` und implizite Casts minimieren.

**Kurz:**

- Type Safety ist ein Prozess, keine einmalige Aktion.
- Den größten Effekt bringt ein CI-Gate für Typen.
- Schrittweise steigende Strenge funktioniert besser als ein Big Bang.

</details>

<details>
<summary>158. Was ist `TypedDict`?</summary>

#### Python

`TypedDict` beschreibt die typisierte Form eines Dictionaries: welche Schlüssel erwartet werden und welche Typen ihre Werte haben.

```python
from typing import TypedDict
class UserPayload(TypedDict): name: str; active: bool
```

**Kurz:**

- `TypedDict` typisiert ein `dict` mit festen Schlüsseln.
- Es ist praktisch für JSON-ähnliche Strukturen.
- Es wird durch statische Analyzer geprüft.

</details>

<details>
<summary>159. Was ist `Protocol` im Modul `typing`?</summary>

#### Python

`Protocol` beschreibt einen Verhaltensvertrag (Structural Typing): Ein Typ ist kompatibel, wenn er die erforderlichen Methoden oder Attribute besitzt, unabhängig von Vererbung.

**Kurz:**

- `Protocol` bringt Duck Typing in die statische Typisierung.
- Es reduziert die starre Kopplung an konkrete Klassen.
- Es ist nützlich für testbare und erweiterbare APIs.

</details>

<details>
<summary>160. Was sind Generics in Python?</summary>

#### Python

Generics erlauben es, Typen und Funktionen zu schreiben, die durch andere Typen parametrisiert sind.
In moderner Syntax: `class Box[T]: ...`, `def first[T](...) -> T`.

**Kurz:**

- Generics machen Typen wiederverwendbar.
- Sie stärken die Type Safety von Collections und Containern.
- Sie reduzieren die Duplizierung typisierten Codes.

</details>

<details>
<summary>161. Was ist Pydantic und wofür wird es verwendet?</summary>

#### Python

Pydantic ist eine Bibliothek zur Beschreibung von Datenschemata mit Runtime-Validierung,
Typkonvertierung und komfortabler Serialisierung.

Typische Einsatzfälle: FastAPI-Request-/Response-Modelle und Anwendungskonfiguration.

**Kurz:**

- Pydantic validiert externe Daten zur Laufzeit.
- Es ist praktisch für APIs und Integrationen.
- Es liefert klare Validierungsfehler und Schemata.

</details>

<details>
<summary>162. Was sind Exceptions in Python?</summary>

#### Python

Eine Exception ist ein Objekt, das eine fehlerhafte oder außergewöhnliche Situation
während der Codeausführung signalisiert.

**Kurz:**

- Exceptions unterbrechen den normalen Ablauf.
- Sie sollten dort behandelt werden, wo eine Entscheidung getroffen werden kann.
- Ein korrektes Fehlermodell erhöht die Zuverlässigkeit eines Systems.

</details>

<details>
<summary>163. Welche drei Arten von Fehlern gibt es in Python und worin unterscheiden sie sich?</summary>

#### Python

- Syntax Errors: Syntaxfehler vor dem Start;
- Runtime Exceptions: Fehler während der Ausführung;
- Logical Errors: Der Code läuft, aber das Ergebnis ist falsch.

**Kurz:**

- Syntax- und Runtime-Fehler erkennt der Interpreter.
- Logische Fehler werden durch Tests und Reviews gefunden.
- Jeder Fehlertyp erfordert einen anderen Diagnoseansatz.

</details>

<details>
<summary>164. Wie verwendet man `try`, `except`, `else` und `finally`?</summary>

#### Python

`try` enthält die riskante Operation, `except` behandelt den Fehler, `else` wird
ausgeführt, wenn kein Fehler aufgetreten ist, und `finally` läuft immer für Cleanup.

```python
try: data = load()
except FileNotFoundError: data = {}
else: validate(data)
finally: close_connections()
```

**Kurz:**

- `else` sollte für den Code des Erfolgswegs reserviert sein.
- `finally` dient Ressourcenfreigabe und Cleanup.
- Fangen Sie konkrete Exceptions und nicht pauschal alles ab.

</details>

<details>
<summary>165. Was bedeutet die Reihenfolge von `except`-Kategorien?</summary>

#### Python

`except`-Blöcke werden von oben nach unten geprüft. Daher stehen die spezifischsten
Exceptions zuerst und allgemeine wie `Exception` am Ende.

**Kurz:**

- Die Reihenfolge von `except` beeinflusst, welcher Handler ausgeführt wird.
- Ein zu allgemeines `except` oben verschluckt spezifische Fälle.
- Das ist kritisch für einen korrekten Recovery-Flow.

</details>

<details>
<summary>166. Wozu dient das Schlüsselwort `assert` in Python-Code?</summary>

#### Python

`assert` prüft eine Invariante und löst `AssertionError` aus, wenn die Bedingung falsch ist.
Es eignet sich für interne Entwicklerprüfungen, nicht für die Validierung von User Input.

**Kurz:**

- `assert` dokumentiert: "Das muss wahr sein".
- Es ersetzt keine produktive Fehlerbehandlung.
- Verwenden Sie es für Verträge in interner Logik.

</details>

<details>
<summary>167. Worin unterscheidet sich `raise` von einem einfachen Print einer Fehlermeldung in Python?</summary>

#### Python

`raise` verändert den Kontrollfluss und signalisiert dem Aufrufer einen Fehler.
`print` gibt nur Text aus und stoppt kein fehlerhaftes Szenario.

**Kurz:**

- `raise` ist ein Mechanismus für Fehlerbehandlung, `print` nicht.
- Exceptions lassen sich zentral abfangen und loggen.
- `print` dient Diagnosezwecken, nicht als Fehlervertrag.

</details>

<details>
<summary>168. Wie erstellt man eine eigene Exception (Custom Exception)?</summary>

#### Python

Erstellen Sie eine Klasse, die von `Exception` oder einer spezifischeren Basisausnahme erbt.

```python
class InvalidOrderError(Exception):
    pass
```

**Kurz:**

- Eine Custom Exception macht Fehler domänenspezifisch ausdrucksstark.
- Sie erlaubt das gezielte Abfangen benötigter Fälle.
- Sie ist besser als überall ein generisches `ValueError`.

</details>

<details>
<summary>169. Welche Bedeutung haben Custom Exceptions in Python und wie verbessern sie die Fehlerbehandlung?</summary>

#### Python

Eigene Exceptions bilden ein explizites Fehlermodell der Domäne und trennen technische
Fehler von Geschäftsregeln.

**Kurz:**

- Sie verbessern Lesbarkeit und Wartbarkeit von Handlern.
- Sie geben Logs und APIs präzisere Semantik.
- Sie vereinfachen das Testen negativer Szenarien.

</details>

<details>
<summary>170. Wie sind Exceptions in Python organisiert und wie sieht die Hierarchie der Exception-Klassen aus?</summary>

#### Python

Die Hierarchie ist von `BaseException` aus aufgebaut.
Im Anwendungscode arbeitet man fast immer mit Nachkommen von `Exception`.

Wichtige Zweige sind: `ValueError`, `TypeError`, `KeyError`, `OSError`, `RuntimeError`.

**Kurz:**

- Exceptions bilden einen Klassenbaum.
- Es ist besser, konkrete Unterklassen zu fangen.
- `BaseException` wird in Business-Logik normalerweise nicht abgefangen.

</details>

<details>
<summary>171. Welche Ansätze gibt es zur Behandlung mehrerer unterschiedlicher Exceptions in Python und warum sollte man sie getrennt behandeln?</summary>

#### Python

Ansätze:

- separate `except`-Blöcke für jeden Typ;
- Gruppierung logisch gleicher Fälle: `except (A, B):`;
- getrennte Recovery-Strategien für jede Kategorie.

**Kurz:**

- Unterschiedliche Exceptions erfordern oft unterschiedliche Maßnahmen.
- Getrennte Behandlung reduziert versteckte Defekte.
- Logs werden präziser und nützlicher.

</details>

<details>
<summary>172. Wozu dient das erneute Auslösen einer Exception (re-raise) in Python und wann ist das nützlich?</summary>

#### Python

Ein Re-Raise (`raise` ohne Argumente in `except`) erlaubt es, Kontext wie Logs,
Metriken oder Cleanup hinzuzufügen und denselben Fehler weiter nach oben zu geben.

**Kurz:**

- Ein Re-Raise bewahrt den ursprünglichen Traceback.
- Es ist nützlich für zentrale Behandlung auf höherer Ebene.
- Kritische Fehler sollten nicht unnötig verschluckt werden.

</details>

<details>
<summary>173. Warum sollte die Verwendung von `try-except`-Blöcken in Python-Programmen begrenzt werden und wie wirkt sich das auf die Performance aus?</summary>

#### Python

`try/except` ist notwendig, sollte aber nicht vorsorglich große Blöcke umschließen.
Besonders teuer wird es, wenn Exceptions häufig auftreten, also bei exception-driven flow.

**Kurz:**

- Fangen Sie nur erwartete Fehler an engen Stellen ab.
- Häufige Exceptions verschlechtern Performance und Lesbarkeit.
- Explizite Prüfungen sind dort besser, wo sie sinnvoll sind.

</details>

<details>
<summary>174. Wie behandelt man Fehler bei der Arbeit mit Dateien?</summary>

#### Python

Verwenden Sie `with` und fangen Sie konkrete Ausnahmen wie `FileNotFoundError`,
`PermissionError`, `UnicodeDecodeError` oder `OSError`.

```python
try:
    with open(path, "r", encoding="utf-8") as f:
        content = f.read()
except FileNotFoundError:
    ...
```

**Kurz:**

- `with` garantiert das Schließen der Datei.
- Behandeln Sie konkrete I/O-Fehler.
- Loggen Sie Kontext wie Pfad, Modus und Kodierung.

</details>

<details>
<summary>175. Welche Dateimodi gibt es in Python?</summary>

#### Python

Grundlegende Modi:

- `r` Lesen;
- `w` Überschreiben;
- `a` Anhängen am Ende;
- `x` Erstellen einer neuen Datei;
- `b` Binärmodus;
- `t` Textmodus (Standard);
- `+` Lesen und Schreiben.

**Kurz:**

- Der Modus bestimmt Sicherheits- und Änderungssemantik der Datei.
- `w` überschreibt den Inhalt, `a` bewahrt den vorhandenen.
- Für Byte-Daten verwenden Sie `b`.

</details>

<details>
<summary>176. Warum ist es wichtig, Dateien nach Operationen zu schließen, und was kann passieren, wenn eine Datei offen bleibt?</summary>

#### Python

Eine offene Datei hält einen OS-Dateideskriptor. Wenn sie nicht geschlossen wird:

- kommt es zu einem Leak von Dateideskriptoren;
- können Dateisperren oder unvollständige Flushes auftreten;
- entsteht Instabilität in lang laufenden Prozessen.

**Kurz:**

- Das Schließen einer Datei gibt OS-Ressourcen frei.
- `with` automatisiert sicheres Schließen.
- Das ist kritisch für Services und Batch-Skripte.

</details>

<details>
<summary>177. Worin besteht der Unterschied zwischen `read()`, `readline()` und `readlines()` beim Lesen von Dateien?</summary>

#### Python

- `read()` liest die ganze Datei oder `n` Bytes/Zeichen;
- `readline()` liest genau eine Zeile;
- `readlines()` liest alle Zeilen in eine Liste.

**Kurz:**

- `read()` und `readlines()` können speicherintensiv sein.
- Für große Dateien ist `for line in file` meist besser.
- Die Wahl hängt von Datenmenge und Verarbeitungsszenario ab.

</details>

<details>
<summary>178. Wie schreibt man in Python Daten in eine Datei und worin besteht der Unterschied zwischen `w` (write) und `a` (append)?</summary>

#### Python

Schreiben:

```python
with open("out.txt", "w", encoding="utf-8") as f:
    f.write("hello\n")
```

`w` überschreibt die Datei von Anfang an, `a` fügt neuen Inhalt am Ende an.

**Kurz:**

- `w` löscht alte Daten.
- `a` bewahrt den vorhandenen Inhalt.
- Für Logs verwendet man typischerweise `a`.

</details>

<details>
<summary>179. Wie arbeitet man effizient mit großen Dateien?</summary>

#### Python

- streamend lesen, also zeilenweise oder in Chunks;
- vermeiden, die gesamte Datei in den Speicher zu laden;
- Pufferung und Generatoren verwenden;
- für spalten- oder tabellenförmige Daten passende Formate und Parser wählen.

**Kurz:**

- Der Schlüssel ist Streaming statt Full Read.
- Generatoren reduzieren den Speicherverbrauch.
- Der Verarbeitungsalgorithmus ist wichtiger als Mikrooptimierungen.

</details>

<details>
<summary>180. Was sind Kontextmanager?</summary>

#### Python

Ein Kontextmanager verwaltet eine Ressource über das Protokoll `__enter__/__exit__`:
Initialisierung beim Eintritt und garantiertes Beenden bzw. Cleanup beim Austritt.

**Kurz:**

- Er bietet einen sicheren Lebenszyklus für Ressourcen.
- Er arbeitet über `with`.
- Er reduziert die Zahl von Ressourcenlecks.

</details>

<details>
<summary>181. Wie funktioniert die Konstruktion `with`?</summary>

#### Python

`with` ruft beim Eintritt in den Block `__enter__` und beim Verlassen `__exit__` auf,
selbst wenn ein Fehler auftritt.

```python
with open("data.txt", "r", encoding="utf-8") as f:
    data = f.read()
```

**Kurz:**

- `with` garantiert Cleanup.
- Es macht die Arbeit mit Ressourcen deklarativ.
- Es wird für Dateien, Locks, Transaktionen und Sessions empfohlen.

</details>

<details>
<summary>182. Wie erstellt man einen eigenen Kontextmanager?</summary>

#### Python

Es gibt zwei Ansätze:

- eine Klasse mit `__enter__`/`__exit__`;
- eine Funktion mit `contextlib.contextmanager`.

```python
from contextlib import contextmanager

@contextmanager
def temp_flag():
    yield
```

**Kurz:**

- Eine Klasse eignet sich für komplexen Zustand.
- `contextmanager` ist praktisch für kurze Szenarien.
- Beide garantieren Cleanup.

</details>

<details>
<summary>183. Wie verwaltet Python Speicher?</summary>

#### Python

CPython verwendet Reference Counting und einen zyklischen Garbage Collector.
Zusätzlich gibt es einen internen Allokator (`pymalloc`) für kleine Objekte.

**Kurz:**

- Der Basismus ist der Referenzzähler.
- Der GC entfernt zyklische Referenzen.
- Speicher wird auf OS-Ebene nicht immer sofort freigegeben.

</details>

<details>
<summary>184. Was ist Reference Counting in Python und warum ist es wichtig für die Speicherverwaltung?</summary>

#### Python

Jedes Objekt hat einen Referenzzähler. Wenn er auf null fällt, kann das Objekt
freigegeben werden. Das ermöglicht die schnelle Freigabe der meisten kurzlebigen Objekte.

**Kurz:**

- Reference Counting gibt einen vorhersehbaren Objektlebenszyklus.
- Es löst zyklische Referenzen nicht allein.
- Zusammen mit dem GC bildet es das vollständige Speichermanagementmodell.

</details>

<details>
<summary>185. Was ist Garbage Collection in Python?</summary>

#### Python

Garbage Collection in CPython findet und entfernt unerreichbare Objektzyklen,
die nicht allein durch Reference Counting bereinigt werden können.

**Kurz:**

- GC ergänzt Reference Counting.
- Er ist besonders wichtig für zyklische Referenzgraphen.
- Er kann über das Modul `gc` gesteuert werden.

</details>

<details>
<summary>186. Wie erhält man die Speicheradresse eines Objekts in Python?</summary>

#### Python

In CPython entspricht `id(obj)` häufig der Speicheradresse des Objekts als Ganzzahl.
Das ist ein Diagnosewerkzeug, kein stabiler externer Identifikator.

**Kurz:**

- `id()` liefert die Identität eines Objekts.
- In CPython ist das meist die Speicheradresse.
- Verwenden Sie das nicht für Business-Logik.

</details>

<details>
<summary>187. Wofür dient die Funktion `getrefcount()` aus dem Modul `sys` und wie funktioniert sie in Python?</summary>

#### Python

`sys.getrefcount(obj)` gibt den aktuellen Referenzzähler eines Objekts zurück
(in CPython). Der Wert ist meist um 1 höher wegen der temporären Argumentreferenz.

**Kurz:**

- Das ist ein Werkzeug zur Diagnose des Speicherverhaltens.
- Es ist nützlich für die Analyse von Referenzlecks.
- In Anwendungslogik sollte man sich nicht darauf verlassen.

</details>

<details>
<summary>188. Erklären Sie anhand von Beispielen den Unterschied zwischen mutable und immutable Objekten im Hinblick auf Reference Counting und Speicherverwaltung.</summary>

#### Python

Immutable Objekte ändern sich nicht, daher erzeugt eine "Änderung" ein neues Objekt.
Mutable Objekte werden in-place verändert, und alle Referenzen sehen die Änderung.

```python
a = "x"; b = a; a += "y"   # neues Objekt
x = [1]; y = x; y.append(2) # Änderung desselben Objekts
```

**Kurz:**

- Immutable Objekte reduzieren Seiteneffekte.
- Mutable Objekte sind effizienter für In-Place-Änderungen.
- Der Unterschied ist kritisch für Kopieren und geteilte Referenzen.

</details>

<details>
<summary>189. Worin besteht der Unterschied zwischen Shallow Copy und Deep Copy in Python und wann verwendet man welchen Ansatz?</summary>

#### Python

Eine Shallow Copy kopiert nur den äußeren Container, verschachtelte Objekte bleiben gemeinsam.
Eine Deep Copy kopiert die gesamte Struktur rekursiv.

```python
import copy
copy.copy(obj)
copy.deepcopy(obj)
```

**Kurz:**

- Eine Shallow Copy reicht für flache Strukturen.
- Eine Deep Copy ist nötig für isoliertes Arbeiten mit verschachtelten mutable Daten.
- Eine Deep Copy ist teurer in Zeit und Speicher.

</details>

<details>
<summary>190. Was sind Modules und Packages in Python?</summary>

#### Python

Ein Module ist eine einzelne `.py`-Datei mit Code.
Ein Package ist ein Verzeichnis von Modulen, also ein Namensraum zur Organisation größeren Codes.

**Kurz:**

- Module = eine Codeeinheit.
- Package = Struktur zur Skalierung von Modulen.
- Die Aufteilung in Module und Packages verbessert die Wartbarkeit.

</details>

<details>
<summary>191. Wie importiert man ein Module in Python?</summary>

#### Python

Grundlegende Formen:

- `import module`;
- `import module as m`;
- `from module import name`;
- `from package import submodule`.

**Kurz:**

- Ein Import lädt ein Modul und macht es im Namespace verfügbar.
- Ein Alias (`as`) verbessert Lesbarkeit und vermeidet Konflikte.
- Bevorzugen Sie explizite Importe.

</details>

<details>
<summary>192. Welche Arten von Imports gibt es?</summary>

#### Python

Gängige Arten:

- absolute;
- relative;
- selektive (`from x import y`);
- Alias-Importe (`as`);
- dynamische (`importlib`).

**Kurz:**

- Die Importart beeinflusst Lesbarkeit und Wartbarkeit.
- In Produktion verwendet man meist absolute Importe.
- Dynamische Importe sollten gezielt eingesetzt werden.

</details>

<details>
<summary>193. Wie funktioniert das Importsystem?</summary>

#### Python

Der Interpreter sucht ein Modul über `sys.path`, lädt es einmal und cached es in
`sys.modules`. Ein erneuter Import verwendet den Cache.

**Kurz:**

- Import = Suche + Ausführung des Moduls + Caching.
- Das erklärt, warum Modulcode beim ersten Import ausgeführt wird.
- Zyklische Importe entstehen durch die Reihenfolge der Modulinitialisierung.

</details>

<details>
<summary>194. Worin besteht der Unterschied zwischen absolutem und relativem Import?</summary>

#### Python

Ein absoluter Import beginnt am Package-Root (`from app.utils import x`).
Ein relativer Import verwendet Punkte (`from .utils import x`).

**Kurz:**

- Absolute Importe sind lesbarer und stabiler.
- Relative sind innerhalb eines Packages praktisch, aber schlechter für Refactoring.
- In großen Projekten sollte man standardmäßig absolute Importe bevorzugen.

</details>

<details>
<summary>195. Was macht die Funktion `dir()` und wie kann man sie auf Module anwenden?</summary>

#### Python

`dir(obj)` gibt eine Liste verfügbarer Attribute bzw. Namen eines Objekts zurück.
Bei Modulen ist das ein schneller Weg, das API anzusehen.

```python
import math
dir(math)
```

**Kurz:**

- `dir()` hilft bei der interaktiven Untersuchung von Modulen.
- Es ist nützlich im REPL und beim Debugging.
- Es ersetzt keine offizielle Dokumentation.

</details>

<details>
<summary>196. Erklären Sie die Rolle der Konstruktion `if __name__ == "__main__":` in Python-Skripten.</summary>

#### Python

Dieser Block wird nur ausgeführt, wenn die Datei als Skript gestartet und nicht als
Modul importiert wird. Dadurch werden wiederverwendbarer Code und CLI-Entrypoint getrennt.

**Kurz:**

- Er erlaubt, ein Modul sowohl zu starten als auch zu importieren.
- Er verhindert unerwünschte Ausführung beim Import.
- Das ist ein Standardmuster für Skripte.

</details>

<details>
<summary>197. Was bedeutet die Datei `__init__.py` in einem Python-Package?</summary>

#### Python

`__init__.py` markiert ein Verzeichnis als Package und kann das Package-Level-API initialisieren,
zum Beispiel durch Re-Export von Klassen oder Funktionen.

**Kurz:**

- Es formt die öffentliche Schnittstelle des Packages.
- Es kann minimale Initialisierung enthalten.
- Man sollte es nicht mit schwerer Logik überladen.

</details>

<details>
<summary>198. Welche Best Practices gibt es für den Importstil in Python-Code?</summary>

#### Python

- Importe gruppieren: Stdlib, Third-Party, lokal;
- `from x import *` vermeiden;
- Importe am Dateianfang halten, außer bei begründeten Lazy-Import-Fällen;
- Sortierung und Formatierung mit Tools wie `ruff` oder `isort` verwenden.

**Kurz:**

- Konsistente Importe verbessern die Lesbarkeit.
- Explizite Importe reduzieren Namenskonflikte.
- Tooling-Automatisierung eliminiert manuelle Fehler.

</details>

<details>
<summary>199. Welche populären Standardmodule gibt es in Python?</summary>

#### Python

Beispiele populärer Module aus der Standardbibliothek:

- `os`, `sys`, `pathlib`, `json`, `datetime`, `re`,
- `collections`, `itertools`, `functools`, `typing`,
- `asyncio`, `subprocess`, `logging`, `argparse`.

**Kurz:**

- Die Standardbibliothek deckt die meisten grundlegenden Aufgaben ab.
- Das reduziert die Zahl externer Abhängigkeiten.
- Man sollte die Standardbibliothek gut kennen, bevor man Fremdpakete hinzufügt.

</details>
<details>
<summary>200. Was wissen Sie über das Paket `collections` und welche weiteren Standardmodule wurden verwendet?</summary>

#### Python

`collections` bietet höherwertige Datenstrukturen:

- `Counter`, `defaultdict`, `deque`, `namedtuple`, `ChainMap`.

Typischerweise wird es kombiniert mit:

- `itertools` für Iterations-Pipelines;
- `functools` für Caching und funktionale Hilfsmittel;
- `pathlib`, `json`, `datetime` in Anwendungsaufgaben.

**Kurz:**

- `collections` erweitert die Basiskontainer um praktische Strukturen.
- Es erhöht oft Einfachheit und Performance des Codes.
- Es arbeitet gut zusammen mit `itertools` und `functools`.

</details>

<details>
<summary>201. Was gibt `sys.argv` zurück?</summary>

#### Python

`sys.argv` gibt eine Liste von Kommandozeilenargumenten zurück:

- `sys.argv[0]` — der Name des Skripts;
- die übrigen Elemente — die übergebenen Argumente.

**Kurz:**

- `sys.argv` ist die grundlegende Schnittstelle für CLI-Argumente.
- Die Werte kommen als Strings an.
- Für komplexe CLI ist `argparse` besser.

</details>

<details>
<summary>202. Welches ist das Hauptmodul für die Arbeit mit dem Betriebssystem in Python?</summary>

#### Python

Das Hauptmodul ist `os` zusammen mit `os.path`, und für ein modernes Pfad-API
wird `pathlib` empfohlen.

**Kurz:**

- `os` bietet Zugriff auf Process-, Env- und Filesystem-APIs des Betriebssystems.
- `pathlib` ist bequemer für die Arbeit mit Pfaden.
- In realen Projekten verwendet man oft beide.

</details>

<details>
<summary>203. Wie mischt man Listenelemente mit dem Modul `random`?</summary>

#### Python

Verwenden Sie `random.shuffle(list_)` für ein In-Place-Mischen.

```python
import random
items = [1, 2, 3, 4]
random.shuffle(items)
```

**Kurz:**

- `shuffle` verändert die Originalliste.
- Es funktioniert nur mit mutablen Sequenzen, zum Beispiel Listen.
- Für eine neue Kopie: `random.sample(items, k=len(items))`.

</details>

<details>
<summary>204. Was ist eine Virtual Environment?</summary>

#### Python

Eine Virtual Environment ist eine isolierte Python-Umgebung mit eigenen Paketen
und Versionsständen der Abhängigkeiten für ein konkretes Projekt.

**Kurz:**

- Isolation beseitigt Abhängigkeitskonflikte zwischen Projekten.
- Das Standardwerkzeug ist `venv`.
- Das ist eine grundlegende Praxis für reproduzierbare Entwicklung.

</details>

<details>
<summary>205. Wie funktioniert `pip`?</summary>

#### Python

`pip` installiert, aktualisiert und entfernt Pakete aus Paketindizes, meist PyPI,
löst Abhängigkeiten auf und installiert sie in die aktuelle Umgebung.

**Kurz:**

- `pip` ist der Standard-Paketmanager für Python.
- Er arbeitet innerhalb des aktiven venv bzw. Interpreters.
- Für Stabilität sind gepinnte Versionen wichtig.

</details>

<details>
<summary>206. Was ist `requirements.txt`?</summary>

#### Python

`requirements.txt` ist eine Datei mit einer Liste von Abhängigkeiten, oft mit exakten Versionen,
die für reproduzierbare Installationen verwendet wird.

**Kurz:**

- Das Format ist einfach und kompatibel mit `pip install -r`.
- Für Produktion sollten Versionen möglichst exakt fixiert werden.
- Die Datei wird oft durch Tools wie `pip-tools` oder `poetry export` aus deklarativen Listen oder Lockfiles erzeugt.

</details>

<details>
<summary>207. Was ist `pyproject.toml` und warum ist es zum Standard geworden?</summary>

#### Python

`pyproject.toml` ist die standardisierte Projektkonfigurationsdatei: Paket-Metadaten,
Build-System und Tool-Konfigurationen wie `ruff`, `pytest` oder `mypy`.

**Kurz:**

- Sie zentralisiert die Konfiguration eines Python-Projekts.
- Sie wird von modernem Packaging-Tooling unterstützt.
- Sie reduziert die Anzahl verstreuter Konfigurationsdateien.

</details>

<details>
<summary>208. Wie verwaltet man Abhängigkeiten in einem modernen Python-Projekt?</summary>

#### Python

- die Umgebung isolieren (`venv`);
- Abhängigkeiten in `pyproject.toml` definieren;
- Lockfiles bzw. Constraints für Reproduzierbarkeit festhalten;
- regelmäßig mit CI-Prüfungen aktualisieren.

**Kurz:**

- Abhängigkeitsmanagement muss reproduzierbar sein.
- Globale und projektspezifische Pakete sollten nicht vermischt werden.
- Updates sollten kontrolliert über Tests erfolgen.

</details>

<details>
<summary>209. Wie organisiert man die Struktur eines großen Python-Projekts sinnvoll?</summary>

#### Python

- den Code in domänenspezifische Packages aufteilen;
- separate Schichten wie `api`, `services`, `domain`, `infrastructure` haben;
- `tests/`, `scripts/` und `configs/` getrennt halten;
- klare Modulgrenzen und ein explizites öffentliches API definieren.

**Kurz:**

- Die Struktur sollte die Domäne widerspiegeln, nicht zufällige technische Details.
- Klare Grenzen reduzieren zyklische Abhängigkeiten.
- Tests und Tooling sollten ein First-Class-Bestandteil des Projekts sein.

</details>

<details>
<summary>210. Worin besteht der Unterschied zwischen automatisiertem und manuellem Testen und welche Vorteile hat automatisiertes Testen?</summary>

#### Python

Manuelles Testen wird von einer Person Schritt für Schritt durchgeführt.
Automatisiertes Testen wird durch Skripte oder Frameworks ausgeführt.

**Kurz:**

- Automatisierte Tests sind schnell, wiederholbar und für CI geeignet.
- Manuelles Testen ist nützlich für explorative UX-Szenarien.
- In der Praxis braucht man eine Kombination beider Ansätze.

</details>

<details>
<summary>211. Was ist TDD (Test-Driven Development)?</summary>

#### Python

TDD ist ein Zyklus: einen fehlschlagenden Test schreiben -> minimale Implementierung -> Refactoring.

**Kurz:**

- TDD formt das API über Tests.
- Es gibt schnelles Feedback zu Regressionen.
- Es funktioniert am besten für modulare Geschäftslogik.

</details>

<details>
<summary>212. Welche populären Test-Frameworks gibt es in Python?</summary>

#### Python

Am populärsten sind `pytest`, `unittest` aus der Stdlib sowie `hypothesis`
für Property-Based-Tests.

**Kurz:**

- `pytest` wird für neue Projekte am häufigsten gewählt.
- `unittest` ist als Standard-Basiswerkzeug nützlich.
- `hypothesis` stärkt die Abdeckung von Edge Cases.

</details>

<details>
<summary>213. Was ist `unittest` in Python?</summary>

#### Python

`unittest` ist das eingebaute xUnit-Framework für Tests: Test-Case-Klassen,
Assert-Methoden, Setup/Teardown und Test Runner.

**Kurz:**

- Es ist Teil der Standardbibliothek.
- Es eignet sich für konservative Umgebungen ohne externe Abhängigkeiten.
- Seine Syntax ist zeremonieller als die von `pytest`.

</details>

<details>
<summary>214. Was ist `pytest` und worin unterscheidet es sich syntaktisch und funktional von `unittest`?</summary>

#### Python

`pytest` ist ein Framework mit einfacher Syntax für funktionale Tests, mächtigen
Fixtures, Parametrisierung und einem Plugin-Ökosystem.

**Kurz:**

- `pytest` ist weniger boilerplate-lastig und bequemer für große Test-Suiten.
- `unittest` ist klassenbasiert und Teil der Stdlib.
- In modernen Projekten dominiert meist `pytest`.

</details>

<details>
<summary>215. Beschreiben Sie, wie `pytest.raises` verwendet wird, um das Auftreten bestimmter Exceptions in Python-Code zu testen.</summary>

#### Python

`pytest.raises(ExpectedError)` prüft, dass ein Codeblock genau die erwartete
Exception auslöst.

```python
import pytest
with pytest.raises(ValueError):
    int("abc")
```

**Kurz:**

- Es testet negative Szenarien explizit.
- Es schützt davor, dass Fehler stillschweigend durchrutschen.
- Es kann auch Nachricht oder Attribute der Exception prüfen.

</details>

<details>
<summary>216. Was ist Parametrisierung in Tests und wie unterstützt pytest sie über `@pytest.mark.parametrize`?</summary>

#### Python

Parametrisierung führt einen Test mit mehreren Eingabedatensätzen aus.
In pytest erfolgt das mit dem Decorator `@pytest.mark.parametrize`.

**Kurz:**

- Weniger Duplizierung von Testcode.
- Testfälle lassen sich leicht skalieren.
- Die Abdeckung von Eingabeszenarien wird transparenter.

</details>

<details>
<summary>217. Wie kann man in pytest eigene Testnamen für parametrisierte Tests vergeben, um die Lesbarkeit zu verbessern?</summary>

#### Python

Verwenden Sie den Parameter `ids` in `parametrize`.

```python
@pytest.mark.parametrize("value,expected", [(2, True), (3, False)], ids=["even", "odd"])
```

**Kurz:**

- `ids` macht die Ausgabe des Test-Runs verständlicher.
- Das erleichtert die Diagnose von Fehlschlägen.
- Besonders nützlich bei vielen Testfällen.

</details>

<details>
<summary>218. Was ist Arrange/Setup im Testen und warum ist das wichtig?</summary>

#### Python

Arrange/Setup ist die Vorbereitung des Testzustands: Daten, Objekte, Mocks und Umgebung.
Ein gutes Setup macht einen Test deterministisch.

**Kurz:**

- Instabiles Setup bedeutet flaky Tests.
- Ein gutes Setup isoliert den Test von äußeren Effekten.
- Ein klares Arrange verbessert die Lesbarkeit des Szenarios.

</details>

<details>
<summary>219. Welche Schritte umfasst Cleanup/Teardown und warum ist das wichtig?</summary>

#### Python

Teardown räumt alles auf, was der Test erzeugt hat: temporäre Dateien, Verbindungen,
Mocks und Testeinträge in der Datenbank.

**Kurz:**

- Cleanup sorgt für Isolation zwischen Tests.
- Es reduziert Seiteneffekte und Flakiness.
- In pytest lässt sich das bequem über Fixture-Finalizer oder Yield-Fixtures machen.

</details>

<details>
<summary>220. Worin besteht der Unterschied zwischen `setUp()` und `setUpClass()` in `unittest`?</summary>

#### Python

`setUp()` wird vor **jeder** Testmethode ausgeführt.
`setUpClass()` als Classmethod wird **einmal** vor allen Tests der Klasse ausgeführt.

**Kurz:**

- `setUp` dient der Isolation pro Test.
- `setUpClass` ist für teure gemeinsame Ressourcen gedacht.
- Zu viel gemeinsamer Zustand über `setUpClass` kann Tests erschweren.

</details>

<details>
<summary>221. Was ist ein Mock-Objekt und wie hilft es, die Qualität von Tests zu verbessern?</summary>

#### Python

Ein Mock-Objekt ist ein Ersatzobjekt, das eine Abhängigkeit imitiert und es erlaubt,
Verhalten zu kontrollieren bzw. Aufrufe zu prüfen.

**Kurz:**

- Mocks isolieren die Unit von externen Diensten.
- Sie machen Tests schneller und stabiler.
- Sie erlauben die Prüfung von Interaktionen, nicht nur des Ergebnisses.

</details>

<details>
<summary>222. Worin besteht der Unterschied zwischen `mock.patch` in unittest und `monkeypatch` in pytest beim Mocken von Objekten?</summary>

#### Python

`mock.patch` aus `unittest.mock` patcht Objekte über ihren Importpfad und bietet
ein reichhaltiges API zur Prüfung von Aufrufen.
`monkeypatch` in pytest ändert einfacher Attribute, Environment-Variablen oder Dicts für die Dauer des Tests.

**Kurz:**

- `patch` ist mächtiger für Mock-Assertion-Szenarien.
- `monkeypatch` ist praktisch für schnelle Test-Ersetzungen.
- Je nach Fall werden beide oft kombiniert.

</details>

<details>
<summary>223. Wozu dient der Parameter `scope` in pytest-Fixtures?</summary>

#### Python

`scope` definiert den Lebenszyklus einer Fixture: `function`, `class`, `module`,
`package`, `session`.

**Kurz:**

- Ein kleinerer Gültigkeitsbereich bedeutet bessere Isolation.
- Ein größerer Gültigkeitsbereich beschleunigt große Test-Suiten.
- Die Wahl des Gültigkeitsbereichs ist ein Gleichgewicht zwischen Geschwindigkeit und Unabhängigkeit.

</details>

<details>
<summary>224. Was ist algorithmische Komplexität und wie wird sie bestimmt?</summary>

#### Python

Die Komplexität eines Algorithmus bewertet, wie Zeit- und Speicheraufwand mit
wachsender Größe der Eingabedaten `n` zunehmen.

**Kurz:**

- Man misst Zeit- und Speicherkomplexität.
- Die Bewertung ist meist asymptotisch.
- Das hilft bei der Wahl von Algorithmen und Datenstrukturen.

</details>

<details>
<summary>225. Erklären Sie das Konzept der Big-O-Notation und ihre Bedeutung für die Bewertung algorithmischer Komplexität.</summary>

#### Python

Big O beschreibt die obere Schranke des Wachstums der Kosten eines Algorithmus bei großem `n`
und ignoriert Konstanten sowie Terme niedriger Ordnung.

**Kurz:**

- Big O zeigt Skalierbarkeit, nicht exakte Laufzeit.
- Es liefert eine Sprache zum Vergleich von Algorithmen.
- Für Performance bei großen Datenmengen ist es kritisch wichtig.

</details>

<details>
<summary>226. Welche Arten algorithmischer Komplexität kommen am häufigsten vor?</summary>

#### Python

Am häufigsten sind `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`, `O(n^2)`.

**Kurz:**

- `O(n)` und `O(n log n)` sind in Anwendungsaufgaben am typischsten.
- `O(n^2)` und mehr werden oft zum Bottleneck.
- Man muss auch Speicher und nicht nur Zeit berücksichtigen.

</details>

<details>
<summary>227. Nennen Sie Beispiele für Aufgaben, die effizient mit linearen Algorithmen (O(n)) gelöst werden.</summary>

#### Python

Beispiele:

- Suche nach Maximum/Minimum;
- Filtern von Elementen;
- Häufigkeitszählung mit `Counter`;
- Prüfung von Bedingungen für jedes Element.

**Kurz:**

- O(n) bedeutet einen Durchlauf durch die Daten.
- Das ist für viele Aggregationen optimal.
- Lineare Algorithmen skalieren gut.

</details>

<details>
<summary>228. Wie funktioniert `lru_cache` und wann sollte man es verwenden?</summary>

#### Python

`functools.lru_cache` cached Funktionsergebnisse anhand der Argumente und gibt bei
wiederholten Aufrufen den fertigen Wert zurück.

**Kurz:**

- Es ist effektiv für pure Funktionen mit wiederholten Eingabedaten.
- Für Funktionen mit Side Effects ist es ungeeignet.
- `maxsize` steuert die Größe des Caches im Speicher.

</details>

<details>
<summary>229. Wie profiliert man die Performance von Python-Code?</summary>

#### Python

Grundlegende Werkzeuge:

- `timeit` für Mikromessungen;
- `cProfile`/`pstats` für Profile auf Call-Ebene;
- `py-spy`/`scalene` für produktionsnahe Analyse.

**Kurz:**

- Optimieren Sie erst nach Messungen.
- Profilieren Sie realistische Lastszenarien.
- Halten Sie Baselines vor und nach Änderungen fest.

</details>

<details>
<summary>230. Welche grundlegenden Wege gibt es, Python-Code zu optimieren?</summary>

#### Python

- die richtigen Datenstrukturen wählen;
- die asymptotische Komplexität verringern;
- unnötige Kopien vermeiden;
- Generatoren bzw. Lazy Pipelines nutzen;
- teure Berechnungen cachen;
- Hot Paths bei Bedarf nach C, Rust oder NumPy auslagern.

**Kurz:**

- Den größten Gewinn bringt der Algorithmus, nicht ein syntaktischer Tweak.
- Optimierung muss sich auf Profiling stützen.
- Lesbarkeit sollte man nicht ohne gemessenen Nutzen opfern.

</details>

<details>
<summary>231. Wann sollte man C-Extensions oder PyPy verwenden?</summary>

#### Python

C-Extensions sind sinnvoll für enge CPU-Hotspots und die Integration mit nativen
Bibliotheken. PyPy ist sinnvoll, wenn langlebiger Pure-Python-Code von JIT profitiert.

**Kurz:**

- C-Extension: maximale Performance zum Preis höherer Build-Komplexität.
- PyPy: potenzieller Gewinn ohne Umschreiben nach C.
- Die Wahl sollte auf Benchmarks Ihrer Workload basieren.

</details>

<details>
<summary>232. Was ist Memory Profiling?</summary>

#### Python

Memory Profiling misst, wo und wie viel Speicher ein Code im Zeitverlauf verbraucht,
um Leaks und schwere Abschnitte zu finden.

**Kurz:**

- Es zeigt Memory Hot Spots und Peaks.
- Es ist nützlich für Batch- und Daten-Workloads.
- Werkzeuge: `tracemalloc`, `memory_profiler`, `scalene`.

</details>

<details>
<summary>233. Was ist der GIL (Global Interpreter Lock)?</summary>

#### Python

Der GIL ist ein Mechanismus in CPython, der nur einem Thread gleichzeitig erlaubt,
Python-Bytecode innerhalb eines Prozesses auszuführen.

**Kurz:**

- Der GIL beeinflusst CPU-bound Multithreading.
- Für I/O-bound Aufgaben bleiben Threads nützlich.
- Für CPU-Parallelismus nutzt man häufiger Multiprocessing.

</details>

<details>
<summary>234. Wie beeinflusst der Global Interpreter Lock (GIL) die Concurrency in CPython und welche Folgen hat das für Multithreading?</summary>

#### Python

Wegen des GIL führen Threads in CPython Python-Bytecode bei CPU-bound Code nicht
wirklich parallel aus. Sie wechseln kooperativ zwischen einander.

Folgen:

- für I/O-bound Threads ist der Effekt gut, weil I/O-Wartezeiten überlappt werden;
- für CPU-bound Aufgaben ist der Gewinn durch Threads meist begrenzt.

**Kurz:**

- Der GIL begrenzt den Parallelismus von Threads in CPU-bound Szenarien.
- Threads bleiben für Netzwerk und Festplatte nützlich.
- Für CPU-intensive Arbeit verwenden Sie Prozesse oder native Berechnungen.

</details>

<details>
<summary>235. Wie beeinflusst der GIL die Performance?</summary>

#### Python

Der GIL stört bei I/O-bound Aufgaben kaum, begrenzt aber den Throughput von
CPU-bound multithreaded Python-Code innerhalb eines Prozesses.

**Kurz:**

- Die Wirkung des GIL hängt von der Art der Last ab.
- CPU-bound plus Threads skaliert in CPython oft nicht.
- Die Architektur sollte nach dem Aufgabenprofil gewählt werden.

</details>

<details>
<summary>236. Erklären Sie das Konzept von Threading in Python und wie es sich von Multiprocessing unterscheidet.</summary>

#### Python

`threading` startet mehrere Threads in einem Prozess mit gemeinsamem Speicher.
`multiprocessing` startet separate Prozesse mit getrenntem Speicher.

**Kurz:**

- Threads sind leichter und praktisch für I/O-bound Aufgaben.
- Prozesse liefern echten CPU-Parallelismus.
- Prozesse haben höhere Overheads für IPC und Erstellung.

</details>

<details>
<summary>237. Wann sollte man Multiprocessing statt Threading verwenden?</summary>

#### Python

Wenn eine Aufgabe CPU-bound ist und mehrere Kerne in CPython nutzen soll.
Beispiele: schweres Parsing, Bild- und Videoverarbeitung, numerische Berechnungen.

**Kurz:**

- CPU-bound -> meist `multiprocessing`.
- I/O-bound -> meist `threading` oder `asyncio`.
- Berücksichtigen Sie die Kosten der Serialisierung zwischen Prozessen.

</details>

<details>
<summary>238. Worin besteht der Unterschied zwischen Concurrency und Parallelism in der Programmierung, und wann sollte man welches einsetzen?</summary>

#### Python

Concurrency bedeutet Überlappung von Aufgaben in der Zeit.
Parallelism bedeutet tatsächliche gleichzeitige Ausführung auf mehreren Kernen.

**Kurz:**

- Concurrency ist nützlich bei I/O-Wartezeiten.
- Parallelism ist nötig für CPU-intensive Berechnungen.
- In Python hängt die Werkzeugwahl vom Typ des Bottlenecks ab.

</details>

<details>
<summary>239. Was ist Concurrency in Python?</summary>

#### Python

Concurrency in Python ist die Organisation der Ausführung mehrerer Aufgaben so,
dass sie gemeinsam Fortschritt machen: über Threads, asyncio oder Prozesse.

**Kurz:**

- Es geht um das Management vieler Aufgaben, nicht zwingend parallel.
- Es kann den Throughput von I/O-Szenarien erhöhen.
- Es erfordert sauberes Design für Synchronisation und Cancellation.

</details>

<details>
<summary>240. Worin besteht der Unterschied zwischen IO-bound und CPU-bound Aufgaben?</summary>

#### Python

IO-bound Aufgaben warten überwiegend auf Netzwerk, Festplatte oder Datenbank.
CPU-bound Aufgaben verbringen die meiste Zeit mit Prozessorberechnungen.

**Kurz:**

- IO-bound skaliert gut über asyncio oder Threads.
- CPU-bound skaliert besser über Multiprocessing oder nativen Code.
- Bestimmen Sie zuerst das Bottleneck durch Profiling.

</details>

<details>
<summary>241. Wofür wird das Modul `asyncio` in Python benötigt und wie ermöglicht es asynchrone Programmierung?</summary>

#### Python

`asyncio` bietet Ereignisschleife, Aufgabenplanung und asynchrone Primitive für kooperative
Nebenläufigkeit in I/O-gebundenen Aufgaben.

**Kurz:**

- Es erlaubt die effiziente Bedienung vieler I/O-Operationen.
- Es basiert auf `async`/`await`.
- Es eignet sich gut für Netzwerkdienste und Clients.

</details>

<details>
<summary>242. Worin unterscheiden sich synchrone und asynchrone Programmierung in Python?</summary>

#### Python

Synchron: Ein Aufruf blockiert den aktuellen Thread bis zum Abschluss.
Asynchron: `await` gibt die Kontrolle an den Event Loop zurück, während die Operation auf I/O wartet.

**Kurz:**

- Async reduziert Leerlaufzeit bei I/O.
- Sync ist einfacher für lineare Logik.
- Async erhöht die Komplexität von Task-Steuerung und Cancellation.

</details>

<details>
<summary>243. Was ist `async`/`await`?</summary>

#### Python

`async def` definiert eine Coroutine-Funktion.
`await` pausiert eine Coroutine bis ein Awaitable bereit ist und gibt die Kontrolle an den Loop zurück.

**Kurz:**

- Das ist die Syntax des asynchronen kooperativen Modells.
- Sie wird zusammen mit `asyncio` und Async-Bibliotheken verwendet.
- `await` ist nur innerhalb von `async def` möglich.

</details>

<details>
<summary>244. Wie funktioniert `asyncio`?</summary>

#### Python

`asyncio` startet einen Event Loop, der Tasks bzw. Coroutines ausführt, an
`await`-Stellen umschaltet und bereite I/O-Operationen plant.

**Kritische Regel:**
Die Ereignisschleife läuft in einem einzigen Thread.
Jede blockierende Operation (`time.sleep()`, synchrone
`requests`-Aufrufe, schwere Berechnungen) stoppt den **gesamten** Loop
und alle anderen Tasks.

**Kurz:**

- Ein Thread kann über Kooperativität viele I/O-Aufgaben bedienen.
- Das Scheduling ist nicht präemptiv.
- Blockierende Aufrufe ruinieren die Performance von asyncio.

</details>

<details>
<summary>245. Was ist ein Event Loop?</summary>

#### Python

Eine Ereignisschleife ist ein Scheduler, der Ereignisse bzw. I/O-Bereitschaft verfolgt und
passende Callbacks oder Coroutines startet.

**Kurz:**

- Er ist die zentrale Komponente des asyncio-Modells.
- Er steuert den Lebenszyklus asynchroner Tasks.
- Er bestimmt, wann welche Coroutine weiterläuft.

</details>

<details>
<summary>246. Wie ermöglicht `asyncio` asynchrone Programmierung und welche Hauptkomponenten sind in asyncio-Code beteiligt?</summary>

#### Python

Wichtige Komponenten:

- Ereignisschleife;
- Coroutine (`async def`);
- Task (`asyncio.create_task`);
- Awaitables (Futures, Tasks, Coroutines);
- Synchronisationsprimitive (`Lock`, `Queue`, `Semaphore`).

**Kurz:**

- `asyncio` verbindet Scheduling und Async API in einem Modell.
- Tasks teilen sich kooperativ einen Ausführungsthread.
- Die Architektur muss Timeouts, Wiederholungen und Abbrüche berücksichtigen.

</details>

<details>
<summary>247. Wann bringt `asyncio` keine Vorteile?</summary>

#### Python

Wenn die Last CPU-gebunden ist oder die verwendeten Hauptbibliotheken blockieren und kein Async-API haben.
Außerdem lohnt es sich nicht für einfache kurze Skripte.

**Lösung für blockierenden Code:**
Wenn eine blockierende Bibliothek in einer Async-Umgebung verwendet werden muss,
nutzen Sie `loop.run_in_executor(None, sync_func)`.
Damit läuft sie in einem separaten Thread, ohne den Event Loop zu blockieren.

**Kurz:**

- Async beschleunigt keine reinen Berechnungen.
- Ohne nicht blockierende I/O-Bibliotheken ist der Nutzen minimal.
- `run_in_executor` hilft bei der Integration von Legacy- bzw. Sync-Code.
- Die Komplexität von Async muss durch die Last gerechtfertigt sein.

</details>

<details>
<summary>248. Wie funktioniert asyncio Cancellation?</summary>

#### Python

Das Abbrechen eines Tasks (`task.cancel()`) löst `CancelledError` in der Coroutine aus.
Der Code muss Cleanup korrekt in `try/finally` behandeln.

**Kurz:**

- Cancellation ist normaler Control Flow in Async-Code.
- Die Behandlung von Abbrüchen muss im Coroutine-Design eingeplant werden.
- Ignorierte Cancellation führt zu hängenden Tasks.

</details>

<details>
<summary>249. Was ist `contextvars`?</summary>

#### Python

`contextvars` liefert context-lokale Variablen, die für Async- und Thread-Szenarien sicher sind.
Das ist nützlich für Request-ID, Correlation-ID und Tenant-Kontext.

**Kurz:**

- Es ist eine Alternative zu globalem State in konkurrierendem Code.
- Der Wert ist pro Kontext isoliert.
- Es verbessert Tracing und Observability.

</details>

<details>
<summary>250. Welche Best Practices sollte man beim Schreiben von Python-Code anwenden?</summary>

#### Python

- PEP 8 einhalten und Formatierung automatisieren;
- explizite Type Hints für das öffentliche API schreiben;
- `with` für Ressourcen verwenden;
- Geschäftslogik mit Tests abdecken;
- vorzeitige Optimierung vermeiden und stattdessen profilieren;
- Module klein mit klarer Verantwortung halten;
- Abhängigkeiten über `pyproject.toml` plus Lock-Strategie verwalten.

**Kurz:**

- Lesbarkeit und Vorhersehbarkeit sind wichtiger als "Tricks".
- Qualität beruht auf Automatisierung: Lint, Types, Tests, CI.
- Architektonische Einfachheit senkt die Wartungskosten.

</details>
