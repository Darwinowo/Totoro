![image](https://github.com/weskerty/TheMysticMOD/assets/82781997/ffc6bf43-938e-4349-90fe-638c01bb1799)

## ⬇️ Descargar Termux
Descaga la version compatible con tu Telefono de Aqui: [Termux Github](https://github.com/termux/termux-app/releases)

Suele decir ""termux-app_vxxx-+apt-android-7-github-debug_universal.apk"" 
Android 7 se refiere a que funciona con Android 7 y Superior, hay otra version para Android 7 e Inferior llamado Android5. Tambien puedes usar [Termux Monect](https://github.com/KitsunedFox/termux-monet) 
> [!CAUTION]
> JAMAS INSTALES TERMUX DE GOOGLE PLAY, TIENE DEMASIADAS INCOMPATIBILIDADES.

## ⬇️ Instalar Requerimientos
Lamentablemente Termux no es compatible con algunos modulos de nodejs que requiere el bot, asi que Instalaremos una Instancia Linux Debian con Estos comandos:
Deberas entrar en Termux y Pegar cada Linea.

```sh
pkg install proot-distro -y
```
Luego:

```sh
proot-distro install debian -y
```
Esperas un Rato dependiendo de la velocidad de tu internet...

## 🖥️ Iniciar Debian

```sh
proot-distro login debian
```

## 🐧 Ahora puedes Instalar el Bot normalmente con los mismos pasos que Linux Debian y Derivados.


```sh
apt install git curl wget ffmpeg imagemagick -y
```

```sh
curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh
sudo -E bash nodesource_setup.sh
sudo apt-get install -y nodejs
```

```sh
git clone https://github.com/BrunoSobrino/TheMystic-Bot-MD.git mystic
cd mystic
npm install
```

## ⚙️Preferencias del Bot
Debes ajustar el `config.js` para agregar el numero del bot, tus administradores del bot, el pais de la fecha y clima y el nombre del paquete de stickers etc.
Desde Termux es `nano config.js` Editas lo que necesites, para guardar es Ctrl+O luego Enter. Para Salir de Nano es Ctrl+X.
En Caso de que tengas Root o una version inferior a Android 11 puedes ir a ver los archivos de Termux y ajustarlos desde el explorador de Archivos de Android en la carpeta /data/data/com.termux/files/home/ 

## 🟢 Iniciar Bot
Una vez que hayas ajustado todo, inicia el bot con:
```sh
npm start .
```

## 🔌 Mantener Abierto Termux
El bot funcionara mientras Termux este abierto y con Conexion a Internet.
Permite a Termux ejecutarse sin Restricciones ni Optimizaciones de bateria. 
Activa el WakeLock desde la Notificacion de Termux.
> [!IMPORTANT]
>Android 12 y Superior tienen limitaciones de ejecucion, unicamente se puede Resolver con ADB, Root o Custom ROM.

## 💡 Evitar cerrado Forzoso (Opcional)
En caso de que termux se te cierre a cada rato, puedes seguir estos pasos OPCIONALES.

- ADB desde Terminal en PC:
```
adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
adb shell settings put global settings_enable_monitor_phantom_procs false
```

#### Con ROOT:
- On Termux (or any Terminal Emulator), paste the following commands on the following order:
```
su -c /system/bin/device_config set_sync_disabled_for_tests persistent
su -c /system/bin/device_config put activity_manager max_phantom_processes 2147483647
su -c setprop persist.sys.fflag.override.settings_enable_monitor_phantom_procs false
```

#### O Instalando un Modulo de Magisk

[![](https://img.shields.io/static/v1?message=LetTheGhostsOut.zip&logo=magisk&labelColor=5c5c5c&color=00af9c&logoColor=white&label=%20&style=for-the-badge)](https://raw.githubusercontent.com/HardcodedCat/termux-monet/master/ppr/PhantomProcessRetainer-main.zip)


[Fuente Termux Monect](https://github.com/KitsunedFox/termux-monet/blob/master/README.md)

## ↪️ Volver a iniciar en caso de Cierre
 Abris termux y Pega esto:
 
 ```
    proot-distro login debian
  ```

```
    cd mystic
	npm start 
 ```
## Servidor Eco-Friendly
Puedes utilizar un telefono antiguo y Automatizarlo con Tasker como es mi caso.
Utilizo un Telefono Roto con un Panel Solar para Mantener el bot para [Toda esta Comunidad](https://chat.whatsapp.com/JtrXf1pGoewLlX5Ww2VXDs).

<a href="https://www.hmd.com/en_int/nokia-g-20/environmental-profile"><img src="https://github.com/weskerty/TheMysticMOD/assets/82781997/497b42f7-7317-42b4-bf10-9ab107be313a" width="400" height="300" alt="NokiaG20"/> </a>
