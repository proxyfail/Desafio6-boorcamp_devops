# Desafio6-ansible-devops
Este proyecto tiene como objetivo implementar un playbook de Ansible y roles para desplegar un sitio web de WordPress en una instancia EC2 de AWS Academy.

## Objetivo
El objetivo principal es modularizar el proyecto de gestión de configuración utilizando Ansible, instalando y configurando PHP y MySQL en una instancia EC2.

## Estructura del Proyecto
El proyecto se organiza de la siguiente manera:

- **ansible.cfg**: Configuración de Ansible.
- **inventory.ini**: Inventario de hosts que Ansible gestionará.
- **playbook.yml**: Playbook principal que orquesta la instalación de PHP y MySQL.
- **roles/**: Carpeta que contiene los roles para PHP y MySQL.
  - **mysql/**: Rol para la instalación y configuración de MySQL.
  - **php/**: Rol para la instalación y configuración de PHP.
- **docs/**: Documentación adicional, incluyendo diagramas y evidencia de pruebas.

## Comando Tree de Linux:
Desafio6-boorcamp_devops/
├── ansible.cfg
├── inventory.ini
├── playbook.yml
├── README.md
├── docs
│   ├── Diagrama-de-Arquitectura-de-Alto-Nivel.md
│   └── Evidencia-de-Pruebas-para-el-Despl.md
└── roles
    ├── mysql
    │   ├── defaults
    │   │   └── main.yml
    │   ├── handlers
    │   │   └── main.yml
    │   ├── tasks
    │   │   └── main.yml
    │   ├── templates
    │   └── vars
    │       └── main.yml
    └── php
        ├── defaults
        │   └── main.yml
        ├── handlers
        │   └── main.yml
        ├── tasks
        │   └── main.yml
        ├── templates
        └── vars
            └── main.yml

## Requisitos
1. Utilizar un Bastion de AWS Academy.
2. Identificar y crear posibles variables reutilizables.
3. Crear un archivo playbook y roles específicos para PHP y MySQL.
4. Testar y validar que todo funciona correctamente.

## Entregables
1. Código fuente del playbook de Ansible publicado en un repositorio de GitHub.
2. Guía detallada de cómo utilizar el rol, publicada en este archivo README.md.
3. Evidencia de las pruebas con resultados exitosos.

## Instrucciones de Uso
1. Clona el repositorio en tu máquina local.
2. Configura el archivo `inventory.ini` con los detalles de tu instancia EC2.
3. Ejecuta el playbook utilizando el comando:
   ```
   ansible-playbook -i inventory.ini playbook.yml
   ```
4. Verifica que PHP y MySQL estén instalados y funcionando correctamente en la instancia EC2.

## Documentación Adicional
- **docs/high-level-diagram.md**: Diagrama de alto nivel de la arquitectura del proyecto.
- **docs/test-evidence.md**: Evidencia de las pruebas realizadas y resultados obtenidos.
