# CSS Moderno Desde Cero

## Capítulo 004 - Colores

En los capítulos anteriores aprendimos qué es CSS, cómo conectarlo con HTML y cómo seleccionar elementos.

Ahora comenzaremos a modificar su apariencia utilizando colores.

---

# ¿Qué aprenderás?

- Cómo cambiar el color del texto.
- Cómo cambiar el color de fondo.
- Colores por nombre.
- Colores hexadecimales.
- Colores RGB.
- Colores HSL.

---

# La propiedad color

Para modificar el color del texto utilizamos:

```css
color:
```

Por ejemplo:

```css
h1 {
    color: blue;
}
```

Esto hará que el texto contenido dentro del `<h1>` se muestre en azul.

---

# Colores por nombre

CSS reconoce nombres de colores.

```css
p {
    color: red;
}
```

Otros ejemplos:

```text
blue
white
black
green
yellow
orange
```

Es una forma sencilla de comenzar, aunque proporciona menos control que otros formatos.

---

# Colores hexadecimales

También podemos representar un color mediante hexadecimal.

Por ejemplo:

```css
h1 {
    color: #264de4;
}
```

Un color hexadecimal suele representarse mediante:

```text
#RRGGBB
```

donde los pares representan:

```text
RR → rojo
GG → verde
BB → azul
```

Por ejemplo:

```text
#FF0000 → rojo
#00FF00 → verde
#0000FF → azul
#FFFFFF → blanco
#000000 → negro
```

---

# RGB

RGB representa las cantidades de:

```text
Red
Green
Blue
```

Su sintaxis es:

```css
color: rgb(rojo, verde, azul);
```

Por ejemplo:

```css
p {
    color: rgb(60, 60, 60);
}
```

Cada canal utiliza normalmente valores entre:

```text
0 y 255
```

---

# HSL

Otra forma de representar colores es HSL.

Significa:

```text
Hue        → tono
Saturation → saturación
Lightness  → luminosidad
```

Por ejemplo:

```css
h2 {
    color: hsl(230, 75%, 52%);
}
```

HSL puede resultar especialmente cómodo cuando queremos modificar visualmente un color manteniendo una relación entre diferentes tonos.

---

# Color de fondo

Hasta ahora modificamos el texto.

Para cambiar el fondo utilizamos:

```css
background-color:
```

Por ejemplo:

```css
.destacado {
    background-color: #264de4;
}
```

También podemos combinar ambas propiedades:

```css
.destacado {
    color: white;
    background-color: #264de4;
}
```

---

# color vs background-color

Es importante distinguirlas:

```text
color
↓
Color del texto


background-color
↓
Color del fondo
```

Ejemplo:

```css
.destacado {
    color: white;
    background-color: blue;
}
```

---

# Comparación rápida

| Formato | Ejemplo |
|---|---|
| Nombre | `blue` |
| Hexadecimal | `#264de4` |
| RGB | `rgb(38, 77, 228)` |
| HSL | `hsl(230, 79%, 52%)` |

Todos representan colores.

La diferencia está en cómo definimos sus valores.

---

# Ejercicio

Crear una página con:

- Un título.
- Un subtítulo.
- Dos párrafos.
- Un elemento destacado.

Aplicar diferentes formatos:

```css
h1 {
    color: blue;
}

h2 {
    color: #264de4;
}

p {
    color: rgb(60, 60, 60);
}

.destacado {
    color: white;
    background-color: #264de4;
}
```

Después modificar los valores y observar los resultados.

---

# Dato importante

`color` y `background-color` cumplen funciones diferentes.

```css
color: white;
```

modifica el texto.

Mientras que:

```css
background-color: blue;
```

modifica el fondo.

---

# Próximo capítulo

Continuaremos trabajando sobre la presentación visual de nuestra página incorporando nuevas propiedades CSS.
