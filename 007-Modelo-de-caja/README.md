# CSS Moderno Desde Cero

## Capítulo 007 - Modelo de caja

En CSS, prácticamente todos los elementos se representan como cajas.

Comprender cómo funciona esa caja es fundamental para controlar tamaños y espacios.

---

# ¿Qué aprenderás?

- Qué es el modelo de caja.
- Qué es el contenido.
- Qué hace `padding`.
- Qué hace `border`.
- Qué hace `margin`.
- Cómo funciona `width`.
- Qué hace `box-sizing`.
- Diferencia entre `content-box` y `border-box`.

---

# El modelo de caja

Cada elemento puede imaginarse así:

```text
MARGIN
  │
  └── BORDER
       │
       └── PADDING
            │
            └── CONTENT
```

O visualmente:

```text
┌─────────────────────────────┐
│           MARGIN            │
│   ┌─────────────────────┐   │
│   │       BORDER        │   │
│   │   ┌─────────────┐   │   │
│   │   │   PADDING   │   │   │
│   │   │  ┌───────┐  │   │   │
│   │   │  │CONTENT│  │   │   │
│   │   │  └───────┘  │   │   │
│   │   └─────────────┘   │   │
│   └─────────────────────┘   │
└─────────────────────────────┘
```

---

# Content

El contenido es la parte interna del elemento.

Por ejemplo:

```html
<div>
    Hola
</div>
```

El texto:

```text
Hola
```

forma parte del contenido.

---

# Padding

`padding` agrega espacio dentro de la caja.

```css
.tarjeta {
    padding: 20px;
}
```

Se encuentra entre:

```text
contenido
y
borde
```

---

# Border

`border` rodea al contenido y al padding.

```css
.tarjeta {
    border: 2px solid black;
}
```

Tenemos:

```text
2px   → grosor
solid → estilo
black → color
```

---

# Margin

`margin` crea espacio fuera del borde.

```css
.tarjeta {
    margin: 30px;
}
```

Este espacio separa el elemento de otras cajas.

---

# Diferencia entre padding y margin

Podemos pensarlo así:

```text
PADDING
↓
espacio interno


MARGIN
↓
espacio externo
```

Esta diferencia es fundamental.

---

# Width

Podemos definir:

```css
width: 300px;
```

Pero aparece una pregunta:

> ¿300px incluyen el padding y el border?

Depende de `box-sizing`.

---

# content-box

Por defecto, CSS utiliza:

```css
box-sizing: content-box;
```

Con:

```css
width: 300px;
padding: 20px;
border: 2px solid black;
```

el ancho total visible será mayor que 300px.

Tenemos:

```text
300px contenido
+
40px padding
+
4px border
=
344px
```

El margin queda fuera de ese cálculo.

---

# border-box

Si utilizamos:

```css
box-sizing: border-box;
```

el valor definido en:

```css
width: 300px;
```

incluye:

```text
contenido
+
padding
+
border
```

Por lo tanto:

```text
ANCHO TOTAL
=
300px
```

Esto suele resultar mucho más fácil de manejar.

---

# Una regla muy utilizada

Es común encontrar:

```css
* {
    box-sizing: border-box;
}
```

El selector:

```css
*
```

selecciona todos los elementos.

Así aplicamos `border-box` a toda la página.

---

# Ejemplo completo

```css
* {
    box-sizing: border-box;
}

.tarjeta {
    width: 300px;
    padding: 20px;
    border: 2px solid #333;
    margin: 30px;
}
```

---

# Comparación

## content-box

```text
width = contenido

300
+ padding
+ border

= más de 300px
```

## border-box

```text
width = caja total

contenido
+ padding
+ border

= 300px
```

---

# ¿Y el margin?

El `margin` siempre queda fuera del tamaño de la caja definido por `width`.

Podemos representar:

```text
MARGIN
    │
    ▼
┌──────────────────────────┐

        CAJA
        300px

└──────────────────────────┘
```

El espacio de margin se suma externamente.

---

# Ejercicio

Crear:

```html
<div class="caja">
    Aprendiendo CSS
</div>
```

Aplicar:

```css
.caja {
    width: 300px;
    padding: 20px;
    border: 5px solid blue;
    margin: 30px;
}
```

Primero probar sin:

```css
box-sizing: border-box;
```

Después agregar:

```css
box-sizing: border-box;
```

y observar cómo cambia el tamaño.

---

# Dato importante

`padding` y `margin` no hacen lo mismo.

```text
padding
→ espacio dentro del borde

margin
→ espacio fuera del borde
```

Y:

```css
box-sizing: border-box;
```

hace que controlar `width` y `height` sea mucho más predecible.

---

# Próximo capítulo

Comprender el modelo de caja nos permitirá trabajar mucho mejor con tamaños, espacios y distribución de elementos.

Es una base fundamental para empezar a construir layouts más complejos.
