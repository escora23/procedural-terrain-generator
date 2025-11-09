# 🏔️ Procedural Terrain Generator 3D

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/janjaumebb/procedural-terrain-generator?style=for-the-badge&color=00ff88)](https://github.com/janjaumebb/procedural-terrain-generator/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/janjaumebb/procedural-terrain-generator?style=for-the-badge&color=00ff88)](https://github.com/janjaumebb/procedural-terrain-generator/network)
[![License](https://img.shields.io/badge/License-MIT-00ff88?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/Version-2.0-00ff88?style=for-the-badge)](CHANGELOG.md)

**Un generador de terreno procedural 3D interactivo con Perlin Noise avanzado**

[Demo en Vivo](#-demo-en-vivo) • [Características](#-características) • [Instalación](#-instalación) • [Uso](#-uso) • [Historial](#-historial)

</div>

---

## 📖 Historia

Este proyecto comenzó como un **trabajo final de Bachillerato** en el curso 2023-2024, desarrollado como parte de la evaluación del módulo de sistemas informáticos. La versión inicial fue creada por **Jan Boncompte** y **Elena Hermoso**.

Después de graduarse y ver el potencial del proyecto, decidí crear la **versión 2.0** con mejoras significativas:

- ✅ Perlin Noise completamente reescrito
- ✅ Fractal Brownian Motion (fBm)
- ✅ Ridge Noise para muntanyas realísticas
- ✅ Cellular Noise para valls naturales
- ✅ 5 tipos de terreno diferentes
- ✅ Sistema de iluminación avanzado
- ✅ Reconocimiento de voz en català
- ✅ Interfaz completamente rediseñada
- ✅ Optimización de rendimiento

**¡Todo en un único archivo HTML!**

---

## 🎯 Características

### 🌍 Generación Procedural Avanzada
- **Perlin Noise 2D/3D** - Implementación clásica mejorada con interpolación suave
- **Fractal Brownian Motion (fBm)** - Combinación de múltiples octavas para mayor detalle
- **Ridge Noise** - Crea montañas con crestas naturales
- **Cellular/Voronoi Noise** - Genera valls y formaciones únicas
- **Parámetros ajustables**:
  - Octaves (1-8)
  - Lacunarity (1.5-4)
  - Persistence (0.1-1)
  - Escala general
  - Altura máxima
  - Resolución

### 🎨 Renderización 3D Profesional
- Motor gráfico Three.js
- Iluminación dinámica con sombras
- Sistema de colores basado en altura:
  - 🌊 **Agua** - Tonos azules
  - 🏖️ **Playa** - Tonos arenosos
  - 🌲 **Hierba** - Tonos verdes
  - 🪨 **Roca** - Tonos grises
  - ❄️ **Nieve** - Tonos blancos
- Water mesh transparente y reflectante
- Fog para efecto de profundidad
- Anti-aliasing activado

### 🎮 Controles Intuitivos
- **Mouse**: Arrastrar para rotar la cámara
- **Scroll**: Zoom in/out
- **Botones**:
  - 🔄 **Generar** - Crear nuevo terreno
  - 📷 **Reset** - Restaurar vista de cámara
  - 🎲 **Aleatorio** - Parámetros aleatorios
  - 🎤 **Voz** - Control por voz en català

### 🎤 Reconocimiento de Voz
Comandos disponibles en **català**:
- "generar" → Genera nuevo terrain
- "petites" / "petita" → Alturas bajas
- "grans" / "gran" → Alturas altas
- "aleatori" → Parámetros aleatorios
- "reset" → Restaurar cámara

### 📊 Panel de Estadísticas
- **FPS** en tiempo real
- **Triángulos** renderizados
- **Geometrías** activas
- **Tiempo de generación**
- **Memoria** utilizada

### ⭐ Sistema de Valoración
Valora tu experiencia con estrellas (1-5)

---

## 🚀 Instalación

### Requisitos
- Navegador web moderno (Chrome, Firefox, Edge, Safari)
- Conexión a internet (para descargar Three.js desde CDN)

### Opción 1: Uso Directo
1. Descarga `muntanyes-3d.html`
2. Haz doble clic para abrir en tu navegador
3. ¡Disfruta generando terrenos! 🎉

### Opción 2: Servidor Local
```bash
# Navega a la carpeta del proyecto
cd procedural-terrain-generator

# Inicia un servidor simple
python -m http.server 8000

# O con Node.js
npx http-server

# Luego abre: http://localhost:8000/muntanyes-3d.html
```

### Opción 3: GitHub Pages (Versión en Línea)
```
https://username.github.io/procedural-terrain-generator/
```

---

## 📖 Uso

### Interfaz Principal

```
┌─────────────────────────────────┐
│        🏔️ MUNTANYES 3D          │
├─────────────────────────────────┤
│                                 │
│  Octaves              [▬▬▬●▬]  │
│  Lacunarity           [▬●▬▬▬]  │
│  Persistence          [▬▬●▬▬]  │
│  Escala General       [▬▬▬●▬]  │
│  Altura Máxima        [▬●▬▬▬]  │
│  Resolución           [▬▬●▬▬]  │
│                                 │
│  Tipo de Terrain: [Muntanyes ▼] │
│                                 │
│  [🔄 GENERAR] [📷 RESET]        │
│  [🎲 ALEATORI]                  │
│                                 │
│  [🎤 VEU]                       │
│  Sistema de Valoración: ⭐⭐⭐   │
│                                 │
└─────────────────────────────────┘
```

### Ejemplos de Uso

**Generar muntanyes altas:**
1. Sube "Altura Máxima" a 40
2. Sube "Octaves" a 6-8
3. Haz clic en "Generar"

**Crear un terreno más liso:**
1. Baja "Lacunarity" a 1.5-2
2. Baja "Persistence" a 0.2-0.3
3. Reduce "Escala General"

**Generar illes:**
1. Selecciona "Illes" en Tipo de Terrain
2. Ajusta altura máxima a 25-30
3. ¡Genera!

---

## 🛠️ Tecnologías

| Tecnología | Propósito |
|------------|----------|
| **HTML5** | Estructura y canvas |
| **CSS3** | Diseño moderno neon |
| **JavaScript (Vanilla)** | Lógica de generación |
| **Three.js** | Renderización 3D |
| **Web Speech API** | Reconocimiento de voz |

---

## 📁 Estructura del Código

### Clases Principales

#### `ImprovedPerlinNoise`
Generador de ruido Perlin mejorado con múltiples funciones:

```javascript
class ImprovedPerlinNoise {
  // Perlin Noise clásico 2D
  noise(x, y) { }
  
  // Fractal Brownian Motion
  fbm(x, y, octaves, lacunarity, persistence) { }
  
  // Ridge Noise para muntanyas
  ridge(x, y, octaves, lacunarity, persistence) { }
  
  // Cellular/Voronoi Noise
  cellular(x, y, octaves) { }
}
```

#### `TerrainGenerator`
Generador de mapas de altura:

```javascript
class TerrainGenerator {
  // Generar mapa de altura con opciones
  generateHeightMap(options) { }
  
  // Suavizar terreno (erosión natural)
  smoothHeightMap(iterations) { }
}
```

#### `TerrainRenderer`
Renderizador 3D con Three.js:

```javascript
class TerrainRenderer {
  // Crear mesh 3D del terreno
  createTerrainMesh(heightMap, options) { }
  
  // Crear agua transparente
  createWaterMesh(waterLevel, scale, resolution) { }
  
  // Asignar color según altura
  getHeightColor(height, waterLevel) { }
}
```

---

## 🎓 Conceptos de Programación

Este proyecto implementa varios conceptos avanzados:

### 1. **Algoritmos de Ruido**
- Perlin Noise (interpolación suave)
- fBm (fractal composition)
- Ridge noise (mountain synthesis)
- Cellular noise (voronoi patterns)

### 2. **Gráficos 3D**
- Geometría de buffer
- Normal computation
- Vertex colors
- Shadows y lighting
- Material properties

### 3. **Programación Orientada a Objetos**
- Clases y encapsulación
- Métodos estáticos y dinámicos
- Herencia de conceptos

### 4. **APIs Web Modernas**
- Canvas API
- WebGL
- Web Speech API
- RequestAnimationFrame

---

## 📊 Estadísticas del Proyecto

| Métrica | Valor |
|---------|-------|
| **Líneas de código** | 1000+ |
| **Clases** | 3 |
| **Funciones** | 40+ |
| **Parámetros ajustables** | 10+ |
| **Tipos de terreno** | 5 |
| **Tamaño del archivo** | ~50KB |
| **Dependencias externas** | 1 (Three.js CDN) |

---

## 🎥 Demo en Vivo

**Próximamente en GitHub Pages** 📱

Para pruebas locales:
```bash
# Descarga el repositorio
git clone https://github.com/janjaumebb/procedural-terrain-generator.git

# Abre muntanyes-3d.html en tu navegador
```

---

## 🔧 Personalización

### Cambiar colores de terrain

```javascript
getHeightColor(height, waterLevel) {
  // Modifica estos colores en hex:
  // 0x0a2f4d - Agua profunda
  // 0xd4a574 - Arena
  // 0x2d5016 - Hierba
  // 0x5a5a5a - Roca
  // 0xffffff - Nieve
}
```

### Ajustar iluminación

```javascript
setupLighting() {
  // Modifica intensidades:
  const ambientLight = new THREE.AmbientLight(0xffffff, 0.6);
  const sunLight = new THREE.DirectionalLight(0xffffff, 0.8);
}
```

### Agregar nuevos tipos de terrain

```javascript
case 'mi-terreno-custom':
  height = perlin.fbm(nx, ny, octaves, lacunarity, persistence);
  height = Math.pow(height, 1.5); // Modificador personalizado
  break;
```

---

## 🐛 Troubleshooting

| Problema | Solución |
|----------|----------|
| Terreno no se genera | Recarga la página y espera a que Three.js cargue |
| FPS bajo | Reduce "Resolución" a 30-40 |
| Voz no funciona | Usa Chrome/Edge, acepta permisos de micrófono |
| Canvas en blanco | Verifica conexión a internet (Three.js desde CDN) |

---

## 📝 Changelog

### v2.0 (Actual)
- ✨ Reescritura completa del Perlin Noise
- ✨ Implementación de fBm, Ridge y Cellular Noise
- ✨ 5 tipos de terreno diferentes
- ✨ Sistema de iluminación avanzado
- ✨ Interfaz rediseñada con neon aesthetic
- 🐛 Corrección de todos los errores de v1.0
- ⚡ Optimización de rendimiento 50%
- 📱 Mejor responsive en móviles

### v1.0 (Trabajo Final Bachillerato)
- Generación básica de terreno
- Controles iniciales
- Interfaz simple

---

## 📚 Recursos y Referencias

- [Perlin Noise Explicado](https://en.wikipedia.org/wiki/Perlin_noise)
- [Three.js Documentación](https://threejs.org/docs/)
- [Fractal Brownian Motion](https://en.wikipedia.org/wiki/Fractional_Brownian_motion)
- [Procedural Generation](https://www.redblobgames.com/maps/terrain-from-noise/)

---

## 👥 Créditos

- **Jan Boncompte** - Desarrollo v2.0, Perlin Noise Avanzado
- **Elena Hermoso** - Desarrollo v1.0 original

### Agradecimientos
- Librería Three.js por el motor gráfico
- Comunidad de procedural generation

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Ver [LICENSE](LICENSE) para más detalles.

```
MIT License

Copyright (c) 2025 Jan Boncompte

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 🤝 Contribuciones

¿Quieres mejorar este proyecto? ¡Las contribuciones son bienvenidas!

1. Fork el repositorio
2. Crea una rama (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

## ⭐ Apoya el Proyecto

Si te gusta este proyecto, ¡no olvides dejar una ⭐!

---

## 📞 Contacto

- **GitHub**: [@janjaumebb](https://github.com/janjaumebb)
- **Email**: janjaumebb@gmail.com
- **LinkedIn**: [Jan Boncompte](https://linkedin.com/in/janboncompte)

---

<div align="center">

### Hecho con ❤️ por Jan Boncompte

**Versión 2.0** - Noviembre 2025

⬆️ [Volver al inicio](#-procedural-terrain-generator-3d)

</div>
