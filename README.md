# Laboratorio de Red Corporativa en Cisco Packet Tracer

Práctica de redes simulada en **Cisco Packet Tracer**. Diseñé una topología para una pequeña empresa dividida en áreas de trabajo, asegurando que cada departamento tenga su propio segmento de red y que todos puedan comunicarse entre sí.

## ¿Cómo está configurada la red?

- **Segmentación por VLANs:** Separé la red en tres grupos para ordenar el tráfico:
  - VLAN 10: Administración
  - VLAN 20: Operaciones
  - VLAN 30: Red Wi-Fi para Invitados
- **Enrutamiento (Router-on-a-Stick):** Usé un router Cisco 4321 con subinterfaces para comunicar las distintas VLANs a través de un switch Cisco 2960 con puertos troncales.
- **Direccionamiento automático (DHCP):** El router asigna las direcciones IP automáticamente a las computadoras de cada departamento, reservando las primeras direcciones para las puertas de enlace.
- **Punto de acceso Wi-Fi:** Conecté un Access Point en la VLAN 30 protegido con contraseña (WPA2-PSK) para los dispositivos inalámbricos.

## Pruebas realizadas
- Comprobé la conectividad enviando `ping` entre equipos de diferentes departamentos.
- Verifiqué el estado de las interfaces y tablas de red mediante comandos como `show ip interface brief` y revisión de tablas ARP.
