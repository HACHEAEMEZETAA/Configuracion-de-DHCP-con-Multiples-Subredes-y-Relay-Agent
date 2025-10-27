# Proyecto: Configuración de DHCP con Múltiples Subredes y Relay Agent 🌐

Este proyecto implementa y verifica una solución de red avanzada utilizando el servidor **ISC-DHCP-SERVER** en un entorno de máquinas virtuales, demostrando la asignación de direcciones IP a través de múltiples segmentos de red local y remota.

---

## Objetivos Clave

* **Enrutamiento Centralizado:** Configuración del Servidor DHCP como un router multi-homed para gestionar el tráfico y las concesiones de dos redes conectadas directamente (una local y una de tránsito).
* **Agente de Retransmisión (Relay Agent):** Despliegue del servicio `isc-dhcp-relay` en una máquina router separada para interconectar una red remota con el Servidor DHCP central.
* **Rutas Estáticas Esenciales:** Implementación de rutas estáticas en ambos routers para asegurar el tráfico de retorno y la conectividad completa entre todos los segmentos de la red.
* **Monitorización del Protocolo:** Verificación del proceso de concesión DHCP (**DORA**) utilizando la herramienta `dhcpdump`, demostrando cómo el Relay Agent convierte los mensajes de descubrimiento (`DHCPDISCOVER`) de *broadcast* a *unicast*.

---

## Resultado

Se estableció la conectividad total (`ping`) entre todos los clientes de las diferentes subredes y se validó el funcionamiento del Agente de Retransmisión, permitiendo a los clientes remotos obtener su configuración IP desde un servidor que reside en un segmento de red distinto.
