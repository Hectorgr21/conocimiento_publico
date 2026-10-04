# Docker · "port is already allocated"

**Versión:** Docker 24+ · **Visto en:** Infra Web G070701

## Síntoma
`docker run -p 8080:80 ...` falla con `Bind for 0.0.0.0:8080 failed: port is already allocated`.

## Causa
Otro contenedor o un servicio local ya usa ese puerto en el host.

## Solución
1. Ver quién lo usa: `docker ps --filter "publish=8080"` o `sudo ss -ltnp | grep 8080`.
2. Detener el contenedor viejo (`docker stop <id>`) o cambiar el puerto del host: `-p 8081:80`.
