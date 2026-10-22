# Sistemas Informáticos Industriales - Práctica 1

Repositorio de las prácticas de la asignatura Sistemas Informáticos
Industriales (ETSIDI, UPM).

## Proyecto

Juego de tenis para dos jugadores en C++ con OpenGL y GLUT.

- Jugador izquierdo: teclas `w` (arriba) y `s` (abajo).
- Jugador derecho: teclas `o` (arriba) y `l` (abajo).

## Compilación

    cd workspace
    mkdir build && cd build
    cmake ..
    make
    ./tenis

## Autor

Álvaro Pérez Ruano - 57616

## Práctica 2: Comunicación mediante FIFO

- Nuevo programa `logger` que recibe del juego, a través de una tubería con nombre (FIFO), cada punto marcado: jugador y puntos totales.
- El logger crea, abre en lectura y destruye la FIFO; el tenis la abre en escritura y envía un mensaje en cada punto.
- La partida termina cuando un jugador alcanza 3 puntos; al cerrarse el tenis, el logger también termina.
- La tecla ESC cierra el juego.

**Ejecución** (desde `workspace/build`, en dos terminales y en este orden):
1. `./logger`
2. `./tenis`
