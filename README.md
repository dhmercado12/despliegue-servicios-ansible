# Task 3 - Despliegue de servicios con Ansible

## Entorno
- Sistema operativo remoto: openSUSE Leap 16.0
- Herramienta de automatización: Ansible
- Host remoto: suse16B

## Servicios desplegados
- Apache y PHP
- phpMyAdmin
- MariaDB
- Samba
- FTP mediante vsftpd

## Estructura
- inventory/: inventario de hosts
- roles/: roles para desplegar y configurar los servicios
- group_vars/servidores/vault.yml: variables protegidas con Ansible Vault
- site.yml: playbook principal

## Ejecución
Desde el directorio del proyecto:

    ansible-playbook site.yml -K --ask-vault-pass

El comando solicita las contraseñas necesarias durante la ejecución.
No almacenar contraseñas en texto plano en el repositorio.
