# CSS Moderno desde cero — 012: Z-index

**Fecha:** 09/10/2026  
**Tipo:** Código  
**Progreso:** 12/40  
**Autor:** Jonatan Jubert — Learning CSS

En el capítulo anterior vimos `position`.
Ahora vamos a controlar el orden de los elementos superpuestos.

## ¿Qué aprenderemos?

- Para qué sirve `z-index`.
- Cómo modificar el orden de dos cajas.
- Por qué importa el contexto de apilamiento.

## 1. El orden de las capas

`z-index` controla el nivel de apilamiento.

Entre elementos comparables dentro del mismo contexto,
un valor mayor queda delante de un valor menor.

```css
.caja {
  position: absolute;
}

.caja-a {
  background: #3498db;
  z-index: 1;
}

.caja-b {
  background: #7c3aed;
  z-index: 2;
}
```

En este ejemplo, B queda delante de A.

## 2. Cambiar el resultado

Modificamos el valor de A:

```css
.caja-a {
  z-index: 3;
}
```

Ahora A queda delante de B, que conserva `z-index: 2`.

| Ejemplo | Caja A | Caja B | Delante |
| --- | --- | --- | --- |
| Inicial | 1 | 2 | B |
| Modificado | 3 | 2 | A |

## 3. Detalles importantes

- Acepta números enteros: positivos, cero y negativos.
- Su valor inicial es `auto`.
- Se aplica a elementos posicionados y también a ítems flex o grid.
- No modifica el tamaño ni la posición de las cajas.

## 4. Contexto de apilamiento

Un contexto de apilamiento agrupa elementos cuyo orden
se resuelve como una unidad frente a otros contextos.

Por eso, un hijo con `z-index: 9999` no puede escapar
del contexto de su padre.

En nuestro ejemplo, cada escenario utiliza:

```css
.escenario {
  position: relative;
  z-index: 0;
}
```

Así, cada comparación tiene un contexto local.
Sus dos cajas se comparan dentro de ese contexto.

## 5. Probalo vos

1. Guardá `index.html` y `style.css` en la misma carpeta.
2. Abrí `index.html` en el navegador.
3. Compará los dos ejemplos.
4. Cambiá el `z-index` de `.caja-b` a `4`.
5. Observá qué caja queda delante en cada escenario.

## Idea para recordar

El valor importa, pero también el contexto donde se compara.

## Documentación

- [MDN: z-index](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/z-index)
- [MDN: contexto de apilamiento](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Positioned_layout/Stacking_context)

Repositorio:
https://github.com/Jonajubert/CSS-Moderno-Desde-Cero

**Jonatan Jubert — Learning CSS**  
Pequeños pasos, grandes resultados.
