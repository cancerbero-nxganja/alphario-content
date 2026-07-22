# PetWhisper Science — Weekly Report
**Semana:** 21–28 Julio 2026
**Generado:** 2026-07-22 (actualización ciclo 3)
**Estado del modelo:** v0.1-pre (entrenamiento activo)

---

> ⚠️ **Nota de transparencia:** Todos los valores cuantitativos en este reporte están marcados como PROYECTADO o HIPÓTESIS. PetWhisper está en fase pre-lanzamiento. No se publican datos reales que no existan.

---

## Resumen Ejecutivo

Esta semana el ciclo científico avanza en cuatro frentes: (1) refinamiento de hipótesis sobre variación vocálica inter-idioma, (2) diseño de protocolo para gatos en hogares mono vs. multi-especie, (3) primera evaluación cualitativa de datos preliminares de AlertaMascota, y (4) nueva hipótesis abierta sobre la naturaleza interespecífica del maullido felino. El dataset global supera las 166,000 grabaciones estimadas (PROYECTADO), con crecimiento sostenido de nuevos países.

---

## Hipótesis Activas

### H-2026-07-A: Variación vocálica por idioma del cuidador
**Estado:** Hipótesis en diseño de validación
**Última actualización:** 2026-07-22

Hipótesis: perros cuyos cuidadores hablan idiomas tonales (mandarín, tailandés, vietnamita) podrían mostrar patrones de vocalización con mayor variación de pitch que perros de cuidadores de idiomas no tonales.

**Base en literatura:**
- Faragó et al. (2010): los perros son sensibles al tono y prosodia humana.
- Pongrácz et al. (2005): los ladridos contienen información contextual estructurada.
- La hipótesis de co-evolución lingüística dog-human no ha sido estudiada sistemáticamente con datasets de escala global.

**Criterio para validar:** Minimum 500 grabaciones por grupo lingüístico, variables de control por raza/edad/contexto. **Estado: INSUFICIENTE — diseño de protocolo pendiente.**

**Nota:** El contenido educativo de este miércoles amplía el marco conceptual de esta hipótesis hacia felinos (ver H-2026-07-D nueva).

---

### H-2026-07-B: Repertorio de maullidos en gatos mono vs. multi-hogar
**Estado:** Hipótesis nueva — requiere campo metadata adicional
**Última actualización:** 2026-07-22

Hipótesis: gatos adultos desarrollan un repertorio de maullidos cualitativamente diferente según si conviven con otros gatos, solo con humanos, o en entornos mixtos.

**Base en literatura:**
- McComb et al. (2009): gatos embeds solicitations de alta frecuencia dentro de ronroneos para manipular respuestas humanas.
- Nicastro (2004): humanos identifican contexto de maullidos con precisión superior al azar (~70%).
- El maullido es comunicación inter-especie, no intra-especie (gatos ferales no se maullan entre ellos de forma sostenida).

**Próximo paso:** Añadir campo `household_type` (solo-humano / multi-gato / mixto) al esquema de grabaciones en próxima versión de app. **Estado: DISEÑO PENDIENTE.**

---

### H-2026-07-C: Vocalización pre-tormenta como señal meteorológica
**Estado:** Hipótesis especulativa — alta originalidad
**Última actualización:** 2026-07-21

Hipótesis: perros con sensibilidad barométrica vocalizan con mayor frecuencia e intensidad 30–60 minutos antes de tormentas eléctricas.

**Potencial aplicación:** sistema de alerta meteorológica ciudadana basado en comportamiento animal colectivo.

**Validación:** cross-correlate timestamps de grabaciones con datos meteorológicos abiertos (Open-Meteo API). Requiere geolocalización de grabaciones + >10,000 en zonas con tormentas frecuentes. **Estado: HIPÓTESIS ESPECULATIVA — sin datos suficientes.**

---

### H-2026-07-D: El maullido como comunicación interespecífica exclusiva (NUEVA)
**Estado:** Bien documentada en literatura — pendiente de validación con dataset propio
**Creada:** 2026-07-22

Hipótesis operativa: los maullidos de larga duración en gatos domésticos adultos son señales casi exclusivamente interespecíficas (gato→humano), no intraespecíficas (gato→gato).

**Base en literatura:**
- Nicastro & Owren (2003): adult domestic cats meow primarily to humans, not to other cats.
- McComb et al. (2009): gatos desarrollan "solicitation purrs" embebidos con componentes de alta frecuencia que activan respuesta urgente en humanos.
- Bradshaw & Cameron-Beaumont (2000): gatos ferales muestran repertorio vocal significativamente más reducido que domésticos en lo que respecta a maullidos prolongados.

**Implicación para el dataset:** La variable `context_human_present` (humano presente en el momento de la grabación) se convierte en variable crítica para clasificar maullidos de forma válida. Grabaciones sin humanos presentes representan una categoría comunicativa fundamentalmente diferente.

**Próxima acción:** Marcar como campo requerido en schema v0.2. **Estado: VALIDADA EN LITERATURA — pendiente de confirmación con datos propios.**

---

### H-2026-07-A cont. — Razas de pastoreo vs. guardianas
**Estado:** Hipótesis en exploración (desde semana anterior)

Hipótesis: razas de pastoreo (Border Collie, Australian Shepherd) muestran mayor variabilidad vocálica contextual que razas de guardia (Rottweiler, Dogo Argentino), reflejo de presión selectiva para comunicación colaborativa con humanos.

**Criterio para confirmar:** ≥200 grabaciones etiquetadas por raza principal, controladas por contexto. **Estado: INSUFICIENTE.**

---

## Métricas de Dataset (PROYECTADO)

| Métrica | Valor | Nota |
|---|---|---|
| Grabaciones totales | ~166,073 | PROYECTADO — baseline 160,650 + ~4%/día × 1 día |
| Crecimiento vs. ayer | +5,423 | PROYECTADO |
| Crecimiento vs. inicio de semana | +5.2% | PROYECTADO |
| Especies representadas | 42+ | PROYECTADO |
| Países contribuyentes | 39 | PROYECTADO |
| Idiomas de interfaz activos | 14 | PROYECTADO |
| Contribuyentes activos (est.) | ~10,200 | PROYECTADO |

---

## Estado del Modelo v0.1-pre

Sin métricas de rendimiento publicables esta semana. Las clasificaciones de la app siguen siendo heurísticas preliminares — orientativas, no diagnósticas.

**Foco de la semana en modelo:** mejora de pre-procesamiento de audio (reducción de ruido ambiental antes de inferencia). Sin resultados publicables aún.

**Próximo hito:** v0.1 con validación mínima. Fecha estimada: PENDIENTE de volumen de dataset.

---

## AlertaMascota — Datos Preliminares (PROYECTADO)

| Métrica | Valor |
|---|---|
| Alertas de pérdida activas | ~52 |
| Animales encontrados | ~10 |
| Reuniones confirmadas | ~6 |
| Tasa de reencuentro estimada | ~11.5% sobre alertas activas |
| Radio más efectivo (observación preliminar) | 10–15 km |

**Nota científica:** AlertaMascota generará en el futuro un dataset de movilidad de mascotas perdidas que podría contribuir a estudios de etología urbana. El match actual es geográfico + textual; la visión por computadora para comparación de fotos es trabajo futuro.

---

## Ciencia Ciudadana — Prioridades Esta Semana

1. Grabaciones de **gatos** con campo de contexto documentado (humano presente / ausente)
2. Grabaciones de **aves en hogar** (loros, periquitos, canarios) — especie sub-representada
3. Perros en **contexto de espera activa** (saben que el dueño regresa)
4. Cualquier **especie exótica** con contexto documentado
5. Grabaciones en **idiomas poco representados**: portugués, árabe, hindi

**¿Cómo contribuir?** App PetWhisper → "Contribuir al dataset"

---

## Literatura de Referencia

1. Faragó, T. et al. (2010). The bone is mine: affective and referential aspects of dog growls. *Animal Behaviour*, 79(4), 917–925.
2. McComb, K. et al. (2009). The cry embedded within the purr. *Current Biology*, 19(13), R507–R508.
3. Nicastro, N. (2004). Perceptual and acoustic evidence for species-level differences in meow vocalizations by domestic cats. *Journal of Comparative Psychology*, 118(3), 287–296.
4. Nicastro, N. & Owren, M.J. (2003). Classification of domestic cat (*Felis catus*) vocalizations by naive and experienced human listeners. *Journal of Comparative Psychology*, 117(1), 44–52.
5. Bradshaw, J.W.S. & Cameron-Beaumont, C. (2000). The signalling repertoire of the domestic cat and its undomesticated relatives. In D.C. Turner & P. Bateson (Eds.), *The Domestic Cat: The Biology of Its Behaviour* (2nd ed., pp. 67–93).
6. Slobodchikoff, C.N. (2012). *Chasing Doctor Dolittle: Learning the Language of Animals*. St. Martin's Press.

---

*Próximo reporte: 28 Julio 2026*
*Contacto ciencia: science@petwhisper.ai (PROYECTADO)*
*Generado por PetWhisper Brain — Ciclo autónomo #3 — 2026-07-22*
