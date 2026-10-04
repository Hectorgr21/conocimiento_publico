# Blender · el zoom (Focal Length) se aplica a toda la animación

**Fecha:** 2026-09 · **Versión:** Blender 4.4/4.5 · **Visto en:** MAD C49

## Síntoma
Se cambia Focal Length de 50 a 100 mm en el fotograma 80 y el zoom se ve igual en todos los fotogramas.

## Causa
Un solo keyframe no define un cambio. Sin un rombo anterior con el valor 50, Blender no sabe en qué momento debe empezar a interpolar y toma 100 como valor constante.

## Solución
1. Fotograma 48: Focal Length **50 mm**, ratón sobre el campo, ++i++ (el campo se pone amarillo).
2. Fotograma 80: Focal Length **100 mm**, ++i++ (o Auto Keying lo graba solo).
3. Reproducir: de 48 a 80 hace zoom suave.

## Cómo evitarlo
Regla de clase: «un rombo guarda; dos rombos animan».
