# Around The U.S.

## Descripción

Around The U.S. es un proyecto web interactivo que simula una red social de fotografías de lugares. Permite a los usuarios editar su perfil, agregar nuevas tarjetas con imágenes de sitios, darles "me gusta", eliminarlas y ver una versión ampliada de cada fotografía en una ventana emergente.

El proyecto está construido con HTML y CSS semántico siguiendo la metodología **BEM**, y toda la interactividad (apertura/cierre de ventanas emergentes, renderizado dinámico de tarjetas y manejo de eventos) está implementada con **JavaScript puro (Vanilla JS)**, sin frameworks ni librerías externas.

## Funcionalidad

- **Editar perfil:** el usuario puede abrir una ventana emergente para actualizar su nombre y descripción. Los campos del formulario se rellenan automáticamente con la información actual antes de mostrarse.
- **Agregar tarjetas:** el usuario puede abrir una ventana emergente para crear una nueva tarjeta indicando un título y un enlace a una imagen. La nueva tarjeta se agrega como primer elemento del listado.
- **Renderizado dinámico de tarjetas:** las tarjetas se generan a partir de un elemento `<template>` de HTML y un array de datos, en lugar de estar codificadas manualmente en el markup.
- **Manejo de datos incompletos:** si a una tarjeta le falta el nombre o el enlace de la imagen, se muestran valores predeterminados ("Sin título" y una imagen de marcador de posición).
- **Me gusta:** cada tarjeta cuenta con un botón que alterna su apariencia (color del ícono de corazón) al hacer clic.
- **Eliminar tarjetas:** cada tarjeta puede eliminarse del DOM individualmente mediante su botón de papelera.
- **Vista ampliada de imagen:** al hacer clic en la imagen de una tarjeta, se abre una ventana emergente que muestra la fotografía en tamaño completo junto con su título.

## Tecnologías y herramientas utilizadas

- **HTML5** — estructura semántica del documento.
- **CSS3** — estilos y maquetación, siguiendo la metodología BEM (Block, Element, Modifier).
- **JavaScript (ES6+)** — lógica de interactividad: manipulación del DOM, manejo de eventos, plantillas (`<template>`), parámetros predeterminados, entre otros.

## Estructura del proyecto

```
├── images/            # Recursos gráficos (logo, avatar, placeholder, íconos)
├── pages/
│   └── index.css      # Hoja de estilos principal
├── scripts/
│   └── index.js       # Lógica de la aplicación
└── index.html         # Documento principal
```

## Cómo ejecutar el proyecto

1. Clona o descarga este repositorio.
2. Abre el archivo `index.html` en tu navegador (no requiere instalación de dependencias ni servidor).

## Próximas mejoras

- Validación de formularios en tiempo real.
- Persistencia de datos mediante un backend/API.
- Confirmación antes de eliminar una tarjeta.
