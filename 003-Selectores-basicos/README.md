# CSS Moderno Desde Cero

## Capítulo 003 - Selectores básicos

En los capítulos anteriores aprendimos qué es CSS y cómo conectarlo con un documento HTML.

Ahora comenzaremos a utilizar CSS para seleccionar elementos específicos de nuestra página.

Para hacerlo utilizamos **selectores**.

---

# ¿Qué aprenderás?

- Qué es un selector.
- Selector de etiqueta.
- Selector de clase.
- Selector de ID.
- Diferencias entre `.clase` y `#id`.

---

# ¿Qué es un selector?

Un selector le indica a CSS:

> ¿A qué elemento HTML quiero aplicar estos estilos?

Por ejemplo:

```css
p {
    color: gray;
}
```

En este caso:

```css
p
```

es el selector.

CSS buscará todos los elementos:

```html
<p>
```

y aplicará el estilo indicado.

---

# 1. Selector de etiqueta

Selecciona todos los elementos HTML de un determinado tipo.

```css
p {
    color: #555;
}
```

Si nuestra página tiene cinco elementos `<p>`, el estilo se aplicará a los cinco.

---

# 2. Selector de clase

Las clases permiten identificar uno o varios elementos.

En HTML:

```html
<p class="destacado">
    Texto destacado
</p>
```

En CSS utilizamos un punto:

```css
.destacado {
    background-color: #f0f0f0;
}
```

La misma clase puede utilizarse en varios elementos.

---

# 3. Selector de ID

Un ID identifica un elemento concreto del documento.

En HTML:

```html
<h1 id="titulo-principal">
    CSS Moderno Desde Cero
</h1>
```

En CSS utilizamos `#`:

```css
#titulo-principal {
    color: #264de4;
}
```

---

# Comparación rápida

| HTML | CSS | Tipo |
|---|---|---|
| `<p>` | `p` | Etiqueta |
| `class="destacado"` | `.destacado` | Clase |
| `id="titulo-principal"` | `#titulo-principal` | ID |

La forma más sencilla de recordarlo es:

```text
p           → etiqueta
.destacado  → clase
#titulo     → ID
```

---

# ¿Clase o ID?

Una clase puede reutilizarse:

```html
<p class="destacado">Texto 1</p>

<p class="destacado">Texto 2</p>
```

Un ID debe identificar de forma única a un elemento dentro del documento:

```html
<h1 id="titulo-principal">
    Mi página
</h1>
```

---

# Ejercicio

Crear:

- Un `<h1>`.
- Dos párrafos.
- Una clase llamada `destacado`.
- Un ID llamado `titulo-principal`.

Luego aplicar:

```css
p {
    color: #555;
}

.destacado {
    background-color: #f0f0f0;
}

#titulo-principal {
    color: #264de4;
}
```

Probar después cambiar los valores y observar qué elementos son afectados.

---

# Dato importante

Los selectores son una de las bases fundamentales de CSS.

A medida que avancemos aprenderemos selectores más potentes que permiten seleccionar elementos según su posición, atributos, estado o relación con otros elementos.

---

# Próximo capítulo

## Colores en CSS

Continuaremos trabajando sobre esta misma página y aprenderemos diferentes formas de definir colores.
