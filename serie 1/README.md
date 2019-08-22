# Serie 1

Esta serie tiene como objetivo estudiar el comportamiento de un cluster de HTCondor simulado sobre GNS3
![Alt text](overview.png?raw=true "apariencia") 



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
![Alt text](config.png?raw=true "apariencia") 

---------------------------------------------------
![Alt text](config2.png?raw=true "apariencia") 
