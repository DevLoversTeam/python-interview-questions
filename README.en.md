**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

# Python <img src="./assets/python.svg" width="40" height="40" alt="Python logo"/>

## The Most Popular Python Interview Questions and Answers

<details>
<summary>1. What is Python and what are its main features?</summary>

#### Python

**Python** is a high-level general-purpose language focused on readability, fast
development, and a large standard toolkit.

Main features:

- **Simple syntax**: code is easy to read and maintain.
- **Interpreted execution model**: a fast change cycle without a manual
  compilation step.
- **Cross-platform**: the same code runs on Linux, macOS, and Windows.
- **Multi-paradigm**: procedural, OOP, and functional approaches can coexist in
  one project.
- **Strong ecosystem**: `pip`, `venv`, `pyproject.toml`, and thousands of ready
  libraries.
- **Modern Python 3.10+ features**: type hints, `dataclass`, `async/await`,
  `match/case`, generators, and context managers.

Example of a production-style function:

```python
from dataclasses import dataclass

@dataclass(slots=True)
class User:
    name: str
    active: bool

def process_users(users: list[User]) -> list[str]:
    return [user.name for user in users if user.active]
```

**In short:**

- Python speeds up development thanks to its simple syntax and large standard
  library.
- The language is suitable for backend, automation, data/ML, testing, and
  DevOps.
- In Python 3.10+, key practices include type hints, async I/O, and a modern
  standard library.

</details>

<details>
<summary>2. What are Python's key advantages?</summary>

#### Python

Key production advantages of Python:

- high development speed due to concise syntax;
- a large standard library (`pathlib`, `itertools`, `collections`, `asyncio`);
- a mature package ecosystem for backend, data, automation, and testing;
- portability across operating systems;
- strong support for typing (`typing`, `mypy`, `pyright`) and modern practices.

**In short:**

- Python reduces time to market.
- It provides many ready-to-use tools without extra dependencies.
- It works well for both MVPs and scalable services.

</details>

<details>
<summary>3. How is Python different from compiled programming languages?</summary>

#### Python

Python is usually executed by an interpreter: code is compiled to bytecode and
run at runtime inside the CPython VM. In compiled languages such as C/C++ and
Rust, code is typically compiled ahead of time into machine code.

Practical consequences:

- Python is faster for development and prototyping.
- Native compiled languages are usually faster for CPU-bound tasks.
- In Python, performance is often improved through better algorithms, profiling,
  and C extensions.

**In short:**

- Python optimizes for development speed.
- Compilation to machine code usually provides better raw performance.
- The choice depends on the domain and latency/throughput requirements.

</details>

<details>
<summary>4. What does dynamic typing mean in Python?</summary>

#### Python

Dynamic typing means that the type is bound to the object, not to the variable
name. A name can refer to values of different types at different points in
execution.

```python
value = 10        # int
value = "10"      # str
```

Types are checked at runtime, so type errors appear during execution unless a
static type analyzer is used.

**In short:**

- In Python, the object has the type, not the variable.
- The type can change when a name is rebound.
- Type hints add control before code execution.

</details>

<details>
<summary>5. What does strong typing mean in Python?</summary>

#### Python

Strong typing in Python means that the interpreter does not perform unsafe
implicit conversions between incompatible types.

```python
1 + "2"  # TypeError
```

Explicit conversion is required for operations between different types:

```python
1 + int("2")  # 3
```

**In short:**

- Python is dynamically typed but strict about type compatibility.
- Unsafe implicit conversions are blocked with an error.
- Explicit conversion makes behavior predictable.

</details>

<details>
<summary>6. What is a REPL and when is it used?</summary>

#### Python

REPL (Read-Eval-Print Loop) is an interactive mode where you enter an
expression, get the result immediately, and quickly test hypotheses.

Use cases:

- inspect a library API;
- quickly test an expression or algorithm;
- explore data before implementing logic in a module.

Tools: standard `python`, `ipython`, `ptpython`.

**In short:**

- A REPL gives the fastest feedback loop.
- It is convenient for experiments and debugging.
- It does not replace tests, but it shortens idea-validation time.

</details>

<details>
<summary>7. What are literals in Python? Give examples of different literal types.</summary>

#### Python

A literal is a fixed value written directly in code.

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

**In short:**

- Literals are built-in constant values written in code.
- Each basic type has its own literal syntax.
- They are often used to initialize data.

</details>

<details>
<summary>8. What are keywords in Python?</summary>

#### Python

Keywords are reserved words in the language that have a special syntactic
meaning and cannot be used as variable names.

Examples: `if`, `for`, `class`, `def`, `match`, `case`, `try`, `except`,
`async`, `await`.

To view the list:

```python
import keyword
print(keyword.kwlist)
```

**In short:**

- Keywords form Python syntax.
- They cannot be used as identifiers.
- The list is available through the `keyword` module.

</details>

<details>
<summary>9. What is a variable in Python?</summary>

#### Python

A variable in Python is a name, that is, a reference to an object in memory.
Assignment binds a name to an object rather than "putting a value into a box."

```python
x = [1, 2]
y = x
y.append(3)
# x and y refer to the same list
```

**In short:**

- A variable is a reference to an object.
- Multiple names can refer to the same mutable object.
- This matters for understanding copying and side effects.

</details>

<details>
<summary>10. What are `pass` and `...` (Ellipsis) in Python?</summary>

#### Python

`pass` is a placeholder statement: it does nothing, but it allows a
syntactically valid empty block.

`...` (Ellipsis) is a separate object named `Ellipsis`. It is often used as a
marker for "not implemented yet", in type hints, and in libraries such as NumPy.

```python
def feature() -> None:
    pass

PLACEHOLDER = ...
```

**In short:**

- `pass` is used for empty code blocks.
- `...` is an object value, not a keyword.
- Both can be used as temporary placeholders, but with different semantics.

</details>

<details>
<summary>11. What is a PEP and how does it influence Python's development?</summary>

#### Python

A PEP (Python Enhancement Proposal) is an official document that describes a new
feature, standard, or process in the Python ecosystem.

PEPs cover:

- design discussion;
- technical justification;
- an acceptance or rejection decision;
- standardization of practices.

Examples: PEP 8 (style), PEP 484 (type hints), PEP 634 (pattern matching).

**In short:**

- A PEP is the mechanism used to evolve the language and its tooling.
- It makes changes transparent and formalized.
- Many modern Python practices are defined through PEPs.

</details>

<details>
<summary>12. What is PEP 8 and why is it needed?</summary>

#### Python

PEP 8 is the official style guide for Python code: naming, formatting,
indentation, imports, line length, and readability of constructs.

Why it matters:

- code has a consistent style across the team;
- code review becomes faster;
- there is less noise in diffs;
- maintainability improves.

In practice, style is automated through `ruff format` or `black` + `ruff`.

**In short:**

- PEP 8 standardizes Python code style.
- It is about readability and maintenance, not performance.
- Compliance is best automated with tools.

</details>

<details>
<summary>13. What new features appeared in modern Python versions (3.10+)?</summary>

#### Python

Key modern Python features:

- `match/case` (structural pattern matching);
- improved syntax and error messages;
- union types via `|` (`int | None`);
- `typing.Self`, `typing.TypeAlias`, `typing.override`;
- PEP 695-style generics (`class Box[T]: ...`, `def f[T](...) -> ...`);
- `tomllib` in the standard library.

In practice, this reduces boilerplate and improves the reliability of typed
code.

**In short:**

- Python 3.10+ significantly improved syntax and typing.
- `match/case` and modern `typing` have the most visible impact on code.
- New features should be used by default in new code.

</details>

<details>
<summary>14. What is a docstring in Python?</summary>

#### Python

A docstring is a documentation string that appears as the first expression in a
module, class, or function. It is available through `__doc__` and is used by
IDEs, `help()`, and documentation generators.

```python
def normalize_email(email: str) -> str:
    """Return lowercase email without surrounding spaces."""
    return email.strip().lower()
```

It is recommended to describe what the function does, its arguments, return
value, and exceptions.

**In short:**

- A docstring is built-in documentation inside the code.
- It serves as a source for `help()` and autogenerated docs.
- A good docstring reduces the need to read the implementation.

</details>

<details>
<summary>15. How does indentation work in Python?</summary>

#### Python

In Python, indentation defines code blocks such as the body of `if`, `for`,
`def`, and `class`. That means indentation is part of the syntax, not just
style.

```python
if is_ready:
    run_task()
else:
    stop_task()
```

Mixing tabs and spaces can lead to `IndentationError` or an incorrect block
structure.

**In short:**

- Indentation in Python defines program structure.
- Incorrect indentation breaks execution.
- Use a consistent style with 4 spaces.

</details>

<details>
<summary>16. How many spaces should be used for indentation according to PEP 8, and why is consistent indentation important?</summary>

#### Python

PEP 8 recommends **4 spaces** for one indentation level.

Why this is critical:

- the same block structure across the whole project;
- predictable rendering in different editors;
- fewer errors caused by tab/space conflicts;
- cleaner Git diffs.

**In short:**

- The standard indentation is 4 spaces.
- A unified style removes an entire class of formatting errors.
- This directly improves readability and maintainability.

</details>

<details>
<summary>17. What is the difference between `ruff` and `black` in terms of functionality and usage?</summary>

#### Python

`black` is a code formatter with fixed rules.

`ruff` is a fast linter, and also a formatter and autofixer for many rules (PEP
8, imports, potential bugs, syntax simplifications).

Practical approaches:

- either `ruff check --fix` + `ruff format`;
- or `ruff` for linting and `black` for formatting.

**In short:**

- `black` focuses on formatting.
- `ruff` covers linting and some autofixes.
- In modern projects, `ruff` alone is often enough.

</details>

<details>
<summary>18. Explain the purpose of type annotations in Python and provide an example of a function with type annotations.</summary>

#### Python

Type annotations describe the expected types of arguments and return values.
They improve autocompletion, static analysis, and API readability.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Annotations do not perform runtime validation by themselves, but they help find
errors during CI through `mypy` or `pyright`.

**In short:**

- Type hints document the contract of a function.
- They enable early error detection through static checking.
- They improve API quality in large codebases.

</details>

<details>
<summary>19. What is debugging and why is it an important skill for programmers?</summary>

#### Python

Debugging is the systematic process of finding the cause of incorrect code
behavior and removing it. It is not just about "finding a bug," but also
reproducing, isolating, and verifying the fix.

Basic cycle:

- reproduce the problem;
- narrow down the code area;
- verify the hypothesis with logs or a debugger;
- add a test that captures the scenario.

**In short:**

- Debugging reduces MTTR and the number of regressions.
- It works best as a process, not as chaotic searching.
- A complete debugging outcome is: fix + test + post-check.

</details>

<details>
<summary>20. Explain the purpose of using the `print` function for debugging. Give an example of when this approach is useful.</summary>

#### Python

`print` debugging is a quick way to inspect variable values and execution order
without launching more complex tools.

It is useful when you need to quickly verify a hypothesis in a local script:

```python
def parse_port(raw: str) -> int:
    value = raw.strip()
    print(f"raw={raw!r} value={value!r}")
    return int(value)
```

For production code, it is better to switch to `logging` to get log levels and
controlled output.

**In short:**

- `print` is suitable for short local diagnostics.
- It quickly shows variable state at the problematic point.
- For stable diagnostics in services, use `logging`.

</details>

<details>
<summary>21. Describe how Python Debugger (PDB) can be used for debugging. What advantages does PDB have over `print`?</summary>

#### Python

`pdb` lets you pause program execution, step through lines, inspect variable
state, and view the call stack.

Basic usage:

```python
import pdb

def compute(x: int) -> int:
    pdb.set_trace()
    return x * 2
```

Key commands: `n` (next), `s` (step), `c` (continue), `p expr` (print expr), `l`
(list), `bt` (backtrace).

**In short:**

- `pdb` provides interactive execution control.
- It is more effective than `print` for complex scenarios.
- It lets you diagnose state without cluttering code with logs.

</details>

<details>
<summary>22. What strategies can be used to debug loops and functions in Python?</summary>

#### Python

Practical strategies:

- isolate the bug with a minimal reproducible example;
- log invariants during loop iterations;
- place breakpoints at function entry and exit;
- check edge cases such as empty data, `None`, and large inputs;
- cover the problematic path with a test.

For loops, it is useful to log the index and key intermediate states.

**In short:**

- Start by reproducing and narrowing down the problem.
- Check invariants and edge conditions.
- Finalize the fix with a regression-catching test.

</details>

<details>
<summary>23. What impact do long-running functions have on application performance?</summary>

#### Python

Long-running functions increase latency, block workers or threads, and reduce
service throughput.

Risks:

- slow API responses;
- timeouts;
- growing task queues;
- worse CPU/I/O utilization.

Approach: profile with `cProfile`, split work into smaller steps, use generators
or streaming, and move heavy computation to `multiprocessing` or background
workers.

**In short:**

- Long functions directly hurt latency.
- Optimization should be based on profiling, not intuition.
- Architecturally, it is better to separate CPU-bound and I/O-bound work.

</details>

<details>
<summary>24. What is logging and why is it better to use it instead of `print`?</summary>

#### Python

`logging` is the standard mechanism for recording events with levels (`DEBUG`,
`INFO`, `WARNING`, `ERROR`, `CRITICAL`), formats, and handlers such as console
and file output.

Why it is better than `print`:

- configurable verbosity levels;
- structured output;
- centralized configuration;
- integration with an observability stack.

**In short:**

- `logging` is production-ready; `print` is not.
- Log levels let you control noise.
- Logs should be structured and consistent.

</details>

<details>
<summary>25. What is a traceback?</summary>

#### Python

A traceback is the call stack that Python shows when an exception occurs: where
execution started, which functions were called, and where exactly the error
happened.

Uses:

- quickly find the file and line where the error originated;
- understand the execution path that led to the failure;
- build an exact reproduction test.

**In short:**

- A traceback is the "route" to an error.
- The most valuable part is the last stack frames and the exception type.
- Traceback analysis speeds up root-cause discovery.

</details>

<details>
<summary>26. What are the main data types in Python?</summary>

#### Python

Main built-in types:

- numeric: `int`, `float`, `complex`;
- boolean: `bool`;
- strings/bytes: `str`, `bytes`, `bytearray`;
- collections: `list`, `tuple`, `set`, `dict`, `frozenset`;
- special: `NoneType` (`None`).

It is important to understand mutability:

- mutable: `list`, `dict`, `set`, `bytearray`;
- immutable: `int`, `str`, `tuple`, `frozenset`.

**In short:**

- Python has a rich set of basic types out of the box.
- The choice of data structure affects operation complexity.
- Mutability defines copying behavior and side effects.

</details>

<details>
<summary>27. What is the difference between regular division (`/`) and integer division (`//`) in Python?</summary>

#### Python

`/` performs regular division and always returns a `float`.

`//` performs floor division: it rounds down toward `-∞`, and for integer
operands the result is usually an `int`.

```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

**In short:**

- `/` -> floating-point result.
- `//` -> rounded down integer result.
- For negative numbers, `//` is not the same as truncation toward zero.

</details>

<details>
<summary>28. Explain the use of the modulo operator (`%`) in Python. How can it be used to determine whether a number is even or odd?</summary>

#### Python

The `%` operator returns the remainder of a division.

Parity check:

```python
def is_even(n: int) -> bool:
    return n % 2 == 0
```

If `n % 2 == 0`, the number is even; otherwise, it is odd.

Typical use cases include cyclic indices, grouping, and calendar calculations.

**In short:**

- `%` returns the remainder.
- `n % 2` is the standard evenness check.
- It is often used in cyclic logic.

</details>

<details>
<summary>29. How does Python handle large integers and what limitations exist when working with very large numbers?</summary>

#### Python

Python `int` has arbitrary precision, which means it is not limited to 32 or 64
bits as in many other languages.

The limitations are practical:

- process memory;
- computation time for very large values;
- operation cost grows with the number of digits.

**In short:**

- There is no `int` overflow in the usual fixed-size sense.
- The limitation is machine resources, not a fixed bit width.
- For large-number computations, algorithms and profiling matter.

</details>

<details>
<summary>30. Why is handling division by zero important in Python, and how can `ZeroDivisionError` be prevented in code?</summary>

#### Python

Division by zero raises `ZeroDivisionError`. It should be handled explicitly
when the divisor comes from external input or is calculated dynamically.

```python
def safe_div(a: float, b: float) -> float | None:
    if b == 0:
        return None
    return a / b
```

In critical scenarios, use `try/except` and log the context.

**In short:**

- Division by zero is a controlled runtime error.
- The simplest prevention is checking the divisor before the operation.
- For external data, add both protection and diagnostics.

</details>

<details>
<summary>31. Describe the use of the `random` module in Python. What are the most common functions in this module?</summary>

#### Python

`random` is used for pseudorandom values in simulations, test data, and
non-cryptographic tasks.

Common functions:

- `random()` — a number in `[0.0, 1.0)`;
- `randint(a, b)` — an integer in a range;
- `randrange(start, stop, step)` — like `range`, but returns a random element;
- `choice(seq)` / `choices(seq, k=...)`;
- `shuffle(list_)` — shuffles a list in place;
- `sample(population, k)` — a unique sample.

For cryptography, use `secrets`, not `random`.

**In short:**

- `random` is suitable for normal application-level randomness.
- The most common functions are `randint`, `choice`, `shuffle`, and `sample`.
- Security-sensitive tasks require `secrets`.

</details>

<details>
<summary>32. How can you work with numbers more accurately in Python?</summary>

#### Python

For financial and exact decimal calculations, use `decimal.Decimal` instead of
`float`.

```python
from decimal import Decimal

total = Decimal("0.1") + Decimal("0.2")  # Decimal('0.3')
```

For rational numbers, `fractions.Fraction` is useful.

**In short:**

- `float` is convenient, but it has binary representation errors.
- For exact decimal arithmetic, choose `Decimal`.
- The numeric type should match the problem domain.

</details>

<details>
<summary>33. What are escape characters in Python strings and how are they used? Give examples for `\n`, `\t`, `\r`, `\"`, and `\'`.</summary>

#### Python

Escape sequences are special combinations with `\` that encode control
characters inside a string.

- `\n` — newline
- `\t` — tab
- `\r` — carriage return
- `\"` — a double quote inside a string delimited by `"`
- `\'` — a single quote inside a string delimited by `'`

```python
text = "A\tB\n\"quoted\"\nI\'m here\rX"
```

**In short:**

- Escape characters control string formatting.
- They let you include quotes without breaking syntax.
- For paths and regex, raw strings like `r"..."` are often convenient.

</details>

<details>
<summary>34. Explain the use of `strip`, `lstrip`, and `rstrip` in Python. How do they differ?</summary>

#### Python

These methods work on the edges of a string:

- `strip()` removes characters from both sides;
- `lstrip()` only from the left;
- `rstrip()` only from the right.

By default, they remove whitespace, or a specific set of characters:

```python
"  hello  ".strip()      # "hello"
"--id--".strip("-")      # "id"
```

**In short:**

- The `strip` family does not modify a string in place; it returns a new one.
- The difference is only which side gets trimmed.
- They are often used on input data.

</details>

<details>
<summary>35. Describe the purpose of the `count` method on strings. How does it work?</summary>

#### Python

`str.count(sub[, start[, end]])` counts the number of non-overlapping
occurrences of substring `sub` in the selected range.

```python
"banana".count("an")      # 2
"banana".count("a", 2)    # 2
```

It returns `0` if there are no occurrences.

**In short:**

- `count` quickly returns the number of substring occurrences.
- It supports restricting the search through `start/end`.
- It counts non-overlapping matches.

</details>

<details>
<summary>36. How does the `join` method work in Python and what is it most commonly used for?</summary>

#### Python

`sep.join(iterable)` joins a sequence of strings into one string using separator
`sep`.

```python
names = ["Ada", "Linus", "Guido"]
result = ", ".join(names)  # "Ada, Linus, Guido"
```

Typical uses include building CSV-like lines, logs, SQL fragments, URL paths,
and messages.

**In short:**

- `join` is the standard and efficient way to concatenate strings.
- It is called on the separator, not on the list.
- It is more efficient than repeated `+=` inside a loop.

</details>

<details>
<summary>37. What is slicing in Python and how can it be used to get substrings? Give examples with positive and negative indices.</summary>

#### Python

Slicing is selecting part of a sequence with `[start:stop:step]`.

```python
s = "python"
s[1:4]     # "yth"
s[:2]      # "py"
s[-3:]     # "hon"
s[::-1]    # "nohtyp"
```

`start` is included, `stop` is excluded.

**In short:**

- Slicing works for strings, lists, and tuples.
- Negative indices count from the end.
- It is a fundamental tool for sequence processing without loops.

</details>

<details>
<summary>38. Explain the `replace` method for strings. How can it be used to replace multiple occurrences of a substring?</summary>

#### Python

`str.replace(old, new, count=-1)` returns a new string where `old` is replaced
with `new`. By default, all occurrences are replaced.

```python
"foo bar foo".replace("foo", "baz")      # "baz bar baz"
"foo bar foo".replace("foo", "baz", 1)   # "baz bar foo"
```

**In short:**

- `replace` does not modify the string in place.
- Without `count`, it replaces all occurrences.
- `count` lets you control how many replacements are made.

</details>

<details>
<summary>39. How does the `split` method work on strings?</summary>

#### Python

`split(sep=None, maxsplit=-1)` splits a string into a list of substrings.

- without `sep`, it splits on any whitespace;
- with `sep`, it splits on a specific delimiter;
- `maxsplit` limits the number of splits.

```python
"a,b,c".split(",")         # ["a", "b", "c"]
"a b   c".split()          # ["a", "b", "c"]
"k=v=x".split("=", 1)      # ["k", "v=x"]
```

**In short:**

- `split` turns a string into a list of tokens.
- `sep=None` has special behavior for whitespace.
- `maxsplit` is useful for parsing key/value formats.

</details>

<details>
<summary>40. How does type casting work?</summary>

#### Python

Type casting is explicit conversion of a value between types using constructors:
`int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`, `set()`, `dict()`.

```python
age = int("42")
price = float("19.99")
text = str(10)
```

Invalid data raises an exception (`ValueError`, `TypeError`), so external input
requires validation.

**In short:**

- Python provides explicit functions for type conversion.
- Not every value can be safely converted.
- User input requires checks and exception handling.

</details>

<details>
<summary>41. How does Python automatically convert different data types to boolean values?</summary>

#### Python

In a boolean context, Python applies truthiness rules.

Values treated as `False`:

- `False`, `None`;
- zero numbers: `0`, `0.0`, `0j`;
- empty collections: `""`, `[]`, `{}`, `set()`, `tuple()`, `range(0)`.

Everything else is usually `True`.

```python
bool([])      # False
bool("0")     # True
```

**In short:**

- Boolean conversion is based on truthy/falsy rules.
- Empty and zero values become `False`.
- A non-empty string like `"0"` is still `True`.

</details>

<details>
<summary>42. Explain how to convert a string to an integer or a floating-point number in Python. What happens if the string cannot be converted to a number?</summary>

#### Python

Use `int()` and `float()` for conversion:

```python
count = int("42")
ratio = float("3.14")
```

If the string is invalid, Python raises `ValueError`.

```python
def parse_int(value: str) -> int | None:
    try:
        return int(value)
    except ValueError:
        return None
```

**In short:**

- `int()` and `float()` perform explicit conversion from strings.
- An invalid format raises `ValueError`.
- External input should be handled with `try/except`.

</details>

<details>
<summary>43. What does Python do when comparing different data types such as integers and floats, or integers and booleans?</summary>

#### Python

Python allows numeric comparison for compatible numeric types.

- `int` and `float` are compared by value.
- `bool` is a subclass of `int`: `False == 0`, `True == 1`.

```python
1 == 1.0      # True
True == 1     # True
False < 1     # True
```

For incompatible types such as `int` and `str`, ordering comparisons (`<`, `>`)
raise `TypeError`.

**In short:**

- `int`, `float`, and `bool` share numeric semantics.
- `bool` behaves like `0` or `1` in comparisons.
- Incompatible types cannot be compared with ordering operators.

</details>

<details>
<summary>44. How does Python handle comparisons between lists and sets?</summary>

#### Python

`list` and `set` are different types with different semantics, so direct
ordering comparisons between them are not supported.

```python
[1, 2] == {1, 2}   # False
[1, 2] < {1, 2}    # TypeError
```

If you need to compare their elements, normalize the type first:

```python
set([1, 2]) == {1, 2}  # True
```

**In short:**

- `list` and `set` are compared as different data structures.
- `==` between them is usually `False`.
- For meaningful comparison, convert both to the same type first.

</details>

<details>
<summary>45. Describe the use of the `bool()` function in Python.</summary>

#### Python

`bool(x)` returns the boolean value of `x` according to truthiness rules.

Typical use cases:

- explicit conversion of a value to `True` or `False`;
- more readable conditions;
- building filters.

```python
bool("text")   # True
bool("")       # False
bool(0)        # False
```

**In short:**

- `bool()` standardizes empty/non-empty checks.
- It relies on built-in truthy/falsy rules.
- It is useful for validation and conditional logic.

</details>

<details>
<summary>46. What is the difference between `list` and `tuple`?</summary>

#### Python

The main difference is that `list` is mutable, while `tuple` is immutable.

Practical consequences:

- `list` is suitable for data that changes;
- `tuple` is suitable for fixed records;
- `tuple` can be used as a dictionary key if its elements are hashable.

```python
coords: tuple[float, float] = (50.45, 30.52)
queue: list[str] = ["task-1", "task-2"]
```

**In short:**

- `list` is for mutable collections.
- `tuple` is for immutable data structures.
- This choice affects API safety and usage in `dict` and `set`.

</details>

<details>
<summary>47. How can you create a `tuple`?</summary>

#### Python

Main ways:

```python
t1 = (1, 2, 3)
t2 = 1, 2, 3
t3 = tuple([1, 2, 3])
single = (42,)     # the comma is required
empty = ()
```

For a single element, the comma is required. Otherwise, it is just an expression
in parentheses.

**In short:**

- A `tuple` can be created with a literal or `tuple(iterable)`.
- `single = (x,)` is a valid one-element tuple.
- An empty tuple is `()`.

</details>

<details>
<summary>48. What is the difference between the `reverse` method and slicing `[::-1]` when reversing a list?</summary>

#### Python

`list.reverse()` modifies the existing list in place and returns `None`.

`lst[::-1]` creates a new reversed list, which is a copy.

```python
values = [1, 2, 3]
values.reverse()      # values -> [3, 2, 1]

other = values[::-1]  # new list
```

**In short:**

- `reverse()` changes the original.
- `[::-1]` returns a new object.
- The choice depends on whether you need to preserve the original data.

</details>

<details>
<summary>49. Explain the purpose and use of the `sort` method for lists. How do you sort a list in descending order?</summary>

#### Python

`list.sort()` sorts a list in place. It supports these parameters:

- `key` for a sort key function;
- `reverse=True` for descending order.

```python
nums = [5, 1, 7]
nums.sort(reverse=True)  # [7, 5, 1]
```

If you need a new sorted copy, use `sorted(iterable)`.

**In short:**

- `sort()` changes the list in place.
- Use `reverse=True` for descending order.
- `sorted()` is convenient when you need to preserve the original.

</details>

<details>
<summary>50. What is the difference between the `copy` method and directly assigning one list to another? Why is it sometimes important to use `copy`?</summary>

#### Python

Assignment copies only the reference:

```python
a = [1, 2]
b = a
b.append(3)   # a will also change
```

`a.copy()` creates a new shallow list:

```python
a = [1, 2]
b = a.copy()
b.append(3)   # a will not change
```

For nested structures, you may need `copy.deepcopy`.

**In short:**

- `=` does not copy data; it shares the same object between variables.
- `copy()` isolates changes at the top-level list.
- Use `deepcopy` for nested objects.

</details>

<details>
<summary>51. What does the `pop` method do in a list? How does its behavior differ when you specify an index and when you do not?</summary>

#### Python

`pop()` removes and returns an element from a list.

- `pop()` without arguments removes the last element;
- `pop(i)` removes the element at index `i`.

```python
items = ["a", "b", "c"]
last = items.pop()     # "c"
first = items.pop(0)   # "a"
```

An invalid index raises `IndexError`.

**In short:**

- `pop` combines removal and returning a value.
- Without an index, it works on the end of the list.
- With an index, it removes a specific position.

</details>

<details>
<summary>52. How do you combine two lists in Python using the `+` operator and the `extend` method? What is the key difference between these two approaches?</summary>

#### Python

`a + b` creates a **new** list, while `a.extend(b)` modifies list `a` **in
place**.

```python
a = [1, 2]
b = [3, 4]

c = a + b         # [1, 2, 3, 4], a is unchanged
a.extend(b)       # a -> [1, 2, 3, 4]
```

**In short:**

- `+` returns a new object.
- `extend()` mutates the existing list.
- The choice depends on whether you need to preserve the original.

</details>

<details>
<summary>53. What are the functions `min`, `max`, `sum`, `all`, and `any` used for in the context of lists?</summary>

#### Python

These are basic aggregators for iterable collections:

- `min()` / `max()` return the minimum and maximum;
- `sum()` returns the sum of numbers;
- `all()` returns `True` if all elements are truthy;
- `any()` returns `True` if at least one element is truthy.

```python
nums = [3, 10, 1]
min(nums), max(nums), sum(nums)  # (1, 10, 14)
all([True, 1, "x"])              # True
any([0, "", None, 5])            # True
```

**In short:**

- These functions reduce boilerplate in loops.
- They work with any iterable.
- They combine well with generators for lazy processing.

</details>

<details>
<summary>54. What is a dictionary (`dict`) in Python, and how is it different from other data structures?</summary>

#### Python

`dict` is an associative array that stores `key -> value` pairs. Keys must be
hashable, while values can be of any type.

Differences:

- access is by key, not by index;
- average lookup, insertion, and deletion complexity is close to `O(1)`;
- since Python 3.7+, it preserves key insertion order.

**In short:**

- `dict` is optimal for fast key-based access.
- It is the primary structure for configs and mappings.
- Keys must be immutable in practice, meaning hashable.

</details>

<details>
<summary>55. What is the difference between getting a value from a dictionary with square brackets `[]` and using the `get` method?</summary>

#### Python

`d[key]` returns the value or raises `KeyError` if the key does not exist.

`d.get(key, default)` returns the value or `default` (or `None`) without raising
an exception.

```python
config = {"timeout": 30}
config["timeout"]         # 30
config.get("retries", 3)  # 3
```

**In short:**

- `[]` is for required keys.
- `get()` is for optional fields.
- `get()` reduces the need for `try/except` when reading data.

</details>

<details>
<summary>56. Describe how you can update and delete elements in a dictionary.</summary>

#### Python

Updating:

- `d[key] = value` inserts or updates a single key;
- `d.update({...})` performs a bulk update.

Deletion:

- `del d[key]` deletes a key and raises an error if it is missing;
- `d.pop(key, default)` deletes and returns the value;
- `d.popitem()` removes the last key-value pair;
- `d.clear()` clears the entire dictionary.

**In short:**

- `[]` and `update()` are suitable for upsert behavior.
- `pop()` is more common for safe deletion.
- Choose the API based on the behavior you want for missing keys.

</details>

<details>
<summary>57. What are the `keys`, `values`, and `items` methods used for in dictionaries?</summary>

#### Python

These methods return dictionary view objects:

- `keys()` returns all keys;
- `values()` returns all values;
- `items()` returns `(key, value)` pairs.

```python
data = {"a": 1, "b": 2}
for key, value in data.items():
    ...
```

Views are dynamic and reflect the current state of the dictionary.

**In short:**

- `keys/values/items` are used for iteration and checks.
- `items()` is the most convenient for loops over keys and values.
- These are not copies but live views of the data.

</details>

<details>
<summary>58. How is `dict` implemented under the hood in Python?</summary>

#### Python

`dict` is implemented as a hash table with memory and fast-access optimizations.
The key is hashed, a slot is selected from the hash, and collisions are resolved
by an internal probing algorithm.

Practical consequences:

- average access time is close to `O(1)`;
- the quality of `__hash__` and `__eq__` affects behavior;
- mutable objects cannot be used as keys.

**In short:**

- `dict` is a high-performance hash-based structure.
- Its speed comes from hashing.
- Keys must be hashable and stable.

</details>

<details>
<summary>59. What is a hash function?</summary>

#### Python

A hash function converts an object into an integer value, called a hash, which
is used for fast placement and lookup in `dict` and `set`.

Correctness requirements:

- if `a == b`, then `hash(a) == hash(b)`;
- the hash value must remain stable during the object's lifetime.

**In short:**

- A hash function is the foundation of fast `dict` and `set` operations.
- It does not guarantee uniqueness because collisions are possible.
- For custom classes, `__eq__` and `__hash__` must be consistent.

</details>

<details>
<summary>60. What is a `set` in Python, and how is it different from other data structures?</summary>

#### Python

`set` is an unordered collection of **unique** elements.

Differences:

- it automatically removes duplicates;
- it provides fast membership checks with `x in s`;
- it supports set operations such as union, intersection, and difference.

**In short:**

- `set` is optimal for uniqueness and membership checks.
- The order of elements is not guaranteed.
- Elements must be hashable.

</details>

<details>
<summary>61. How do you create a `set` in Python, and what restrictions apply to set elements?</summary>

#### Python

Creation:

```python
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # {1, 2, 3}
empty = set()            # not {}
```

Restrictions:

- elements must be hashable, for example `int`, `str`, or `tuple`;
- `list`, `dict`, and `set` cannot be added directly.

**In short:**

- `set()` creates an empty set.
- Duplicates are removed automatically.
- Only hashable elements are allowed.

</details>

<details>
<summary>62. What is the `intersection()` method used for in a Python set, and how is it different from `union()`?</summary>

#### Python

`intersection()` returns the common elements of sets, while `union()` combines
all unique elements from both sets.

```python
a = {1, 2, 3}
b = {3, 4}

a.intersection(b)  # {3}
a.union(b)         # {1, 2, 3, 4}
```

**In short:**

- `intersection` means overlap, the common part.
- `union` means the full combination of unique elements.
- Both methods are fundamental for comparing data sets.

</details>

<details>
<summary>63. Which data types are immutable?</summary>

#### Python

Common immutable types:

- `int`, `float`, `bool`, `complex`;
- `str`, `bytes`;
- `tuple` if its elements are also immutable;
- `frozenset`;
- `NoneType`.

**In short:**

- An immutable object cannot be changed after creation.
- Instead of mutation, a new object is created.
- These types are safer for `dict` keys and `set` elements.

</details>

<details>
<summary>64. Which data types are mutable?</summary>

#### Python

Common mutable types:

- `list`;
- `dict`;
- `set`;
- `bytearray`;
- most user-defined class objects.

**In short:**

- Mutable objects are changed in place.
- Mutations can create side effects because of shared references.
- You need to be careful with copying.

</details>

<details>
<summary>65. Why is it important to understand mutability when working with dictionaries or sets?</summary>

#### Python

`dict` and `set` are based on hashing, so their keys and elements must be
stable, meaning hashable. Mutable objects cannot be safely used as dictionary
keys or set elements.

Also, mutating values through shared references often leads to unexpected bugs.

**In short:**

- Mutability affects whether keys in `dict` and elements in `set` are valid.
- Shared mutable objects often cause side effects.
- Explicit copies and controlled mutation reduce bugs.

</details>

<details>
<summary>66. What is `None`?</summary>

#### Python

`None` is a special singleton value of type `NoneType` that means "no value" or
"absence of a value".

Typical use cases:

- a function does not explicitly return anything;
- optional parameters;
- a marker that data has not been set yet.

It should be checked with `is`:

```python
if value is None:
    ...
```

**In short:**

- `None` means the absence of a value.
- It is a singleton, so it should be compared with `is`.
- It is often used in APIs as an optional state.

</details>

<details>
<summary>67. What is `id` in Python, how is it used, and why is it important?</summary>

#### Python

`id(obj)` returns the identifier of an object, which is unique during the
object's lifetime in the current process.

It is useful for diagnostics:

- whether this is the same object;
- whether a copy was created;
- whether a shared reference was mutated.

**In short:**

- `id` helps analyze object identity.
- It is useful when debugging copying and mutation issues.
- It should not be used as a business identifier.

</details>

<details>
<summary>68. What is the difference between the `is` and `==` operators?</summary>

#### Python

`==` compares **values** for equality, while `is` compares **identity**, meaning
whether two references point to the same object in memory.

```python
a = [1, 2]
b = [1, 2]
a == b   # True
a is b   # False
```

**Important about optimizations (interning):** CPython caches small integers
from `-5` to `256` and some short strings during compilation or loading. As a
result, `is` may return `True` for them even if they were created separately.
But this is an implementation detail and should not be relied on in business
logic.

Always use `is` for `None`.

**In short:**

- `==` is about value equality.
- `is` is about object identity.
- Interning can cause non-obvious `is True` results for small `int` values and
  strings.
- `value is None` is the correct way to check for `None`.

</details>

<details>
<summary>69. How is the Singleton pattern used in Python? Give examples of singleton objects in Python.</summary>

#### Python

Singleton means one global instance of an object in a process. In Python, it is
often replaced by module-level state because modules are imported only once.

Examples of language-level singleton objects:

- `None`;
- `True` and `False`;
- `Ellipsis`.

In application code, strict Singleton implementations are often replaced with
dependency injection containers or factories for better testability.

**In short:**

- Python already has built-in singleton objects.
- Module scope is often enough without a separate pattern.
- Overusing Singleton makes testing harder.

</details>

<details>
<summary>70. What are the `break` and `continue` operators used for in Python loops?</summary>

#### Python

`break` terminates a loop early, while `continue` skips the current iteration
and moves to the next one.

```python
for n in range(10):
    if n == 5:
        break
    if n % 2 == 0:
        continue
```

**In short:**

- `break` stops the loop completely.
- `continue` skips only the current step.
- They make loop control explicit and readable.

</details>

<details>
<summary>71. Explain the concept of an infinite loop. In what cases is it appropriate to use an infinite loop, and how do you ensure it terminates correctly?</summary>

#### Python

An infinite loop is a loop without a natural termination condition, for example
`while True`. It is used for daemon or worker processes, polling, and event-loop
logic.

Correct termination requires:

- a clear `break` condition;
- handling termination signals;
- timeouts and `try/finally` for cleanup.

```python
while True:
    task = queue.get()
    if task is None:
        break
    handle(task)
```

**In short:**

- `while True` is appropriate for long-running service loops.
- You need a controlled shutdown mechanism.
- Always plan for resource cleanup.

</details>

<details>
<summary>72. Describe how nested loops work in Python. What performance problems can arise when using them, and how can you avoid them?</summary>

#### Python

A nested loop is a loop inside another loop. Its complexity often becomes
`O(n*m)` or worse, which is critical for large data sets.

Optimizations:

- replace list lookups with `set` or `dict`;
- move invariants outside the inner loop;
- use generators, `itertools`, or vectorization;
- profile hot paths.

**In short:**

- Nested loops multiply computational cost quickly.
- Data structures are often more important than micro-optimizations.
- Profiling shows what actually needs optimization.

</details>

<details>
<summary>73. What is structural pattern matching (`match`/`case`)?</summary>

#### Python

`match/case` in Python 3.10+ is a mechanism for matching data structures against
patterns. It works with literals, types, sequences, dictionaries, and classes.

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

**In short:**

- `match/case` reads better for complex branching.
- It lets you validate shape and extract data at the same time.
- It is especially useful for protocols, events, and structured parsing.

</details>

<details>
<summary>74. When is pattern matching better than `if`/`elif`?</summary>

#### Python

`match/case` is better when you need to:

- check many mutually exclusive data shapes;
- unpack nested structures;
- avoid long `if/elif` chains.

`if/elif` is better for simple boolean conditions and short logic.

**In short:**

- `match/case` is better for structural scenarios.
- `if/elif` is enough for simple conditions.
- The selection criterion is readability and maintainability.

</details>

<details>
<summary>75. What is a function in Python?</summary>

#### Python

A function is a named callable block of code that accepts arguments, returns a
result, and encapsulates logic.

```python
def normalize_name(name: str) -> str:
    return name.strip().title()
```

Functions support default values, keyword arguments, `*args`, `**kwargs`, type
annotations, and decorators.

**In short:**

- A function is the basic unit of code reuse.
- It defines a clear contract through parameters and a return value.
- Type hints make that contract explicit.

</details>

<details>
<summary>76. What types of function arguments exist?</summary>

#### Python

In modern Python:

- positional-only (`/`);
- positional-or-keyword;
- keyword-only (`*`);
- variadic positional (`*args`);
- variadic keyword (`**kwargs`).

```python
def f(a, /, b, *, c, **kwargs):
    ...
```

**In short:**

- Python gives flexible control over how a function can be called.
- `/` and `*` formalize the API contract.
- `*args` and `**kwargs` are useful for extensible interfaces.

</details>

<details>
<summary>77. What are positional and keyword arguments?</summary>

#### Python

Positional arguments are passed by order, while keyword arguments are passed by
parameter name.

```python
def connect(host: str, port: int) -> str:
    return f"{host}:{port}"

connect("localhost", 5432)           # positional
connect(host="localhost", port=5432) # keyword
```

**In short:**

- Positional arguments depend on parameter order.
- Keyword arguments improve call readability.
- They can be combined as long as the function signature rules are respected.

</details>

<details>
<summary>78. What are default arguments, and what problems can they cause?</summary>

#### Python

Default arguments are used when a value is not passed during the call. They are
evaluated **once** when the function is defined.

The main problem is a mutable default.

```python
def add_item(item: int, bucket: list[int] | None = None) -> list[int]:
    if bucket is None:
        bucket = []
    bucket.append(item)
    return bucket
```

**In short:**

- Defaults are convenient for stable values.
- A mutable default can accumulate state between calls.
- The safe pattern is `None` plus initialization inside the function.

</details>

<details>
<summary>79. Explain the purpose and use of `*args` and `**kwargs` in Python functions. How are they different?</summary>

#### Python

`*args` collects extra positional arguments into a `tuple`. `**kwargs` collects
extra keyword arguments into a `dict`.

```python
def log_event(event: str, *args: object, **kwargs: object) -> None:
    ...
```

Typical uses include wrappers, API adapters, decorators, and parameter
forwarding.

**In short:**

- `*args` means extra positional arguments.
- `**kwargs` means extra keyword arguments.
- They make functions flexible, but they require clear validation.

</details>

<details>
<summary>80. How do you define a function with type annotations in Python? Give an example and explain the advantages of this approach.</summary>

#### Python

Types are defined in the parameter signature and the return value.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Advantages:

- better developer experience with autocomplete and navigation;
- static checking in CI;
- an explicit contract for other developers.

**In short:**

- Type annotations document the API.
- They reduce the risk of integration errors.
- They provide the most value in medium and large codebases.

</details>

<details>
<summary>81. What are lambda functions?</summary>

#### Python

`lambda` is an anonymous single-expression function. It is usually used for
short callbacks in `sorted`, `map`, and `filter`.

```python
users = [{"name": "Ada"}, {"name": "Bob"}]
users_sorted = sorted(users, key=lambda u: u["name"])
```

For complex logic, a regular `def` function is better.

**In short:**

- `lambda` is convenient for short local expressions.
- It is limited to a single expression.
- For readability, complex logic is better moved into `def`.

</details>

<details>
<summary>82. What is the scope of variables inside a function?</summary>

#### Python

Python uses the LEGB rule to resolve names:

- `L`ocal;
- `E`nclosing (outer functions);
- `G`lobal (module);
- `B`uiltins.

Inside a function, assignment creates a local variable unless `global` or
`nonlocal` is declared.

**In short:**

- Scope defines where a name is available and mutable.
- LEGB explains the order in which variables are resolved.
- Misunderstanding scope often leads to `UnboundLocalError`.

</details>

<details>
<summary>83. What are local and global variables in Python?</summary>

#### Python

Local variables exist inside a function body. Global variables are defined at
the module level.

To modify a global variable from a function, you need `global`, but this is
usually worth avoiding because it creates implicit dependencies.

**In short:**

- Local variables are safer for maintenance and testing.
- Global variables simplify access but make state harder to control.
- It is better to pass dependencies through parameters.

</details>

<details>
<summary>84. What is the difference between local and nonlocal variables in Python?</summary>

#### Python

`nonlocal` is used in a nested function to modify a variable from the nearest
enclosing scope, not the global scope.

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

**In short:**

- A local variable belongs to the current function.
- `nonlocal` modifies the state of the outer function.
- It is a key mechanism for stateful closures.

</details>

<details>
<summary>85. What is unpacking in Python, and how is it used in assignment?</summary>

#### Python

Unpacking means splitting elements of a sequence or structure into separate
variables.

```python
x, y = (10, 20)
first, *middle, last = [1, 2, 3, 4]
```

It also works with dictionaries in `match/case`, function calls, and loops.

**In short:**

- Unpacking makes code more compact and readable.
- It supports starred capture of remaining values.
- It is often used when parsing data structures.

</details>

<details>
<summary>86. Explain the concept of packing values in Python and give examples.</summary>

#### Python

Packing means collecting multiple values into one structure such as a `tuple`,
`list`, or `dict`.

```python
point = 10, 20                 # tuple packing

def collect(*args: int) -> tuple[int, ...]:
    return args
```

`*args` and `**kwargs` are typical examples of argument packing.

**In short:**

- Packing collects many values into one container.
- It is most often used in function signatures.
- It combines well with unpacking on the caller side.

</details>

<details>
<summary>87. What is the `*` operator used for in packing and unpacking?</summary>

#### Python

In function parameters, `*` packs positional arguments into `*args`, and in a
call it unpacks an iterable into positional arguments.

```python
def add(a: int, b: int) -> int:
    return a + b

nums = [2, 3]
add(*nums)  # 5
```

`*` is also used in assignment to capture the "rest" of the elements.

**In short:**

- `*` is a universal operator for working with varargs.
- In a signature it packs, and in a call it unpacks.
- It reduces boilerplate when passing data around.

</details>

<details>
<summary>88. What is a closure, and how is it related to decorators?</summary>

#### Python

A closure is an inner function that remembers variables from the enclosing scope
even after the outer function has finished.

Decorators are usually implemented with closures: the wrapper keeps a reference
to the original function and any extra parameters.

**In short:**

- A closure is a function plus captured context.
- A decorator is often a practical use of a closure.
- It lets you add behavior without changing the function body.

</details>

<details>
<summary>89. What is a decorator in Python, and how does it work?</summary>

#### Python

A decorator is a callable that takes a function or class and returns a modified
version, usually a wrapper.

```python
from functools import wraps

def log_calls(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Common uses include logging, caching, authorization, retries, and metrics.

**In short:**

- A decorator adds cross-cutting behavior.
- It works by wrapping a callable.
- It helps avoid duplicating technical logic in business code.

</details>

<details>
<summary>90. Can you use multiple decorators on a single function?</summary>

#### Python

Yes, you can stack multiple decorators. They are applied from bottom to top,
meaning the one closest to `def` wraps the function first.

```python
@decorator_a
@decorator_b
def handler() -> None:
    ...
```

Equivalent form: `handler = decorator_a(decorator_b(handler))`.

**In short:**

- Multiple decorators are valid and common.
- The order of application matters.
- A decorator stack should be documented for clarity.

</details>

<details>
<summary>91. Describe a possible problem with the order of decorators when applying them to a function.</summary>

#### Python

The wrong order can change semantics. For example, applying caching before an
access check can cache an unwanted result or bypass expected logic.

Typical risks:

- logging sees already modified arguments;
- retries wrap the wrong exception;
- caching is applied before or after validation at the wrong point.

**In short:**

- The order of decorators affects function behavior.
- This is a common source of hidden bugs.
- Critical decorator chains need tests for execution order.

</details>

<details>
<summary>92. Can you create a decorator using a class?</summary>

#### Python

Yes. A class-based decorator implements `__call__` so that its instance behaves
like a function.

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.calls = 0

    def __call__(self, *args, **kwargs):
        self.calls += 1
        return self.func(*args, **kwargs)
```

**In short:**

- A decorator can be implemented not only as a function but also as a class.
- A class is convenient when you need internal state.
- The key mechanism is `__call__`.

</details>

<details>
<summary>93. How do you define a decorator that accepts parameters?</summary>

#### Python

You need a three-level structure: decorator factory -> decorator -> wrapper.

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

**In short:**

- A parameterized decorator is a function that returns a decorator.
- A closure is often used to preserve the parameters.
- This approach is convenient for configurable behavior.

</details>

<details>
<summary>94. What is `functools.wraps` used for in decorator functions?</summary>

#### Python

`functools.wraps` copies metadata from the original function to the wrapper: its
name, docstring, module, and `__wrapped__`.

This matters for:

- correct debugging and logs;
- introspection and documentation;
- compatibility with tools that inspect the function signature.

**In short:**

- `wraps` preserves the identity of the original function.
- Without it, decorated functions lose useful metadata.
- It is a best practice for all wrapper decorators.

</details>

<details>
<summary>95. How do dict comprehension, list comprehension, and set comprehension work?</summary>

#### Python

A comprehension creates a collection from an expression and one or more loops,
optionally with a filter.

```python
squares = [x * x for x in range(6)]
mapping = {x: x * x for x in range(6)}
unique = {x % 3 for x in range(10)}
```

Formats:

- list: `[expr for x in it if cond]`
- set: `{expr for x in it if cond}`
- dict: `{k_expr: v_expr for x in it if cond}`

**In short:**

- Comprehensions express data transformation compactly.
- They work for `list`, `set`, and `dict`.
- They produce cleaner code than manual appending in a loop.

</details>

<details>
<summary>96. What are the advantages of using list comprehensions compared to regular loops?</summary>

#### Python

Advantages:

- shorter and more declarative code;
- fewer temporary variables;
- usually slightly better performance in CPython;
- lower risk of forgetting `append`.

A drawback is that very complex logic can reduce readability in a comprehension.

**In short:**

- A list comprehension is well suited for simple transformations.
- It is often faster and cleaner than a manual loop.
- For complex branching, a regular `for` loop is better.

</details>

<details>
<summary>97. Can you give an example of a nested list comprehension?</summary>

#### Python

Example of flattening a matrix:

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for row in matrix for item in row]  # [1, 2, 3, 4, 5, 6]
```

Example with a condition:

```python
pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
```

**In short:**

- A nested comprehension contains multiple `for` clauses in one expression.
- The order of `for` clauses matches nested loops.
- Use it only when the expression remains readable.

</details>

<details>
<summary>98. What is faster in Python: a list comprehension or creating a list with a loop?</summary>

#### Python

In typical scenarios, a list comprehension is slightly faster than a loop with
`append` because it uses optimized bytecode and has less overhead.

Important: the real gain depends on the body of the operation, so for critical
paths you should measure it with tools like `timeit` or `pyperf`.

**In short:**

- A list comprehension is often faster.
- The difference may be small.
- For production decisions, rely on measurement.

</details>

<details>
<summary>99. What is an iterator in Python?</summary>

#### Python

An iterator is an object that returns elements one by one and remembers its
current state. It implements this protocol:

- `__iter__()` returns itself;
- `__next__()` returns the next element or raises `StopIteration`.

**In short:**

- An iterator provides element-by-element access without loading all data at
  once.
- It is the basis of `for` loops, generators, and lazy processing.
- After exhaustion, an iterator does not rewind itself.

</details>

<details>
<summary>100. How do you create an iterator from an iterable object using the `iter()` function?</summary>

#### Python

Call `iter(iterable)` to get an iterator.

```python
items = [10, 20, 30]
it = iter(items)
```

After that, values are read with `next(it)`.

**In short:**

- `iter()` converts an iterable into an iterator.
- It is an explicit way to control iteration manually.
- It is used in lower-level stream processing.

</details>

<details>
<summary>101. What is the `next()` function used for when working with iterators?</summary>

#### Python

`next(iterator[, default])` returns the next element from an iterator. When the
elements are exhausted, it raises `StopIteration` or returns `default` if one is
provided.

```python
it = iter([1, 2])
next(it)        # 1
next(it)        # 2
next(it, None)  # None
```

**In short:**

- `next()` gives manual control over iteration steps.
- Without `default`, the end of the stream raises `StopIteration`.
- With `default`, you can read a stream safely.

</details>

<details>
<summary>102. Can `__next__()` and `__iter__()` be used interchangeably with the `next()` and `iter()` functions?</summary>

#### Python

Yes, but with an iterator protocol nuance:

- `iter(obj)` calls `obj.__iter__()`;
- `next(it)` calls `it.__next__()`.

So these functions are the standard interface to the dunder methods and are
usually used instead of calling the methods directly.

**In short:**

- `iter()` corresponds to `__iter__()`.
- `next()` corresponds to `__next__()`.
- In application code, built-in functions are preferred.

</details>

<details>
<summary>103. What is the role of `StopIteration` in iterator design, and when does it usually occur?</summary>

#### Python

`StopIteration` signals that an iterator has been exhausted. A `for` loop
intercepts it automatically and ends iteration.

It usually occurs:

- when `next(it)` is called after the last element;
- in custom iterators when the data is exhausted.

**In short:**

- `StopIteration` is the normal end of a stream.
- It should not be logged as an error in normal flow.
- In custom iterators, it must be raised correctly.

</details>

<details>
<summary>104. What is a generator, and how is it different from an iterator or a regular function?</summary>

#### Python

A generator is a special iterator created by a function with `yield`. It
produces values one by one and preserves internal state between calls.

Differences:

- from a regular function: it does not finish with a single `return` but pauses
  and resumes;
- from a manual iterator: it is simpler to implement because no explicit
  `__next__` class is needed.

**In short:**

- A generator is the most convenient way to implement lazy iteration.
- It requires less code than a custom iterator class.
- It is especially useful for large data streams.

</details>

<details>
<summary>105. How do you create a generator function?</summary>

#### Python

You define a function that uses `yield`.

```python
def countdown(start: int):
    current = start
    while current > 0:
        yield current
        current -= 1
```

Calling `countdown(3)` returns a generator object that can be iterated.

**In short:**

- The presence of `yield` makes the function a generator.
- A generator returns values step by step.
- The function state is preserved between iterations.

</details>

<details>
<summary>106. How does the `yield` keyword enable generator functionality, and why do generators save memory?</summary>

#### Python

`yield` returns the next value and freezes the function context, including local
variables and execution position. The next `next()` call resumes execution from
that point.

Generators save memory because data is not created fully in advance. It is
computed on demand.

**In short:**

- `yield` implements pause and resume behavior.
- A generator supports lazy evaluation.
- This reduces memory footprint for large data sets.

</details>

<details>
<summary>107. What is the difference between `return` and `yield`?</summary>

#### Python

`return` ends a function and returns one final value. `yield` returns an
intermediate value and preserves state so execution can continue later.

In a generator, `return` means the end of iteration and results in
`StopIteration`.

**In short:**

- `return` means function completion.
- `yield` means step-by-step value production.
- `yield` is used for streaming-style processing.

</details>

<details>
<summary>108. What is Object-Oriented Programming (OOP), and what are its main principles in Python?</summary>

#### Python

OOP is an approach where data and behavior are combined in objects.

Key principles:

- encapsulation;
- inheritance;
- polymorphism;
- abstraction.

In Python, OOP is usually combined with composition and duck typing.

**In short:**

- OOP structures the domain through classes and objects.
- Python supports OOP flexibly, without excessive boilerplate.
- In practice, composition is often better than deep inheritance.

</details>

<details>
<summary>109. What is a `class` in Python?</summary>

#### Python

A `class` is a blueprint for creating objects with attributes and methods.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name
```

A class defines the structure and behavior of future instances.

**In short:**

- A class describes data and operations on that data.
- Objects, or instances, are created from a class.
- It is the basic modeling unit in OOP.

</details>

<details>
<summary>110. How do you create an object in Python?</summary>

#### Python

An object is created by calling a class:

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

user = User("Ada")
```

During creation, `__init__` runs to initialize the state.

**In short:**

- An object is an instance of a class.
- Creation looks like `instance = ClassName(...)`.
- `__init__` sets up the initial attributes.

</details>

<details>
<summary>111. What are objects and attributes?</summary>

#### Python

An object is a concrete instance of a type or class. An attribute is a
name-value pair associated with an object, either data or a method.

```python
user.name       # data attribute
user.save()     # method attribute
```

**In short:**

- An object stores state and behavior.
- Attributes describe that state and behavior.
- Attributes are accessed with dot notation.

</details>

<details>
<summary>112. What role does the `__init__()` method play in a class?</summary>

#### Python

`__init__` is the instance initializer. It is called after object creation and
fills in the initial state.

```python
class Account:
    def __init__(self, owner: str, balance: float = 0.0) -> None:
        self.owner = owner
        self.balance = balance
```

**In short:**

- `__init__` sets the initial attributes of an object.
- It works as the entry point for instance configuration.
- It does not create the object, it only initializes it.

</details>

<details>
<summary>113. What is the `self` parameter used for in Python class methods?</summary>

#### Python

`self` is a reference to the current instance. Through it, a method reads and
modifies instance attributes.

```python
def deposit(self, amount: float) -> None:
    self.balance += amount
```

The name `self` is not syntactically reserved, but it is the accepted standard.

**In short:**

- `self` binds a method to a specific object.
- Instance data is accessed through `self`.
- It is the required first parameter of an instance method.

</details>

<details>
<summary>114. How do you define methods in a class?</summary>

#### Python

Methods are defined as functions inside a `class`.

```python
class Calculator:
    def add(self, a: int, b: int) -> int:
        return a + b
```

Common kinds are instance methods with `self`, class methods with `@classmethod`
and `cls`, and static methods with `@staticmethod` and no `self` or `cls`.

**In short:**

- A method is a function inside a class body.
- The method type is determined by its decorator and signature.
- The most common type is the instance method.

</details>

<details>
<summary>115. Explain the concept of "everything is an object" in Python and give examples.</summary>

#### Python

In Python, almost everything is an object: numbers, strings, functions, classes,
and modules. That means everything has a type, attributes, and behavior.

```python
type(10)          # <class 'int'>
type(len)         # <class 'builtin_function_or_method'>
type(str)         # <class 'type'>
```

**In short:**

- A unified object model simplifies the language.
- Functions and classes are also first-class objects.
- This makes Python flexible for metaprogramming.

</details>

<details>
<summary>116. Give an example of a class with methods that perform calculations based on attributes.</summary>

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

**In short:**

- Methods can calculate values from instance attributes.
- This encapsulates domain logic inside the object.
- The class API becomes self-documenting.

</details>

<details>
<summary>117. Describe a situation where using multiple classes may be necessary in a Python program.</summary>

#### Python

When a domain has multiple responsibilities, they are separated into different
classes. For example, in e-commerce: `Order`, `OrderItem`, `PaymentService`, and
`InventoryService`.

This provides:

- a clear separation of responsibilities;
- looser coupling;
- easier replacement and testing of components.

**In short:**

- Multiple classes are needed to model a complex domain.
- Separation of responsibilities improves maintainability.
- Class composition is usually better than a god object.

</details>

<details>
<summary>118. What is the difference between an instance method, a class method, and a static method?</summary>

#### Python

- An instance method has `self` and works with a specific instance.
- A class method has `cls` and works with the class as a whole.
- A static method has no `self` or `cls` and is a utility function in the class
  namespace.

**In short:**

- Instance means instance-level logic.
- Class means class-level logic or alternative constructors.
- Static means helper logic without state access.

</details>

<details>
<summary>119. What is `@classmethod` in Python, and how is it different from regular methods?</summary>

#### Python

`@classmethod` passes the class `cls` as the first argument instead of an
instance. It is often used for factory methods.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

    @classmethod
    def from_email(cls, email: str) -> User:
        return cls(email.split("@")[0])
```

**In short:**

- A `classmethod` works at the class level.
- It is convenient for alternative constructors.
- It does not require an already created instance.

</details>

<details>
<summary>120. What is `@staticmethod` in Python classes, and when is it appropriate to use it?</summary>

#### Python

`@staticmethod` defines a method without automatic `self` or `cls`. It logically
belongs to the class but does not depend on class or instance state.

```python
class Math:
    @staticmethod
    def clamp(value: int, min_v: int, max_v: int) -> int:
        return max(min_v, min(value, max_v))
```

**In short:**

- A `staticmethod` is a function in the class namespace.
- Use it for helper logic without access to attributes.
- It is not suitable when you need instance or class state.

</details>

<details>
<summary>121. What is the difference between `@classmethod` and `@staticmethod` in Python classes?</summary>

#### Python

The difference is in the first argument and the access level:

- `@classmethod` receives `cls` and can work with class state;
- `@staticmethod` receives nothing automatically.

`classmethod` is more often used for factories and polymorphic constructors,
while `staticmethod` is used for utilities.

**In short:**

- `classmethod` knows about the class.
- `staticmethod` is isolated from class and instance state.
- The choice depends on whether access to `cls` is needed.

</details>

<details>
<summary>122. What are instance attributes in Python classes, and how are they different from class attributes?</summary>

#### Python

Instance attributes belong to a specific object, for example `self.x`. Class
attributes belong to the class and are shared by all instances.

```python
class User:
    role = "member"           # class attribute
    def __init__(self, name: str) -> None:
        self.name = name      # instance attribute
```

**In short:**

- Instance attributes store individual state.
- Class attributes store shared configuration.
- Mutating a class attribute affects all instances.

</details>

<details>
<summary>123. What is `__slots__` in Python?</summary>

#### Python

`__slots__` restricts the set of allowed attributes in a class and can reduce
memory usage by removing `__dict__` from instances.

```python
class Point:
    __slots__ = ("x", "y")
    def __init__(self, x: int, y: int) -> None:
        self.x = x
        self.y = y
```

**Usage nuances:**

- **Memory savings:** objects take significantly less space because attributes
  are stored in a fixed layout instead of the `__dict__` hash table.
- **Speed:** attribute access with `__slots__` is usually slightly faster.
- **No `__dict__`:** you cannot dynamically add new attributes that are not
  listed in `__slots__`, unless you explicitly add `"__dict__"` to the slots.
- **Weak references:** if you want to use `weakref`, you must explicitly add
  `"__weakref__"` to `__slots__`.

**In short:**

- `__slots__` is useful for millions of lightweight objects, for example graph
  nodes.
- It removes `__dict__` and `__weakref__` by default.
- It reduces flexibility in exchange for performance and control.

</details>

<details>
<summary>124. What are magic methods, or dunder methods, in Python classes, and why are they called "magic"?</summary>

#### Python

Dunder methods such as `__init__`, `__str__`, `__len__`, and `__eq__` are
special hooks that Python calls automatically in response to operators and
built-ins.

They are called "magic" because they integrate your class into the behavior of
the language itself.

**In short:**

- Dunder methods define the protocol behavior of an object.
- They let your classes behave like built-in types.
- Use them only when there is a clear semantic need.

</details>

<details>
<summary>125. What is the `__del__` method used for?</summary>

#### Python

`__del__` is a finalizer that may be called before an object is destroyed by the
garbage collector. Its behavior is not deterministic, so resource management is
better handled with context managers like `with` and explicit closing.

**In short:**

- `__del__` does not guarantee timely execution.
- Do not rely on it alone for critical cleanup.
- The recommended approach is `with` or `try/finally`.

</details>

<details>
<summary>126. Give an example of using the `__str__` magic method to define a text representation of your own class in Python.</summary>

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

`str(user)` and `print(user)` will use `__str__`.

**In short:**

- `__str__` provides a human-readable representation of an object.
- It is useful for logs and CLI output.
- It should be short and readable.

</details>

<details>
<summary>127. What are `__str__` and `__repr__` used for?</summary>

#### Python

`__str__` is aimed at the end reader. `__repr__` is aimed at the developer or
debugging and should ideally be unambiguous.

`print(obj)` usually uses `__str__`, while the REPL and `repr(obj)` use
`__repr__`.

**In short:**

- `__str__` is for friendly output.
- `__repr__` is for technical representation.
- Good practice is to have both if the class is a domain object.

</details>

<details>
<summary>128. How does operator overloading work in Python, and why is it useful?</summary>

#### Python

Operator overloading means implementing operator dunder methods such as
`__add__`, `__sub__`, and `__eq__` so that objects of your own class can use
operators.

```python
class Vector2:
    def __init__(self, x: float, y: float) -> None:
        self.x = x
        self.y = y

    def __add__(self, other: "Vector2") -> "Vector2":
        return Vector2(self.x + other.x, self.y + other.y)
```

**In short:**

- It provides natural syntax for domain types.
- It improves API expressiveness.
- It is important to preserve mathematically expected semantics.

</details>

<details>
<summary>129. What is inheritance?</summary>

#### Python

Inheritance allows you to create a child class that inherits attributes and
methods from a base class and can extend or override behavior.

**In short:**

- Inheritance promotes code reuse.
- A child class can override base class methods.
- Deep hierarchies make maintenance harder, so composition is often better.

</details>

<details>
<summary>130. What is single inheritance in Python?</summary>

#### Python

Single inheritance means that a class has only one direct parent.

```python
class Animal:
    ...

class Dog(Animal):
    ...
```

This is the simplest and usually the most readable form of inheritance.

**In short:**

- One child class means one base class.
- It has a simple method resolution model.
- It is often enough for most business models.

</details>

<details>
<summary>131. How do you implement inheritance in Python classes, and what syntax is used for it?</summary>

#### Python

The syntax is `class Child(Base):`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return "hi"
```

Use `super()` when you need to call base-class logic.

**In short:**

- Inheritance is declared in parentheses after the class name.
- A child class receives the base class API.
- Overriding lets you adapt behavior.

</details>

<details>
<summary>132. How do you access members of a base class in a child class?</summary>

#### Python

Access is possible directly through inherited attributes and methods or through
`super()`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return super().greet() + " world"
```

**In short:**

- Inherited members are available in the child class automatically.
- `super()` calls base-class logic correctly.
- This matters for extension rather than duplication of behavior.

</details>

<details>
<summary>133. What is the `super()` function used for in Python inheritance, and how is it used?</summary>

#### Python

`super()` returns a proxy to the next class in the MRO so you can call its
methods. It is typically used in `__init__` and in cooperative multiple
inheritance.

```python
class Child(Base):
    def __init__(self, value: int) -> None:
        super().__init__()
        self.value = value
```

**In short:**

- `super()` calls a parent implementation without hardcoding the class name.
- It helps preserve MRO correctness.
- It is the recommended way to work with inheritance.

</details>

<details>
<summary>134. Describe the `isinstance()` function in Python and give an example of its use.</summary>

#### Python

`isinstance(obj, cls_or_tuple)` checks whether an object belongs to a type or to
one of its subclasses.

```python
isinstance(10, int)                 # True
isinstance(True, int)               # True
isinstance("x", (str, bytes))       # True
```

**In short:**

- `isinstance` is safer than `type(obj) is ...` in polymorphic code.
- It respects inheritance hierarchies.
- It supports tuples of types.

</details>

<details>
<summary>135. Explain the `issubclass()` function in Python and give an example of its use.</summary>

#### Python

`issubclass(Sub, Base)` checks whether class `Sub` is a subclass of `Base`.

```python
class Animal: ...
class Dog(Animal): ...

issubclass(Dog, Animal)  # True
```

**In short:**

- It works with classes, not instances.
- It is useful for validating APIs at the type level.
- It respects transitive inheritance.

</details>

<details>
<summary>136. What is multiple inheritance?</summary>

#### Python

Multiple inheritance means inheriting one class from several base classes.

```python
class A: ...
class B: ...
class C(A, B): ...
```

It gives flexibility, but it requires discipline in method design and `super()`
usage.

**In short:**

- One class can inherit behavior from multiple sources.
- It is useful for the mixin approach.
- It can make MRO harder to understand.

</details>

<details>
<summary>137. How does MRO, or Method Resolution Order, work in multiple inheritance?</summary>

#### Python

MRO defines the order in which methods are searched in a class hierarchy. In
Python, the C3 linearization algorithm is used.

**Diamond Problem:** This is the classic case where class `D` inherits from `B`
and `C`, and both of them inherit from `A`. MRO guarantees that `A` is
considered only after all of its descendants, `B` and `C`, have been considered.

```python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass

print(D.mro())
# [D, B, C, A, object]
```

You can inspect the order through `ClassName.__mro__` or `ClassName.mro()`.

**In short:**

- MRO decides which base class provides the method.
- The order is predictable and formally defined by C3.
- Thanks to MRO, Python handles the Diamond Problem correctly.
- In cooperative inheritance, all classes should call `super()`.

</details>

<details>
<summary>138. What are the advantages and disadvantages of using multiple inheritance?</summary>

#### Python

Advantages:

- reuse of behavior from multiple sources;
- convenient mixins for adding capabilities.

Disadvantages:

- more complex MRO;
- risk of name and behavior conflicts;
- harder debugging and onboarding.

**In short:**

- Multiple inheritance is powerful, but it requires strict design rules.
- For most cases, composition is simpler.
- Use multiple inheritance mainly for small mixins.

</details>

<details>
<summary>139. What are mixins?</summary>

#### Python

A mixin is a small class with narrow additional behavior that is intended to be
combined through inheritance rather than used on its own.

Examples include `TimestampMixin` and `JsonSerializableMixin`.

**In short:**

- A mixin adds one specific capability.
- It usually does not have its own full lifecycle.
- It combines well with multiple inheritance.

</details>

<details>
<summary>140. What is encapsulation in Python?</summary>

#### Python

Encapsulation means hiding internal implementation behind a stable public API.
In Python, this is implemented mainly through conventions and `property`, not
through strict access modifiers.

**In short:**

- Client code works with the interface, not with internal details.
- Encapsulation reduces coupling between components.
- It makes it easier to change internals without breaking the API.

</details>

<details>
<summary>141. What is the difference between public, private, and protected access?</summary>

#### Python

In Python, this is mostly implemented through naming conventions:

- `public`: `name`, accessible everywhere;
- `protected`: `_name`, intended for internal use by convention;
- `private`: `__name`, which triggers name mangling as `_ClassName__name`, but
  does not provide absolute protection.

**In short:**

- Python does not have strict access modifiers like Java or C#.
- `_name` and `__name` are intention signals for developers.
- Real access control is achieved through API design.

</details>

<details>
<summary>142. What is polymorphism, and how is it implemented in Python?</summary>

#### Python

Polymorphism is the ability to work with different objects through a common
interface. In Python, it is often implemented through duck typing and protocols.

```python
def render(obj) -> str:
    return obj.to_text()
```

Any object with a `to_text` method is suitable.

**In short:**

- One interface can have many implementations.
- In Python, polymorphism is often behavioral rather than hierarchical.
- This makes it easier to extend a system with new types.

</details>

<details>
<summary>143. What is abstraction in Python?</summary>

#### Python

Abstraction means exposing the essential API while hiding unnecessary
implementation details. Client code works with the contract, not the internal
steps.

**In short:**

- Abstraction reduces cognitive load.
- It makes it easier to replace an implementation without changing client code.
- It is implemented through interfaces, ABCs, protocols, and facades.

</details>

<details>
<summary>144. How do you implement data abstraction?</summary>

#### Python

Approach:

- hide direct access to internal fields such as `_field`;
- expose a controlled API through methods or `@property`;
- validate invariants in setter logic.

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

**In short:**

- Data abstraction protects object invariants.
- `property` provides controlled access to state.
- Internal details can change without changing the API.

</details>

<details>
<summary>145. What are an ABC and `@abstractmethod`?</summary>

#### Python

An ABC, or Abstract Base Class, is an abstract base class from the `abc` module.
`@abstractmethod` marks a method that a subclass must implement.

```python
from abc import ABC, abstractmethod

class Storage(ABC):
    @abstractmethod
    def save(self, data: bytes) -> None:
        ...
```

**In short:**

- An ABC formalizes the contract of a hierarchy.
- `@abstractmethod` prevents instantiation of an incomplete implementation.
- This is useful in pluggable and extensible architectures.

</details>

<details>
<summary>146. What is a property in Python, and how is it used?</summary>

#### Python

`property` turns accessor methods into an attribute-like API with support for
validation, calculations, or lazy logic.

```python
class User:
    def __init__(self, name: str) -> None:
        self._name = name

    @property
    def name(self) -> str:
        return self._name
```

**In short:**

- `property` gives access control without changing external syntax.
- It is suitable for validation and derived values.
- It allows the API to evolve without breaking clients.

</details>

<details>
<summary>147. What is `@property`?</summary>

#### Python

`@property` is a decorator for a getter method. Together with `@x.setter` and
`@x.deleter`, it forms a managed attribute.

**In short:**

- `@property` lets a method be read like a field.
- It helps encapsulate internal implementation.
- It is often used for backward-compatible APIs.

</details>

<details>
<summary>148. What is a descriptor in Python?</summary>

#### Python

A descriptor is an object that implements `__get__`, `__set__`, or `__delete__`
and controls access to attributes of another class.

`property`, `classmethod`, and `staticmethod` all work through descriptors.

**In short:**

- A descriptor is a low-level attribute access mechanism.
- It lets you reuse validation or field proxy logic.
- It is the foundation of many Python metaprogramming techniques.

</details>

<details>
<summary>149. What is the difference between a property and a descriptor?</summary>

#### Python

A `property` is a ready-made high-level descriptor for a single attribute. A
custom descriptor is a more general mechanism that can be reused across many
fields and classes.

**In short:**

- A `property` is simpler and local.
- A descriptor is more flexible and scalable.
- `property` is actually built on the descriptor protocol.

</details>

<details>
<summary>150. When is it more appropriate to use a property, and when a descriptor?</summary>

#### Python

Use a `property` when the logic concerns one or two fields of a specific class.
Use a descriptor when the same logic, such as validation, casting, or lazy
initialization, must be reused across many classes.

**In short:**

- Local field logic points to `property`.
- Reusable access policy points to a descriptor.
- Descriptors are beneficial in large domain models.

</details>

<details>
<summary>151. What are `setattr()`, `getattr()`, and `hasattr()` used for? What is the difference between them?</summary>

#### Python

These are functions for dynamic attribute access:

- `getattr(obj, name[, default])` reads an attribute;
- `setattr(obj, name, value)` sets an attribute;
- `hasattr(obj, name)` checks whether an attribute exists.

```python
value = getattr(user, "email", None)
if not hasattr(user, "active"):
    setattr(user, "active", True)
```

**In short:**

- `getattr/setattr/hasattr` are used for dynamic work with objects.
- They are useful in generic code, serialization, and adapters.
- It is important not to overuse them so readability is not lost.

</details>

<details>
<summary>152. Explain the meaning of the `__set_name__` method in Python descriptors and give an example of its use.</summary>

#### Python

`__set_name__(self, owner, name)` is called during class creation and lets the
descriptor know the name of the attribute it is bound to.

```python
class Field:
    def __set_name__(self, owner, name): self.name = name
```

**In short:**

- `__set_name__` initializes a descriptor with class context.
- It lets you build reusable field validators.
- It runs once during class creation.

</details>

<details>
<summary>153. What is a `dataclass`, and when should it be used?</summary>

#### Python

`@dataclass` automatically generates boilerplate such as `__init__`, `__repr__`,
and `__eq__`. It is suitable for data models without complex behavior.

```python
from dataclasses import dataclass
@dataclass(slots=True)
class User:
    name: str
    active: bool = True
```

**In short:**

- `dataclass` reduces code for data models.
- It is a good choice for DTOs and configurations.
- More complex validation often requires other tools.

</details>

<details>
<summary>154. What is the difference between `dataclass` and Pydantic?</summary>

#### Python

`dataclass` focuses on convenient structure definition. Pydantic adds runtime
validation, parsing, and data serialization.

**In short:**

- `dataclass` is lighter and faster for internal models.
- Pydantic is better for external input and APIs.
- The choice depends on whether runtime validation is needed.

</details>

<details>
<summary>155. What are type hints, and why are they needed?</summary>

#### Python

Type hints are type annotations in signatures and variables that form an
explicit contract. They improve IDE assistance and static analysis.

**In short:**

- Type hints improve API clarity.
- They allow earlier detection of a class of errors.
- They are useful even in a dynamic language.

</details>

<details>
<summary>156. How does static type checking with `mypy` work?</summary>

#### Python

`mypy` reads type hints and analyzes code without running it, checking type
compatibility. It catches integration errors before runtime.

**In short:**

- `mypy` performs compile-time-like checks for Python.
- It works best in CI.
- Strict modes reduce the number of production bugs.

</details>

<details>
<summary>157. How do you ensure type safety in a Python project?</summary>

#### Python

- consistently add type hints to the public API;
- enable `mypy` or `pyright` in CI;
- use `TypedDict`, `Protocol`, and generics;
- minimize `Any` and implicit casts.

**In short:**

- Type safety is a process, not a one-time action.
- The biggest effect comes from a CI gate for types.
- Gradually increasing strictness works better than a big-bang approach.

</details>

<details>
<summary>158. What is `TypedDict`?</summary>

#### Python

`TypedDict` describes a typed dictionary shape: which keys are expected and what
types their values should have.

```python
from typing import TypedDict
class UserPayload(TypedDict): name: str; active: bool
```

**In short:**

- `TypedDict` types a `dict` with fixed keys.
- It is convenient for JSON-like structures.
- It is checked by a static analyzer.

</details>

<details>
<summary>159. What is `Protocol` in typing?</summary>

#### Python

`Protocol` describes a behavioral contract through structural typing: a type is
compatible if it has the required methods or attributes, regardless of
inheritance.

**In short:**

- `Protocol` brings duck typing into static typing.
- It reduces tight coupling to concrete classes.
- It is useful for testable and extensible APIs.

</details>

<details>
<summary>160. What are generics in Python?</summary>

#### Python

Generics let you write types and functions parameterized by other types. In
modern syntax: `class Box[T]: ...`, `def first[T](...) -> T`.

**In short:**

- Generics make types reusable.
- They strengthen type safety for collections and containers.
- They reduce duplication in typed code.

</details>

<details>
<summary>161. What is Pydantic, and what is it used for?</summary>

#### Python

Pydantic is a library for describing data schemas with runtime validation, type
conversion, and convenient serialization.

Typical use cases include FastAPI request and response models and application
configuration.

**In short:**

- Pydantic validates external data at runtime.
- It is convenient for APIs and integrations.
- It provides clear validation errors and schemas.

</details>

<details>
<summary>162. What are exceptions in Python?</summary>

#### Python

An exception is an object that signals an error or exceptional situation during
code execution.

**In short:**

- Exceptions interrupt normal flow.
- They should be handled where a decision can be made.
- A correct error model improves system reliability.

</details>

<details>
<summary>163. What are the three types of errors in Python, and how do they differ?</summary>

#### Python

- Syntax errors, which are syntax mistakes before execution;
- runtime exceptions, which happen during execution;
- logical errors, where code runs but the result is wrong.

**In short:**

- The interpreter catches syntax and runtime issues.
- Logical errors are found through tests and review.
- Each type requires a different diagnostic approach.

</details>

<details>
<summary>164. How do you use `try`, `except`, `else`, and `finally`?</summary>

#### Python

`try` contains the risky operation, `except` handles the error, `else` runs when
no error occurred, and `finally` always runs for cleanup.

```python
try: data = load()
except FileNotFoundError: data = {}
else: validate(data)
finally: close_connections()
```

**In short:**

- Keep `else` for success-path code.
- Use `finally` for resources and cleanup.
- Catch specific exceptions, not everything.

</details>

<details>
<summary>165. What does the order of `except` categories mean?</summary>

#### Python

`except` blocks are checked from top to bottom, so the most specific exceptions
should come first and general ones such as `Exception` should come last.

**In short:**

- The order of `except` blocks affects which handler runs.
- A broad `except` at the top swallows specific cases.
- This is critical for a correct recovery flow.

</details>

<details>
<summary>166. What is the purpose of the `assert` keyword in Python code?</summary>

#### Python

`assert` checks an invariant and raises `AssertionError` if the condition is
false. It is suitable for internal developer checks, not for validating user
input.

**In short:**

- `assert` documents that something must be true.
- It does not replace production error handling.
- Use it for contracts in internal logic.

</details>

<details>
<summary>167. How is `raise` different from simply printing an error message in Python?</summary>

#### Python

`raise` changes control flow and signals an error to the caller. `print` only
outputs text and does not stop an erroneous scenario.

**In short:**

- `raise` is an error-handling mechanism, `print` is not.
- Exceptions can be caught and logged centrally.
- `print` is for diagnostics, not for an error contract.

</details>

<details>
<summary>168. How do you create your own exception, or custom exception?</summary>

#### Python

Create a class that inherits from `Exception`, or from a more specific base
exception.

```python
class InvalidOrderError(Exception):
    pass
```

**In short:**

- A custom exception makes errors domain-specific and expressive.
- It lets you catch exactly the cases you need.
- It is better than using a generic `ValueError` everywhere.

</details>

<details>
<summary>169. Why does creating custom exceptions matter in Python, and how do they improve error handling?</summary>

#### Python

Custom exceptions form an explicit domain error model and separate technical
errors from business rules.

**In short:**

- They improve readability and maintainability of handlers.
- They provide more precise semantics in logs and APIs.
- They simplify testing of negative scenarios.

</details>

<details>
<summary>170. How are exceptions organized in Python, and what is the hierarchy of exception classes?</summary>

#### Python

The hierarchy is built from `BaseException`. In application code, you almost
always work with subclasses of `Exception`.

Key branches include `ValueError`, `TypeError`, `KeyError`, `OSError`, and
`RuntimeError`.

**In short:**

- Exceptions form a class hierarchy tree.
- It is better to catch specific subclasses.
- `BaseException` is usually not caught in business logic.

</details>

<details>
<summary>171. What approaches are used to handle multiple different exceptions in Python, and why should they be handled separately?</summary>

#### Python

Common approaches:

- separate `except` blocks for each type;
- grouping logically identical ones with `except (A, B):`;
- separate recovery strategies for each category.

**In short:**

- Different exceptions often require different actions.
- Separate handling reduces hidden defects.
- Logs become more precise and useful.

</details>

<details>
<summary>172. Why would you re-raise an exception in Python, and when is it useful?</summary>

#### Python

Re-raising with `raise` without arguments inside `except` lets you add context
such as logging, metrics, or cleanup and then propagate the same error upward.

**In short:**

- Re-raising preserves the original traceback.
- It is useful for centralized handling at a higher level.
- Do not swallow critical errors without a good reason.

</details>

<details>
<summary>173. Why should the use of try-except blocks be limited in Python programs, and how does it affect performance?</summary>

#### Python

`try/except` is necessary, but it should not wrap large blocks just in case. It
is especially costly when exceptions occur frequently and become part of the
normal control flow.

**In short:**

- Catch only expected errors in a narrow place.
- Frequent exceptions hurt performance and readability.
- Prefer explicit checks where appropriate.

</details>

<details>
<summary>174. How should you handle errors when working with files?</summary>

#### Python

Use `with` and catch specific exceptions such as `FileNotFoundError`,
`PermissionError`, `UnicodeDecodeError`, and `OSError`.

```python
try:
    with open(path, "r", encoding="utf-8") as f:
        content = f.read()
except FileNotFoundError:
    ...
```

**In short:**

- `with` guarantees that the file is closed.
- Handle specific I/O errors.
- Log the context: path, mode, and encoding.

</details>

<details>
<summary>175. What file modes are available in Python?</summary>

#### Python

The main modes are:

- `r` for reading;
- `w` for overwriting;
- `a` for appending to the end;
- `x` for creating a new file;
- `b` for binary mode;
- `t` for text mode, the default;
- `+` for reading and writing.

**In short:**

- The chosen mode defines how the file can be accessed and modified.
- `w` erases existing content, while `a` preserves it.
- Use `b` for byte data.

</details>

<details>
<summary>176. Why is it important to close files after operations, and what can happen if a file is left open?</summary>

#### Python

An open file holds an OS file descriptor. If you do not close it:

- file descriptors can leak;
- files can remain locked or not fully flushed;
- long-running processes can become unstable.

**In short:**

- Closing a file releases OS resources.
- `with` automates safe closing.
- This is critical for services and batch scripts.

</details>

<details>
<summary>177. What is the difference between the `read()`, `readline()`, and `readlines()` methods for reading files?</summary>

#### Python

- `read()` reads the entire file or `n` bytes or characters;
- `readline()` reads one line;
- `readlines()` reads all lines into a list.

**In short:**

- `read()` and `readlines()` can be memory-heavy.
- For large files, iterating with `for line in file` is better.
- The choice depends on the file size and processing scenario.

</details>

<details>
<summary>178. How do you write data to a file in Python, and what is the difference between `w` write mode and `a` append mode?</summary>

#### Python

Writing:

```python
with open("out.txt", "w", encoding="utf-8") as f:
    f.write("hello\n")
```

`w` overwrites the file from the beginning, while `a` appends new content to the
end.

**In short:**

- `w` erases old data.
- `a` preserves existing content.
- Log files usually use `a`.

</details>

<details>
<summary>179. How do you work efficiently with large files?</summary>

#### Python

- read in a streaming way, by lines or chunks;
- avoid loading the entire file into memory;
- use buffering and generators;
- choose appropriate formats and parsers for columnar or tabular data.

**In short:**

- The key is streaming instead of reading the whole file at once.
- Generators reduce memory footprint.
- The processing algorithm matters more than micro-optimizations.

</details>

<details>
<summary>180. What are context managers?</summary>

#### Python

A context manager controls a resource through the `__enter__` and `__exit__`
protocol: opening or initialization and guaranteed finalization or cleanup.

**In short:**

- It provides a safe resource lifecycle.
- It works through `with`.
- It reduces resource leaks.

</details>

<details>
<summary>181. How does the `with` construct work?</summary>

#### Python

`with` calls `__enter__` when entering the block and `__exit__` when leaving it,
even if an error occurs.

```python
with open("data.txt", "r", encoding="utf-8") as f:
    data = f.read()
```

**In short:**

- `with` guarantees cleanup.
- It makes work with resources declarative.
- It is recommended for files, locks, transactions, and sessions.

</details>

<details>
<summary>182. How do you create your own context manager?</summary>

#### Python

There are two approaches:

- a class with `__enter__` and `__exit__`;
- a function with `contextlib.contextmanager`.

```python
from contextlib import contextmanager

@contextmanager
def temp_flag():
    yield
```

**In short:**

- A class is suitable for complex state.
- `contextmanager` is convenient for short scenarios.
- Both provide guaranteed cleanup.

</details>

<details>
<summary>183. How does Python manage memory?</summary>

#### Python

CPython uses reference counting and a cyclic garbage collector. In addition, it
has an internal allocator, `pymalloc`, for small objects.

**In short:**

- The basic mechanism is reference counting.
- The garbage collector removes cyclic references.
- Memory is not always returned to the OS immediately.

</details>

<details>
<summary>184. What is reference counting in Python, and why is it important for memory management?</summary>

#### Python

Each object has a reference count. When it reaches zero, the object can be
freed. This makes cleanup of most short-lived objects fast.

**In short:**

- Reference counting gives objects a predictable lifecycle.
- It does not solve cyclic references on its own.
- Together with the garbage collector, it forms the full memory model.

</details>

<details>
<summary>185. What is garbage collection in Python?</summary>

#### Python

Garbage collection in CPython finds and removes unreachable object cycles that
cannot be cleaned up by reference counting alone.

**In short:**

- The garbage collector complements reference counting.
- It is especially important for cyclic reference graphs.
- It can be controlled through the `gc` module.

</details>

<details>
<summary>186. How do you get the memory address of an object in Python?</summary>

#### Python

In CPython, `id(obj)` often corresponds to the object's memory address as an
integer. It is a diagnostic tool, not a stable external identifier.

**In short:**

- `id()` gives object identity.
- In CPython, it is usually the memory address.
- Do not use it for business logic.

</details>

<details>
<summary>187. What is the `getrefcount()` function from the `sys` module used for, and how does it work in Python?</summary>

#### Python

`sys.getrefcount(obj)` returns the current reference count of an object in
CPython. The value is usually one higher because of the temporary reference held
by the function argument.

**In short:**

- It is a diagnostic tool for memory behavior.
- It is useful for analyzing reference leaks.
- It should not be relied on in application logic.

</details>

<details>
<summary>188. Explain with examples the difference between mutable and immutable objects in terms of reference counting and memory management.</summary>

#### Python

Immutable objects do not change, so a "modification" creates a new object.
Mutable objects change in place, and all references see that change.

```python
a = "x"; b = a; a += "y"    # new object
x = [1]; y = x; y.append(2)  # mutation of the same object
```

**In short:**

- Immutable objects reduce side effects.
- Mutable objects are more efficient for in-place modification.
- The difference is critical for copying and shared references.

</details>

<details>
<summary>189. What is the difference between shallow copy and deep copy in Python, and when should each approach be used?</summary>

#### Python

A shallow copy copies only the outer container, while nested objects remain
shared. A deep copy recursively copies the entire structure.

```python
import copy
copy.copy(obj)
copy.deepcopy(obj)
```

**In short:**

- Shallow copy is enough for flat structures.
- Deep copy is needed for isolated work with nested mutable data.
- Deep copy is more expensive in time and memory.

</details>

<details>
<summary>190. What are modules and packages in Python?</summary>

#### Python

A module is a single `.py` file with code. A package is a directory of modules,
or a namespace, that organizes code into larger blocks.

**In short:**

- A module is a unit of code.
- A package is a structure for scaling modules.
- Splitting code into modules and packages improves maintainability.

</details>

<details>
<summary>191. How do you import a module in Python?</summary>

#### Python

Main forms:

- `import module`;
- `import module as m`;
- `from module import name`;
- `from package import submodule`.

**In short:**

- Import loads a module and makes it available in the namespace.
- An alias with `as` improves readability and helps avoid conflicts.
- Prefer explicit imports.

</details>

<details>
<summary>192. What types of imports are there?</summary>

#### Python

Common types:

- absolute;
- relative;
- selective imports such as `from x import y`;
- alias imports with `as`;
- dynamic imports through `importlib`.

**In short:**

- The import type affects readability and maintainability.
- In production code, absolute imports are usually preferred.
- Dynamic imports should be used selectively.

</details>

<details>
<summary>193. How does the import system work?</summary>

#### Python

The interpreter searches for a module through `sys.path`, loads it once, and
caches it in `sys.modules`. Repeated imports use the cache.

**In short:**

- Import means lookup, module execution, and caching.
- This explains why module code runs on the first import.
- Circular imports arise because of module initialization order.

</details>

<details>
<summary>194. What is the difference between absolute and relative import?</summary>

#### Python

An absolute import starts from the package root, for example
`from app.utils import x`. A relative import uses dots, for example
`from .utils import x`.

**In short:**

- Absolute imports are more readable and stable.
- Relative imports are convenient inside a package, but worse for refactoring.
- In large projects, it is better to standardize on absolute imports.

</details>

<details>
<summary>195. What does the `dir()` function do, and how can it be applied to modules?</summary>

#### Python

`dir(obj)` returns a list of available attributes or names of an object. For
modules, it is a quick way to inspect the API.

```python
import math
dir(math)
```

**In short:**

- `dir()` helps with interactive exploration of modules.
- It is useful in the REPL and during debugging.
- It does not replace official documentation.

</details>

<details>
<summary>196. Explain the role of `if __name__ == "__main__":` in Python scripts.</summary>

#### Python

This block runs only when the file is executed as a script, not when it is
imported as a module. It separates reusable code from the CLI entry point.

**In short:**

- It lets a module be both executed and imported.
- It prevents unwanted execution during import.
- It is the standard pattern for scripts.

</details>

<details>
<summary>197. What does the `__init__.py` file mean in a Python package?</summary>

#### Python

`__init__.py` marks a directory as a package and can initialize a package-level
API, for example by re-exporting classes or functions.

**In short:**

- It shapes the public interface of the package.
- It may contain minimal initialization.
- It should not be overloaded with heavy logic.

</details>

<details>
<summary>198. What are the best practices for import style in Python code?</summary>

#### Python

- group imports into stdlib, third-party, and local;
- avoid `from x import *`;
- keep imports at the top of the file, except for justified lazy-import cases;
- use sorting and formatting tools such as `ruff` and `isort`.

**In short:**

- Consistent imports improve readability.
- Explicit imports reduce naming conflicts.
- Tooling automation removes manual mistakes.

</details>

<details>
<summary>199. What popular built-in modules exist in Python?</summary>

#### Python

Examples of popular standard library modules:

- `os`, `sys`, `pathlib`, `json`, `datetime`, `re`,
- `collections`, `itertools`, `functools`, `typing`,
- `asyncio`, `subprocess`, `logging`, `argparse`.

**In short:**

- The standard library covers most basic tasks.
- This reduces the number of external dependencies.
- It is worth knowing the stdlib well before adding third-party packages.

</details>
<details>
<summary>200. What do you know about the `collections` package, and what other built-in modules have been used?</summary>

#### Python

`collections` provides high-level structures:

- `Counter`, `defaultdict`, `deque`, `namedtuple`, `ChainMap`.

It is typically combined with:

- `itertools` for iteration pipelines;
- `functools` for caching and functional tools;
- `pathlib`, `json`, and `datetime` in application tasks.

**In short:**

- `collections` extends basic containers with practical structures.
- It often improves both simplicity and performance.
- It works especially well together with `itertools` and `functools`.

</details>

<details>
<summary>201. What does `sys.argv` return?</summary>

#### Python

`sys.argv` returns a list of command-line arguments:

- `sys.argv[0]` is the script name;
- the remaining elements are the passed arguments.

**In short:**

- `sys.argv` is the basic interface for CLI arguments.
- Values come in as strings.
- For complex CLIs, `argparse` is a better choice.

</details>

<details>
<summary>202. What is the main module for working with the operating system in Python?</summary>

#### Python

The main module is `os` (together with `os.path`), and `pathlib` is recommended
for a modern path API.

**In short:**

- `os` provides access to process, environment, and filesystem OS APIs.
- `pathlib` is more convenient for working with paths.
- Real projects often use both.

</details>

<details>
<summary>203. How do you shuffle the elements of a list using the `random` module?</summary>

#### Python

Use `random.shuffle(list_)` for in-place shuffling.

```python
import random
items = [1, 2, 3, 4]
random.shuffle(items)
```

**In short:**

- `shuffle` modifies the original list.
- It only works with mutable sequences, such as lists.
- For a new copy, use `random.sample(items, k=len(items))`.

</details>

<details>
<summary>204. What is a virtual environment?</summary>

#### Python

A virtual environment is an isolated Python environment with its own packages
and dependency versions for a specific project.

**In short:**

- Isolation removes dependency conflicts between projects.
- The standard tool is `venv`.
- It is a basic practice for reproducible development.

</details>

<details>
<summary>205. How does `pip` work?</summary>

#### Python

`pip` installs, upgrades, and removes packages from indexes, mostly PyPI,
resolves dependencies, and installs them into the current environment.

**In short:**

- `pip` is Python's standard package manager.
- It works within the active virtual environment or interpreter.
- Pinned versions are important for stability.

</details>

<details>
<summary>206. What is `requirements.txt`?</summary>

#### Python

`requirements.txt` is a file containing a list of dependencies, often with exact
versions, used for reproducible installation.

**In short:**

- The format is simple and compatible with `pip install -r`.
- Exact versions are best for production.
- It is often generated by tools such as `pip-tools` or `poetry export` from a
  declarative dependency list or lock files.

</details>

<details>
<summary>207. What is `pyproject.toml`, and why did it become the standard?</summary>

#### Python

`pyproject.toml` is a standardized project configuration file containing package
metadata, the build system, and tool settings such as ruff, pytest, and mypy.

**In short:**

- It centralizes Python project configuration.
- It is supported by modern packaging tools.
- It reduces the number of scattered config files.

</details>

<details>
<summary>208. How do you manage dependencies in a modern Python project?</summary>

#### Python

- isolate the environment with `venv`;
- define dependencies in `pyproject.toml`;
- pin lock files or constraints for reproducibility;
- update regularly with CI checks.

**In short:**

- Dependency management must be reproducible.
- Do not mix global and project-specific packages.
- Perform updates in a controlled way through tests.

</details>

<details>
<summary>209. How should you organize the structure of a large Python project?</summary>

#### Python

- split the code into domain packages;
- keep separate layers such as `api`, `services`, `domain`, and
  `infrastructure`;
- keep separate `tests/`, `scripts/`, and `configs/` directories;
- maintain explicit module boundaries and a public API.

**In short:**

- The structure should reflect the domain, not arbitrary technical details.
- Clear boundaries reduce cyclic dependencies.
- Tests and tooling should be a first-class part of the tree.

</details>

<details>
<summary>210. What is the difference between automated and manual testing, and what are the advantages of automated testing?</summary>

#### Python

Manual testing is performed by a person step by step. Automated testing is
performed by scripts and frameworks.

**In short:**

- Automated tests are fast, repeatable, and suitable for CI.
- Manual testing is useful for exploratory UX scenarios.
- In production, you need a combination of both approaches.

</details>

<details>
<summary>211. What is TDD (Test-Driven Development)?</summary>

#### Python

TDD is a cycle: write a failing test -> add the minimum implementation ->
refactor.

**In short:**

- TDD shapes the API through tests.
- It provides fast feedback on regressions.
- It works best for modular business logic.

</details>

<details>
<summary>212. What are the popular testing frameworks in Python?</summary>

#### Python

The most popular ones are `pytest`, `unittest` from the standard library, and
`hypothesis` for property-based tests.

**In short:**

- `pytest` is most often chosen for new projects.
- `unittest` is the standard built-in testing tool.
- `hypothesis` improves coverage of edge cases.

</details>

<details>
<summary>213. What is `unittest` in Python?</summary>

#### Python

`unittest` is a built-in xUnit-style testing framework with test case classes,
assert methods, setup and teardown hooks, and a test runner.

**In short:**

- It is part of the standard library.
- It fits conservative environments without external dependencies.
- Its syntax is more verbose than `pytest`.

</details>

<details>
<summary>214. What is `pytest`, and how does it differ from `unittest` in syntax and functionality?</summary>

#### Python

`pytest` is a framework with a simple function-based test syntax, powerful
fixtures, parametrization, and a rich plugin ecosystem.

**In short:**

- `pytest` requires less boilerplate and is more convenient for large test
  suites.
- `unittest` is class-based and part of the standard library.
- In modern projects, `pytest` is usually preferred.

</details>

<details>
<summary>215. Describe how the `pytest.raises` method is used to test that specific exceptions are raised in Python code.</summary>

#### Python

`pytest.raises(ExpectedError)` verifies that a block of code raises the expected
exception.

```python
import pytest
with pytest.raises(ValueError):
    int("abc")
```

**In short:**

- It tests negative scenarios explicitly.
- It protects against errors passing silently.
- It can also verify exception messages and attributes.

</details>

<details>
<summary>216. What is test parametrization, and how does pytest support it through `@pytest.mark.parametrize`?</summary>

#### Python

Parametrization runs one test against multiple sets of input data. In pytest,
this is done with the `@pytest.mark.parametrize` decorator.

**In short:**

- It reduces duplication in test code.
- It makes test cases easy to scale.
- It gives better visibility into coverage of input scenarios.

</details>

<details>
<summary>217. How can you assign custom test names in pytest parametrized tests for better readability?</summary>

#### Python

Use the `ids` parameter in `parametrize`.

```python
@pytest.mark.parametrize("value,expected", [(2, True), (3, False)], ids=["even", "odd"])
```

**In short:**

- `ids` makes test output easier to read.
- It simplifies diagnosing failures.
- It is especially useful when you have many cases.

</details>

<details>
<summary>218. What is Arrange/Setup in testing, and why is it important?</summary>

#### Python

Arrange/Setup is the preparation of test state: data, objects, mocks, and the
environment. A solid setup makes the test deterministic.

**In short:**

- Unstable setup leads to flaky tests.
- Good setup isolates the test from external effects.
- Clear Arrange steps improve scenario readability.

</details>

<details>
<summary>219. What stages does Cleanup/Teardown include, and why is it important?</summary>

#### Python

Teardown removes everything created by the test: temporary files, connections,
mocks, and test records in the database.

**In short:**

- Cleanup ensures isolation between tests.
- It reduces side effects and flakiness.
- In pytest, this is conveniently handled with fixture finalizers or yield-based
  fixtures.

</details>

<details>
<summary>220. What is the difference between the `setUp()` and `setUpClass()` methods in unittest?</summary>

#### Python

`setUp()` runs before **each** test method. `setUpClass()` as a class method
runs **once** before all tests in the class.

**In short:**

- `setUp` is for per-test isolation.
- `setUpClass` is for expensive shared resources.
- Too much shared state through `setUpClass` can make tests harder to maintain.

</details>

<details>
<summary>221. What is a mock object, and how does it help improve test quality?</summary>

#### Python

A mock object is a substitute object that imitates a dependency and lets you
control behavior and verify calls.

**In short:**

- Mocks isolate the unit from external services.
- They make tests faster and more stable.
- They let you verify interactions, not just results.

</details>

<details>
<summary>222. What is the difference between using `mock.patch` in unittest and `monkeypatch` in pytest for mocking objects?</summary>

#### Python

`mock.patch` from `unittest.mock` patches objects by import path and provides a
rich API for verifying calls. `monkeypatch` in pytest more simply changes
attributes, environment variables, or dictionaries for the duration of a test.

**In short:**

- `patch` is more powerful for mock-assertion scenarios.
- `monkeypatch` is convenient for quick test substitutions.
- They are often combined depending on the use case.

</details>

<details>
<summary>223. What is the purpose of the `scope` parameter in pytest fixtures?</summary>

#### Python

`scope` defines the fixture lifecycle: `function`, `class`, `module`, `package`,
or `session`.

**In short:**

- A smaller scope means better isolation.
- A larger scope can speed up large test suites.
- Choosing scope is a balance between speed and independence.

</details>

<details>
<summary>224. What is algorithm complexity, and how is it determined?</summary>

#### Python

Algorithm complexity evaluates how time and memory costs grow as the size of the
input data `n` increases.

**In short:**

- Time and space complexity are measured.
- The evaluation is usually asymptotic.
- It helps you choose algorithms and data structures.

</details>

<details>
<summary>225. Explain the concept of Big O notation and its importance in evaluating algorithm complexity.</summary>

#### Python

Big O describes the upper bound of an algorithm's cost growth for large `n`,
ignoring constants and lower-order terms.

**In short:**

- Big O shows scalability, not exact running time.
- It provides a common language for comparing algorithms.
- It is critical for performance at large scale.

</details>

<details>
<summary>226. Which types of algorithmic complexity occur most often?</summary>

#### Python

The most common complexity classes are `O(1)`, `O(log n)`, `O(n)`, `O(n log n)`,
and `O(n^2)`.

**In short:**

- `O(n)` and `O(n log n)` are the most typical in practical tasks.
- `O(n^2)` and above often become bottlenecks.
- You also need to consider memory, not just time.

</details>

<details>
<summary>227. Give examples of tasks that are efficiently solved by linear O(n) algorithms.</summary>

#### Python

Examples:

- finding the maximum or minimum;
- filtering elements;
- counting frequencies with `Counter`;
- checking conditions for each element.

**In short:**

- O(n) means one pass through the data.
- This is optimal for many aggregation tasks.
- Linear algorithms scale well.

</details>

<details>
<summary>228. How does `lru_cache` work, and when should it be used?</summary>

#### Python

`functools.lru_cache` caches function results by argument values and returns the
stored result on repeated calls.

**In short:**

- It is effective for pure functions with repeated inputs.
- It is not suitable for functions with side effects.
- `maxsize` controls how much cache is kept in memory.

</details>

<details>
<summary>229. How do you profile Python code performance?</summary>

#### Python

Basic tools:

- `timeit` for micro-benchmarks;
- `cProfile` and `pstats` for call-level profiling;
- `py-spy` and `scalene` for analysis under realistic workloads.

**In short:**

- Optimize only after measurement.
- Profile realistic load scenarios.
- Record a baseline before and after changes.

</details>

<details>
<summary>230. What are the main ways to optimize Python code?</summary>

#### Python

- choose the right data structures;
- reduce asymptotic complexity;
- avoid unnecessary copies;
- use generators and lazy pipelines;
- cache expensive computations;
- move hot paths to C, Rust, or NumPy if needed.

**In short:**

- The biggest gains come from better algorithms, not syntax tweaks.
- Optimization should be based on profiling.
- Readability should not be sacrificed without measured benefit.

</details>

<details>
<summary>231. When should you use C extensions or PyPy?</summary>

#### Python

C extensions are appropriate for narrow CPU hotspots and integration with native
libraries. PyPy is appropriate when long-running pure Python code benefits from
JIT compilation.

**In short:**

- C extensions provide maximum performance at the cost of build complexity.
- PyPy can improve performance without rewriting code in C.
- The choice should be based on benchmarks for your workload.

</details>

<details>
<summary>232. What is memory profiling?</summary>

#### Python

Memory profiling measures where and how much memory code consumes over time in
order to find leaks and heavy sections.

**In short:**

- It shows memory hot spots and peaks.
- It is useful for batch and data workloads.
- Tools include `tracemalloc`, `memory_profiler`, and `scalene`.

</details>

<details>
<summary>233. What is the GIL (Global Interpreter Lock)?</summary>

#### Python

The GIL is a mechanism in CPython that allows only one thread at a time to
execute Python bytecode within a process.

**In short:**

- The GIL affects CPU-bound multithreading.
- Threads are still useful for I/O-bound tasks.
- For CPU parallelism, multiprocessing is used more often.

</details>

<details>
<summary>234. How does Python's Global Interpreter Lock (GIL) affect concurrency in CPython, and what are the implications for multithreading?</summary>

#### Python

Because of the GIL, threads in CPython do not execute Python bytecode in true
parallel for CPU-bound code. They switch cooperatively.

Implications:

- for I/O-bound threads, the effect is good because I/O wait time overlaps;
- for CPU-bound tasks, the performance gain from threads is usually limited.

**In short:**

- The GIL limits thread parallelism in CPU-bound scenarios.
- Threads remain useful for network and disk I/O.
- For CPU work, use processes or native computations.

</details>

<details>
<summary>235. How does the GIL affect performance?</summary>

#### Python

The GIL has little impact on I/O-bound tasks, but it limits the throughput of
CPU-bound multithreaded Python code in a single process.

**In short:**

- The impact of the GIL depends on the type of workload.
- CPU-bound code with threads in CPython often does not scale.
- The architecture should be chosen based on the workload profile.

</details>

<details>
<summary>236. Explain the concept of threading in Python and how it differs from multiprocessing.</summary>

#### Python

`threading` runs multiple threads within one process with shared memory.
`multiprocessing` runs separate processes with separate memory.

**In short:**

- Threads are lighter and more convenient for I/O-bound work.
- Processes provide real CPU parallelism.
- Processes have higher IPC and creation overhead.

</details>

<details>
<summary>237. When should you use multiprocessing instead of threading?</summary>

#### Python

When the task is CPU-bound and needs to use multiple cores in CPython. Examples
include heavy parsing, image or video processing, and numerical computations.

**In short:**

- CPU-bound usually means `multiprocessing`.
- I/O-bound usually means `threading` or `asyncio`.
- Consider the cost of serialization between processes.

</details>

<details>
<summary>238. What is the difference between concurrency and parallelism in programming, and when should each be used?</summary>

#### Python

Concurrency is the overlap of tasks in time. Parallelism is the actual
simultaneous execution of tasks on multiple CPU cores.

**In short:**

- Concurrency is useful for I/O latency.
- Parallelism is needed for CPU-intensive computation.
- In Python, the choice of tool depends on the type of bottleneck.

</details>

<details>
<summary>239. What is concurrency in Python?</summary>

#### Python

Concurrency in Python is the coordination of multiple tasks so that they make
progress together through threads, asyncio, or processes.

**In short:**

- It is about managing many tasks, not necessarily in parallel.
- It can improve throughput in I/O-heavy scenarios.
- It requires careful synchronization and cancellation design.

</details>

<details>
<summary>240. What is the difference between I/O-bound and CPU-bound tasks?</summary>

#### Python

I/O-bound tasks mostly wait on the network, disk, or database. CPU-bound tasks
mostly spend time on CPU computation.

**In short:**

- I/O-bound work scales well with asyncio or threads.
- CPU-bound work scales better with multiprocessing or native code.
- First identify the bottleneck through profiling.

</details>

<details>
<summary>241. What is the `asyncio` module used for in Python, and how does it enable asynchronous programming?</summary>

#### Python

`asyncio` provides an event loop, task scheduling, and async primitives for
cooperative concurrency in I/O-bound tasks.

**In short:**

- It lets you handle many I/O operations efficiently.
- It is built around `async` and `await`.
- It is well suited to network services and clients.

</details>

<details>
<summary>242. What is the difference between synchronous and asynchronous programming in Python?</summary>

#### Python

Synchronous programming blocks the current thread until the call finishes.
Asynchronous programming uses `await` to return control to the event loop while
an operation waits for I/O.

**In short:**

- Async reduces idle time during I/O.
- Sync is simpler for linear logic.
- Async adds complexity in task management and cancellation.

</details>

<details>
<summary>243. What are `async` and `await`?</summary>

#### Python

`async def` defines a coroutine function. `await` suspends the coroutine until
an awaitable is ready and returns control to the loop.

**In short:**

- This is the syntax of Python's cooperative asynchronous model.
- It is used together with `asyncio` and async libraries.
- `await` can only be used inside `async def`.

</details>

<details>
<summary>244. How does `asyncio` work?</summary>

#### Python

`asyncio` runs an event loop that executes tasks, meaning coroutines, by
switching at `await` points and scheduling ready I/O operations.

**Critical rule:** The event loop runs in a single thread. Any blocking
operation such as `time.sleep()`, synchronous `requests` calls, or heavy
computations stops the **entire** loop and all other tasks.

**In short:**

- One thread can handle many I/O tasks through cooperative scheduling.
- Scheduling is non-preemptive.
- Blocking calls destroy asyncio performance.

</details>

<details>
<summary>245. What is an event loop?</summary>

#### Python

An event loop is a scheduler that tracks events and I/O readiness and runs the
corresponding callbacks or coroutines.

**In short:**

- It is the central component of the asyncio model.
- It manages the lifecycle of async tasks.
- It determines when each coroutine continues execution.

</details>

<details>
<summary>246. How does `asyncio` enable asynchronous programming, and what are the main components involved in asyncio code?</summary>

#### Python

Key components:

- event loop;
- coroutine with `async def`;
- task created with `asyncio.create_task`;
- awaitables (futures, tasks, coroutines);
- synchronization primitives such as `Lock`, `Queue`, and `Semaphore`.

**In short:**

- `asyncio` combines scheduling and async APIs into one model.
- Tasks cooperatively share one execution thread.
- The architecture should account for timeouts, retries, and cancellation.

</details>

<details>
<summary>247. When does `asyncio` not provide benefits?</summary>

#### Python

It does not help when the workload is CPU-bound or when the main libraries are
blocking and do not provide async APIs. It is also not worth the complexity for
simple short scripts.

**Solution for blocking code:** If you need to use a blocking library in an
async environment, use `loop.run_in_executor(None, sync_func)`, which runs it in
a separate thread without blocking the event loop.

**In short:**

- Async does not speed up pure CPU computation.
- Without non-blocking I/O libraries, the benefit is minimal.
- `run_in_executor` helps integrate legacy synchronous code.
- Async complexity should be justified by the workload.

</details>

<details>
<summary>248. How does asyncio cancellation work?</summary>

#### Python

Cancelling a task with `task.cancel()` raises `CancelledError` inside the
coroutine. The code must handle cleanup correctly in `try/finally`.

**In short:**

- Cancellation is a normal control flow mechanism in async code.
- Cancellation handling should be built into coroutine design.
- Ignoring cancellation can leave tasks hanging.

</details>

<details>
<summary>249. What are `contextvars`?</summary>

#### Python

`contextvars` provide context-local variables that are safe for async and
threaded scenarios. They are useful for request IDs, correlation IDs, and tenant
context.

**In short:**

- They are an alternative to global state in concurrent code.
- Values are isolated per context.
- They improve tracing and observability.

</details>

<details>
<summary>250. What best practices should be applied when writing Python code?</summary>

#### Python

- follow PEP 8 and automate formatting;
- write explicit type hints for the public API;
- use `with` for resource management;
- cover business logic with tests;
- avoid premature optimization and profile first;
- keep modules small with clear responsibility;
- manage dependencies through `pyproject.toml` and a lock strategy.

**In short:**

- Readability and predictability matter more than tricks.
- Quality depends on automation: linting, type checks, tests, and CI.
- Architectural simplicity reduces maintenance cost.

</details>
