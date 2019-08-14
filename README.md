# **Pipes and Filters design pattern**
 
## ¿En qué consiste?

Consiste en un conjunto de tuberías (pipes) y filtros (filters), cada filtro es independiente de los demás. El sistema puede ser tan complejo como sea necesario. Es decir, que a un filtro le pueden entrar y salir cuantas tuberías sean necesarias.

![](https://miro.medium.com/max/700/1*qikehZcDhhl_wWsqeI_nvg.png)

## Cuando usarlo
Es recomendable usarlo cuando se tiene una estructura compleja que procesa una gran cantidad de datos. Se debe dividir este gran proceso en subprocesos (filtros) y cada subproceso se conecta con otros subprocesos interactuando mediante las salidas y entradas de cada filtro (tuberías).

 ## Ventajas:
 - Se tiene una estructura mucho más flexible y modular, lo que otorga un poco más de control.
- Mejoras en el rendimiento, debido a que se puede aplicar paralelismo a los filtros, ya que estos no necesariamente trabajan secuencialmente (Sistemas distribuidos).
- Mayor escalabilidad y reusabilidad.

## Desventajas
- Si un filtro procesa muchas entradas (le entran muchas tuberías) necesitaría un buffer grande.
- Si los filtros que se comunican entre sí no “hablan” el mismo lenguaje el sistema tiende a ser ineficiente, ya que la “traducción” absorbe mucho tiempo.

## Más Información:
- https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013
- http://www.dossier-andreas.net/software_architecture/pipe_and_filter.html
- https://docs.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters
