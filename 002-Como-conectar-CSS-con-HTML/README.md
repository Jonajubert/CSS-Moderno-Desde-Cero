# CSS Moderno Desde Cero

# 📖 Capítulo 002

## Cómo conectar CSS con HTML

En el capítulo anterior aprendimos qué es CSS.

Ahora veremos cómo hacer que un documento HTML pueda utilizar los estilos escritos en un archivo CSS.

---

# 🎯 ¿Qué aprenderás?

- CSS Externo
- CSS Interno
- CSS en línea
- Cuándo utilizar cada uno
- Cuál es la opción recomendada

---

# Existen tres formas de conectar CSS

## 1️⃣ CSS Externo ✅ (Recomendado)

Se crea un archivo independiente llamado, por ejemplo:

```
styles.css
```

Luego se conecta desde el `<head>`.

```html
<link rel="stylesheet" href="styles.css">
```

### Ventajas

- Código organizado.
- Fácil mantenimiento.
- Reutilizable.
- Más profesional.

---

## 2️⃣ CSS Interno

Los estilos se escriben dentro de:

```html
<style>

</style>
```

ubicado en el `<head>`.

Es útil para páginas pequeñas o pruebas rápidas.

---

## 3️⃣ CSS en línea

Se utiliza el atributo:

```html
style=""
```

Ejemplo:

```html
<button style="color:red;">
```

No es recomendable utilizarlo de forma habitual.

---

# ¿Cuál debería utilizar?

En proyectos reales prácticamente siempre se utiliza:

✅ CSS Externo

porque mantiene separado el contenido (HTML) del diseño (CSS).

---

# Estructura del proyecto

```
002-Como-conectar-CSS-con-HTML

│

├── index.html

└── styles.css
```

---

# Ejercicio

Crear una página que tenga:

- un título
- un párrafo
- un botón

Aplicar:

- CSS externo al párrafo.
- CSS interno al título.
- CSS en línea al botón.

---

# ¿Sabías que?

Separar HTML y CSS facilita el mantenimiento del proyecto y permite reutilizar los mismos estilos en múltiples páginas.

Es una de las buenas prácticas más importantes del desarrollo web.

---

# 🚀 Próximo capítulo

**Capítulo 003**

Selectores CSS.
