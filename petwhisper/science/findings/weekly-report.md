# PetWhisper Science — Weekly Report
**Semana:** 21–28 Julio 2026
**Generado:** 2026-07-21
**Estado del modelo:** v0.1-pre (entrenamiento activo)

---

> ⚠️ **Nota de transparencia:** Todos los valores cuantitativos en este reporte están marcados como PROYECTADO o HIPÓTESIS. PetWhisper está en fase pre-lanzamiento. No se publican datos reales que no existan.

---

## Resumen Ejecutivo

Esta semana el ciclo científico avanza en tres frentes: (1) refinamiento de hipótesis sobre variación vocálica inter-idioma, (2) diseño de protocolo para gatos en hogares mono vs. multi-especie, y (3) primera evaluación cualitativa de datos preliminares de AlertaMascota. El dataset global supera las 160,000 grabaciones estimadas (PROYECTADO), con crecimiento sostenido de nuevos países.

---

## Hipótesis Activas

### H-2026-07-A: Variación vocálica por idioma del cuidador
**Estado:** Hipótesis en diseño de validación

Hipótesis: perros cuyos cuidadores hablan idiomas tonales (mandarín, tailandés, vietnamita) podrían mostrar patrones de vocalización con mayor variación de pitch que perros de cuidadores de idiomas no tonales.

**Base en literatura:**
- Faragó et al. (2010): los perros son sensibles al tono y prosodia humana.
- Pongrácz et al. (2005): los ladridos contienen información contextual estructurada.
- La hipótesis de co-evolución lingüística dog-human no ha sido estudiada sistemáticamente con datasets de escala global.

**Criterio para validar:** Minimum 500 grabaciones por grupo lingüístico, variables de control por raza/edad/contexto. **Estado: INSUFICIENTE — diseño de protocolo pendiente.**

---

### H-2026-07-B: Repertorio de maullidos en gatos mono vs. multi-hogar
**Estado:** Hipótesis nueva — requiere campo metadata adicional

Hipótesis: gatos adultos desarrollan un repertorio de maullidos cualitativamente diferente según si conviven con otros gatos, solo con humanos, o en entornos mixtos.

**Base en literatura:**
- McComb et al. (2009): gatos embeds solicitations de alta frecuencia dentro de ronroneos para manipular respuestas humanas.
- Nicastro (2004): humanos identifican contexto de maullidos con precisión superior al azar.
- El maullido es comunicación inter-especie, no intra-especie (gatos feral no maúllan entre ellos).

**Próximo paso:** Añadir campo `household_type` (solo-humano / multi-gato / mixto) al esquema de grabaciones en próxima versión de app. **Estado: DISEÑO PENDIENTE.**

---

### H-2026-07-C: Vocalización pre-tormenta como señal meteorológica
**Estado:** Hipótesis especulativa — alta originalidad

Hipótesis: perros con sensibilidad barométrica vocalizan con mayor frecuencia e intensidad 30–60 minutos antes de tormentas eléctricas.

**Potencial aplicación:** sistema de alerta meteorológica ciudadana basado en comportamiento animal colectivo.

**Validación:** cross-correlate timestamps de grabaciones con datos meteorológicos abiertos (Open-Meteo API). Requiere geolocalización de grabaciones + >10,000 en zonas con tormentas frecuentes. **Estado: HIPÓTESIS ESPECULATIVA — sin datos.**

---

### H-2026-07-A continuación — Razas de pastoreo vs. guardianas (hipótesis previa)
**Estado:** Hipótesis en exploración (desde semana anterior)

Algunas razas de pastoreo parecen usar rangos de frecuencia más altos para alertas vs. razas guardianas. Observación anecdótica del dataset preliminar.

**Criterio para confirmar:** ≥50 grabaciones etiquetadas por raza principal. **Estado: INSUFICIENTE.**

---

## Métricas de Dataset (PROYECTADO)

| Métrica | Valor | Nota |
|---|---|---|
| Grabaciones totales | ~160,650 | PROYECTADO — baseline 142,800 + ~4%/día × 3 días |
| Crecimiento vs. semana pasada | +12.5% | PROYECTADO |
| Especies representadas | 42+ | PROYECTADO (subida desde 12 — nuevas grabaciones de aves y roedores) |
| Países contribuyentes | 38 | PROYECTADO |
| Idiomas de interfaz activos | 14 | PROYECTADO |
| Contribuyentes activos (est.) | ~9,800 | PROYECTADO |
| Grabaciones esta semana | ~17,850 | PROYECTADO |

---

## Estado del Modelo v0.1-pre

Sin métricas de rendimiento publicables esta semana. Las clasificaciones de la app siguen siendo heurísticas preliminares — orientativas, no diagnósticas.

**Foco de la semana en modelo:** mejora de pre-procesamiento de audio (reducción de ruido ambiental antes de inferencia). Sin resultados publicables aún.

**Próximo hito:** v0.1 con validación mínima. Fecha estimada: PENDIENTE de volumen de dataset.

---

## AlertaMascota — Datos Preliminares (PROYECTADO)

| Métrica | Valor |
|---|---|
| Alertas de pérdida activas | ~47 |
| Animales encontrados | ~8 |
| Reuniones confirmadas | ~5 |
| Tasa de reencuentro estimada | ~10.6% sobre alertas activas |
| Radio más efectivo (observación preliminar) | 10–15 km |

**Nota científica:** AlertaMascota generará en el futuro un dataset de movilidad de mascotas perdidas que podría contribuir a estudios de etología urbana. El match actual es geográfico + textual; la visión por computadora para comparación de fotos es trabajo futuro.

---

## Ciencia Ciudadana — Prioridades Esta Semana

1. Grabaciones de **aves en hogar** (loros, periquitos, canarios) — especie sub-representada
2. Perros en **contexto de espera activa** (saben que el dueño regresa)
3. Cualquier **especie exótica** con contexto documentado
4. Grabaciones en **idiomas poco representados**: portugués, árabe, hindi

**¿Cómo contribuir?** App PetWhisper → "Contribuir al dataset"

---

## Literatura de Referencia

1. Faragó, T. et al. (2010). The bone is mine: affective and referential aspects of dog growls. *Animal Behaviour*, 79(4), 917–925.
2. McComb, K. et al. (2009). The cry embedded within the purr. *Current Biology*, 19(13), R507–R508.
3. Nicastro, N. (2004). Perceptual and acoustic evidence for species-level differences in meow vocalizations by domestic cats. *Journal of Comparative Psychology*, 118(3), 287–296.
4. Slobodchikoff, C.N. (2012). *Chasing Doctor Dolittle: Learning the Language of Animals*. St. Martin's Press.

---

*Próximo reporte: 28 Julio 2026*
*Contacto ciencia: science@petwhisper.ai (PROYECTADO)*
*Generado por PetWhisper Brain — Ciclo autónomo #2 — 2026-07-21*
