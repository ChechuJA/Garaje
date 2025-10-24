# 📊 Análisis Completo del Repositorio — Estrategia del Comprador

**Fecha:** 24 octubre 2025  
**Objetivo:** Negociar plazas de garaje con máximo ahorro posible  
**Referencia base:** Plaza 401 = 9.000 € (218,29 €/m²)

---

## 🎯 Resumen Ejecutivo

### Tu Posición como Comprador

✅ **VENTAJAS:**
- Tienes datos completos de las 32 plazas (precio, ubicación, metros)
- Has calculado un precio objetivo justo: **218,29 €/m²**
- Hay **inconsistencias evidentes** de precio entre plazas similares
- El vendedor tiene 32 plazas = presión para vender (inventario grande)
- Pagas al contado/rápido = ventaja competitiva

⚠️ **PUNTOS DE ATENCIÓN:**
- Plazas en P.S.3 (sótano 3) tienen precios similares a P.S.1 y P.S.2 (no tiene sentido)
- Rango de precios muy amplio: 10.500€ - 13.000€ (diferencia de 2.500€)
- Plazas grandes (>60 m²) ya tienen buen €/m² pero precio absoluto alto

---

## 💰 Análisis de Archivos del Repositorio

### 1. `plazas-garaje.md` (CANONICAL — NO TOCAR)
**Contenido:** Tabla original con 32 plazas + análisis de negociación  
**Estado:** ✅ Protegido y usado como backup ORIGINAL

**Datos clave:**
- Total plazas: 32
- Rango precios: 10.500€ - 13.000€
- Rango metros: 26,42 m² - 62,97 m²
- Precio medio €/m²: ~340 €/m² (DEMASIADO ALTO)

**Recomendaciones del archivo:**
- Plaza 356 y 320: 220,71 €/m² — Ya cerca de tu objetivo ✅
- Plaza 368: 206,46 €/m² — Mejor €/m² pero grande (62,97 m²)
- Plazas 300/301: 10.500€ — MÁS BARATAS (úsalas como referencia en negociación)

### 2. `plazas-garaje-analisis.md`
**Contenido:** Análisis detallado para negociación  
**Puntos fuertes para argumentar:**

1. **Oportunidades por €/m²** (ya documentadas)
2. **Inconsistencias de precio:**
   - Plaza 72 (36,92 m²): 10.800€ vs Plaza 299 (36,22 m²): 12.000€ → 1.200€ diferencia sin justificación
   - Plaza 341 (26,42 m²): 10.800€ vs Plaza 323 (26,42 m²): 10.500€ → MISMO tamaño, 300€ diferencia
3. **Argumentos por ubicación:**
   - P.S.3 debería ser MÁS BARATO que P.S.1 y P.S.2 (más profundo = menos accesible)
   - Actualmente hay plazas en P.S.3 más caras que P.S.1 = INCONSISTENCIA

### 3. `plazas-garaje-analisis-estimaciones.md`
**Contenido:** Cálculo de estimaciones usando plaza 401 como base  
**Hallazgos importantes:**

- **Plazas que EXCEDEN tu precio objetivo:**
  - Plaza 336: -359,20€ (más cara que tu oferta ideal)
  - Plaza 368: -745,57€ (más cara que tu oferta ideal)
  
- **Plazas con MEJOR oportunidad de ahorro:**
  - Plaza 61: ahorro potencial 5.377,86€
  - Plaza 62: ahorro potencial 5.342,93€
  - Plaza 239: ahorro potencial 5.542,93€

**⚠️ Nota:** Este archivo usa una estimación lineal (218,29 €/m² × metros). La app web usa reglas más sofisticadas:
- Reducción mínima 4.000€
- Si precio/m² > 218,29 → igualar a 218,29 €/m²

### 4. `plazas.json`
**Contenido:** Datos máquina-readable (JSON)  
**Estado:** ✅ Actualizado con plaza 401: precio 13.000€, oferta 9.000€  
**Uso:** Alimenta la app web interactiva

### 5. `index.html` — TU HERRAMIENTA PRINCIPAL
**Contenido:** App web interactiva con agente de negociación  
**Funcionalidades implementadas:**

✅ **Tabla principal:**
- Ordenación por metros, precio, OFERTA, ahorro
- Filtros por columna (UR, plaza, precio, ubicación, metros)
- Selección hasta 3 plazas para crear lote
- Favoritos y notas persistentes (localStorage)
- Marcar vendidas (se tachan y ocultan opcionalmente)

✅ **Tabla básica (móvil):**
- Vista compacta: Nº Plaza, Precio, OFERTA, Diferencia
- Ideal para consulta rápida en terreno

✅ **Guía de Visita (NUEVA):**
- Checklist de qué observar en cada plaza
- Estrategia de negociación con argumentos
- Mejores oportunidades destacadas

✅ **ORIGINAL:**
- Carga directamente desde `plazas-garaje.md`
- Tabla completa con columna UR/REGISTRAL
- Backup de datos sin modificar

✅ **Gastos Totales:**
- ITP (8% sobre OFERTA)
- Notaría: 400€-600€
- Gestoría: 100€-150€
- Total por plaza: rango mín-máx

✅ **Agente Flotante 🚗 (NUEVO):**
- Botón flotante accesible desde cualquier tab
- Ventana de chat optimizada para móvil
- Responde a:
  - `"top"` o `"mejores"` o `"chollos"` → **TOP 10 mejores oportunidades** (ordenadas por precio/m² y ahorro) 🏆
  - `"plaza 401"` → Ficha completa con OFERTA y gastos
  - `"401"` → Atajo (solo número)
  - `"calculame el precio del m2 si la plaza 401 vale 9000€"` → Cálculo precio/m², OFERTA recomendada, comparación con objetivo, ahorro, gastos
  - `"APACAAQUITUCOCHE marcar 401 favorito"` → Marca favorito
  - `"APACAAQUITUCOCHE marcar 401 vendida"` → Marca vendida
- Iconos y formato optimizado para lectura rápida
- Botones inline para favorito/vendida

✅ **Exportar/Importar:**
- CSV con todos los datos + OFERTA + Gastos
- JSON de selección (compartir entre dispositivos)
- URL compartible con estado (selección + ordenación)

### 6. `README.md`
**Contenido:** Documentación del proyecto  
**Estado:** ✅ Actualizado con funcionalidades principales  
**Recomendación:** Añadir sección sobre el agente flotante y comandos soportados

---

## 🎯 Estrategia de Negociación Recomendada

### Reglas de OFERTA (implementadas en la app)

1. **Reducción mínima:** Siempre restar al menos 4.000€ del precio de venta
2. **Equalización a objetivo:** Si precio/m² > 218,29 €/m² → ofrecer exactamente 218,29 €/m² × metros
3. **Aplicar la menor de ambas:** min(precio - 4.000€, 218,29 €/m² × metros)

**Ejemplo Plaza 401:**
- Precio venta: 13.000€
- Opción 1: 13.000€ - 4.000€ = 9.000€
- Opción 2: 218,29 €/m² × 41,23 m² = 9.000€
- **OFERTA:** 9.000€ ✅

### Tácticas en Terreno

#### ANTES de visitar:
1. **Identifica tus top 3-5 plazas** (usa la tabla ordenada por ahorro)
2. **Marca favoritas** en la app (botón ⭐)
3. **Añade notas** con requisitos específicos (ej: "debe caber SUV", "cerca de ascensor")
4. **Exporta selección** a JSON (backup en caso de que el móvil falle)

#### DURANTE la visita:
1. **Usa el agente flotante 🚗** para consultas instantáneas:
   - ¿Te enseñan plaza 324? → Escribe `"324"` y verás precio/OFERTA/ahorro al instante
   - ¿El vendedor dice "puedo dejártela en 10.500€"? → Escribe `"calculame el precio del m2 si la plaza 324 vale 10500"` y sabrás si está por debajo de tu objetivo
2. **Checklist física:**
   - Mide largo × ancho con cinta métrica (verifica datos)
   - Prueba entrar/salir con tu coche
   - Observa columnas, tuberías, humedad
   - Toma fotos (esquinas, obstáculos, altura)
3. **Marca vendidas** las que descubras que ya no están disponibles

#### DURANTE la negociación:
1. **Argumentos de inconsistencia:**
   - "He visto que la plaza 300 está a 10.500€ y es similar. ¿Por qué esta vale 11.500€?"
   - "Plazas en P.S.1 están más baratas que algunas de P.S.3. P.S.3 debería ser más económico por la profundidad."
   - "Plaza 72 y 299 son casi iguales en tamaño pero 1.200€ de diferencia. No tiene sentido."

2. **Ancla con tu precio objetivo:**
   - "He calculado que el precio justo por m² en este garaje es 218€/m²."
   - "Plaza 401 la he valorado en 9.000€ considerando su ubicación y tamaño."

3. **Ofrece ventajas:**
   - "Si aceptas mi precio, puedo pagar al contado esta semana."
   - "Estoy interesado en comprar 2-3 plazas si el precio es razonable."

4. **Usa el silencio:**
   - Haz tu oferta y calla. Quien habla primero pierde.
   - Si dice "no puedo bajar tanto", repite tu oferta y espera.

---

## 🎖️ Top 5 Plazas Recomendadas (Mejor Relación Calidad-Precio)

### 1. ⭐ Plaza 356 (P.S.3)
- **Precio venta:** 11.000€
- **Tu OFERTA:** 7.000€ (220,71 €/m² pero aplicando reducción 4.000€)
- **Metros:** 49,84 m² (GRANDE)
- **€/m² actual:** 220,71 €/m² (casi en objetivo)
- **Ahorro esperado:** 4.000€
- **Ventajas:** Muy grande, ya tiene buen precio/m², P.S.3
- **Usar argumento:** "Ya está cerca de precio justo, pero P.S.3 debe ser más barato."

### 2. ⭐ Plaza 320 (P.S.3)
- **Precio venta:** 11.000€
- **Tu OFERTA:** 7.000€
- **Metros:** 49,84 m² (GRANDE, igual que 356)
- **€/m² actual:** 220,71 €/m²
- **Ahorro esperado:** 4.000€
- **Ventajas:** Gemela de plaza 356
- **Estrategia:** Oferta por LOTE (356 + 320) = podría aceptar 7.000€ × 2 = 14.000€ por ambas

### 3. 🏆 Plaza 368 (P.S.3)
- **Precio venta:** 13.000€
- **Tu OFERTA:** 9.000€ (reducción 4.000€, pero €/m² sería 142,92 — MUY por debajo de objetivo)
- **Metros:** 62,97 m² (LA MÁS GRANDE)
- **€/m² actual:** 206,46 €/m² (mejor €/m² del conjunto)
- **Ahorro esperado:** 4.000€
- **Ventajas:** Plaza ENORME si necesitas mucho espacio
- **Riesgo:** Precio absoluto alto; pregunta por qué es tan cara si P.S.3 debería ser barato

### 4. 💰 Plaza 300 o 301 (P.S.3)
- **Precio venta:** 10.500€ (LAS MÁS BARATAS)
- **Tu OFERTA:** 6.500€
- **Metros:** ~27-29 m² (pequeñas pero suficientes)
- **€/m² actual:** ~360-387 €/m² (alto €/m² pero bajo precio absoluto)
- **Ahorro esperado:** 4.000€
- **Ventajas:** Precio absoluto más bajo, úsalas como referencia
- **Estrategia:** "Si estas están a 10.500€, las más grandes no deberían estar tanto más caras."

### 5. 🎯 Plaza 336 (P.S.3)
- **Precio venta:** 13.000€
- **Tu OFERTA:** 9.000€
- **Metros:** 61,20 m² (muy grande)
- **€/m² actual:** 212,42 €/m² (segundo mejor €/m²)
- **Ahorro esperado:** 4.000€
- **Ventajas:** Casi tan grande como 368, mejor €/m² después de 368
- **Comparar con:** Plaza 368 (misma OFERTA pero 368 es 1,77 m² más grande)

---

## 📱 Uso Óptimo de la App en Terreno

### Escenario 1: Antes de la visita — Identifica los chollos
1. Abre la app en el móvil
2. Pulsa el botón flotante 🚗
3. Escribe `"top"` o `"mejores"`
4. Guarda mentalmente las 3 primeras (🥇🥈🥉)
5. Pide al vendedor ver esas plazas específicamente

### Escenario 2: El vendedor te enseña plazas aleatorias
1. Pulsa el botón flotante 🚗
2. Escribe el número de plaza que estás viendo
3. Lee OFERTA y argumentos al instante
4. **No muestres la pantalla al vendedor** (mantén tu estrategia privada)

### Escenario 3: Te dice "puedo dejártela en X€"
1. Pulsa 🚗
2. Escribe: `"calculame el precio del m2 si la plaza 401 vale 10000"` (reemplaza 401 y 10000 por plaza y precio)
3. Mira si el precio/m² supera 218,29 €/m²
4. Si supera → rechaza o contraoferta más baja
5. Si está por debajo → acepta o negocia un poco más bajo

### Escenario 4: Visitas múltiples plazas en una hora
1. Usa la **Tabla Básica** (vista móvil)
2. Ordena por "Ahorro" descendente
3. Marca vendidas las que ya no estén disponibles
4. Añade notas rápidas: "columna molesta", "húmeda", "perfecta"
5. Exporta selección al final del día

---

## ⚠️ Puntos Críticos a Verificar

### En la visita física:

#### 🚗 Tamaño real vs anunciado
- **PROBLEMA:** Algunos vendedores inflan los metros
- **SOLUCIÓN:** Lleva cinta métrica, mide largo × ancho
- **Si los metros son menores:** Recalcula OFERTA con metros reales (usa el agente 🚗)

#### 🏗️ Obstáculos no visibles en planos
- Columnas en el centro (dificultan maniobras)
- Tuberías a baja altura (reduce altura útil)
- Pendiente pronunciada (dificulta entrada/salida)

#### 💧 Estado de conservación
- **Humedad/filtraciones:** Resta 500€-1.000€ de tu OFERTA
- **Grietas en suelo/paredes:** Puede indicar problemas estructurales
- **Iluminación deficiente:** No es defecto de la plaza pero molesto

#### 📍 Ubicación exacta en el sótano
- **Cerca de ascensor/escalera:** Más cómodo (justifica precio más alto)
- **Lejos de ascensor:** Menos cómodo (justifica precio más bajo)
- **Junto a rampa de salida:** Más fácil acceso (ventaja)
- **En rincón oscuro:** Menos atractivo (restar valor)

---

## 🎁 Recomendaciones Finales

### Para TI como comprador:

1. **No te enamores de ninguna plaza antes de verlas todas**
   - Visita al menos tus top 5
   - Compara físicamente antes de decidir

2. **Tu presupuesto máximo por plaza:**
   - Plazas pequeñas (~27 m²): 6.500€ - 7.000€
   - Plazas medianas (~40 m²): 8.500€ - 9.000€
   - Plazas grandes (~50 m²): 10.500€ - 11.000€
   - Plazas muy grandes (~60+ m²): 12.000€ - 13.000€

3. **Lotes ventajosos (comprar 2-3 juntas):**
   - **Lote Grande:** 356 + 320 (gemelas, ~100 m² total) → Oferta 14.000€ por ambas
   - **Lote Pequeño:** 300 + 301 (~55 m² total) → Oferta 12.000€ por ambas
   - **Lote Premium:** 368 + 336 (~124 m² total) → Oferta 17.000€ por ambas

4. **Si el vendedor no acepta tu OFERTA:**
   - Pregunta cuál es su "precio final"
   - Usa el agente 🚗 para calcular si vale la pena
   - Si supera 218,29 €/m² → rechaza educadamente
   - Deja tu contacto "por si cambia de opinión"

5. **Firma sólo si:**
   - Has verificado metros físicamente
   - Has probado tu coche dentro
   - Has revisado estado (humedad, obstáculos)
   - El precio está dentro de tu presupuesto

---

## 📊 Resumen de Archivos del Repo (Valoración)

| Archivo | Utilidad | Estado | Acción |
|---------|----------|--------|--------|
| `plazas-garaje.md` | ⭐⭐⭐⭐⭐ Canonical | ✅ Protegido | No tocar, usar como backup |
| `plazas-garaje-analisis.md` | ⭐⭐⭐⭐ Argumentos negociación | ✅ Completo | Leer antes de visita |
| `plazas-garaje-analisis-estimaciones.md` | ⭐⭐⭐ Referencia rápida | ✅ Completo | Consulta opcional |
| `plazas.json` | ⭐⭐⭐⭐⭐ Datos máquina | ✅ Actualizado | Alimenta la app |
| `index.html` | ⭐⭐⭐⭐⭐ Herramienta principal | ✅ Optimizado móvil | Usar en terreno |
| `README.md` | ⭐⭐⭐ Documentación | ⚠️ Actualizar | Añadir info agente 🚗 |

---

## ✅ Checklist Final Antes de la Visita

- [ ] Revisar top 5 plazas recomendadas en este análisis
- [ ] Abrir app en móvil y verificar que funciona
- [ ] Marcar favoritas las plazas de interés
- [ ] Exportar selección a JSON (backup)
- [ ] Probar el agente flotante 🚗 con consultas de ejemplo
- [ ] Llevar cinta métrica
- [ ] Llevar linterna (sótanos oscuros)
- [ ] Llevar libreta para notas rápidas (o usar app)
- [ ] Preparar argumentos de negociación (leer sección "Tácticas")
- [ ] Decidir presupuesto máximo por plaza según tamaño

---

**¡Buena suerte en la negociación! 🚗💰**

Recuerda: Tú tienes el dinero, ellos tienen presión por vender 32 plazas. **Tu posición es fuerte.**
