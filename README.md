# myporfolio

Estructura de maquetación desarrollada con **HTML semántico + CSS puro (metodología BEM y Custom Properties)**.

## url

figma - https://www.figma.com/design/C6e2QHKmGlzFIQc9iF00kH/Myporfolio?node-id=0-1&t=1ypDAo0nV6HsxGbf-0
github - https://github.com/Magrey16/myporfolio

## Arquitectura

```mermaid
flowchart LR
    Diseno[Diseño Figma] --> HTML[Páginas HTML semánticas · html/]
    HTML --> GlobalCSS[CSS Global · css/global.css]
    HTML --> PageCSS[CSS Específico · css/index.css]
    HTML --> Assets[Recursos · assets/fonts y images]
    HTML --> JS[Interactividad · js/main.js]
```

GitHub renderiza este bloque `mermaid` automáticamente como un diagrama de flujo[cite: 1].

## Estructura

```text
porfolio/
├── assets/
│   ├── fonts/
│   │   ├── questrial/
│   │   └── source_code_pro/
│   └── images/
├── css/
│   ├── global.css        
│   └── index.css
├── html/
│   ├── contacto.html
│   ├── index.html
│   ├── proyecto.html
│   ├── sobremi.html
│   └── tecnologia.html
├── js/
│   └── main.js
├── LICENSE
└── README.md
```

# Variables (:root), reset y componentes globales (BEM)
# Estilos específicos de la página principal

## Cómo trabajar

1. **Previsualización:** Abre `html/index.html` con la extensión **Live Server** de VS Code para ver los cambios en tiempo real al guardar.
2. **Design Tokens:** Define y reutiliza toda la paleta de colores y tipografías (`--font-primaria`, `--font-secundaria`) desde el selector `:root` en `css/global.css`.
3. **Metodología BEM:** Nombra las clases siguiendo la convención `.bloque__elemento--modificador` (por ejemplo, `.nav`, `.nav__menu`, `.nav__link`) para mantener baja la especificidad y facilitar el mantenimiento.
4. **HTML semántico:** Estructura las vistas con etiquetas semánticas (`header`, `nav`, `main`, `section`, `footer`) y mantén los nombres de archivos y carpetas en minúsculas y sin espacios.
5. **Interactividad:** Añade la lógica dinámica de la interfaz en `js/main.js`.