# PetWhisper Science — Weekly Report
*Semana del 2026-07-20 al 2026-07-26 | Actualizado: Ciclo #6*

---

## Resumen Ejecutivo

Sexta semana del programa de ciencia ciudadana PetWhisper. Se añaden nuevas hipótesis longitudinales, se consolida el marco de análisis cruzado por raza e idioma, y se abre el protocolo de colaboración con refugios. Dataset en crecimiento proyectado: ~194,300 grabaciones (PROYECTADO), 43 especies, 39 países.

---

## Hipótesis Activas (6 total)

### H-2026-07-A: Variación tonal por tamaño corporal (perros)
- **Estado:** Exploratoria
- **Observación:** Tendencia preliminar a mayor frecuencia media en razas pequeñas vs grandes en contexto de juego (PROYECTADO / requiere validación)
- **Próximo paso:** Segmentar por contexto emocional antes de comparar

### H-2026-07-B: Patrón de llamada de atención (gatos domésticos)
- **Estado:** Activa — recopilación de datos
- **Observación:** Posible convergencia de vocalizaciones dirigidas-a-humanos independiente del origen geográfico del gato (PROYECTADO)
- **Próximo paso:** Análisis de espectrograma comparativo ES vs BR vs MX

### H-2026-07-B-ext: Reducción vocal en felinos en refugio
- **Estado:** Nueva — diseño de protocolo
- **Observación:** Hipótesis derivada de H-2026-07-B. Felinos con >30 días en refugio podrían mostrar reducción cuantitativa y cualitativa de vocalizaciones como indicador de estrés crónico (PROYECTADO)
- **Implicación práctica:** El perfil vocal podría ser indicador de bienestar para protocolo de adopción
- **Colaboración necesaria:** Refugio con acceso a grabaciones longitudinales

### H-2026-07-C: Idioma del dueño y forma de llamada a mascotas
- **Estado:** Exploratoria
- **Observación:** ¿La prosodia del idioma del humano influye en la respuesta vocal del animal? Datos insuficientes aún (PROYECTADO)
- **Próximo paso:** Recolectar pares humano-animal estratificados por idioma

### H-2026-07-D: Ciclo vocal como predictor de adaptación
- **Estado:** Nueva — hipótesis de diseño
- **Observación:** Mascotas recién adoptadas podrían mostrar un arco vocal predecible (silencio → exploración → confianza) detectable con grabaciones seriadas (PROYECTADO)
- **Implicación:** Métrica de adaptación post-adopción para la app
- **Requiere:** Campo `shelter_days` y `recording_series_id` en schema v0.2

### H-2026-07-E: Correlación raza-idioma en respuesta a comandos
- **Estado:** Exploratoria temprana
- **Observación:** ¿Las razas desarrolladas en culturas específicas (Border Collie UK, Xoloitzcuintle MX) muestran respuesta diferencial a comandos en el idioma de origen vs idioma del dueño actual? (PROYECTADO)
- **Próximo paso:** Definir protocolo de recolección dirigida

---

## Progreso del Dataset

| Métrica | Semana Anterior | Esta Semana | Tendencia |
|---------|----------------|-------------|-----------|
| Grabaciones globales | ~172,700 | ~194,300 (PROYECTADO) | +12.5% (acum.) |
| Especies representadas | 41 | 43 | +2 |
| Países activos | 37 | 39 | +2 |
| Hipótesis activas | 4 | 6 | +2 |
| Perfiles emocionales demo | 1 | 2 | +1 |

*Todos los valores numéricos son PROYECTADOS para planificación. PetWhisper está en fase pre-lanzamiento.*

---

## Schema v0.2 — Campos Pendientes

Los siguientes campos están bloqueados como necesarios para las hipótesis activas:

1. **`breed_work_type`** — función histórica de la raza (herding, hunting, companion, guard, etc.)
   - Relevante para: H-2026-07-E
2. **`household_type`** — composición del hogar (adulto solo, pareja, familia con niños, multimascotas)
   - Relevante para: H-2026-07-B, H-2026-07-C
3. **`shelter_days`** — días en refugio al momento de grabación (0 = no proviene de refugio)
   - Relevante para: H-2026-07-B-ext, H-2026-07-D
4. **`recording_series_id`** — ID de agrupación para grabaciones longitudinales del mismo animal
   - Relevante para: H-2026-07-D

**Decisión pendiente:** Migración de datos existentes vs captura forward-only con schema v0.2.

---

## AlertaMascota (PROYECTADO)

| Métrica | Valor |
|---------|-------|
| Casos activos | ~68 |
| Reuniones confirmadas esta semana | ~4 |
| Tasa de resolución acumulada | ~15% |
| Radio más usado | 10km |
| Historia destacada semana | Luna (CDMX) — gata naranja, 72h, 47 colaboradores |

---

## Hallazgo Destacado de la Semana

**H-2026-07-D** — El concepto de "arco vocal de adaptación" en mascotas post-adopción es la hipótesis con mayor potencial de impacto directo en la app. Si se valida, permitiría:
- Dar al nuevo dueño un indicador objetivo de adaptación
- Detectar mascotas en proceso de adopción fallida antes de que sea tarde
- Crear un perfil longitudinal que refuerce el vínculo humano-animal

Esto conecta directamente con la misión: los animales son seres libres, y la tecnología debe ayudar a que vivan como tales.

---

## Próximas Acciones

1. Diseñar protocolo de colaboración formal con primer refugio (H-2026-07-B-ext)
2. Publicar schema v0.2 como propuesta técnica en CONTRIBUTING.md
3. Revisar literatura sobre acústica animal en contexto de estrés crónico
4. Definir criterios de validación para H-2026-07-D (¿cuántas grabaciones por animal? ¿qué intervalo?)
5. Explorar ciudades piloto para AlertaMascota: CDMX, Buenos Aires, São Paulo, Madrid

---

## Contenido Científico Publicado Esta Semana

| Día | Plataforma | Tema |
|-----|-----------|------|
| Lun 2026-07-21 | TikTok / IG / Twitter | Demo análisis de sonido — viral |
| Mar 2026-07-22 | TikTok / IG / Twitter | Adopción — Kira, perfil emocional |
| Mié 2026-07-23 | TikTok / IG / Twitter | Educación — lenguaje de las colas |
| Jue (pendiente) | — | — |
| Vie (pendiente) | — | — |
| Sáb 2026-07-25 | TikTok / IG / Twitter | Adopción — Mango, perfil emocional |
| Dom 2026-07-26 | TikTok / IG / Twitter | Comunidad — Luna, historia AlertaMascota |

---

*Generado por PetWhisper Brain — Ciclo autónomo #6 — 2026-07-26*
