# devsecops-replica

Corridas de réplica del flujo reutilizable `ManuelArango1229/devsecops-engine-`
sobre los casos de estudio del artículo de
Arango, Castaño y Delgado. Cada archivo de `.github/workflows/` lanza un caso a
mano con los mismos parámetros que usó el repositorio original.

Los reportes de cada corrida se bajan a
`papers-project/papers/security-arango-castano/data/`.

El flujo se toma de la bifurcación `cardel/devsecops-engine-`, rama
`replica-trivy-keyring`, que difiere del commit `1aeabed` del original en un
solo paso: la instalación de Trivy registra la llave en un keyring, porque el
ejecutor `ubuntu-latest` ya no trae `apt-key`. Los guiones del motor se siguen
clonando del repositorio original.
