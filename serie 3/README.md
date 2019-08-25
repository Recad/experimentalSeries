# Serie 3

Esta serie experimental tiene como objetivo comprender el funcionamiento de Flocking en el contexto de 
la red institucional de la Universidad del Valle. 
Más precisamente estudiar cuales son los factores de la red que afectan su funcionamiento.
![Alt text](image2.png?raw=true "apariencia") 


## Consideraciones

Para ejecutar de forma correcta la simulación se requiere que en cada nodo de HTCondor se realicen configuraciones,
algunas de ellas se puden realizar sobre la interfaz de GNS3 otras es preferible realizarlos sobre en nodo en ejecución 
y recargar el nodo despues de dicha configuración.

Los parametros que se pueden configurar desde la interfaz de GNS son:
- Definir las varibles de ambiente master y shared_port.
- Modificar el archivo /etc/hosts para añadir las direciones correspondientes a los recursos.
- Definir la configuración de red de cada nodo. 

En la serie 1 se evidencia mejor la configuración anterior.

## Recursos

Los recursos necesarios los encontraras en: https://hub.docker.com/u/recad

### Configuraciones
Otra configuración importante es el archivo /etc/condor/condor_config.local en el cual tenemos que 
definir FLOCK_TO y FLOCK_FROM para ambos nodos mestro.

A nivel del Firewall se reliza una Destination NAT y Source NAT con el recurso cancerbero con la IP "publica" 192.168.131.72, esta configuración se puede evidenciar 
en la siguiente imagen:

![Alt text](firewall.png?raw=true "firewall") 
