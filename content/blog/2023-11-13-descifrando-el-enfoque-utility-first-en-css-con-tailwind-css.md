---
layout: blog
title: Descifrando el Enfoque Utility-First en CSS con Tailwind CSS
date: '2023-11-13T11:58:45-05:00'
thumbnail: >-
  /assets/images/ive-started-breaking-tailwind-classes-into-multiple-lines-v0-2gvo1zwi4ix91.webp
rating: '5'
---
El enfoque utility-first ha cambiado la forma en que trabajamos con CSS en los últimos tiempos, haciendo que Tailwind CSS sea muy popular. Pero, ¿en qué consiste y por qué debería importarnos?

Vamos a simplificarlo usando el ejemplo de un simple botón.

Aunque los botones son pequeños, pueden volverse problemáticos.

Comparémoslos con Bootstrap, donde los botones solo tienen 2 clases (por ejemplo, .btn y .btn-primary). En Tailwind, los botones parecen más complicados.

¿Por qué?

En Bootstrap, clases como .btn o .btn-primary se encargan de muchas cosas: relleno, márgenes, color, estado de hover, estado activo y más.

```html
<!-- Botón típico de Bootstrap -->
<button class="btn btn-primary">Botón</button>
```

**Capa de Abstracción**

Cuando no podemos adivinar fácilmente qué hace exactamente una clase (como .btn) solo por su nombre, decimos que impone una capa de abstracción.

Por ejemplo, podemos adivinar que la clase .btn crea un botón, pero no sabemos exactamente qué significa "primario".

En términos simples, si no podemos adivinar qué hace una clase solo por su nombre, decimos que es abstracta o que impone una capa de abstracción.

**¿Qué propone el enfoque utility-first?**

Es una forma de trabajar con CSS donde construyes tus estilos usando muchas clases pequeñas y específicas.

**CSS Tradicional**

Imagina que quieres estilizar un botón con CSS tradicional.

Primero, creas una clase .btn y le aplicas propiedades CSS:

```css
.btn { 
  padding: 0.5em 1em; 
  background-color: blue; 
  color: white;
  border-radius: 0.25em; 
}
```

Luego, usas esa clase en tu HTML:

```html
<button class="btn">Haz clic</button>
```

Y este será el resultado:

"Haz clic"

**Tailwind CSS**

Ahora, estilizar el mismo botón con Tailwind usando el enfoque utility-first se ve así:

```html
<button class="rounded-md bg-blue-500 px-4 py-2 text-white">
  Haz clic
</button>
```

La diferencia es que el botón de Tailwind tiene más clases que el de CSS tradicional.

Pero, ¿qué ganamos con esto?

* **Composición:** Puedes crear diseños complejos aplicando muchas clases utilitarias. Esto evita tener que crear clases únicas para cada variación de un componente.
* **Mapeo Directo:** El estilo de un elemento es claro al mirar el HTML. No es necesario revisar un archivo CSS separado para entender los estilos.
* **Personalización:** Puedes personalizar clases utilitarias desde tu configuración en Tailwind para adaptarse a tu proyecto.
* **Diseño Responsivo:** Tailwind proporciona clases utilitarias para manejar diseños responsivos. Puedes controlar los estilos para diferentes tamaños de pantalla usando estas clases.
* **Eficiencia:** Evitas inflar tu CSS con estilos innecesarios. Este enfoque fomenta crear estilos según sea necesario, haciendo el CSS más eficiente.
* **Consistencia:** Este enfoque fomenta la consistencia en un proyecto, ya que naturalmente crea un conjunto limitado de estilos.

Aunque puede parecer más detallado al principio, el enfoque utility-first promueve consistencia, personalización y eficiencia en tus estilos. Una vez que te acostumbras, puede hacer tu proceso de desarrollo más rápido.
