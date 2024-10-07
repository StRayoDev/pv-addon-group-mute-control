# pv-addon-group-mute-control
**pv-addon-group-mute-control** es un plugin para Minecraft (versión 1.20.1) basado en **Spigot** que facilita la gestión del chat de voz en **Plasmo Voice**, permitiendo habilitar o deshabilitar el permiso `pv.activation.proximity` para un grupo específico de **LuckPerms** mediante comandos sencillos.

### Características:
- **Comando principal**: `/pv`
  - **`/pv toggle`**: Alterna el permiso `pv.activation.proximity` para un grupo de **LuckPerms** definido en la configuración. Ideal para eventos o situaciones globales donde se requiera silenciar o activar el chat de voz.
  - **`/pv set <grupo>`**: Establece un nuevo grupo de **LuckPerms** para gestionar el permiso en futuros comandos.
  - **`/pv reload`**: Recarga la configuración del plugin sin necesidad de reiniciar el servidor.

### Requisitos:
- **Spigot** o **Paper** 1.20.1
- **LuckPerms** (para la gestión de grupos y permisos)
- **Plasmo Voice** (para la integración con el chat de voz)

### Instalación:
1. Descarga el archivo JAR desde la sección de **releases** del repositorio.
2. Coloca el archivo JAR en la carpeta `plugins` de tu servidor.
3. Inicia o reinicia el servidor para cargar el plugin.
4. Configura el plugin modificando el archivo `config.yml` para establecer el grupo de **LuckPerms** que desees controlar.
5. Asegúrate de que los jugadores que usarán el comando tengan el permiso `groupmutecontrol.use`.

### Uso:
- **`/pv toggle`**: Alterna la activación del chat de voz para el grupo configurado en el archivo `config.yml`. Si el permiso está activado, se desactivará, y viceversa.
- **`/pv set <grupo>`**: Cambia el grupo objetivo para aplicar los cambios de permisos. Ejemplo: `/pv set admins` para gestionar el grupo "admins".
- **`/pv reload`**: Recarga la configuración del plugin para aplicar cambios realizados en el archivo `config.yml`.

### Configuración:
El archivo de configuración (`config.yml`) incluye el nombre del grupo de **LuckPerms** al que se aplicarán los cambios. Si no se especifica un grupo, se usará el grupo predeterminado `"default"`.

```yaml
# Nombre del grupo de LuckPerms que controlará el permiso de activación del chat de voz
group: "default"
```

### Permisos:
- `groupmutecontrol.use`: Permite el uso de los comandos `/pv toggle`, `/pv set`, y `/pv reload`.
