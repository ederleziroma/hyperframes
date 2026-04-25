# Guía de Replicación: Reel Enfermedad de Pompe 🧬

Este documento detalla los lineamientos técnicos y visuales para replicar el reel con estética **"Japo-Mex Refinado"** (Notebook Japonés + Rótulo Mexicano), optimizado para áreas de seguridad de Instagram y TikTok.

## 1. Identidad Visual (Brand Kit)

### Paleta de Colores
*   **Fondo (Base):** `#FFFFFF` (Blanco puro)
*   **Contraste Principal:** `#102A43` (Azul Profundo / Casi Negro)
*   **Acento 1 (Rótulo):** `#FFD600` (Amarillo Vibrante)
*   **Acento 2 (Alerta):** `#D81B60` (Rosa Mexicano)
*   **Acento 3 (Ciencia):** `#0091EA` (Cian Vivo)

### Tipografía
*   **Fuente:** `Inter` (Sans-serif de alta legibilidad).
*   **Titulares:** 900 (Black), Todo en Mayúsculas.
*   **Cuerpo:** 500-700 (Medium/Bold).

## 2. Especificaciones Técnicas

*   **Resolución:** 1080 x 1920 (9:16).
*   **Duración Total:** 24 segundos.
*   **FPS:** 30.
*   **Tecnología:** Hyperframes (HTML5 + GSAP 3).

## 3. Zonas de Seguridad (Safe Areas)

Para evitar obstrucciones de la interfaz de la App (likes, descripción, notch):

*   **Margen Superior:** 220px (Libre de texto crítico).
*   **Margen Inferior:** 450px (Libre de texto crítico).
*   **Márgenes Laterales:** 120px.
*   **Zona de Acción:** 840px de ancho x 1250px de alto (Centro vertical).

## 4. Estructura de Contenido (Escenas)

1.  **Gancho (0-6s):** Título masivo "ENFERMEDAD DE POMPE". Definición rápida en tarjeta blanca.
2.  **Mecanismo (6-12s):** Explicación de la falta de enzima GAA y acumulación de glucógeno.
3.  **Síntomas (12-19s):** Lista numerada (01-03) con iconos representativos.
4.  **Cierre (19-24s):** CTA directo "¡Comparte!" y mensaje de diagnóstico temprano.

## 5. Reglas de Animación (GSAP)

*   **Layout First:** Posiciona todo en su estado final con CSS.
*   **Entradas:** Usa siempre `gsap.from()` con un desplazamiento de `y: 30` o `x: -30`.
*   **Escalonamiento (Stagger):** Aplica `stagger: 0.2` en listas de ítems para guiar la vista.
*   **Transiciones:** Desvanecimiento simple (`opacity: 1` a `opacity: 0`) entre escenas para no cansar al usuario.
*   **Barra de Progreso:** Siempre presente en la parte superior (20px de alto) para retención de audiencia.

## 6. Comandos de Renderizado

Para generar el archivo final listo para subir:

```bash
npx hyperframes render --output pompe_reel_final.mp4 --quality high
```

---
*Diseño desarrollado para concientización médica en redes sociales.*
