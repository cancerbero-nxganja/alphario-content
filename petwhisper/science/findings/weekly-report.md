# PetWhisper Science — Weekly Report
*Semana del 2026-07-27 al 2026-08-02 | Actualizado: Ciclo #7*

---

## Resumen Ejecutivo

Séptima semana del programa de ciencia ciudadana PetWhisper. Se inicia nueva semana con lanzamiento del #PetWhisperChallenge (pilar viral). Se consolidan 6 hipótesis activas y se abre H-2026-07-F sobre señales de confort. Dataset en crecimiento proyectado: ~202,100 grabaciones (PROYECTADO), 43 especies, 39 países.

---

## Hipótesis Activas (7 total)

### H-2026-07-A: Variación tonal por tamaño corporal (perros)
- **Estado:** Exploratoria
- **Observación:** Tendencia preliminar a mayor frecuencia media en razas pequeñas vs grandes en contexto de juego (PROYECTADO / requiere validación)
- **Próximo paso:** Segmentar por contexto emocional antes de comparar

### H-2026-07-B: Patrón de llamada de atención (gatos domésticos)
- **Estado:** Activa — recopilación de datos
- **Observación:** Posible convergencia de vocalizaciones dirigidas-a-humanos independiente del origen geográfico del gato (PROYECTADO)
- **Próximo paso:** Análisis de espectrograma comparativo ES vs BR vs MX

### H-2026-07-B-ext: Reducción vocal en felinos en refugio
- **Estado:** Diseño de protocolo
- **Observación:** Felinos con >30 días en refugio podrían mostrar reducción cuantitativa y cualitativa de vocalizaciones como indicador de estrés crónico (PROYECTADO)
- **Implicación práctica:** El perfil vocal podría ser indicador de bienestar para protocolo de adopción
- **Colaboración necesaria:** Refugio con acceso a grabaciones longitudinales

### H-2026-07-C: Idioma del dueño y forma de llamada a mascotas
- **Estado:** Exploratoria
- **Observación:** ¿La prosodia del idioma del humano influye en la respuesta vocal del animal? Datos insuficientes aún (PROYECTADO)
- **Próximo paso:** Recolectar pares humano-animal estratificados por idioma

### H-2026-07-D: Ciclo vocal como predictor de adaptación
- **Estado:** Diseño de protocolo
- **Observación:** Mascotas recién adoptadas podrían mostrar un arco vocal predecible (silencio → exploración → confianza) detectable con grabaciones seriadas (PROYECTADO)
- **Implicación:** Métrica de adaptación post-adopción para la app
- **Requiere:** Campo `shelter_days` y `recording_series_id` en schema v0.2

### H-2026-07-E: Correlación raza-idioma en respuesta a comandos
- **Estado:** Exploratoria temprana
- **Observación:** ¿Las razas desarrolladas en culturas específicas (Border Collie UK, Xoloitzcuintle MX) muestran respuesta diferencial a comandos en el idioma de origen vs idioma del dueño actual? (PROYECTADO)
- **Próximo paso:** Definir protocolo de recolección dirigida

### H-2026-07-F: Firmas acústicas de confort activo *(nueva)*
- **Estado:** Exploratoria — apertura
- **Observación:** Los animales podrían producir vocalizaciones específicas en estado de confort activo (ronroneo, gruñido suave de juego, vocalización de bienvenida) con firmas espectrales consistentes entre individuos de la misma especie. Si se confirma, servirían como baseline emocional positivo para detectar desvíos (PROYECTADO)
- **Implicación:** Crear categoría "confort" en el modelo además de "estrés/alerta/juego"
- **Próximo paso:** Revisar dataset existente buscando grabaciones etiquetadas como "contento/feliz"

---

## Progreso del Dataset

| Métrica | Semana Anterior | Esta Semana (inicio) | Tendencia |
|---------|----------------|----------------------|-----------|
| Grabaciones globales | ~194,300 | ~202,100 (PROYECTADO) | +4% diario |
| Especies representadas | 43 | 43 | estable |
| Países activos | 39 | 39 | estable |
| Hipótesis activas | 6 | 7 | +1 |
| Grabaciones del #PetWhisperChallenge | — | pendiente | — |

*Todos los valores numéricos son PROYECTADOS para planificación. PetWhisper está en fase pre-lanzamiento.*

---

## Schema v0.2 — Campos Pendientes

1. **`breed_work_type`** — función histórica de la raza (herding, hunting, companion, guard, etc.)
   - Relevante para: H-2026-07-E
2. **`household_type`** — composición del hogar (adulto solo, pareja, familia con niños, multimascotas)
   - Relevante para: H-2026-07-B, H-2026-07-C
3. **`shelter_days`** — días en refugio al momento de grabación (0 = no proviene de refugio)
   - Relevante para: H-2026-07-B-ext, H-2026-07-D
4. **`recording_series_id`** — ID de agrupación para grabaciones longitudinales del mismo animal
   - Relevante para: H-2026-07-D
5. **`emotional_baseline_label`** — etiqueta de estado base del animal ("confort", "alerta", "juego", "estrés")
   - Relevante para: H-2026-07-F *(nuevo)*

---

## AlertaMascota (PROYECTADO)

| Métrica | Valor |
|---------|-------|
| Casos activos | ~71 |
| Reuniones confirmadas acumuladas | ~22 |
| Tasa de resolución acumulada | ~15% |
| Radio más usado | 10km |
| Ciudades piloto potenciales | CDMX, Buenos Aires, São Paulo, Madrid |

---

## Hallazgo Destacado — Semana Actual

**H-2026-07-F (nueva)** — Las firmas de confort son científicamente menos estudiadas que las de estrés porque no generan alarma conductual, pero son igual de importantes para entender el bienestar animal. Si PetWhisper puede detectar cuándo un animal está activamente en bienestar — no solo ausencia de malestar — tendríamos una herramienta única para dueños y refugios.

Esto refuerza la misión: los animales son seres libres con vida emocional propia, y la tecnología debe ayudar a escucharla en toda su dimensión.

---

## Contenido Científico — Semana 2026-07-27 al 2026-08-02

| Día | Pilar | Tema |
|-----|-------|------|
| Lun 2026-07-27 | Viral | #PetWhisperChallenge — demo app |
| Mar 2026-07-28 | Adopción | Perfil emocional refugio (pendiente) |
| Mié 2026-07-29 | Educación | Dato científico lenguaje animal (pendiente) |
| Jue 2026-07-30 | Ciencia | H-2026-07-F firmas de confort (pendiente) |
| Vie 2026-07-31 | Viral | Challenge viral (pendiente) |
| Sáb 2026-08-01 | Adopción | Perfil emocional refugio (pendiente) |
| Dom 2026-08-02 | Comunidad | Resumen semanal + historia AlertaMascota (pendiente) |

---

## Próximas Acciones

1. Monitorear respuesta al #PetWhisperChallenge — métricas de engagement
2. Diseñar protocolo formal para colaboración con primer refugio (H-2026-07-B-ext)
3. Publicar schema v0.2 como propuesta técnica en CONTRIBUTING.md
4. Revisar dataset para grabaciones etiquetadas como "confort" (H-2026-07-F)
5. Definir ciudades piloto para AlertaMascota: CDMX, Buenos Aires, São Paulo, Madrid

---

*Generado por PetWhisper Brain — Ciclo autónomo #7 — 2026-07-27*
