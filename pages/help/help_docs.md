---
title: ¿Cómo documentar?
keywords: help
sidebar: help_sidebar
permalink: help_docs.html
folder: help
summary: En esta sección se explica como agregar documentación de manera ágil. Se explica un poco el funcionamiento de Jekyll, en conjunto con el theme seleccionado.

author: Lucas Liaño
author-email: lliano@frba.utn.edu.ar
---

## Jekyll: Introducción a los generadores estáticos

TODO: Completar! [Referencia rápida](https://idratherbewriting.com/documentation-theme-jekyll/index.html).

## ¿Cómo agregar documentación?

### Agregando pages

Para agregar una nueva página de documentación hace falta crear un documento de markdown dentro de la carpeta _pages/_. Este documento deberá ubicarse dentro de la subcarpeta adecuada para mantener el orden.

Supongamos que queremos agregar una nueva página dentro de la sección _Proyecto de Investigación_, en el menú principal. Para ello agregaremos un documento con el título 'pid_test.md' dentro de _pages/pid/_. El documento deberá contener el siguiente header obligatoriamente:

```markdown
---
title: Título de la página
keywords: alguna_keyword
sidebar: home_sidebar
permalink: pid_test.html
folder: pid
summary: Resúmen del contenido de la página.

author: Nombre Apellido
author-email: napellido@frba.utn.edu.ar
---
```

Al finalizar con esta descripción se deberá escribir el contenido del documento utilizado la sintaxis de markdown. En el [ejemplo](/general-docs/help_empty_example.html) se pueden ver algunos recursos para utilizar en la documentación. El autor es libre de utilizar cualquier recurso de los descriptos en la [documentación oficial](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_adding_tooltips.html) del theme de Jekyll.

### Editando sidebar

Para poder acceder a la página que hemos creado, es necesario agregar una referencia a la misma en el sidebar correspondiente. Otra alternativa es editar el topnav.

Para editar el sidebar debemos editar el archivo correspondiente. Por ejemplo, si queremos agregar una referencia a este documento en el sidebar principal, debemos editar el archivo _'_data/sidebars/home_sidebar.yml'_:


<pre>
entries:
- title: Sidebar
  product: Contenidos
  levels: one
  folders:
  
  - title: Proyecto de Investigación
    output: web
    folderitems:
    - title: Introducción
      url: /index.html
      output: web
    - title: ¿Quiénes somos?
      url: /pid_quienes_somos.html
      output: web
<span class="red">    - title: Página de prueba</span>
<span class="red">        url: /pid_test.html</span>
<span class="red">        output: web</span>

  - title: Ejemplos
    output: web
    folderitems:
    - title: Product 1
      url: /p1_landing_page.html
      output: web
    - title: Product 2
      url: /p2_landing_page.html
      output: web

  - title: Help
    output: web
    folderitems:
      - title: Help
        url: /help_docs.html
        output: web
</pre>


Si ahora regresamos al menú principal, podremos ver la nueva página creada en el sidebar.