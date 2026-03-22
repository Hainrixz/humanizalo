# Humanizalo

**[Read in English](README.md)**

Haz que el texto generado por IA suene como si lo hubiera escrito una persona real.

---

## El problema

La IA escribe de una forma que se nota. Usa las mismas palabras rebuscadas una y otra vez ("profundizar," "panorama," "tejido"). Le encantan los guiones largos. Empieza las oraciones con "La verdad es que:" y termina con "El futuro se ve prometedor." Suena como un robot tratando de parecer inteligente.

Humanizalo arregla eso.

## Como funciona (la version simple)

Le das texto que suena como si lo escribio una IA. Te devuelve texto que suena como si lo escribiste tu.

**Antes:**
> En el panorama actual en rapida evolucion, es crucial aprovechar las sinergias multifuncionales y fomentar una cultura de innovacion. Las implicaciones son significativas. El futuro se ve prometedor.

**Despues:**
> Muevete mas rapido. Tu competencia ya lo esta haciendo.

Eso es todo. Pegas texto de robot, te devuelve texto humano.

---

## Instalacion (2 minutos)

Necesitas tener [Claude Code](https://claude.ai/code) instalado en tu computadora.

### Paso 1: Abre tu terminal

En Mac, abre la app Terminal. En Windows, abre Command Prompt o PowerShell.

### Paso 2: Copia y pega este comando

```bash
git clone https://github.com/Hainrixz/humanizalo.git ~/.claude/skills/humanizalo
```

Presiona Enter. Espera a que termine. Listo.

### Si eso no funciono

Tambien puedes hacerlo manualmente:
1. Descarga este proyecto (boton verde "Code" en GitHub, luego "Download ZIP")
2. Descomprime el archivo
3. Pon la carpeta en esta ruta en tu computadora: `~/.claude/skills/humanizalo/`

Los archivos importantes son `SKILL.md` y la carpeta `references/`. Esos tienen que estar dentro de esa ruta.

---

## Como usarlo

### Opcion 1: El comando slash

En Claude Code, escribe:

```
/humanizalo
```

Luego pega el texto que quieres humanizar.

### Opcion 2: Solo pidelo

Escribe algo como:

```
Por favor humaniza este texto: [pega tu texto aqui]
```

### Opcion 3: Apuntalo a un archivo

```
Humaniza el texto en mi-borrador.md
```

---

## Que hace exactamente?

Humanizalo busca 40 patrones especificos que delatan la escritura de IA. Aqui van las cinco categorias:

### 1. Contenido inflado

A la IA le encanta hacer que las cosas suenen mas importantes de lo que son. "Un hito fundamental" cuando podria decir simplemente "un punto de inflexion." "Los expertos opinan" sin nombrar a ningun experto.

### 2. Vocabulario de robot

La IA tiene palabras favoritas. Probablemente ya las has notado: "profundizar," "crucial," "potenciar," "panorama," "fomentar," "subrayar." Humanizalo las cambia por palabras normales.

### 3. Estructuras predecibles

A la IA le encantan patrones como "No es X. Es Y." o darle acciones humanas a cosas que no son humanas ("los datos nos dicen" en vez de "vimos los datos y encontramos"). Tambien fuerza todo en grupos de tres.

### 4. Formato delator

Guiones largos por todos lados. Texto en negritas en todo. Mayusculas En Cada Palabra De Cada Titulo. Humanizalo elimina todo eso.

### 5. Habitos de chatbot

"Espero que esto te ayude!" "Excelente pregunta!" "Segun mi ultima actualizacion..." "Vale la pena mencionar que..." Esto grita "un chatbot escribio esto." Fuera.

---

## El ingrediente secreto: revisa su propio trabajo

La mayoria de las herramientas reescriben una vez y ya. Humanizalo reescribe, luego se pregunta "esto todavia suena a IA?" y arregla lo que encuentra. Hace esto hasta 3 veces.

Tambien califica el resultado en 6 cualidades (claridad, ritmo, confianza, autenticidad, densidad y alma) en una escala del 1 al 10 cada una. Si el total esta por debajo de 42 de 60, sigue trabajando.

---

## Que recibes de vuelta

Cuando Humanizalo termina, recibes:

1. **Tu texto humanizado** - la version final
2. **Una calificacion** - que tan humano suena (de 60)
3. **Que cambio** - un resumen corto de lo que arreglo

---

## La lista completa de patrones

Para los curiosos, aqui estan los 40 patrones que detecta:

| # | Que detecta | Tipo |
|---|------------|------|
| P01 | Hacer que las cosas suenen mas importantes de lo que son | Contenido |
| P02 | Mencionar nombres famosos sin citas reales | Contenido |
| P03 | Palabras "-ando/-endo" falsamente profundas (destacando, reflejando) | Contenido |
| P04 | Lenguaje de ventas (impresionante, innovador, vibrante) | Contenido |
| P05 | "Los expertos dicen" sin nombrar expertos | Contenido |
| P06 | "A pesar de los desafios... sigue prosperando" | Contenido |
| P07 | Finales tipo "El futuro se ve prometedor" | Contenido |
| P08 | Declaraciones vagas y grandiosas ("Lo que esta en juego es mucho") | Contenido |
| P09 | Palabras favoritas de la IA (profundizar, panorama, tejido, etc.) | Vocabulario |
| P10 | "Funge como" en vez de "es" | Vocabulario |
| P11 | Demasiados adverbios (realmente, genuinamente, fundamentalmente) | Vocabulario |
| P12 | Jerga corporativa (sinergia, inmersion profunda, apostar por) | Vocabulario |
| P13 | "Todos," "siempre," "nunca" (generalizaciones) | Vocabulario |
| P14 | Demasiados pares con guion (multifuncional, basado-en-datos) | Vocabulario |
| P15 | Contrastes dramaticos "No es X. Es Y." | Estructura |
| P16 | Listas negativas "No es... No es... Es..." | Estructura |
| P17 | Fragmentos tipo "Velocidad. Eso es todo." | Estructura |
| P18 | "Que pasaria si te dijera que..." introducciones | Estructura |
| P19 | Cosas haciendo acciones humanas ("los datos nos dicen") | Estructura |
| P20 | Voz de narrador flotante ("La gente tiende a...") | Estructura |
| P21 | Voz pasiva ("Se cometieron errores") | Estructura |
| P22 | Construcciones "No solo X, sino tambien Y" | Estructura |
| P23 | Forzar todo en grupos de tres | Estructura |
| P24 | Usar diferentes palabras para lo mismo para no repetir | Estructura |
| P25 | Rangos falsos "De X a Y" | Estructura |
| P26 | Todas las oraciones del mismo largo | Estructura |
| P27 | Guiones largos por todos lados | Formato |
| P28 | Negritas en todo | Formato |
| P29 | Emojis random en texto serio | Formato |
| P30 | Comillas tipograficas "fancy" | Formato |
| P31 | Mayusculas En Cada Palabra Del Titulo | Formato |
| P32 | Frases de chatbot "Espero que esto te ayude!" | Comunicacion |
| P33 | Advertencias tipo "Segun mi ultima actualizacion..." | Comunicacion |
| P34 | Amabilidad y acuerdo exagerados | Comunicacion |
| P35 | Introducciones tipo "La verdad es que:" | Comunicacion |
| P36 | Trucos de enfasis "Dejalo reposar." | Comunicacion |
| P37 | "En esta seccion veremos..." narrar la estructura | Comunicacion |
| P38 | "Te lo prometo" y "esto es genuinamente dificil" | Comunicacion |
| P39 | "Con el fin de" en vez de solo "para" | Comunicacion |
| P40 | Acumular dudas ("podria potencialmente quizas tal vez") | Comunicacion |

---

## Archivos en este proyecto

```
humanizalo/
├── SKILL.md              # El cerebro (Claude lee este archivo)
├── README.md             # Este archivo en ingles
├── README.es.md          # Estas aqui
├── LICENSE               # MIT (usalo como quieras)
└── references/
    ├── vocabulary.md     # Listas de palabras de IA y sus reemplazos
    ├── structures.md     # Patrones estructurales a evitar
    ├── formatting.md     # Reglas de formato
    ├── communication.md  # Habitos de chatbot a eliminar
    └── examples.md       # 5 ejemplos de antes/despues
```

---

## Licencia

MIT. Usalo, modificalo, compartelo.
