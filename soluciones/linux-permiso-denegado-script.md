# Linux · "Permiso denegado" al ejecutar un script

**Versión:** bash · **Visto en:** SO G060201

## Síntoma
`./script.sh` responde `bash: ./script.sh: Permiso denegado`.

## Causa
El archivo no tiene permiso de ejecución (al crearlo o al copiarlo desde Windows o una USB).

## Solución
1. `chmod +x script.sh`
2. Si está en una USB FAT32/exFAT, ejecútalo con `bash script.sh` (ese sistema de archivos no guarda permisos).
3. Si aparece `/bin/bash^M: intérprete erróneo`, tiene finales de línea de Windows: `sed -i 's/\r$//' script.sh`.
