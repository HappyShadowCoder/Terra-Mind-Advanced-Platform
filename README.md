# Terra Mind Advanced Platform (TMAP)

Terra Mind Advanced Platform (TMAP) is a lightweight, cloud-native GIS platform for visualizing, exploring, and analyzing geospatial data in the web browser and as a desktop application.

---

## Prerequisites

Before getting started, make sure you have the following installed:

- **Node.js**: version `22` or newer ([nodejs.org](https://nodejs.org/))
- **npm**: version `10` or newer (comes with Node.js)
- **Rust toolchain** *(optional)*: required only if you want to run or build the desktop app ([rustup.rs](https://rustup.rs/))
- **Python 3.10+** *(optional)*: required only if you want to build the local JupyterLite notebook panel or run the backend conversion sidecar

---

## Setup & Installation

1. **Install dependencies:**
   ```bash
   npm install
   ```

> [!TIP]
> If you encounter corrupted package warnings or download failures during `npm install`, clean your npm cache and retry:
> ```bash
> npm cache clean --force
> npm install
> ```

---

## Running the Project

### 1. Web Application (Browser)

To start the local web development server with hot-module reloading:

```bash
npm run dev
```

Once started, open your browser at:
**[http://localhost:5173](http://localhost:5173)**

---

### 2. Desktop Application (Tauri)

To run the native desktop application (requires Rust):

```bash
npm run tauri:dev
```

---

## Building the Project

### Build for Web
```bash
npm run build
```

Preview the production build locally:
```bash
npm run preview -w geolibre-desktop
```

### Build for Desktop (Installer / Binary)
```bash
npm run tauri:build
```

---

## Optional: JupyterLite Support

TMAP can embed a local JupyterLite notebook panel. If you need this feature enabled locally:

1. Install Python dependencies:
   ```bash
   pip install -r apps/geolibre-desktop/jupyterlite/requirements.txt
   ```
2. Build JupyterLite assets:
   ```bash
   npm run build:jupyterlite
   ```
