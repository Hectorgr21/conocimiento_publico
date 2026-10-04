# Mixamo → Blender · el personaje importado mide 100 m

**Versión:** Blender 4.x · **Visto en:** AAEV proyecto video mix, AAEV T2

## Causa
Mixamo exporta en centímetros; el FBX llega con escala 100.

## Solución
Seleccionar armature y malla › ++n++ › Scale 0.01 en los tres ejes › ++ctrl+a++ › **All Transforms**. Al importar, activar **Automatic Bone Orientation**.
