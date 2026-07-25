# PetWhisper Science — Weekly Report
**Semana:** 21–28 Julio 2026
**Generado:** 2026-07-25 (actualización ciclo 5)
**Estado del modelo:** v0.1-pre (entrenamiento activo)

---

> ⚠️ **Nota de transparencia:** Todos los valores cuantitativos en este reporte están marcados como PROYECTADO o HIPÓTESIS. PetWhisper está en fase pre-lanzamiento. No se publican datos reales que no existan.

---

## Resumen Ejecutivo

Semana 4 del ciclo científico activo. Esta actualización (ciclo #5, sábado 2026-07-25) incorpora: (1) consolidación del perfil emocional de adopción como metodología, (2) formalización del caso de uso "traducción emocional para refugios", (3) nueva hipótesis H-2026-07-B-ext sobre reducción vocal en felinos con larga estancia en refugio, y (4) nueva hipótesis H-2026-07-D sobre ciclo vocal como predictor de adaptación post-adopción. El dataset global proyectado supera las 186,800 grabaciones (PROYECTADO), con 43+ especies en 39 países.

---

## Hipótesis Activas

### H-2026-07-A: Variación vocálica por idioma del cuidador
**Estado:** En diseño de validación | **Última actualización:** 2026-07-23

Hipótesis: perros cuyos cuidadores hablan idiomas tonales (mandarín, tailandés, vietnamita) muestran mayor variación de pitch que perros de cuidadores de idiomas no tonales.

**Base en literatura:** Faragó et al. (2010), Pongrácz et al. (2005). **Criterio:** 500+ grabaciones por grupo lingüístico, controles por raza/edad/contexto. **Estado: INSUFICIENTE.**

---

### H-2026-07-A-ext: Variabilidad vocal por presión evolutiva selectiva
**Estado:** Base bibliográfica sólida | **Creada:** 2026-07-23

Hipótesis: perros de razas de pastoreo tienen repertorio vocal más variado que razas de guardia, como consecuencia de selección artificial para comunicación colaborativa.

**Base:** Pongrácz et al. (2005), Hare & Woods (2013), Yin & McCowan (2004). **Criterio:** 200+ grabaciones/raza, 5+ razas pastoreo vs. 5+ guardia. **Estado: INSUFICIENTE — campo `breed_work_type` pendiente.**

---

### H-2026-07-B: Repertorio de maullidos en gatos mono vs. multi-hogar
**Estado:** Diseño pendiente | **Última actualización:** 2026-07-25

Hipótesis: gatos adultos desarrollan un repertorio de maullidos cualitativamente diferente según composición del hogar.

**Base:** McComb et al. (2009), Nicastro (2004). **Estado: campo `household_type` pendiente de implementar en schema v0.2.**

---

### H-2026-07-B-ext: Reducción vocal en felinos con larga estancia en refugio (NUEVA)
**Estado:** Hipótesis especulativa | **Creada:** 2026-07-25

Hipótesis: gatos que llevan más de 90 días en refugio muestran reducción estadística en variedad y frecuencia de maullidos dirigidos-a-humano, como indicador de "learned helplessness" parcial.

**Relevancia práctica:** Posible alerta automática para refugios: "Este animal lleva X días sin vocalización activa — revisión recomendada."

**Base en literatura:** Kry & Casey (2007), McCobb et al. (2005). **Estado: HIPÓTESIS ESPECULATIVA — requiere protocolo longitudinal con refugio colaborador.**

---

### H-2026-07-C: Vocalización pre-tormenta como señal meteorológica
**Estado:** Hipótesis especulativa | **Última actualización:** 2026-07-23

Hipótesis: perros con sensibilidad barométrica vocalizan con mayor frecuencia 30–60 min antes de tormentas. Cross-correlación con Open-Meteo API. **Estado: SIN DATOS SUFICIENTES.**

---

### H-2026-07-D: Ciclo vocal como predictor de adaptación post-adopción (NUEVA)
**Estado:** Hipótesis operacional | **Creada:** 2026-07-25

Hipótesis: el patrón "llamada → espera → repetición" (observado en demo Mango) es común en perros de alta orientación social y predice el tiempo de adaptación post-adopción.

**Relevancia:** "Índice de persistencia vocal" podría informar recomendaciones de match adoptante-animal. **Estado: HIPÓTESIS OPERACIONAL — surge de demo cualitativo. Requiere datos reales.**

---

## Dataset Global (PROYECTADO)

| Métrica | Valor | Nota |
|---------|-------|------|
| Grabaciones totales | ~186,800 | PROYECTADO — baseline 172,716 + ~4%/día × 2 días |
| Especies representadas | 43+ | PROYECTADO |
| Países activos | 39 | PROYECTADO |
| Versión del modelo | v0.1-pre | Pre-lanzamiento |
| Idiomas activos | 3 (ES, EN, PT) | Confirmado |

---

## AlertaMascota (PROYECTADO)

| Métrica | Valor |
|---------|-------|
| Casos activos | ~62 |
| Reuniones confirmadas semana | ~3 |
| Tasa de resolución acumulada | ~14% |
| Radio más usado | 10km |

---

## Campos Pendientes — Schema v0.2

1. `breed_work_type` — función histórica de la raza
2. `household_type` — composición del hogar
3. `shelter_days` — días en refugio al momento de grabación
4. `recording_series_id` — agrupación de grabaciones longitudinales

---

## Próximas Acciones

1. Diseñar protocolo longitudinal para refugio colaborador (H-2026-07-B-ext)
2. Definir schema v0.2 e impacto en app
3. Revisar literatura sobre acústica en contexto de refugio
4. Documentar metodología de perfil emocional de adopción como feature formal

---

*Generado por PetWhisper Brain — Ciclo autónomo #5 — 2026-07-25*
