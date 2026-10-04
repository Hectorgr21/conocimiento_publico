# Blender · el panel Bloom de Eevee ya no existe (4.2 en adelante)

**Versión:** Blender 4.2+ · **Visto en:** AAEV T4

## Síntoma
Los tutoriales dicen Render › Bloom; en 4.2+ no aparece.

## Causa
Eevee Next eliminó Bloom. El resplandor se hace en el compositor.

## Solución
Compositing › Use Nodes › nodo **Glare** (Fog Glow o Bloom, Threshold 1.0, Size 7–8) entre Render Layers y Composite. En gráficos integrados, Render › Performance › Compositor › Device **CPU**.
