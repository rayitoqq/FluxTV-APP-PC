# FluxTV

**FluxTV** es una aplicación de escritorio para ver TV en vivo, escuchar radio y reproducir música desde YouTube, todo en un solo lugar. Construida con Electron, React y Vite.

## Características

- **TV en vivo** — Navega y reproduce canales de TV desde listas IPTV
- **Radio online** — Escucha estaciones de radio de todo el mundo
- **YouTube** — Busca y reproduce videos musicales
- **Multi-idioma** — Interfaz en español, inglés, portugués y francés
- **Temas claro/oscuro** — Cambia entre tema oscuro y claro
- **Búsqueda global** — Encuentra canales y estaciones al instante
- **Modo cine** — Maximiza el reproductor de video
- **Pantalla completa (F11)** — Experiencia inmersiva con overlay de información
- **Notificaciones de escritorio** — Recibe alertas al cambiar de canal
- **Equalizador** — Presets de audio para la radio
- **Temporizador de sueño** — Apagado automático programado
- **Atajos de teclado** — Navegación rápida sin mouse
- **Teclas multimedia** — Soporte para controles de reproducción del sistema

## Requisitos

- Windows 10/11 (64-bit)
- 2 GB RAM mínimo
- Conexión a internet

## Instalación

### Versión compilada (Windows)

Descarga el instalador o la versión portable desde la carpeta `release/`:

- `FluxTV-2.1.0-x64.exe` — Instalador (recomendado)
- `FluxTV-Portable-2.1.0.exe` — Versión portable (no requiere instalación)

### Desarrollo

```bash
# Clonar el repositorio
git clone <url-del-repo>
cd fluxtv

# Instalar dependencias
npm install

# Iniciar en modo desarrollo
npm run electron:dev

# Compilar para producción
npm run electron:build
```

## Uso

Al abrir la app, FluxTV cargará automáticamente los canales de TV y radio desde la API pública de IPTV. Usa las pestañas superiores para alternar entre TV y radio. La barra lateral permite filtrar por país o categoría.

### Atajos de teclado

| Tecla | Acción |
|---|---|
| `F11` | Pantalla completa |
| `Ctrl + F` / `Cmd + F` | Búsqueda global |
| `Ctrl + ,` | Abrir configuración |
| `Ctrl + R` | Recargar canales |
| `Esc` | Salir de pantalla completa / cerrar modal |
| `Flechas` | Navegar entre canales |
| `Enter` | Seleccionar canal |
| `Media keys` | Play/Pause, Siguiente, Anterior |

## Configuración del proyecto

```
fluxtv/
├── electron/          # Proceso principal de Electron
│   ├── main.js        # Ventana, IPC, teclas multimedia
│   └── preload.js     # Puente de comunicación seguro
├── src/               # Código fuente (React)
│   ├── components/    # Componentes de la UI
│   ├── hooks/         # Hooks personalizados
│   ├── i18n/          # Sistema de traducciones
│   ├── services/      # Servicios (IPTV, radio, YouTube)
│   └── stores/        # Estado global (Zustand)
├── index.html         # Punto de entrada HTML
├── vite.config.js     # Configuración de Vite
└── package.json       # Dependencias y scripts
```

## Stack tecnológico

- **Electron 29** — Marco de aplicación de escritorio
- **React 18** — Librería de UI
- **Vite 5** — Bundler y dev server
- **Zustand** — Manejo de estado
- **Tailwind CSS** — Estilos
- **HLS.js** — Reproducción de video HLS
- **Howler.js** — Reproducción de audio
- **@phosphor-icons/react** — Íconos

## Licencia

Copyright © 2024 FluxTV
