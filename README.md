# Around The U.S.

## Descripción

Around The U.S. es un proyecto web interactivo que simula una red social de fotografías de lugares. Permite a los usuarios editar su perfil, agregar nuevas tarjetas con imágenes de sitios, darles "me gusta", eliminarlas y ver una versión ampliada de cada fotografía en una ventana emergente.

El proyecto está construido con HTML y CSS semántico siguiendo la metodología **BEM**, y toda la interactividad (validación en tiempo real, apertura/cierre de ventanas emergentes, renderizado dinámico de tarjetas y manejo de eventos) está implementada con **JavaScript modular (ES6+)**, sin frameworks ni librerías externas.

## Funcionalidad

- **Editar perfil:** El usuario puede abrir una ventana emergente para actualizar su nombre y descripción. Los campos del formulario se rellenan automáticamente con la información actual antes de mostrarse.
- **Agregar tarjetas:** El usuario puede abrir una ventana emergente para crear una nueva tarjeta indicando un título y un enlace a una imagen. La nueva tarjeta se agrega al inicio del listado.
- **Validación en tiempo real:** Todos los formularios cuentan con validación dinámica utilizando la API nativa de HTML5 (`ValidityState`). Se muestran mensajes de error personalizados debajo de cada campo y el botón de envío se inhabilita automáticamente si la información no es válida.
- **Cierre mejorado de modales:** Las ventanas emergentes pueden cerrarse de múltiples formas: mediante el botón de cierre (`X`), haciendo clic en el fondo oscuro (overlay) o presionando la tecla `Escape`. Los escuchadores de eventos del teclado se gestionan de forma eficiente, agregándose solo cuando un modal está abierto.
- **Renderizado dinámico de tarjetas:** Las tarjetas se generan a partir de una plantilla HTML (`<template>`) y un array de datos, en lugar de estar codificadas manualmente en el markup.
- **Manejo de datos incompletos:** Si a una tarjeta le falta el nombre o el enlace de la imagen, se asignan valores predeterminados ("Sin título" y una imagen de marcador de posición).
- **Me gusta:** Cada tarjeta cuenta con un botón que alterna su apariencia (color del ícono de corazón) al hacer clic.
- **Eliminar tarjetas:** Cada tarjeta puede eliminarse del DOM individualmente mediante su botón de papelera.
- **Vista ampliada de imagen:** Al hacer clic en la imagen de una tarjeta, se abre una ventana emergente que muestra la fotografía en tamaño completo junto con su título.

## Tecnologías y herramientas utilizadas

- **HTML5** — Estructura semántica del documento, atributos de validación (`required`, `minlength`, `maxlength`, `type="url"`) y etiquetas `<template>`.
- **CSS3** — Estilos y maquetación responsiva siguiendo la metodología BEM (Block, Element, Modifier).
- **JavaScript (ES6 Modules)** — Lógica modularizada importando/exportando funciones entre scripts (`import` / `export`). Manipulación del DOM, controladores de eventos (`keydown`, `click`, `input`, `submit`), clonación de plantillas y gestión de estado de validación.

## Estructura del proyecto

├── blocks/ # Archivos CSS organizados bajo la metodología BEM
├── images/ # Recursos gráficos (logo, avatar, placeholder, íconos)
├── pages/
│ └── index.css # Hoja de estilos principal que importa los bloques
├── scripts/
│ ├── index.js # Lógica principal de la aplicación y manejo de modales/tarjetas
│ └── validate.js # Módulo para la validación universal de formularios
├── index.html # Documento principal
└── README.md # Documentación del proyecto

## Cómo ejecutar el proyecto

1. Clona o descarga este repositorio.
2. Abre el archivo `index.html` directamente en tu navegador o mediante un servidor local (como Live Server en VS Code) para un correcto funcionamiento de los módulos ES6.
