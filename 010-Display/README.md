# CSS Moderno Desde Cero

## Capítulo 010 - Display

La propiedad:

```css
display
```

determina cómo se comporta un elemento dentro del flujo de la página.

En este capítulo veremos tres valores fundamentales:

```css
block
inline
inline-block
```

---

## display: block

Un elemento `block` comienza en una nueva línea y, de forma predeterminada, ocupa el ancho disponible de su contenedor.

```css
.caja {
    display: block;
}
```

Elementos HTML como:

```html
<div>
<p>
<section>
```

se comportan normalmente como elementos de bloque.

Visualmente:

```text
┌────────────────────────────┐
│ Elemento 1                 │
└────────────────────────────┘

┌────────────────────────────┐
│ Elemento 2                 │
└────────────────────────────┘
```

---

## display: inline

Un elemento `inline` participa en el flujo de texto y ocupa solamente el espacio necesario para su contenido.

```css
.elemento {
    display: inline;
}
```

Por ejemplo:

```html
<span>HTML</span>
<span>CSS</span>
<span>JavaScript</span>
```

pueden aparecer:

```text
HTML  CSS  JavaScript
```

sin comenzar necesariamente una nueva línea.

---

## Una diferencia importante

En elementos `inline`, propiedades como `width` y `height` no controlan la caja de la misma manera que en un elemento `block`.

Por eso existe otra alternativa:

```css
inline-block
```

---

## display: inline-block

`inline-block` combina características de ambos comportamientos.

```css
.boton {
    display: inline-block;

    width: 150px;
    padding: 10px;
}
```

Los elementos pueden permanecer uno al lado del otro:

```text
┌────────────┐ ┌────────────┐
│ Elemento 1 │ │ Elemento 2 │
└────────────┘ └────────────┘
```

pero podemos controlar dimensiones y propiedades del modelo de caja de forma similar a un bloque.

---

## Comparación

```text
BLOCK
────────────────────────
Nueva línea
Ocupa el ancho disponible
Permite width y height


INLINE
────────────────────────
Permanece en línea
Ocupa el espacio necesario
width y height no actúan
como en un bloque


INLINE-BLOCK
────────────────────────
Permanece en línea
Permite controlar
width y height
```

---

## display: none

Existe otro valor muy utilizado:

```css
display: none;
```

Por ejemplo:

```css
.mensaje {
    display: none;
}
```

El elemento deja de participar en el layout y no se muestra.

Esto será especialmente útil cuando combinemos CSS con JavaScript.

---

## display y HTML

Los elementos HTML ya poseen un valor de `display` predeterminado definido por la hoja de estilos del navegador.

Por ejemplo, normalmente:

```html
<div>
```

se comporta como:

```css
display: block;
```

Mientras que:

```html
<span>
```

se comporta como:

```css
display: inline;
```

CSS nos permite modificar ese comportamiento.

---

## Curiosidad

`display` es una propiedad histórica y central de CSS, pero ha evolucionado considerablemente.

Actualmente también encontraremos valores como:

```css
display: flex;
```

y:

```css
display: grid;
```

Estos permiten construir sistemas de distribución mucho más potentes.

Los veremos en capítulos posteriores.

---

## Ejercicio

Crear tres elementos:

```html
<span class="elemento">HTML</span>
<span class="elemento">CSS</span>
<span class="elemento">JavaScript</span>
```

Primero utilizar:

```css
.elemento {
    display: inline;
}
```

Después cambiar a:

```css
display: block;
```

y finalmente:

```css
display: inline-block;
```

Observar cómo cambia la distribución.

---

## Desafío

Crear tres botones visuales utilizando:

```html
<a href="#">Inicio</a>
<a href="#">Productos</a>
<a href="#">Contacto</a>
```

Aplicar:

```css
display: inline-block;
```

y después agregar:

```css
padding: 10px 20px;
margin: 5px;
border: 2px solid #7c3aed;
```

El objetivo es obtener tres elementos alineados horizontalmente pero con dimensiones y espaciado controlables.

---

## Resumen

```css
display: block;
```

→ elemento en bloque.

```css
display: inline;
```

→ elemento dentro de la línea.

```css
display: inline-block;
```

→ permanece en línea pero permite controlar su caja.

```css
display: none;
```

→ oculta el elemento y lo elimina del layout.

Comprender `display` es uno de los pasos fundamentales antes de avanzar hacia sistemas de layout como **Flexbox y CSS Grid**.
