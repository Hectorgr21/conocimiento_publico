# Proceso vs. hilo

- **Proceso:** programa en ejecución con su propio espacio de memoria, archivos abiertos y PID.
- **Hilo:** unidad de ejecución dentro de un proceso; comparte la memoria con los demás hilos del mismo proceso.
- **Consecuencia:** crear hilos es más barato y comunicarlos es más fácil, pero un error de memoria en un hilo tumba todo el proceso.
