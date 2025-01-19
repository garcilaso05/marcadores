# Marcadores EWW (Personalización de escritorio con EWW)

Este proyecto tiene como objetivo simplificar y personalizar el entorno de escritorio usando EWW (Elvain's Window Widgets). Proporciona una interfaz con "marcadores" o "stickers" que pueden abrirse y cerrarse fácilmente, junto con un menú personalizado y la capacidad de manejar ventanas flotantes de información.

## Requisitos

1. **EWW**: Necesitas instalar EWW para gestionar los marcadores y las ventanas flotantes.
   - Para instalar EWW en Arch Linux, ejecuta:
   
     ```bash
     sudo pacman -S eww
     

2. **Archivos de configuración**: Asegúrate de tener los siguientes archivos de configuración de las ventanas:
   - `eww.scss`
   - `eww.yuck`

## Iniciar y manejar EWW

El funcionamiento de EWW es simple. Aquí están los comandos básicos:

- **Iniciar el programa**:

  ```bash
  .config/eww/target/release/eww daemon
- **Abrir un "sticker" (marcador)**:

  ```bash
  .config/eww/target/release/eww open objeto
- **Cerrar un "sticker" (marcador)**:

  ```bash
  .config/eww/target/release/eww close objeto
- **Cerrar el programa EWW**:

  ```bash
  pkill eww
  
## Esquema de funcionamiento del menú

1. **Abrir el menú con atajo** `WINDOWS + O`: Este atajo abrirá hasta dos monitores con un recuadro de menú y un botón desplegable de los marcadores. El código ejecutado es el siguiente:
   - `widgets.sh`:
  
     ```bash
     pkill eww
      /home/blackhole/.config/eww/target/release/eww daemon
      /home/blackhole/.config/eww/target/release/eww open search3
      /home/blackhole/.config/eww/target/release/eww open flechad
      /home/blackhole/.config/eww/target/release/eww open search3o
      /home/blackhole/.config/eww/target/release/eww open flechado
     ```
     
2. **Botón de menú**: Al presionar el botón grande de menú, se lanzará un menú personalizado con wofi. Si te interesa, puedes descargar el menú desde mi repositorio [mywofimenu](https://github.com/garcilaso05/mywofimenu.git).

3. **Flecha en el marcador**: Si se pulsa la flecha, dependiendo del monitor, se desplegarán más o menos marcadores.
   - `marcadores1.sh` y `marcadores1o.sh`: Para desplegar el menú y girar la flecha del desplegable.
   - `marcadores2.sh` y `marcadores2o.sh`: Para recoger el menú y volver a girar la flecha.
   Cada botón en el marcador tiene una acción específica, que puedes ver en el archivo `eww.yuck`.

4. **Función adicional**: Además, hay una función extra que abre varias ventanas flotantes con información sobre el sistema.

5. **Cerrar el menú con atajo**: Con el atajo `WINDOWS + K` se cerrarán todas las ventanas flotantes creadas por EWW.

## Iconos

Este proyecto incluye iconos (imágenes) para los botones de los marcadores, los cuales han sido extraídos de FlatIcon. No se realizan atribuciones personalizadas, ya que este proyecto es puramente para personalización y simplificación de tareas, sin fines de lucro.

## Imágenes

+ Iniciar programa
  
![2025-01-19-200806_hyprshot](https://github.com/user-attachments/assets/7172b5a3-96ea-4d01-9baf-130a1e4af417)

+ Desplegar menú

![2025-01-19-200817_hyprshot](https://github.com/user-attachments/assets/0caf158c-ad3b-4e02-b159-bd7889dca6cb)

+ Ejecutar marcadores

![2025-01-19-201004_hyprshot](https://github.com/user-attachments/assets/4af402ca-eda3-4187-a161-befa8933ed04)

+ Ejecución en un monitor mas pequeño

![2025-01-19-201033_hyprshot](https://github.com/user-attachments/assets/db51776f-70c7-421c-8a39-1680c3a38cbd)

+ Ejecución de funciones extra

![2025-01-19-201132_hyprshot](https://github.com/user-attachments/assets/2fcaa6a2-3167-49db-9041-1f55d0f7a0d6)

## Video de funcionamiento

