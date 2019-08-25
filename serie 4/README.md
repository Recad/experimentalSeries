# Serie 4

 Esta serie experimental tiene como propósito probar la efectividad del TCP Forwarding Host 
 como configuración que permita evitar que el Pool de recursos se presente con IPs privadas 
 a otros Pools con los que desea compartir recursos.
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

Adicional a lo anterior se debe definir la configuración de Forwarding Host para los nodos maestro y nodos de ejecución.

### Nodo Mestro Forwarding Host
```bash
FILESYSTEM_DOMAIN = $(FULL_HOSTNAME)
TCP_FORWARDING_HOST = 192.168.131.72
# Node IP inside NAT/IP del nodo en el NAT
PRIVATE_NETWORK_INTERFACE = 172.17.9.3 
PRIVATE_NETWORK_NAME = eisc.univalle.edu.co
```
La configuración anterior aplica tambien para los nodos de ejecución, solo se varia PRIVATE_NETWORK_INTERFACE 
colocando la direccion correspondiente a cada nodo

La configuración del Firewall no varia respecto a la serie 3.


