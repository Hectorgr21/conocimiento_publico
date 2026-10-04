# Blender · el keyframe de la cámara no se graba con el botón automático

**Fecha:** 2026-09 · **Versión:** Blender 4.4/4.5 · **Visto en:** MAD C49

## Síntoma
Con Auto Keying activado se mueve la cámara en el fotograma 48 y no aparece ningún rombo; al reproducir, la cámara no se mueve.

## Causa
El keyframe se inserta en el **objeto activo**. Si el cubo seguía activo (o nada lo estaba), el rombo fue al cubo o a ningún lado. En otros casos, Auto Keying solo graba los canales que ya tenían keyframe.

## Solución
1. Clic izquierdo sobre la cámara: borde naranja.
2. Línea azul en el fotograma 48.
3. ++g++ / ++r++ para reencuadrar.
4. Con el ratón sobre el viewport, ++i++ › **Location & Rotation**. Esto fuerza el rombo sin depender del botón automático.

## Cómo evitarlo
Antes de ++i++ decir en voz alta qué está seleccionado. Insertar el primer keyframe de cada objeto a mano; después Auto Keying sí funciona.
