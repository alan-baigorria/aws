Actualizar el sistema
```
sudo apt update && sudo apt upgrade -y
```

Instalar Java 21
```
sudo apt install -y openjdk-21-jdk
```
Crear carpeta del servidor
```
mkdir minecraft
cd minecraft
```
Descargar Paper
```
curl -o paper.jar https://fill-data.papermc.io/v1/objects/d4f897545310f31e623d9680786b25dd20a9989e139db050d1aacf81ecafd05c/paper-1.21.10-113.jar
```
_*aca va la ultima version_

Aceptar EULA
```
echo "eula=true" > eula.txt
```

USAR SCREEN PARA CORRERLO EN SEGUNDO PLANO
Instalar screen
```
sudo apt install -y screen
```

Crear sesión screen
```
screen -S mc
```

Iniciar el servidor dentro del screen
```
java -Xms512M -Xmx1700M -jar paper.jar nogui
```
_* este es para t3.small, si pagan pueden meterle más ram para 2-4 sin mods sirve*_

Salir del screen SIN apagar el servidor (teclas)
```
Presioná:
CTRL + A + D
```

VOLVER A ENTRAR AL SERVER
Reanudar la sesión screen
```
screen -r mc
```

APAGAR EL SERVER
Comando dentro de screen
```
stop

```
