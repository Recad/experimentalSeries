# Serie 5

Esta serie experimental tiene como objetivo observar el comportamiento del 
Flocking de HTCondor sobre redes superpuestas basadas en VPN.

![Alt text](image2.png?raw=true "apariencia") 


## Consideraciones

Para ejecutar de forma correcta la simulación se requiere que en cada nodo de HTCondor se realicen configuraciones,
algunas de ellas se puden realizar sobre la interfaz de GNS3 otras es preferible realizarlos sobre en nodo en ejecución 
y recargar el nodo despues de dicha configuración.

Los parametros que se pueden configurar desde la interfaz de GNS son:
- Definir las varibles de ambiente master y shared_port.
- Modificar el archivo /etc/hosts para añadir las direciones correspondientes a los recursos.
- Definir la configuración de red de cada nodo (considerando el uso de OpenVPN). 

En la serie 1 se evidencia mejor la configuración anterior.

### Sobre OpenVPN
Este aspecto de la simulación requiere de mucha atención. para configurar OpenVPN de forma correcta se debe
definir cual sera el servidor y cuales los clientes, realizar la configuración correspondiente de los certificados.
Para tener una idea mas clara se recomeinda leer el articulo disponible en 
https://www.digitalocean.com/community/tutorials/como-configurar-un-servidor-openvpn-en-ubuntu-16-04-es

Otro aspecto importante es que para estudiar el Flocking con OpenVPN es recomendable definir todos los aspectos de configuración de
HTCondor a nivel de red con las direcciones que define OpenVPN. De esta manera se evitan otras configuraciones que no se estudian
en esta serie experimental. Sin embargo si desea estudiar este aspecto se recomeinda estudiar el uso de 
PRIVATE_NETWORK_INTERFACE y PRIVATE_NETWORK_NAME como configuraciones de los nodos de un Pool

## Recursos

Los recursos necesarios los encontraras en: https://hub.docker.com/u/recad

Las imagenes de HTCondor con OpenVPN ya poseen la herramienta para configurar los certificados








