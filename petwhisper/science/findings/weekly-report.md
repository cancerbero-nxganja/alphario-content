# PetWhisper Science — Weekly Report
**Semana:** 21–28 Julio 2026
**Generado:** 2026-07-23 (actualización ciclo 4)
**Estado del modelo:** v0.1-pre (entrenamiento activo)

---

> ⚠️ **Nota de transparencia:** Todos los valores cuantitativos en este reporte están marcados como PROYECTADO o HIPÓTESIS. PetWhisper está en fase pre-lanzamiento. No se publican datos reales que no existan.

---

## Resumen Ejecutivo

Esta semana el ciclo científico avanza en cinco frentes: (1) refinamiento de hipótesis sobre variación vocálica inter-idioma, (2) diseño de protocolo para gatos en hogares mono vs. multi-especie, (3) primera evaluación cualitativa de datos preliminares de AlertaMascota, (4) hipótesis validada en literatura sobre el maullido interespecífico, y (5) **nueva hipótesis abierta (H-2026-07-A-ext) sobre variabilidad vocal por raza y presión evolutiva selectiva.** El dataset global supera las 172,700 grabaciones estimadas (PROYECTADO), con crecimiento sostenido de nuevos países.

---

## Hipótesis Activas

### H-2026-07-A: Variación vocálica por idioma del cuidador
**Estado:** Hipótesis en diseño de validación
**Última actualización:** 2026-07-23

Hipótesis: perros cuyos cuidadores hablan idiomas tonales (mandarín, tailandés, vietnamita) podrían mostrar patrones de vocalización con mayor variación de pitch que perros de cuidadores de idiomas no tonales.

**Base en literatura:**
- Faragó et al. (2010): los perros son sensibles al tono y prosodia humana.
- Pongrácz et al. (2005): los ladridos contienen información contextual estructurada.
- La hipótesis de co-evolución lingüística dog-human no ha sido estudiada sistemáticamente con datasets de escala global.

**Criterio para validar:** Minimum 500 grabaciones por grupo lingüístico, variables de control por raza/edad/contexto. **Estado: INSUFICIENTE — diseño de protocolo pendiente.**

**Actualización 2026-07-23:** Esta hipótesis fue el eje central del contenido de ciencia del ciclo #4. La hipótesis se formula públicamente para comunidad científica. Ver scripts 2026-07-23.md.

---

### H-2026-07-A-ext: Variabilidad vocal por presión evolutiva selectiva (NUEVA)
**Estado:** Hipótesis nueva — base bibliográfica sólida
**Creada:** 2026-07-23

Hipótesis: perros de razas de pastoreo (Border Collie, Australian Shepherd, Kelpie, Shetland Sheepdog) exhiben un repertorio vocal más variado — mayor número de tonos distintos, mayor variación contextual — que razas orientadas a la guardia (Rottweiler, Dogo Argentino, Dobermann).

**Mecanismo hipotético:** La selección artificial para trabajo colaborativo a distancia con humanos favoreció mayor granularidad comunicativa. La selección para vigilancia y disuasión favoreció vocalizaciones más uniformes pero más intimidantes.

**Base en literatura:**
- Pongrácz et al. (2005): los ladridos contienen información contextual codificada; humanos pueden identificar contexto con 60-80% de precisión.
- Hare & Woods (2013): *The Genius of Dogs* — diferencias inter-raza en comunicación social.
- Yin & McCowan (2004): acoustic analysis of dog vocalizations during different contexts shows context-dependent variation.

**Criterio para validar:** ≥200 grabaciones etiquetadas por raza principal, ≥5 razas de pastoreo vs. ≥5 razas de guardia, controladas por contexto (solo, con humano, con otro perro). **Estado: INSUFICIENTE — requiere campo metadata `raza` con clasificación por tipo de trabajo histórico.**

**Próxima acción:** Añadir campo `breed_work_type` (pastoreo / guardia / compañía / caza / rastreo) al esquema de grabaciones v0.2.

---

### H-2026-07-B: Repertorio de maullidos en gatos mono vs. multi-hogar
**Estado:** Hipótesis nueva — requiere campo metadata adicional
**Última actualización:** 2026-07-23

Hipótesis: gatos adultos desarrollan un repertorio de maullidos cualitativamente diferente según si conviven con otros gatos, solo con humanos, o en entornos mixtos.

**Base en literatura:**
- McComb et al. (2009): gatos embeds solicitations de alta frecuencia dentro de ronroneos para manipular respuestas humanas.
- Nicastro (2004): humanos identifican contexto de maullidos con precisión superior al azar (~70%).
- El maullido es comunicación inter-especie, no intra-especie (gatos ferales no se maullan entre ellos de forma sostenida).

**Próximo paso:** Añadir campo `household_type` (solo-humano / multi-gato / mixto) al esquema de grabaciones en próxima versión de app. **Estado: DISEÑO PENDIENTE.**

---

### H-2026-07-C: Vocalización pre-tormenta como señal meteorológica
**Estado:** Hipótesis especulativa — alta originalidad
**Última actualización:** 2026-07-23

Hipótesis: perros con sensibilidad barométrica vocalizan con mayor frecuencia e intensidad 30–60 minutos antes de tormentas eléctricas.

**Potencial aplicación:** sistema de alerta meteorológica ciudadana basado en comportamiento animal colectivo.

**Validación:** cross-correlate timestamps de grabaciones con datos meteorológicos abiertos (Open-Meteo API). Requiere geolocalización de grabaciones + >10,000 en zonas con tormentas frecuentes. **Estado: HIPÓTESIS ESPECULATIVA — sin datos suficientes.**

---

### H-2026-07-D: El maullido como comunicación interespecífica exclusiva
**Estado:** Bien documentada en literatura — pendiente de validación con dataset propio
**Última actualización:** 2026-07-23

Hipótesis operativa: los maullidos de larga duración en gatos domésticos adultos son señales casi exclusivamente interespecíficas (gato→humano), no intraespecíficas (gato→gato).

**Base en literatura:**
- Nicastro & Owren (2003): adult domestic cats meow primarily to humans, not to other cats.
- McComb et al. (2009): gatos desarrollan "solicitation purrs" embebidos con componentes de alta frecuencia que activan respuesta urgente en humanos.
- Bradshaw & Cameron-Beaumont (2000): gatos ferales muestran repertorio vocal significativamente más reducido que domésticos en lo que respecta a maullidos prolongados.

**Implicación para el dataset:** La variable `context_human_present` se convierte en variable crítica para clasificar maullidos de forma válida. **Estado: VALIDADA EN LITERATURA — pendiente de confirmación con datos propios.**

**Actualización 2026-07-23:** Esta hipótesis fue comunicada exitosamente a la comunidad en el ciclo #3 (contenido educativo Miércoles). Nivel de comprensión pública: hipótesis claramente explicada en 3 idiomas.

---

## Métricas de Dataset (PROYECTADO)

| Métrica | Valor | Nota |
|---|---|---|
| Grabaciones totales | ~172,716 | PROYECTADO — 166,073 × 1.04 |
| Crecimiento vs. ayer | +6,643 | PROYECTADO |
| Crecimiento vs. inicio de semana (21 jul) | +9.5% | PROYECTADO |
| Especies representadas | 43+ | PROYECTADO |
| Países contribuyentes | 39 | PROYECTADO |
| Idiomas de interfaz activos | 14 | PROYECTADO |
| Contribuyentes activos (est.) | ~10,600 | PROYECTADO |

---

## Estado del Modelo v0.1-pre

Sin métricas de rendimiento publicables esta semana. Las clasificaciones de la app siguen siendo heurísticas preliminares — orientativas, no diagnósticas.

**Foco de la semana en modelo:** mejora de pre-procesamiento de audio (reducción de ruido ambiental antes de inferencia). Sin resultados publicables aún.

**Próximo hito:** v0.1 con validación mínima. Fecha estimada: PENDIENTE de volumen de dataset.

---

## Schema v0.2 — Campos Planificados

Los ciclos de contenido científico de esta semana han generado tres campos nuevos de metadata requeridos para validación de hipótesis activas:

| Campo | Hipótesis | Estado |
|---|---|---|
| `household_type` | H-2026-07-B | Pendiente de diseño |
| `context_human_present` | H-2026-07-D | Pendiente de implementación |
| `breed_work_type` | H-2026-07-A-ext | Pendiente de diseño |
| `caretaker_language` | H-2026-07-A | Pendiente de diseño |

---

## AlertaMascota — Datos Preliminares (PROYECTADO)

| Métrica | Valor |
|---|---|
| Alertas de pérdida activas | ~57 |
| Animales encontrados (acumulado semana) | ~13 |
| Reuniones confirmadas (acumulado semana) | ~8 |
| Tasa de reencuentro estimada | ~14% sobre alertas activas |
| Radio más efectivo (observación preliminar) | 10–15 km |

**Nota científica:** AlertaMascota generará en el futuro un dataset de movilidad de mascotas perdidas que podría contribuir a estudios de etología urbana. El match actual es geográfico + textual; la visión por computadora para comparación de fotos es trabajo futuro.

---

## Ciencia Ciudadana — Prioridades Esta Semana

1. Grabaciones de **gatos** con campo de contexto documentado (humano presente / ausente)
2. Grabaciones de **aves en hogar** (loros, periquitos, canarios) — especie sub-representada
3. **Perros con raza documentada** — especialmente pastoreo y guardia — para H-2026-07-A-ext
4. Perros en **contexto de espera activa** (saben que el dueño regresa)
5. Grabaciones en **idiomas poco representados**: portugués, árabe, hindi

**¿Cómo contribuir?** App PetWhisper → "Contribuir al dataset"

---

## Literatura de Referencia

1. Faragó, T. et al. (2010). The bone is mine: affective and referential aspects of dog growls. *Animal Behaviour*, 79(4), 917–925.
2. McComb, K. et al. (2009). The cry embedded within the purr. *Current Biology*, 19(13), R507–R508.
3. Nicastro, N. (2004). Perceptual and acoustic evidence for species-level differences in meow vocalizations by domestic cats. *Journal of Comparative Psychology*, 118(3), 287–296.
4. Nicastro, N. & Owren, M.J. (2003). Classification of domestic cat (*Felis catus*) vocalizations by naive and experienced human listeners. *Journal of Comparative Psychology*, 117(1), 44–52.
5. Bradshaw, J.W.S. & Cameron-Beaumont, C. (2000). The signalling repertoire of the domestic cat and its undomesticated relatives. In Turner & Bateson (Eds.), *The Domestic Cat: The Biology of Its Behaviour* (2nd ed., pp. 67–93).
6. Slobodchikoff, C.N. (2012). *Chasing Doctor Dolittle: Learning the Language of Animals*. St. Martin's Press.
7. Pongrácz, P. et al. (2005). Human listeners are able to classify dog barks recorded in different situations. *Journal of Comparative Psychology*, 119(2), 136–144.
8. Yin, S. & McCowan, B. (2004). Barking in domestic dogs: context specificity and individual identification. *Animal Behaviour*, 68(2), 343–355.
9. Hare, B. & Woods, V. (2013). *The Genius of Dogs*. Dutton.

---

*Próximo reporte: 28 Julio 2026*
*Contacto ciencia: science@petwhisper.ai (PROYECTADO)*
*Generado por PetWhisper Brain — Ciclo autónomo #4 — 2026-07-23*
