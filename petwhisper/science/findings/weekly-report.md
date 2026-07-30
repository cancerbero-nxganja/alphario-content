# PetWhisper Science — Weekly Report
*Semana del 2026-07-27 al 2026-08-02 | Actualizado: Ciclo #10 — 2026-07-30*

---

## Resumen Ejecutivo

Décimo ciclo del programa de ciencia ciudadana PetWhisper. Semana en curso con avance en hipótesis de correlación raza-idioma (H-2026-07-E) y apertura formal de H-2026-08-A sobre lateralización vocal en vocalizaciones de bienestar. Dataset proyectado: ~225,100 grabaciones (PROYECTADO), 43 especies, 39 países. AlertaMascota: ~78 casos activos, ~26 reuniones confirmadas acumuladas (PROYECTADO).

---

## Hipótesis Activas (8 total)

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

### H-2026-07-E: Correlación raza-idioma en respuesta a comandos *(foco del día)*
- **Estado:** Exploratoria — activada para recolección dirigida
- **Observación:** Las razas desarrolladas en culturas específicas (Border Collie UK, Xoloitzcuintle MX, Akita JP, Podenco ES) podrían mostrar respuesta vocal diferencial a comandos en el idioma histórico de la raza vs el idioma actual del dueño (PROYECTADO)
- **Mecanismo propuesto:** Siglos de coevolución habrían dejado sesgos en el procesamiento prosódico de la raza — no cognición lingüística, sino preferencias auditivas heredadas culturalmente
- **Razas objetivo para recolección:** Border Collie, Xoloitzcuintle, Akita Inu, Podenco Ibicenco, Chow Chow, Basenji
- **Protocolo mínimo:** Mismo comando, dos idiomas (origen histórico vs idioma actual del dueño), mismo contexto (neutro, sin carga emocional previa), grabación separada de respuesta vocal
- **Próximo paso:** Publicar protocolo de recolección dirigida en app (campo `breed_work_type` requerido)

### H-2026-07-F: Firmas acústicas de confort activo
- **Estado:** Exploratoria — revisión de dataset existente
- **Observación:** Los animales podrían producir vocalizaciones específicas en estado de confort activo con firmas espectrales consistentes entre individuos de la misma especie (PROYECTADO)
- **Implicación:** Crear categoría "confort" en modelo v0.2 como baseline positivo
- **Próximo paso:** Revisar grabaciones etiquetadas "contento/feliz" en dataset actual

### H-2026-08-A: Lateralización vocal en vocalizaciones de bienestar *(nueva — ciclo 10)*
- **Estado:** Apertura formal
- **Observación:** Las vocalizaciones de estados positivos (ronroneo, gemido suave de juego, vocalización de bienvenida) podrían mostrar lateralización acústica: origen preferente en un lado del aparato fonador o procesamiento auditivo asimétrico (PROYECTADO)
- **Base científica:** La lateralización cerebral en procesamiento emocional está documentada en mamíferos (revisión Vallortigara & Rogers, 2005 [PUBLICADO]). La extensión al dominio acústico en contextos de bienestar es una extrapolación de ciencia ciudadana aún sin validar en este dataset.
- **Implicación:** Si se confirma, PetWhisper sería el primer dataset ciudadano en documentarlo sistemáticamente en múltiples especies y contextos
- **Protocolo:** Requiere grabaciones estereofónicas o grabaciones dirigidas desde el frente y desde el flanco del animal
- **Próximo paso:** Habilitar campo `recording_direction` en schema v0.2 para etiquetar posición del micrófono

---

## Progreso del Dataset

| Métrica | Ciclo #7 | Ciclo #9 | Ciclo #10 (hoy) | Tendencia |
|---------|----------|----------|-----------------|-----------|
| Grabaciones globales | ~202,100 | ~216,400 | ~225,100 (PROYECTADO) | +4% diario |
| Especies representadas | 43 | 43 | 43 | estable |
| Países activos | 39 | 39 | 39 | estable |
| Hipótesis activas | 7 | 7 | 8 | +1 (H-2026-08-A) |
| Protocolo dirigido abierto | — | — | H-2026-07-E | nuevo |

*Todos los valores numéricos son PROYECTADOS para planificación. PetWhisper está en fase pre-lanzamiento.*

---

## Schema v0.2 — Campos Pendientes (actualizado)

1. **`breed_work_type`** — función histórica de la raza (herding, hunting, companion, guard, etc.)
   - Relevante para: H-2026-07-E
2. **`breed_origin_language`** — idioma/idiomas hablados en la cultura de origen de la raza
   - Relevante para: H-2026-07-E *(nuevo — ciclo 10)*
3. **`household_type`** — composición del hogar (adulto solo, pareja, familia con niños, multimascotas)
   - Relevante para: H-2026-07-B, H-2026-07-C
4. **`shelter_days`** — días en refugio al momento de grabación (0 = no proviene de refugio)
   - Relevante para: H-2026-07-B-ext, H-2026-07-D
5. **`recording_series_id`** — ID de agrupación para grabaciones longitudinales del mismo animal
   - Relevante para: H-2026-07-D
6. **`emotional_baseline_label`** — etiqueta de estado base del animal ("confort", "alerta", "juego", "estrés")
   - Relevante para: H-2026-07-F
7. **`recording_direction`** — posición del micrófono relativa al animal (frente/flanco-izquierdo/flanco-derecho/omnidireccional)
   - Relevante para: H-2026-08-A *(nuevo — ciclo 10)*

---

## AlertaMascota (PROYECTADO)

| Métrica | Ciclo #7 | Ciclo #9 | Ciclo #10 (hoy) |
|---------|----------|----------|-----------------|
| Casos activos | ~71 | ~76 | ~78 |
| Reuniones confirmadas acumuladas | ~22 | ~25 | ~26 |
| Tasa de resolución acumulada | ~15% | ~16% | ~17% |
| Radio más usado | 10km | 10km | 10km |
| Ciudades piloto potenciales | CDMX, BsAs, São Paulo, Madrid | idem | idem |

*Todos los valores son PROYECTADOS. AlertaMascota en diseño/spec.*

---

## Hallazgo Destacado — Ciclo 10

**H-2026-07-E (activada para recolección dirigida)**

La hipótesis de correlación raza-idioma es científicamente audaz porque cruza dos campos que raramente se intersectan: lingüística comparada y etología de razas caninas. La base teórica existe (coevolución humano-perro está documentada; la lateralización en procesamiento emocional también), pero la extrapolación a diferencias prosódicas entre razas es una hipótesis de ciencia ciudadana original.

Si PetWhisper logra recolectar suficientes grabaciones dirigidas de razas con historia cultural documentada, en múltiples idiomas, podríamos tener el primer dataset que permite explorar esta pregunta a escala. Eso es único.

**H-2026-08-A (apertura formal)**

La lateralización vocal en bienestar es el complemento científico a H-2026-07-F (firmas de confort). Si los animales muestran asimetría en cómo producen sus vocalizaciones de bienestar, eso habla de un sistema nervioso que organiza la emoción positiva de forma especializada. Entender eso es entender mejor cómo los animales experimentan el estar bien — no solo el estar mal.

Los animales son seres libres con vida emocional propia. La ciencia debe escucharlos en toda su dimensión.

---

## Calendario de Contenido — Semana 2026-07-27 al 2026-08-02

| Día | Pilar | Tema | Estado |
|-----|-------|------|--------|
| Lun 2026-07-27 | Viral | #PetWhisperChallenge — demo app | ✅ Publicado |
| Mar 2026-07-28 | Adopción | Perfil emocional refugio con IA | ✅ Publicado |
| Mié 2026-07-29 | Educación | Asimetría vocal en perros (Vallortigara 2007) | ✅ Publicado |
| Jue 2026-07-30 | Ciencia | H-2026-07-E + H-2026-08-A | ✅ Publicado hoy |
| Vie 2026-07-31 | Viral | Challenge + resultados preliminares semana | Pendiente |
| Sáb 2026-08-01 | Adopción | Perfil refugio + traducción emocional | Pendiente |
| Dom 2026-08-02 | Comunidad | Resumen semanal + historia AlertaMascota | Pendiente |
