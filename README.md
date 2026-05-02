<div align="center">

# 🐾 AdoptaCol

### *Porque cada peludito merece una segunda oportunidad*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

![Estado](https://img.shields.io/badge/Estado-En_Desarrollo-blue?style=flat-square)
![Responsive](https://img.shields.io/badge/Responsive-Sí-success?style=flat-square)
![Licencia](https://img.shields.io/badge/Licencia-MIT-green?style=flat-square)

<br>

> **AdoptaCol** es una plataforma web estática que conecta a personas con mascotas rescatadas en Colombia.
> Busca combatir el abandono animal promoviendo la adopción responsable a través de una experiencia
> sencilla, bonita y funcional — sin necesidad de aplicaciones ni registros obligatorios.

<br>

![Preview de AdoptaCol](https://images.unsplash.com/photo-1543466835-00a7907e9de1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80)

</div>

---

## 📋 Tabla de Contenidos

- [¿Qué es AdoptaCol?](#-qué-es-adoptacol)
- [Funcionalidades](#-funcionalidades)
- [Tecnologías usadas](#-tecnologías-usadas)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Cómo usar el proyecto](#-cómo-usar-el-proyecto)
- [Decisiones técnicas](#-decisiones-técnicas)
- [Responsive design](#-responsive-design)
- [Lo que viene después](#-lo-que-viene-después)
- [Contribuir](#-contribuir)

---

## 🐶 ¿Qué es AdoptaCol?

AdoptaCol nació como proyecto frontend para practicar HTML semántico, CSS personalizado y Bootstrap 5 en un caso de uso real y con propósito social.

La página simula una plataforma de adopción de mascotas en Colombia que le permite a cualquier persona:

- **Explorar** animales disponibles filtrando por ciudad, edad, tamaño y raza
- **Conocer** los refugios aliados y ver qué mascotas tiene disponibles cada uno
- **Encontrar** veterinarias solidarias con tarifas reducidas para adoptantes
- **Contactar** directamente al refugio llenando un formulario de solicitud de adopción

Todo esto desde un solo archivo HTML, sin frameworks de JavaScript, sin backend y sin base de datos.

---

## ✨ Funcionalidades

### 🔍 Galería con filtros en tiempo real
Las mascotas se pueden filtrar simultáneamente por **ciudad**, **edad**, **tamaño** y **tipo de raza**. Los filtros actúan sobre los atributos `data-*` de cada tarjeta sin recargar la página. Si ninguna mascota coincide, aparece un mensaje amigable.

```
Ciudad → Bogotá / Medellín / Cali
Edad   → Cachorro / Adulto
Tamaño → Pequeño / Mediano / Grande
Raza   → Mestizo (Criollo) / Raza Pura
```

### 🏠 Sección de Refugios Aliados
Cada refugio tiene su tarjeta con nombre, ciudad y descripción. El botón **"Ver mascotas disponibles"** preselecciona automáticamente la ciudad del refugio en el filtro y lleva al usuario directo a la galería con los resultados ya aplicados.

### 🏥 Directorio de Veterinarias Solidarias
Lista de clínicas con tarifas reducidas o servicio gratuito para animales rescatados. Cada veterinaria muestra sus servicios solidarios y tiene un botón de **contacto directo por WhatsApp** que abre la app sin salir de la página.

### 💌 Formulario de Adopción
Al hacer clic en **"Me interesa"** en cualquier tarjeta disponible, se abre un modal con el nombre y los datos de esa mascota ya precargados. El formulario pide nombre, correo, teléfono y un mensaje personal al refugio.

> Las mascotas *en proceso de adopción* tienen el botón deshabilitado visualmente para evitar solicitudes duplicadas.

### 🔐 Inicio de Sesión
Modal con formulario de login, opción para mostrar/ocultar la contraseña y enlace de recuperación. Preparado para conectarse a un backend real en el futuro.

### 📱 Menú responsivo (hamburguesa)
En celulares el menú de navegación se colapsa en un botón de tres rayitas que despliega los links verticalmente al hacer clic. En escritorio se ve como siempre.

### 🔔 Navegación por anclas
Los botones **Refugios** y **Veterinarias Solidarias** en el navbar hacen scroll suave hasta sus secciones usando solo `href="#id"` — sin JavaScript.

---

## 🛠 Tecnologías usadas

| Tecnología | Uso en el proyecto |
|---|---|
| **HTML5 semántico** | Estructura con `<nav>`, `<header>`, `<main>`, `<section>`, `<article>`, `<footer>` |
| **CSS3 personalizado** | Grid, Flexbox, variables de color, transiciones, animaciones y media queries |
| **Bootstrap 5.3** | Sistema de columnas responsivo, modales, toasts, navbar colapsable |
| **Bootstrap Icons 1.11** | Íconos en botones, badges, tarjetas y formularios |
| **JavaScript vanilla** | Filtros, modales dinámicos, scroll programático, toggle de contraseña |

Sin librerías externas de JS. Sin npm. Sin compiladores. Abre el `index.html` y listo.

---

## 📁 Estructura del proyecto

```
adoptacol/
│
├── index.html        # Todo el HTML: secciones, modales, scripts
├── style.css         # Estilos personalizados + media queries responsive
└── README.md         # Este archivo
```

### Secciones del `index.html`

```
1.  Barra de navegación        → navbar responsivo con menú hamburguesa
2.  Hero / Banner              → imagen de fondo con degradado y CTA
3.  Filtros de búsqueda        → 4 selects + botones Buscar y Limpiar
4.  Galería de mascotas        → grid de tarjetas con data-* para filtrar
5.  Sección de Refugios        → tarjetas con botón de filtrado directo
6.  Veterinarias Solidarias    → tarjetas con servicios y link a WhatsApp
7.  Footer                     → créditos y misión
8.  Modal: Iniciar Sesión      → formulario con toggle de contraseña
9.  Modal: Me Interesa         → formulario dinámico por mascota
10. Toast: Próximamente        → notificación para secciones en desarrollo
11. Scripts                    → toda la lógica JS comentada línea por línea
```

---

## 🚀 Cómo usar el proyecto

### Opción 1 — Abrirlo directo en el navegador

```bash
# Clona el repositorio
git clone https://github.com/tu-usuario/adoptacol.git

# Entra a la carpeta
cd adoptacol

# Abre el archivo (Windows)
start index.html

# Abre el archivo (Mac)
open index.html

# Abre el archivo (Linux)
xdg-open index.html
```

### Opción 2 — Con Live Server en VS Code

1. Instala la extensión **Live Server** de Ritwick Dey
2. Clic derecho sobre `index.html`
3. Selecciona **"Open with Live Server"**
4. El navegador se abre con recarga automática al guardar cambios

### Agregar una nueva mascota

Copia este bloque dentro del `<div class="mascotas-grid">` en el `index.html` y reemplaza los valores:

```html
<article class="mascota-card"
         data-ciudad="bogota"
         data-edad="cachorro"
         data-tamano="pequeno"
         data-raza="criollo"
         data-nombre="Nombre"
         data-detalle="Raza · Edad">

    <img src="URL_DE_LA_FOTO" alt="Descripción" class="mascota-img">

    <div class="card-content">
        <h4 class="mascota-nombre">Nombre</h4>
        <p class="mascota-detalle">Raza · Edad</p>
        <span class="status-badge bg-success">Disponible</span>

        <button class="btn-interes"
                onclick="abrirModalInteres(this)"
                data-bs-toggle="modal"
                data-bs-target="#modalInteres">
            <i class="bi bi-heart me-1"></i> Me interesa
        </button>
    </div>
</article>
```

> ⚠️ Los valores de `data-ciudad`, `data-edad`, `data-tamano` y `data-raza` deben coincidir exactamente con los `value` de los `<option>` en el formulario de filtros para que el filtrado funcione correctamente.

---

## 🧠 Decisiones técnicas

### ¿Por qué `data-*` y no clases para los filtros?
Los atributos `data-*` están diseñados exactamente para guardar información extra en elementos HTML sin afectar el estilo. Usar clases para filtrar mezclaría responsabilidades: una clase debe describir cómo se ve un elemento, no qué datos tiene.

### ¿Por qué un solo modal para todas las mascotas?
Tener un modal por cada mascota hubiera multiplicado el HTML innecesariamente. En cambio, el JS lee los `data-nombre` y `data-detalle` de la tarjeta clickeada y los inyecta en el modal antes de que Bootstrap lo muestre. Un modal, infinitas mascotas.

### ¿Por qué `scroll-behavior: smooth` en CSS y no JS?
Para el scroll entre secciones (Refugios, Veterinarias, galería) se usa una propiedad CSS nativa en lugar de `window.scrollTo()`. Es más simple, más performante y funciona sin JavaScript activo.

### ¿Por qué `navbar-expand-lg` y no solo `navbar-expand`?
`navbar-expand` mantiene el menú siempre desplegado en cualquier tamaño de pantalla. En celulares esto hace que los links se amontonen o desborden. Con `navbar-expand-lg` Bootstrap sabe que debe colapsarlo en pantallas menores a 992px y mostrar el botón hamburguesa.

### ¿Por qué `object-fit: cover` en las fotos?
Las imágenes de mascotas vienen de fuentes externas con proporciones distintas. Sin `object-fit: cover` algunas aparecerían aplastadas o estiradas. Cover recorta la foto para llenar el espacio fijo de `240px` sin deformarla, como un zoom centrado.

---

## 📱 Responsive Design

El sitio se adapta a tres tamaños de pantalla usando media queries en `style.css`:

| Pantalla | Galería | Refugios | Navbar |
|---|---|---|---|
| **Escritorio** (≥ 992px) | 4 columnas | 3 columnas | Links visibles |
| **Tableta** (576px–991px) | 2 columnas | 2 columnas | Menú hamburguesa |
| **Celular** (≤ 575px) | 1 columna | 1 columna | Menú hamburguesa |

Los filtros de búsqueda también se reorganizan:
- **Escritorio:** 4 selects en fila (`col-lg-2`)
- **Tableta:** 3 por fila (`col-md-4`)
- **Celular:** 2 por fila (`col-6`)

---

## 🔮 Lo que viene después

Estas son las funcionalidades planeadas para versiones futuras:

- [ ] Backend real con base de datos de mascotas (Node.js + MongoDB o Firebase)
- [ ] Sistema de autenticación para refugios (registrar y editar sus mascotas)
- [ ] Página de detalle por mascota con galería de fotos y historia
- [ ] Mapa interactivo de refugios y veterinarias por ciudad
- [ ] Filtro por especie (perro / gato / conejo / ave)
- [ ] Formulario para que nuevos refugios soliciten unirse a la plataforma
- [ ] Notificaciones por correo al refugio cuando alguien envía una solicitud
- [ ] Panel de administración para gestionar solicitudes de adopción

---

## 🤝 Contribuir

¿Quieres ayudar a que más peluditos encuentren hogar? Las contribuciones son bienvenidas.

```bash
# 1. Haz un fork del repositorio
# 2. Crea una rama para tu cambio
git checkout -b feature/nombre-del-cambio

# 3. Haz tus cambios y confirma
git commit -m "feat: descripción corta del cambio"

# 4. Súbela a tu fork
git push origin feature/nombre-del-cambio

# 5. Abre un Pull Request en GitHub
```

Por favor mantén los **comentarios en el código** — este proyecto está pensado también como material de aprendizaje, así que cada decisión debe quedar explicada directamente en el HTML y el CSS.

---

<div align="center">

Hecho con 🐾 y mucho amor por los animales en Colombia

*"Adoptar es la decisión más humana que puedes tomar."*

</div>
