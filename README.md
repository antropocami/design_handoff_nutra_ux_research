# Handoff: Nutra UX Research Presentation

## Overview
Este paquete contiene los archivos de diseño para la presentación de UX Research de Nutra — una app mobile de seguimiento de macronutrientes para pacientes de nutricionistas. Incluye un deck de slides (9 pantallas) y un carrusel de LinkedIn (8 slides cuadrados 1:1).

## Sobre los archivos de diseño
Los archivos `.html` incluidos son **prototipos de diseño de alta fidelidad** — no código de producción para copiar directamente. La tarea es **recrear estos diseños en el entorno existente del proyecto** (React Native / Expo, que es la stack actual de Nutra) usando sus patrones y librerías establecidos.

## Fidelidad
**Alta fidelidad (hifi)**: Los prototipos son pixel-perfect con colores finales, tipografía, espaciado e interacciones definidas. El desarrollador debe recrear la UI con fidelidad usando las librerías existentes del codebase.

---

## Archivos incluidos

| Archivo | Descripción |
|---|---|
| `Nutra UX Research.html` | Deck principal de 9 slides (1920×1080px) |
| `Nutra LinkedIn Carousel.html` | Carrusel interactivo de 8 slides (540×540px) |
| `Nutra LinkedIn Carousel-print.html` | Versión para exportar como PDF (210×210mm por slide) |
| `deck-stage.js` | Web component que maneja el scaling, navegación y speaker notes del deck |

---

## Design Tokens

### Colores
```
--green:       #4CAF78   (primario, CTAs, progreso)
--green-dark:  #388E5A   (hover states, texto sobre verde)
--green-light: #ADD899   (streak card background)
--green-bg:    #F0F4F0   (background general de la app)
--pink:        #DA7297   (números de racha, acentos secundarios)
--amber:       #F59E0B   (warning, progreso parcial, hidratos)
--purple:      #8B5CF6   (proteínas)
--dark:        #1A2E1A   (texto primario, fondos oscuros)
--mid:         #6B7280   (texto secundario)
--light:       #E5E7EB   (bordes, dots vacíos)
--white:       #FFFFFF   (cards)

Nutrientes:
  proteinas: #8B5CF6
  hidratos:  #F59E0B
  frutas:    #EC4899
  grasas:    #10B981
  verduras:  #22C55E
  agua:      #38BDF8
```

### Tipografía
```
Font family: Plus Jakarta Sans (Google Fonts)
Weights: 300, 400, 500, 600, 700, 800

Escala (deck 1920px):
  h1: 88px / weight 800 / tracking -2px
  h2: 64px / weight 800 / tracking -1.5px
  h3: 44px / weight 700 / tracking -0.5px
  h4: 32px / weight 700
  body: 22px / weight 400 / line-height 1.6
  body-sm: 18px / weight 400 / line-height 1.6
  label: 13px / weight 700 / tracking 2.5px / uppercase
```

### Espaciado
```
Padding slides:    72px horizontal, 48px top
Gap entre secciones: 24–48px
Border radius cards: 20–24px
Border radius pills: 999px
```

### Sombras
```
Cards:    0 4px 24px rgba(0,0,0,0.07)
Teléfono: 0 48px 120px rgba(0,0,0,0.45)
Botones:  0 2px 12px rgba(0,0,0,0.06)
```

---

## Slides del deck (9 slides, 1920×1080px)

### 01 · Cover
- **Fondo**: `#F0F4F0`
- **Barra izquierda**: 8px ancho, `#4CAF78`
- **Izquierda**: Logo Nutra + título "Nutra: UX Research & Discovery" (h1) + subtítulo + autor
- **Derecha**: Mockup de teléfono (300×620px) con la app Nutra renderizada
- **Mockup teléfono**: Frame `#0e1e0e`, dynamic island, screen con MealCards, StreakCard y tab bar
- **Footer**: Metadata (Rol · Duración · Métodos · Plataforma)

### 02 · Overview del Proyecto
- **Layout**: Grid 2 columnas (1fr 1fr), gap 48px
- **Izquierda**: Contexto narrativo + 3 items con iconos (Objetivo, Rol, Timeline)
- **Derecha**: Grid 2×2 de stat cards (8 entrevistas, 47 encuestas, 4 apps, 3 rondas) + card resultado clave dark

### 03 · Problema & Oportunidad
- **Fondo**: `#1A2E1A` (dark)
- **Layout**: Grid 5fr / 4fr
- **Izquierda**: Titular + 3 pain points con íconos
- **Derecha**: Card verde con oportunidad + 2 stat cards (68%, 91%)

### 04 · Metodología
- **Fondo**: `#F0F4F0`
- **Timeline**: 4 fases con círculos de colores (verde, rosa, amber, purple) conectados por gradiente
- **Footer**: Pills de métodos usados

### 05 · Entrevistas a Usuarios
- **Layout**: Grid 2fr / 3fr
- **Izquierda**: Perfil de participantes con barras de género + cards de datos
- **Derecha**: 3 citas de usuarios con borde izquierdo de color + pill de categoría

### 06 · Benchmark Competitivo
- **Tabla**: MyFitnessPal, Cronometer, Lifesum, FatSecret vs Nutra
- **Columnas**: Porciones equiv. · Vinculación nutricionista · Sin calorías · Sistema racha · Notif. inteligentes · UX simplificada
- **Nutra row**: Fondo `linear-gradient(90deg, #DCFCE7, #F0FFF7)`, todos ✅

### 07 · Insights Clave
- **Fondo**: `#1A2E1A`
- **Grid**: 2×2 de insight cards
- **Cada card**: Ícono + número + título + descripción + chip de solución al fondo
- Colores: verde (01), rosa (02), amber (03), purple (04)

### 08 · De Insights a Soluciones
- **Grid**: 3 columnas iguales
- **Cada columna**: Ícono · Label · Título · Descripción · Barra de validación · Lista de features

### 09 · Próximos Pasos
- **Layout**: Grid 5fr / 4fr
- **Izquierda**: 3 items de roadmap con pill de prioridad
- **Derecha**: Card dark de cierre + card verde con métricas finales (82%, 4.8★)

---

## Carrusel LinkedIn (8 slides, 540×540px)

Mismos contenidos que el deck pero adaptados a formato cuadrado 1:1. Cada slide es autónomo visualmente — diseñado para ser capturado como imagen individual y subido a LinkedIn como carrusel nativo (o PDF).

**Navegación**: flechas ← → y dots. Persiste posición en `localStorage`.

**Para exportar como PDF**: usar `Nutra LinkedIn Carousel-print.html` → `Cmd+P` → Guardar como PDF, tamaño 210×210mm, sin márgenes.

---

## Mockup de teléfono (slide Cover)

El mockup replica la pantalla principal de Nutra con:
- **Dynamic Island** (90×26px, `#0e1e0e`)
- **Status bar**: hora 9:41, íconos de señal/wifi/batería en SVG
- **DayHeader**: nombre del paciente + anillo de progreso circular (SVG, 75% completado)
- **MealCards** (3): Desayuno completo (borde verde), Almuerzo parcial (borde amber), Cena sin empezar (borde gris)
  - Cada card: border-left de color, barra de progreso, dots de nutrientes por categoría
- **StreakCard**: fondo `#ADD899`, número en `#DA7297`, últimos 5 días como cuadrados
- **Tab bar**: 4 tabs (Inicio activo en verde, Historial, Guía, Perfil) con íconos SVG

---

## Stack del proyecto (Nutra)
- **Framework**: React Native + Expo
- **Estilos**: NativeWind (Tailwind para RN)
- **Estado**: Zustand (`useNutritionStore`)
- **Backend**: Firebase (Firestore + Storage)
- **Navegación**: Expo Router (file-based routing)
- **Notificaciones**: Expo Notifications

## Estructura de rutas
```
app/
  (tabs)/
    index.tsx        → Pantalla principal (hoy)
    historial.tsx    → Historial de registros
    equivalencias.tsx → Guía de alimentos
    perfil.tsx       → Perfil y configuración
  meal/[mealId].tsx  → Detalle de comida
  login.tsx
  onboarding.tsx
  recetas.tsx
src/
  components/home/   → DayHeader, MealCard, StreakCard, WaterTracker, ExerciseTracker
  store/             → useNutritionStore (Zustand)
  theme/colors.ts    → Tokens de color
```

---

## Notas para el desarrollador

1. La fuente **Plus Jakarta Sans** no está en el proyecto actualmente — se puede agregar con `expo-font` o `@expo-google-fonts/plus-jakarta-sans`
2. Los colores ya están definidos en `src/theme/colors.ts` — usarlos directamente
3. El sistema de porciones usa equivalencias (no calorías) — cada nutriente tiene N checkboxes que el usuario toca
4. El código de acceso de 6 caracteres conecta al paciente con el plan de su nutricionista via Firestore
