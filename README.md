# TorneoFutbol
Proyecto torneo de futbol (Tarea 2)
# TorneoFutbol

Aplicación de gestión de torneos de fútbol escolar desarrollada con PySide6 y SQLite.

## Características

- **Gestión de Equipos**: Crear, editar y eliminar equipos con nombre, curso, color de camiseta y escudo.
- **Participantes**: Registrar jugadores y árbitros con estadísticas (goles, tarjetas amarillas/rojas), asignar a equipos.
- **Calendario**: Programar partidos por fases eliminatorias, editar resultados con doble click, generar partidos aleatorios.
- **Clasificación**: Mostrar tabla de clasificación con puntos, partidos jugados, etc., y exportar a CSV.
- **Créditos y Ayuda**: Pestañas con información del programa y ayuda básica.
- **Interfaz Moderna**: Tema oscuro, iconos, tooltips y estilos personalizados.

## Base de Datos

- **Equipos**: id, nombre, curso, color, escudo
- **Participantes**: id, nombre, fecha_nacimiento, curso, es_jugador, es_arbitro, posicion, equipo_id, goles, t_amarillas, t_rojas
- **Partidos**: id, fase, equipo_local_id, equipo_visitante_id, arbitro_id, goles_local, goles_visitante, fecha, hora, ganador_id, id_partido_siguiente

Relaciones: Participantes -> Equipos (equipo_id), Partidos -> Equipos (local/visitante), Partidos -> Participantes (arbitro)

## Requisitos

- Python 3.x
- PySide6
- SQLite (incluido)

## Instalación

1. Instalar dependencias:
   ```
   pip install PySide6
   ```

2. Ejecutar:
   ```
   python main.py
   ```

## Empaquetado

Para crear un ejecutable con PyInstaller:
```
pip install pyinstaller
pyinstaller --onefile --windowed main.py
```

## Autor

Álvaro Neculau Moreno.
