# CSS Moderno Desde Cero

## Capítulo 008 - Margin y padding

En el capítulo anterior aprendimos cómo funciona el modelo de caja.

Ahora veremos dos propiedades fundamentales para controlar los espacios:

```css
margin
padding
```

---

## ¿Qué aprenderás?

- Qué es `padding`.
- Qué es `margin`.
- Diferencias entre ambos.
- Cómo modificar cada lado.
- Cómo utilizar la sintaxis abreviada.
- Cómo aplicar estos conceptos en un ejemplo.

---

# Padding

`padding` controla el espacio interno de un elemento.

```css
.caja {
    padding: 20px;
}
```

Podemos representarlo:

```text
┌──────────── BORDER ────────────┐
│                               │
│           PADDING             │
│                               │
│        ┌────────────┐         │
│        │ CONTENIDO  │         │
│        └────────────┘         │
│                               │
└───────────────────────────────┘
```

El espacio se encuentra entre el contenido y el borde.

---

# Margin

`margin` controla el espacio externo.

```css
.caja {
    margin: 30px;
}
```

Podemos representarlo:

```text
              MARGIN

       ┌───────────────┐
       │     CAJA      │
       └───────────────┘

              MARGIN
```

Sirve para separar un elemento de otros elementos.

---

# Diferencia fundamental

```text
PADDING
   ↓
Espacio interno


MARGIN
   ↓
Espacio externo
```

Esta es la diferencia principal que debemos recordar.

---

# Controlar cada lado

Podemos modificar cada lado individualmente.

## Margin

```css
.caja {
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 30px;
    margin-left: 40px;
}
```

## Padding

```css
.caja {
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 30px;
    padding-left: 40px;
}
```

---

# Forma abreviada

También podemos utilizar cuatro valores:

```css
margin: 10px 20px 30px 40px;
```

El orden es:

```text
arriba
derecha
abajo
izquierda
```

Podemos recordarlo siguiendo las agujas del reloj:

```text
        ARRIBA
           ↓

IZQUIERDA ← □ → DERECHA

           ↓
         ABAJO
```

---

# Dos valores

También podemos escribir:

```css
margin: 10px 20px;
```

Esto significa:

```text
10px → arriba y abajo
20px → izquierda y derecha
```

Lo mismo funciona con:

```css
padding: 10px 20px;
```

---

# Un valor

Si escribimos:

```css
padding: 20px;
```

aplicamos el mismo valor a los cuatro lados:

```text
       20px
         ↓

20px ← CAJA → 20px

         ↓
       20px
```

---

# Ejemplo

```css
.caja {
    background-color: #4e73df;
    color: white;

    padding: 20px;
    margin: 30px;
}
```

Tenemos:

```text
margin: 30px
↓
separación externa

padding: 20px
↓
separación interna
```

---

# ¿Padding modifica el tamaño?

Sí, dependiendo del modelo de caja utilizado.

Con el comportamiento predeterminado:

```css
box-sizing: content-box;
```

el `padding` se agrega al tamaño definido para el contenido.

Como vimos en el capítulo anterior, podemos utilizar:

```css
* {
    box-sizing: border-box;
}
```

para hacer más predecibles las dimensiones.

---

# ¿Margin modifica el contenido?

No.

`margin` genera espacio alrededor del elemento.

Está fuera del borde y no aumenta el área interna disponible para el contenido.

---

# Ejemplo completo

```css
* {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

.contenedor {
    padding: 20px;
}

.caja {
    background-color: #4e73df;
    color: white;

    padding: 20px;
    margin: 30px;

    border-radius: 8px;
}
```

---

# Dato importante

Recordá:

```text
CONTENT
   ↓
PADDING
   ↓
BORDER
   ↓
MARGIN
```

Por lo tanto:

```text
padding = espacio interno
margin  = espacio externo
```

---

# Ejercicio

Creá:

```html
<div class="caja">
    Aprendiendo CSS
</div>
```

Después aplicá:

```css
.caja {
    padding: 20px;
    margin: 30px;
}
```

Probá cambiar ambos valores y observá qué parte de la caja se modifica.

---

# Desafío

Probá:

```css
padding: 10px 30px;
```

y después:

```css
margin: 10px 20px 30px 40px;
```

Intentá predecir el resultado antes de verlo en el navegador.

---

# Resumen

```text
PADDING
→ dentro de la caja

MARGIN
→ fuera de la caja
```

Dominar estas dos propiedades es fundamental para controlar correctamente el espaciado de una interfaz.
