# Serie 2

Esta serie tiene como objetivo estudiar el comportamiento del Flocking en segmentos de red diferentes.
![Alt text](image14.png?raw=true "apariencia") 


## Consideraciones

Para ejecutar de forma correcta la simulación se requiere que en cada nodo de HTCondor se realicen configuraciones,
algunas de ellas se puden realizar sobre la interfaz de GNS3 otras es preferible realizarlos sobre en nodo en ejecución 
y recargar el nodo despues de dicha configuración.

Los parametros que se pueden configurar desde la interfaz de GNS son:
- Definir las varibles de ambiente master y shared_port.
- Modificar el archivo /etc/hosts para añadir las direciones correspondientes a los recursos.
- Definir la configuración de red de cada nodo. 

## Recursos

Los recursos necesarios los encontraras en: https://hub.docker.com/u/recad

### Configuraciones
Las configuraciones pueden ser iguales a las descritas en la serie uno. La unica diferencia es la configuración del Router
para definir 2 segmentos de red diferentes. se uso router de la serie c7200.

Otra configuración importante es el archivo /etc/condor/condor_config.local en el cual tenemos que 
definir FLOCK_TO y FLOCK_FROM para ambos nodos mestro
