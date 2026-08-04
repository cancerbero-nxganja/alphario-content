# PetWhisper Science — Weekly Report
*Semana del 2026-08-03 al 2026-08-09 | Actualizado: Ciclo #11 — 2026-08-04*

---

## Resumen Ejecutivo

Undécimo ciclo del programa de ciencia ciudadana PetWhisper. Semana en curso con pilar de Adopción: perfil vocal de Viento (mestizo, 3 años, Refugio Patitas Libres Buenos Aires, 47 días en refugio). Caso representativo de H-2026-07-D (arco vocal post-refugio) y H-2026-07-B-ext (reducción vocal en refugio). Dataset proyectado: ~274,050 grabaciones (PROYECTADO), 43 especies, 39 países. AlertaMascota: ~83 casos activos, ~28 reuniones confirmadas acumuladas (PROYECTADO).

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
- **Estado:** Diseño de protocolo — aplicada a caso canino (Viento, ciclo 11)
- **Observación:** Felinos (y caninos) con >30 días en refugio muestran reducción vocal como indicador de estrés de adaptación; la recuperación de vocalizaciones es indicador positivo de readaptación (PROYECTADO)
- **Caso ilustrativo (ciclo 11):** Viento (mestizo, 47 días, Patitas Libres BsAs) mostró transición de silencio a exploración activa — consistente con la hipótesis extendida a caninos
- **Implicación práctica:** El perfil vocal como indicador de bienestar para protocolo de adopción
- **Colaboración necesaria:** Refugio con acceso a grabaciones longitudinales

### H-2026-07-C: Idioma del dueño y forma de llamada a mascotas
- **Estado:** Exploratoria
- **Observación:** ¿La prosodia del idioma del humano influye en la respuesta vocal del animal? Datos insuficientes aún (PROYECTADO)
- **Próximo paso:** Recolectar pares humano-animal estratificados por idioma

### H-2026-07-D: Ciclo vocal como predictor de adaptación *(foco ilustrativo del ciclo 11)*
- **Estado:** Diseño de protocolo — caso representativo activo
- **Observación:** El perfil de Viento (ciclo 11) ilustra el arco predicho: Silencio → Exploración activa → (proyectado) Confianza plena
- **Patrón detectado (PROYECTADO):** Vocalizaciones de exploración activa (380–520 Hz media) + llamada de atención dirigida (estructura repetitiva ascendente) → fase de transición Silencio→Exploración
- **Implicación:** Métrica de adaptación post-adopción para la app
- **Requiere:** Campo `shelter_days` y `recording_series_id` en schema v0.2
- **Nota:** Los valores de frecuencia son representativos/PROYECTADOS para ilustración del modelo

### H-2026-07-E: Correlación raza-idioma en respuesta a comandos
- **Estado:** Exploratoria — activada para recolección dirigida
- **Observación:** Las razas desarrolladas en culturas específicas podrían mostrar respuesta vocal diferencial a comandos en el idioma histórico vs el idioma actual del dueño (PROYECTADO)
- **Razas objetivo:** Border Collie, Xoloitzcuintle, Akita Inu, Podenco Ibicenco, Chow Chow, Basenji
- **Próximo paso:** Publicar protocolo de recolección dirigida en app (campo `breed_work_type` requerido)

### H-2026-07-F: Firmas acústicas de confort activo
- **Estado:** Exploratoria — revisión de dataset existente
- **Observación:** Los animales podrían producir vocalizaciones específicas en estado de confort activo con firmas espectrales consistentes entre individuos de la misma especie (PROYECTADO)
- **Implicación:** Crear categoría "confort" en modelo v0.2 como baseline positivo

### H-2026-08-A: Lateralización vocal en vocalizaciones de bienestar
- **Estado:** Activa — recolección de protocolo
- **Observación:** Las vocalizaciones de estados positivos podrían mostrar lateralización acústica documentable en dataset ciudadano (PROYECTADO)
- **Base científica:** Lateralización cerebral en procesamiento emocional documentada en mamíferos (Vallortigara & Rogers, 2005 [PUBLICADO])
- **Protocolo:** Requiere campo `recording_direction` en schema v0.2

---

## Progreso del Dataset

| Métrica | Ciclo #9 | Ciclo #10 | Ciclo #11 (hoy) | Tendencia |
|---------|----------|-----------|-----------------|-----------|
| Grabaciones globales | ~216,400 | ~225,100 | ~274,050 (PROYECTADO) | +4% diario |
| Especies representadas | 43 | 43 | 43 | estable |
| Países activos | 39 | 39 | 39 | estable |
| Hipótesis activas | 7 | 8 | 8 | estable |
| Casos H-2026-07-D ilustrativos | — | — | 1 (Viento, BsAs) | nuevo |

*Todos los valores numéricos son PROYECTADOS para planificación. PetWhisper está en fase pre-lanzamiento.*

---

## Schema v0.2 — Campos Pendientes (7 pendientes)

1. **`breed_work_type`** — función histórica de la raza (herding, hunting, companion, guard, etc.)
2. **`breed_origin_language`** — idioma/idiomas hablados en la cultura de origen de la raza
3. **`household_type`** — composición del hogar
4. **`shelter_days`** — días en refugio al momento de grabación *(crítico para H-2026-07-B-ext y H-2026-07-D)*
5. **`recording_series_id`** — ID de agrupación para grabaciones longitudinales
6. **`emotional_baseline_label`** — etiqueta de estado base del animal
7. **`recording_direction`** — posición del micrófono relativa al animal *(crítico para H-2026-08-A)*

---

## AlertaMascota (PROYECTADO)

| Métrica | Ciclo #9 | Ciclo #10 | Ciclo #11 (hoy) |
|---------|----------|-----------|-----------------|
| Casos activos | ~76 | ~78 | ~83 |
| Reuniones confirmadas acumuladas | ~25 | ~26 | ~28 |
| Tasa de resolución acumulada | ~16% | ~17% | ~18% |
| Radio más usado | 10km | 10km | 10km |
| Ciudades piloto potenciales | CDMX, BsAs, São Paulo, Madrid | idem | idem |

*Todos los valores son PROYECTADOS. AlertaMascota en diseño/spec. Siempre gratuito.*

---

## Hallazgo Destacado — Ciclo 11

**H-2026-07-D: El arco vocal de Viento**

El perfil de Viento es el primer caso ilustrativo formal de H-2026-07-D. Un perro que llegó al refugio en silencio y que, 47 días después, vocaliza activamente tres tipos distintos de señal — exploración, vigilancia sin miedo, llamada de atención dirigida — muestra exactamente el arco que la hipótesis predice.

Lo que hace esto científicamente interesante no es el caso individual. Es que si este patrón se repite en múltiples animales de múltiples refugios, PetWhisper podría tener el primer dataset ciudadano que cuantifica la adaptación emocional post-refugio mediante análisis vocal. No un cuestionario. No una evaluación de comportamiento puntual. Una grabación.

Cuando un animal vocaliza de una manera específica, está comunicando algo sobre cómo se siente. Escuchar eso — y entenderlo — es lo que PetWhisper hace. Y hacerlo en el contexto de la adopción significa que las personas que quieran adoptar pueden tener una conversación más real con el animal antes de decidir.

Los animales son seres libres con vida emocional propia. La ciencia debe escucharlos — incluyendo en los 47 días en que están esperando que alguien aparezca.

---

## Calendario de Contenido — Semana 2026-08-03 al 2026-08-09

| Día | Pilar | Tema | Estado |
|-----|-------|------|--------|
| Lun 2026-08-03 | Viral | #PetWhisperChallenge — demo app semana 2 | Pendiente |
| Mar 2026-08-04 | Adopción | Perfil de Viento — arco vocal en refugio | ✅ Publicado hoy |
| Mié 2026-08-05 | Educación | Dato científico: lateralización emocional en mamíferos | Pendiente |
| Jue 2026-08-06 | Ciencia | H-2026-08-A: lateralización vocal en bienestar | Pendiente |
| Vie 2026-08-07 | Viral | Challenge + historia AlertaMascota de la semana | Pendiente |
| Sáb 2026-08-08 | Adopción | Segundo perfil refugio + traducción emocional de IA | Pendiente |
| Dom 2026-08-09 | Comunidad | Resumen semanal + reuniones AlertaMascota semana | Pendiente |
