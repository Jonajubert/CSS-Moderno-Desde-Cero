# CSS Moderno Desde Cero

## Capítulo 006 - Tipografías

En los capítulos anteriores comenzamos a modificar la apariencia de nuestras páginas utilizando CSS.

Ya vimos colores y unidades de medida.

Ahora aprenderemos a controlar uno de los elementos visuales más importantes de cualquier interfaz:

**el texto.**

---

# ¿Qué aprenderás?

En este capítulo veremos:

- `font-family`
- `font-size`
- `font-weight`
- `font-style`
- `line-height`
- `text-align`
- Qué es un font stack.
- Por qué la tipografía afecta la legibilidad.

---

# font-family

La propiedad:

```css
font-family
```

permite definir la familia tipográfica.

Por ejemplo:

```css
body {
    font-family: Arial, sans-serif;
}
```

Podemos indicar más de una opción:

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

El navegador intenta utilizarlas en orden.

```text
Arial
  ↓
Helvetica
  ↓
sans-serif
```

Si una fuente no está disponible, intenta utilizar la siguiente.

---

# ¿Qué es sans-serif?

En:

```css
font-family: Arial, Helvetica, sans-serif;
```

`Arial` y `Helvetica` son familias concretas.

En cambio:

```css
sans-serif
```

es una familia genérica.

Le estamos diciendo al navegador:

> Si las anteriores no están disponibles, utilizá una fuente del sistema que pertenezca a la categoría sans-serif.

---

# font-size

Controla el tamaño del texto.

```css
p {
    font-size: 16px;
}
```

También podemos utilizar las unidades que vimos en el capítulo anterior:

```css
h1 {
    font-size: 2.5rem;
}
```

Por ejemplo:

```css
h1 {
    font-size: 2.5rem;
}

h2 {
    font-size: 1.75rem;
}

p {
    font-size: 1rem;
}
```

Esto ayuda a construir una jerarquía visual.

---

# Jerarquía tipográfica

No todo el texto debería tener la misma importancia visual.

Podemos representar una jerarquía sencilla:

```text
TÍTULO PRINCIPAL
2.5rem
████████████████

SUBTÍTULO
1.75rem
████████████

Texto normal
1rem
████████
```

El tamaño ayuda al usuario a identificar rápidamente la estructura del contenido.

---

# font-weight

Controla el grosor de la tipografía.

Por ejemplo:

```css
p {
    font-weight: 400;
}

h1 {
    font-weight: 700;
}
```

Valores habituales incluyen:

```text
400 → normal
700 → negrita
```

Las fuentes pueden admitir distintos pesos dependiendo de la familia tipográfica utilizada.

---

# font-style

Permite definir el estilo de la fuente.

Por ejemplo:

```css
.subtitulo {
    font-style: italic;
}
```

Podemos obtener:

```text
Texto normal

Texto en cursiva
```

---

# line-height

`line-height` controla la altura de línea.

Por ejemplo:

```css
p {
    line-height: 1.5;
}
```

Comparémoslo conceptualmente:

```text
line-height pequeño

Primera línea
Segunda línea
Tercera línea


line-height mayor

Primera línea

Segunda línea

Tercera línea
```

Un espaciado adecuado puede mejorar significativamente la legibilidad de párrafos largos.

---

# text-align

También podemos controlar la alineación del texto:

```css
text-align: left;
```

```css
text-align: center;
```

```css
text-align: right;
```

Por ejemplo:

```css
h1 {
    text-align: center;
}
```

centra el contenido textual del título dentro de su caja.

---

# Ejemplo completo

```css
body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    line-height: 1.5;
}

h1 {
    font-size: 2.5rem;
    font-weight: 700;
    text-align: center;
}

.subtitulo {
    font-size: 1.25rem;
    font-style: italic;
    text-align: center;
}

h2 {
    font-size: 1.75rem;
    font-weight: 600;
}

.destacado {
    font-size: 1.1rem;
    font-weight: 700;
}
```

---

# Tipografía y legibilidad

La tipografía no sirve únicamente para decorar.

También influye en:

```text
LEGIBILIDAD
     │
     ├── Tamaño
     ├── Grosor
     ├── Altura de línea
     ├── Contraste
     └── Jerarquía
```

Una interfaz puede ser visualmente atractiva y, aun así, resultar incómoda de leer.

---

# Font stack

Cuando escribimos:

```css
font-family: Arial, Helvetica, sans-serif;
```

estamos creando un:

```text
FONT STACK
```

Es una lista de fuentes ordenadas por preferencia.

El navegador utiliza la primera disponible.

```text
1. Arial
      ↓
2. Helvetica
      ↓
3. sans-serif
```

Esto permite definir alternativas cuando una fuente específica no está disponible.

---

# Ejercicio

Creá tres elementos:

```html
<h1>Título principal</h1>

<h2>Subtítulo</h2>

<p>
    Este es un párrafo de ejemplo.
</p>
```

Después intentá crear una jerarquía visual utilizando:

```css
font-family
font-size
font-weight
line-height
```

El objetivo es que sea posible distinguir inmediatamente:

```text
TÍTULO
   ↓
SUBTÍTULO
   ↓
CONTENIDO
```

sin modificar el HTML.

---

# Dato importante

Una buena tipografía no significa simplemente elegir una fuente atractiva.

También debemos considerar:

- Tamaño.
- Grosor.
- Espaciado.
- Jerarquía.
- Legibilidad.

CSS nos permite controlar todos estos aspectos.

---

# Próximo capítulo

Ya sabemos modificar colores, medidas y tipografías.

Seguiremos incorporando propiedades para tener cada vez más control sobre el diseño de nuestras páginas.
