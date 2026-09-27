# SCORBOT ER III · Consola de mando v70

Aplicación web para gobernar el brazo robótico **SCORBOT ER III** con su controladora original a través del puerto serie RS-232, directamente desde el navegador. Sustituye al software original (SCORBASE) y funciona en un único archivo HTML, sin instalación.

Desarrollada como parte de la práctica *Diagnosis y mantenimiento correctivo · SCORBOT ER III*.

**by monchopro**

## Probar en línea

👉 **https://TU-USUARIO.github.io/scorbot-er3-pendant/**

Sin brazo conectado puede probarse completa en **modo simulación**, con la controladora virtual y la vista 3D.

## Descargar

La versión oficial se descarga desde la sección **[Releases](../../releases)** de este repositorio: archivo `scorbot-er3-pendant-v70.html`. Basta con abrirlo en el navegador.

## Verificar que el archivo es el original (MD5)

Firma MD5 de la versión v70:

```
da7783c51a7756d260844908ad759d6c
```

Comprueba tu copia descargada y compara el resultado con la firma anterior. Si coincide carácter a carácter, el archivo no ha sido modificado.

**Windows** (símbolo del sistema, en la carpeta de descargas):

```
certutil -hashfile scorbot-er3-pendant-v70.html MD5
```

**Windows** (PowerShell):

```
Get-FileHash .\scorbot-er3-pendant-v70.html -Algorithm MD5
```

**Linux / macOS**:

```
md5sum -c MD5SUMS.txt
```

> La firma MD5 detecta cualquier cambio en el archivo, accidental o no. Verifica siempre sobre el archivo descargado de *Releases*: guardar la página desde el navegador («Guardar como») puede alterar el contenido y cambiar la firma.

## Requisitos

- **Google Chrome o Microsoft Edge** en ordenador (la conexión con la controladora usa la API Web Serial, que no está disponible en Firefox, Safari ni móviles).
- Adaptador **USB a serie RS-232** (probado con chip FTDI) y cable al conector **D25 COMPUTER** de la controladora: 9600 baudios, 8 bits, sin paridad, 2 bits de stop.
- Mando de juegos opcional (probado con mando PS3 genérico).

## Seguridad

- Valida siempre las rutinas en **modo simulación** antes de ejecutarlas sobre el equipo real.
- Durante las pruebas: zona de trabajo despejada, velocidad baja y **mano en el interruptor MOTOR** de la controladora.
- Ninguna orden de software debe considerarse elemento de seguridad: la parada real es el interruptor MOTOR.

## Referencias

Protocolo de comunicación basado en el manual del fabricante del SCORBOT ER III (Eshed Robotec). El manual no se incluye en este repositorio por tratarse de documentación con derechos del fabricante.
