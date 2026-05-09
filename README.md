# LUX Joyería — Sitio web

Atelier desde 1985. Sitio one-page con video hero, catálogo de 4 familias, sobre, reseñas.

## 🚀 URL en producción

Se actualiza con cada push a `main`.

## 📦 Estructura

```
.
├── index.html           ← HTML principal (~100 KB, era 2.62 MB en versión original)
├── assets/img/          ← imágenes y video extraídos
│   ├── 01.jpg           ← imagen producto principal
│   ├── 02.jpg           ← imagen secundaria
│   └── video-01.mp4     ← video del hero
└── README.md
```

## 🤝 Workflow de colaboración

```bash
# Primera vez
git clone https://github.com/Dingler-Dintra/lux-jewelry.git
cd lux-jewelry

# Día a día
git pull origin main          # bajar cambios del otro
# editar archivos
git add .
git commit -m "fix: ..."
git push origin main          # → auto-deploy si está conectado a Vercel
```

## 💡 Cambios respecto a la versión original

- **Tamaño HTML: 2.62 MB → 100 KB** (96% reducción)
- 18 imágenes en base64 → 2 archivos .jpg reales (con dedup)
- 1 video en base64 → archivo .mp4 real
- Estructura cacheable: el browser ya no descarga las imágenes en cada carga
