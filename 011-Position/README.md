# CSS Moderno desde cero — 011: Position

**Fecha:** 02/10/2026  
**Tipo:** Concepto  
**Progreso:** 11/40  
**Autor:** Jonatan Jubert — Learning CSS

En el capítulo anterior vimos `display`. Ahora exploramos cómo
`position` controla el posicionamiento de los elementos.

## ¿Qué aprenderemos?

- Cómo influye `position` en el flujo normal.
- Qué hacen sus cinco valores.
- Cómo combinar un contenedor `relative` con un elemento `absolute`.

## 1. Los cinco valores

El flujo normal es la distribución de los elementos según las
reglas de disposición de la página.

| Valor | Comportamiento |
| --- | --- |
| `static` | Valor inicial. Sigue la disposición normal; los desplazamientos no se aplican. |
| `relative` | Se desplaza desde su posición original y conserva su espacio. |
| `absolute` | Sale del flujo normal y se ubica respecto de su bloque de referencia. |
| `fixed` | Sale del flujo y normalmente queda fijo respecto del viewport. |
| `sticky` | Conserva su espacio y se adhiere durante el scroll, limitado por su contenedor. |

El viewport es el área visible del navegador.

## 2. Una tarjeta con etiqueta

### HTML

```html
<article class="tarjeta">
  <span class="etiqueta">NUEVO</span>
  <h3>Tarjeta de ejemplo</h3>
  <p>La etiqueta se ubica respecto de la tarjeta.</p>
</article>
```

### CSS

```css
.tarjeta {
  position: relative;
  padding: 60px 20px 20px;
}

.etiqueta {
  position: absolute;
  top: 12px;
  right: 12px;
}
```

La tarjeta establece la referencia para su etiqueta.

`top` y `right` separan la etiqueta de los bordes de esa referencia.
El padding deja lugar para evitar que la etiqueta cubra el texto.

`relative` puede establecer esa referencia sin desplazar la tarjeta.

## 3. Detalles que conviene recordar

- `relative` conserva el espacio original, aunque el elemento se desplace.
- `absolute` y `fixed` no reservan espacio en el flujo normal.
- La referencia de `absolute` suele ser el ancestro más cercano
  cuyo `position` no sea `static`. Propiedades como `transform`
  también pueden establecer una referencia.
- Un ancestro con propiedades como `transform` puede cambiar
  la referencia de un elemento `fixed`.
- Para que `sticky` se adhiera en un eje, necesita un límite
  distinto de `auto`, por ejemplo `top: 0`, y espacio para desplazarse.

## 4. Probalo vos

1. Guardá `index.html` y `style.css` en la misma carpeta.
2. Abrí `index.html` en el navegador.
3. Compará las cajas `static` y `relative`.
4. En `.etiqueta`, reemplazá `right: 12px` por `left: 12px`.
5. Quitá temporalmente `position: relative` de `.tarjeta`.
6. Desplazá el panel de `sticky` y después la página completa.

Observá qué elementos conservan su espacio y cuáles salen del flujo.

## Idea para recordar

Antes de ubicar un elemento, identificá su referencia.

## Documentación

- [MDN: position](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/position)
- [W3C: CSS Positioned Layout](https://www.w3.org/TR/css-position-3/)

Repositorio:
https://github.com/Jonajubert/CSS-Moderno-Desde-Cero

**Jonatan Jubert — Learning CSS**  
Pequeños pasos, grandes resultados.
