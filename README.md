# Garaje
Negociación de plazas de garaje

## Web interactiva de análisis

He añadido una pequeña app estática para explorar las plazas y seleccionar lotes:

- `index.html` — interfaz que carga `plazas.json`, permite ordenar, seleccionar hasta 3 plazas, recomendar y compartir la vista mediante URL.
- `plazas.json` — datos con estimados y diferencia frente a la referencia (plaza 401 = 9.000 €).

Publicación en GitHub Pages:
1. Sube/commitea estos archivos en la rama `main`.
2. En GitHub > Settings > Pages, selecciona la rama `main` y carpeta `/ (root)`.
3. Accede a `https://<usuario>.github.io/<repositorio>/` (puede tardar unos minutos en desplegar).

Mejoras posibles:
- Añadir filtros por sótano y rango de metros.
- Permitir comparar varios lotes y exportar como propuesta de compra.

Funcionalidad añadida:
- **Agente Flotante 🚗:** Botón flotante en esquina inferior derecha con chat inteligente. Comandos:
  - `"top"` o `"mejores"` → TOP 10 mejores oportunidades (precio/m² más bajo + mayor ahorro)
  - `"plaza 401"` o `"401"` → Ficha completa con OFERTA, ahorro y gastos
  - `"calculame el precio del m2 si la plaza 401 vale 9000€"` → Cálculo interactivo
  - `"APACAAQUITUCOCHE marcar 401 favorito"` → Marca favorito
  - `"APACAAQUITUCOCHE marcar 401 vendida"` → Marca vendida
- **Guía de Visita 🗺️:** Checklist para visitas presenciales + estrategia de negociación
- Favoritos: marca una plaza como favorita (se guarda en localStorage del navegador).
- Notas: añade notas libres por plaza (ej.: "tuberías encima", "columna molesta"). Las notas se guardan en localStorage y son visibles sólo en el navegador donde se escriben.
- Marcar como VENDIDA: puedes marcar una plaza como vendida (aparece tachada y con menor opacidad). Se guarda en localStorage.
- Filtros por columna: cajas de texto bajo los encabezados para filtrado instantáneo por UR, nº plaza, precio, ubicación o metros.

 - Ocultar vendidas: activa el checkbox "Ocultar vendidas" para no mostrar las plazas ya vendidas.
 - Recomendación: botón "Recomendar mejor lote" selecciona las 3 plazas con mayor ahorro (estimado − precio) entre las plazas no vendidas.
Limitaciones:
- Favoritos y notas son locales al navegador (no se sincronizan ni suben al repositorio). Si quieres sincronizar entre dispositivos, puedo añadir export/import o integrarlo con Gist/servicio.

Export / Import de selección (móvil):
- Puedes exportar la selección actual desde el botón "Exportar selección (JSON)". Esto descarga un archivo `seleccion-plazas.json` que puedes compartir o abrir en otro dispositivo.
- En el móvil, usa "Importar selección (JSON)" para cargar el fichero descargado (o cópialo en el dispositivo). Esto restaurará la selección y la mostrará en la tabla.

Si quieres sincronización automática entre dispositivos, puedo añadir una opción para guardar las notas/selección en un Gist (requiere token) o en un backend simple.
