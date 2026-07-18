# AlertaMascota — Diseño Completo del Feature
**PetWhisper | Módulo de Emergencia Animal**
**Versión:** 1.0 — Spec Inicial
**Fecha:** 2026-07-18
**Estado:** SPEC (pendiente implementación)

---

## Filosofía Central

AlertaMascota es el sistema de alerta tipo Amber Alert para mascotas perdidas y encontradas, integrado directamente en PetWhisper. **Siempre gratuito. Sin excepción.** Un animal perdido es una emergencia. Las emergencias no tienen precio de acceso.

Los animales son seres libres, no objetos. Este sistema existe para acortar el tiempo en que un ser vivo pasa separado de su familia.

---

## Ubicación en la App

- Tab principal: **Alerta** (cuarto ícono en la barra de navegación inferior)
- Acceso desde la pantalla de inicio mediante banner contextual cuando hay alertas activas en la zona del usuario
- Widget opcional en pantalla de bloqueo (Android 14+)

---

## Flujos Principales

### 1. Reportar Mascota Perdida

**Campos requeridos:**
- Foto(s) de la mascota (hasta 5 imágenes)
- Nombre de la mascota
- Especie (perro / gato / ave / conejo / otro)
- Última ubicación GPS conocida (mapa interactivo o coordenadas automáticas)
- Descripción libre (color, tamaño, marcas distintivas, collar, chip)
- Contacto del dueño (teléfono o email — visible solo para usuarios verificados)

**Campos opcionales:**
- Número de microchip
- Raza
- Fecha/hora aproximada de pérdida
- Recompensa (no recomendada pero no bloqueada)

**Al enviar:**
- Se genera una alerta push inmediata a todos los usuarios de PetWhisper dentro del radio configurado (5 / 10 / 25 km)
- Formato de notificación push: `🚨 ALERTA: [especie] perdida cerca de ti — [nombre] — [distancia]km`
- La alerta queda activa en el tab Alerta de usuarios del área
- Se asigna un ID único a la alerta (ej: `PW-2026-07-18-00347`)

**Privacidad del dueño:**
- La ubicación precisa del dueño NUNCA es pública
- Solo se muestra zona general (barrio / colonia aproximada)
- El contacto directo solo es visible tras verificación básica (no bloquea, solo registra)

---

### 2. Reportar Mascota Encontrada

**Principio de fricción cero:** No se requiere registro para reportar una mascota encontrada. Esto es crítico — en emergencias, cada segundo de fricción reduce reportes.

**Flujo:**
1. Usuario abre app → Tab Alerta → "Encontré una mascota"
2. Foto + ubicación GPS actual (obligatorios, el resto opcional)
3. Sistema hace match automático con alertas activas en la zona (radio 5km inicial, expandible a 25km)
4. Si hay match: notificación inmediata al dueño con la ubicación del encuentro
5. Si no hay match: el reporte queda en el historial público de la zona por 72h

**Para usuarios sin cuenta:** flujo simplificado con solo foto + ubicación + botón de contacto manual.

---

### 3. Estados de una Alerta

```
BUSCANDO → ENCONTRADA (posible match) → REUNION CONFIRMADA
                ↓                              ↓
          (false positive)              Caso cerrado ✓
          vuelve a BUSCANDO
```

- **BUSCANDO:** Alerta activa, se distribuye push a usuarios del área
- **ENCONTRADA:** Match detectado, pendiente confirmación del dueño
- **REUNION CONFIRMADA:** Dueño confirmó que recuperó a su mascota — el caso pasa al historial público

---

### 4. Historial Público de Animales Encontrados

- Feed público de casos cerrados con estado REUNION CONFIRMADA
- Muestra: foto, nombre, especie, zona general (no dirección exacta), fecha de reencuentro
- Propósito: motivar a la comunidad a participar ("aquí están las historias donde SÍ funcionó")
- Filtros: por zona, especie, fecha
- No muestra datos personales del dueño ni reportante

---

## Sistema de Match Automático

**Criterios de coincidencia (por peso):**
1. Proximidad geográfica (radio configurable, default 5km) — 40%
2. Especie — 30%
3. Similitud visual (IA de PetWhisper analiza fotos) — 20%
4. Características textuales (color, raza si se indicó) — 10%

**Umbral de notificación:** ≥ 60% de coincidencia genera notificación automática al dueño.
**Umbral de match destacado:** ≥ 80% muestra banner rojo urgente.

---

## Compatibilidad con HumanAlert API

- Integración con HumanAlert API para reportar animales en zonas de desastre (inundaciones, incendios, terremotos)
- En modo desastre: el radio de distribución sube automáticamente a 50km
- Coordinación con autoridades locales vía webhook (configurable por región)
- Los reportes en zona de desastre se marcan con ícono especial y prioridad alta

---

## Notificaciones

### Push a usuarios del área:
```
🚨 ALERTA PetWhisper
[ESPECIE] perdida cerca de ti
[NOMBRE] · [DISTANCIA]km de tu ubicación
[Descripción breve]
→ Toca para ver detalles y ayudar
```

### Push al dueño cuando hay match:
```
📍 ¡Posible avistamiento de [NOMBRE]!
Un usuario reportó una mascota similar a [DISTANCIA]km.
→ Ver ubicación y contactar
```

### Push de confirmación a la comunidad:
```
💚 [NOMBRE] fue encontrada
Gracias a la comunidad de PetWhisper.
[Ciudad] · [FECHA]
```

---

## Privacidad y Seguridad

| Dato | Visible para todos | Visible para usuarios verificados | Nunca visible |
|------|-------------------|-----------------------------------|---------------|
| Foto mascota | ✓ | ✓ | — |
| Nombre mascota | ✓ | ✓ | — |
| Zona general | ✓ | ✓ | — |
| Última ubicación precisa | — | ✓ | — |
| Contacto dueño | — | ✓ | — |
| Dirección exacta del dueño | — | — | ✓ |
| Historial de ubicaciones | — | — | ✓ |

---

## Casos de Uso Estimados (PROYECTADO)

- Tiempo promedio de resolución estimado: < 4 horas en zonas urbanas (PROYECTADO)
- Tasa de match exitoso esperada: 35-55% de casos reportados (PROYECTADO)
- Adopción de feature: se espera sea el segundo más usado después del análisis de sonidos (PROYECTADO)

*Nota: Todos los valores marcados PROYECTADO son estimaciones sin datos reales disponibles.*

---

## Roadmap Técnico

### Fase 1 (MVP)
- [x] Spec completa
- [ ] Reporte de pérdida (formulario básico)
- [ ] Reporte de encontrada (sin registro)
- [ ] Match geográfico simple (sin IA)
- [ ] Push notifications a radio fijo

### Fase 2
- [ ] Match por similitud visual (IA)
- [ ] Radio configurable por el usuario
- [ ] Historial público de reencuentros
- [ ] Integración HumanAlert API

### Fase 3
- [ ] Widget pantalla de bloqueo
- [ ] Modo desastre automático
- [ ] API pública para refugios y protectoras

---

## Principios Inamovibles

1. **Siempre gratuito** — no hay tier de pago para AlertaMascota, jamás.
2. **Fricción cero para reportar encontrada** — sin registro requerido.
3. **Privacidad del dueño protegida** — ubicación precisa nunca pública.
4. **Los animales son seres libres** — el lenguaje de toda la UI refleja dignidad animal.
5. **Comunidad > tecnología** — la notificación humana es el motor real, la IA es el acelerador.
