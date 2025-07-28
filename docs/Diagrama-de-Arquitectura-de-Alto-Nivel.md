# Diagrama de Arquitectura de Alto Nivel

Este documento proporciona una visión general de alto nivel sobre la arquitectura y los componentes involucrados en el despliegue de un sitio WordPress utilizando Ansible en una instancia EC2.

## Componentes

1. **Instancia EC2**
   - El servidor virtual donde se alojará el sitio WordPress.
   - Ejecuta Ubuntu como sistema operativo.

2. **Ansible**
   - Herramienta de gestión de configuración utilizada para automatizar el proceso de despliegue.
   - Utiliza playbooks y roles para gestionar la instalación de servicios.

3. **Roles**
   - **Rol de PHP**
     - Instala PHP y sus extensiones necesarias.
     - Configura los ajustes de PHP para un rendimiento óptimo.
   - **Rol de MySQL**
     - Instala el servidor MySQL.
     - Configura la base de datos para WordPress.

4. **Bastion Host**
   - Proporciona acceso seguro a la instancia EC2.
   - Actúa como puerta de enlace para conexiones SSH.

## Flujo de Despliegue

1. **Acceso al Bastion Host**
   - Conéctate al Bastion Host usando SSH con la clave PEM proporcionada.

2. **Ejecución del Playbook de Ansible**
   - Ejecuta el playbook de Ansible para desplegar los roles de PHP y MySQL en la instancia EC2.

3. **Instalación de Servicios**
   - Ansible instala y configura PHP y MySQL en la instancia EC2.

4. **Configuración de WordPress**
   - Después de instalar los servicios, WordPress puede configurarse para conectarse a la base de datos MySQL.

## Diagrama

[Insertar aquí el diagrama de arquitectura de alto nivel]

Este diagrama debe ilustrar las relaciones entre la instancia EC2, Ansible, los roles de PHP y MySQL, y el Bastion Host.