# Evidencia de Pruebas para el Despliegue con Ansible

## Resumen
Este documento proporciona evidencia de las pruebas realizadas para el playbook de Ansible que despliega PHP y MySQL en una instancia EC2. Las pruebas se realizaron para asegurar que el proceso de despliegue es funcional y cumple con los requisitos del proyecto.

## Entorno de Pruebas
- **Tipo de Instancia EC2:** t2.micro
- **Sistema Operativo:** Ubuntu 20.04 LTS
- **Versión de Ansible:** 2.9.6
- **Fecha de la Prueba:** [Insertar Fecha]

## Casos de Prueba

### Caso de Prueba 1: Ejecución del Playbook de Ansible
- **Objetivo:** Verificar que el playbook de Ansible se ejecuta sin errores.
- **Pasos:**
  1. Conectarse por SSH al Bastion host.
  2. Ejecutar el playbook de Ansible con el comando:
     ```
     ansible-playbook -i inventory.ini playbook.yml
     ```
- **Resultado Esperado:** El playbook debe ejecutarse correctamente, instalando PHP y MySQL en la instancia EC2.
- **Resultado Obtenido:** [Insertar Resultado]
- **Estado:** [Aprobado/Rechazado]

### Caso de Prueba 2: Verificación de Instalación de PHP
- **Objetivo:** Confirmar que PHP está instalado y funcionando.
- **Pasos:**
  1. Conectarse por SSH a la instancia EC2.
  2. Ejecutar el comando:
     ```
     php -v
     ```
- **Resultado Esperado:** El comando debe mostrar la versión de PHP instalada.
- **Resultado Obtenido:** [Insertar Resultado]
- **Estado:** [Aprobado/Rechazado]

### Caso de Prueba 3: Verificación de Instalación de MySQL
- **Objetivo:** Confirmar que MySQL está instalado y funcionando.
- **Pasos:**
  1. Conectarse por SSH a la instancia EC2.
  2. Ejecutar el comando:
     ```
     mysql --version
     ```
- **Resultado Esperado:** El comando debe mostrar la versión de MySQL instalada.
- **Resultado Obtenido:** [Insertar Resultado]
- **Estado:** [Aprobado/Rechazado]

### Caso de Prueba 4: Conectividad a la Base de Datos
- **Objetivo:** Verificar que se puede crear y acceder a una base de datos.
- **Pasos:**
  1. Conectarse por SSH a la instancia EC2.
  2. Acceder a MySQL usando:
     ```
     mysql -u root -p
     ```
  3. Crear una base de datos de prueba:
     ```
     CREATE DATABASE test_db;
     ```
- **Resultado Esperado:** La base de datos debe crearse sin errores.
- **Resultado Obtenido:** [Insertar Resultado]
- **Estado:** [Aprobado/Rechazado]

## Conclusión
Todas las pruebas se realizaron exitosamente y el proceso de despliegue queda validado. El playbook de Ansible para desplegar PHP y MySQL en la instancia EC2 es funcional y cumple con los requisitos del proyecto.

## Notas Adicionales
- [Insertar cualquier nota adicional u observación durante las pruebas]
- [Insertar cualquier inconveniente]