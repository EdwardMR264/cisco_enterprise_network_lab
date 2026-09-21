# Red Corporativa Multi-VLAN y Servicios Locales
Laboratorio practico en Cisco Packet Tracer: Multi-VLAN, Router-on-a-stick y DHCP 

# Arquitectura de Red
**Router central:** Cisco 4321 configurado con subinterfaces 802.1Q (Router-on-a-Stick)
**Conmutación:** Switches Cisco Catalyst 2960 con enlaces troncales y puertos de acceso asignados por departamento
**Segmentación por VLAN:**
  **VLAN 10 (Administración):** Segmento administrativo (`192.168.10.0/24`).
  **VLAN 20 (Operaciones):** Estaciones de trabajo operativas (`192.168.20.0/24`).
  **VLAN 30 (Invitados / Wi-Fi):** Red inalámbrica (`192.168.30.0/24`).

## Servicios y Conectividad
**Enrutamiento Inter-VLAN:** Comunicación fluida entre los tres segmentos mediante subinterfaces virtuales en el router.
**DHCP en Router:** Asignación automática de direccionamiento IP por subred con exclusión de direcciones para gateways.
**WLAN Corporativa:** Access Point integrado en la VLAN 30 con cifrado y autenticación **WPA2-PSK**.

## Pruebas y Diagnóstico
Verificación de tablas ARP en computadoras y switches.
Validación de tablas de enrutamiento y estado de subinterfaces (`show ip interface brief`).
Pruebas de conectividad inter-VLAN de extremo a extremo mediante ICMP (`ping`).
