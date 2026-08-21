# CSS Moderno Desde Cero

## Capítulo 005 - Unidades de medida

CSS necesita unidades para definir tamaños, distancias y espacios.

Hasta ahora vimos valores como:

```css
font-size: 32px;
```

Pero CSS proporciona muchas otras formas de expresar una medida.

En este capítulo conoceremos:

- `px`
- `%`
- `rem`
- `vw`
- `vh`

---

# ¿Qué aprenderás?

- Qué es una unidad de medida.
- Diferencia entre unidades absolutas y relativas.
- Cómo utilizar `px`.
- Cómo utilizar `%`.
- Cómo utilizar `rem`.
- Cómo utilizar `vw`.
- Cómo utilizar `vh`.

---

# ¿Qué es una unidad de medida?

Observemos:

```css
width: 300px;
```

Tenemos:

```text
300 → valor
px  → unidad
```

La unidad indica cómo debe interpretar CSS ese valor.

---

# px

`px` significa píxel CSS.

Por ejemplo:

```css
width: 300px;
```

o:

```css
font-size: 32px;
```

`px` se considera una unidad absoluta en CSS.

Es útil cuando necesitamos especificar una medida concreta.

---

# %

El porcentaje representa una medida relativa.

Por ejemplo:

```css
.contenedor {
    width: 80%;
}
```

En este caso el ancho se calcula normalmente en relación con el ancho del bloque contenedor.

Podemos visualizarlo así:

```text
CONTENEDOR
100%

┌─────────────────────────────┐
│                             │
│   ELEMENTO                  │
│   80%                       │
│   ┌─────────────────────┐   │
│   │                     │   │
│   └─────────────────────┘   │
│                             │
└─────────────────────────────┘
```

El significado exacto de `%` depende de la propiedad donde se utilice.

---

# rem

`rem` es una unidad relativa al tamaño de fuente del elemento raíz:

```html
<html>
```

Por ejemplo:

```css
h1 {
    font-size: 2rem;
}
```

Si el tamaño de fuente raíz es:

```text
16px
```

entonces:

```text
1rem = 16px
2rem = 32px
```

Pero esto depende del tamaño definido para el elemento raíz.

---

# vw

`vw` significa:

```text
Viewport Width
```

Es decir:

```text
ancho del viewport
```

`1vw` representa el 1% del ancho del viewport.

Por ejemplo:

```css
.tarjeta {
    width: 50vw;
}
```

significa que la tarjeta tendrá un ancho equivalente al 50% del viewport.

---

# vh

`vh` significa:

```text
Viewport Height
```

`1vh` representa el 1% de la altura del viewport.

Por ejemplo:

```css
.hero {
    height: 100vh;
}
```

representa una altura equivalente al 100% de la altura del viewport.

---

# Absolutas vs relativas

Podemos hacer una primera clasificación:

| Unidad | Tipo | Referencia |
|---|---|---|
| `px` | Absoluta | Píxel CSS |
| `%` | Relativa | Depende de la propiedad/contexto |
| `rem` | Relativa | Tamaño de fuente raíz |
| `vw` | Relativa | Ancho del viewport |
| `vh` | Relativa | Alto del viewport |

---

# Ejemplo

```css
header {
    padding: 20px;
}

h1 {
    font-size: 2rem;
}

.contenedor {
    width: 80%;
}

.tarjeta {
    width: 50vw;
    min-height: 20vh;
}
```

En un mismo diseño podemos utilizar diferentes unidades.

No existe una única unidad correcta para todo.

---

# ¿Cuál debería utilizar?

Depende de lo que queramos medir.

Por ejemplo:

```text
px
↓
Medidas concretas.

%
↓
Tamaños relativos al contexto.

rem
↓
Muy útil para tamaños relacionados
con la tipografía raíz.

vw / vh
↓
Tamaños relacionados con el viewport.
```

La elección depende del comportamiento que queremos obtener.

---

# Curiosidad

Supongamos que el viewport tiene:

```text
1200px de ancho
```

Entonces:

```css
width: 50vw;
```

representa aproximadamente:

```text
600px
```

Si el viewport pasa a medir:

```text
800px
```

entonces:

```text
50vw
```

representará:

```text
400px
```

El valor se adapta al tamaño del viewport.

---

# Ejercicio

Crear un elemento:

```html
<div class="caja">
    Aprendiendo CSS
</div>
```

Aplicar:

```css
.caja {
    width: 80%;
    min-height: 20vh;
    font-size: 2rem;
}
```

Después modificar el tamaño de la ventana del navegador.

Observá qué medidas cambian junto con ella.

---

# Dato importante

No existe una unidad de medida que debamos utilizar para todo.

La pregunta correcta es:

```text
¿Respecto de qué quiero
que se calcule este tamaño?
```

La respuesta nos ayudará a elegir la unidad adecuada.

---

# Próximo capítulo

Seguiremos construyendo nuestro conocimiento de CSS para crear interfaces cada vez más flexibles y adaptables.
