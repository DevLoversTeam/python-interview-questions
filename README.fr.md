**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

# Python <img src="./assets/python.svg" width="40" height="40" alt="Python logo"/>

## Les questions et réponses les plus populaires d'entretien sur Python

<details>
<summary>1. Qu'est-ce que Python et quelles sont ses principales caractéristiques ?</summary>

#### Python

**Python** est un langage de haut niveau et à usage général, centré sur la
lisibilité, la rapidité de développement et une vaste bibliothèque standard.

Principales caractéristiques :

- **Syntaxe simple** : le code est facile à lire et à maintenir.
- **Modèle d'exécution interprété** : cycle de modification rapide sans étape de
  compilation manuelle.
- **Multiplateforme** : le même code fonctionne sur Linux, macOS et Windows.
- **Multiparadigme** : approches procédurale, POO et fonctionnelle dans un même
  projet.
- **Écosystème solide** : `pip`, `venv`, `pyproject.toml` et des milliers de
  bibliothèques prêtes à l'emploi.
- **Fonctionnalités modernes de Python 3.10+** : annotations de types, `dataclass`,
  `async/await`, `match/case`, générateurs et gestionnaires de contexte.

Exemple de fonction au style production :

```python
from dataclasses import dataclass

@dataclass(slots=True)
class User:
    name: str
    active: bool

def process_users(users: list[User]) -> list[str]:
    return [user.name for user in users if user.active]
```

**En bref :**

- Python accélère le développement grâce à sa syntaxe simple et à sa vaste
  bibliothèque standard.
- Le langage convient au back-end, à l'automatisation, aux données/ML, aux tests et au DevOps.
- En Python 3.10+, les pratiques clés sont les annotations de types, l'I/O asynchrone et une bibliothèque standard moderne.

</details>

<details>
<summary>2. Quels sont les principaux avantages de Python ?</summary>

#### Python

Principaux avantages de Python en production :

- vitesse de développement élevée grâce à une syntaxe concise ;
- vaste bibliothèque standard (`pathlib`, `itertools`, `collections`,
  `asyncio`) ;
- écosystème mature de paquets pour le back-end, les données, l'automatisation et les tests ;
- portabilité du code entre systèmes d'exploitation ;
- bon support du typage (`typing`, `mypy`, `pyright`) et des pratiques modernes.

**En bref :**

- Python réduit le time-to-market.
- Il fournit de nombreux outils prêts à l'emploi sans dépendances supplémentaires.
- Il convient aussi bien aux MVP qu'aux services évolutifs.

</details>

<details>
<summary>3. En quoi Python diffère-t-il des langages compilés ?</summary>

#### Python

Python est généralement exécuté par un interpréteur : le code est compilé en
bytecode puis exécuté à l'exécution dans la VM de CPython. Dans les langages
compilés (C/C++, Rust), il y a le plus souvent une compilation préalable en code machine.

Conséquences pratiques :

- Python est plus rapide pour le développement et le prototypage.
- Les langages compilés nativement sont généralement plus rapides pour les tâches intensives en CPU.
- En Python, les performances sont souvent améliorées par de meilleurs algorithmes, le profilage et les extensions C.

**En bref :**

- Python optimise la vitesse de développement.
- La compilation en code machine offre généralement de meilleures performances brutes.
- Le choix dépend du domaine et des exigences de latence et de débit.

</details>

<details>
<summary>4. Que signifie le typage dynamique en Python ?</summary>

#### Python

Le typage dynamique signifie que le type est lié à l'objet, et non au nom de
la variable. Un nom peut référencer des valeurs de types différents à des moments différents de l'exécution.

```python
value = 10        # int
value = "10"      # str
```

Les types sont vérifiés pendant l'exécution ; les erreurs de type apparaissent donc à l'exécution si aucun analyseur statique de types n'est utilisé.

**En bref :**

- En Python, le type appartient à l'objet, pas à la variable.
- Le type peut changer lorsqu'un nom est réaffecté.
- Les annotations de types ajoutent un contrôle avant l'exécution du code.

</details>

<details>
<summary>5. Que signifie le typage fort en Python ?</summary>

#### Python

Le typage fort en Python signifie que l'interpréteur n'effectue pas de conversions implicites dangereuses entre types incompatibles.

```python
1 + "2"  # TypeError
```

Pour effectuer des opérations entre types différents, une conversion explicite est nécessaire :

```python
1 + int("2")  # 3
```

**En bref :**

- Python est dynamiquement typé, mais strict quant à la compatibilité des types.
- Les conversions implicites dangereuses sont bloquées par une erreur.
- La conversion explicite rend le comportement prévisible.

</details>

<details>
<summary>6. Qu'est-ce que le REPL et quand l'utilise-t-on ?</summary>

#### Python

Le REPL (Read-Eval-Print Loop) est un mode interactif dans lequel vous saisissez une expression, obtenez immédiatement le résultat et validez rapidement des hypothèses.

Cas d'usage :

- vérifier l'API d'une bibliothèque ;
- tester rapidement une expression ou un algorithme ;
- explorer des données avant de les intégrer dans un module.

Outils : `python` standard, `ipython`, `ptpython`.

**En bref :**

- Le REPL offre la boucle de retour la plus rapide.
- Il est pratique pour les expériences et le débogage.
- Il ne remplace pas les tests, mais réduit le temps nécessaire pour valider des idées.

</details>

<details>
<summary>7. Que sont les littéraux en Python ? Donnez des exemples de différents types de littéraux.</summary>

#### Python

Un littéral est une valeur fixe écrite directement dans le code.

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

**En bref :**

- Les littéraux sont des valeurs constantes intégrées au code.
- Chaque type de base possède sa propre syntaxe littérale.
- Ils sont souvent utilisés pour initialiser des données.

</details>

<details>
<summary>8. Que sont les mots-clés en Python ?</summary>

#### Python

Les mots-clés sont des mots réservés du langage qui ont un rôle syntaxique
spécial et ne peuvent pas être utilisés comme noms de variables.

Exemples : `if`, `for`, `class`, `def`, `match`, `case`, `try`, `except`,
`async`, `await`.

Pour afficher la liste :

```python
import keyword
print(keyword.kwlist)
```

**En bref :**

- Les mots-clés définissent la syntaxe de Python.
- Ils ne peuvent pas être utilisés comme identifiants.
- La liste est disponible via le module `keyword`.

</details>

<details>
<summary>9. Qu'est-ce qu'une variable en Python ?</summary>

#### Python

Une variable en Python est un nom (une référence) qui pointe vers un objet en mémoire.
L'affectation lie le nom à l'objet ; elle ne "met pas la valeur dans une boîte".

```python
x = [1, 2]
y = x
y.append(3)
# x et y référencent la même liste
```

**En bref :**

- Une variable est une référence vers un objet.
- Plusieurs noms peuvent pointer vers le même objet mutable.
- C'est important pour comprendre les copies et les effets de bord.

</details>

<details>
<summary>10. Que sont `pass` et `...` (Ellipsis) en Python ?</summary>

#### Python

`pass` est une instruction vide : elle ne fait rien, mais permet de définir un bloc vide syntaxiquement valide.

`...` (Ellipsis) est un objet distinct, `Ellipsis`. Il est souvent utilisé comme marqueur de "pas encore implémenté", dans les annotations de types et dans des bibliothèques comme NumPy.

```python
def feature() -> None:
    pass

PLACEHOLDER = ...
```

**En bref :**

- `pass` est nécessaire pour les blocs de code vides.
- `...` est une valeur-objet, pas un mot-clé.
- Les deux servent de marqueurs temporaires, mais avec une sémantique différente.

</details>

<details>
<summary>11. Qu'est-ce qu'un PEP et comment influence-t-il l'évolution de Python ?</summary>

#### Python

Un PEP (Python Enhancement Proposal) est un document officiel qui décrit une
nouvelle fonctionnalité, une norme ou un processus dans l'écosystème Python.

Un PEP passe par :

- une discussion sur la conception ;
- une argumentation technique ;
- une décision d'acceptation ou de rejet ;
- une standardisation des pratiques.

Exemples : PEP 8 (style), PEP 484 (annotations de types), PEP 634 (pattern matching).

**En bref :**

- Un PEP est le mécanisme d'évolution du langage et de ses outils.
- Il rend les changements transparents et formalisés.
- De nombreuses pratiques modernes de Python ont été établies précisément via les PEP.

</details>

<details>
<summary>12. Qu'est-ce que le PEP 8 et à quoi sert-il ?</summary>

#### Python

Le PEP 8 est le guide de style officiel du code Python : conventions de nommage, formatage,
indentation, imports, longueur des lignes et lisibilité des constructions.

À quoi il sert :

- le code a un style cohérent dans toute l'équipe ;
- les code reviews sont plus rapides ;
- il y a moins de bruit dans les diffs ;
- la maintenabilité est meilleure.

En pratique, le style est automatisé avec `ruff format` ou `black` + `ruff`.

**En bref :**

- Le PEP 8 standardise le style du code Python.
- Il s'agit de lisibilité et de maintenance, pas de performance.
- Il vaut mieux automatiser son respect avec des outils.

</details>

<details>
<summary>13. Quelles nouvelles fonctionnalités sont apparues dans les versions modernes de Python (3.10+) ?</summary>

#### Python

Fonctionnalités clés du Python moderne :

- `match/case` (structural pattern matching) ;
- une syntaxe améliorée et de meilleurs messages d'erreur ;
- les types union avec `|` (`int | None`) ;
- `typing.Self`, `typing.TypeAlias`, `typing.override` ;
- les génériques au style PEP 695 (`class Box[T]: ...`, `def f[T](...) -> ...`) ;
- `tomllib` dans la bibliothèque standard.

En pratique, cela réduit le boilerplate et améliore la fiabilité du code typé.

**En bref :**

- Python 3.10+ a nettement amélioré la syntaxe et le typage.
- `match/case` et le `typing` moderne sont ce qui a l'impact le plus visible sur le code.
- Ces nouvelles fonctionnalités devraient être utilisées par défaut dans le nouveau code.

</details>

<details>
<summary>14. Qu'est-ce qu'une docstring en Python ?</summary>

#### Python

Une docstring est une chaîne de documentation, la première expression d'un module, d'une classe ou d'une fonction. Elle est
accessible via `__doc__` et utilisée par les IDE, `help()` et les générateurs de documentation.

```python
def normalize_email(email: str) -> str:
    """Return lowercase email without surrounding spaces."""
    return email.strip().lower()
```

Il est recommandé d'y décrire : ce que fait la fonction, les arguments, la valeur de retour et les exceptions.

**En bref :**

- Une docstring est une documentation intégrée au code.
- Elle sert de source pour `help()` et la génération automatique de documentation.
- Une docstring de qualité réduit le besoin de lire l'implémentation.

</details>

<details>
<summary>15. Comment fonctionne l'indentation en Python ?</summary>

#### Python

En Python, l'indentation définit les blocs de code (corps de `if`, `for`, `def`, `class`).
L'indentation fait donc partie de la syntaxe, et pas seulement du style.

```python
if is_ready:
    run_task()
else:
    stop_task()
```

Mélanger tabulations et espaces peut provoquer un `IndentationError` ou une
structure de bloc incorrecte.

**En bref :**

- L'indentation définit la structure du programme en Python.
- Une mauvaise indentation casse l'exécution.
- Utilisez un style cohérent (4 espaces).

</details>

<details>
<summary>16. Combien d'espaces faut-il pour l'indentation selon le PEP 8 et pourquoi est-il important de garder une indentation cohérente ?</summary>

#### Python

Le PEP 8 recommande **4 espaces** par niveau d'indentation.

Pourquoi c'est critique :

- structure de blocs cohérente dans tout le projet ;
- rendu prévisible dans différents éditeurs ;
- moins d'erreurs dues aux conflits tabulations/espaces ;
- diffs plus propres dans Git.

**En bref :**

- L'indentation standard est de 4 espaces.
- Un style unique élimine toute une classe d'erreurs de formatage.
- Cela améliore directement la lisibilité et la maintenabilité du code.

</details>

<details>
<summary>17. Quelle est la différence entre `ruff` et `black` en termes de fonctionnalités et d'usage ?</summary>

#### Python

`black` est un formateur de code avec des règles fixes.

`ruff` est un linter rapide, ainsi qu'un formateur et un auto-correcteur pour de nombreuses règles (PEP 8,
imports, bugs potentiels, simplifications de syntaxe).

Approches pratiques :

- soit `ruff check --fix` + `ruff format` ;
- soit `ruff` pour le lint + `black` pour le formatage.

**En bref :**

- `black` se concentre sur le formatage.
- `ruff` couvre le linting et une partie des corrections automatiques.
- Dans les projets modernes, `ruff` seul suffit souvent.

</details>

<details>
<summary>18. Expliquez l'objectif des annotations de types en Python et donnez un exemple de fonction avec annotations de types.</summary>

#### Python

Les annotations de types décrivent les types attendus des arguments et de la valeur de retour. Elles
améliorent l'autocomplétion, l'analyse statique et la lisibilité de l'API.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Les annotations n'effectuent pas elles-mêmes de validation à l'exécution, mais elles aident à trouver
des erreurs au niveau de la CI via `mypy`/`pyright`.

**En bref :**

- Les annotations de types documentent le contrat de la fonction.
- Elles permettent une détection précoce des erreurs via la vérification statique.
- Elles améliorent la qualité des API dans les grandes bases de code.

</details>

<details>
<summary>19. Qu'est-ce que le debugging et pourquoi est-ce une compétence importante pour les programmeurs ?</summary>

#### Python

Le debugging est la recherche systématique de la cause d'un comportement incorrect du code et sa correction.
Il ne s'agit pas seulement de "trouver un bug", mais de le reproduire, le localiser et vérifier le correctif.

Cycle de base :

- reproduire le problème ;
- réduire la zone de code concernée ;
- vérifier une hypothèse (avec des logs/un débogueur) ;
- ajouter un test qui fixe le scénario.

**En bref :**

- Le debugging réduit le MTTR et le nombre de régressions.
- Il fonctionne le mieux comme un processus, pas comme une recherche chaotique.
- La fin du debugging, c'est : correctif + test + vérification finale.

</details>

<details>
<summary>20. Expliquez l'intérêt d'utiliser la fonction `print` pour le débogage. Donnez un exemple de situation où cette approche est utile.</summary>

#### Python

Le `print`-debugging est un moyen rapide de vérifier les valeurs des variables et l'ordre
d'exécution sans lancer d'outils complexes.

Il est utile quand il faut valider rapidement une hypothèse dans un script local :

```python
def parse_port(raw: str) -> int:
    value = raw.strip()
    print(f"raw={raw!r} value={value!r}")
    return int(value)
```

Pour du code de production, il vaut mieux passer à `logging` afin d'avoir des niveaux de logs et
une sortie contrôlée.

**En bref :**

- `print` convient à un diagnostic local court.
- Il montre rapidement l'état des variables au point problématique.
- Pour un diagnostic stable dans un service, utilisez `logging`.

</details>

<details>
<summary>21. Décrivez comment utiliser Python Debugger (PDB) pour le débogage. Quels sont les avantages de PDB par rapport à `print` ?</summary>

#### Python

`pdb` permet de suspendre l'exécution du programme, d'avancer ligne par ligne,
d'inspecter l'état des variables et la pile d'appels.

Utilisation de base :

```python
import pdb

def compute(x: int) -> int:
    pdb.set_trace()
    return x * 2
```

Commandes clés : `n` (next), `s` (step), `c` (continue), `p expr` (print expr),
`l` (list), `bt` (backtrace).

**En bref :**

- `pdb` donne un contrôle interactif de l'exécution.
- Il est plus efficace que `print` pour les scénarios complexes.
- Il permet de diagnostiquer l'état sans encombrer le code de logs.

</details>

<details>
<summary>22. Quelles stratégies peut-on utiliser pour déboguer des boucles et des fonctions en Python ?</summary>

#### Python

Stratégies pratiques :

- isoler le bug avec un exemple minimal reproductible ;
- journaliser les invariants aux itérations de la boucle ;
- placer des breakpoints à l'entrée et à la sortie de la fonction ;
- vérifier les cas limites (données vides, `None`, gros volumes) ;
- couvrir le chemin problématique par un test.

Pour les boucles, il est utile de journaliser l'index et les états
intermédiaires clés.

**En bref :**

- Commencez par reproduire le problème et en réduire le périmètre.
- Vérifiez les invariants et les conditions limites.
- Finalisez le correctif avec un test qui capture la régression.

</details>

<details>
<summary>23. Quel impact les fonctions de longue durée ont-elles sur les performances du programme ?</summary>

#### Python

Les fonctions de longue durée augmentent la latence, bloquent les workers ou les threads et dégradent
le débit du service.

Risques :

- réponses API lentes ;
- timeouts ;
- croissance des files de tâches ;
- moins bonne utilisation du CPU/de l'I/O.

Approche : profiler (`cProfile`), découper en étapes plus petites, utiliser
des générateurs/du streaming, déplacer les calculs lourds vers `multiprocessing` ou l'arrière-plan.

**En bref :**

- Les fonctions longues frappent directement la latence.
- L'optimisation doit se faire à partir du profilage, pas de l'intuition.
- Sur le plan architectural, il vaut mieux séparer les charges CPU-bound et I/O-bound.

</details>

<details>
<summary>24. Qu'est-ce que le logging et pourquoi vaut-il mieux l'utiliser à la place de `print` ?</summary>

#### Python

`logging` est le mécanisme standard de journalisation d'événements avec des niveaux (`DEBUG`,
`INFO`, `WARNING`, `ERROR`, `CRITICAL`), des formats et des handlers (console,
fichier).

Pourquoi c'est préférable à `print` :

- niveaux de détail contrôlables ;
- format structuré ;
- configuration centralisée ;
- possibilité d'intégration avec une stack d'observabilité.

**En bref :**

- `logging` convient à la production, `print` non.
- Les niveaux de logs permettent de contrôler le bruit.
- Les logs doivent être structurés et cohérents.

</details>

<details>
<summary>25. Qu'est-ce qu'une traceback ?</summary>

#### Python

Une traceback est la pile d'appels que Python affiche lors d'une exception : où
l'exécution a commencé, par quelles fonctions le code est passé et où exactement l'erreur s'est produite.

Usage :

- trouver rapidement le fichier/la ligne source de l'erreur ;
- comprendre le chemin d'exécution jusqu'à l'échec ;
- construire un test précis de reproduction.

**En bref :**

- La traceback est la "route" vers l'erreur.
- La partie la plus précieuse : les dernières frames de la pile et le type d'exception.
- L'analyse de la traceback accélère la recherche de la cause racine.

</details>

<details>
<summary>26. Quels sont les principaux types de données en Python ?</summary>

#### Python

Principaux types built-in :

- numériques : `int`, `float`, `complex` ;
- booléen : `bool` ;
- chaînes/octets : `str`, `bytes`, `bytearray` ;
- collections : `list`, `tuple`, `set`, `dict`, `frozenset` ;
- spéciaux : `NoneType` (`None`).

Il est important de comprendre la mutabilité :

- mutable : `list`, `dict`, `set`, `bytearray` ;
- immuable : `int`, `str`, `tuple`, `frozenset`.

**En bref :**

- Python possède un riche ensemble de types de base "out of the box".
- Le choix de la structure de données influence la complexité des opérations.
- La mutabilité détermine le comportement des copies et les effets de bord.

</details>

<details>
<summary>27. Quelle est la différence entre la division classique (`/`) et la division entière (`//`) en Python ?</summary>

#### Python

`/` effectue une division classique et retourne toujours un `float`.

`//` effectue une division par plancher : il retourne la partie entière vers le bas (jusqu'à `-∞`), le type étant généralement
`int` pour des opérandes entiers.

```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

**En bref :**

- `/` -> résultat réel.
- `//` -> arrondi vers le bas à l'entier.
- Pour les nombres négatifs, `//` n'est pas équivalent à un "tronquage vers zéro".

</details>

<details>
<summary>28. Expliquez l'utilisation de l'opérateur modulo (`%`) en Python. Comment peut-on l'utiliser pour déterminer si un nombre est pair ou impair ?</summary>

#### Python

L'opérateur `%` retourne le reste de la division.

Vérification de la parité :

```python
def is_even(n: int) -> bool:
    return n % 2 == 0
```

Si `n % 2 == 0`, le nombre est pair ; sinon, il est impair.

Cas typiques : index cycliques, répartition en groupes, calculs calendaires.

**En bref :**

- `%` retourne le reste.
- `n % 2` est la vérification standard de la parité.
- Il est souvent utilisé pour la logique cyclique.

</details>

<details>
<summary>29. Comment Python gère-t-il les grands entiers et quelles sont les limites lorsqu'on travaille avec de très grands nombres ?</summary>

#### Python

`int` en Python a une précision arbitraire, c'est-à-dire qu'il n'est pas limité
à 32/64 bits comme dans beaucoup de langages.

Les limites sont pratiques :

- la mémoire du processus ;
- le temps de calcul pour des valeurs très grandes ;
- le coût des opérations augmente avec le nombre de chiffres.

**En bref :**

- Il n'y a pas de débordement de `int` au sens classique.
- La limite, ce sont les ressources de la machine, pas une taille fixe en bits.
- Pour les gros calculs, les algorithmes et le profilage sont essentiels.

</details>

<details>
<summary>30. Pourquoi le traitement de la division par zéro est-il important en Python et comment éviter `ZeroDivisionError` dans le code ?</summary>

#### Python

La division par zéro provoque `ZeroDivisionError`. Il faut la gérer explicitement si
le diviseur vient d'une entrée externe ou est calculé dynamiquement.

```python
def safe_div(a: float, b: float) -> float | None:
    if b == 0:
        return None
    return a / b
```

Dans les scénarios critiques, utilisez `try/except` et journalisez le contexte.

**En bref :**

- La division par zéro est une erreur d'exécution contrôlée.
- La prévention la plus simple : vérifier le diviseur avant l'opération.
- Pour les données externes, ajoutez protection et diagnostic.

</details>

<details>
<summary>31. Décrivez l'utilisation du module `random` en Python. Quelles sont les fonctions les plus courantes de ce module ?</summary>

#### Python

`random` est utilisé pour produire des valeurs pseudo-aléatoires dans les simulations, les
données de test et les tâches non cryptographiques.

Fonctions courantes :

- `random()` — nombre dans `[0.0, 1.0)` ;
- `randint(a, b)` — entier dans un intervalle ;
- `randrange(start, stop, step)` — comme `range`, mais retourne un élément aléatoire ;
- `choice(seq)` / `choices(seq, k=...)` ;
- `shuffle(list_)` — mélange une liste in-place ;
- `sample(population, k)` — échantillon unique.

Pour la cryptographie, utilisez `secrets`, pas `random`.

**En bref :**

- `random` convient à l'aléatoire applicatif classique.
- Les plus utilisés sont : `randint`, `choice`, `shuffle`, `sample`.
- Pour les tâches sensibles côté sécurité, il faut `secrets`.

</details>

<details>
<summary>32. Comment travailler avec des nombres plus précis en Python ?</summary>

#### Python

Pour les calculs financiers et les calculs décimaux précis, utilisez `decimal.Decimal`,
et non `float`.

```python
from decimal import Decimal

total = Decimal("0.1") + Decimal("0.2")  # Decimal('0.3')
```

Pour les nombres rationnels, `fractions.Fraction` est utile.

**En bref :**

- `float` est pratique, mais il a des erreurs liées à la représentation binaire.
- Pour une arithmétique décimale exacte, choisissez `Decimal`.
- Le type numérique doit correspondre au domaine du problème.

</details>

<details>
<summary>33. Que sont les caractères d'échappement dans les chaînes Python et comment les utilise-t-on ? Donnez des exemples pour `\n`, `\t`, `\r`, `\"` et `\'`.</summary>

#### Python

Les séquences d'échappement sont des combinaisons spéciales avec `\` qui codent des
caractères de contrôle à l'intérieur d'une chaîne.

- `\n` — nouvelle ligne
- `\t` — tabulation
- `\r` — retour chariot
- `\"` — guillemet double dans une chaîne avec `"`
- `\'` — apostrophe dans une chaîne avec `'`

```python
text = "A\tB\n\"quoted\"\nI\'m here\rX"
```

**En bref :**

- Les caractères d'échappement contrôlent le formatage de la chaîne.
- Ils permettent d'insérer des guillemets sans casser la syntaxe.
- Pour les chemins/regex, il est souvent pratique d'utiliser des chaînes brutes `r"..."`.

</details>

<details>
<summary>34. Expliquez l'utilisation des méthodes `strip`, `lstrip` et `rstrip` en Python. Quelle est leur différence ?</summary>

#### Python

Ces méthodes travaillent sur les bords de la chaîne :

- `strip()` — supprime des caractères des deux côtés ;
- `lstrip()` — uniquement à gauche ;
- `rstrip()` — uniquement à droite.

Par défaut, elles suppriment les espaces blancs, ou un ensemble spécifique de caractères :

```python
"  hello  ".strip()      # "hello"
"--id--".strip("-")      # "id"
```

**En bref :**

- La famille `strip` ne modifie pas la chaîne in-place, mais retourne une nouvelle chaîne.
- La différence se limite au côté nettoyé.
- Ces méthodes sont souvent utilisées sur des données d'entrée.

</details>

<details>
<summary>35. Décrivez l'objectif de la méthode `count` sur les chaînes. Comment fonctionne-t-elle ?</summary>

#### Python

`str.count(sub[, start[, end]])` compte le nombre d'occurrences non chevauchantes de la sous-chaîne
`sub` dans l'intervalle choisi.

```python
"banana".count("an")      # 2
"banana".count("a", 2)    # 2
```

Elle retourne `0` s'il n'y a aucune occurrence.

**En bref :**

- `count` donne rapidement le nombre d'occurrences d'une sous-chaîne.
- Elle prend en charge la limitation de recherche via `start/end`.
- Elle compte les occurrences non chevauchantes.

</details>

<details>
<summary>36. Comment fonctionne la méthode `join` en Python et dans quels cas l'utilise-t-on le plus souvent ?</summary>

#### Python

`sep.join(iterable)` assemble une séquence de chaînes en une seule chaîne avec le séparateur
`sep`.

```python
names = ["Ada", "Linus", "Guido"]
result = ", ".join(names)  # "Ada, Linus, Guido"
```

Usages typiques : génération de chaînes de type CSV, de logs, de fragments SQL,
de chemins d'URL et de messages.

**En bref :**

- `join` est le moyen standard et rapide de concaténer des chaînes.
- Elle s'appelle sur le séparateur, pas sur la liste.
- Elle est plus efficace que des `+=` répétés dans une boucle.

</details>

<details>
<summary>37. Qu'est-ce que le slicing en Python et comment permet-il d'obtenir des sous-chaînes ? Donnez des exemples avec des indices positifs et négatifs.</summary>

#### Python

Le slicing consiste à sélectionner une partie d'une séquence via `[start:stop:step]`.

```python
s = "python"
s[1:4]     # "yth"
s[:2]      # "py"
s[-3:]     # "hon"
s[::-1]    # "nohtyp"
```

`start` est inclus, `stop` est exclu.

**En bref :**

- Le slicing fonctionne pour les chaînes, les listes et les tuples.
- Les indices négatifs sont comptés depuis la fin.
- C'est un outil de base pour traiter des séquences sans boucle.

</details>

<details>
<summary>38. Expliquez la méthode `replace` pour les chaînes. Comment l'utiliser pour remplacer plusieurs occurrences d'une sous-chaîne ?</summary>

#### Python

`str.replace(old, new, count=-1)` retourne une nouvelle chaîne où `old` est remplacé par
`new`. Par défaut, toutes les occurrences sont remplacées.

```python
"foo bar foo".replace("foo", "baz")      # "baz bar baz"
"foo bar foo".replace("foo", "baz", 1)   # "baz bar foo"
```

**En bref :**

- `replace` ne modifie pas la chaîne in-place.
- Sans `count`, elle remplace toutes les occurrences.
- `count` permet de contrôler le nombre de remplacements.

</details>

<details>
<summary>39. Comment fonctionne la méthode `split` sur les chaînes ?</summary>

#### Python

`split(sep=None, maxsplit=-1)` découpe une chaîne en liste de sous-chaînes.

- sans `sep`, elle découpe sur n'importe quel caractère d'espacement ;
- avec `sep`, elle découpe selon un séparateur spécifique ;
- `maxsplit` limite le nombre de découpages.

```python
"a,b,c".split(",")         # ["a", "b", "c"]
"a b   c".split()          # ["a", "b", "c"]
"k=v=x".split("=", 1)      # ["k", "v=x"]
```

**En bref :**

- `split` transforme une chaîne en liste de tokens.
- `sep=None` a un comportement spécial pour les espaces blancs.
- `maxsplit` est utile pour parser des formats key/value.

</details>

<details>
<summary>40. Comment fonctionne la conversion de types (type casting) ?</summary>

#### Python

Le type casting est une conversion explicite d'une valeur entre types via des constructeurs :
`int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`, `set()`, `dict()`.

```python
age = int("42")
price = float("19.99")
text = str(10)
```

Des données invalides provoquent une exception (`ValueError`, `TypeError`), donc
une validation est nécessaire pour les entrées externes.

**En bref :**

- Python fournit des fonctions explicites de conversion de types.
- Toutes les valeurs ne peuvent pas être converties sans risque.
- Pour les entrées utilisateur, il faut des vérifications et une gestion des exceptions.

</details>

<details>
<summary>41. Comment Python convertit-il automatiquement différents types de données en valeurs booléennes ?</summary>

#### Python

Dans un contexte booléen, Python applique les règles de truthiness.

Valeurs de type `False` :

- `False`, `None` ;
- nombres nuls : `0`, `0.0`, `0j` ;
- collections vides : `""`, `[]`, `{}`, `set()`, `tuple()`, `range(0)`.

Tout le reste est généralement `True`.

```python
bool([])      # False
bool("0")     # True
```

**En bref :**

- La conversion booléenne repose sur les règles truthy/falsy.
- Le vide et le zéro donnent `False`.
- Une chaîne non vide `"0"` reste malgré tout `True`.

</details>

<details>
<summary>42. Expliquez comment convertir une chaîne en entier ou en nombre réel en Python. Que se passe-t-il si la chaîne ne peut pas être convertie en nombre ?</summary>

#### Python

Pour la conversion, utilisez `int()` et `float()` :

```python
count = int("42")
ratio = float("3.14")
```

Si la chaîne n'est pas valide, Python lève `ValueError`.

```python
def parse_int(value: str) -> int | None:
    try:
        return int(value)
    except ValueError:
        return None
```

**En bref :**

- `int()`/`float()` effectuent une conversion explicite depuis une chaîne.
- Format invalide -> `ValueError`.
- Pour les données externes, il faut `try/except`.

</details>

<details>
<summary>43. Que fait Python lorsqu'il compare différents types de données, comme des entiers et des réels, ou des entiers et des booléens ?</summary>

#### Python

Python autorise la comparaison numérique de types numériques compatibles.

- `int` et `float` sont comparés par valeur.
- `bool` est une sous-classe de `int` : `False == 0`, `True == 1`.

```python
1 == 1.0      # True
True == 1     # True
False < 1     # True
```

Pour les types incompatibles (par exemple `int` et `str`), la comparaison d'ordre (`<`, `>`)
provoque `TypeError`.

**En bref :**

- `int`, `float` et `bool` partagent une même sémantique numérique.
- `bool` se comporte comme `0/1` dans les comparaisons.
- Les types incompatibles ne se comparent pas avec des opérateurs d'ordre.

</details>

<details>
<summary>44. Comment Python gère-t-il les comparaisons entre listes et sets ?</summary>

#### Python

`list` et `set` sont des types différents avec une sémantique différente ; une comparaison d'ordre directe
entre eux n'est donc pas prise en charge.

```python
[1, 2] == {1, 2}   # False
[1, 2] < {1, 2}    # TypeError
```

Si vous devez comparer la composition des éléments, normalisez le type :

```python
set([1, 2]) == {1, 2}  # True
```

**En bref :**

- `list` et `set` sont comparés comme des structures de données différentes.
- `==` entre eux renvoie généralement `False`.
- Pour une comparaison pertinente, convertissez-les d'abord vers un même type.

</details>

<details>
<summary>45. Décrivez l'utilisation de la fonction `bool()` en Python.</summary>

#### Python

`bool(x)` retourne la valeur booléenne de `x` selon les règles de truthiness.

Scénarios typiques :

- conversion explicite d'une valeur vers `True/False` ;
- conditions plus lisibles ;
- construction de filtres.

```python
bool("text")   # True
bool("")       # False
bool(0)        # False
```

**En bref :**

- `bool()` unifie les vérifications de type "vide/non vide".
- Elle s'appuie sur les règles intégrées truthy/falsy.
- Elle est utile pour la validation et la logique conditionnelle.

</details>

<details>
<summary>46. Quelle est la différence entre `list` et `tuple` ?</summary>

#### Python

La différence principale : `list` est mutable, `tuple` est immuable.

Conséquences pratiques :

- `list` convient aux données qui changent ;
- `tuple` convient aux enregistrements fixes ;
- `tuple` peut être utilisé comme clé de dictionnaire (si ses éléments sont hashables).

```python
coords: tuple[float, float] = (50.45, 30.52)
queue: list[str] = ["task-1", "task-2"]
```

**En bref :**

- `list` sert aux collections modifiables.
- `tuple` sert aux structures de données immuables.
- Le choix influence la sûreté de l'API et l'utilisation dans `dict/set`.

</details>

<details>
<summary>47. Comment peut-on créer un `tuple` ?</summary>

#### Python

Principales façons :

```python
t1 = (1, 2, 3)
t2 = 1, 2, 3
t3 = tuple([1, 2, 3])
single = (42,)     # важлива кома
empty = ()
```

Pour un seul élément, la virgule est obligatoire ; sinon, ce n'est qu'une expression entre parenthèses.

**En bref :**

- On crée un `tuple` avec un littéral ou via `tuple(iterable)`.
- `single = (x,)` est un tuple à un seul élément correct.
- Le tuple vide : `()`.

</details>

<details>
<summary>48. Quelle est la différence entre la méthode `reverse` et le slicing `[::-1]` pour inverser une liste ?</summary>

#### Python

`list.reverse()` modifie la liste existante in-place et retourne `None`.

`lst[::-1]` crée une nouvelle liste inversée (une copie).

```python
values = [1, 2, 3]
values.reverse()      # values -> [3, 2, 1]

other = values[::-1]  # nouvelle liste
```

**En bref :**

- `reverse()` modifie l'original.
- `[::-1]` retourne un nouvel objet.
- Le choix dépend du besoin de conserver les données d'origine.

</details>

<details>
<summary>49. Expliquez le rôle et l'utilisation de la méthode `sort` pour les listes. Comment trier une liste dans l'ordre décroissant ?</summary>

#### Python

`list.sort()` trie la liste in-place. Elle prend en charge les paramètres :

- `key` — fonction de clé de tri ;
- `reverse=True` — ordre décroissant.

```python
nums = [5, 1, 7]
nums.sort(reverse=True)  # [7, 5, 1]
```

Si vous avez besoin d'une nouvelle copie triée, utilisez `sorted(iterable)`.

**En bref :**

- `sort()` modifie la liste sur place.
- Pour l'ordre décroissant, utilisez `reverse=True`.
- `sorted()` est pratique quand il faut conserver l'original.

</details>

<details>
<summary>50. Quelle est la différence entre la méthode `copy` et l'affectation directe d'une liste à une autre ? Pourquoi est-il parfois important d'utiliser `copy` ?</summary>

#### Python

L'affectation ne copie que la référence :

```python
a = [1, 2]
b = a
b.append(3)   # a changera aussi
```

`a.copy()` crée une nouvelle liste (superficielle) :

```python
a = [1, 2]
b = a.copy()
b.append(3)   # a ne changera pas
```

Pour les structures imbriquées, `copy.deepcopy` peut être nécessaire.

**En bref :**

- `=` ne copie pas les données, mais partage un seul objet entre plusieurs variables.
- `copy()` isole les changements au niveau de la liste supérieure.
- Pour les objets imbriqués, utilisez `deepcopy`.

</details>

<details>
<summary>51. Que fait la méthode `pop` sur une liste ? En quoi son comportement diffère-t-il selon qu'on indique un index ou non ?</summary>

#### Python

`pop()` supprime et retourne un élément de la liste.

- `pop()` sans argument supprime le dernier élément ;
- `pop(i)` supprime l'élément à l'index `i`.

```python
items = ["a", "b", "c"]
last = items.pop()     # "c"
first = items.pop(0)   # "a"
```

Un index invalide provoque `IndexError`.

**En bref :**

- `pop` combine suppression et retour de valeur.
- Sans index, elle agit sur la fin de la liste.
- Avec un index, elle supprime une position précise.

</details>

<details>
<summary>52. Comment fusionner deux listes en Python en utilisant l'opérateur `+` et la méthode `extend` ? Quelle est la différence clé entre ces deux approches ?</summary>

#### Python

`a + b` crée une **nouvelle** liste, tandis que `a.extend(b)` modifie la liste `a`
**in-place**.

```python
a = [1, 2]
b = [3, 4]

c = a + b         # [1, 2, 3, 4], a n'a pas changé
a.extend(b)       # a -> [1, 2, 3, 4]
```

**En bref :**

- `+` retourne un nouvel objet.
- `extend()` mute la liste existante.
- Le choix dépend du fait qu'il faille ou non conserver l'original.

</details>

<details>
<summary>53. À quoi servent les fonctions `min`, `max`, `sum`, `all`, `any` dans le contexte des listes ?</summary>

#### Python

Ce sont des agrégateurs de base pour les collections itérables :

- `min()` / `max()` — minimum et maximum ;
- `sum()` — somme des nombres ;
- `all()` — `True` si tous les éléments sont truthy ;
- `any()` — `True` si au moins un élément est truthy.

```python
nums = [3, 10, 1]
min(nums), max(nums), sum(nums)  # (1, 10, 14)
all([True, 1, "x"])              # True
any([0, "", None, 5])            # True
```

**En bref :**

- Ces fonctions réduisent le boilerplate dans les boucles.
- Elles fonctionnent avec n'importe quel iterable.
- Elles se combinent bien avec les générateurs pour un traitement lazy.

</details>

<details>
<summary>54. Qu'est-ce qu'un dictionnaire (`dict`) en Python et en quoi diffère-t-il des autres structures de données ?</summary>

#### Python

`dict` est un tableau associatif : il stocke des paires `clé -> valeur`. Les clés doivent être
hashables, les valeurs peuvent être de n'importe quel type.

Différences :

- accès par clé, et non par index ;
- complexité moyenne de recherche/insertion/suppression proche de `O(1)` ;
- depuis Python 3.7+, conserve l'ordre d'insertion des clés.

**En bref :**

- `dict` est optimal pour un accès rapide par clé.
- C'est la structure principale pour les configurations et les mappings.
- Les clés doivent être immuables (hashables).

</details>

<details>
<summary>55. Quelle est la différence entre récupérer une valeur d'un dictionnaire via des crochets `[]` et via la méthode `get` ?</summary>

#### Python

`d[key]` retourne la valeur ou lève `KeyError` si la clé n'existe pas.

`d.get(key, default)` retourne la valeur ou `default` (ou `None`), sans exception.

```python
config = {"timeout": 30}
config["timeout"]         # 30
config.get("retries", 3)  # 3
```

**En bref :**

- `[]` sert pour les clés obligatoires.
- `get()` sert pour les champs optionnels.
- `get()` réduit le besoin de `try/except` lors de la lecture des données.

</details>

<details>
<summary>56. Décrivez comment mettre à jour et supprimer des éléments dans un dictionnaire.</summary>

#### Python

Mise à jour :

- `d[key] = value` — insérer/mettre à jour une seule clé ;
- `d.update({...})` — mise à jour groupée.

Suppression :

- `del d[key]` — supprimer la clé (erreur si absente) ;
- `d.pop(key, default)` — supprimer et retourner la valeur ;
- `d.popitem()` — supprimer la dernière paire ;
- `d.clear()` — vider tout le dictionnaire.

**En bref :**

- Pour un upsert, `[]` et `update()` conviennent.
- Pour une suppression sûre, on utilise plus souvent `pop()`.
- Choisissez l'API selon le comportement souhaité en cas de clé absente.

</details>

<details>
<summary>57. À quoi servent les méthodes `keys`, `values` et `items` dans les dictionnaires ?</summary>

#### Python

Ces méthodes retournent des objets-vues du dictionnaire :

- `keys()` — toutes les clés ;
- `values()` — toutes les valeurs ;
- `items()` — les paires `(key, value)`.

```python
data = {"a": 1, "b": 2}
for key, value in data.items():
    ...
```

Les vues sont dynamiques : elles reflètent l'état actuel du dictionnaire.

**En bref :**

- `keys/values/items` sont utiles pour l'itération et les vérifications.
- `items()` est la plus pratique pour boucler sur la clé et la valeur.
- Ce ne sont pas des copies, mais des représentations "vivantes" des données.

</details>

<details>
<summary>58. Comment `dict` est-il implémenté en Python sous le capot ?</summary>

#### Python

`dict` est implémenté comme une table de hachage avec des optimisations mémoire et d'accès rapide.
La clé est hachée, une case est choisie à partir du hash, et les collisions sont résolues par un
algorithme interne de probing.

Conséquences pratiques :

- accès moyen proche de `O(1)` ;
- la qualité de `__hash__` et `__eq__` influence le comportement ;
- les objets mutables ne peuvent pas être utilisés comme clés.

**En bref :**

- `dict` est une structure de hachage haute performance.
- Sa rapidité vient du hachage.
- Les clés doivent être hashables et stables.

</details>

<details>
<summary>59. Qu'est-ce qu'une fonction de hachage ?</summary>

#### Python

Une fonction de hachage transforme un objet en entier (hash), utilisé pour
le placement/la recherche rapides dans `dict` et `set`.

Conditions de correction :

- si `a == b`, alors `hash(a) == hash(b)` ;
- la valeur du hash doit rester stable pendant toute la durée de vie de l'objet.

**En bref :**

- La fonction de hachage est la base du fonctionnement rapide de `dict/set`.
- Elle ne garantit pas l'unicité (des collisions sont possibles).
- Pour les classes personnalisées, la cohérence entre `__eq__` et `__hash__` est essentielle.

</details>

<details>
<summary>60. Qu'est-ce qu'un `set` en Python et en quoi diffère-t-il des autres structures de données ?</summary>

#### Python

`set` est une collection non ordonnée d'éléments **uniques**.

Différences :

- supprime automatiquement les doublons ;
- opérations rapides de test d'appartenance (`x in s`) ;
- prend en charge les opérations ensemblistes : union/intersection/difference.

**En bref :**

- `set` est optimal pour l'unicité et les tests d'appartenance.
- L'ordre des éléments n'est pas garanti.
- Les éléments doivent être hashables.

</details>

<details>
<summary>61. Comment créer un `set` en Python et quelles restrictions existent pour ses éléments ?</summary>

#### Python

Création :

```python
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # {1, 2, 3}
empty = set()            # pas {}
```

Restrictions :

- les éléments doivent être hashables (par exemple `int`, `str`, `tuple`) ;
- `list`, `dict`, `set` ne peuvent pas être ajoutés directement.

**En bref :**

- `set()` crée un ensemble vide.
- Les doublons sont supprimés automatiquement.
- Seuls les éléments hashables sont autorisés.

</details>

<details>
<summary>62. À quoi sert la méthode `intersection()` d'un set en Python et en quoi diffère-t-elle de `union()` ?</summary>

#### Python

`intersection()` retourne les éléments communs des ensembles, tandis que `union()` réunit tous
les éléments uniques des deux ensembles.

```python
a = {1, 2, 3}
b = {3, 4}

a.intersection(b)  # {3}
a.union(b)         # {1, 2, 3, 4}
```

**En bref :**

- `intersection` = intersection (commun).
- `union` = union (tout l'unique).
- Ces deux méthodes sont fondamentales pour comparer des jeux de données.

</details>

<details>
<summary>63. Quels types de données sont immuables ?</summary>

#### Python

Types immuables courants :

- `int`, `float`, `bool`, `complex`;
- `str`, `bytes`;
- `tuple` (si ses éléments sont aussi immuables) ;
- `frozenset`;
- `NoneType`.

**En bref :**

- Un objet immuable ne peut pas être modifié après sa création.
- Au lieu d'une mutation, un nouvel objet est créé.
- Ces types sont plus sûrs pour les clés de `dict` et les éléments de `set`.

</details>

<details>
<summary>64. Quels types de données sont mutables ?</summary>

#### Python

Types mutables courants :

- `list`;
- `dict`;
- `set`;
- `bytearray`;
- la plupart des objets de classes définies par l'utilisateur.

**En bref :**

- Les objets mutables changent in-place.
- Les mutations peuvent créer des effets de bord via des références partagées.
- Il faut être prudent avec les copies.

</details>

<details>
<summary>65. Pourquoi est-il important de comprendre la mutabilité quand on travaille avec des dictionnaires ou des sets ?</summary>

#### Python

`dict` et `set` reposent sur le hachage ; leurs éléments/clés doivent donc être
stables (hashables). Les objets mutables ne peuvent pas être utilisés en toute sécurité comme
clés ou comme éléments d'un set.

De plus, la mutation de valeurs via des références partagées produit souvent des bugs inattendus.

**En bref :**

- La mutabilité affecte la validité des clés dans `dict/set`.
- Les objets mutables partagés produisent souvent des effets de bord.
- Les copies explicites et le contrôle des mutations réduisent les bugs.

</details>

<details>
<summary>66. Qu'est-ce que `None` ?</summary>

#### Python

`None` est une valeur singleton spéciale du type `NoneType` qui signifie
"absence de valeur".

Scénarios typiques :

- une fonction ne retourne rien explicitement ;
- des paramètres optionnels ;
- un marqueur "les données ne sont pas encore définies".

La vérification se fait avec `is` :

```python
if value is None:
    ...
```

**En bref :**

- `None` signifie l'absence de valeur.
- C'est un singleton, donc on le compare avec `is`.
- Il est souvent utilisé dans une API comme état optionnel.

</details>

<details>
<summary>67. Qu'est-ce que `id` en Python, comment l'utiliser et pourquoi est-ce important ?</summary>

#### Python

`id(obj)` retourne l'identifiant d'un objet (unique pendant le cycle de vie
de l'objet dans le processus courant).

Utile pour le diagnostic :

- savoir s'il s'agit du même objet ;
- savoir si une copie a été créée ;
- savoir si une mutation d'une référence partagée a eu lieu.

**En bref :**

- `id` aide à analyser l'identité des objets.
- Il est utile pour déboguer les copies et mutations.
- Il n'est pas utilisé comme identifiant métier.

</details>

<details>
<summary>68. Quelle est la différence entre les opérateurs `is` et `==` ?</summary>

#### Python

`==` compare les **valeurs** (équivalence), tandis que `is` compare l'**identité**
(s'il s'agit ou non du même objet en mémoire).

```python
a = [1, 2]
b = [1, 2]
a == b   # True
a is b   # False
```

**Important à propos des optimisations (interning) :** CPython met en cache ("intern") les petits
entiers (de -5 à 256) et les chaînes courtes au moment de la compilation/du chargement. Ainsi,
pour eux, `is` peut retourner `True` même s'ils ont été créés séparément. Mais ce sont des
détails d'implémentation sur lesquels il ne faut pas s'appuyer dans la logique métier.

Pour `None`, utilisez toujours `is`.

**En bref :**

- `==` concerne l'égalité des valeurs.
- `is` concerne le même objet en mémoire.
- L'interning peut produire un `is True` non évident pour de petits `int` et `str`.
- `value is None` est le seul style correct pour tester `None`.

</details>

<details>
<summary>69. Comment le pattern Singleton s'applique-t-il en Python ? Donnez des exemples d'objets singleton en Python.</summary>

#### Python

Singleton signifie une seule instance globale d'un objet dans un processus. En Python,
il est souvent remplacé par le niveau du module (les modules ne sont importés qu'une seule fois).

Exemples d'objets singleton du langage :

- `None`;
- `True` і `False`;
- `Ellipsis`.

Dans le code applicatif, au lieu d'un Singleton rigide, on utilise plus souvent
un conteneur d'injection de dépendances ou des fabriques pour une meilleure testabilité.

**En bref :**

- Python possède déjà des objets singleton intégrés.
- Souvent, une portée au niveau du module suffit sans pattern séparé.
- Abuser du Singleton dégrade la testabilité.

</details>

<details>
<summary>70. À quoi servent les opérateurs `break` et `continue` dans les boucles Python ?</summary>

#### Python

`break` termine la boucle de manière anticipée, `continue` saute l'itération en cours et
passe à la suivante.

```python
for n in range(10):
    if n == 5:
        break
    if n % 2 == 0:
        continue
```

**En bref :**

- `break` arrête complètement la boucle.
- `continue` ne saute que l'étape actuelle.
- Ils rendent le contrôle de la boucle explicite et lisible.

</details>

<details>
<summary>71. Expliquez la notion de boucle infinie. Dans quels cas est-il pertinent d'utiliser une boucle infinie et comment assurer sa terminaison correcte ?</summary>

#### Python

Une boucle infinie est une boucle sans condition naturelle de terminaison, par exemple
`while True`. Elle est utilisée pour des processus daemon/worker, du polling et de la logique
d'event loop.

Arrêt correct :

- une condition `break` claire ;
- la gestion des signaux d'arrêt ;
- des timeouts et `try/finally` pour le nettoyage.

```python
while True:
    task = queue.get()
    if task is None:
        break
    handle(task)
```

**En bref :**

- `while True` est approprié pour des boucles de service de longue durée.
- Un mécanisme d'arrêt contrôlé est nécessaire.
- Prévoyez toujours la libération des ressources.

</details>

<details>
<summary>72. Décrivez le fonctionnement des boucles imbriquées en Python. Quels problèmes de performance peuvent apparaître lors de leur utilisation et comment les éviter ?</summary>

#### Python

Une boucle imbriquée est une boucle à l'intérieur d'une autre boucle. Souvent, la complexité devient `O(n*m)`
ou pire, ce qui est critique sur de grands volumes de données.

Optimisations :

- remplacer les recherches dans des listes par `set`/`dict` ;
- sortir les invariants hors de la boucle interne ;
- utiliser des générateurs, `itertools`, la vectorisation ;
- profiler les zones "chaudes".

**En bref :**

- Les boucles imbriquées multiplient rapidement le coût des calculs.
- Les structures de données sont souvent plus importantes que les micro-optimisations.
- Le profilage montre précisément ce qu'il faut optimiser.

</details>

<details>
<summary>73. Qu'est-ce que le structural pattern matching (`match`/`case`) ?</summary>

#### Python

`match/case` (Python 3.10+) est un mécanisme d'analyse de structures de données par motifs.
Il fonctionne avec des littéraux, des types, des séquences, des dictionnaires et des classes.

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

**En bref :**

- `match/case` se lit mieux pour des branchements complexes.
- Il permet de vérifier la forme et d'extraire des données en même temps.
- Il est particulièrement utile pour les protocoles/événements et le parsing de structures.

</details>

<details>
<summary>74. Dans quels cas le pattern matching est-il meilleur que `if`/`elif` ?</summary>

#### Python

`match/case` est meilleur lorsqu'il faut :

- vérifier de nombreuses formes de données mutuellement exclusives ;
- déstructurer des structures imbriquées ;
- éviter de longues chaînes de `if/elif`.

`if/elif` est meilleur pour des conditions booléennes simples et une logique courte.

**En bref :**

- Pour des scénarios structurels, `match/case` est préférable.
- Pour des conditions simples, `if/elif` suffit.
- Le critère de choix est la lisibilité et la maintenance.

</details>

<details>
<summary>75. Qu'est-ce qu'une fonction en Python ?</summary>

#### Python

Une fonction est un bloc de code invocable nommé qui reçoit des arguments, retourne
un résultat et permet d'encapsuler une logique.

```python
def normalize_name(name: str) -> str:
    return name.strip().title()
```

Les fonctions prennent en charge les valeurs par défaut, les arguments nommés, `*args/**kwargs`,
les annotations de types et les décorateurs.

**En bref :**

- La fonction est l'unité de base de la réutilisation du code.
- Elle définit un contrat clair via les paramètres et la valeur de retour.
- Les annotations de types rendent ce contrat explicite.

</details>

<details>
<summary>76. Quels types d'arguments de fonction existent ?</summary>

#### Python

En Python moderne :

- positional-only (`/`) ;
- positional-or-keyword ;
- keyword-only (`*`) ;
- variadic positional (`*args`) ;
- variadic keyword (`**kwargs`).

```python
def f(a, /, b, *, c, **kwargs):
    ...
```

**En bref :**

- Python offre un contrôle souple sur la manière d'appeler une fonction.
- `/` et `*` formalisent le contrat de l'API.
- `*args/**kwargs` sont utiles pour des interfaces extensibles.

</details>

<details>
<summary>77. Que sont les arguments positionnels et nommés ?</summary>

#### Python

Les arguments positionnels sont passés selon l'ordre, les arguments nommés (`keyword`) selon le nom
du paramètre.

```python
def connect(host: str, port: int) -> str:
    return f"{host}:{port}"

connect("localhost", 5432)           # positionnel
connect(host="localhost", port=5432) # nommé
```

**En bref :**

- Les arguments positionnels dépendent de l'ordre des paramètres.
- Les arguments nommés améliorent la lisibilité de l'appel.
- Ils peuvent être combinés en respectant les règles de la signature.

</details>

<details>
<summary>78. Que sont les arguments par défaut et quels problèmes peuvent-ils poser ?</summary>

#### Python

Les arguments par défaut sont utilisés si aucune valeur n'est passée lors de l'appel.
Ils sont évalués **une seule fois** lors de la définition de la fonction.

Problème : mutable default.

```python
def add_item(item: int, bucket: list[int] | None = None) -> list[int]:
    if bucket is None:
        bucket = []
    bucket.append(item)
    return bucket
```

**En bref :**

- Les valeurs par défaut sont pratiques pour des valeurs stables.
- Un mutable default peut accumuler de l'état entre les appels.
- Le pattern sûr : `None` + initialisation à l'intérieur.

</details>

<details>
<summary>79. Expliquez le rôle et l'utilisation de `*args` et `**kwargs` dans les fonctions Python. Quelle est leur différence ?</summary>

#### Python

`*args` rassemble les arguments positionnels supplémentaires dans un `tuple`. `**kwargs` rassemble
les arguments nommés supplémentaires dans un `dict`.

```python
def log_event(event: str, *args: object, **kwargs: object) -> None:
    ...
```

Usages : wrappers, adaptateurs d'API, décorateurs, relais de paramètres.

**En bref :**

- `*args` = arguments positionnels supplémentaires.
- `**kwargs` = arguments nommés supplémentaires.
- Ils rendent les fonctions flexibles, mais demandent une validation claire.

</details>

<details>
<summary>80. Comment définir une fonction avec des annotations de types en Python ? Donnez un exemple et expliquez les avantages de cette approche.</summary>

#### Python

Les types sont spécifiés dans la signature des paramètres et dans la valeur de retour.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Avantages :

- meilleure DX (autocomplétion, navigation) ;
- vérification statique dans la CI ;
- contrat explicite pour les autres développeurs.

**En bref :**

- Les annotations de types documentent l'API.
- Elles réduisent le risque d'erreurs d'intégration.
- Elles sont le plus utiles dans les bases de code moyennes et grandes.

</details>

<details>
<summary>81. Que sont les fonctions lambda ?</summary>

#### Python

`lambda` est une fonction anonyme à une seule expression. Elle est généralement utilisée pour
de courts callbacks dans `sorted`, `map`, `filter`.

```python
users = [{"name": "Ada"}, {"name": "Bob"}]
users_sorted = sorted(users, key=lambda u: u["name"])
```

Pour une logique complexe, une fonction `def` classique est préférable.

**En bref :**

- `lambda` est pratique pour de courtes expressions locales.
- Elle est limitée à une seule expression.
- Pour la lisibilité, il vaut mieux placer le code complexe dans une `def`.

</details>

<details>
<summary>82. Quelle est la portée des variables dans une fonction ?</summary>

#### Python

Python utilise la règle LEGB pour rechercher des noms :

- `L`ocal ;
- `E`nclosing (fonctions externes) ;
- `G`lobal (module) ;
- `B`uiltins.

À l'intérieur d'une fonction, une affectation crée une variable locale si `global`
ou `nonlocal` ne sont pas déclarés.

**En bref :**

- La portée détermine où un nom est accessible et modifiable.
- LEGB explique l'ordre de recherche des variables.
- Une mauvaise compréhension de la portée conduit souvent à `UnboundLocalError`.

</details>

<details>
<summary>83. Que sont les variables locales et globales en Python ?</summary>

#### Python

Les variables locales vivent dans le corps d'une fonction. Les variables globales sont définies au niveau
du module.

Pour modifier une globale depuis une fonction, `global` est nécessaire, mais il vaut généralement mieux l'éviter
à cause des dépendances implicites.

**En bref :**

- Les variables locales sont plus sûres pour la maintenance et les tests.
- Les variables globales simplifient l'accès, mais compliquent le contrôle de l'état.
- Il vaut mieux passer les dépendances en paramètres.

</details>

<details>
<summary>84. Quelle est la différence entre les variables locales et nonlocal en Python ?</summary>

#### Python

`nonlocal` est utilisé dans une fonction imbriquée pour modifier une variable du
scope englobant le plus proche (et non du scope global).

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

**En bref :**

- Une variable locale appartient à la fonction courante.
- `nonlocal` modifie l'état d'une fonction externe.
- C'est un mécanisme clé pour un closure avec état.

</details>

<details>
<summary>85. Qu'est-ce que l'unpacking en Python et comment l'applique-t-on lors d'une affectation ?</summary>

#### Python

L'unpacking consiste à décomposer les éléments d'une séquence/structure dans des variables séparées.

```python
x, y = (10, 20)
first, *middle, last = [1, 2, 3, 4]
```

Il fonctionne aussi avec les dictionnaires dans `match/case`, les appels de fonctions et les boucles.

**En bref :**

- L'unpacking rend le code plus compact et plus lisible.
- Il prend en charge la capture "avec étoile" du reste des valeurs.
- Il est souvent utilisé dans le parsing de structures de données.

</details>

<details>
<summary>86. Expliquez la notion de packing de valeurs en Python et donnez des exemples.</summary>

#### Python

Le packing consiste à rassembler plusieurs valeurs dans une seule structure (`tuple`, `list`, `dict`).

```python
point = 10, 20                 # tuple packing

def collect(*args: int) -> tuple[int, ...]:
    return args
```

`*args` et `**kwargs` sont un exemple typique de packing d'arguments.

**En bref :**

- Le packing rassemble plusieurs valeurs dans un seul conteneur.
- Il est le plus souvent utilisé dans les signatures de fonctions.
- Il se combine bien avec l'unpacking côté appel.

</details>

<details>
<summary>87. À quoi sert l'opérateur `*` dans le packing et l'unpacking ?</summary>

#### Python

Dans les paramètres de fonction, `*` packe les arguments positionnels (`*args`), et lors de l'appel,
il unpacke un iterable en arguments positionnels.

```python
def add(a: int, b: int) -> int:
    return a + b

nums = [2, 3]
add(*nums)  # 5
```

`*` est aussi utilisé dans une affectation pour capturer "le reste" des éléments.

**En bref :**

- `*` est un opérateur universel pour travailler avec les varargs.
- Dans la signature, il packe ; dans l'appel, il unpacke.
- Il réduit le code répétitif lors du passage de données.

</details>

<details>
<summary>88. Qu'est-ce qu'un closure et quel est son lien avec les decorators ?</summary>

#### Python

Un closure est une fonction interne qui "se souvient" des variables du scope englobant même après
la fin de la fonction externe.

Un decorator est généralement implémenté justement via un closure : le wrapper conserve une référence à
la fonction d'origine et à des paramètres supplémentaires.

**En bref :**

- Un closure est une fonction + un contexte capturé.
- Un decorator est souvent une application pratique d'un closure.
- Il permet d'ajouter un comportement sans modifier le corps de la fonction.

</details>

<details>
<summary>89. Qu'est-ce qu'un decorator en Python et comment fonctionne-t-il ?</summary>

#### Python

Un decorator est un callable qui reçoit une fonction/une classe et retourne une version modifiée
(un wrapper).

```python
from functools import wraps

def log_calls(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Usages : logging, mise en cache, autorisation, retries, métriques.

**En bref :**

- Un decorator ajoute un comportement transverse.
- Il fonctionne en enveloppant un callable.
- Il évite de dupliquer la logique technique dans le code métier.

</details>

<details>
<summary>90. Peut-on utiliser plusieurs decorators pour une seule fonction ?</summary>

#### Python

Oui, on peut empiler plusieurs decorators. Ils s'appliquent de bas en haut
(celui le plus proche de `def` enveloppe en premier).

```python
@decorator_a
@decorator_b
def handler() -> None:
    ...
```

Équivalent : `handler = decorator_a(decorator_b(handler))`.

**En bref :**

- Plusieurs decorators sont autorisés et courants.
- L'ordre d'application a de l'importance.
- La pile de decorators doit être documentée pour rester claire.

</details>

<details>
<summary>91. Décrivez un problème possible lié à l'ordre des decorators lorsqu'ils sont appliqués à une fonction.</summary>

#### Python

Un ordre incorrect peut changer la sémantique : par exemple, mettre le cache avant un contrôle
d'accès peut mettre en cache un résultat indésirable ou contourner la logique attendue.

Risques typiques :

- le logging voit des arguments déjà modifiés ;
- les retries enveloppent la mauvaise exception ;
- le cache est appliqué avant/après la validation au mauvais endroit.

**En bref :**

- L'ordre des decorators influence le comportement de la fonction.
- C'est une cause fréquente de bugs cachés.
- Pour les chaînes critiques, des tests sur l'ordre d'exécution sont nécessaires.

</details>

<details>
<summary>92. Peut-on créer un decorator à l'aide d'une classe ?</summary>

#### Python

Oui. Une classe-decorator implémente `__call__` pour que son instance se comporte comme une fonction.

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.calls = 0

    def __call__(self, *args, **kwargs):
        self.calls += 1
        return self.func(*args, **kwargs)
```

**En bref :**

- Un decorator peut être implémenté non seulement par une fonction, mais aussi par une classe.
- Une classe est pratique lorsqu'un état interne est nécessaire.
- Le mécanisme clé est `__call__`.

</details>

<details>
<summary>93. Comment définir un decorator qui accepte des paramètres ?</summary>

#### Python

Il faut une structure à trois niveaux : fabrique de decorator -> decorator -> wrapper.

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

**En bref :**

- Un decorator paramétré est une fonction qui retourne un decorator.
- On utilise souvent un closure pour conserver les paramètres.
- Cette approche est pratique pour un comportement configurable.

</details>

<details>
<summary>94. À quoi sert `functools.wraps` dans les fonctions decorator ?</summary>

#### Python

`functools.wraps` copie les métadonnées de la fonction d'origine dans le wrapper : nom,
docstring, module, ainsi que `__wrapped__`.

C'est important pour :

- un débogage et des logs corrects ;
- l'introspection et la documentation ;
- la compatibilité avec les outils qui lisent la signature.

**En bref :**

- `wraps` préserve "l'identité" de la fonction d'origine.
- Sans lui, les fonctions décorées perdent des métadonnées utiles.
- C'est une bonne pratique pour tous les decorators de type wrapper.

</details>

<details>
<summary>95. Comment fonctionnent les dict comprehension, list comprehension et set comprehension ?</summary>

#### Python

Une comprehension crée une collection à partir d'une expression et d'une ou plusieurs boucles, éventuellement avec un filtre.

```python
squares = [x * x for x in range(6)]
mapping = {x: x * x for x in range(6)}
unique = {x % 3 for x in range(10)}
```

Format :

- list : `[expr for x in it if cond]`
- set : `{expr for x in it if cond}`
- dict : `{k_expr: v_expr for x in it if cond}`

**En bref :**

- Une comprehension exprime de façon compacte une transformation de données.
- Elle fonctionne pour `list`, `set`, `dict`.
- Elle donne un code plus propre qu'un ajout manuel dans une boucle.

</details>

<details>
<summary>96. Quels sont les avantages des list comprehensions par rapport aux boucles classiques ?</summary>

#### Python

Avantages :

- code plus court et plus déclaratif ;
- moins de variables auxiliaires ;
- généralement des performances légèrement meilleures sous CPython ;
- risque plus faible d'oublier `append`.

Inconvénient : pour une logique très complexe, une comprehension dégrade la lisibilité.

**En bref :**

- Une list comprehension convient bien aux transformations simples.
- Elle est souvent plus rapide et plus propre qu'une boucle manuelle.
- Pour des branches complexes, un `for` classique est préférable.

</details>

<details>
<summary>97. Pouvez-vous donner un exemple de list comprehension imbriquée ?</summary>

#### Python

Exemple de flatten d'une matrice :

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for row in matrix for item in row]  # [1, 2, 3, 4, 5, 6]
```

Exemple avec condition :

```python
pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
```

**En bref :**

- Une comprehension imbriquée, c'est plusieurs `for` dans une même expression.
- L'ordre des `for` correspond à celui des boucles imbriquées.
- Utilisez-la seulement si l'expression reste lisible.

</details>

<details>
<summary>98. Qu'est-ce qui est plus rapide en Python : une list comprehension ou la création d'une liste à l'aide d'une boucle ?</summary>

#### Python

Dans les scénarios typiques, une list comprehension est légèrement plus rapide qu'une boucle avec `append`, car elle bénéficie
d'un bytecode optimisé et de moins de surcoût.

Important : le gain réel dépend du corps de l'opération ; pour les sections critiques,
il faut donc mesurer (`timeit`, `pyperf`).

**En bref :**

- Souvent plus rapide : la list comprehension.
- La différence peut être faible.
- Pour des décisions de production, basez-vous sur des mesures.

</details>

<details>
<summary>99. Qu'est-ce qu'un iterator en Python ?</summary>

#### Python

Un iterator est un objet qui retourne des éléments séquentiellement et mémorise son état courant.
Il implémente le protocole :

- `__iter__()` retourne lui-même ;
- `__next__()` retourne l'élément suivant ou lève `StopIteration`.

**En bref :**

- Un iterator donne un accès élément par élément sans charger toutes les données.
- C'est la base des `for`, des générateurs et du traitement lazy.
- Une fois épuisé, un iterator ne se "rembobine" pas tout seul.

</details>

<details>
<summary>100. Comment créer un iterator à partir d'un objet itérable avec la fonction `iter()` ?</summary>

#### Python

Appelez `iter(iterable)` pour obtenir un iterator.

```python
items = [10, 20, 30]
it = iter(items)
```

Ensuite, les valeurs sont lues via `next(it)`.

**En bref :**

- `iter()` transforme un iterable en iterator.
- C'est une manière explicite de contrôler l'itération manuellement.
- Elle est utilisée dans le traitement bas niveau de flux de données.

</details>

<details>
<summary>101. À quoi sert la fonction `next()` lorsqu'on travaille avec des iterators ?</summary>

#### Python

`next(iterator[, default])` renvoie l'élément suivant d'un iterator. Lorsque
les éléments sont épuisés, elle lève `StopIteration` ou renvoie `default` si
celui-ci a été fourni.

```python
it = iter([1, 2])
next(it)        # 1
next(it)        # 2
next(it, None)  # None
```

**En bref :**

- `next()` donne un contrôle manuel sur le pas d'itération.
- Sans `default`, la fin du flux provoque `StopIteration`.
- Avec `default`, on peut lire le flux de manière sûre.

</details>

<details>
<summary>102. Peut-on utiliser de façon interchangeable `__next__()` et `__iter__()` avec les fonctions `next()` et `iter()` ?</summary>

#### Python

Oui, mais avec une nuance liée au protocole :

- `iter(obj)` appelle `obj.__iter__()` ;
- `next(it)` appelle `it.__next__()`.

Autrement dit, les fonctions sont l'interface standard vers ces méthodes
dunder et sont généralement utilisées à la place d'un appel direct.

**En bref :**

- `iter()` correspond à `__iter__()`.
- `next()` correspond à `__next__()`.
- Dans le code applicatif, il vaut mieux appeler les fonctions intégrées.

</details>

<details>
<summary>103. Quel est le rôle de `StopIteration` dans la conception des iterators et quand cela se produit-il généralement ?</summary>

#### Python

`StopIteration` signale qu'un iterator est épuisé. La boucle `for`
l'intercepte automatiquement et termine l'itération.

Cela se produit généralement :

- lors d'un appel à `next(it)` après le dernier élément ;
- dans des iterators personnalisés, lorsque les données sont terminées.

**En bref :**

- `StopIteration` est la fin normale du flux.
- Il ne faut pas le journaliser comme une « erreur » dans le flux normal.
- Dans vos propres iterators, il faut le lever correctement.

</details>

<details>
<summary>104. Qu'est-ce qu'un generator et en quoi diffère-t-il d'un iterator ou d'une fonction classique ?</summary>

#### Python

Un generator est un iterator spécial créé par une fonction avec `yield`. Il
génère les valeurs une par une et conserve son état interne entre les appels.

Différences :

- par rapport à une fonction classique : il ne se termine pas par un seul
  `return`, mais fonctionne par « pause / reprise » ;
- par rapport à un iterator manuel : l'implémentation est plus simple, sans
  classe explicite avec `__next__`.

**En bref :**

- Un generator est la manière la plus pratique de faire de la lazy iteration.
- Il demande moins de code qu'une classe iterator personnalisée.
- Il est particulièrement utile pour de grands flux de données.

</details>

<details>
<summary>105. Comment créer une generator function ?</summary>

#### Python

Il faut définir une fonction avec `yield`.

```python
def countdown(start: int):
    current = start
    while current > 0:
        yield current
        current -= 1
```

L'appel `countdown(3)` renvoie un objet generator que l'on peut itérer.

**En bref :**

- La présence de `yield` transforme la fonction en générateur.
- Le generator renvoie les valeurs étape par étape.
- L'état de la fonction est conservé entre les itérations.

</details>

<details>
<summary>106. Comment le mot-clé `yield` rend-il possible le fonctionnement des generators et pourquoi économisent-ils de la mémoire ?</summary>

#### Python

`yield` renvoie la valeur suivante et « fige » le contexte de la fonction
(variables locales, position d'exécution). Le `next()` suivant reprend
l'exécution à partir de ce point.

Économie de mémoire : les données ne sont pas créées entièrement à l'avance,
mais calculées on demand.

**En bref :**

- `yield` met en œuvre la pause et la reprise de l'exécution.
- Un generator prend en charge la lazy evaluation.
- Cela réduit l'empreinte mémoire sur de grands ensembles de données.

</details>

<details>
<summary>107. Quelle est la différence entre `return` et `yield` ?</summary>

#### Python

`return` termine la fonction et renvoie une seule valeur finale. `yield`
renvoie une valeur intermédiaire et conserve l'état pour une reprise ultérieure.

Dans un générateur, `return` signifie la fin de l'itération (`StopIteration`).

**En bref :**

- `return` -> termine la fonction.
- `yield` -> produit les valeurs étape par étape.
- `yield` est utilisé pour le traitement en flux.

</details>

<details>
<summary>108. Qu'est-ce que l'Object-Oriented Programming (OOP) et quels sont ses principaux principes en Python ?</summary>

#### Python

L'OOP est une approche où les données et le comportement sont réunis dans des
objets.

Principes clés :

- encapsulation ;
- héritage ;
- polymorphisme ;
- abstraction.

En Python, l'OOP se combine souvent avec la composition et le duck typing.

**En bref :**

- L'OOP structure le domaine à travers les classes et les objets.
- Python prend en charge l'OOP de manière souple, sans code trop cérémoniel.
- En pratique, la composition vaut souvent mieux qu'un héritage profond.

</details>

<details>
<summary>109. Qu'est-ce qu'une `class` en Python ?</summary>

#### Python

Une `class` est un modèle (blueprint) pour créer des objets avec des attributs
et des méthodes.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name
```

La classe définit la structure et le comportement des futures instances.

**En bref :**

- Une classe décrit les données et les opérations qui leur sont associées.
- Les objets (instances) sont créés à partir d'une classe.
- C'est l'unité de base de la modélisation en OOP.

</details>

<details>
<summary>110. Comment créer un object en Python ?</summary>

#### Python

Un objet est créé en appelant la classe :

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

user = User("Ada")
```

Lors de la création, `__init__` est exécuté pour initialiser l'état.

**En bref :**

- Object = instance d'une classe.
- Création : `instance = ClassName(...)`.
- `__init__` configure les attributs initiaux.

</details>

<details>
<summary>111. Que sont les objets et les attributs ?</summary>

#### Python

Un objet est une instance concrète d'un type ou d'une classe. Un attribut est
une paire nom-valeur liée à l'objet (donnée ou méthode).

```python
user.name       # attribut de données
user.save()     # attribut-méthode
```

**En bref :**

- L'objet stocke un état et un comportement.
- Les attributs décrivent cet état et ce comportement.
- L'accès aux attributs se fait avec la notation par point.

</details>

<details>
<summary>112. Quel rôle joue la méthode `__init__()` dans une classe ?</summary>

#### Python

`__init__` est l'initialiseur d'instance : il est appelé après la création de
l'objet et remplit son état initial.

```python
class Account:
    def __init__(self, owner: str, balance: float = 0.0) -> None:
        self.owner = owner
        self.balance = balance
```

**En bref :**

- `__init__` définit les attributs initiaux de l'objet.
- Il sert de point d'entrée pour configurer l'instance.
- Il ne crée pas l'objet, il l'initialise seulement.

</details>

<details>
<summary>113. À quoi sert le paramètre `self` dans les méthodes d'une classe Python ?</summary>

#### Python

`self` est une référence à l'instance courante ; la méthode l'utilise pour lire
ou modifier les attributs d'instance.

```python
def deposit(self, amount: float) -> None:
    self.balance += amount
```

Le nom `self` n'est pas réservé par la syntaxe, mais c'est le standard
généralement accepté.

**En bref :**

- `self` lie la méthode à un objet concret.
- Les données d'instance sont accessibles via `self`.
- C'est le premier paramètre obligatoire d'une méthode d'instance.

</details>

<details>
<summary>114. Comment définir des méthodes dans une classe ?</summary>

#### Python

Les méthodes sont définies comme des fonctions à l'intérieur de `class`.

```python
class Calculator:
    def add(self, a: int, b: int) -> int:
        return a + b
```

Les types les plus courants sont : instance (`self`), classe
(`@classmethod`, `cls`) et statique (`@staticmethod`, sans `self/cls`).

**En bref :**

- Une méthode est une fonction définie dans le corps d'une classe.
- Le type de méthode est déterminé par le décorateur et la signature.
- La méthode d'instance est la plus utilisée.

</details>

<details>
<summary>115. Expliquez le concept « tout est objet » en Python et donnez des exemples.</summary>

#### Python

En Python, presque tout est un objet : les nombres, les chaînes, les fonctions,
les classes, les modules. Cela signifie que tout possède un type, des
attributs et un comportement.

```python
type(10)          # <class 'int'>
type(len)         # <class 'builtin_function_or_method'>
type(str)         # <class 'type'>
```

**En bref :**

- Un modèle objet unique simplifie le langage.
- Les fonctions et les classes sont aussi des objets de première classe.
- Cela rend Python flexible pour la métaprogrammation.

</details>

<details>
<summary>116. Donnez un exemple de classe avec des méthodes qui effectuent des calculs à partir des attributs.</summary>

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

**En bref :**

- Les méthodes peuvent calculer des valeurs à partir des attributs d'instance.
- Cela encapsule la logique métier dans l'objet.
- L'API de la classe devient auto-explicative.

</details>

<details>
<summary>117. Décrivez une situation où l'utilisation de plusieurs classes peut être nécessaire dans un programme Python.</summary>

#### Python

Quand le domaine comporte plusieurs responsabilités, on les répartit entre
plusieurs classes. Par exemple dans l'e-commerce : `Order`, `OrderItem`,
`PaymentService`, `InventoryService`.

Cela apporte :

- une répartition claire des responsabilités ;
- un couplage plus faible ;
- un remplacement et un test plus simples des composants.

**En bref :**

- Plusieurs classes sont nécessaires pour modéliser un domaine complexe.
- La séparation des responsabilités améliore la maintenabilité.
- La composition de classes est généralement préférable à un « god object ».

</details>

<details>
<summary>118. Quelle est la différence entre une instance method, une class method et une static method ?</summary>

#### Python

- Instance method : reçoit `self` et travaille avec une instance concrète.
- Class method : reçoit `cls` et travaille avec la classe dans son ensemble.
- Static method : ne reçoit ni `self` ni `cls` ; c'est une fonction utilitaire
  dans le namespace de la classe.

**En bref :**

- Instance -> logique liée à l'instance.
- Classe -> logique de classe / constructeurs alternatifs.
- Statique -> logique auxiliaire sans accès à l'état.

</details>

<details>
<summary>119. Qu'est-ce que `@classmethod` en Python et en quoi diffère-t-il des méthodes ordinaires ?</summary>

#### Python

`@classmethod` passe la classe (`cls`) en premier argument, et non l'instance.
Il est souvent utilisé pour les méthodes de fabrique.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

    @classmethod
    def from_email(cls, email: str) -> User:
        return cls(email.split("@")[0])
```

**En bref :**

- `classmethod` fonctionne au niveau de la classe.
- Il est pratique pour les constructeurs alternatifs.
- Il ne nécessite pas d'instance déjà créée.

</details>

<details>
<summary>120. Qu'est-ce que `@staticmethod` dans les classes Python et quand est-il pertinent de l'utiliser ?</summary>

#### Python

`@staticmethod` définit une méthode sans `self` ni `cls` automatiques. Elle
appartient logiquement à la classe, mais ne dépend pas de son état.

```python
class Math:
    @staticmethod
    def clamp(value: int, min_v: int, max_v: int) -> int:
        return max(min_v, min(value, max_v))
```

**En bref :**

- `staticmethod` est une fonction dans le namespace de la classe.
- Utilisez-la pour une logique auxiliaire sans accès aux attributs.
- Elle ne convient pas si l'état de l'instance ou de la classe est nécessaire.

</details>

<details>
<summary>121. Quelle est la différence entre `@classmethod` et `@staticmethod` dans les classes Python ?</summary>

#### Python

La différence se situe dans le premier argument et dans le niveau d'accès :

- `@classmethod` reçoit `cls` et peut travailler avec l'état de la classe ;
- `@staticmethod` ne reçoit rien automatiquement.

`classmethod` est plus souvent utilisé pour les fabriques et les constructeurs
polymorphes, `staticmethod` pour les utilitaires.

**En bref :**

- `classmethod` connaît la classe.
- `staticmethod` est isolé de l'état de la classe et de l'instance.
- Le choix dépend du besoin d'accéder à `cls`.

</details>

<details>
<summary>122. Que sont les attributs d'instance dans les classes Python et en quoi diffèrent-ils des attributs de classe ?</summary>

#### Python

Les attributs d'instance appartiennent à un objet concret (`self.x`). Les
attributs de classe appartiennent à la classe et sont partagés entre toutes les
instances.

```python
class User:
    role = "member"           # class attribute
    def __init__(self, name: str) -> None:
        self.name = name      # instance attribute
```

**En bref :**

- Les attributs d'instance stockent un état individuel.
- Les attributs de classe stockent une configuration commune.
- Les mutations des attributs de classe affectent toutes les instances.

</details>

<details>
<summary>123. Qu'est-ce que `__slots__` en Python ?</summary>

#### Python

`__slots__` limite l'ensemble des attributs autorisés dans une classe et peut
réduire la consommation mémoire en supprimant `__dict__` pour les instances.

```python
class Point:
    __slots__ = ("x", "y")
    def __init__(self, x: int, y: int) -> None:
        self.x = x
        self.y = y
```

**Nuances d'utilisation :**

- **Économie de mémoire :** les objets occupent nettement moins de place, car
  les attributs sont stockés dans un tableau fixe plutôt que dans la table de
  hachage `__dict__`.
- **Vitesse :** l'accès aux attributs définis dans `__slots__` est en général un
  peu plus rapide.
- **Absence de `__dict__` :** vous ne pourrez pas ajouter dynamiquement de
  nouveaux attributs qui ne figurent pas dans `__slots__` (sauf si vous ajoutez
  explicitement `"__dict__"` à la liste).
- **Références faibles :** si vous souhaitez utiliser `weakref`, vous devez
  ajouter explicitement `"__weakref__"` à `__slots__`.

**En bref :**

- `__slots__` est utile pour des millions d'objets légers, par exemple des
  nœuds de graphe.
- Il supprime `__dict__` et `__weakref__` par défaut.
- Il réduit la flexibilité au profit des performances et du contrôle.

</details>

<details>
<summary>124. Que sont les magic methods (méthodes dunder) dans les classes Python et pourquoi les appelle-t-on « magiques » ?</summary>

#### Python

Les méthodes dunder (`__init__`, `__str__`, `__len__`, `__eq__`, ...) sont des
hooks spéciaux que Python appelle automatiquement en réponse aux opérateurs et
aux built-ins.

On les appelle « magiques » parce qu'elles intègrent votre classe dans le
comportement du langage.

**En bref :**

- Les méthodes dunder définissent le comportement protocolaire de l'objet.
- Elles permettent à vos classes de se comporter « comme des types intégrés ».
- Utilisez-les seulement lorsqu'il existe un besoin sémantique clair.

</details>

<details>
<summary>125. À quoi sert la méthode `__del__` ?</summary>

#### Python

`__del__` est un finaliseur qui peut être appelé avant la destruction de
l'objet par le GC. Son comportement n'est pas déterministe ; pour gérer les
ressources, il vaut mieux utiliser des gestionnaires de contexte (`with`) et une
fermeture explicite.

**En bref :**

- `__del__` ne garantit pas une exécution au bon moment.
- N'appuyez pas un nettoyage critique uniquement sur lui.
- L'approche recommandée est `with` / `try-finally`.

</details>

<details>
<summary>126. Donnez un exemple d'utilisation de la méthode magique `__str__` pour définir la représentation textuelle d'une classe personnalisée en Python.</summary>

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

`str(user)` et `print(user)` utiliseront `__str__`.

**En bref :**

- `__str__` fournit une représentation de l'objet compréhensible par un humain.
- Il est utile pour les logs et la sortie CLI.
- Il doit être court et lisible.

</details>

<details>
<summary>127. À quoi servent `__str__` et `__repr__` ?</summary>

#### Python

`__str__` est destiné au lecteur final. `__repr__` est destiné au développeur
et au debug ; il est préférable qu'il soit non ambigu.

`print(obj)` utilise généralement `__str__`, alors que le REPL et `repr(obj)`
utilisent `__repr__`.

**En bref :**

- `__str__` sert à un affichage convivial.
- `__repr__` sert à une représentation technique.
- Une bonne pratique consiste à avoir les deux pour une classe métier.

</details>

<details>
<summary>128. Comment fonctionne l'operator overloading en Python et pourquoi est-ce utile ?</summary>

#### Python

L'operator overloading consiste à implémenter les méthodes dunder des
opérateurs (`__add__`, `__sub__`, `__eq__`, ...) afin que les objets de votre
classe personnalisée prennent en charge les opérateurs.

```python
class Vector2:
    def __init__(self, x: float, y: float) -> None:
        self.x = x
        self.y = y

    def __add__(self, other: "Vector2") -> "Vector2":
        return Vector2(self.x + other.x, self.y + other.y)
```

**En bref :**

- Il offre une syntaxe naturelle pour les types métier.
- Il améliore l'expressivité de l'API.
- Il est important de conserver une sémantique mathématiquement attendue.

</details>

<details>
<summary>129. Qu'est-ce que l'inheritance (héritage) ?</summary>

#### Python

L'héritage permet de créer une classe enfant qui hérite des attributs et des
méthodes d'une classe de base et peut étendre ou redéfinir le comportement.

**En bref :**

- L'héritage favorise la réutilisation du code.
- La classe enfant peut redéfinir les méthodes de la classe de base.
- Une hiérarchie excessive complique la maintenance ; la composition est donc
  souvent préférable.

</details>

<details>
<summary>130. Qu'est-ce que le single inheritance en Python ?</summary>

#### Python

Le single inheritance signifie qu'une classe n'a qu'un seul parent direct.

```python
class Animal:
    ...

class Dog(Animal):
    ...
```

C'est la forme d'héritage la plus simple et généralement la plus lisible.

**En bref :**

- Une classe enfant -> une classe de base.
- Un modèle simple de résolution des méthodes.
- C'est souvent suffisant pour la plupart des modèles métier.

</details>

<details>
<summary>131. Comment implémenter l'héritage dans les classes Python et quelle syntaxe utilise-t-on pour cela ?</summary>

#### Python

Syntaxe : `class Child(Base):`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return "hi"
```

Si vous devez appeler la logique de base, utilisez `super()`.

**En bref :**

- L'héritage est défini entre parenthèses après le nom de la classe.
- La classe enfant reçoit l'API de la classe de base.
- La redéfinition permet d'adapter le comportement.

</details>

<details>
<summary>132. Comment accéder aux membres de la classe de base dans une classe enfant ?</summary>

#### Python

L'accès est possible directement via les attributs et méthodes hérités, ou via
`super()`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return super().greet() + " world"
```

**En bref :**

- Les membres hérités sont disponibles automatiquement dans la classe enfant.
- `super()` appelle correctement la logique de la classe de base.
- C'est important pour étendre le comportement plutôt que le dupliquer.

</details>

<details>
<summary>133. À quoi sert la fonction `super()` dans l'héritage Python et comment l'utiliser ?</summary>

#### Python

`super()` renvoie un proxy vers la classe suivante selon la MRO, afin
d'appeler ses méthodes. Elle est typiquement utilisée dans `__init__` et dans
le cadre du cooperative multiple inheritance.

```python
class Child(Base):
    def __init__(self, value: int) -> None:
        super().__init__()
        self.value = value
```

**En bref :**

- `super()` appelle l'implémentation parente sans nommer explicitement la
  classe.
- Elle aide à préserver la cohérence avec la MRO.
- C'est la manière recommandée de travailler avec l'héritage.

</details>

<details>
<summary>134. Décrivez la fonction `isinstance()` en Python et donnez un exemple de son utilisation.</summary>

#### Python

`isinstance(obj, cls_or_tuple)` vérifie si un objet appartient à un type ou à
l'un de ses sous-types.

```python
isinstance(10, int)                 # True
isinstance(True, int)               # True
isinstance("x", (str, bytes))       # True
```

**En bref :**

- `isinstance` est plus sûr que `type(obj) is ...` dans du code polymorphe.
- Il prend en compte la hiérarchie d'héritage.
- Il prend en charge un tuple de types.

</details>

<details>
<summary>135. Expliquez la fonction `issubclass()` en Python et donnez un exemple de son usage.</summary>

#### Python

`issubclass(Sub, Base)` vérifie si la classe `Sub` est une sous-classe de
`Base`.

```python
class Animal: ...
class Dog(Animal): ...

issubclass(Dog, Animal)  # True
```

**En bref :**

- Cela fonctionne avec des classes, pas avec des instances.
- C'est pratique pour valider une API au niveau des types.
- Cela prend en compte l'héritage transitif.

</details>

<details>
<summary>136. Qu'est-ce que le multiple inheritance (héritage multiple) ?</summary>

#### Python

Le multiple inheritance consiste à faire hériter une classe de plusieurs
classes de base.

```python
class A: ...
class B: ...
class C(A, B): ...
```

Cela offre de la flexibilité, mais exige de la discipline dans la conception
des méthodes et dans l'utilisation de `super()`.

**En bref :**

- Une classe peut hériter d'un comportement provenant de plusieurs sources.
- C'est utile pour une approche par mixins.
- Cela peut compliquer la compréhension de la MRO.

</details>

<details>
<summary>137. Comment fonctionne la MRO (Method Resolution Order) en multiple inheritance ?</summary>

#### Python

La MRO définit l'ordre de recherche des méthodes dans la hiérarchie des
classes. En Python, l'algorithme utilisé est la C3 linearization.

**Diamond Problem (problème du diamant) :** c'est le cas classique où la classe
`D` hérite de `B` et `C`, qui héritent toutes deux de `A`. La MRO garantit que
`A` ne sera consultée qu'après tous ses descendants (`B` et `C`).

```python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass

print(D.mro())
# [D, B, C, A, object]
```

Vous pouvez consulter cet ordre via `ClassName.__mro__` ou `ClassName.mro()`.

**En bref :**

- La MRO détermine dans quelle classe de base prendre une méthode.
- L'ordre est prévisible et formellement défini (C3).
- Grâce à la MRO, Python gère correctement le problème du diamant.
- Pour le cooperative inheritance, toutes les classes doivent appeler
  `super()`.

</details>

<details>
<summary>138. Quels sont les avantages et les inconvénients de l'utilisation du multiple inheritance ?</summary>

#### Python

Avantages :

- réutilisation d'un comportement depuis plusieurs sources ;
- mixins pratiques pour « ajouter » des capacités.

Inconvénients :

- MRO plus complexe ;
- risque de conflits de noms ou de comportement ;
- debug et onboarding plus difficiles.

**En bref :**

- Le MI est puissant, mais exige des règles de conception strictes.
- Pour la plupart des cas, la composition est plus simple.
- Utilisez le MI surtout pour de petits mixins.

</details>

<details>
<summary>139. Que sont les mixins ?</summary>

#### Python

Un mixin est une petite classe dotée d'un comportement additionnel ciblé,
destinée à être combinée par héritage plutôt qu'utilisée seule.

Exemples : `TimestampMixin`, `JsonSerializableMixin`.

**En bref :**

- Un mixin ajoute une seule capacité précise.
- Il n'a généralement pas de cycle de vie complet propre.
- Il se combine bien avec le multiple inheritance.

</details>

<details>
<summary>140. Qu'est-ce que l'encapsulation en Python ?</summary>

#### Python

L'encapsulation consiste à masquer l'implémentation interne derrière une API
publique stable. En Python, cela se fait surtout via des conventions et
`property`, plutôt que via des modificateurs d'accès stricts.

**En bref :**

- Le code client travaille avec l'interface, pas avec les détails.
- L'encapsulation réduit le couplage entre les composants.
- Elle facilite l'évolution de l'implémentation interne sans casser l'API.

</details>

<details>
<summary>141. Quelle est la différence entre les accès public, private et protected ?</summary>

#### Python

En Python, il s'agit surtout de conventions de nommage :

- `public` : `name` — accessible partout ;
- `protected` : `_name` — usage interne par convention ;
- `private` : `__name` — name mangling (`_ClassName__name`), sans protection
  absolue.

**En bref :**

- Python n'a pas de modificateurs d'accès stricts comme Java ou C#.
- `_name` et `__name` sont des signaux d'intention pour les développeurs.
- Le vrai contrôle d'accès se construit par le design de l'API.

</details>

<details>
<summary>142. Qu'est-ce que le polymorphism (polymorphisme) et comment est-il implémenté en Python ?</summary>

#### Python

Le polymorphisme est la capacité à travailler avec différents objets via une
interface commune. En Python, il est souvent implémenté par le duck typing et
les protocoles.

```python
def render(obj) -> str:
    return obj.to_text()
```

Tout objet disposant d'une méthode `to_text` convient.

**En bref :**

- Une interface, plusieurs implémentations.
- En Python, le polymorphisme est souvent comportemental plutôt que
  hiérarchique.
- Cela facilite l'extension du système avec de nouveaux types.

</details>

<details>
<summary>143. Qu'est-ce que l'abstraction en Python ?</summary>

#### Python

L'abstraction consiste à exposer l'API essentielle tout en masquant les détails
d'implémentation inutiles. Le client travaille avec un contrat, pas avec les
étapes internes.

**En bref :**

- L'abstraction réduit la charge cognitive.
- Elle facilite le remplacement d'une implémentation sans changer le code
  client.
- Elle se met en place via des interfaces, des ABC, des protocoles et des
  façades.

</details>

<details>
<summary>144. Comment implémenter la data abstraction ?</summary>

#### Python

Approche :

- masquer l'accès direct aux champs internes (`_field`) ;
- fournir une API contrôlée via des méthodes ou `@property` ;
- valider les invariants dans la logique du setter.

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

**En bref :**

- La data abstraction protège les invariants de l'objet.
- `property` donne un accès contrôlé à l'état.
- Les détails internes peuvent évoluer sans changer l'API.

</details>

<details>
<summary>145. Que sont les ABC et `@abstractmethod` ?</summary>

#### Python

Une ABC (Abstract Base Class) est une classe de base abstraite du module
`abc`. `@abstractmethod` marque une méthode qui doit obligatoirement être
implémentée par une sous-classe.

```python
from abc import ABC, abstractmethod

class Storage(ABC):
    @abstractmethod
    def save(self, data: bytes) -> None:
        ...
```

**En bref :**

- Une ABC formalise le contrat d'une hiérarchie.
- `@abstractmethod` empêche d'instancier une implémentation incomplète.
- C'est utile pour des architectures à plugins ou extensibles.

</details>

<details>
<summary>146. Qu'est-ce qu'une property en Python et comment l'utilise-t-on ?</summary>

#### Python

`property` transforme des méthodes d'accès en une API ressemblant à des
attributs, avec possibilité de validation, de calculs ou de logique lazy.

```python
class User:
    def __init__(self, name: str) -> None:
        self._name = name

    @property
    def name(self) -> str:
        return self._name
```

**En bref :**

- `property` permet de contrôler l'accès sans changer la syntaxe externe.
- Elle convient à la validation et aux valeurs dérivées.
- Elle permet de faire évoluer l'API sans casser les clients.

</details>

<details>
<summary>147. Qu'est-ce que `@property` ?</summary>

#### Python

`@property` est un décorateur pour une méthode getter. Avec `@x.setter` et
`@x.deleter`, il forme un attribut contrôlé.

**En bref :**

- `@property` permet de lire une méthode comme un champ.
- Il aide à encapsuler l'implémentation interne.
- Il est souvent utilisé pour des API backward-compatible.

</details>

<details>
<summary>148. Qu'est-ce qu'un descriptor en Python ?</summary>

#### Python

Un descriptor est un objet qui implémente `__get__`, `__set__` ou `__delete__`
et contrôle l'accès aux attributs d'une autre classe.

`property`, `classmethod` et `staticmethod` fonctionnent via le mécanisme des
descriptors.

**En bref :**

- Un descriptor est un mécanisme bas niveau d'accès aux attributs.
- Il permet de réutiliser une logique de validation ou de proxy pour les
  champs.
- C'est la base de nombreuses techniques de métaprogrammation en Python.

</details>

<details>
<summary>149. Quelle est la différence entre une property et un descriptor ?</summary>

#### Python

`property` est un descriptor prêt à l'emploi et de haut niveau pour un seul
attribut. Un descriptor personnalisé est un mécanisme plus général, réutilisable
dans plusieurs champs ou classes.

**En bref :**

- `property` est plus simple et local.
- Un descriptor est plus flexible et plus réutilisable.
- `property` est en pratique construit sur le protocole des descriptors.

</details>

<details>
<summary>150. Quand vaut-il mieux utiliser une property, et quand un descriptor ?</summary>

#### Python

Utilisez `property` lorsque la logique concerne un ou deux champs d'une classe
concrète. Utilisez un descriptor lorsque la même logique (validation, casting,
initialisation paresseuse) doit être réutilisée dans plusieurs classes.

**En bref :**

- Logique locale d'un champ -> `property`.
- Réutilisation d'une politique d'accès -> descriptor.
- Un descriptor est avantageux dans de grands modèles métier.

</details>

<details>
<summary>151. À quoi servent `setattr()`, `getattr()` et `hasattr()` ? Quelle est la différence entre eux ?</summary>

#### Python

Ce sont des fonctions d'accès dynamique aux attributs :

- `getattr(obj, name[, default])` — lire un attribut ;
- `setattr(obj, name, value)` — définir un attribut ;
- `hasattr(obj, name)` — vérifier sa présence.

```python
value = getattr(user, "email", None)
if not hasattr(user, "active"):
    setattr(user, "active", True)
```

**En bref :**

- `getattr/setattr/hasattr` sont utiles pour travailler dynamiquement avec des
  objets.
- Ils sont utiles dans le code générique, la sérialisation et les adaptateurs.
- Il ne faut pas en abuser pour ne pas perdre en lisibilité.

</details>

<details>
<summary>152. Expliquez le rôle de la méthode `__set_name__` dans les descripteurs Python et donnez un exemple de son utilisation.</summary>

#### Python

`__set_name__(self, owner, name)` est appelée lors de la création de la classe
et informe le descripteur du nom de l'attribut auquel il est lié.

```python
class Field:
    def __set_name__(self, owner, name): self.name = name
```

**En bref :**

- `__set_name__` initialise le descripteur avec le contexte de la classe.
- Il permet de créer des validateurs de champs réutilisables.
- Il s'exécute une seule fois au moment de la création de la classe.

</details>

<details>
<summary>153. Qu'est-ce qu'une `dataclass` et quand faut-il l'utiliser ?</summary>

#### Python

`@dataclass` génère automatiquement le boilerplate (`__init__`, `__repr__`,
`__eq__`). Elle convient aux modèles de données sans comportement complexe.

```python
from dataclasses import dataclass
@dataclass(slots=True)
class User:
    name: str
    active: bool = True
```

**En bref :**

- Une `dataclass` réduit le code des modèles de données.
- C'est un bon choix pour les DTO et les configurations.
- Pour une validation complexe, d'autres outils sont souvent nécessaires.

</details>

<details>
<summary>154. Quelle est la différence entre `dataclass` et Pydantic ?</summary>

#### Python

`dataclass` se concentre sur une description pratique de la structure.
Pydantic ajoute la validation à l'exécution, le parsing et la sérialisation des
données.

**En bref :**

- `dataclass` est plus léger et plus rapide pour les modèles internes.
- Pydantic est meilleur pour les entrées externes et les API.
- Le choix dépend du besoin de validation à l'exécution.

</details>

<details>
<summary>155. Que sont les type hints et à quoi servent-ils ?</summary>

#### Python

Les type hints sont des annotations de type dans les signatures et les
variables, qui forment un contrat explicite. Ils améliorent l'aide de l'IDE et
l'analyse statique.

**En bref :**

- Les type hints améliorent la clarté de l'API.
- Ils permettent de détecter tôt toute une classe d'erreurs.
- Ils restent utiles même dans un langage dynamique.

</details>

<details>
<summary>156. Comment fonctionne la vérification statique des types (`mypy`) ?</summary>

#### Python

`mypy` lit les type hints et analyse le code sans l'exécuter, en vérifiant la
compatibilité des types. Il détecte des erreurs d'intégration avant le runtime.

**En bref :**

- `mypy` apporte à Python une vérification proche du compile-time.
- Il fonctionne particulièrement bien dans la CI.
- Les modes stricts réduisent le nombre de bugs en production.

</details>

<details>
<summary>157. Comment garantir la type safety dans un projet Python ?</summary>

#### Python

- ajouter progressivement des type hints dans l'API publique ;
- activer `mypy` ou `pyright` dans la CI ;
- utiliser `TypedDict`, `Protocol` et les generics ;
- minimiser `Any` et les casts implicites.

**En bref :**

- La type safety est un processus, pas une action ponctuelle.
- Le plus grand effet vient d'un garde-fou de types dans la CI.
- Une augmentation progressive du niveau de strictness fonctionne mieux qu'un
  « big bang ».

</details>

<details>
<summary>158. Qu'est-ce que `TypedDict` ?</summary>

#### Python

`TypedDict` décrit la forme typée d'un dictionnaire : quelles clés sont
attendues et quels sont les types de leurs valeurs.

```python
from typing import TypedDict
class UserPayload(TypedDict): name: str; active: bool
```

**En bref :**

- `TypedDict` type un `dict` avec des clés fixes.
- Il est pratique pour les structures proches de JSON.
- Il est vérifié par l'analyseur statique.

</details>

<details>
<summary>159. Qu'est-ce qu'un `Protocol` dans `typing` ?</summary>

#### Python

`Protocol` décrit un contrat comportemental (structural typing) : un type est
compatible s'il possède les méthodes ou attributs requis, indépendamment de
l'héritage.

**En bref :**

- `Protocol` implémente le duck typing dans le typage statique.
- Il réduit le couplage fort avec des classes concrètes.
- Il est utile pour des API testables et extensibles.

</details>

<details>
<summary>160. Que sont les generics en Python ?</summary>

#### Python

Les generics permettent d'écrire des types et des fonctions paramétrés par
d'autres types. Dans la syntaxe moderne : `class Box[T]: ...`,
`def first[T](...) -> T`.

**En bref :**

- Les generics rendent les types réutilisables.
- Ils renforcent la type safety des collections et des conteneurs.
- Ils réduisent la duplication du code typé.

</details>

<details>
<summary>161. Qu'est-ce que Pydantic et à quoi sert-il ?</summary>

#### Python

Pydantic est une bibliothèque pour décrire des schémas de données avec
validation à l'exécution, conversion de types et sérialisation pratique.

Cas typiques : modèles de requête et de réponse FastAPI, configuration
d'application.

**En bref :**

- Pydantic valide les données externes à l'exécution.
- Il est pratique pour les API et les intégrations.
- Il fournit des erreurs de validation claires et des schémas explicites.

</details>

<details>
<summary>162. Que sont les exceptions en Python ?</summary>

#### Python

Une exception est un objet qui signale une situation erronée ou exceptionnelle
pendant l'exécution du code.

**En bref :**

- Les exceptions interrompent le flux normal.
- Il faut les traiter là où une décision peut être prise.
- Un bon modèle d'erreurs améliore la fiabilité du système.

</details>

<details>
<summary>163. Quels sont les trois types d'erreurs en Python et en quoi diffèrent-ils ?</summary>

#### Python

- Syntax errors : erreurs de syntaxe avant l'exécution ;
- Runtime exceptions : erreurs pendant l'exécution ;
- Logical errors : le code s'exécute, mais le résultat est incorrect.

**En bref :**

- Les erreurs de syntaxe et d'exécution sont détectées par l'interpréteur.
- Les erreurs logiques sont détectées par les tests et la revue.
- Chaque type d'erreur exige une approche de diagnostic différente.

</details>

<details>
<summary>164. Comment utiliser `try`, `except`, `else` et `finally` ?</summary>

#### Python

`try` contient l'opération risquée, `except` traite l'erreur, `else` s'exécute
si aucune erreur n'a eu lieu, et `finally` s'exécute toujours (clean-up).

```python
try: data = load()
except FileNotFoundError: data = {}
else: validate(data)
finally: close_connections()
```

**En bref :**

- Réservez `else` au code du « chemin de succès ».
- Utilisez `finally` pour les ressources et le nettoyage.
- Interceptez des exceptions précises, pas « tout ce qui passe ».

</details>

<details>
<summary>165. Que signifie l'ordre des catégories `except` ?</summary>

#### Python

Les blocs `except` sont vérifiés de haut en bas, donc les exceptions les plus
spécifiques doivent venir d'abord, et les plus générales (`Exception`) à la
fin.

**En bref :**

- L'ordre des `except` influence le gestionnaire qui sera exécuté.
- Un `except` trop large placé en haut « mange » les cas spécifiques.
- C'est critique pour un recovery-flow correct.

</details>

<details>
<summary>166. À quoi sert le mot-clé `assert` dans le code Python ?</summary>

#### Python

`assert` vérifie un invariant et lève `AssertionError` si la condition est
fausse. Il convient aux vérifications internes du développeur, pas à la
validation des entrées utilisateur.

**En bref :**

- `assert` documente que « ceci doit être vrai ».
- Il ne remplace pas la gestion des erreurs en production.
- Utilisez-le pour des contrats dans la logique interne.

</details>

<details>
<summary>167. En quoi `raise` diffère-t-il d'un simple message d'erreur affiché avec `print` en Python ?</summary>

#### Python

`raise` modifie le flux de contrôle et signale l'erreur à l'appelant. `print`
se contente d'afficher du texte et n'arrête pas le scénario erroné.

**En bref :**

- `raise` est un mécanisme de gestion des erreurs, `print` ne l'est pas.
- Les exceptions peuvent être interceptées et journalisées de manière
  centralisée.
- `print` sert au diagnostic, pas au contrat d'erreur.

</details>

<details>
<summary>168. Comment créer une exception personnalisée (custom exception) ?</summary>

#### Python

Créez une classe qui hérite de `Exception` (ou d'une exception de base plus
spécifique).

```python
class InvalidOrderError(Exception):
    pass
```

**En bref :**

- Une exception personnalisée rend les erreurs plus expressives pour le domaine.
- Elle permet d'intercepter précisément les cas voulus.
- Elle est préférable à l'utilisation systématique d'un `ValueError`
  universel.

</details>

<details>
<summary>169. Quelle est l'utilité de créer des custom exceptions en Python et comment améliorent-elles la gestion des erreurs ?</summary>

#### Python

Les exceptions personnalisées forment un modèle d'erreurs explicite du domaine
et séparent les erreurs techniques des règles métier.

**En bref :**

- Elles améliorent la lisibilité et la maintenabilité des gestionnaires.
- Elles donnent une sémantique plus précise dans les logs et les API.
- Elles simplifient les tests de scénarios négatifs.

</details>

<details>
<summary>170. Comment les exceptions sont-elles organisées en Python et quelle est la hiérarchie des classes d'exception ?</summary>

#### Python

La hiérarchie part de `BaseException`. Dans le code applicatif, on travaille
presque toujours avec les descendants de `Exception`.

Branches principales : `ValueError`, `TypeError`, `KeyError`, `OSError`,
`RuntimeError`.

**En bref :**

- Les exceptions forment un arbre de classes.
- Il vaut mieux intercepter des sous-classes spécifiques.
- `BaseException` n'est généralement pas interceptée dans la logique métier.

</details>

<details>
<summary>171. Quelles approches utiliser pour gérer plusieurs exceptions différentes en Python et pourquoi faut-il les traiter séparément ?</summary>

#### Python

Approches :

- des blocs `except` séparés pour chaque type ;
- le regroupement de cas logiquement identiques : `except (A, B):` ;
- des stratégies de recovery distinctes pour chaque catégorie.

**En bref :**

- Des exceptions différentes exigent souvent des actions différentes.
- Un traitement séparé réduit les défauts cachés.
- Les logs deviennent plus précis et plus utiles.

</details>

<details>
<summary>172. Pourquoi faut-il parfois relancer une exception (re-raise) en Python et quand est-ce utile ?</summary>

#### Python

Le re-raise (`raise` sans argument dans un `except`) permet d'ajouter du
contexte (logs, métriques, nettoyage) et de propager la même erreur vers un
niveau supérieur.

**En bref :**

- Le re-raise conserve le traceback initial.
- Il est utile pour une gestion centralisée à un niveau supérieur.
- N'avalez pas les erreurs critiques sans raison.

</details>

<details>
<summary>173. Pourquoi faut-il limiter l'utilisation des blocs try-except dans les programmes Python et quel est l'impact sur les performances ?</summary>

#### Python

`try/except` est nécessaire, mais ne doit pas entourer de grands blocs « au cas
où ». C'est particulièrement coûteux lorsque les exceptions se produisent
souvent (exception-driven flow).

**En bref :**

- Interceptez seulement les erreurs attendues à l'endroit précis.
- Des exceptions fréquentes dégradent les performances et la lisibilité.
- Préférez des vérifications explicites lorsque c'est pertinent.

</details>

<details>
<summary>174. Comment gérer les erreurs lors du travail avec des fichiers ?</summary>

#### Python

Utilisez `with` et interceptez les exceptions concrètes (`FileNotFoundError`,
`PermissionError`, `UnicodeDecodeError`, `OSError`).

```python
try:
    with open(path, "r", encoding="utf-8") as f:
        content = f.read()
except FileNotFoundError:
    ...
```

**En bref :**

- `with` garantit la fermeture du fichier.
- Traitez les erreurs I/O spécifiques.
- Journalisez le contexte (chemin, mode, encodage).

</details>

<details>
<summary>175. Quels sont les modes d'ouverture de fichiers en Python ?</summary>

#### Python

Modes principaux :

- `r` lecture ;
- `w` écrasement ;
- `a` ajout à la fin ;
- `x` création d'un nouveau fichier ;
- `b` mode binaire ;
- `t` mode texte (par défaut) ;
- `+` lecture + écriture.

**En bref :**

- Le mode détermine la sémantique de sécurité et de modification du fichier.
- `w` efface le contenu, `a` conserve l'existant.
- Utilisez `b` pour les données binaires.

</details>

<details>
<summary>176. Pourquoi est-il important de fermer les fichiers après les opérations et que peut-il se passer si un fichier reste ouvert ?</summary>

#### Python

Un fichier ouvert retient un descripteur du système d'exploitation. Si vous ne
le fermez pas :

- fuite de file descriptors ;
- verrous sur les fichiers ou flush incomplet ;
- instabilité dans les processus de longue durée.

**En bref :**

- La fermeture d'un fichier libère les ressources du système.
- `with` automatise une fermeture sûre.
- C'est critique pour les services et les scripts batch.

</details>

<details>
<summary>177. Quelle est la différence entre `read()`, `readline()` et `readlines()` pour lire des fichiers ?</summary>

#### Python

- `read()` lit tout le fichier (ou `n` octets/caractères) ;
- `readline()` lit une seule ligne ;
- `readlines()` lit toutes les lignes dans une liste.

**En bref :**

- `read()` et `readlines()` peuvent être coûteux en mémoire.
- Pour les gros fichiers, mieux vaut itérer avec `for line in file`.
- Le choix dépend du volume et du scénario de traitement.

</details>

<details>
<summary>178. Comment écrire des données dans un fichier en Python et quelle est la différence entre les modes `w` (write) et `a` (append) ?</summary>

#### Python

Écriture :

```python
with open("out.txt", "w", encoding="utf-8") as f:
    f.write("hello\n")
```

`w` réécrit le fichier depuis le début, `a` ajoute le nouveau contenu à la fin.

**En bref :**

- `w` efface les anciennes données.
- `a` conserve le contenu existant.
- Pour les journaux, on utilise généralement `a`.

</details>

<details>
<summary>179. Comment travailler efficacement avec de gros fichiers ?</summary>

#### Python

- lire en streaming (ligne par ligne ou par chunks) ;
- éviter de charger tout le fichier en mémoire ;
- utiliser la mise en mémoire tampon et les générateurs ;
- pour les données tabulaires ou en colonnes, choisir les formats et parseurs
  adaptés.

**En bref :**

- Le point clé : le streaming au lieu du full-read.
- Les générateurs réduisent l'empreinte mémoire.
- L'algorithme de traitement est plus important que les micro-optimisations.

</details>

<details>
<summary>180. Que sont les gestionnaires de contexte ?</summary>

#### Python

Un gestionnaire de contexte gère une ressource via le protocole `__enter__/__exit__` :
ouverture ou initialisation, puis terminaison ou nettoyage garanti.

**En bref :**

- Il fournit un cycle de vie sûr à la ressource.
- Il fonctionne via `with`.
- Il réduit le nombre de fuites de ressources.

</details>

<details>
<summary>181. Comment fonctionne la construction `with` ?</summary>

#### Python

`with` appelle `__enter__` à l'entrée dans le bloc et `__exit__` à la sortie,
même lorsqu'une erreur s'est produite.

```python
with open("data.txt", "r", encoding="utf-8") as f:
    data = f.read()
```

**En bref :**

- `with` garantit le nettoyage.
- Il rend le travail avec les ressources déclaratif.
- Il est recommandé pour les fichiers, les locks, les transactions et les
  sessions.

</details>

<details>
<summary>182. Comment créer son propre gestionnaire de contexte ?</summary>

#### Python

Deux approches :

- une classe avec `__enter__` / `__exit__` ;
- une fonction avec `contextlib.contextmanager`.

```python
from contextlib import contextmanager

@contextmanager
def temp_flag():
    yield
```

**En bref :**

- Une classe convient à un état complexe.
- `contextmanager` est pratique pour des scénarios courts.
- Les deux garantissent un nettoyage sûr.

</details>

<details>
<summary>183. Comment Python gère-t-il la mémoire ?</summary>

#### Python

CPython utilise le reference counting et un garbage collector cyclique. Il
dispose en plus d'un allocateur interne (`pymalloc`) pour les petits objets.

**En bref :**

- Le mécanisme de base est le compteur de références.
- Le GC supprime les références cycliques.
- La mémoire n'est pas toujours libérée instantanément au niveau de l'OS.

</details>

<details>
<summary>184. Qu'est-ce que le reference counting en Python et pourquoi est-ce important pour la gestion de la mémoire ?</summary>

#### Python

Chaque objet possède un compteur de références. Lorsqu'il atteint zéro, l'objet
peut être libéré. Cela permet de libérer rapidement la plupart des objets à
courte durée de vie.

**En bref :**

- Le reference counting donne un cycle de vie prévisible aux objets.
- Il ne résout pas à lui seul les références cycliques.
- Avec le GC, il forme un modèle complet de gestion mémoire.

</details>

<details>
<summary>185. Qu'est-ce que le garbage collection en Python ?</summary>

#### Python

Le garbage collection dans CPython détecte et supprime les cycles d'objets
inaccessibles qui ne peuvent pas être nettoyés par le seul reference counting.

**En bref :**

- Le GC complète le reference counting.
- Il est particulièrement important pour les graphes cycliques de références.
- On peut le contrôler via le module `gc`.

</details>

<details>
<summary>186. Comment obtenir l'adresse mémoire d'un objet en Python ?</summary>

#### Python

Dans CPython, `id(obj)` correspond souvent à l'adresse mémoire de l'objet (sous
forme d'entier). C'est un outil de diagnostic, pas un identifiant externe
stable.

**En bref :**

- `id()` donne l'identité de l'objet.
- Dans CPython, c'est généralement une adresse mémoire.
- Ne l'utilisez pas dans la logique métier.

</details>

<details>
<summary>187. À quoi sert la fonction `getrefcount()` du module `sys` et comment fonctionne-t-elle en Python ?</summary>

#### Python

`sys.getrefcount(obj)` renvoie le compteur de références actuel de l'objet
(dans CPython). La valeur est généralement supérieure de 1 à cause de la
référence temporaire de l'argument.

**En bref :**

- C'est un outil de diagnostic du comportement mémoire.
- Il est utile pour analyser les fuites de références.
- Il ne faut pas s'y fier dans la logique applicative.

</details>

<details>
<summary>188. Expliquez avec des exemples la différence entre objets mutables et immutables du point de vue du reference counting et de la gestion mémoire.</summary>

#### Python

Les objets immutables ne changent pas, donc une « modification » crée un
nouvel objet. Les objets mutables changent in-place, et toutes les références
voient la modification.

```python
a = "x"; b = a; a += "y"   # новий об'єкт
x = [1]; y = x; y.append(2) # зміна того ж об'єкта
```

**En bref :**

- Les objets immutables réduisent les effets de bord.
- Les objets mutables sont plus efficaces pour les modifications in-place.
- La différence est critique pour la copie et le partage de références.

</details>

<details>
<summary>189. Quelle est la différence entre shallow copy et deep copy en Python, et quand utiliser chaque approche ?</summary>

#### Python

Une shallow copy copie seulement le conteneur externe, tandis que les objets
imbriqués restent partagés. Une deep copy copie récursivement toute la
structure.

```python
import copy
copy.copy(obj)
copy.deepcopy(obj)
```

**En bref :**

- Une shallow copy suffit pour les structures « plates ».
- Une deep copy est nécessaire pour travailler de manière isolée avec des
  données mutables imbriquées.
- Une deep copy coûte plus cher en temps et en mémoire.

</details>

<details>
<summary>190. Que sont les modules et les packages en Python ?</summary>

#### Python

Un module est un fichier `.py` distinct contenant du code. Un package est un
répertoire de modules (espace de noms) qui organise le code en blocs plus
grands.

**En bref :**

- Module = unité de code.
- Package = structure pour faire évoluer un ensemble de modules.
- La séparation en modules et packages améliore la maintenabilité.

</details>

<details>
<summary>191. Comment importer un module en Python ?</summary>

#### Python

Formes principales :

- `import module`;
- `import module as m`;
- `from module import name`;
- `from package import submodule`.

**En bref :**

- L'import charge un module et le rend accessible dans le namespace.
- Les alias (`as`) améliorent la lisibilité et évitent les conflits.
- Il vaut mieux privilégier les imports explicites.

</details>

<details>
<summary>192. Quels types d'imports existe-t-il ?</summary>

#### Python

Types courants :

- absolus ;
- relatifs ;
- sélectifs (`from x import y`) ;
- avec alias (`as`) ;
- dynamiques (`importlib`).

**En bref :**

- Le type d'import influence la lisibilité et la maintenance.
- En production, on utilise surtout des imports absolus.
- Les imports dynamiques s'emploient de manière ciblée.

</details>

<details>
<summary>193. Comment fonctionne le système d'import ?</summary>

#### Python

L'interpréteur cherche le module dans `sys.path`, le charge une seule fois et
le met en cache dans `sys.modules`. Un import répété réutilise ce cache.

**En bref :**

- Import = recherche + exécution du module + mise en cache.
- Cela explique pourquoi le code du module s'exécute au premier import.
- Les imports cycliques apparaissent à cause de l'ordre d'initialisation des
  modules.

</details>

<details>
<summary>194. Quelle est la différence entre un import absolu et un import relatif ?</summary>

#### Python

Un import absolu commence depuis la racine du package (`from app.utils import x`).
Un import relatif utilise des points (`from .utils import x`).

**En bref :**

- Les imports absolus sont plus lisibles et plus stables.
- Les imports relatifs sont pratiques à l'intérieur d'un package, mais moins
  bons pour le refactoring.
- Pour les grands projets, il vaut mieux standardiser sur les imports absolus.

</details>

<details>
<summary>195. Que fait la fonction `dir()` et comment peut-on l'utiliser avec des modules ?</summary>

#### Python

`dir(obj)` renvoie la liste des attributs ou noms disponibles sur un objet.
Pour les modules, c'est un moyen rapide d'inspecter l'API.

```python
import math
dir(math)
```

**En bref :**

- `dir()` aide à explorer interactivement les modules.
- Il est utile dans le REPL et pour le debug.
- Il ne remplace pas la documentation officielle.

</details>

<details>
<summary>196. Expliquez le rôle de la construction `if __name__ == "__main__":` dans les scripts Python.</summary>

#### Python

Ce bloc ne s'exécute que lorsque le fichier est lancé comme script, et non
importé comme module. Cela sépare le code réutilisable et le point d'entrée CLI.

**En bref :**

- Il permet d'utiliser le module à la fois comme script et comme import.
- Il évite une exécution non souhaitée lors de l'import.
- C'est un pattern standard pour les scripts.

</details>

<details>
<summary>197. Que signifie le fichier `__init__.py` dans un package Python ?</summary>

#### Python

`__init__.py` marque un répertoire comme package et peut initialiser l'API au
niveau du package, par exemple en réexportant des classes ou des fonctions.

**En bref :**

- Il façonne l'interface publique du package.
- Il peut contenir une initialisation minimale.
- Il ne faut pas le surcharger avec une logique lourde.

</details>

<details>
<summary>198. Quelles sont les best practices pour le style des imports en Python ?</summary>

#### Python

- regrouper les imports : stdlib, third-party, local ;
- éviter `from x import *` ;
- garder les imports au début du fichier, sauf cas justifiés de lazy import ;
- utiliser le tri et le formatage (`ruff`, `isort`).

**En bref :**

- Des imports cohérents améliorent la lisibilité.
- Les imports explicites réduisent les conflits de noms.
- L'automatisation avec des outils élimine les erreurs manuelles.

</details>

<details>
<summary>199. Quels built-in modules populaires existe-t-il en Python ?</summary>

#### Python

Exemples de modules populaires de la bibliothèque standard :

- `os`, `sys`, `pathlib`, `json`, `datetime`, `re`,
- `collections`, `itertools`, `functools`, `typing`,
- `asyncio`, `subprocess`, `logging`, `argparse`.

**En bref :**

- La bibliothèque standard couvre la plupart des tâches de base.
- Cela réduit le nombre de dépendances externes.
- Il vaut mieux bien connaître la stdlib avant d'ajouter des packages tiers.

</details>
<details>
<summary>200. Que savez-vous du package `collections`, et quels autres built-in modules ont été utilisés ?</summary>

#### Python

`collections` fournit des structures de haut niveau :

- `Counter`, `defaultdict`, `deque`, `namedtuple`, `ChainMap`.

Il se combine souvent avec :

- `itertools` pour les pipelines d'itération ;
- `functools` pour le caching et les outils fonctionnels ;
- `pathlib`, `json`, `datetime` dans les tâches applicatives.

**En bref :**

- `collections` étend les conteneurs de base avec des structures pratiques.
- Il améliore souvent la simplicité et les performances du code.
- Il fonctionne bien avec `itertools` et `functools`.

</details>

<details>
<summary>201. Que renvoie `sys.argv` ?</summary>

#### Python

`sys.argv` renvoie une liste d'arguments de ligne de commande :

- `sys.argv[0]` — le nom du script ;
- les autres éléments — les arguments passés.

**En bref :**

- `sys.argv` est l'interface de base des arguments CLI.
- Les valeurs arrivent sous forme de chaînes.
- Pour des CLI plus complexes, mieux vaut utiliser `argparse`.

</details>

<details>
<summary>202. Quel est le module principal pour travailler avec le système d'exploitation en Python ?</summary>

#### Python

Le module principal est `os` (avec `os.path`), et pour une API moderne de
gestion des chemins, `pathlib` est recommandé.

**En bref :**

- `os` donne accès aux API de processus, d'environnement et de système de
  fichiers de l'OS.
- `pathlib` est plus pratique pour travailler avec les chemins.
- Dans les vrais projets, on utilise souvent les deux.

</details>

<details>
<summary>203. Comment mélanger les éléments d'une liste avec le module `random` ?</summary>

#### Python

Utilisez `random.shuffle(list_)` pour un mélange in-place.

```python
import random
items = [1, 2, 3, 4]
random.shuffle(items)
```

**En bref :**

- `shuffle` modifie la liste d'origine.
- Il fonctionne uniquement avec des séquences mutables, comme les listes.
- Pour obtenir une nouvelle copie : `random.sample(items, k=len(items))`.

</details>

<details>
<summary>204. Qu'est-ce qu'un virtual environment ?</summary>

#### Python

Un virtual environment est un environnement Python isolé avec ses propres
packages et versions de dépendances pour un projet donné.

**En bref :**

- L'isolation supprime les conflits de dépendances entre projets.
- L'outil standard est `venv`.
- C'est une pratique de base pour un développement reproductible.

</details>

<details>
<summary>205. Comment fonctionne `pip` ?</summary>

#### Python

`pip` installe, met à jour et supprime des packages depuis des index
(principalement PyPI), résout les dépendances et les installe dans
l'environnement courant.

**En bref :**

- `pip` est le gestionnaire de paquets standard de Python.
- Il fonctionne dans le venv ou l'interpréteur actif.
- Pour la stabilité, il est important d'épingler les versions.

</details>

<details>
<summary>206. Qu'est-ce que `requirements.txt` ?</summary>

#### Python

`requirements.txt` est un fichier contenant la liste des dépendances, souvent
avec des versions exactes, utilisé pour une installation reproductible.

**En bref :**

- Le format est simple et compatible avec `pip install -r`.
- Il vaut mieux fixer des versions exactes pour la production.
- Il est souvent généré par des outils comme `pip-tools` ou `poetry export`
  à partir d'une liste déclarative ou de lock files.

</details>

<details>
<summary>207. Qu'est-ce que `pyproject.toml` et pourquoi est-il devenu un standard ?</summary>

#### Python

`pyproject.toml` est un fichier standardisé de configuration du projet : les
métadonnées du package, le build-system et les réglages d'outils comme `ruff`,
`pytest`, `mypy`, etc.

**En bref :**

- Il centralise la configuration d'un projet Python.
- Il est pris en charge par les outils modernes de packaging.
- Il réduit le nombre de fichiers de configuration dispersés.

</details>

<details>
<summary>208. Comment gérer les dépendances dans un projet Python moderne ?</summary>

#### Python

- isoler l'environnement (`venv`) ;
- définir les dépendances dans `pyproject.toml` ;
- fixer des lock files ou des constraints pour la reproductibilité ;
- mettre à jour régulièrement avec des vérifications en CI.

**En bref :**

- La gestion des dépendances doit être reproductible.
- Ne mélangez pas les packages globaux et ceux du projet.
- Faites les mises à jour de manière contrôlée via les tests.

</details>

<details>
<summary>209. Comment organiser correctement la structure d'un grand projet Python ?</summary>

#### Python

- répartir le code en packages métier ;
- avoir des couches séparées : `api`, `services`, `domain`, `infrastructure` ;
- isoler `tests/`, `scripts/`, `configs/` ;
- maintenir des frontières de modules explicites et une API publique claire.

**En bref :**

- La structure doit refléter le domaine, et non des détails techniques
  accidentels.
- Des frontières claires réduisent les dépendances cycliques.
- Les tests et le tooling doivent être des éléments de première classe dans
  l'arborescence.

</details>

<details>
<summary>210. Quelle est la différence entre les tests automatisés et les tests manuels, et quels sont les avantages des tests automatisés ?</summary>

#### Python

Le test manuel est effectué par une personne pas à pas. Le test automatisé est
exécuté par des scripts ou des frameworks.

**En bref :**

- Les autotests sont rapides, répétables et adaptés à la CI.
- Les tests manuels sont utiles pour les scénarios UX exploratoires.
- En production, une combinaison des deux approches est nécessaire.

</details>

<details>
<summary>211. Qu'est-ce que le TDD (Test-Driven Development) ?</summary>

#### Python

Le TDD suit un cycle : écrire un test qui échoue -> implémentation minimale ->
refactoring.

**En bref :**

- Le TDD façonne l'API à travers les tests.
- Il donne un feedback rapide sur les régressions.
- Il fonctionne le mieux pour une logique métier modulaire.

</details>

<details>
<summary>212. Quels sont les frameworks de test populaires en Python ?</summary>

#### Python

Les plus populaires sont `pytest`, `unittest` (stdlib), ainsi que `hypothesis`
pour les tests basés sur des propriétés.

**En bref :**

- `pytest` est le plus souvent choisi pour les nouveaux projets.
- `unittest` reste utile comme outil standard de base.
- `hypothesis` renforce la couverture des cas limites.

</details>

<details>
<summary>213. Qu'est-ce que `unittest` en Python ?</summary>

#### Python

`unittest` est le framework xUnit intégré pour les tests : classes de cas de
test, méthodes d'assertion, setup/teardown et exécuteur de tests.

**En bref :**

- Il fait partie de la bibliothèque standard.
- Il convient aux environnements conservateurs sans dépendances externes.
- Sa syntaxe est plus « cérémonielle » que celle de pytest.

</details>

<details>
<summary>214. Qu'est-ce que `pytest` et en quoi diffère-t-il de `unittest` par sa syntaxe et ses fonctionnalités ?</summary>

#### Python

`pytest` est un framework avec une syntaxe simple pour les tests fonctionnels,
des fixtures puissantes, la paramétrisation et un écosystème de plugins.

**En bref :**

- `pytest` est moins verbeux et plus pratique pour de grands jeux de tests.
- `unittest` est class-based et standard dans la stdlib.
- Dans les projets modernes, `pytest` domine généralement.

</details>

<details>
<summary>215. Décrivez comment `pytest.raises` est utilisé pour tester l'apparition d'exceptions spécifiques dans du code Python.</summary>

#### Python

`pytest.raises(ExpectedError)` vérifie qu'un bloc de code lève bien
l'exception attendue.

```python
import pytest
with pytest.raises(ValueError):
    int("abc")
```

**En bref :**

- Il teste explicitement les scénarios négatifs.
- Il protège contre un passage « silencieux » des erreurs.
- Il peut aussi vérifier le message ou les attributs de l'exception.

</details>

<details>
<summary>216. Qu'est-ce que la paramétrisation dans les tests et comment pytest la prend-il en charge avec `@pytest.mark.parametrize` ?</summary>

#### Python

La paramétrisation exécute un même test sur plusieurs jeux de données d'entrée.
Dans pytest, cela se fait avec le décorateur `@pytest.mark.parametrize`.

**En bref :**

- Cela réduit la duplication du code de test.
- Il devient facile de faire évoluer les cas.
- La couverture des scénarios d'entrée est plus transparente.

</details>

<details>
<summary>217. Comment définir des noms personnalisés dans pytest pour des tests paramétrés afin d'améliorer la lisibilité ?</summary>

#### Python

Utilisez le paramètre `ids` dans `parametrize`.

```python
@pytest.mark.parametrize("value,expected", [(2, True), (3, False)], ids=["even", "odd"])
```

**En bref :**

- `ids` rend la sortie de l'exécution des tests plus compréhensible.
- Il facilite le diagnostic des échecs.
- C'est particulièrement utile lorsqu'il y a beaucoup de cas.

</details>

<details>
<summary>218. Qu'est-ce que l'étape Arrange/Setup en test, et pourquoi est-ce important ?</summary>

#### Python

Arrange/Setup consiste à préparer l'état du test : données, objets, mocks,
environnement. Un bon setup rend le test déterministe.

**En bref :**

- Un setup instable produit des tests flaky.
- Un bon setup isole le test des effets externes.
- Un Arrange clair améliore la lisibilité du scénario.

</details>

<details>
<summary>219. Que comprend l'étape Cleanup/Teardown et pourquoi est-ce important ?</summary>

#### Python

Le teardown supprime tout ce que le test a créé : fichiers temporaires,
connexions, mocks, enregistrements de test en base de données.

**En bref :**

- Le nettoyage garantit l'isolation entre les tests.
- Il réduit les effets de bord et la flakiness.
- Dans pytest, on le fait facilement via les fixture finalizers et les
  yield-fixtures.

</details>

<details>
<summary>220. Quelle est la différence entre `setUp()` et `setUpClass()` dans unittest ?</summary>

#### Python

`setUp()` s'exécute avant **chaque** méthode de test. `setUpClass()`
(classmethod) s'exécute **une seule fois** avant tous les tests de la classe.

**En bref :**

- `setUp` sert à l'isolation test par test.
- `setUpClass` sert aux ressources partagées coûteuses.
- Un état partagé excessif via `setUpClass` peut compliquer les tests.

</details>

<details>
<summary>221. Qu'est-ce qu'un mock object et comment aide-t-il à améliorer la qualité des tests ?</summary>

#### Python

Un mock object est un objet de substitution qui imite une dépendance et permet
de contrôler le comportement ou de vérifier les appels.

**En bref :**

- Les mocks isolent l'unité des services externes.
- Ils rendent les tests plus rapides et plus stables.
- Ils permettent de vérifier les interactions, pas seulement le résultat.

</details>

<details>
<summary>222. Quelle est la différence entre `mock.patch` dans unittest et `monkeypatch` dans pytest pour le mocking d'objets ?</summary>

#### Python

`mock.patch` de `unittest.mock` patche des objets via leur chemin d'import et
fournit une API riche pour vérifier les appels. `monkeypatch` dans pytest
modifie plus simplement des attributs, des variables d'environnement ou des
dictionnaires pendant le test.

**En bref :**

- `patch` est plus puissant pour les scénarios de mock assertion.
- `monkeypatch` est pratique pour des remplacements de test rapides.
- On les combine souvent selon le cas.

</details>

<details>
<summary>223. Quel est le rôle du paramètre `scope` dans les fixtures pytest ?</summary>

#### Python

`scope` définit le cycle de vie d'une fixture : `function`, `class`, `module`,
`package`, `session`.

**En bref :**

- Un scope plus petit = une meilleure isolation.
- Un scope plus grand = une exécution plus rapide des grands jeux de tests.
- Le choix du scope est un équilibre entre vitesse et indépendance.

</details>

<details>
<summary>224. Qu'est-ce que la complexité d'un algorithme et comment est-elle déterminée ?</summary>

#### Python

La complexité d'un algorithme évalue la croissance du coût en temps et en
mémoire lorsque la taille des données d'entrée `n` augmente.

**En bref :**

- On mesure la complexité temporelle et spatiale.
- L'évaluation est généralement asymptotique.
- Cela aide à choisir l'algorithme et les structures de données.

</details>

<details>
<summary>225. Expliquez la notation Big O et son importance dans l'évaluation de la complexité des algorithmes.</summary>

#### Python

Big O décrit la borne supérieure de croissance du coût d'un algorithme lorsque
`n` devient grand, en ignorant les constantes et les termes inférieurs.

**En bref :**

- Big O montre le passage à l'échelle, pas le temps exact.
- Elle fournit un langage pour comparer les algorithmes.
- Elle est cruciale pour les performances sur de grands volumes.

</details>

<details>
<summary>226. Quels types de complexité algorithmique rencontre-t-on le plus souvent ?</summary>

#### Python

Les plus fréquents sont : `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`, `O(n^2)`.

**En bref :**

- `O(n)` et `O(n log n)` sont les plus courants dans les tâches applicatives.
- `O(n^2)` et au-delà deviennent souvent un goulot d'étranglement.
- Il faut considérer la mémoire, pas seulement le temps.

</details>

<details>
<summary>227. Donnez des exemples de problèmes efficacement résolus par des algorithmes linéaires (O(n)).</summary>

#### Python

Exemples :

- recherche du maximum ou du minimum ;
- filtrage d'éléments ;
- comptage de fréquences avec `Counter` ;
- vérification de conditions pour chaque élément.

**En bref :**

- O(n) signifie un seul parcours des données.
- C'est optimal pour de nombreuses agrégations.
- Les algorithmes linéaires passent bien à l'échelle.

</details>

<details>
<summary>228. Comment fonctionne `lru_cache` et quand faut-il l'utiliser ?</summary>

#### Python

`functools.lru_cache` met en cache les résultats d'une fonction selon ses
arguments et renvoie la valeur déjà calculée lors des appels répétés.

**En bref :**

- Il est efficace pour des fonctions pures avec des entrées répétées.
- Il ne convient pas aux fonctions ayant des effets de bord.
- `maxsize` contrôle la taille du cache en mémoire.

</details>

<details>
<summary>229. Comment profiler les performances d'un code Python ?</summary>

#### Python

Outils de base :

- `timeit` pour les micro-mesures ;
- `cProfile` / `pstats` pour un profil au niveau des appels ;
- `py-spy` / `scalene` pour une analyse proche de la production.

**En bref :**

- N'optimisez qu'après avoir mesuré.
- Profilez des scénarios de charge réalistes.
- Fixez une baseline avant et après les changements.

</details>

<details>
<summary>230. Quels sont les principaux moyens d'optimiser du code Python ?</summary>

#### Python

- choisir les bonnes structures de données ;
- réduire la complexité asymptotique ;
- éviter les copies inutiles ;
- utiliser des générateurs et des pipelines lazy ;
- mettre en cache les calculs coûteux ;
- déplacer les chemins critiques vers C, Rust ou NumPy si nécessaire.

**En bref :**

- Le plus grand gain vient de l'algorithme, pas d'un tweak syntaxique.
- L'optimisation doit s'appuyer sur le profiling.
- Il ne faut pas sacrifier la lisibilité sans bénéfice mesuré.

</details>

<details>
<summary>231. Quand faut-il utiliser des C extensions ou PyPy ?</summary>

#### Python

Les C extensions sont pertinentes pour des points chauds CPU très ciblés et
l'intégration avec des bibliothèques natives. PyPy est pertinent lorsque du
code pure Python de longue durée bénéficie du JIT.

**En bref :**

- C extension : performances maximales au prix d'une complexité de build.
- PyPy : gain potentiel sans réécriture en C.
- Le choix doit se faire sur la base de benchmarks de votre charge réelle.

</details>

<details>
<summary>232. Qu'est-ce que le memory profiling ?</summary>

#### Python

Le memory profiling consiste à mesurer où et combien de mémoire le code
consomme au fil du temps afin d'identifier les fuites et les zones coûteuses.

**En bref :**

- Il met en évidence les points chauds mémoire et les pics.
- Il est utile pour les traitements batch et les charges de données.
- Outils : `tracemalloc`, `memory_profiler`, `scalene`.

</details>

<details>
<summary>233. Qu'est-ce que le GIL (Global Interpreter Lock) ?</summary>

#### Python

Le GIL est un mécanisme de CPython qui permet à un seul thread d'exécuter du
bytecode Python à la fois dans un processus.

**En bref :**

- Le GIL affecte le multithreading CPU-bound.
- Pour les tâches I/O-bound, les threads restent utiles.
- Pour le parallélisme CPU, on utilise plus souvent le multiprocessing.

</details>

<details>
<summary>234. Comment le GIL de Python affecte-t-il la concurrency dans CPython et quelles conséquences cela a-t-il pour le multithreading ?</summary>

#### Python

À cause du GIL, les threads dans CPython n'exécutent pas le bytecode Python
réellement en parallèle pour du code CPU-bound. Ils se relaient de manière coopérative.

Conséquences :

- pour les threads I/O-bound, l'effet est positif car l'attente I/O se
  recouvre ;
- pour les tâches CPU-bound, le gain des threads est généralement limité.

**En bref :**

- Le GIL limite le parallélisme des threads dans les scénarios CPU-bound.
- Les threads restent utiles pour le réseau et le disque.
- Pour le CPU, utilisez des processus ou du calcul natif.

</details>

<details>
<summary>235. Comment le GIL affecte-t-il les performances ?</summary>

#### Python

Le GIL gêne peu les tâches I/O-bound, mais il freine le throughput du code
Python multithreadé CPU-bound dans un seul processus.

**En bref :**

- L'effet du GIL dépend du type de charge.
- CPU-bound + threads dans CPython passe souvent mal à l'échelle.
- L'architecture doit être choisie selon le profil des tâches.

</details>

<details>
<summary>236. Expliquez le threading en Python et en quoi il diffère du multiprocessing.</summary>

#### Python

`threading` lance plusieurs threads dans un même processus avec une mémoire
partagée. `multiprocessing` lance des processus séparés avec des mémoires
distinctes.

**En bref :**

- Les threads sont plus légers et pratiques pour l'I/O-bound.
- Les processus offrent un vrai parallélisme CPU.
- Les processus ont un surcoût plus élevé de création et d'IPC.

</details>

<details>
<summary>237. Quand utiliser multiprocessing plutôt que threading ?</summary>

#### Python

Lorsque la tâche est CPU-bound et nécessite plusieurs cœurs dans CPython.
Exemples : parsing intensif, traitement d'images ou de vidéo, calculs numériques.

**En bref :**

- CPU-bound -> généralement `multiprocessing`.
- I/O-bound -> généralement `threading` ou `asyncio`.
- Tenez compte du coût de sérialisation entre les processus.

</details>

<details>
<summary>238. Quelle est la différence entre concurrency et parallelism en programmation, et quand utiliser l'un ou l'autre ?</summary>

#### Python

La concurrency est le chevauchement de tâches dans le temps. Le parallelism
est l'exécution physique simultanée de tâches sur plusieurs cœurs.

**En bref :**

- La concurrency est utile pour les latences I/O.
- Le parallelism est nécessaire pour les calculs intensifs en CPU.
- En Python, le choix de l'outil dépend du type de goulot d'étranglement.

</details>

<details>
<summary>239. Qu'est-ce que la concurrency en Python ?</summary>

#### Python

La concurrency en Python est l'organisation de l'exécution de plusieurs tâches
afin qu'elles progressent ensemble, via des threads, asyncio ou des processus.

**En bref :**

- Il s'agit de gérer de nombreuses tâches, pas forcément en parallèle.
- Elle permet d'augmenter le débit des scénarios I/O.
- Elle demande une conception soignée de la synchronisation et de l'annulation.

</details>

<details>
<summary>240. Quelle est la différence entre les tâches IO-bound et CPU-bound ?</summary>

#### Python

Les tâches IO-bound attendent surtout le réseau, le disque ou la base de
données. Les tâches CPU-bound passent surtout du temps dans les calculs du
processeur.

**En bref :**

- L'IO-bound passe bien à l'échelle via asyncio ou les threads.
- Le CPU-bound passe mieux à l'échelle via multiprocessing ou du code natif.
- Identifiez d'abord le goulot d'étranglement par le profiling.

</details>

<details>
<summary>241. À quoi sert le module `asyncio` en Python et comment permet-il de mettre en œuvre la programmation asynchrone ?</summary>

#### Python

`asyncio` fournit un event loop, l'ordonnancement des tâches et des primitives asynchrones
pour une concurrence coopérative dans les tâches I/O-bound.

**En bref :**

- Il permet de gérer efficacement de nombreuses opérations I/O.
- Il repose sur `async` / `await`.
- Il convient bien aux services et clients réseau.

</details>

<details>
<summary>242. Quelle est la différence entre programmation synchrone et asynchrone en Python ?</summary>

#### Python

Synchrone : un appel bloque le thread courant jusqu'à sa fin. Asynchrone :
`await` rend la main à l'event loop pendant que l'opération attend l'I/O.

**En bref :**

- L'async réduit le temps d'inactivité pendant l'I/O.
- Le sync est plus simple pour une logique linéaire.
- L'async ajoute de la complexité dans la gestion des tâches et de la
  cancellation.

</details>

<details>
<summary>243. Que sont `async` / `await` ?</summary>

#### Python

`async def` définit une fonction coroutine. `await` suspend la coroutine
jusqu'à ce que l'awaitable soit prêt et rend le contrôle à la loop.

**En bref :**

- C'est la syntaxe du modèle asynchrone coopératif.
- Elle s'utilise avec `asyncio` et les bibliothèques async.
- `await` n'est possible qu'à l'intérieur d'un `async def`.

</details>

<details>
<summary>244. Comment fonctionne `asyncio` ?</summary>

#### Python

`asyncio` exécute un event loop qui traite les tâches (coroutines), en basculant
aux points `await` et en planifiant les opérations I/O prêtes.

**Règle critique :** l'event loop fonctionne dans un seul thread. Toute
opération bloquante (`time.sleep()`, requêtes synchrones via `requests`,
calculs lourds) arrête **toute** la boucle et toutes les autres tâches.

**En bref :**

- Un seul thread peut servir de nombreuses tâches I/O grâce à la coopération.
- L'ordonnancement n'est pas préemptif.
- Les appels bloquants détruisent les performances d'asyncio.

</details>

<details>
<summary>245. Qu'est-ce qu'un event loop ?</summary>

#### Python

L'event loop est un ordonnanceur qui surveille les événements et la disponibilité
de l'I/O, puis lance les callbacks ou coroutines correspondants.

**En bref :**

- C'est le composant central du modèle asyncio.
- Il gère le cycle de vie des tâches async.
- Il détermine quand chaque coroutine reprend son exécution.

</details>

<details>
<summary>246. Comment `asyncio` permet-il la programmation asynchrone et quels sont les principaux composants impliqués dans du code asyncio ?</summary>

#### Python

Composants clés :

- event loop ;
- coroutine (`async def`) ;
- task (`asyncio.create_task`) ;
- awaitables (futures, tasks, coroutines) ;
- primitives de synchronisation (`Lock`, `Queue`, `Semaphore`).

**En bref :**

- `asyncio` réunit l'ordonnancement et l'API async dans un modèle unique.
- Les tâches partagent un seul thread d'exécution de manière coopérative.
- L'architecture doit prendre en compte les timeouts, le retry et la
  cancellation.

</details>

<details>
<summary>247. Quand `asyncio` n'apporte-t-il pas d'avantage ?</summary>

#### Python

Lorsque la charge est CPU-bound ou que les bibliothèques principales sont
bloquantes et n'ont pas d'API async. Cela ne se justifie pas non plus pour des
scripts simples et courts.

**Solution pour le code bloquant :** si vous devez utiliser une bibliothèque
bloquante dans un environnement async, utilisez
`loop.run_in_executor(None, sync_func)`, qui l'exécutera dans un thread séparé
sans bloquer l'event loop.

**En bref :**

- L'async n'accélère pas les calculs purs.
- Sans bibliothèques I/O non bloquantes, le gain est minimal.
- `run_in_executor` aide à intégrer du code legacy ou sync.
- La complexité de l'async doit être justifiée par la charge.

</details>

<details>
<summary>248. Comment fonctionne l'annulation dans asyncio ?</summary>

#### Python

L'annulation d'une tâche (`task.cancel()`) lève `CancelledError` dans la
coroutine. Le code doit gérer correctement le nettoyage dans `try/finally`.

**En bref :**

- La cancellation fait partie du flux de contrôle normal en async.
- Il faut intégrer sa gestion dans le design des coroutines.
- L'ignorer conduit à des tâches « bloquées ».

</details>

<details>
<summary>249. Qu'est-ce que `contextvars` ?</summary>

#### Python

`contextvars` fournit des variables locales au contexte, sûres pour des
scénarios async ou multithread. C'est utile pour les request-id,
correlation-id ou tenant-context.

**En bref :**

- C'est une alternative à l'état global dans du code concurrent.
- La valeur est isolée par contexte.
- Cela améliore le traçage et l'observability.

</details>

<details>
<summary>250. Quelles best practices faut-il appliquer lors de l'écriture de code Python ?</summary>

#### Python

- respecter PEP 8 et automatiser le formatage ;
- écrire des type hints explicites pour l'API publique ;
- utiliser `with` pour les ressources ;
- couvrir la logique métier par des tests ;
- éviter l'optimisation prématurée et profiler ;
- garder les modules petits avec une responsabilité claire ;
- gérer les dépendances via `pyproject.toml` + une stratégie de lock.

**En bref :**

- La lisibilité et la prévisibilité sont plus importantes que les « astuces ».
- La qualité repose sur l'automatisation : lint, types, tests, CI.
- La simplicité architecturale réduit le coût de maintenance.

</details>
