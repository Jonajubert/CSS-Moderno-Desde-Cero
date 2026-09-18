# CSS Moderno Desde Cero

## Capítulo 009 - Bordes

En capítulos anteriores aprendimos sobre:

- Modelo de caja.
- Margin.
- Padding.

Ahora veremos otro componente fundamental del modelo de caja:

```css
border
```

---

## ¿Qué aprenderás?

- Qué es un borde.
- Cómo utilizar `border`.
- Grosor del borde.
- Estilo del borde.
- Color del borde.
- Cómo modificar lados individuales.
- Cómo utilizar `border-radius`.

---

# ¿Dónde está el border?

Recordemos el modelo de caja:

```text
MARGIN
┌─────────────────────────┐
│         BORDER          │
│   ┌─────────────────┐   │
│   │     PADDING     │   │
│   │   ┌─────────┐   │   │
│   │   │ CONTENT │   │   │
│   │   └─────────┘   │   │
│   └─────────────────┘   │
└─────────────────────────┘
```

El borde se encuentra:

```text
padding
   ↓
BORDER
   ↓
margin
```

---

# Crear un borde

Podemos escribir:

```css
.caja {
    border: 2px solid black;
}
```

La propiedad contiene tres componentes:

```text
2px
↓
grosor

solid
↓
estilo

black
↓
color
```

Por lo tanto:

```css
border: grosor estilo color;
```

---

# Grosor

El primer valor controla el grosor:

```css
border: 1px solid black;
```

```css
border: 3px solid black;
```

```css
border: 5px solid black;
```

Cuanto mayor sea el valor, más grueso será el borde.

---

# Estilos

CSS ofrece diferentes estilos.

## solid

```css
border: 3px solid black;
```

```text
──────────────
```

---

## dashed

```css
border: 3px dashed black;
```

```text
── ── ── ──
```

---

## dotted

```css
border: 3px dotted black;
```

```text
· · · · · ·
```

Existen otros valores, pero estos tres son suficientes para comenzar.

---

# Color

El tercer valor establece el color.

```css
border: 3px solid red;
```

También podemos utilizar:

```css
border: 3px solid #7c3aed;
```

o:

```css
border: 3px solid rgb(124, 58, 237);
```

Los colores funcionan de la misma forma que vimos en el capítulo dedicado a colores.

---

# Propiedades individuales

También podemos separar los componentes.

En lugar de:

```css
border: 3px solid black;
```

podemos escribir:

```css
border-width: 3px;
border-style: solid;
border-color: black;
```

Ambas formas pueden producir el mismo resultado.

La primera es una propiedad abreviada o `shorthand`.

---

# Cada lado por separado

Podemos aplicar bordes solamente a determinados lados.

```css
border-top: 3px solid red;
```

```css
border-right: 3px solid blue;
```

```css
border-bottom: 3px solid green;
```

```css
border-left: 3px solid orange;
```

Por ejemplo:

```css
.titulo {
    border-bottom: 2px solid #7c3aed;
}
```

Esto crea solamente una línea debajo del elemento.

---

# Border radius

También podemos redondear las esquinas:

```css
.caja {
    border: 2px solid #7c3aed;
    border-radius: 10px;
}
```

Tenemos:

```text
ANTES

┌───────────────┐
│     CAJA      │
└───────────────┘


DESPUÉS

╭───────────────╮
│     CAJA      │
╰───────────────╯
```

---

# Aumentar el radio

Podemos probar:

```css
border-radius: 5px;
```

```css
border-radius: 15px;
```

```css
border-radius: 30px;
```

Cuanto mayor sea el radio, más redondeadas serán las esquinas.

---

# Crear un círculo

Si tenemos:

```css
.circulo {
    width: 100px;
    height: 100px;

    border: 3px solid #7c3aed;
    border-radius: 50%;
}
```

obtenemos un elemento circular.

Para que sea un círculo:

```text
ancho = alto
```

y utilizamos:

```css
border-radius: 50%;
```

---

# Ejemplo completo

```css
.tarjeta {
    width: 300px;

    padding: 20px;
    margin: 20px;

    border: 2px solid #7c3aed;
    border-radius: 10px;
}
```

Aquí estamos combinando conceptos de los últimos capítulos:

```text
CONTENT
   ↓
PADDING
   ↓
BORDER
   ↓
MARGIN
```

Además:

```text
border-radius
```

redondea las esquinas.

---

# Dato importante

La propiedad:

```css
border
```

puede resumir tres características:

```text
GROSOR
   +
ESTILO
   +
COLOR
```

Por ejemplo:

```css
border: 3px solid #7c3aed;
```

Mientras que:

```css
border-radius: 10px;
```

controla el redondeo de las esquinas.

Son propiedades diferentes.

---

# Ejercicio

Creá:

```html
<div class="tarjeta">
    Aprendiendo CSS
</div>
```

Aplicale:

```css
.tarjeta {
    padding: 20px;

    border: 3px solid #7c3aed;

    border-radius: 10px;
}
```

Después modificá:

1. El grosor.
2. El estilo.
3. El color.
4. El radio.

Observá cómo cambia el elemento.

---

# Desafío

Creá tres cajas:

```text
SOLID
DASHED
DOTTED
```

Cada una debe utilizar un estilo de borde diferente.

Después agregá una cuarta caja con:

```css
border-radius: 20px;
```

Intentá conseguir cuatro diseños claramente diferentes utilizando solamente las propiedades vistas hasta ahora.

---

# Resumen

La estructura básica es:

```css
border: grosor estilo color;
```

Por ejemplo:

```css
border: 3px solid #7c3aed;
```

Los estilos más comunes que vimos son:

```text
solid
dashed
dotted
```

También podemos modificar lados individuales:

```css
border-top
border-right
border-bottom
border-left
```

y redondear las esquinas utilizando:

```css
border-radius
```

Con `border`, `padding` y `margin` ya podemos controlar gran parte de la apariencia y el espaciado del modelo de caja.
