## 1. Gestión de Paquetes
- **Actualizar Repositorios:**
  ```bash
  sudo apt update
  ```

- **Actualizar Paquetes Instalados:**
  ```bash
  sudo apt upgrade
  ```

- **Instalar Nuevo Paquete:**
  ```bash
  sudo apt install nombre_paquete
  ```

- **Eliminar Paquete:**
  ```bash
  sudo apt remove nombre_paquete
  ```

- **Eliminar Paquete con Configuración:**
  ```bash
  sudo apt purge nombre_paquete
  ```

## 2. Gestión de Archivos y Directorios
- **Navegar entre Directorios:**
  ```bash
  cd ruta_del_directorio
  ```

- **Listar Contenido de un Directorio:**
  ```bash
  ls
  ```

- **Crear Nuevo Directorio:**
  ```bash
  mkdir nombre_directorio
  ```

- **Eliminar Directorio Vacío:**
  ```bash
  rmdir nombre_directorio
  ```

- **Eliminar Directorio y su Contenido:**
  ```bash
  rm -r nombre_directorio
  ```

## 3. Gestión de Usuarios y Permisos
- **Crear Nuevo Usuario:**
  ```bash
  sudo adduser nombre_usuario
  ```

- **Cambiar Contraseña de Usuario:**
  ```bash
  sudo passwd nombre_usuario
  ```

- **Cambiar Propietario de Archivo/Directorio:**
  ```bash
  sudo chown nuevo_propietario archivo_directorio
  ```

- **Cambiar Permisos de Archivo/Directorio:**
  ```bash
  sudo chmod permisos archivo_directorio
  ```

## 4. Redes y Conectividad
- **Ver Configuración de Red:**
  ```bash
  ip addr show
  ```

- **Reiniciar Servicio de Red:**
  ```bash
  sudo systemctl restart networking
  ```

- **Verificar Conexión a Internet:**
  ```bash
  ping ejemplo.com
  ```

## 5. Tareas de Administración
- **Reiniciar el Sistema:**
  ```bash
  sudo reboot
  ```

- **Apagar el Sistema:**
  ```bash
  sudo shutdown now
  ```

- **Verificar Uso de Recursos del Sistema:**
  ```bash
  top
  ```

## 6. Gestión de Procesos
- **Listar Procesos en Ejecución:**
  ```bash
  ps aux
  ```

- **Matar un Proceso por ID:**
  ```bash
  sudo kill ID_proceso
  ```

## 7. Archivos de Configuración
- **Editar Archivo de Configuración con Nano:**
  ```bash
  sudo nano archivo_configuracion
  ```

- **Editar Archivo de Configuración con Vim:**
  ```bash
  sudo vim archivo_configuracion
  ```

## 8. Seguridad y Actualizaciones
- **Actualizar Sistema:**
  ```bash
  sudo apt update && sudo apt upgrade
  ```

- **Instalar Actualizaciones de Seguridad:**
  ```bash
  sudo apt install unattended-upgrades
  ```

## 9. Logs y Registro de Eventos
- **Ver Registro de Arranque:**
  ```bash
  dmesg
  ```

- **Ver Registro de Sistema:**
  ```bash
  journalctl
  ```


```bash
sudo apt 
```

### 10. Instalar/Desinstalar archivos .deb

Los archivos de paquetes asociados con kubuntu tienen todos el sufijo _.deb_ debido a la estrecha relación de Kubuntu con la distribucíon de GNU/Linux llamada Debian. Usted podrá descargar e instalar archivos de paquetes _.deb_. Para ello, necesitará permisos de administrador (véase [“Usuario "root" y sudo”](https://help.ubuntu.com/kubuntu/desktopguide/es/root-and-sudo.html "Usuario "root" y sudo")).

1. Para instalar un .deb, simplemente haga click Derecho con el ratón sobre el archivo .deb, y elija Menú de Paquetes Kubuntu->Instalar Paquete.
2. Como alternativa, también puede instalar un archivo .deb abriendo una terminal y escribiendo:
```bash
sudo dpkg -i package_file.deb
```

3. Para desinstalar un archivo .deb, elimínelo con **Adept**, o escriba:

```bash
sudo apt-get remove nombre_del_paquete
```
