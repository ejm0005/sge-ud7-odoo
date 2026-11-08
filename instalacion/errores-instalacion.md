# Errores en la instalación y prevenciones
## Errores
Dado a que no he encontrado ningún problema o error en mi proceso de instalación de Odoo, he decidido documentar en una tabla el fallo más común, que es el error de puerto ocupado:  
| Error | Causa Raíz | Procedimiento | Fuente Consultada |
| :--- | :--- | :--- | :--- |
| Fallo al iniciar el servidor indicando que el puerto `8069` está ocupado. | El puerto predeterminado de Odoo (el cual por defecto es `8069`) ya está siendo utilizado por otra instancia en el equipo. | 1. Identificar que pdoceso está ocupando el puerto con `netstat -ano \| findstr 8069`.<br>2. Finalizar el proceso que ocupa el puerto, y si no se puede, cambiar el puerto predeterminado de Odoo en el archivo de configuración `odoo.conf` modificando el parámetro `xmlrpc_port`, indicando un puerto que esté completamente libre. | [Documentación Oficial de Odoo - Configuración del Servidor](https://www.odoo.com/documentation/) |  

## Prevenciones realizadas
* Verificar mediante comandos de Powershell que los puertos 8069 (Odoo) y el 5432 (PostgreSQL) se encuentran totalmente disponibles antes de ejecutar la instalación
* Asegurar que las dependencias de Python y librerías de sistema instaladas en mi equipo cumplen con los requisitos técnicos oficiales de la versión que se va a instalar (en este caso Odoo Community versión 19)