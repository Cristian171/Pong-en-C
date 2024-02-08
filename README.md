[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12356849&assignment_repo_type=AssignmentRepo)

# Evaluación Unidad #4

## PONG en C Implementación de Hilos y Semaforos en C para Reproducción de Audios
<b>Playing Pong Game</b><br>
![alt_tag](https://media.discordapp.net/attachments/876619774044549130/1172359249276436532/Video_sin_titulo_Hecho_con_Clipchamp.gif?ex=656007a2&is=654d92a2&hm=c7dcf3c8354ecd9258e6a4a9fb1791cc3b487633291c9d77426e91fa3009978f&=&width=383&height=215)

Este proyecto utiliza hilos y semáforos en C para lograr una reproducción de audios sin interrupciones, permitiendo que cada audio se reproduzca sin que se interponga con otro. La implementación se realiza utilizando la biblioteca SDL (Simple DirectMedia Layer) para la manipulación de audio.

## Objetivo

El objetivo principal es evitar la superposición de audios al reproducir varios sonidos en paralelo, garantizando que cada audio tenga el tiempo suficiente para reproducirse antes de que comience otro.

### Hilos

Se utilizan hilos para realizar la reproducción de audio en paralelo, permitiendo que múltiples sonidos se reproduzcan simultáneamente sin bloquear el hilo principal del programa.

### Semaforos

Se emplean semáforos para controlar el acceso a los recursos compartidos, en este caso, el dispositivo de audio. Cada hilo espera a que el semáforo esté disponible antes de acceder al dispositivo de audio, asegurando así que no haya interferencias entre los hilos.

## Estructura del Proyecto

- **`constants.h`**: Archivo que contiene las constantes utilizadas en el proyecto.
- **`main.c`**: Código principal del programa que implementa la lógica del juego y la reproducción de audio.

## Dependencias

- **SDL**: La implementación depende de la biblioteca SDL para la manipulación de audio. Asegúrate de tener SDL instalado en tu sistema Descargar los VC.
 
- https://github.com/libsdl-org/SDL/releases/tag/release-2.28.5
- https://github.com/libsdl-org/SDL_ttf/releases

## Configuraciones necesarias de visual code 2023
- Configuraciones necesitas para poder inicar el juego dentro de visual studio code 2022.
- Dentro de propiedades se añaden las siguentes consiguraciones SDL2 las puedes encontrar dentro del archivo las puedes descargar y darle la ruta donde esten ubicadas.
SDL2.lib
SDL2main.lib
SDL2_ttf.lib

![FOTO](https://cdn.discordapp.com/attachments/755609390853128222/1165400548556668948/image.png?ex=6546b6d6&is=653441d6&hm=4c88b41029a700802d6fde872a62df2111f15a6de6eabdffdb1a9e960aa82ff3&)
![FOTO](https://cdn.discordapp.com/attachments/755609390853128222/1165402038188908585/image.png?ex=6546b83a&is=6534433a&hm=e093e29ee1b2690d7dbeb9eb1a5026a1db9c19e585bf2e38b149985fd5cab8d3&)
![FOTO](https://cdn.discordapp.com/attachments/755609390853128222/1165402407845503137/image.png?ex=6546b892&is=65344392&hm=98055e7bf43e6ae94aed8903f20841e76c82ab8b6f1e91166c7e5c5df39d1fff&)

## Video Explicando como funcionan los hilos y Semaforos

https://www.youtube.com/watch?v=XuKGZjTI2Jk

Para compilar el programa, puedes utilizar el siguiente comando:

```bash
gcc main.c audio.c -o nombre_del_programa -lSDL2 -lSDL2_ttf -lpthread
