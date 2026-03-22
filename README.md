# 🎬 MovieSerna

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Flexbox](https://img.shields.io/badge/Flexbox-1a1a2e?style=for-the-badge&logo=css3&logoColor=white)
![Responsive](https://img.shields.io/badge/Responsive-Mobile_First-e63946?style=for-the-badge)

</div>

---

## Datod del Alumno
| Campo | Dato |
|---|---|
| **Nombre** | Serna Segura Noel Alberto |
| **Matrícula** | 22210354 |
| **Materia** | Programación Web |
| **Tecnologías** | HTML y CSS |
| **Año** | 2024 |

---

## 📄 Descripción

**MovieSerna** es un sitio web estático que muestra el detalle de una película y el perfil de un actor. Desarrollado con **HTML5 y CSS3 puro**, sin frameworks ni librerías externas.

El proyecto consta de **dos páginas**:

- `Pelicula.html` → Detalle de la película *Spider-Man (2002)*
- `Actor.html` → Perfil del actor *Tobey Maguire*
- `Styles.css` → Hoja de estilos compartida para ambas páginas

---

##    Estructura 

```
movieserna/
├── Pelicula.html     ← Página de detalle de película
├── Actor.html        ← Página de detalle de actor
├── Styles.css        ← Estilos compartidos (Flexbox + Media Queries)
└── README.md         ← Este archivo
```

---

##  Tecnologías Usadas

| Tecnología | Para qué se usó |
|---|---|
| **HTML5** | Estructura semántica: `<nav>`, `<main>`, `<section>`, `<footer>` |
| **CSS3** | Estilos, colores, bordes redondeados, transiciones hover |
| **Flexbox** | Layout de dos columnas (imagen + texto) y alineación de chips |
| **CSS Variables** | Paleta de colores centralizada con `:root` |
| **Media Queries** | Diseño responsivo Mobile First (`max-width: 700px`) |
| **Google Fonts** | Tipografía `Poppins` importada desde fonts.googleapis.com |
| **TMDB CDN** | Imágenes del póster y foto del actor vía URL pública |

---

##  Flexbox — Conceptos Aplicados

Se usó `display: flex` en **6 lugares distintos** del proyecto:

### 1. Navbar — logo y links en fila
```css
.navbar {
    display: flex;
    justify-content: space-between; /* logo izquierda, links derecha */
    align-items: center;            /* centrado vertical */
}
```

### 2. Layout principal — póster | información
```css
.pelicula-card {
    display: flex;
    flex-direction: row;      /* lado a lado en escritorio */
    align-items: flex-start;
    gap: 32px;
}
```

### 3. Chips de metadatos y géneros
```css
.metadatos, .generos {
    display: flex;
    flex-wrap: wrap;   /* bajan de línea si no caben */
    gap: 8px;
}
```

### 4. Tarjetas del actor — dos columnas
```css
.tarjetas-grid {
    display: flex;
    flex-direction: row;
    gap: 20px;
}
```

### 5. Lista de datos personales — clave | valor
```css
.lista-datos li {
    display: flex;
    gap: 12px;
    align-items: baseline;
}
```

### 6. Items de filmografía — año | título | flecha
```css
.pelicula-item {
    display: flex;
    align-items: center;
    gap: 14px;
}
```

---

##  Diseño Responsivo — Mobile First

El diseño base es para **celular** (una sola columna). Con una sola Media Query se adapta a escritorio:

```css
/* BASE — móvil: todo en columna */
.pelicula-card  { flex-direction: column; }
.tarjetas-grid  { flex-direction: column; }

/* ESCRITORIO — a partir de 700px: dos columnas */
@media (min-width: 700px) {
    .pelicula-card  { flex-direction: row; }
    .tarjetas-grid  { flex-direction: row; }
}
```

| Pantalla | Comportamiento |
|---|---|
|  Móvil `< 700px` | Imagen arriba, texto abajo. Todo en columna. |
|  Escritorio `≥ 700px` | Imagen a la izquierda, información a la derecha. |

---

##  Paleta de Colores

```css
:root {
    --color-primario:    #1a1a2e;   /* azul marino — navbar y títulos   */
    --color-acento:      #e63946;   /* rojo         — botones y tags     */
    --color-fondo:       #f4f6f9;   /* gris azulado — fondo del body     */
    --color-card:        #ffffff;   /* blanco       — fondo de tarjetas  */
    --color-borde:       #e0e4eb;   /* gris clarito — bordes             */
    --color-texto-suave: #6b7280;   /* gris medio   — texto secundario   */
}
```

---

##  Cómo Ejecutar

**Opción 1 — Directo en el navegador:**
1. Descarga o clona este repositorio
2. Abre `Pelicula.html` o `Actor.html` con doble clic
3. No requiere instalación ni servidor

**Opción 2 — Con Live Server en VS Code:**
1. Abre la carpeta en VS Code
2. Instala la extensión **Live Server** de Ritwick Dey
3. Clic derecho en `Pelicula.html` → *Open with Live Server*

**Opción 3 — Clonar desde GitHub:**
```bash
git clone https://github.com/tu-usuario/movieserna.git
cd movieserna
```

---

## 📸 Páginas del Proyecto

###  Detalle de Película — `Pelicula.html`
- Póster de la película
- Título, año, duración, clasificación y puntuación
- Nombre del director
- Sinopsis completa
- Tags de géneros con efecto hover
- Chips del reparto principal
- Botones de acción

###  Detalle de Actor — `Actor.html`
- Foto circular del actor
- Nombre, profesión y datos rápidos
- Biografía
- Tarjeta de datos personales (tabla clave/valor)
- Filmografía destacada con año y personaje

---

<div align="center">

**Serna Segura Noel Alberto · 22210354 · Programación Web · 2024**

</div>
