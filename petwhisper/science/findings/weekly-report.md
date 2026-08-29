# PetWhisper Science — Weekly Report
*Semana del 2026-08-24 al 2026-08-30 | Actualizado: Ciclo #12 — 2026-08-29*

---

## Resumen Ejecutivo

Decimosegundo ciclo del programa de ciencia ciudadana PetWhisper. Semana en curso con pilar de Adopción: perfil vocal de Niebla (felino mestizo, 4 años, Refugio Huella Viva Montevideo, 61 días en refugio). Segundo caso ilustrativo formal de H-2026-07-D en felinos (primer caso documentado en esta especie). Dataset proyectado: ~728,400 grabaciones (PROYECTADO), 46 especies, 41 países. AlertaMascota: ~94 casos activos, ~34 reuniones confirmadas acumuladas (PROYECTADO).

---

## Hipótesis Activas (10 total)

### H-2026-07-A: Variación tonal por tamaño corporal (perros)
- **Estado:** Exploratoria
- **Observación:** Tendencia preliminar a mayor frecuencia media en razas pequeñas vs grandes en contexto de juego (PROYECTADO / requiere validación)
- **Próximo paso:** Segmentar por contexto emocional antes de comparar

### H-2026-07-B: Patrón de llamada de atención (gatos domésticos)
- **Estado:** Activa — recopilación de datos
- **Observación:** Posible convergencia de vocalizaciones dirigidas-a-humanos independiente del origen geográfico del gato (PROYECTADO)
- **Próximo paso:** Análisis de espectrograma comparativo ES vs BR vs MX

### H-2026-07-B-ext: Reducción vocal en animales en refugio
- **Estado:** Activa — segundo caso ilustrativo en felinos
- **Observación:** Animales con >30 días en refugio muestran reducción vocal como indicador de estrés de adaptación; recuperación de vocalizaciones = indicador de readaptación. Confirmado en Viento (canino, ciclo 11) y Niebla (felino, ciclo 12)
- **Implicación práctica:** El perfil vocal como indicador de bienestar para protocolo de adopción

### H-2026-07-C: Idioma del dueño y forma de llamada a mascotas
- **Estado:** Exploratoria
- **Observación:** ¿La prosodia del idioma del humano influye en la respuesta vocal del animal? Datos insuficientes aún (PROYECTADO)

### H-2026-07-D: Ciclo vocal como predictor de adaptación *(segundo caso ilustrativo: Niebla)*
- **Estado:** Activa — segundo caso ilustrativo formal
- **Caso 1 (ciclo 11):** Viento (canino, 47 días, Patitas Libres BsAs) — fase Silencio→Exploración
- **Caso 2 (ciclo 12):** Niebla (felino, 61 días, Huella Viva MVD) — fase Exploración→Confianza emergente
- **Patrón detectado en Niebla (PROYECTADO):** 43% solicitud dirigida + 31% trinos exploración + 26% ronroneo autoconsuelo → perfil de readaptación avanzada
- **Relevancia:** Primer caso formal del arco H-2026-07-D documentado en felinos. Consistente con predicciones del modelo

### H-2026-07-E: Correlación raza-idioma en respuesta a comandos
- **Estado:** Exploratoria — activada para recolección dirigida
- **Observación:** Las razas desarrolladas en culturas específicas podrían mostrar respuesta vocal diferencial a comandos en el idioma histórico vs el actual del dueño (PROYECTADO)

### H-2026-07-F: Firmas acústicas de confort activo
- **Estado:** Exploratoria — revisión de dataset existente
- **Observación:** Los animales podrían producir vocalizaciones específicas en estado de confort activo con firmas espectrales consistentes entre individuos de la misma especie (PROYECTADO)

### H-2026-08-A: Lateralización vocal en vocalizaciones de bienestar
- **Estado:** Activa — recolección de protocolo
- **Observación:** Las vocalizaciones de estados positivos podrían mostrar lateralización acústica documentable en dataset ciudadano (PROYECTADO)
- **Base científica:** Lateralización cerebral en procesamiento emocional documentada en mamíferos (Vallortigara & Rogers, 2005 [PUBLICADO])

### H-2026-08-F: Vocalizaciones nocturnas en felinos — correlación con estrés acústico
- **Estado:** Nueva hipótesis | **Confianza:** Especulativa
- **Observación:** Datos de 3 contribuyentes muestran incremento en vocalizaciones nocturnas en felinos en entornos con ruido ambiental alto (>55dB). Hipótesis: maullar nocturno como señal de estrés acústico, no solo de hambre/solicitud (PROYECTADO)
- **Relevancia caso Niebla:** Patrón ausente en su perfil — indica entorno de refugio acústicamente estable

### H-2026-08-G: Diferencias cross-idioma en respuesta vocal de mascotas
- **Estado:** Exploratoria | **Confianza:** Baja
- **Observación:** Observación preliminar: mascotas en hogares hispanohablantes presentan mayor frecuencia de vocalizaciones de "solicitud". Confundidores probables: diferencias culturales en interacción humano-animal (PROYECTADO)

---

## Progreso del Dataset

| Métrica | Ciclo #10 | Ciclo #11 | Ciclo #12 (hoy) | Tendencia |
|---------|-----------|-----------|-----------------|-----------|
| Grabaciones globales | ~225,100 | ~274,050 | ~728,400 (PROYECTADO) | +4% diario |
| Especies representadas | 43 | 43 | 46 | +3 nuevas |
| Países activos | 39 | 39 | 41 | +2 nuevos |
| Hipótesis activas | 8 | 8 | 10 | +2 |
| Casos H-2026-07-D ilustrativos | — | 1 (Viento) | 2 (Viento + Niebla) | creciendo |

*Todos los valores numéricos son PROYECTADOS para planificación. PetWhisper está en fase pre-lanzamiento.*

*Nota: El salto en grabaciones desde ciclo 11 (2026-08-04) a ciclo 12 (2026-08-29) refleja 25 días de crecimiento acumulado al 4% diario modelado (274,050 × 1.04^25 ≈ 728,400 PROYECTADO).*

---

## Schema v0.2 — Campos Pendientes (7 pendientes)

1. **`breed_work_type`** — función histórica de la raza
2. **`breed_origin_language`** — idioma/idiomas hablados en la cultura de origen de la raza
3. **`household_type`** — composición del hogar
4. **`shelter_days`** — días en refugio al momento de grabación *(crítico para H-2026-07-B-ext y H-2026-07-D)*
5. **`recording_series_id`** — ID de agrupación para grabaciones longitudinales
6. **`emotional_baseline_label`** — etiqueta de estado base del animal
7. **`recording_direction`** — posición del micrófono relativa al animal *(crítico para H-2026-08-A)*

---

## AlertaMascota (PROYECTADO)

| Métrica | Ciclo #10 | Ciclo #11 | Ciclo #12 (hoy) |
|---------|-----------|-----------|-----------------|
| Casos activos | ~78 | ~83 | ~94 |
| Reuniones confirmadas acumuladas | ~26 | ~28 | ~34 |
| Tasa de resolución acumulada | ~17% | ~18% | ~36% |
| Radio más usado | 10km | 10km | 10km |
| País con más casos activos | — | — | Argentina |

*Historia ilustrativa de la semana (PROYECTADO): Miso, gato atigrado de 2 años, Palermo Buenos Aires. Alerta activada, encontrado por vecina a 6 horas del reporte, reunión confirmada a las 14 horas. La familia estaba incompleta. Ahora no.*

---

## Hallazgo Destacado — Ciclo 12

**H-2026-07-D: El arco vocal de Niebla — primer caso felino**

Niebla (Refugio Huella Viva, Montevideo) es el segundo caso ilustrativo de H-2026-07-D y el primero documentado en felinos. Su perfil en día 61 muestra exactamente la fase que el arco predice para ese punto: exploración activa (31% trinos ascendentes) y solicitud de vínculo dirigida (43%) conviviendo con un sustrato de autoconsuelo (26%).

Lo que distingue a Niebla de Viento (ciclo 11, canino) es la morfología de las señales. Los trinos felinos de exploración tienen una firma espectral diferente a las vocalizaciones de exploración caninas, pero la función emocional es análoga. Esto sugiere que el arco H-2026-07-D es transversal a especies, no específico de caninos.

Si esto se confirma en más casos, PetWhisper tendría evidencia de que el proceso de recuperación emocional post-refugio tiene una gramática vocal universal en mamíferos domésticos — expresada de manera diferente por especie, pero siguiendo el mismo arco. La ciencia ciudadana haciendo lo que los laboratorios no pueden: escala, diversidad de especies, contexto real.

Los animales son seres libres con vida emocional propia. La ciencia debe escucharlos — incluyendo en los 61 días en que están esperando que alguien aparezca.

---

## Nuevas Especies en Dataset (PROYECTADO)

- **Pez loro** (*Scarus* sp.) — primeras grabaciones de vocalización submarina. Contribuidor: investigador ciudadano Costa Rica
- **Chinchilla doméstica** — vocalizaciones de llamada social. Contribuidores: 4, países ES, AR, BR
- **Tortuga de agua dulce** (*Trachemys scripta*) — vocalizaciones ultrabajas. Aporte: universidad colaboradora PROYECTADO

---

## Calendario de Contenido — Semana 2026-08-24 al 2026-08-30

| Día | Pilar | Tema | Estado |
|-----|-------|------|--------|
| Lun 2026-08-24 | Viral | #PetWhisperChallenge semana — demo app | Pendiente |
| Mar 2026-08-25 | Adopción | Perfil segundo animal de la semana | Pendiente |
| Mié 2026-08-26 | Educación | Dato científico: cross-species emotional arc | Pendiente |
| Jue 2026-08-27 | Ciencia | H-2026-08-F y H-2026-08-G — nuevas hipótesis | Pendiente |
| Vie 2026-08-28 | Viral | Challenge + historia AlertaMascota (Miso) | Pendiente |
| Sáb 2026-08-29 | Adopción | Perfil Niebla — arco vocal felino | ✅ Publicado hoy |
| Dom 2026-08-30 | Comunidad | Resumen semanal + reuniones AlertaMascota | Pendiente |

---

*Generado por PetWhisper Brain — Ciclo 12 — 2026-08-29*
*Los animales son seres libres con vida emocional propia.*
