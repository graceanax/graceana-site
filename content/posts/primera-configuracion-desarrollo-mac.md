+++
date = '2025-01-03T00:10:16-06:00'
draft = false
title = 'Primera Configuracion Desarrollo Mac'
categories = ["MacOS", "Desarrollo de Software", "Configuración de entornos", "Herramientas"]
tags = ["MacOS", "Configuración", "Homebrew", "GitHub", "Git", "SSH", "Terminal"]
description = "Guía para configurar un entorno de desarrollo básico en Mac."
+++

Configurar un entorno de desarrollo en macOS puede ser sencillo. Uno de los aspectos clave al trabajar en desarrollo es aprender a utilizar la Terminal, una herramienta poderosa para instalar y ejecutar paquetes, programas y mucho más.

### Accede a la Terminal

Puedes abrir la Terminal fácilmente desde Spotlight: presiona `Command + Barra espaciadora` y escribe "Terminal". Verás algo como esto:
![Terminal 1](/images/primera-conf-mac-os/primera-conf-mac-os-1.png)

El área que ves es el "prompt", donde podrás introducir comandos. El texto que está antes del cursor muestra tu usuario y el nombre de tu Mac.

### Instalando Homebrew

Homebrew es un gestor de paquetes que facilita la instalación de herramientas y programas en macOS. Aquí [su sitio oficial](https://brew.sh/es/).

Para instalarlo, copia y pega este comando en tu Terminal:

```bash

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Durante el proceso, también se instalarán las Command Line Tools para Xcode. Al finalizar el proceso, sigue las instrucciones que aparecerán, copia y pega cada uno de los comandos que aparecen en la terminal línea por línea. 

Los comandos inician así:

```bash
echo >> ..
echo >> ..
eval ...
```

![Terminal 2](/images/primera-conf-mac-os/primera-conf-mac-os-2.png)

Una vez completado, verifica que todo esté correctamente configurado con:

```bash
brew doctor
```

Si todo está bien, verás el mensaje: *"Your system is ready to brew."*

### ¿Por qué usar Git?

Git es como un "historial de cambios" para tus proyectos y se ha convertido en en estándar en desarrollo. Te permite:

- **Guardar versiones:** Si algo sale mal, puedes volver a un punto anterior.
- **Trabajar en equipo:** Coordina cambios con otras personas sin sobrescribir su trabajo.
- **Publicar tus proyectos:** Súbelos a plataformas como GitHub para compartirlos o colaborar.

### Configurando Git

1. Introduce tu nombre y correo para que tus cambios queden registrados con tus datos:
    > 💡 Si utilizas Github, te recomiendo utilizar el correo que tienes registrado
    
    ```bash
    git config --global user.name "tu_nombre_de_usuario"
    git config --global user.email "tu_correo@example.com
    ```
    
2. Verifica que todo esté bien configurado:
    
    ```bash
    git config --list
    ```
    

### ¿Por qué conectar Git con GitHub (y qué son las SSH keys)?

GitHub es como una nube para desarrolladores. Permite guardar tu código, hacer un historial de cambios, colaborar con otros, mostrar tus proyectos, entre muchas cosas más. Es ideal para trabajar en equipo o para crear un portafolio de tus trabajos.

Si vas a trabajar con GitHub, configurar una clave SSH hace que conectarte sea más seguro y sin tener que escribir tu contraseña cada vez. Es como tener una llave maestra.

SSH (Secure Shell) es una forma segura de conectar tu computadora con servicios como GitHub. Usa un sistema de llaves:

- **Llave pública:** La compartes con GitHub para identificarte.
- **Llave privada:** Queda en tu computadora y es como tu firma secreta, no se debe compartir.

Esto hace que las conexiones sean más seguras y evita que tengas que escribir tu usuario y contraseña cada vez.

1. Genera tu clave SSH:
    
    ```bash
    ssh-keygen -t ed25519 -C "tu_correo_de_github@example.com"
    ```
    
    - Presiona Enter para aceptar el nombre por defecto.
    - Opcional: Puedes agregar una contraseña para mayor seguridad.
2. Copia la clave pública:
    
    ```bash
    pbcopy < ~/.ssh/id_ed25519.pub
    
    ```
    
3. Ve a [Configuración de claves SSH en GitHub](https://github.com/settings/keys) , agrega una nueva clave SSH y pega la clave copiada.
    
    ![Nueva llave SSH en GitHub](/images/primera-conf-mac-os/primera-conf-mac-os-3.png)
    
    Te recomiendo que agregues un título descriptivo, yo suelo colocar el nombre de mi computadora para poder identificar las llaves, ya que por cada computadora que quieras conectar, debes generarlas.
    
    ![Nueva llave SSH en GitHub 2](/images/primera-conf-mac-os/primera-conf-mac-os-4.png)
    
4. En tu terminal, agrega pega el siguiente comando para verificar la conexión:
    
    ```bash
    ssh -T git@github.com
    ```
    
    ![Terminal 3](/images/primera-conf-mac-os/primera-conf-mac-os-5.png)
    

¡Listo! Ahora tu Mac y GitHub están conectados.

### Mejoremos el aspecto de nuestra terminal con Oh My Zsh

Una terminal atractiva y funcional hace que trabajar sea más cómodo. Para esto usaremos **Oh My Zsh**, un framework gratuito y de código abierto para mejorar su aspecto. 

### Cómo instalar Oh My Zsh

La instalación es sencilla. Solo ejecuta este comando en tu terminal:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Al instalarlo, notarás que tu terminal tiene un diseño más limpio y atractivo:

![Terminal 4](/images/primera-conf-mac-os/primera-conf-mac-os-6.png)

Oh My Zsh también tiene una variedad de temas que puedes explorar para personalizar aún más tu terminal, pero eso lo dejamos para otro día.