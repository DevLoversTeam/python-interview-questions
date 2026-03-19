**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

# Python <img src="./assets/python.svg" width="40" height="40" alt="Python logo"/>

## Las preguntas y respuestas más populares de entrevistas sobre Python

<details>
<summary>1. ¿Qué es Python y cuáles son sus características principales?</summary>

#### Python

**Python** es un lenguaje de alto nivel y de propósito general, enfocado en la
legibilidad, el desarrollo rápido y una amplia biblioteca estándar.

Características principales:

- **Sintaxis simple**: el código es fácil de leer y mantener.
- **Modelo de ejecución interpretado**: ciclo rápido de cambios sin una fase de
  compilación manual.
- **Multiplataforma**: el mismo código funciona en Linux, macOS y Windows.
- **Multiparadigma**: enfoques procedimental, POO y funcional en un mismo
  proyecto.
- **Ecosistema sólido**: `pip`, `venv`, `pyproject.toml` y miles de bibliotecas
  listas para usar.
- **Funciones modernas de Python 3.10+**: anotaciones de tipos, `dataclass`,
  `async/await`, `match/case`, generadores y gestores de contexto.

Ejemplo de una función con estilo de producción:

```python
from dataclasses import dataclass

@dataclass(slots=True)
class User:
    name: str
    active: bool

def process_users(users: list[User]) -> list[str]:
    return [user.name for user in users if user.active]
```

**En resumen:**

- Python acelera el desarrollo gracias a su sintaxis simple y a su gran
  biblioteca estándar.
- El lenguaje sirve para back-end, automatización, datos/ML, pruebas y DevOps.
- En Python 3.10+, las prácticas clave son las anotaciones de tipos, el I/O asíncrono y una biblioteca estándar moderna.

</details>

<details>
<summary>2. ¿Cuáles son las ventajas clave de Python?</summary>

#### Python

Ventajas clave de Python en producción:

- alta velocidad de desarrollo gracias a su sintaxis concisa;
- gran biblioteca estándar (`pathlib`, `itertools`, `collections`, `asyncio`);
- ecosistema maduro de paquetes para back-end, datos, automatización y pruebas;
- portabilidad del código entre distintos sistemas operativos;
- buen soporte para tipado (`typing`, `mypy`, `pyright`) y prácticas modernas.

**En resumen:**

- Python reduce el tiempo de salida al mercado.
- Proporciona muchas herramientas listas para usar sin dependencias
  adicionales.
- Sirve tanto para MVP como para servicios escalables.

</details>

<details>
<summary>3. ¿En qué se diferencia Python de los lenguajes compilados?</summary>

#### Python

Python normalmente se ejecuta mediante un intérprete: el código se compila a
bytecode y se ejecuta en tiempo de ejecución en la VM de CPython. En los lenguajes
compilados como C/C++ o Rust, normalmente hay una compilación previa a código
máquina.

Consecuencias prácticas:

- Python es más rápido para desarrollo y prototipado.
- Los lenguajes compilados nativos suelen ser más rápidos en tareas intensivas de CPU.
- En Python, el rendimiento suele mejorarse con algoritmos, perfilado y
  extensiones en C.

**En resumen:**

- Python optimiza la velocidad de desarrollo.
- La compilación a código máquina normalmente ofrece mejor rendimiento bruto.
- La elección depende del dominio y de los requisitos de latencia y rendimiento.

</details>

<details>
<summary>4. ¿Qué significa el tipado dinámico en Python?</summary>

#### Python

El tipado dinámico significa que el tipo está asociado al objeto, no al nombre
de la variable. Un nombre puede referirse a valores de distintos tipos en
diferentes momentos de la ejecución.

```python
value = 10        # int
value = "10"      # str
```

Los tipos se comprueban durante la ejecución, por lo que los errores de tipos
aparecen en tiempo de ejecución si no se usa un analizador estático de tipos.

**En resumen:**

- En Python, el tipo pertenece al objeto, no a la variable.
- El tipo puede cambiar cuando se reasigna el nombre.
- Las anotaciones de tipos añaden control antes de ejecutar el código.

</details>

<details>
<summary>5. ¿Qué significa strong typing en Python?</summary>

#### Python

Strong typing en Python significa que el intérprete no realiza conversiones
implícitas peligrosas entre tipos incompatibles.

```python
1 + "2"  # TypeError
```

Para operar entre tipos distintos se requiere una conversión explícita:

```python
1 + int("2")  # 3
```

**En resumen:**

- Python tiene tipado dinámico, pero es estricto respecto a la compatibilidad de
  tipos.
- Las conversiones implícitas peligrosas se bloquean con un error.
- La conversión explícita hace que el comportamiento sea predecible.

</details>

<details>
<summary>6. ¿Qué es el REPL y cuándo se utiliza?</summary>

#### Python

El REPL (Read-Eval-Print Loop) es un modo interactivo en el que introduces una
expresión, obtienes el resultado de inmediato y validas hipótesis rápidamente.

Casos de uso:

- comprobar la API de una biblioteca;
- probar rápidamente una expresión o un algoritmo;
- explorar datos antes de implementarlos en un módulo.

Herramientas: `python` estándar, `ipython`, `ptpython`.

**En resumen:**

- El REPL ofrece el ciclo de retroalimentación más rápido.
- Es útil para experimentos y para depurar.
- No sustituye a las pruebas, pero reduce el tiempo para validar ideas.

</details>

<details>
<summary>7. ¿Qué son los literals en Python? Da ejemplos de distintos tipos.</summary>

#### Python

Un literal es un valor fijo escrito directamente en el código.

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

**En resumen:**

- Los literals son valores constantes incorporados en el código.
- Cada tipo básico tiene su propia sintaxis literal.
- Se usan con frecuencia para inicializar datos.

</details>

<details>
<summary>8. ¿Qué son las keywords en Python?</summary>

#### Python

Las keywords son palabras reservadas del lenguaje con un propósito sintáctico
especial y no pueden usarse como nombres de variables.

Ejemplos: `if`, `for`, `class`, `def`, `match`, `case`, `try`, `except`,
`async`, `await`.

Para ver la lista:

```python
import keyword
print(keyword.kwlist)
```

**En resumen:**

- Las keywords definen la sintaxis de Python.
- No pueden usarse como identificadores.
- La lista está disponible a través del módulo `keyword`.

</details>

<details>
<summary>9. ¿Qué es una variable en Python?</summary>

#### Python

Una variable en Python es un nombre, una referencia, que apunta a un objeto en
memoria. La asignación vincula el nombre con el objeto, no "mete el valor en
una caja".

```python
x = [1, 2]
y = x
y.append(3)
# x e y apuntan a la misma lista
```

**En resumen:**

- Una variable es una referencia a un objeto.
- Varios nombres pueden apuntar al mismo objeto mutable.
- Esto es importante para entender las copias y los efectos secundarios.

</details>

<details>
<summary>10. ¿Qué son `pass` y `...` (Ellipsis) en Python?</summary>

#### Python

`pass` es una instrucción vacía: no hace nada, pero permite definir un bloque
vacío sintácticamente correcto.

`...` (Ellipsis) es un objeto separado, `Ellipsis`. A menudo se usa como marca
de "aún no implementado", en anotaciones de tipos y en bibliotecas como NumPy.

```python
def feature() -> None:
    pass

PLACEHOLDER = ...
```

**En resumen:**

- `pass` se necesita para bloques de código vacíos.
- `...` es un valor-objeto, no una keyword.
- Ambos se usan como marcadores temporales, pero con distinta semántica.

</details>

<details>
<summary>11. ¿Qué es PEP y cómo influye en la evolución de Python?</summary>

#### Python

PEP (Python Enhancement Proposal) es un documento oficial que describe una
nueva funcionalidad, un estándar o un proceso dentro del ecosistema de Python.

A través de un PEP pasan:

- discusión de diseño;
- argumentación técnica;
- decisión de aceptación o rechazo;
- estandarización de prácticas.

Ejemplos: PEP 8 (estilo), PEP 484 (anotaciones de tipos), PEP 634 (coincidencia estructural de patrones).

**En resumen:**

- PEP es el mecanismo de evolución del lenguaje y de sus herramientas.
- Hace que los cambios sean transparentes y formalizados.
- Muchas prácticas modernas de Python quedaron fijadas precisamente a través de
  los PEP.

</details>

<details>
<summary>12. ¿Qué es PEP 8 y para qué sirve?</summary>

#### Python

PEP 8 es la guía oficial de estilo para código Python: nombres, formato,
indentación, importaciones, longitud de líneas y legibilidad de construcciones.

Para qué sirve:

- el código mantiene un estilo uniforme en el equipo;
- el code review es más rápido;
- hay menos ruido en el diff;
- aumenta la mantenibilidad.

En la práctica, el estilo se automatiza con `ruff format` o con `black` + `ruff`.

**En resumen:**

- PEP 8 estandariza el estilo del código Python.
- Trata de legibilidad y mantenimiento, no de rendimiento.
- Su cumplimiento se automatiza mejor con herramientas.

</details>

<details>
<summary>13. ¿Qué funcionalidades nuevas aparecieron en las versiones modernas de Python 3.10+?</summary>

#### Python

Funcionalidades clave de Python moderno:

- `match/case` (coincidencia estructural de patrones);
- mejoras en la sintaxis y en los mensajes de error;
- union types con `|` (`int | None`);
- `typing.Self`, `typing.TypeAlias`, `typing.override`;
- generics al estilo de PEP 695 (`class Box[T]: ...`, `def f[T](...) -> ...`);
- `tomllib` en la biblioteca estándar.

En la práctica, esto reduce el código repetitivo y mejora la fiabilidad del código
tipado.

**En resumen:**

- Python 3.10+ mejoró de forma notable la sintaxis y el typing.
- `match/case` y el `typing` moderno son lo que más impacta el código.
- Las nuevas features conviene usarlas por defecto en código nuevo.

</details>

<details>
<summary>14. ¿Qué es un docstring en Python?</summary>

#### Python

Un docstring es una cadena de documentación, la primera expresión dentro de un
módulo, clase o función. Está disponible mediante `__doc__` y la usan IDEs,
`help()` y generadores de documentación.

```python
def normalize_email(email: str) -> str:
    """Return lowercase email without surrounding spaces."""
    return email.strip().lower()
```

Se recomienda describir qué hace la función, sus argumentos, el valor de
retorno y las excepciones.

**En resumen:**

- El docstring es documentación integrada en el código.
- Sirve como fuente para `help()` y para la generación automática de docs.
- Un buen docstring reduce la necesidad de leer la implementación.

</details>

<details>
<summary>15. ¿Cómo funcionan las indentaciones en Python?</summary>

#### Python

En Python, la indentación define los bloques de código, como el cuerpo de
`if`, `for`, `def` o `class`. Es decir, la indentación es parte de la sintaxis,
no solo del estilo.

```python
if is_ready:
    run_task()
else:
    stop_task()
```

Mezclar tabs y spaces puede provocar `IndentationError` o una estructura de
bloque incorrecta.

**En resumen:**

- La indentación en Python define la estructura del programa.
- Una indentación incorrecta rompe la ejecución.
- Usa un estilo consistente: 4 espacios.

</details>

<details>
<summary>16. ¿Cuántos espacios deben usarse para la indentación según PEP 8 y por qué es importante mantenerla consistente?</summary>

#### Python

PEP 8 recomienda **4 espacios** por cada nivel de indentación.

Por qué es importante:

- estructura de bloques uniforme en todo el proyecto;
- apariencia predecible en distintos editores;
- menos errores por conflictos entre tab y space;
- diffs más limpios en Git.

**En resumen:**

- La indentación estándar es de 4 espacios.
- Un estilo único elimina toda una clase de errores de formato.
- Esto mejora directamente la legibilidad y el mantenimiento del código.

</details>

<details>
<summary>17. ¿Cuál es la diferencia entre `ruff` y `black` en funcionalidad y uso?</summary>

#### Python

`black` es un formateador de código con reglas fijas.

`ruff` es un linter rápido, además de formateador y autofixer de muchas reglas
como PEP 8, imports, bugs potenciales y simplificaciones de sintaxis.

En la práctica:

- o bien `ruff check --fix` + `ruff format`;
- o bien `ruff` para análisis estático + `black` para formateo.

**En resumen:**

- `black` se centra en el formateo.
- `ruff` cubre el linting y parte de las autocorrecciones.
- En proyectos modernos, a menudo basta con solo `ruff`.

</details>

<details>
<summary>18. Explica el propósito de las anotaciones de tipos en Python y muestra un ejemplo de función con anotaciones de tipos.</summary>

#### Python

Las anotaciones de tipos describen los tipos esperados de los argumentos y del
valor de retorno. Mejoran el autocompletado, el análisis estático y la
legibilidad de la API.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Las anotaciones no realizan validación en tiempo de ejecución por sí mismas, pero ayudan a
detectar errores en CI mediante `mypy` o `pyright`.

**En resumen:**

- Las anotaciones de tipos documentan el contrato de la función.
- Permiten detectar errores antes mediante comprobación estática.
- Mejoran la calidad de la API en bases de código grandes.

</details>

<details>
<summary>19. ¿Qué es la depuración y por qué es una habilidad importante para los programadores?</summary>

#### Python

La depuración es la búsqueda sistemática de la causa de un comportamiento
incorrecto del código y su corrección. No es solo "encontrar un bug", sino
reproducirlo, localizarlo y verificar la corrección.

Ciclo básico:

- reproducir el problema;
- reducir la zona de código;
- comprobar la hipótesis con logs o depurador;
- añadir un test que fije el escenario.

**En resumen:**

- La depuración reduce el MTTR y la cantidad de regresiones.
- Funciona mejor como proceso, no como búsqueda caótica.
- El cierre correcto de la depuración es: corrección + test + verificación posterior.

</details>

<details>
<summary>20. Explica el propósito de usar `print` para depurar. Da un ejemplo de una situación donde este enfoque sea útil.</summary>

#### Python

La depuración con `print` es una forma rápida de comprobar valores de variables y el
orden de ejecución sin lanzar herramientas más complejas.

Es útil cuando necesitas validar rápidamente una hipótesis en un script local:

```python
def parse_port(raw: str) -> int:
    value = raw.strip()
    print(f"raw={raw!r} value={value!r}")
    return int(value)
```

Para código de producción, es mejor pasar a `logging`, para disponer de niveles de
log y una salida controlada.

**En resumen:**

- `print` sirve para un diagnóstico local corto.
- Muestra rápidamente el estado de las variables en el punto problemático.
- Para un diagnóstico estable en un servicio, usa `logging`.

</details>

<details>
<summary>21. Describe cómo usar Python Debugger (PDB) para depurar. ¿Qué ventajas tiene PDB frente a `print`?</summary>

#### Python

`pdb` permite detener la ejecución del programa, avanzar línea por línea, ver
el estado de las variables y la pila de llamadas.

Uso básico:

```python
import pdb

def compute(x: int) -> int:
    pdb.set_trace()
    return x * 2
```

Comandos clave: `n` (next), `s` (step), `c` (continue), `p expr` (print expr),
`l` (list), `bt` (backtrace).

**En resumen:**

- `pdb` da control interactivo sobre la ejecución.
- Es más eficaz que `print` para escenarios complejos.
- Permite diagnosticar el estado sin ensuciar el código con logs.

</details>

<details>
<summary>22. ¿Qué estrategias se pueden aplicar para depurar bucles y funciones en Python?</summary>

#### Python

Estrategias prácticas:

- aislar el error con un ejemplo mínimo reproducible;
- registrar invariantes en las iteraciones del bucle;
- poner breakpoints en la entrada y salida de la función;
- comprobar casos límite como datos vacíos, `None` o volúmenes grandes;
- cubrir la ruta problemática con un test.

En los bucles, es útil registrar el índice y los estados intermedios clave.

**En resumen:**

- Empieza reproduciendo y acotando el problema.
- Comprueba invariantes y condiciones límite.
- Cierra el fix con un test que detecte la regresión.

</details>

<details>
<summary>23. ¿Qué impacto tienen las funciones de larga duración en el rendimiento del programa?</summary>

#### Python

Las funciones de larga duración aumentan la latencia y bloquean procesos de trabajo o hilos
y empeoran el rendimiento del servicio.

Riesgos:

- respuestas lentas de la API;
- tiempos de espera;
- crecimiento de las colas de tareas;
- peor uso de CPU e I/O.

Enfoque: perfilar con `cProfile`, dividir en pasos más pequeños, usar
generadores o procesamiento en flujo y mover los cálculos pesados a `multiprocessing` o a
tareas en segundo plano.

**En resumen:**

- Las funciones largas golpean directamente la latencia.
- La optimización debe basarse en perfilado, no en intuición.
- A nivel de arquitectura, conviene separar el trabajo intensivo de CPU del intensivo de I/O.

</details>

<details>
<summary>24. ¿Qué es logging y por qué es mejor usarlo en lugar de `print`?</summary>

#### Python

`logging` es el mecanismo estándar para registrar eventos con niveles como
`DEBUG`, `INFO`, `WARNING`, `ERROR` y `CRITICAL`, además de formatos y handlers
como consola y archivo.

Por qué es mejor que `print`:

- niveles de detalle controlables;
- formato estructurado;
- configuración centralizada;
- posibilidad de integración con un stack de observability.

**En resumen:**

- `logging` sirve para producción; `print`, no.
- Los niveles de log permiten controlar el ruido.
- Los logs deben ser estructurados y consistentes.

</details>

<details>
<summary>25. ¿Qué es un traceback?</summary>

#### Python

Un traceback es el stack de llamadas que Python muestra cuando ocurre una
excepción: dónde empezó la ejecución, por qué funciones pasó el código y en qué
punto exacto ocurrió el error.

Uso:

- encontrar rápidamente el archivo y la línea del origen del error;
- entender el camino de ejecución hasta el fallo;
- construir un test preciso para reproducirlo.

**En resumen:**

- El traceback es la "ruta" hacia el error.
- La parte más valiosa son los últimos frames del stack y el tipo de excepción.
- Analizar el traceback acelera el root cause analysis.

</details>

<details>
<summary>26. ¿Cuáles son los tipos de datos principales en Python?</summary>

#### Python

Tipos built-in principales:

- numéricos: `int`, `float`, `complex`;
- lógico: `bool`;
- cadenas y bytes: `str`, `bytes`, `bytearray`;
- colecciones: `list`, `tuple`, `set`, `dict`, `frozenset`;
- especiales: `NoneType` (`None`).

Es importante entender la mutability:

- mutable: `list`, `dict`, `set`, `bytearray`;
- immutable: `int`, `str`, `tuple`, `frozenset`.

**En resumen:**

- Python incluye un conjunto rico de tipos básicos "out of the box".
- La elección de la estructura de datos afecta la complejidad de las operaciones.
- La mutability define el comportamiento de las copias y de los efectos
  secundarios.

</details>

<details>
<summary>27. ¿Cuál es la diferencia entre la división normal (`/`) y la división entera (`//`) en Python?</summary>

#### Python

`/` realiza una división normal y siempre devuelve `float`.

`//` realiza una floor division: devuelve la parte entera hacia abajo, hasta
`-∞`, y normalmente el tipo es `int` cuando los operandos son enteros.

```python
7 / 2    # 3.5
7 // 2   # 3
-7 // 2  # -4
```

**En resumen:**

- `/` devuelve un resultado decimal.
- `//` redondea hacia abajo hasta un entero.
- Para números negativos, `//` no equivale a "truncar hacia cero".

</details>

<details>
<summary>28. Explica el uso del operador módulo (`%`) en Python. ¿Cómo se usa para saber si un número es par o impar?</summary>

#### Python

El operador `%` devuelve el resto de una división.

Comprobación de paridad:

```python
def is_even(n: int) -> bool:
    return n % 2 == 0
```

Si `n % 2 == 0`, el número es par; en caso contrario, es impar.

Casos típicos: índices cíclicos, partición en grupos y cálculos de calendario.

**En resumen:**

- `%` devuelve el resto.
- `n % 2` es la comprobación estándar de paridad.
- Se usa a menudo en lógica cíclica.

</details>

<details>
<summary>29. ¿Cómo trabaja Python con enteros grandes y qué límites existen al trabajar con números muy grandes?</summary>

#### Python

`int` en Python tiene precisión arbitraria, es decir, no está limitado a
32/64 bits como en muchos otros lenguajes.

Los límites son prácticos:

- memoria del proceso;
- tiempo de cálculo con valores muy grandes;
- el coste de las operaciones crece con el número de dígitos.

**En resumen:**

- No existe overflow de `int` en el sentido tradicional.
- El límite lo ponen los recursos de la máquina, no un tamaño fijo en bits.
- Para cálculos grandes, importan mucho los algoritmos y el perfilado.

</details>

<details>
<summary>30. ¿Qué importancia tiene manejar la división entre cero en Python y cómo prevenir `ZeroDivisionError` en el código?</summary>

#### Python

Dividir entre cero provoca `ZeroDivisionError`. Debe manejarse de forma
explícita si el divisor llega desde entrada externa o se calcula dinámicamente.

```python
def safe_div(a: float, b: float) -> float | None:
    if b == 0:
        return None
    return a / b
```

En escenarios críticos, usa `try/except` y registra el contexto.

**En resumen:**

- Dividir entre cero es un error de ejecución controlado.
- La prevención más simple es comprobar el divisor antes de operar.
- Con datos externos, añade protección y diagnóstico.

</details>

<details>
<summary>31. Describe el uso del módulo `random` en Python. ¿Cuáles son las funciones más comunes de este módulo?</summary>

#### Python

`random` se usa para valores pseudoaleatorios en simulaciones, datos de prueba
y tareas no criptográficas.

Funciones comunes:

- `random()` devuelve un número en `[0.0, 1.0)`;
- `randint(a, b)` devuelve un entero en un rango;
- `randrange(start, stop, step)` funciona como `range`, pero devuelve un
  elemento aleatorio;
- `choice(seq)` / `choices(seq, k=...)`;
- `shuffle(list_)` mezcla una lista in-place;
- `sample(population, k)` devuelve una muestra única.

Para criptografía, usa `secrets`, no `random`.

**En resumen:**

- `random` sirve para aleatoriedad de propósito general.
- Las más usadas son `randint`, `choice`, `shuffle` y `sample`.
- Para tareas sensibles a la seguridad, necesitas `secrets`.

</details>

<details>
<summary>32. ¿Cómo trabajar con números con mejor precisión en Python?</summary>

#### Python

Para cálculos financieros y decimales exactos, usa `decimal.Decimal` en lugar
de `float`.

```python
from decimal import Decimal

total = Decimal("0.1") + Decimal("0.2")  # Decimal('0.3')
```

Para números racionales, también es útil `fractions.Fraction`.

**En resumen:**

- `float` es cómodo, pero tiene errores por representación binaria.
- Para aritmética decimal exacta, elige `Decimal`.
- El tipo numérico debe corresponder al dominio del problema.

</details>

<details>
<summary>33. ¿Qué son los caracteres de escape en strings de Python y cómo se usan? Da ejemplos de `\n`, `\t`, `\r`, `\"` y `\'`.</summary>

#### Python

Las secuencias de escape son combinaciones especiales con `\` que codifican
caracteres de control dentro de un string.

- `\n` es nueva línea
- `\t` es tabulación
- `\r` es retorno de carro
- `\"` es una comilla doble dentro de un string con `"`
- `\'` es una comilla simple dentro de un string con `'`

```python
text = "A\tB\n\"quoted\"\nI\'m here\rX"
```

**En resumen:**

- Los caracteres de escape controlan el formato del string.
- Permiten insertar comillas sin romper la sintaxis.
- Para rutas o regex, suele ser útil usar raw strings `r"..."`.

</details>

<details>
<summary>34. Explica el uso de los métodos `strip`, `lstrip` y `rstrip` en Python. ¿En qué se diferencian?</summary>

#### Python

Estos métodos trabajan sobre los extremos del string:

- `strip()` elimina caracteres de ambos lados;
- `lstrip()` solo del lado izquierdo;
- `rstrip()` solo del lado derecho.

Por defecto, eliminan whitespace o un conjunto específico de caracteres:

```python
"  hello  ".strip()      # "hello"
"--id--".strip("-")      # "id"
```

**En resumen:**

- La familia `strip` no modifica el string in-place, sino que devuelve uno nuevo.
- La diferencia está solo en el lado que se limpia.
- Se usa muy a menudo sobre datos de entrada.

</details>

<details>
<summary>35. Describe el propósito del método `count` en strings. ¿Cómo funciona?</summary>

#### Python

`str.count(sub[, start[, end]])` cuenta cuántas apariciones no superpuestas de
la subcadena `sub` hay en el rango indicado.

```python
"banana".count("an")      # 2
"banana".count("a", 2)    # 2
```

Devuelve `0` si no hay coincidencias.

**En resumen:**

- `count` devuelve rápidamente la cantidad de apariciones de una subcadena.
- Soporta limitar la búsqueda con `start/end`.
- Cuenta solo apariciones no superpuestas.

</details>

<details>
<summary>36. ¿Cómo funciona el método `join` en Python y para qué se usa con más frecuencia?</summary>

#### Python

`sep.join(iterable)` une una secuencia de strings en un solo string usando
`sep` como separador.

```python
names = ["Ada", "Linus", "Guido"]
result = ", ".join(names)  # "Ada, Linus, Guido"
```

Usos típicos: construir strings tipo CSV, logs, fragmentos SQL, rutas URL y
mensajes.

**En resumen:**

- `join` es la forma estándar y rápida de concatenar strings.
- Se llama sobre el separador, no sobre la lista.
- Es más eficiente que hacer `+=` muchas veces en un bucle.

</details>

<details>
<summary>37. ¿Qué es slicing en Python y cómo se usa para obtener substrings? Da ejemplos con índices positivos y negativos.</summary>

#### Python

Slicing es la selección de una parte de una secuencia mediante `[start:stop:step]`.

```python
s = "python"
s[1:4]     # "yth"
s[:2]      # "py"
s[-3:]     # "hon"
s[::-1]    # "nohtyp"
```

`start` se incluye y `stop` no se incluye.

**En resumen:**

- Slicing funciona con strings, listas y tuplas.
- Los índices negativos se cuentan desde el final.
- Es una herramienta básica para procesar secuencias sin bucles.

</details>

<details>
<summary>38. Explica el método `replace` para strings. ¿Cómo puede usarse para reemplazar varias apariciones de una subcadena?</summary>

#### Python

`str.replace(old, new, count=-1)` devuelve un nuevo string donde `old` se
reemplaza por `new`. Por defecto, reemplaza todas las apariciones.

```python
"foo bar foo".replace("foo", "baz")      # "baz bar baz"
"foo bar foo".replace("foo", "baz", 1)   # "baz bar foo"
```

**En resumen:**

- `replace` no modifica el string in-place.
- Sin `count`, reemplaza todas las apariciones.
- `count` permite controlar cuántos reemplazos se hacen.

</details>

<details>
<summary>39. ¿Cómo funciona el método `split` en strings?</summary>

#### Python

`split(sep=None, maxsplit=-1)` divide un string en una lista de subcadenas.

- sin `sep`, divide por cualquier whitespace;
- con `sep`, divide por un separador concreto;
- `maxsplit` limita el número de divisiones.

```python
"a,b,c".split(",")         # ["a", "b", "c"]
"a b   c".split()          # ["a", "b", "c"]
"k=v=x".split("=", 1)      # ["k", "v=x"]
```

**En resumen:**

- `split` convierte un string en una lista de tokens.
- `sep=None` tiene un comportamiento especial para whitespace.
- `maxsplit` es útil para parsear formatos key/value.

</details>

<details>
<summary>40. ¿Cómo funciona la conversión de tipos (type casting)?</summary>

#### Python

Type casting es la conversión explícita de un valor entre tipos mediante
constructores como `int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`,
`set()` y `dict()`.

```python
age = int("42")
price = float("19.99")
text = str(10)
```

Los datos incorrectos provocan una excepción como `ValueError` o `TypeError`,
por lo que la entrada externa requiere validación.

**En resumen:**

- Python ofrece funciones explícitas de conversión de tipos.
- No todos los valores pueden convertirse de forma segura.
- La entrada del usuario requiere validación y manejo de excepciones.

</details>

<details>
<summary>41. ¿Cómo convierte Python automáticamente distintos tipos de datos a valores booleanos?</summary>

#### Python

En un contexto booleano, Python aplica las reglas de truthiness.

Valores falsy:

- `False`, `None`;
- números cero: `0`, `0.0`, `0j`;
- colecciones vacías: `""`, `[]`, `{}`, `set()`, `tuple()`, `range(0)`.

Todo lo demás suele ser `True`.

```python
bool([])      # False
bool("0")     # True
```

**En resumen:**

- La conversión a booleano se basa en reglas truthy/falsy.
- Lo vacío y lo cero dan `False`.
- El string no vacío `"0"` sigue siendo `True`.

</details>

<details>
<summary>42. Explica cómo convertir un string a entero o a número decimal en Python. ¿Qué pasa si el string no puede convertirse?</summary>

#### Python

Para convertir, usa `int()` y `float()`:

```python
count = int("42")
ratio = float("3.14")
```

Si el string no es válido, Python lanza `ValueError`.

```python
def parse_int(value: str) -> int | None:
    try:
        return int(value)
    except ValueError:
        return None
```

**En resumen:**

- `int()` y `float()` realizan una conversión explícita desde string.
- Un formato inválido produce `ValueError`.
- Para datos externos, hace falta `try/except`.

</details>

<details>
<summary>43. ¿Qué hace Python al comparar distintos tipos de datos, como enteros y flotantes, o enteros y booleanos?</summary>

#### Python

Python permite comparaciones numéricas entre numeric types compatibles.

- `int` y `float` se comparan por valor.
- `bool` es una subclase de `int`: `False == 0`, `True == 1`.

```python
1 == 1.0      # True
True == 1     # True
False < 1     # True
```

Para tipos incompatibles como `int` y `str`, las comparaciones de orden como
`<` y `>` lanzan `TypeError`.

**En resumen:**

- `int`, `float` y `bool` comparten una semántica numérica común.
- `bool` se comporta como `0/1` en comparaciones.
- Los tipos incompatibles no se comparan con operadores de orden.

</details>

<details>
<summary>44. ¿Cómo maneja Python la comparación entre listas y sets?</summary>

#### Python

`list` y `set` son tipos distintos con semánticas diferentes, por lo que la
comparación directa de orden entre ellos no está soportada.

```python
[1, 2] == {1, 2}   # False
[1, 2] < {1, 2}    # TypeError
```

Si necesitas comparar el contenido de elementos, primero normaliza el tipo:

```python
set([1, 2]) == {1, 2}  # True
```

**En resumen:**

- `list` y `set` se comparan como estructuras de datos distintas.
- `==` entre ellas normalmente da `False`.
- Para una comparación con sentido, primero conviértelas al mismo tipo.

</details>

<details>
<summary>45. Describe el uso de la función `bool()` en Python.</summary>

#### Python

`bool(x)` devuelve el valor booleano de `x` según las reglas de truthiness.

Escenarios típicos:

- conversión explícita de un valor a `True/False`;
- condiciones más legibles;
- construcción de filtros.

```python
bool("text")   # True
bool("")       # False
bool(0)        # False
```

**En resumen:**

- `bool()` unifica la comprobación de "vacío/no vacío".
- Se basa en las reglas integradas de truthy/falsy.
- Es útil para validación y lógica condicional.

</details>

<details>
<summary>46. ¿Cuál es la diferencia entre `list` y `tuple`?</summary>

#### Python

La diferencia principal es que `list` es mutable y `tuple` es immutable.

Consecuencias prácticas:

- `list` sirve para datos que cambian;
- `tuple` sirve para registros fijos;
- `tuple` puede usarse como clave de diccionario si sus elementos son hashables.

```python
coords: tuple[float, float] = (50.45, 30.52)
queue: list[str] = ["task-1", "task-2"]
```

**En resumen:**

- `list` es para colecciones mutables.
- `tuple` es para estructuras de datos inmutables.
- La elección afecta la seguridad de la API y su uso en `dict/set`.

</details>

<details>
<summary>47. ¿Cómo se puede crear un `tuple`?</summary>

#### Python

Formas principales:

```python
t1 = (1, 2, 3)
t2 = 1, 2, 3
t3 = tuple([1, 2, 3])
single = (42,)     # la coma es importante
empty = ()
```

Para un solo elemento, la coma es obligatoria; de lo contrario, es solo una
expresión entre paréntesis.

**En resumen:**

- Un `tuple` se crea con un literal o con `tuple(iterable)`.
- `single = (x,)` es un tuple válido de un solo elemento.
- El tuple vacío es `()`.

</details>

<details>
<summary>48. ¿Cuál es la diferencia entre el método `reverse` y el slicing `[::-1]` al invertir una lista?</summary>

#### Python

`list.reverse()` modifica la lista existente in-place y devuelve `None`.

`lst[::-1]` crea una nueva lista invertida, es decir, una copia.

```python
values = [1, 2, 3]
values.reverse()      # values -> [3, 2, 1]

other = values[::-1]  # nueva lista
```

**En resumen:**

- `reverse()` modifica el original.
- `[::-1]` devuelve un objeto nuevo.
- La elección depende de si necesitas conservar los datos originales.

</details>

<details>
<summary>49. Explica el propósito y el uso del método `sort` para listas. ¿Cómo ordenar una lista en orden descendente?</summary>

#### Python

`list.sort()` ordena la lista in-place. Soporta estos parámetros:

- `key`, una función de clave de ordenación;
- `reverse=True`, para orden descendente.

```python
nums = [5, 1, 7]
nums.sort(reverse=True)  # [7, 5, 1]
```

Si necesitas una copia nueva ordenada, usa `sorted(iterable)`.

**En resumen:**

- `sort()` modifica la lista en el lugar.
- Para orden descendente, usa `reverse=True`.
- `sorted()` es conveniente cuando necesitas conservar el original.

</details>

<details>
<summary>50. ¿Cuál es la diferencia entre el método `copy` y la asignación directa de una lista a otra? ¿Por qué a veces es importante usar `copy`?</summary>

#### Python

La asignación copia solo la referencia:

```python
a = [1, 2]
b = a
b.append(3)   # a también cambiará
```

`a.copy()` crea una lista nueva, superficial:

```python
a = [1, 2]
b = a.copy()
b.append(3)   # a no cambiará
```

Para estructuras anidadas, puede hacer falta `copy.deepcopy`.

**En resumen:**

- `=` no copia los datos; comparte el mismo objeto entre variables.
- `copy()` aísla los cambios a nivel de la lista superior.
- Para objetos anidados, usa `deepcopy`.

</details>

<details>
<summary>51. ¿Qué hace el método `pop` en una lista? ¿En qué se diferencia su comportamiento si se indica un índice o no?</summary>

#### Python

`pop()` elimina y devuelve un elemento de la lista.

- `pop()` sin argumentos elimina el último elemento;
- `pop(i)` elimina el elemento con índice `i`.

```python
items = ["a", "b", "c"]
last = items.pop()     # "c"
first = items.pop(0)   # "a"
```

Un índice inválido produce `IndexError`.

**En resumen:**

- `pop` combina eliminación y devolución del valor.
- Sin índice, trabaja sobre el final de la lista.
- Con índice, elimina una posición concreta.

</details>

<details>
<summary>52. ¿Cómo unir dos listas en Python usando el operador `+` y el método `extend`? ¿Cuál es la diferencia clave entre ambos enfoques?</summary>

#### Python

`a + b` crea una **nueva** lista, mientras que `a.extend(b)` modifica la lista
`a` **in-place**.

```python
a = [1, 2]
b = [3, 4]

c = a + b         # [1, 2, 3, 4], a no cambió
a.extend(b)       # a -> [1, 2, 3, 4]
```

**En resumen:**

- `+` devuelve un objeto nuevo.
- `extend()` muta la lista existente.
- La elección depende de si necesitas conservar el original.

</details>

<details>
<summary>53. ¿Para qué se usan las funciones `min`, `max`, `sum`, `all` y `any` en el contexto de listas?</summary>

#### Python

Son agregadores básicos para colecciones iterables:

- `min()` / `max()` para mínimo y máximo;
- `sum()` para suma de números;
- `all()` devuelve `True` si todos los elementos son truthy;
- `any()` devuelve `True` si al menos un elemento es truthy.

```python
nums = [3, 10, 1]
min(nums), max(nums), sum(nums)  # (1, 10, 14)
all([True, 1, "x"])              # True
any([0, "", None, 5])            # True
```

**En resumen:**

- Estas funciones reducen el código repetitivo en los bucles.
- Funcionan con cualquier iterable.
- Combinan bien con generadores para procesamiento perezoso.

</details>

<details>
<summary>54. ¿Qué es un diccionario (`dict`) en Python y en qué se diferencia de otras estructuras de datos?</summary>

#### Python

`dict` es un array asociativo que almacena pares `clave -> valor`. Las claves
deben ser hashable y los valores pueden ser de cualquier tipo.

Diferencias:

- acceso por clave y no por índice;
- complejidad media de búsqueda, inserción y eliminación cercana a `O(1)`;
- desde Python 3.7+ conserva el orden de inserción de las claves.

**En resumen:**

- `dict` es óptimo para acceso rápido por clave.
- Es la estructura principal para configuraciones y mappings.
- Las claves deben ser inmutables y hashable.

</details>

<details>
<summary>55. ¿Cuál es la diferencia entre obtener un valor de un diccionario con corchetes `[]` y con el método `get`?</summary>

#### Python

`d[key]` devuelve el valor o lanza `KeyError` si la clave no existe.

`d.get(key, default)` devuelve el valor o `default`, o `None`, sin lanzar excepción.

```python
config = {"timeout": 30}
config["timeout"]         # 30
config.get("retries", 3)  # 3
```

**En resumen:**

- `[]` sirve para claves obligatorias.
- `get()` sirve para campos opcionales.
- `get()` reduce la necesidad de `try/except` al leer datos.

</details>

<details>
<summary>56. Describe cómo se pueden actualizar y eliminar elementos de un diccionario.</summary>

#### Python

Actualización:

- `d[key] = value` inserta o actualiza una sola clave;
- `d.update({...})` hace una actualización masiva.

Eliminación:

- `del d[key]` elimina una clave, con error si no existe;
- `d.pop(key, default)` elimina y devuelve el valor;
- `d.popitem()` elimina el último par;
- `d.clear()` limpia todo el diccionario.

**En resumen:**

- Para upsert, sirven `[]` y `update()`.
- Para eliminación segura, suele usarse `pop()`.
- Elige la API según el comportamiento deseado si la clave falta.

</details>

<details>
<summary>57. ¿Para qué sirven los métodos `keys`, `values` e `items` en los diccionarios?</summary>

#### Python

Estos métodos devuelven objetos vista del diccionario:

- `keys()` devuelve todas las claves;
- `values()` devuelve todos los valores;
- `items()` devuelve pares `(key, value)`.

```python
data = {"a": 1, "b": 2}
for key, value in data.items():
    ...
```

Las vistas son dinámicas: reflejan el estado actual del diccionario.

**En resumen:**

- `keys/values/items` sirven para iteración y comprobaciones.
- `items()` es lo más cómodo para recorrer clave y valor en un bucle.
- No son copias, sino vistas "vivas" de los datos.

</details>

<details>
<summary>58. ¿Cómo está implementado `dict` internamente en Python?</summary>

#### Python

`dict` está implementado como una hash table optimizada para memoria y acceso
rápido. La clave se hashea, se elige una celda por el hash y las colisiones se
resuelven con un algoritmo interno de probing.

Consecuencias prácticas:

- el acceso medio es cercano a `O(1)`;
- la calidad de `__hash__` y `__eq__` influye en el comportamiento;
- los objetos mutables no pueden usarse como claves.

**En resumen:**

- `dict` es una estructura hash de alto rendimiento.
- Su velocidad se consigue gracias al hash.
- Las claves deben ser hashable y estables.

</details>

<details>
<summary>59. ¿Qué es una hash function?</summary>

#### Python

Una hash function transforma un objeto en un número entero, el hash, que se
usa para ubicarlo o buscarlo rápidamente en `dict` y `set`.

Condiciones de corrección:

- si `a == b`, entonces `hash(a) == hash(b)`;
- el valor del hash debe ser estable durante la vida del objeto.

**En resumen:**

- La hash function es la base del rendimiento rápido de `dict` y `set`.
- No garantiza unicidad, porque puede haber colisiones.
- En clases personalizadas, `__eq__` y `__hash__` deben ser coherentes.

</details>

<details>
<summary>60. ¿Qué es `set` en Python y en qué se diferencia de otras estructuras de datos?</summary>

#### Python

`set` es una colección no ordenada de elementos **únicos**.

Diferencias:

- elimina duplicados automáticamente;
- ofrece operaciones rápidas de pertenencia, `x in s`;
- soporta operaciones de teoría de conjuntos como unión, intersección y diferencia.

**En resumen:**

- `set` es óptimo para unicidad y membership checks.
- El orden de los elementos no está garantizado.
- Los elementos deben ser hashable.

</details>

<details>
<summary>61. ¿Cómo crear un `set` en Python y qué restricciones existen para sus elementos?</summary>

#### Python

Creación:

```python
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # {1, 2, 3}
empty = set()            # no {}
```

Restricciones:

- los elementos deben ser hashable, por ejemplo `int`, `str`, `tuple`;
- `list`, `dict` y `set` no pueden añadirse directamente.

**En resumen:**

- `set()` crea un conjunto vacío.
- Los duplicados se eliminan automáticamente.
- Solo se permiten elementos hashable.

</details>

<details>
<summary>62. ¿Para qué se usa el método `intersection()` en un set de Python y en qué se diferencia de `union()`?</summary>

#### Python

`intersection()` devuelve los elementos comunes entre conjuntos, mientras que
`union()` reúne todos los elementos únicos de ambos conjuntos.

```python
a = {1, 2, 3}
b = {3, 4}

a.intersection(b)  # {3}
a.union(b)         # {1, 2, 3, 4}
```

**En resumen:**

- `intersection` equivale a intersección, lo común.
- `union` equivale a unión, todo lo único.
- Ambos métodos son básicos para comparar conjuntos de datos.

</details>

<details>
<summary>63. ¿Qué tipos de datos son immutable?</summary>

#### Python

Tipos immutable comunes:

- `int`, `float`, `bool`, `complex`;
- `str`, `bytes`;
- `tuple`, si sus elementos también son immutable;
- `frozenset`;
- `NoneType`.

**En resumen:**

- Un objeto immutable no puede cambiar después de crearse.
- En lugar de mutarlo, se crea un objeto nuevo.
- Estos tipos son más seguros como claves de `dict` y elementos de `set`.

</details>

<details>
<summary>64. ¿Qué tipos de datos son mutable?</summary>

#### Python

Tipos mutable comunes:

- `list`;
- `dict`;
- `set`;
- `bytearray`;
- la mayoría de objetos de clases definidas por el usuario.

**En resumen:**

- Los objetos mutable cambian in-place.
- Las mutaciones pueden generar efectos secundarios por referencias compartidas.
- Hay que tener cuidado con las copias.

</details>

<details>
<summary>65. ¿Por qué es importante entender la mutabilidad al trabajar con diccionarios o sets?</summary>

#### Python

`dict` y `set` se basan en hashing, por lo que sus claves y elementos deben ser
estables y hashable. Los objetos mutable no pueden usarse con seguridad como
claves o elementos de un set.

Además, mutar valores a través de referencias compartidas suele producir bugs
inesperados.

**En resumen:**

- La mutability afecta la corrección de claves en `dict` y `set`.
- Los objetos mutable compartidos suelen causar efectos secundarios.
- Las copias explícitas y el control de mutaciones reducen bugs.

</details>

<details>
<summary>66. ¿Qué es `None`?</summary>

#### Python

`None` es un valor singleton especial del tipo `NoneType` que significa
"ausencia de valor".

Escenarios típicos:

- una función no devuelve nada explícitamente;
- parámetros opcionales;
- marcador de "dato aún no definido".

La comprobación se hace con `is`:

```python
if value is None:
    ...
```

**En resumen:**

- `None` significa ausencia de valor.
- Es un singleton, por eso se compara con `is`.
- Se usa a menudo en APIs como estado opcional.

</details>

<details>
<summary>67. ¿Qué es `id` en Python, cómo se usa y por qué es importante?</summary>

#### Python

`id(obj)` devuelve el identificador del objeto, único dentro del ciclo de vida
del objeto en el proceso actual.

Es útil para diagnóstico:

- saber si es el mismo objeto;
- verificar si se creó una copia;
- detectar si hubo mutación de una referencia compartida.

**En resumen:**

- `id` ayuda a analizar la identidad de los objetos.
- Es útil al depurar copias y mutaciones.
- No se usa como identificador de negocio.

</details>

<details>
<summary>68. ¿Cuál es la diferencia entre los operadores `is` y `==`?</summary>

#### Python

`==` compara **valores**, es decir equivalencia, mientras que `is` compara
**identidad**, o sea si se trata del mismo objeto en memoria.

```python
a = [1, 2]
b = [1, 2]
a == b   # True
a is b   # False
```

**Importante sobre optimizaciones, interning:** CPython cachea enteros pequeños
de `-5` a `256` y strings cortos durante compilación o carga. Por eso, `is`
puede devolver `True` incluso si parecen creados por separado. Pero esto es un
detalle de implementación y no debe usarse en lógica de negocio.

Para `None`, usa siempre `is`.

**En resumen:**

- `==` trata sobre igualdad de valores.
- `is` trata sobre el mismo objeto en memoria.
- El interning puede producir un `is True` inesperado para `int` y `str` pequeños.
- `value is None` es la única forma correcta de comprobar `None`.

</details>

<details>
<summary>69. ¿Cómo se aplica el patrón Singleton en Python? Da ejemplos de objetos de instancia única en Python.</summary>

#### Python

Singleton significa una sola instancia global de un objeto dentro del proceso.
En Python, a menudo se sustituye por el nivel de módulo, ya que los módulos se
importan una sola vez.

Ejemplos de objetos de instancia única del lenguaje:

- `None`;
- `True` y `False`;
- `Ellipsis`.

En código de aplicación, en lugar de un Singleton rígido, suele preferirse un
contenedor de DI o factorías para mejorar la testabilidad.

**En resumen:**

- Python ya tiene objetos de instancia única integrados.
- A menudo basta con el alcance de módulo sin aplicar un patrón separado.
- Abusar de Singleton empeora la testabilidad.

</details>

<details>
<summary>70. ¿Para qué se usan los operadores `break` y `continue` en los bucles de Python?</summary>

#### Python

`break` finaliza el bucle de forma anticipada, mientras que `continue` omite la
iteración actual y pasa a la siguiente.

```python
for n in range(10):
    if n == 5:
        break
    if n % 2 == 0:
        continue
```

**En resumen:**

- `break` detiene el bucle por completo.
- `continue` omite solo el paso actual.
- Hacen que el control del bucle sea explícito y legible.

</details>

<details>
<summary>71. Explica el concepto de un bucle infinito. ¿Cuándo es apropiado usarlo y cómo asegurar su terminación correcta?</summary>

#### Python

Un bucle infinito es un bucle sin una condición natural de finalización, por
ejemplo `while True`. Se usa para procesos en segundo plano o de trabajo, sondeo y lógica de
bucle de eventos.

Terminación correcta:

- una condición `break` clara;
- manejo de señales de terminación;
- tiempos de espera y `try/finally` para la limpieza final.

```python
while True:
    task = queue.get()
    if task is None:
        break
    handle(task)
```

**En resumen:**

- `while True` es adecuado para bucles de servicio de larga duración.
- Hace falta un mecanismo de parada controlado.
- Siempre hay que prever la liberación de recursos.

</details>

<details>
<summary>72. Describe cómo funcionan los bucles anidados en Python. ¿Qué problemas de rendimiento pueden causar y cómo evitarlos?</summary>

#### Python

Un bucle anidado es un bucle dentro de otro. La complejidad suele convertirse
en `O(n*m)` o peor, lo que resulta crítico con grandes volúmenes de datos.

Optimizaciones:

- sustituir búsquedas en listas por `set` o `dict`;
- sacar los invariantes fuera del bucle interno;
- usar generadores, `itertools` y vectorización;
- perfilar las zonas calientes.

**En resumen:**

- Los bucles anidados multiplican rápidamente el coste computacional.
- Las estructuras de datos suelen ser más importantes que las microoptimizaciones.
- El perfilado muestra exactamente qué debe optimizarse.

</details>

<details>
<summary>73. ¿Qué es la coincidencia estructural de patrones (`match`/`case`)?</summary>

#### Python

`match/case` en Python 3.10+ es un mecanismo para analizar estructuras de datos
mediante patrones. Funciona con literales, tipos, secuencias, diccionarios y
clases.

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

**En resumen:**

- `match/case` se lee mejor en ramificaciones complejas.
- Permite comprobar la forma y extraer datos al mismo tiempo.
- Es especialmente útil para protocolos, eventos y parsing de estructuras.

</details>

<details>
<summary>74. ¿En qué casos la coincidencia de patrones es mejor que `if`/`elif`?</summary>

#### Python

`match/case` es mejor cuando necesitas:

- comprobar muchas formas de datos mutuamente excluyentes;
- desempaquetar estructuras anidadas;
- evitar cadenas largas de `if/elif`.

`if/elif` es mejor para condiciones booleanas simples y lógica breve.

**En resumen:**

- Para escenarios estructurales, es mejor `match/case`.
- Para condiciones simples, basta con `if/elif`.
- El criterio de elección es la legibilidad y el mantenimiento.

</details>

<details>
<summary>75. ¿Qué es una función en Python?</summary>

#### Python

Una función es un bloque de código invocable con nombre que recibe argumentos,
devuelve un resultado y permite encapsular lógica.

```python
def normalize_name(name: str) -> str:
    return name.strip().title()
```

Las funciones soportan valores por defecto, argumentos nombrados, `*args/**kwargs`,
anotaciones de tipos y decoradores.

**En resumen:**

- La función es la unidad básica de reutilización de código.
- Define un contrato claro mediante parámetros y valor de retorno.
- Las anotaciones de tipos hacen explícito ese contrato.

</details>

<details>
<summary>76. ¿Qué tipos de argumentos de función existen?</summary>

#### Python

En Python moderno:

- positional-only (`/`);
- posicional o nombrado;
- solo nombrado (`*`);
- variadic positional (`*args`);
- variadic keyword (`**kwargs`).

```python
def f(a, /, b, *, c, **kwargs):
    ...
```

**En resumen:**

- Python ofrece un control flexible sobre cómo se llama una función.
- `/` y `*` formalizan el contrato de la API.
- `*args/**kwargs` son útiles para interfaces extensibles.

</details>

<details>
<summary>77. ¿Qué son los argumentos posicionales y los argumentos nombrados?</summary>

#### Python

Los argumentos posicionales se pasan por orden, y los argumentos nombrados
se pasan por nombre del parámetro.

```python
def connect(host: str, port: int) -> str:
    return f"{host}:{port}"

connect("localhost", 5432)           # posicional
connect(host="localhost", port=5432) # nombrado
```

**En resumen:**

- Los posicionales dependen del orden de los parámetros.
- Los nombrados mejoran la legibilidad de la llamada.
- Se pueden combinar respetando las reglas de la firma.

</details>

<details>
<summary>78. ¿Qué son los argumentos por defecto y qué problemas pueden tener?</summary>

#### Python

Los argumentos por defecto se usan cuando no se pasa un valor en la llamada.
Se evalúan **una sola vez** al definir la función.

Problema: valor mutable por defecto.

```python
def add_item(item: int, bucket: list[int] | None = None) -> list[int]:
    if bucket is None:
        bucket = []
    bucket.append(item)
    return bucket
```

**En resumen:**

- Los valores por defecto son cómodos para valores estables.
- Un valor mutable por defecto puede acumular estado entre llamadas.
- El patrón seguro es `None` más inicialización interna.

</details>

<details>
<summary>79. Explica el propósito y uso de `*args` y `**kwargs` en funciones de Python. ¿En qué se diferencian?</summary>

#### Python

`*args` recoge argumentos posicionales adicionales en un `tuple`. `**kwargs`
recoge argumentos nombrados adicionales en un `dict`.

```python
def log_event(event: str, *args: object, **kwargs: object) -> None:
    ...
```

Usos típicos: envoltorios, adaptadores de API, decoradores y reenvío de parámetros.

**En resumen:**

- `*args` significa posicionales adicionales.
- `**kwargs` significa nombrados adicionales.
- Hacen las funciones más flexibles, pero requieren validación clara.

</details>

<details>
<summary>80. ¿Cómo definir una función con anotaciones de tipos en Python? Da un ejemplo y explica las ventajas de este enfoque.</summary>

#### Python

Los tipos se indican en la firma de los parámetros y en el valor de retorno.

```python
def process_users(users: list[dict[str, object]]) -> list[str]:
    return [str(user["name"]) for user in users if bool(user.get("active"))]
```

Ventajas:

- mejor experiencia de desarrollo, como autocompletado y navegación;
- comprobación estática en CI;
- contrato explícito para otros desarrolladores.

**En resumen:**

- Las anotaciones de tipos documentan la API.
- Reducen el riesgo de errores de integración.
- Aportan más valor en bases de código medianas y grandes.

</details>

<details>
<summary>81. ¿Qué son las funciones lambda?</summary>

#### Python

`lambda` es una función anónima de una sola expresión. Normalmente se usa para
funciones de devolución de llamada cortas en `sorted`, `map` y `filter`.

```python
users = [{"name": "Ada"}, {"name": "Bob"}]
users_sorted = sorted(users, key=lambda u: u["name"])
```

Para lógica compleja, es mejor una función normal definida con `def`.

**En resumen:**

- `lambda` es cómoda para expresiones locales cortas.
- Está limitada a una sola expresión.
- Para mantener la legibilidad, el código complejo debe ir en una `def`.

</details>

<details>
<summary>82. ¿Cuál es el alcance de las variables dentro de una función?</summary>

#### Python

Python usa la regla LEGB para buscar nombres:

- `L`ocal;
- `E`nclosing, funciones externas;
- `G`lobal, módulo;
- `B`uiltins, nombres integrados.

Dentro de una función, una asignación crea una variable local si no se declara
`global` o `nonlocal`.

**En resumen:**

- El alcance define dónde un nombre está disponible y puede modificarse.
- LEGB explica el orden de búsqueda de variables.
- Entender mal el alcance suele provocar `UnboundLocalError`.

</details>

<details>
<summary>83. ¿Qué son las variables locales y globales en Python?</summary>

#### Python

Las variables locales viven dentro del cuerpo de una función. Las variables
globales se definen a nivel de módulo.

Para modificar una global desde una función hace falta `global`, pero
normalmente conviene evitarlo por las dependencias implícitas que crea.

**En resumen:**

- Las locales son más seguras para mantenimiento y pruebas.
- Las globales simplifican el acceso, pero complican el control del estado.
- Es mejor pasar las dependencias como parámetros.

</details>

<details>
<summary>84. ¿Cuál es la diferencia entre variables locales y nonlocal en Python?</summary>

#### Python

`nonlocal` se usa dentro de una función anidada para modificar una variable del
alcance envolvente más cercano, no del alcance global.

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

**En resumen:**

- Una variable local pertenece a la función actual.
- `nonlocal` modifica el estado de la función externa.
- Es un mecanismo clave para cierres con estado.

</details>

<details>
<summary>85. ¿Qué es el desempaquetado en Python y cómo se aplica en asignaciones?</summary>

#### Python

El desempaquetado es descomponer los elementos de una secuencia o estructura en
variables separadas.

```python
x, y = (10, 20)
first, *middle, last = [1, 2, 3, 4]
```

También funciona con diccionarios en `match/case`, en llamadas de funciones y
en bucles.

**En resumen:**

- El desempaquetado hace el código más compacto y legible.
- Soporta la captura del resto de valores con el operador estrella.
- Se usa a menudo al parsear estructuras de datos.

</details>

<details>
<summary>86. Explica el concepto de empaquetado de valores en Python y da ejemplos.</summary>

#### Python

El empaquetado es reunir varios valores en una sola estructura como `tuple`, `list` o
`dict`.

```python
point = 10, 20                 # empaquetado en tuple

def collect(*args: int) -> tuple[int, ...]:
    return args
```

`*args` y `**kwargs` son ejemplos típicos de empaquetado de argumentos.

**En resumen:**

- El empaquetado reúne muchos valores en un solo contenedor.
- Se usa con mucha frecuencia en firmas de funciones.
- Combina bien con el desempaquetado del lado de la llamada.

</details>

<details>
<summary>87. ¿Para qué se usa el operador `*` en el empaquetado y desempaquetado?</summary>

#### Python

En parámetros de función, `*` empaqueta argumentos posicionales en `*args`, y
en la llamada desempaqueta un iterable en argumentos posicionales.

```python
def add(a: int, b: int) -> int:
    return a + b

nums = [2, 3]
add(*nums)  # 5
```

También se usa en asignaciones para capturar "el resto" de los elementos.

**En resumen:**

- `*` es un operador universal para trabajar con argumentos variables.
- En la firma empaqueta y en la llamada desempaqueta.
- Reduce el código repetitivo al pasar datos.

</details>

<details>
<summary>88. ¿Qué es un cierre y qué relación tiene con los decoradores?</summary>

#### Python

Un cierre es una función interna que "recuerda" las variables del alcance envolvente
incluso después de que la función externa haya terminado.

Un decorador suele implementarse precisamente mediante un cierre: la envoltura
conserva una referencia a la función original y a parámetros adicionales.

**En resumen:**

- Un cierre es función más contexto capturado.
- Un decorador suele ser una aplicación práctica de un cierre.
- Permite añadir comportamiento sin cambiar el cuerpo de la función.

</details>

<details>
<summary>89. ¿Qué es un decorador en Python y cómo funciona?</summary>

#### Python

Un decorador es un objeto invocable que recibe una función o clase y devuelve una
versión modificada, una envoltura.

```python
from functools import wraps

def log_calls(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs)
    return wrapper
```

Aplicaciones típicas: registro, caché, autorización, reintentos y métricas.

**En resumen:**

- Un decorador añade comportamiento transversal.
- Funciona envolviendo un objeto invocable.
- Evita duplicar lógica técnica dentro del código de negocio.

</details>

<details>
<summary>90. ¿Se pueden usar varios decoradores en una misma función?</summary>

#### Python

Sí, se pueden apilar varios decoradores. Se aplican de abajo hacia arriba: el
más cercano a `def` envuelve primero.

```python
@decorator_a
@decorator_b
def handler() -> None:
    ...
```

Equivalente: `handler = decorator_a(decorator_b(handler))`.

**En resumen:**

- Usar varios decoradores es válido y común.
- El orden de aplicación importa.
- La pila de decoradores debe documentarse para mantener claridad.

</details>

<details>
<summary>91. Describe un posible problema con el orden de los decoradores al aplicarlos a una función.</summary>

#### Python

Un orden incorrecto puede cambiar la semántica: por ejemplo, aplicar caché antes
de una comprobación de acceso puede almacenar un resultado no deseado o saltarse
la lógica esperada.

Riesgos típicos:

- el registro ve argumentos ya modificados;
- los reintentos envuelven la excepción equivocada;
- la caché se aplica antes o después de la validación en el punto incorrecto.

**En resumen:**

- El orden de los decoradores afecta al comportamiento de la función.
- Es una causa frecuente de bugs ocultos.
- Las cadenas críticas necesitan pruebas sobre el orden de ejecución.

</details>

<details>
<summary>92. ¿Se puede crear un decorador con una clase?</summary>

#### Python

Sí. Una clase decoradora implementa `__call__` para que su instancia se comporte
como una función.

```python
class CallCounter:
    def __init__(self, func):
        self.func = func
        self.calls = 0

    def __call__(self, *args, **kwargs):
        self.calls += 1
        return self.func(*args, **kwargs)
```

**En resumen:**

- Un decorador puede implementarse no solo con una función, sino también con una clase.
- La clase es útil cuando se necesita estado interno.
- El mecanismo clave es `__call__`.

</details>

<details>
<summary>93. ¿Cómo definir un decorador que acepta parámetros?</summary>

#### Python

Hace falta una estructura de tres niveles: fábrica de decoradores, decorador y envoltura.

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

**En resumen:**

- Un decorador parametrizado es una función que devuelve otro decorador.
- A menudo se usa un cierre para conservar los parámetros.
- Este enfoque es cómodo para comportamiento configurable.

</details>

<details>
<summary>94. ¿Para qué se usa `functools.wraps` en funciones decoradoras?</summary>

#### Python

`functools.wraps` copia los metadatos de la función original a la envoltura: nombre,
docstring, módulo y también `__wrapped__`.

Esto es importante para:

- depuración y logs correctos;
- introspección y documentación;
- compatibilidad con herramientas que leen la firma.

**En resumen:**

- `wraps` conserva la "identidad" de la función original.
- Sin él, las funciones decoradas pierden metadatos útiles.
- Es una buena práctica para todos los decoradores de envoltura.

</details>

<details>
<summary>95. ¿Cómo funcionan dict comprehension, list comprehension y set comprehension?</summary>

#### Python

Una comprehension crea una colección a partir de una expresión y uno o varios
bucles, opcionalmente con filtro.

```python
squares = [x * x for x in range(6)]
mapping = {x: x * x for x in range(6)}
unique = {x % 3 for x in range(10)}
```

Formato:

- list: `[expr for x in it if cond]`
- set: `{expr for x in it if cond}`
- dict: `{k_expr: v_expr for x in it if cond}`

**En resumen:**

- Una comprehension expresa transformaciones de datos de forma compacta.
- Funciona con `list`, `set` y `dict`.
- Produce un código más limpio que agregar elementos manualmente en un bucle.

</details>

<details>
<summary>96. ¿Qué ventajas tienen las list comprehensions frente a los bucles normales?</summary>

#### Python

Ventajas:

- código más corto y declarativo;
- menos variables auxiliares;
- normalmente un poco mejor de rendimiento en CPython;
- menor riesgo de olvidar `append`.

Desventaja: para lógica muy compleja, una comprehension empeora la legibilidad.

**En resumen:**

- Una list comprehension es ideal para transformaciones simples.
- A menudo es más rápida y más limpia que un bucle manual.
- Para ramas complejas, es mejor un `for` normal.

</details>

<details>
<summary>97. ¿Puedes dar un ejemplo de una list comprehension anidada?</summary>

#### Python

Ejemplo de flatten de una matriz:

```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [item for row in matrix for item in row]  # [1, 2, 3, 4, 5, 6]
```

Ejemplo con condición:

```python
pairs = [(x, y) for x in range(3) for y in range(3) if x != y]
```

**En resumen:**

- Una comprehension anidada son varios `for` dentro de una sola expresión.
- El orden de los `for` corresponde al de los bucles anidados.
- Úsala cuando la expresión siga siendo legible.

</details>

<details>
<summary>98. ¿Qué es más rápido en Python: una list comprehension o crear una lista con un bucle?</summary>

#### Python

En escenarios típicos, una list comprehension es un poco más rápida que un
bucle con `append`, porque tiene bytecode optimizado y menos sobrecarga.

Importante: la mejora real depende del cuerpo de la operación, así que en zonas
críticas conviene medir con `timeit` o `pyperf`.

**En resumen:**

- A menudo la list comprehension es más rápida.
- La diferencia puede ser pequeña.
- Para decisiones de producción, guíate por mediciones.

</details>

<details>
<summary>99. ¿Qué es un iterador en Python?</summary>

#### Python

Un iterador es un objeto que devuelve elementos secuencialmente y recuerda su
estado actual. Implementa el protocolo:

- `__iter__()` devuelve a sí mismo;
- `__next__()` devuelve el siguiente elemento o lanza `StopIteration`.

**En resumen:**

- Un iterador da acceso elemento por elemento sin cargar todos los datos.
- Es la base de `for`, de los generadores y del procesamiento perezoso.
- Una vez agotado, un iterador no se reinicia solo.

</details>

<details>
<summary>100. ¿Cómo crear un iterador a partir de un objeto iterable usando la función `iter()`?</summary>

#### Python

Llama a `iter(iterable)` para obtener un iterador.

```python
items = [10, 20, 30]
it = iter(items)
```

Después de eso, los valores se leen con `next(it)`.

**En resumen:**

- `iter()` convierte un iterable en un iterador.
- Es una forma explícita de controlar la iteración manualmente.
- Se usa en procesamiento de flujos de datos a bajo nivel.

</details>

<details>
<summary>101. ¿Para qué sirve la función `next()` al trabajar con iterators?</summary>

#### Python

`next(iterator[, default])` devuelve el siguiente elemento del iterador. Cuando
los elementos se han agotado, lanza `StopIteration` o devuelve `default` si se
ha pasado.

```python
it = iter([1, 2])
next(it)        # 1
next(it)        # 2
next(it, None)  # None
```

**En resumen:**

- `next()` da control manual sobre cada paso de la iteración.
- Sin `default`, el final del flujo produce `StopIteration`.
- Con `default`, se puede leer el flujo de forma segura.

</details>

<details>
<summary>102. ¿Se pueden usar de forma intercambiable los métodos `__next__()` y `__iter__()` con las funciones `next()` e `iter()`?</summary>

#### Python

Sí, pero con el matiz del protocolo:

- `iter(obj)` llama a `obj.__iter__()`;
- `next(it)` llama a `it.__next__()`.

Es decir, estas funciones son la interfaz estándar para los métodos dunder y
normalmente se usan en lugar de invocarlos directamente.

**En resumen:**

- `iter()` corresponde a `__iter__()`.
- `next()` corresponde a `__next__()`.
- En código de aplicación, es mejor usar las funciones integradas.

</details>

<details>
<summary>103. ¿Qué papel tiene `StopIteration` en el diseño de iterators y cuándo suele aparecer?</summary>

#### Python

`StopIteration` indica que el iterador se ha agotado. El bucle `for` lo captura
automáticamente y finaliza la iteración.

Normalmente aparece:

- al llamar a `next(it)` después del último elemento;
- en iterators personalizados, cuando los datos se terminan.

**En resumen:**

- `StopIteration` es el final normal del flujo.
- No debe registrarse como "error" dentro del flujo normal.
- En iterators propios, debe lanzarse correctamente.

</details>

<details>
<summary>104. ¿Qué es un generador y en qué se diferencia de un iterador o de una función normal?</summary>

#### Python

Un generador es un iterador especial que se crea con una función que usa
`yield`. Genera valores uno por uno y conserva su estado interno entre llamadas.

Diferencias:

- frente a una función normal: no termina con un único `return`, sino que
  funciona con "pausa/reanudación";
- frente a un iterador manual: tiene una implementación más simple, sin una
  clase explícita con `__next__`.

**En resumen:**

- Un generador es la forma más cómoda de hacer iteración perezosa.
- Requiere menos código que una clase iteradora personalizada.
- Es especialmente útil para grandes flujos de datos.

</details>

<details>
<summary>105. ¿Cómo se crea una función generadora?</summary>

#### Python

Hay que definir una función con `yield`.

```python
def countdown(start: int):
    current = start
    while current > 0:
        yield current
        current -= 1
```

La llamada `countdown(3)` devuelve un objeto generador que se puede iterar.

**En resumen:**

- La presencia de `yield` convierte la función en un generador.
- Un generador devuelve valores por etapas.
- El estado de la función se conserva entre iteraciones.

</details>

<details>
<summary>106. ¿Cómo proporciona la palabra clave `yield` la funcionalidad de los generadores y por qué ahorran memoria?</summary>

#### Python

`yield` devuelve el siguiente valor y "congela" el contexto de la función
(variables locales, posición de ejecución). El siguiente `next()` reanuda la
ejecución desde ese punto.

El ahorro de memoria se debe a que los datos no se crean por completo de
antemano, sino que se calculan bajo demanda.

**En resumen:**

- `yield` implementa la pausa y la reanudación de la ejecución.
- Un generador soporta evaluación perezosa.
- Esto reduce el consumo de memoria en conjuntos de datos grandes.

</details>

<details>
<summary>107. ¿Cuál es la diferencia entre `return` y `yield`?</summary>

#### Python

`return` finaliza la función y devuelve un único valor final. `yield` devuelve
un valor intermedio y conserva el estado para poder continuar después.

En un generador, `return` significa el final de la iteración (`StopIteration`).

**En resumen:**

- `return` -> finalización de la función.
- `yield` -> entrega de valores por etapas.
- `yield` se usa para procesamiento en flujo.

</details>

<details>
<summary>108. ¿Qué es la programación orientada a objetos (POO) y cuáles son sus principios principales en Python?</summary>

#### Python

La POO es un enfoque en el que los datos y el comportamiento se agrupan en objetos.

Principios clave:

- encapsulación;
- herencia;
- polimorfismo;
- abstracción.

En Python, la POO suele combinarse con composición y tipado por comportamiento.

**En resumen:**

- La POO estructura el dominio mediante clases y objetos.
- Python soporta la POO de forma flexible, sin demasiado código ceremonial.
- En la práctica, la composición suele ser mejor que una herencia profunda.

</details>

<details>
<summary>109. ¿Qué es una `class` en Python?</summary>

#### Python

Una `class` es una plantilla para crear objetos con atributos y
métodos.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name
```

La clase define la estructura y el comportamiento de futuras instancias.

**En resumen:**

- Una clase describe los datos y las operaciones sobre ellos.
- A partir de una clase se crean objetos (instancias).
- Es la unidad básica de modelado en POO.

</details>

<details>
<summary>110. ¿Cómo se crea un objeto en Python?</summary>

#### Python

Un objeto se crea llamando a la clase:

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

user = User("Ada")
```

Durante la creación, se ejecuta `__init__` para inicializar el estado.

**En resumen:**

- Objeto = instancia de una clase.
- Creación: `instancia = ClassName(...)`.
- `__init__` configura los atributos iniciales.

</details>

<details>
<summary>111. ¿Qué son los objetos y los atributos?</summary>

#### Python

Un objeto es una instancia concreta de un tipo o clase. Un atributo es un par
nombre-valor asociado al objeto (dato o método).

```python
user.name       # atributo de datos
user.save()     # atributo método
```

**En resumen:**

- Un objeto almacena estado y comportamiento.
- Los atributos describen ese estado y comportamiento.
- El acceso a los atributos se hace con notación de punto.

</details>

<details>
<summary>112. ¿Qué papel cumple el método `__init__()` en una clase?</summary>

#### Python

`__init__` es el inicializador de la instancia: se llama después de crear el
objeto y rellena su estado inicial.

```python
class Account:
    def __init__(self, owner: str, balance: float = 0.0) -> None:
        self.owner = owner
        self.balance = balance
```

**En resumen:**

- `__init__` define los atributos iniciales del objeto.
- Funciona como punto de entrada para configurar la instancia.
- No crea el objeto, solo lo inicializa.

</details>

<details>
<summary>113. ¿Para qué sirve el parámetro `self` en los métodos de clase de Python?</summary>

#### Python

`self` es una referencia a la instancia actual. A través de él, el método lee y
modifica los atributos de la instancia.

```python
def deposit(self, amount: float) -> None:
    self.balance += amount
```

El nombre `self` no está reservado por la sintaxis, pero es el estándar
aceptado de forma general.

**En resumen:**

- `self` vincula el método con un objeto concreto.
- A través de `self` se accede a los datos de la instancia.
- Es el primer parámetro obligatorio de un método de instancia.

</details>

<details>
<summary>114. ¿Cómo se definen los métodos dentro de una clase?</summary>

#### Python

Los métodos se definen como funciones dentro de una `class`.

```python
class Calculator:
    def add(self, a: int, b: int) -> int:
        return a + b
```

Tipos habituales: de instancia (`self`), de clase (`@classmethod`, `cls`) y estático
(`@staticmethod`, sin `self/cls`).

**En resumen:**

- Un método es una función dentro del cuerpo de una clase.
- El tipo de método lo determinan el decorador y la firma.
- El más común es el método de instancia.

</details>

<details>
<summary>115. Explique el concepto de "todo es un objeto" en Python y dé ejemplos.</summary>

#### Python

En Python, casi todo es un objeto: números, strings, funciones, clases y
módulos. Por eso, todo tiene tipo, atributos y comportamiento.

```python
type(10)          # <class 'int'>
type(len)         # <class 'builtin_function_or_method'>
type(str)         # <class 'type'>
```

**En resumen:**

- Un modelo de objetos unificado simplifica el lenguaje.
- Las funciones y las clases también son objetos de primera clase.
- Esto hace que Python sea flexible para metaprogramación.

</details>

<details>
<summary>116. Dé un ejemplo de una clase con métodos que realicen cálculos basados en atributos.</summary>

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

**En resumen:**

- Los métodos pueden calcular valores a partir de los atributos de la instancia.
- Esto encapsula la lógica de dominio dentro del objeto.
- La API de la clase se vuelve más autodocumentada.

</details>

<details>
<summary>117. Describa una situación en la que pueda ser necesario usar varias clases en un programa de Python.</summary>

#### Python

Cuando el dominio tiene varias responsabilidades, se reparten entre distintas
clases. Por ejemplo, en e-commerce: `Order`, `OrderItem`, `PaymentService`,
`InventoryService`.

Esto aporta:

- una separación clara de responsabilidades;
- menor acoplamiento;
- sustitución y pruebas de componentes más simples.

**En resumen:**

- Varias clases hacen falta para modelar un dominio complejo.
- Separar responsabilidades mejora el mantenimiento.
- La composición de clases suele ser mejor que un "god object".

</details>

<details>
<summary>118. ¿Cuál es la diferencia entre método de instancia, método de clase y método estático?</summary>

#### Python

- Método de instancia: tiene `self` y trabaja con una instancia concreta.
- Método de clase: tiene `cls` y trabaja con la clase en general.
- Método estático: no tiene `self/cls`; es una función utilitaria dentro del
  espacio de nombres de la clase.

**En resumen:**

- Instancia -> lógica de la instancia.
- Clase -> lógica de la clase o constructores alternativos.
- Static -> lógica auxiliar sin acceso al estado.

</details>

<details>
<summary>119. ¿Qué es `@classmethod` en Python y en qué se diferencia de los métodos normales?</summary>

#### Python

`@classmethod` pasa la clase (`cls`) como primer argumento, no la instancia. A
menudo se usa para métodos factoría.

```python
class User:
    def __init__(self, name: str) -> None:
        self.name = name

    @classmethod
    def from_email(cls, email: str) -> User:
        return cls(email.split("@")[0])
```

**En resumen:**

- `classmethod` trabaja a nivel de clase.
- Es cómodo para constructores alternativos.
- No requiere una instancia ya creada.

</details>

<details>
<summary>120. ¿Qué es `@staticmethod` en las clases de Python y cuándo conviene usarlo?</summary>

#### Python

`@staticmethod` define un método sin `self` ni `cls` automáticos. Pertenece
lógicamente a la clase, pero no depende de su estado.

```python
class Math:
    @staticmethod
    def clamp(value: int, min_v: int, max_v: int) -> int:
        return max(min_v, min(value, max_v))
```

**En resumen:**

- `staticmethod` es una función dentro del espacio de nombres de la clase.
- Úsalo para lógica auxiliar sin acceso a atributos.
- No sirve si necesitas estado de instancia o de clase.

</details>

<details>
<summary>121. ¿Cuál es la diferencia entre `@classmethod` y `@staticmethod` en las clases de Python?</summary>

#### Python

La diferencia está en el primer argumento y en el nivel de acceso:

- `@classmethod` recibe `cls` y puede trabajar con el estado de la clase;
- `@staticmethod` no recibe nada automáticamente.

`classmethod` se usa más a menudo para factorías o constructores polimórficos,
y `staticmethod` para utilidades.

**En resumen:**

- `classmethod` conoce la clase.
- `staticmethod` está aislado del estado de clase y de instancia.
- La elección depende de si necesitas acceso a `cls`.

</details>

<details>
<summary>122. ¿Qué son los atributos de instancia en las clases de Python y en qué se diferencian de los atributos de clase?</summary>

#### Python

Los atributos de instancia pertenecen a un objeto concreto (`self.x`). Los
atributos de clase pertenecen a la clase y se comparten entre todas las
instancias.

```python
class User:
    role = "member"           # atributo de clase
    def __init__(self, name: str) -> None:
        self.name = name      # atributo de instancia
```

**En resumen:**

- Los atributos de instancia almacenan estado individual.
- Los atributos de clase almacenan configuración compartida.
- Las mutaciones de atributos de clase afectan a todas las instancias.

</details>

<details>
<summary>123. ¿Qué es `__slots__` en Python?</summary>

#### Python

`__slots__` limita el conjunto de atributos permitidos en una clase y puede
reducir el consumo de memoria al eliminar `__dict__` en las instancias.

```python
class Point:
    __slots__ = ("x", "y")
    def __init__(self, x: int, y: int) -> None:
        self.x = x
        self.y = y
```

**Matices de uso:**

- **Ahorro de memoria:** los objetos ocupan bastante menos espacio, porque los
  atributos se almacenan en un array fijo y no en la tabla hash `__dict__`.
- **Velocidad:** el acceso a atributos con `__slots__` suele ser un poco más rápido.
- **Ausencia de `__dict__`:** no podrás añadir dinámicamente nuevos atributos
  que no estén en la lista `__slots__` (a menos que añadas `"__dict__"` a la
  propia lista).
- **Referencias débiles:** si quieres usar `weakref`, debes añadir
  explícitamente `"__weakref__"` a `__slots__`.

**En resumen:**

- `__slots__` es útil para millones de objetos ligeros, por ejemplo nodos de un grafo.
- Elimina `__dict__` y `__weakref__` por defecto.
- Reduce flexibilidad a cambio de rendimiento y control.

</details>

<details>
<summary>124. ¿Qué son los magic methods (métodos dunder) en las clases de Python y por qué se llaman "mágicos"?</summary>

#### Python

Los métodos dunder (`__init__`, `__str__`, `__len__`, `__eq__`, ...) son puntos
de enganche especiales que Python llama automáticamente en respuesta a
operadores y funciones integradas.

Se llaman "mágicos" porque integran tu clase en el comportamiento del lenguaje.

**En resumen:**

- Los métodos dunder definen el comportamiento protocolario del objeto.
- Permiten que tus clases se comporten "como tipos integrados".
- Úsalos solo cuando haya una necesidad semántica clara.

</details>

<details>
<summary>125. ¿Para qué sirve el método `__del__`?</summary>

#### Python

`__del__` es un finalizador que puede llamarse antes de que el GC destruya el
objeto. Su comportamiento no es determinista, así que para gestionar recursos
es mejor usar gestores de contexto (`with`) y cierre explícito.

**En resumen:**

- `__del__` no garantiza una ejecución oportuna.
- No apoyes una limpieza crítica solo en él.
- El enfoque recomendado es `with` o `try-finally`.

</details>

<details>
<summary>126. Dé un ejemplo de uso del método mágico `__str__` para definir la representación textual de una clase propia en Python.</summary>

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

`str(user)` y `print(user)` usarán `__str__`.

**En resumen:**

- `__str__` da una representación comprensible para humanos del objeto.
- Es útil para logs y salida en CLI.
- Debe ser corto y legible.

</details>

<details>
<summary>127. ¿Para qué se usan `__str__` y `__repr__`?</summary>

#### Python

`__str__` está orientado al lector final. `__repr__` está orientado al
desarrollador y a la depuración, y es deseable que sea inequívoco.

`print(obj)` usa principalmente `__str__`, mientras que REPL y `repr(obj)` usan
`__repr__`.

**En resumen:**

- `__str__` sirve para una salida amigable.
- `__repr__` sirve para una representación técnica.
- Es buena práctica tener ambos si la clase es de dominio.

</details>

<details>
<summary>128. ¿Cómo funciona la sobrecarga de operadores en Python y por qué es útil?</summary>

#### Python

La sobrecarga de operadores es la implementación de métodos dunder de
operadores (`__add__`, `__sub__`, `__eq__`, ...) para que los objetos de tu
propia clase soporten operadores.

```python
class Vector2:
    def __init__(self, x: float, y: float) -> None:
        self.x = x
        self.y = y

    def __add__(self, other: "Vector2") -> "Vector2":
        return Vector2(self.x + other.x, self.y + other.y)
```

**En resumen:**

- Da una sintaxis natural para tipos de dominio.
- Mejora la expresividad de la API.
- Es importante mantener una semántica matemáticamente esperable.

</details>

<details>
<summary>129. ¿Qué es la herencia?</summary>

#### Python

La herencia permite crear una clase hija que hereda atributos y métodos de una
clase base y puede ampliar o sobrescribir su comportamiento.

**En resumen:**

- La herencia favorece la reutilización de código.
- La clase hija puede sobrescribir métodos de la clase base.
- Una jerarquía excesiva complica el mantenimiento, por eso la composición suele ser mejor.

</details>

<details>
<summary>130. ¿Qué es la herencia simple en Python?</summary>

#### Python

La herencia simple significa que una clase tiene solo un padre directo.

```python
class Animal:
    ...

class Dog(Animal):
    ...
```

Esta es la forma más simple y normalmente la más legible de herencia.

**En resumen:**

- Una clase hija -> una clase base.
- Modelo de resolución de métodos simple.
- Suele ser suficiente para la mayoría de modelos de negocio.

</details>

<details>
<summary>131. ¿Cómo se implementa la herencia en las clases de Python y qué sintaxis se usa para ello?</summary>

#### Python

La sintaxis es `class Child(Base):`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return "hi"
```

Si necesitas llamar a la lógica base, usa `super()`.

**En resumen:**

- La herencia se define entre paréntesis después del nombre de la clase.
- La clase hija recibe la API de la clase base.
- La sobrescritura permite adaptar el comportamiento.

</details>

<details>
<summary>132. ¿Cómo acceder a los miembros de la clase base desde una clase hija?</summary>

#### Python

El acceso es posible directamente a través de atributos y métodos heredados o
mediante `super()`.

```python
class Base:
    def greet(self) -> str:
        return "hello"

class Child(Base):
    def greet(self) -> str:
        return super().greet() + " world"
```

**En resumen:**

- Los miembros heredados están disponibles automáticamente en la clase hija.
- `super()` llama correctamente a la lógica de la clase base.
- Esto es importante para ampliar comportamiento, no para duplicarlo.

</details>

<details>
<summary>133. ¿Para qué sirve la función `super()` en la herencia de Python y cómo se usa?</summary>

#### Python

`super()` devuelve un proxy a la siguiente clase según el MRO para llamar a sus
métodos. Se usa típicamente en `__init__` y en herencia múltiple cooperativa.

```python
class Child(Base):
    def __init__(self, value: int) -> None:
        super().__init__()
        self.value = value
```

**En resumen:**

- `super()` llama a la implementación padre sin fijar el nombre de la clase.
- Ayuda a mantener la corrección del MRO.
- Es la forma recomendada de trabajar con herencia.

</details>

<details>
<summary>134. Describa la función `isinstance()` en Python y dé un ejemplo de uso.</summary>

#### Python

`isinstance(obj, cls_or_tuple)` comprueba si un objeto pertenece a un tipo o a
su subclase.

```python
isinstance(10, int)                 # True
isinstance(True, int)               # True
isinstance("x", (str, bytes))       # True
```

**En resumen:**

- `isinstance` es más seguro que `type(obj) is ...` en código polimórfico.
- Tiene en cuenta la jerarquía de herencia.
- Soporta tuplas de tipos.

</details>

<details>
<summary>135. Explique la función `issubclass()` en Python y dé un ejemplo de uso.</summary>

#### Python

`issubclass(Sub, Base)` comprueba si la clase `Sub` es subclase de `Base`.

```python
class Animal: ...
class Dog(Animal): ...

issubclass(Dog, Animal)  # True
```

**En resumen:**

- Trabaja con clases, no con instancias.
- Es útil para validar APIs a nivel de tipos.
- Tiene en cuenta la herencia transitiva.

</details>

<details>
<summary>136. ¿Qué es la herencia múltiple?</summary>

#### Python

La herencia múltiple es la herencia de una clase a partir de varias clases base.

```python
class A: ...
class B: ...
class C(A, B): ...
```

Da flexibilidad, pero exige disciplina en el diseño de métodos y en `super()`.

**En resumen:**

- Una clase puede heredar comportamiento de varias fuentes.
- Es útil para el enfoque basado en mixins.
- Puede hacer más difícil entender el MRO.

</details>

<details>
<summary>137. ¿Cómo funciona el MRO (Method Resolution Order) en la herencia múltiple?</summary>

#### Python

El MRO define el orden de búsqueda de métodos en la jerarquía de clases. En
Python se usa el algoritmo de linealización C3.

**Diamond Problem (problema del diamante):** es el caso clásico en el que la
clase `D` hereda de `B` y `C`, y ambas heredan de `A`. El MRO garantiza que
`A` se revisará solo después de que se hayan revisado todos sus descendientes
(`B` y `C`).

```python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass

print(D.mro())
# [D, B, C, A, object]
```

El orden puede verse mediante `ClassName.__mro__` o `ClassName.mro()`.

**En resumen:**

- El MRO decide de qué clase base tomar un método.
- El orden es predecible y está definido formalmente (C3).
- Gracias al MRO, Python maneja correctamente el problema del diamante.
- Para la herencia cooperativa, todas las clases deben llamar a `super()`.

</details>

<details>
<summary>138. ¿Cuáles son las ventajas y desventajas de usar herencia múltiple?</summary>

#### Python

Ventajas:

- reutilización de comportamiento desde varias fuentes;
- mixins cómodos para "añadir" capacidades.

Desventajas:

- MRO más complejo;
- riesgo de conflictos de nombres o comportamiento;
- depuración e incorporación más difíciles.

**En resumen:**

- La herencia múltiple es potente, pero exige reglas de diseño estrictas.
- Para la mayoría de casos, la composición es más simple.
- Usa herencia múltiple sobre todo para mixins pequeños.

</details>

<details>
<summary>139. ¿Qué son los mixins?</summary>

#### Python

Un mixin es una clase pequeña con comportamiento adicional y específico, pensada
para combinarse mediante herencia y no para usarse por sí sola.

Ejemplos: `TimestampMixin`, `JsonSerializableMixin`.

**En resumen:**

- Un mixin añade una capacidad concreta.
- Normalmente no tiene su propio ciclo de vida completo.
- Encaja bien con la herencia múltiple.

</details>

<details>
<summary>140. ¿Qué es la encapsulación en Python?</summary>

#### Python

La encapsulación es ocultar la implementación interna detrás de una API pública
estable. En Python se implementa principalmente con convenciones y `property`,
no con modificadores de acceso rígidos.

**En resumen:**

- El código cliente trabaja con la interfaz, no con los detalles.
- La encapsulación reduce el acoplamiento entre componentes.
- Facilita cambiar la implementación interna sin romper la API.

</details>

<details>
<summary>141. ¿Cuál es la diferencia entre acceso público, privado y protegido?</summary>

#### Python

En Python esto son principalmente convenciones de nombres:

- `public`: `name` -> accesible en todas partes;
- `protected`: `_name` -> uso interno por convención;
- `private`: `__name` -> cambio interno de nombre (`_ClassName__name`), no protección
  absoluta.

**En resumen:**

- Python no tiene modificadores de acceso estrictos como Java o C#.
- `_name` y `__name` son señales de intención para desarrolladores.
- El control real de acceso se construye mediante diseño de API.

</details>

<details>
<summary>142. ¿Qué es el polimorfismo y cómo se implementa en Python?</summary>

#### Python

El polimorfismo es la posibilidad de trabajar con distintos objetos a través de
una interfaz común. En Python suele implementarse con duck typing y protocolos.

```python
def render(obj) -> str:
    return obj.to_text()
```

Cualquier objeto con un método `to_text` sirve.

**En resumen:**

- Una interfaz, muchas implementaciones.
- En Python, el polimorfismo suele ser conductual, no jerárquico.
- Esto simplifica ampliar el sistema con nuevos tipos.

</details>

<details>
<summary>143. ¿Qué es la abstracción en Python?</summary>

#### Python

La abstracción consiste en destacar la API esencial y ocultar detalles
innecesarios de implementación. El cliente trabaja con el contrato, no con los
pasos internos.

**En resumen:**

- La abstracción reduce la carga cognitiva.
- Facilita sustituir la implementación sin cambiar el código cliente.
- Se implementa mediante interfaces, ABC, protocolos y fachadas.

</details>

<details>
<summary>144. ¿Cómo implementar abstracción de datos?</summary>

#### Python

Enfoque:

- ocultar el acceso directo a campos internos (`_field`);
- ofrecer una API controlada mediante métodos o `@property`;
- validar invariantes en la lógica del setter.

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

**En resumen:**

- La abstracción de datos protege los invariantes del objeto.
- `property` da acceso controlado al estado.
- Los detalles internos pueden cambiarse sin cambiar la API.

</details>

<details>
<summary>145. ¿Qué son ABC y `@abstractmethod`?</summary>

#### Python

ABC (Abstract Base Class) es una clase base abstracta del módulo `abc`.
`@abstractmethod` marca un método que la subclase debe implementar
obligatoriamente.

```python
from abc import ABC, abstractmethod

class Storage(ABC):
    @abstractmethod
    def save(self, data: bytes) -> None:
        ...
```

**En resumen:**

- ABC formaliza el contrato de la jerarquía.
- `@abstractmethod` impide instanciar una implementación incompleta.
- Es útil para arquitecturas extensibles o basadas en complementos.

</details>

<details>
<summary>146. ¿Qué es property en Python y cómo se usa?</summary>

#### Python

`property` convierte métodos de acceso en una API similar a atributos, con
posibilidad de validación, cálculos o lógica perezosa.

```python
class User:
    def __init__(self, name: str) -> None:
        self._name = name

    @property
    def name(self) -> str:
        return self._name
```

**En resumen:**

- `property` da control de acceso sin cambiar la sintaxis externa.
- Sirve para validación y valores derivados.
- Permite evolucionar la API sin romper a los clientes.

</details>

<details>
<summary>147. ¿Qué es `@property`?</summary>

#### Python

`@property` es un decorador para un método getter. Junto con `@x.setter` y
`@x.deleter`, forma un atributo gestionado.

**En resumen:**

- `@property` permite leer un método como si fuera un campo.
- Ayuda a encapsular la implementación interna.
- A menudo se usa para APIs retrocompatibles.

</details>

<details>
<summary>148. ¿Qué es un descriptor en Python?</summary>

#### Python

Un descriptor es un objeto que implementa `__get__`, `__set__` o `__delete__`
y controla el acceso a atributos de otra clase.

A través de descriptores funcionan `property`, `classmethod` y `staticmethod`.

**En resumen:**

- Un descriptor es un mecanismo de bajo nivel para acceso a atributos.
- Permite reutilizar lógica de validación o proxy de campos.
- Es la base de muchas técnicas de metaprogramación en Python.

</details>

<details>
<summary>149. ¿Cuál es la diferencia entre property y descriptor?</summary>

#### Python

`property` es un descriptor de alto nivel ya preparado para un atributo. Un
descriptor personalizado es un mecanismo más general que puede reutilizarse en
muchos campos o clases.

**En resumen:**

- `property` es más simple y local.
- Un descriptor es más flexible y escalable.
- `property` está construido sobre el protocolo descriptor.

</details>

<details>
<summary>150. ¿Cuándo conviene usar property y cuándo un descriptor?</summary>

#### Python

Usa `property` cuando la lógica afecta a uno o dos campos de una clase
concreta. Usa un descriptor cuando la misma lógica (validación, casting,
inicialización perezosa) debe reutilizarse en muchas clases.

**En resumen:**

- Lógica local de un campo -> `property`.
- Reutilización de la política de acceso -> descriptor.
- Un descriptor es ventajoso en modelos de dominio grandes.

</details>

<details>
<summary>151. ¿Para qué se usan `setattr()`, `getattr()` y `hasattr()`? ¿Cuál es la diferencia entre ellos?</summary>

#### Python

Son funciones de acceso dinámico a atributos:

- `getattr(obj, name[, default])` -> leer un atributo;
- `setattr(obj, name, value)` -> establecer un atributo;
- `hasattr(obj, name)` -> comprobar si existe.

```python
value = getattr(user, "email", None)
if not hasattr(user, "active"):
    setattr(user, "active", True)
```

**En resumen:**

- `getattr/setattr/hasattr` sirven para trabajar dinámicamente con objetos.
- Son útiles en código genérico, serialización y adaptadores.
- Es importante no abusar de ellas para no perder legibilidad.

</details>

<details>
<summary>152. Explique el significado del método `__set_name__` en los descriptores de Python y dé un ejemplo de uso.</summary>

#### Python

`__set_name__(self, owner, name)` se llama durante la creación de la clase y
permite que el descriptor conozca el nombre del atributo al que está vinculado.

```python
class Field:
    def __set_name__(self, owner, name): self.name = name
```

**En resumen:**

- `__set_name__` inicializa el descriptor con el contexto de la clase.
- Permite crear validadores de campos reutilizables.
- Se ejecuta una sola vez en la etapa de creación de la clase.

</details>

<details>
<summary>153. ¿Qué es `dataclass` y cuándo conviene usarlo?</summary>

#### Python

`@dataclass` genera automáticamente código repetitivo (`__init__`, `__repr__`,
`__eq__`). Es adecuado para modelos de datos sin comportamiento complejo.

```python
from dataclasses import dataclass
@dataclass(slots=True)
class User:
    name: str
    active: bool = True
```

**En resumen:**

- `dataclass` reduce código en modelos de datos.
- Es una buena opción para DTO y configuraciones.
- Para validación compleja, a menudo hacen falta otras herramientas.

</details>

<details>
<summary>154. ¿Cuál es la diferencia entre `dataclass` y Pydantic?</summary>

#### Python

`dataclass` se centra en describir la estructura de forma cómoda. Pydantic
añade validación en tiempo de ejecución, análisis y serialización de datos.

**En resumen:**

- `dataclass` es más ligero y rápido para modelos internos.
- Pydantic es mejor para entrada externa y APIs.
- La elección depende de la necesidad de validación en ejecución.

</details>

<details>
<summary>155. ¿Qué son las anotaciones de tipos y para qué sirven?</summary>

#### Python

Las anotaciones de tipos son anotaciones en firmas y variables que forman un
contrato explícito. Mejoran las sugerencias del IDE y el análisis estático.

**En resumen:**

- Las anotaciones de tipos aumentan la claridad de la API.
- Permiten detectar antes cierta clase de errores.
- Son útiles incluso en un lenguaje dinámico.

</details>

<details>
<summary>156. ¿Cómo funciona la comprobación estática de tipos (`mypy`)?</summary>

#### Python

`mypy` lee anotaciones de tipos y analiza el código sin ejecutarlo, comprobando la
compatibilidad de tipos. Detecta errores de integración antes de la ejecución.

**En resumen:**

- `mypy` realiza una comprobación parecida al tiempo de compilación para Python.
- Funciona mejor en CI.
- Los modos estrictos reducen la cantidad de bugs en producción.

</details>

<details>
<summary>157. ¿Cómo garantizar seguridad de tipos en un proyecto Python?</summary>

#### Python

- añadir anotaciones de tipos de forma consistente en la API pública;
- activar `mypy`/`pyright` en CI;
- usar `TypedDict`, `Protocol` y genéricos;
- minimizar `Any` y los castings implícitos.

**En resumen:**

- La seguridad de tipos es un proceso, no una acción puntual.
- El mayor efecto lo da una puerta de CI para tipos.
- Aumentar el rigor de forma gradual funciona mejor que un "big bang".

</details>

<details>
<summary>158. ¿Qué es `TypedDict`?</summary>

#### Python

`TypedDict` describe una forma tipada de diccionario: qué claves se esperan y
de qué tipo son sus valores.

```python
from typing import TypedDict
class UserPayload(TypedDict): name: str; active: bool
```

**En resumen:**

- `TypedDict` tipa un `dict` con claves fijas.
- Es cómodo para estructuras parecidas a JSON.
- Lo comprueba un analizador estático.

</details>

<details>
<summary>159. ¿Qué es `Protocol` en typing?</summary>

#### Python

`Protocol` describe un contrato conductual (tipado estructural): un tipo es
compatible si tiene los métodos o atributos necesarios, independientemente de la
herencia.

**En resumen:**

- `Protocol` implementa duck typing en el tipado estático.
- Reduce el acoplamiento rígido a clases concretas.
- Es útil para APIs testeables y extensibles.

</details>

<details>
<summary>160. ¿Qué son los genéricos en Python?</summary>

#### Python

Los genéricos permiten escribir tipos y funciones parametrizados por otros tipos.
En la sintaxis moderna: `class Box[T]: ...`, `def first[T](...) -> T`.

**En resumen:**

- Los genéricos hacen que los tipos sean reutilizables.
- Refuerzan la seguridad de tipos de colecciones y contenedores.
- Reducen la duplicación de código tipado.

</details>

<details>
<summary>161. ¿Qué es Pydantic y para qué se usa?</summary>

#### Python

Pydantic es una biblioteca para describir esquemas de datos con validación en
tiempo de ejecución, conversión de tipos y serialización cómoda.

Casos típicos: modelos de solicitud y respuesta de FastAPI y configuración de la
aplicación.

**En resumen:**

- Pydantic valida datos externos durante la ejecución.
- Es cómodo para APIs e integraciones.
- Proporciona errores de validación claros y esquemas.

</details>

<details>
<summary>162. ¿Qué son las exceptions en Python?</summary>

#### Python

Una exception es un objeto que señala una situación errónea o excepcional
durante la ejecución del código.

**En resumen:**

- Las exceptions interrumpen el flujo normal.
- Deben manejarse donde se pueda tomar una decisión.
- Un modelo correcto de errores aumenta la fiabilidad del sistema.

</details>

<details>
<summary>163. ¿Cuáles son los tres tipos de errores en Python y en qué se diferencian?</summary>

#### Python

- Syntax errors: errores de sintaxis antes de la ejecución;
- Excepciones en tiempo de ejecución: errores durante la ejecución;
- Logical errors: el código se ejecuta, pero el resultado es incorrecto.

**En resumen:**

- Los errores de sintaxis y de ejecución los detecta el intérprete.
- Los errores lógicos se detectan con pruebas y revisión.
- Cada tipo requiere un enfoque de diagnóstico distinto.

</details>

<details>
<summary>164. ¿Cómo usar `try`, `except`, `else` y `finally`?</summary>

#### Python

`try` contiene una operación de riesgo, `except` maneja el error, `else` se
ejecuta cuando no hubo error y `finally` se ejecuta siempre (limpieza).

```python
try: data = load()
except FileNotFoundError: data = {}
else: validate(data)
finally: close_connections()
```

**En resumen:**

- Usa `else` para el código de la ruta exitosa.
- Usa `finally` para recursos y limpieza.
- Captura exceptions concretas, no "todo".

</details>

<details>
<summary>165. ¿Qué significa el orden de las categorías `except`?</summary>

#### Python

Los `except` se comprueban de arriba abajo, así que primero se colocan las
exceptions más concretas y las generales (`Exception`) al final.

**En resumen:**

- El orden de `except` influye en qué manejador se ejecutará.
- Un `except` amplio arriba "se come" los casos específicos.
- Esto es crítico para un flujo de recuperación correcto.

</details>

<details>
<summary>166. ¿Cuál es el propósito de la palabra clave `assert` en código Python?</summary>

#### Python

`assert` comprueba un invariante y lanza `AssertionError` si la condición es
falsa. Sirve para comprobaciones internas del desarrollador, no para validar
entrada de usuario.

**En resumen:**

- `assert` documenta "esto debe ser verdadero".
- No sustituye el manejo de errores en producción.
- Úsalo para contratos en la lógica interna.

</details>

<details>
<summary>167. ¿En qué se diferencia `raise` de simplemente imprimir un mensaje de error en Python?</summary>

#### Python

`raise` cambia el flujo de control y señala el error al llamador. `print` solo
muestra texto y no detiene el escenario erróneo.

**En resumen:**

- `raise` es un mecanismo de manejo de errores; `print`, no.
- Las exceptions pueden capturarse y registrarse de forma centralizada.
- `print` sirve para diagnóstico, no para contratos de error.

</details>

<details>
<summary>168. ¿Cómo crear una excepción propia?</summary>

#### Python

Crea una clase que herede de `Exception` (o de una excepción base más específica).

```python
class InvalidOrderError(Exception):
    pass
```

**En resumen:**

- Una excepción propia hace que los errores sean expresivos para el dominio.
- Permite capturar con precisión los casos necesarios.
- Es mejor que usar `ValueError` para todo.

</details>

<details>
<summary>169. ¿Qué valor tiene crear excepciones propias en Python y cómo mejoran el manejo de errores?</summary>

#### Python

Las exceptions propias forman un modelo de errores explícito del dominio y
separan los fallos técnicos de las reglas de negocio.

**En resumen:**

- Mejoran la legibilidad y el mantenimiento de los manejadores.
- Aportan una semántica más precisa en logs y APIs.
- Simplifican las pruebas de escenarios negativos.

</details>

<details>
<summary>170. ¿Cómo están organizadas las excepciones en Python y cuál es la jerarquía de sus clases?</summary>

#### Python

La jerarquía parte de `BaseException`. En código de aplicación casi siempre se
trabaja con descendientes de `Exception`.

Ramas principales: `ValueError`, `TypeError`, `KeyError`, `OSError`, `RuntimeError`.

**En resumen:**

- Las excepciones forman un árbol de clases.
- Es mejor capturar subclases concretas.
- `BaseException` normalmente no se captura en la lógica de negocio.

</details>

<details>
<summary>171. ¿Qué enfoques hay para manejar varias excepciones distintas en Python y por qué conviene tratarlas por separado?</summary>

#### Python

Enfoques:

- `except` separados para cada tipo;
- agrupación de casos lógicamente equivalentes: `except (A, B):`;
- estrategias de recuperación distintas para cada categoría.

**En resumen:**

- Distintas excepciones suelen requerir acciones diferentes.
- El manejo separado reduce defectos ocultos.
- Los logs se vuelven más precisos y útiles.

</details>

<details>
<summary>172. ¿Para qué sirve relanzar una excepción en Python y cuándo es útil?</summary>

#### Python

Relanzar (`raise` sin argumentos dentro de `except`) permite añadir contexto
(logs, métricas, limpieza) y propagar el mismo error hacia arriba.

**En resumen:**

- El relanzamiento conserva el traceback original.
- Es útil para un manejo centralizado en niveles superiores.
- No "tragues" errores críticos sin necesidad.

</details>

<details>
<summary>173. ¿Por qué conviene limitar el uso de bloques try-except en programas Python y cómo afecta eso al rendimiento?</summary>

#### Python

`try/except` es necesario, pero no debería envolver bloques grandes "por si
acaso". Es especialmente costoso cuando las excepciones ocurren con frecuencia
(flujo guiado por excepciones).

**En resumen:**

- Captura solo errores esperados en un punto estrecho.
- Las excepciones frecuentes empeoran el rendimiento y la legibilidad.
- Prefiere comprobaciones explícitas cuando sea adecuado.

</details>

<details>
<summary>174. ¿Cómo manejar errores al trabajar con archivos?</summary>

#### Python

Usa `with` y captura excepciones concretas (`FileNotFoundError`,
`PermissionError`, `UnicodeDecodeError`, `OSError`).

```python
try:
    with open(path, "r", encoding="utf-8") as f:
        content = f.read()
except FileNotFoundError:
    ...
```

**En resumen:**

- `with` garantiza el cierre del archivo.
- Maneja errores concretos de entrada y salida.
- Registra el contexto: ruta, modo y codificación.

</details>

<details>
<summary>175. ¿Qué modos de trabajo con archivos existen en Python?</summary>

#### Python

Modos principales:

- `r` lectura;
- `w` sobrescritura;
- `a` anexar al final;
- `x` creación de un archivo nuevo;
- `b` modo binario;
- `t` modo texto (por defecto);
- `+` lectura y escritura.

**En resumen:**

- El modo define la semántica de seguridad y cambio del archivo.
- `w` borra el contenido; `a` conserva lo existente.
- Para datos binarios, usa `b`.

</details>

<details>
<summary>176. ¿Por qué es importante cerrar archivos después de las operaciones y qué puede pasar si se dejan abiertos?</summary>

#### Python

Un archivo abierto mantiene un descriptor del sistema operativo. Si no se cierra:

- fuga de descriptores de archivo;
- bloqueos de archivos o vaciado incompleto del búfer;
- inestabilidad en procesos largos.

**En resumen:**

- Cerrar un archivo libera recursos del sistema operativo.
- `with` automatiza un cierre seguro.
- Esto es crítico para servicios y scripts por lotes.

</details>

<details>
<summary>177. ¿Cuál es la diferencia entre `read()`, `readline()` y `readlines()` al leer archivos?</summary>

#### Python

- `read()` lee todo el archivo, o `n` bytes o caracteres;
- `readline()` lee una sola línea;
- `readlines()` lee todas las líneas en una lista.

**En resumen:**

- `read()` y `readlines()` pueden ser pesados en memoria.
- Para archivos grandes, es mejor iterar con `for line in file`.
- La elección depende del volumen y del escenario de procesamiento.

</details>

<details>
<summary>178. ¿Cómo escribir datos en un archivo en Python y cuál es la diferencia entre `w` (escritura) y `a` (anexar)?</summary>

#### Python

Escritura:

```python
with open("out.txt", "w", encoding="utf-8") as f:
    f.write("hello\n")
```

`w` sobrescribe el archivo desde el principio; `a` añade contenido nuevo al final.

**En resumen:**

- `w` borra los datos antiguos.
- `a` conserva el contenido existente.
- Para registros, normalmente se usa `a`.

</details>

<details>
<summary>179. ¿Cómo trabajar de forma eficiente con archivos grandes?</summary>

#### Python

- leer en flujo, por líneas o por bloques;
- evitar cargar todo el archivo en memoria;
- usar búferes y generadores;
- para datos columnares o tabulares, elegir formatos y analizadores adecuados.

**En resumen:**

- La clave es la lectura en flujo en lugar de la lectura completa.
- Los generadores reducen el consumo de memoria.
- El algoritmo de procesamiento importa más que las microoptimizaciones.

</details>

<details>
<summary>180. ¿Qué son los gestores de contexto?</summary>

#### Python

Un gestor de contexto administra un recurso mediante el protocolo
`__enter__/__exit__`: apertura o inicialización y finalización o limpieza
garantizada.

**En resumen:**

- Proporciona un ciclo de vida seguro del recurso.
- Funciona mediante `with`.
- Reduce la cantidad de fugas de recursos.

</details>

<details>
<summary>181. ¿Cómo funciona la construcción `with`?</summary>

#### Python

`with` llama a `__enter__` al entrar en el bloque y a `__exit__` al salir,
incluso si ocurre un error.

```python
with open("data.txt", "r", encoding="utf-8") as f:
    data = f.read()
```

**En resumen:**

- `with` garantiza la limpieza.
- Hace que el trabajo con recursos sea declarativo.
- Se recomienda para archivos, bloqueos, transacciones y sesiones.

</details>

<details>
<summary>182. ¿Cómo crear un gestor de contexto propio?</summary>

#### Python

Hay dos enfoques:

- una clase con `__enter__` y `__exit__`;
- una función con `contextlib.contextmanager`.

```python
from contextlib import contextmanager

@contextmanager
def temp_flag():
    yield
```

**En resumen:**

- Una clase sirve para estado complejo.
- `contextmanager` es cómodo para escenarios cortos.
- Ambos garantizan la limpieza.

</details>

<details>
<summary>183. ¿Cómo gestiona Python la memoria?</summary>

#### Python

CPython usa conteo de referencias y un recolector cíclico de basura. Además,
tiene un asignador interno (`pymalloc`) para objetos pequeños.

**En resumen:**

- El mecanismo básico es el conteo de referencias.
- El GC elimina referencias cíclicas.
- La memoria no siempre se libera de inmediato a nivel del sistema operativo.

</details>

<details>
<summary>184. ¿Qué es el conteo de referencias en Python y por qué es importante para la gestión de memoria?</summary>

#### Python

Cada objeto tiene un contador de referencias. Cuando llega a cero, el objeto
puede liberarse. Esto permite liberar rápidamente la mayoría de objetos de vida corta.

**En resumen:**

- El conteo de referencias da un ciclo de vida predecible a los objetos.
- No resuelve por sí solo las referencias cíclicas.
- Junto con el GC, forma un modelo completo de gestión de memoria.

</details>

<details>
<summary>185. ¿Qué es la recolección de basura en Python?</summary>

#### Python

La recolección de basura en CPython encuentra y elimina ciclos inalcanzables de
objetos que no pueden limpiarse solo con conteo de referencias.

**En resumen:**

- El GC complementa el conteo de referencias.
- Es especialmente importante para grafos cíclicos de referencias.
- Puede controlarse mediante el módulo `gc`.

</details>

<details>
<summary>186. ¿Cómo obtener la dirección de memoria de un objeto en Python?</summary>

#### Python

En CPython, `id(obj)` suele corresponder a la dirección de memoria del objeto
(como un entero). Es una herramienta de diagnóstico, no un identificador
externo estable.

**En resumen:**

- `id()` da la identidad del objeto.
- En CPython suele ser la dirección de memoria.
- No lo uses en lógica de negocio.

</details>

<details>
<summary>187. ¿Para qué sirve la función `getrefcount()` del módulo `sys` y cómo funciona en Python?</summary>

#### Python

`sys.getrefcount(obj)` devuelve el contador actual de referencias de un objeto
(en CPython). El valor suele ser 1 mayor por la referencia temporal del argumento.

**En resumen:**

- Es una herramienta de diagnóstico del comportamiento de memoria.
- Es útil para analizar fugas de referencias.
- No debe usarse como base en lógica de aplicación.

</details>

<details>
<summary>188. Explique con ejemplos la diferencia entre objetos mutables e inmutables en relación con el conteo de referencias y la gestión de memoria.</summary>

#### Python

Los objetos inmutables no cambian, así que una "modificación" crea un objeto
nuevo. Los objetos mutables cambian en el lugar, y todas las referencias ven el cambio.

```python
a = "x"; b = a; a += "y"   # nuevo objeto
x = [1]; y = x; y.append(2) # cambio del mismo objeto
```

**En resumen:**

- Los inmutables reducen efectos secundarios.
- Los mutables son más eficientes para modificaciones en el lugar.
- La diferencia es crítica para copiado y referencias compartidas.

</details>

<details>
<summary>189. ¿Cuál es la diferencia entre copia superficial y copia profunda en Python, y cuándo conviene usar cada enfoque?</summary>

#### Python

La copia superficial copia solo el contenedor externo; los objetos anidados
siguen siendo compartidos. La copia profunda copia recursivamente toda la estructura.

```python
import copy
copy.copy(obj)
copy.deepcopy(obj)
```

**En resumen:**

- La copia superficial es suficiente para estructuras "planas".
- La copia profunda hace falta para trabajar de forma aislada con datos mutables anidados.
- La copia profunda es más costosa en tiempo y memoria.

</details>

<details>
<summary>190. ¿Qué son los módulos y paquetes en Python?</summary>

#### Python

Un módulo es un archivo `.py` independiente con código. Un paquete es un
directorio de módulos (espacio de nombres) que organiza el código en bloques
más grandes.

**En resumen:**

- Módulo = unidad de código.
- Paquete = estructura para escalar módulos.
- Dividir en módulos y paquetes mejora el mantenimiento.

</details>

<details>
<summary>191. ¿Cómo importar un módulo en Python?</summary>

#### Python

Formas principales:

- `import module`;
- `import module as m`;
- `from module import name`;
- `from package import submodule`.

**En resumen:**

- La importación carga un módulo y lo hace disponible en el espacio de nombres.
- Un alias (`as`) mejora la legibilidad y evita conflictos.
- Conviene preferir importaciones explícitas.

</details>

<details>
<summary>192. ¿Qué tipos de imports existen?</summary>

#### Python

Tipos habituales:

- absolutos;
- relativos;
- selectivos (`from x import y`);
- con alias (`as`);
- dinámicos (`importlib`).

**En resumen:**

- El tipo de importación influye en la legibilidad y el mantenimiento.
- En producción suelen usarse importaciones absolutas.
- Las importaciones dinámicas se aplican de forma puntual.

</details>

<details>
<summary>193. ¿Cómo funciona el sistema de importaciones?</summary>

#### Python

El intérprete busca el módulo en `sys.path`, lo carga una vez y lo almacena en
la caché de `sys.modules`. Una importación repetida usa esa caché.

**En resumen:**

- Importar = búsqueda + ejecución del módulo + almacenamiento en caché.
- Esto explica por qué el código del módulo se ejecuta en la primera importación.
- Las importaciones cíclicas aparecen por el orden de inicialización de módulos.

</details>

<details>
<summary>194. ¿Cuál es la diferencia entre importación absoluta y relativa?</summary>

#### Python

La importación absoluta empieza desde la raíz del paquete (`from app.utils import x`).
La importación relativa usa puntos (`from .utils import x`).

**En resumen:**

- Las importaciones absolutas son más legibles y estables.
- Las relativas son cómodas dentro del paquete, pero peores para refactorizar.
- En proyectos grandes, conviene usar absolutas por defecto.

</details>

<details>
<summary>195. ¿Qué hace la función `dir()` y cómo puede aplicarse a módulos?</summary>

#### Python

`dir(obj)` devuelve una lista de atributos o nombres disponibles del objeto.
Para módulos, es una forma rápida de inspeccionar la API.

```python
import math
dir(math)
```

**En resumen:**

- `dir()` ayuda en la exploración interactiva de módulos.
- Es útil en REPL y depuración.
- No sustituye la documentación oficial.

</details>

<details>
<summary>196. Explique el papel de `if __name__ == "__main__":` en scripts de Python.</summary>

#### Python

Ese bloque se ejecuta solo cuando el archivo se lanza como script y no cuando
se importa como módulo. Esto separa el código reutilizable del punto de entrada de CLI.

**En resumen:**

- Permite tanto ejecutar el módulo como importarlo.
- Evita ejecución no deseada durante la importación.
- Es el patrón estándar para scripts.

</details>

<details>
<summary>197. ¿Qué significa el archivo `__init__.py` en un paquete Python?</summary>

#### Python

`__init__.py` marca un directorio como paquete y puede inicializar la API a
nivel de paquete, por ejemplo, reexportando clases o funciones.

**En resumen:**

- Define la interfaz pública del paquete.
- Puede contener una inicialización mínima.
- No conviene sobrecargarlo con lógica pesada.

</details>

<details>
<summary>198. ¿Qué buenas prácticas existen para el estilo de importaciones en código Python?</summary>

#### Python

- agrupar importaciones: biblioteca estándar, terceros y locales;
- evitar `from x import *`;
- mantener las importaciones al principio del archivo, salvo casos justificados de importación diferida;
- usar ordenación y formateo (`ruff`, `isort`).

**En resumen:**

- Las importaciones consistentes mejoran la legibilidad.
- Las importaciones explícitas reducen conflictos de nombres.
- La automatización con herramientas elimina errores manuales.

</details>

<details>
<summary>199. ¿Qué módulos integrados populares existen en Python?</summary>

#### Python

Ejemplos de módulos populares de la biblioteca estándar:

- `os`, `sys`, `pathlib`, `json`, `datetime`, `re`,
- `collections`, `itertools`, `functools`, `typing`,
- `asyncio`, `subprocess`, `logging`, `argparse`.

**En resumen:**

- La biblioteca estándar cubre la mayoría de tareas básicas.
- Esto reduce la cantidad de dependencias externas.
- Conviene conocer bien la biblioteca estándar antes de añadir paquetes de terceros.

</details>
<details>
<summary>200. ¿Qué sabe sobre el paquete `collections` y qué otros módulos integrados se han usado?</summary>

#### Python

`collections` proporciona estructuras de alto nivel:

- `Counter`, `defaultdict`, `deque`, `namedtuple`, `ChainMap`.

Suele combinarse con:

- `itertools` para pipelines iterativos;
- `functools` para caché y utilidades funcionales;
- `pathlib`, `json`, `datetime` en tareas de aplicación.

**En resumen:**

- `collections` amplía los contenedores básicos con estructuras prácticas.
- A menudo mejora la simplicidad y el rendimiento del código.
- Funciona bien junto con `itertools` y `functools`.

</details>

<details>
<summary>201. ¿Qué devuelve `sys.argv`?</summary>

#### Python

`sys.argv` devuelve una lista de argumentos de la línea de comandos:

- `sys.argv[0]` -> nombre del script;
- el resto de elementos -> argumentos pasados.

**En resumen:**

- `sys.argv` es la interfaz básica de argumentos de línea de comandos.
- Los valores llegan como cadenas.
- Para CLIs complejas, es mejor `argparse`.

</details>

<details>
<summary>202. ¿Cuál es el módulo principal para trabajar con el sistema operativo en Python?</summary>

#### Python

El módulo principal es `os` junto con `os.path`, y para una API moderna de
rutas se recomienda `pathlib`.

**En resumen:**

- `os` da acceso a la API de procesos, entorno y sistema de archivos del SO.
- `pathlib` es más cómodo para trabajar con rutas.
- En proyectos reales, a menudo se usan ambos.

</details>

<details>
<summary>203. ¿Cómo mezclar elementos de una lista usando el módulo `random`?</summary>

#### Python

Usa `random.shuffle(list_)` para mezclar en el lugar.

```python
import random
items = [1, 2, 3, 4]
random.shuffle(items)
```

**En resumen:**

- `shuffle` modifica la lista original.
- Funciona solo con secuencias mutables, por ejemplo listas.
- Para una copia nueva: `random.sample(items, k=len(items))`.

</details>

<details>
<summary>204. ¿Qué es un entorno virtual?</summary>

#### Python

Un entorno virtual es un entorno Python aislado con sus propios paquetes y
versiones de dependencias para un proyecto concreto.

**En resumen:**

- El aislamiento elimina conflictos de dependencias entre proyectos.
- La herramienta estándar es `venv`.
- Es una práctica básica para un desarrollo reproducible.

</details>

<details>
<summary>205. ¿Cómo funciona `pip`?</summary>

#### Python

`pip` instala, actualiza y elimina paquetes desde índices, normalmente PyPI,
resuelve dependencias y los instala en el entorno actual.

**En resumen:**

- `pip` es el gestor de paquetes estándar de Python.
- Funciona dentro del intérprete o venv activo.
- Para estabilidad, son importantes las versiones fijadas.

</details>

<details>
<summary>206. ¿Qué es `requirements.txt`?</summary>

#### Python

`requirements.txt` es un archivo con la lista de dependencias, a menudo con
versiones exactas, que se usa para una instalación reproducible.

**En resumen:**

- El formato es simple y compatible con `pip install -r`.
- Lo mejor es fijar versiones exactas para producción.
- A menudo lo generan herramientas como `pip-tools` o `poetry export` a partir
  de listas declarativas o archivos de bloqueo.

</details>

<details>
<summary>207. ¿Qué es `pyproject.toml` y por qué se convirtió en estándar?</summary>

#### Python

`pyproject.toml` es un archivo estandarizado de configuración del proyecto:
metadatos del paquete, sistema de compilación y configuración de herramientas como
`ruff`, `pytest`, `mypy`, etc.

**En resumen:**

- Centraliza la configuración del proyecto Python.
- Lo soportan las herramientas modernas de packaging.
- Reduce la cantidad de archivos de configuración dispersos.

</details>

<details>
<summary>208. ¿Cómo gestionar dependencias en un proyecto Python moderno?</summary>

#### Python

- aislar el entorno con `venv`;
- definir dependencias en `pyproject.toml`;
- fijar archivos de bloqueo o restricciones para reproducibilidad;
- actualizar regularmente con comprobaciones en CI.

**En resumen:**

- La gestión de dependencias debe ser reproducible.
- No mezcles paquetes globales y del proyecto.
- Haz las actualizaciones de forma controlada mediante pruebas.

</details>

<details>
<summary>209. ¿Cómo organizar correctamente la estructura de un proyecto Python grande?</summary>

#### Python

- dividir el código en paquetes de dominio;
- tener capas separadas: `api`, `services`, `domain`, `infrastructure`;
- separar `tests/`, `scripts/`, `configs/`;
- mantener límites claros entre módulos y una API pública explícita.

**En resumen:**

- La estructura debe reflejar el dominio, no detalles técnicos accidentales.
- Los límites claros reducen dependencias cíclicas.
- Las pruebas y las herramientas deben ser una parte de primera clase del árbol.

</details>

<details>
<summary>210. ¿Cuál es la diferencia entre las pruebas automatizadas y las manuales, y cuáles son las ventajas de las pruebas automatizadas?</summary>

#### Python

Las pruebas manuales las realiza una persona paso a paso. Las pruebas automatizadas
las ejecutan scripts o marcos de pruebas.

**En resumen:**

- Las pruebas automáticas son rápidas, repetibles y aptas para CI.
- Las pruebas manuales son útiles para escenarios exploratorios de UX.
- En producción hace falta una combinación de ambos enfoques.

</details>

<details>
<summary>211. ¿Qué es TDD (Test-Driven Development)?</summary>

#### Python

TDD es un ciclo: escribir una prueba que falla -> implementación mínima -> refactorización.

**En resumen:**

- TDD moldea la API a través de pruebas.
- Da retroalimentación rápida sobre regresiones.
- Funciona mejor para lógica de negocio modular.

</details>

<details>
<summary>212. ¿Qué marcos de pruebas populares existen en Python?</summary>

#### Python

Los más populares son `pytest`, `unittest` de la biblioteca estándar y también
`hypothesis` para pruebas basadas en propiedades.

**En resumen:**

- `pytest` es la opción más habitual en proyectos nuevos.
- `unittest` es útil como herramienta base estándar.
- `hypothesis` refuerza la cobertura de casos límite.

</details>

<details>
<summary>213. ¿Qué es `unittest` en Python?</summary>

#### Python

`unittest` es el marco xUnit integrado para pruebas: clases de caso de prueba,
métodos de aserción, preparación/limpieza y ejecutor de pruebas.

**En resumen:**

- Forma parte de la biblioteca estándar.
- Encaja en entornos conservadores sin dependencias externas.
- Tiene una sintaxis más ceremonial que `pytest`.

</details>

<details>
<summary>214. ¿Qué es `pytest` y en qué se diferencia de `unittest` por sintaxis y funcionalidad?</summary>

#### Python

`pytest` es un marco con sintaxis simple para pruebas funcionales, fixtures
potentes, parametrización y un ecosistema de complementos.

**En resumen:**

- `pytest` requiere menos código repetitivo y es más cómodo para suites grandes.
- `unittest` está basado en clases y es estándar en la biblioteca estándar.
- En proyectos modernos suele dominar `pytest`.

</details>

<details>
<summary>215. Describa cómo se usa `pytest.raises` para comprobar que aparece una excepción concreta en código Python.</summary>

#### Python

`pytest.raises(ExpectedError)` comprueba que un bloque de código lanza
exactamente la excepción esperada.

```python
import pytest
with pytest.raises(ValueError):
    int("abc")
```

**En resumen:**

- Prueba escenarios negativos de forma explícita.
- Protege contra el paso silencioso de errores.
- También puede verificar el mensaje o atributos de la excepción.

</details>

<details>
<summary>216. ¿Qué es la parametrización en pruebas y cómo la soporta pytest con `@pytest.mark.parametrize`?</summary>

#### Python

La parametrización ejecuta una prueba con varios conjuntos de datos de entrada. En
pytest se hace con el decorador `@pytest.mark.parametrize`.

**En resumen:**

- Menos duplicación de código de prueba.
- Facilita escalar casos.
- Da más transparencia sobre la cobertura de escenarios de entrada.

</details>

<details>
<summary>217. ¿Cómo definir nombres propios de pruebas parametrizadas en pytest para mejorar la legibilidad?</summary>

#### Python

Usa el parámetro `ids` en `parametrize`.

```python
@pytest.mark.parametrize("value,expected", [(2, True), (3, False)], ids=["even", "odd"])
```

**En resumen:**

- `ids` hace más clara la salida de la ejecución de pruebas.
- Facilita diagnosticar fallos.
- Es especialmente útil con muchos casos.

</details>

<details>
<summary>218. ¿Qué es Arrange/Setup en pruebas y por qué es importante?</summary>

#### Python

Arrange/Setup es la preparación del estado de prueba: datos, objetos, mocks y
entorno. Una buena preparación hace que la prueba sea determinista.

**En resumen:**

- Una preparación inestable produce pruebas inestables.
- Una buena preparación aísla la prueba de efectos externos.
- Un Arrange claro mejora la legibilidad del escenario.

</details>

<details>
<summary>219. ¿Qué etapas incluye la limpieza final y por qué es importante?</summary>

#### Python

La fase de limpieza final elimina todo lo que creó la prueba: archivos temporales, conexiones,
mocks y registros de prueba en la base de datos.

**En resumen:**

- La limpieza garantiza aislamiento entre pruebas.
- Reduce efectos secundarios e inestabilidad.
- En pytest es cómodo hacerlo con finalizadores de fixtures o fixtures con `yield`.

</details>

<details>
<summary>220. ¿Cuál es la diferencia entre `setUp()` y `setUpClass()` en unittest?</summary>

#### Python

`setUp()` se ejecuta antes de **cada** método de prueba. `setUpClass()`
(classmethod) se ejecuta **una vez** antes de todas las pruebas de la clase.

**En resumen:**

- `setUp` sirve para el aislamiento por prueba.
- `setUpClass` sirve para recursos compartidos costosos.
- Demasiado estado compartido vía `setUpClass` puede complicar las pruebas.

</details>

<details>
<summary>221. ¿Qué es un objeto mock y cómo ayuda a mejorar la calidad de las pruebas?</summary>

#### Python

Un objeto mock es un objeto sustituto que imita una dependencia y permite
controlar el comportamiento o verificar llamadas.

**En resumen:**

- Los mocks aíslan la unidad de servicios externos.
- Hacen las pruebas más rápidas y estables.
- Permiten comprobar interacciones, no solo resultados.

</details>

<details>
<summary>222. ¿Cuál es la diferencia entre usar `mock.patch` en unittest y `monkeypatch` en pytest para mockear objetos?</summary>

#### Python

`mock.patch` de `unittest.mock` parchea objetos por ruta de importación y tiene
una API completa para verificar llamadas. `monkeypatch` en pytest cambia de forma
más simple atributos, variables de entorno o diccionarios durante la prueba.

**En resumen:**

- `patch` es más potente para escenarios con aserciones sobre mocks.
- `monkeypatch` es cómodo para sustituciones rápidas en pruebas.
- A menudo se combinan según el caso.

</details>

<details>
<summary>223. ¿Cuál es el propósito del parámetro `scope` en las fixtures de pytest?</summary>

#### Python

`scope` define el ciclo de vida de una fixture: `function`, `class`, `module`,
`package`, `session`.

**En resumen:**

- Un alcance menor da mejor aislamiento.
- Un alcance mayor acelera la ejecución de suites grandes.
- Elegir el alcance es un equilibrio entre velocidad e independencia.

</details>

<details>
<summary>224. ¿Qué es la complejidad algorítmica y cómo se determina?</summary>

#### Python

La complejidad algorítmica evalúa cómo crecen los costes de tiempo y memoria al
aumentar el tamaño de los datos de entrada `n`.

**En resumen:**

- Se mide la complejidad temporal y espacial.
- La evaluación suele ser asintótica.
- Ayuda a elegir algoritmos y estructuras de datos.

</details>

<details>
<summary>225. Explique la notación Big O y su importancia para evaluar la complejidad de algoritmos.</summary>

#### Python

Big O describe el límite superior del crecimiento del coste de un algoritmo con
`n` grande, ignorando constantes y términos menores.

**En resumen:**

- Big O muestra escalabilidad, no tiempo exacto.
- Proporciona un lenguaje para comparar algoritmos.
- Es crítica para el rendimiento con grandes volúmenes.

</details>

<details>
<summary>226. ¿Qué tipos de complejidad algorítmica aparecen con más frecuencia?</summary>

#### Python

Las más comunes son `O(1)`, `O(log n)`, `O(n)`, `O(n log n)` y `O(n^2)`.

**En resumen:**

- `O(n)` y `O(n log n)` son las más típicas en tareas aplicadas.
- `O(n^2)` o peor suele convertirse en cuello de botella.
- También hay que considerar memoria, no solo tiempo.

</details>

<details>
<summary>227. Dé ejemplos de tareas que se resuelven eficientemente con algoritmos lineales O(n).</summary>

#### Python

Ejemplos:

- búsqueda de máximo o mínimo;
- filtrado de elementos;
- conteo de frecuencias con `Counter`;
- comprobación de condiciones para cada elemento.

**En resumen:**

- O(n) significa una sola pasada sobre los datos.
- Es óptimo para muchas agregaciones.
- Los algoritmos lineales escalan bien.

</details>

<details>
<summary>228. ¿Cómo funciona `lru_cache` y cuándo conviene usarlo?</summary>

#### Python

`functools.lru_cache` guarda en caché los resultados de una función según sus
argumentos y devuelve el valor ya preparado en llamadas repetidas.

**En resumen:**

- Es eficaz para funciones puras con entradas repetidas.
- No encaja en funciones con efectos secundarios.
- `maxsize` controla el tamaño de la caché en memoria.

</details>

<details>
<summary>229. ¿Cómo perfilar el rendimiento de código Python?</summary>

#### Python

Herramientas básicas:

- `timeit` para micro-mediciones;
- `cProfile`/`pstats` para perfiles a nivel de llamadas;
- `py-spy`/`scalene` para análisis más cercanos a producción.

**En resumen:**

- Optimiza solo después de medir.
- Perfila escenarios de carga realistas.
- Fija una línea base antes y después de los cambios.

</details>

<details>
<summary>230. ¿Cuáles son las formas principales de optimizar código Python?</summary>

#### Python

- elegir las estructuras de datos correctas;
- reducir la complejidad asintótica;
- evitar copias innecesarias;
- usar generadores o pipelines perezosos;
- almacenar en caché cálculos costosos;
- mover rutas críticas a C, Rust o NumPy si hace falta.

**En resumen:**

- La mayor mejora la da el algoritmo, no un ajuste sintáctico.
- La optimización debe apoyarse en perfilado.
- No conviene sacrificar legibilidad sin un beneficio medido.

</details>

<details>
<summary>231. ¿Cuándo conviene usar extensiones en C o PyPy?</summary>

#### Python

Las extensiones en C son adecuadas para puntos críticos de CPU muy concretos y
para integrarse con bibliotecas nativas. PyPy conviene cuando código Python
puro de larga duración se beneficia del JIT.

**En resumen:**

- Extensión en C: máximo rendimiento a costa de mayor complejidad de compilación.
- PyPy: mejora potencial sin reescribir en C.
- La elección debe basarse en pruebas comparativas de tu carga real.

</details>

<details>
<summary>232. ¿Qué es el perfilado de memoria?</summary>

#### Python

El perfilado de memoria mide dónde y cuánta memoria consume el código con el
tiempo para encontrar fugas y zonas pesadas.

**En resumen:**

- Muestra puntos calientes de memoria y picos.
- Es útil para cargas batch y de datos.
- Herramientas: `tracemalloc`, `memory_profiler`, `scalene`.

</details>

<details>
<summary>233. ¿Qué es el GIL (Global Interpreter Lock)?</summary>

#### Python

El GIL es un mecanismo de CPython que permite que solo un hilo ejecute
bytecode de Python al mismo tiempo dentro de un proceso.

**En resumen:**

- El GIL afecta al multihilo en tareas intensivas de CPU.
- Para tareas limitadas por I/O, los hilos siguen siendo útiles.
- Para paralelismo de CPU, suele usarse `multiprocessing`.

</details>

<details>
<summary>234. ¿Cómo afecta el GIL a la concurrencia en CPython y qué consecuencias tiene para el multithreading?</summary>

#### Python

Debido al GIL, los hilos en CPython no ejecutan bytecode de Python en paralelo
real para código intensivo de CPU. Se alternan de forma cooperativa.

Consecuencias:

- para hilos limitados por I/O, el efecto es bueno porque la espera de I/O se solapa;
- para tareas intensivas de CPU, la mejora con hilos suele ser limitada.

**En resumen:**

- El GIL limita el paralelismo de hilos en escenarios intensivos de CPU.
- Los hilos siguen siendo útiles para red y disco.
- Para CPU, usa procesos o cómputo nativo.

</details>

<details>
<summary>235. ¿Cómo afecta el GIL al rendimiento?</summary>

#### Python

El GIL casi no molesta en tareas limitadas por I/O, pero limita la capacidad de procesamiento de código
Python multihilo intensivo de CPU dentro de un proceso.

**En resumen:**

- El impacto del GIL depende del tipo de carga.
- El código intensivo de CPU con hilos en CPython a menudo no escala.
- La arquitectura debe elegirse según el perfil de tareas.

</details>

<details>
<summary>236. Explique el concepto de threading en Python y en qué se diferencia de multiprocessing.</summary>

#### Python

`threading` ejecuta varios hilos dentro de un proceso con memoria compartida.
`multiprocessing` ejecuta procesos separados con memoria separada.

**En resumen:**

- Los hilos son más ligeros y cómodos para tareas limitadas por I/O.
- Los procesos dan paralelismo real de CPU.
- Los procesos tienen más sobrecarga de IPC y creación.

</details>

<details>
<summary>237. ¿Cuándo usar multiprocessing en lugar de threading?</summary>

#### Python

Cuando la tarea es intensiva de CPU y necesita usar varios núcleos en CPython.
Ejemplos: parsing pesado, procesamiento de imagen o vídeo y cálculo numérico.

**En resumen:**

- Intensiva de CPU -> normalmente `multiprocessing`.
- Limitada por I/O -> normalmente `threading` o `asyncio`.
- Ten en cuenta el coste de serialización entre procesos.

</details>

<details>
<summary>238. ¿Cuál es la diferencia entre concurrencia y paralelismo y cuándo conviene usar cada uno?</summary>

#### Python

La concurrencia es el solapamiento de tareas en el tiempo. El paralelismo es la
ejecución física simultánea de tareas en varios núcleos.

**En resumen:**

- La concurrencia es útil para latencias de I/O.
- El paralelismo es necesario para cálculos intensivos de CPU.
- En Python, la herramienta depende del tipo de cuello de botella.

</details>

<details>
<summary>239. ¿Qué es la concurrencia en Python?</summary>

#### Python

La concurrencia en Python es la organización de varias tareas para que
progresen juntas mediante hilos, asyncio o procesos.

**En resumen:**

- Trata de gestionar muchas tareas, no necesariamente en paralelo.
- Permite aumentar la capacidad de procesamiento en escenarios de I/O.
- Requiere diseñar bien sincronización y cancelación.

</details>

<details>
<summary>240. ¿Cuál es la diferencia entre tareas limitadas por I/O y tareas intensivas de CPU?</summary>

#### Python

Las tareas limitadas por I/O esperan sobre todo red, disco o base de datos. Las tareas
intensivas de CPU gastan sobre todo tiempo en cálculo del procesador.

**En resumen:**

- Las tareas limitadas por I/O escalan bien con asyncio o hilos.
- Las tareas intensivas de CPU escalan mejor con multiprocessing o código nativo.
- Primero identifica el cuello de botella con perfilado.

</details>

<details>
<summary>241. ¿Para qué sirve el módulo `asyncio` en Python y cómo permite implementar programación asíncrona?</summary>

#### Python

`asyncio` proporciona un bucle de eventos, planificación de tareas y primitivas asíncronas
para concurrencia cooperativa en tareas limitadas por I/O.

**En resumen:**

- Permite atender muchas operaciones de I/O de forma eficiente.
- Se basa en `async` y `await`.
- Encaja bien en servicios y clientes de red.

</details>

<details>
<summary>242. ¿En qué se diferencian la programación síncrona y la asíncrona en Python?</summary>

#### Python

Síncrono: una llamada bloquea el hilo actual hasta completarse. Asíncrono:
`await` cede el control al bucle de eventos mientras la operación espera I/O.

**En resumen:**

- La asincronía reduce el tiempo ocioso durante I/O.
- El modelo síncrono es más simple para lógica lineal.
- La asincronía añade complejidad en gestión de tareas y cancelación.

</details>

<details>
<summary>243. ¿Qué son `async` y `await`?</summary>

#### Python

`async def` define una corrutina. `await` pausa la corrutina hasta que
el objeto esperable esté listo y devuelve el control al bucle.

**En resumen:**

- Es la sintaxis de un modelo asíncrono cooperativo.
- Se usa junto con `asyncio` y bibliotecas asíncronas.
- `await` solo es válido dentro de `async def`.

</details>

<details>
<summary>244. ¿Cómo funciona `asyncio`?</summary>

#### Python

`asyncio` ejecuta un bucle de eventos que procesa tareas (corrutinas), cambiando en
los puntos `await` y planificando operaciones I/O listas.

**Regla crítica:** El bucle de eventos funciona en un solo hilo. Cualquier operación
bloqueante (`time.sleep()`, peticiones síncronas con `requests`, cálculos
pesados) detiene **todo** el ciclo y todas las demás tareas.

**En resumen:**

- Un hilo puede atender muchas tareas I/O gracias a la cooperación.
- La planificación no expulsa tareas de forma preventiva.
- Las llamadas bloqueantes destruyen el rendimiento de `asyncio`.

</details>

<details>
<summary>245. ¿Qué es el bucle de eventos?</summary>

#### Python

El bucle de eventos es un planificador que sigue eventos o disponibilidad de I/O y
ejecuta las devoluciones de llamada o corrutinas correspondientes.

**En resumen:**

- Es el componente central del modelo de `asyncio`.
- Gestiona el ciclo de vida de las tareas asíncronas.
- Determina cuándo cada corrutina continúa ejecutándose.

</details>

<details>
<summary>246. ¿Cómo permite `asyncio` implementar programación asíncrona y qué componentes principales intervienen en código asyncio?</summary>

#### Python

Componentes clave:

- bucle de eventos;
- corrutina (`async def`);
- tarea (`asyncio.create_task`);
- objetos esperables (futures, tareas, corrutinas);
- primitivas de sincronización (`Lock`, `Queue`, `Semaphore`).

**En resumen:**

- `asyncio` combina planificación y API asíncrona en un solo modelo.
- Las tareas comparten un hilo de ejecución de forma cooperativa.
- La arquitectura debe tener en cuenta tiempos de espera, reintentos y cancelación.

</details>

<details>
<summary>247. ¿Cuándo `asyncio` no aporta ventajas?</summary>

#### Python

Cuando la carga es intensiva de CPU o las bibliotecas principales son bloqueantes y no
tienen API asíncrona. Tampoco compensa en scripts simples y cortos.

**Solución para código bloqueante:** Si necesitas usar una biblioteca bloqueante
en un entorno asíncrono, usa `loop.run_in_executor(None, sync_func)`, que la
ejecutará en un hilo aparte sin bloquear el bucle de eventos.

**En resumen:**

- La asincronía no acelera cálculos puros.
- Sin bibliotecas I/O no bloqueantes, la ganancia es mínima.
- `run_in_executor` ayuda a integrar código heredado o síncrono.
- La complejidad asíncrona debe justificarse por la carga.

</details>

<details>
<summary>248. ¿Cómo funciona la cancelación en asyncio?</summary>

#### Python

La cancelación de una tarea (`task.cancel()`) lanza `CancelledError` dentro de
la corrutina. El código debe manejar correctamente la limpieza en `try/finally`.

**En resumen:**

- La cancelación es un flujo de control normal en código asíncrono.
- Hay que diseñar las corrutinas teniendo en cuenta la cancelación.
- Ignorar la cancelación lleva a tareas colgadas.

</details>

<details>
<summary>249. ¿Qué es `contextvars`?</summary>

#### Python

`contextvars` proporciona variables locales al contexto, seguras para
escenarios asíncronos e hilos. Es útil para identificador de solicitud,
identificador de correlación y contexto de inquilino.

**En resumen:**

- Es una alternativa al estado global en código concurrente.
- El valor queda aislado por contexto.
- Mejora el trazado y la observabilidad.

</details>

<details>
<summary>250. ¿Qué buenas prácticas conviene aplicar al escribir código Python?</summary>

#### Python

- seguir PEP 8 y automatizar el formateo;
- escribir anotaciones de tipos explícitas para la API pública;
- usar `with` para recursos;
- cubrir la lógica de negocio con pruebas;
- evitar la optimización prematura y perfilar;
- mantener módulos pequeños con responsabilidad clara;
- gestionar dependencias mediante `pyproject.toml` y una estrategia de bloqueo.

**En resumen:**

- La legibilidad y la previsibilidad importan más que los "trucos".
- La calidad se sostiene en la automatización: análisis estático, tipos, pruebas y CI.
- La simplicidad arquitectónica reduce el coste de mantenimiento.

</details>
