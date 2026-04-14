 Sistema de Liga de Futbol

Estudiante:Kanny Fernanda Gutierrez Infante  

Descripcion
Es una aplicacion de consola en C++ que gestiona una liga de futbol completa. Permite registrar partidos, consultar la tabla de posiciones y revisar el historial de jornadas. Todo el estado se guarda en archivos de texto y persiste entre ejecuciones.

Compilar

bash
g++ -o liga src/main.cpp


Ejecutar

bash
./liga


En Windows: 'liga.exe'
El programa debe ejecutarse desde la carpeta que contiene los archivos `.txt`.

  Formato de config.txt


 Comentario
liga=Liga Profesional Colombia
victoria=3
empate=1
derrota=0
equipo=Atletico Nacional
equipo=Millonarios FC


 Formato de partidos.txt

2025-03-15|Atletico Nacional|Millonarios FC|2|1
2025-03-15|America de Cali|Junior FC|0|0


Formato de fechas.txt


JORNADA=1|2025-03-15
Atletico Nacional|Millonarios FC|2|1
FIN_JORNADA


Decisiones de diseño

- Todo el input usa 'getline' para evitar que quede basura en el buffer de 'cin'.
- El delimitador '|' se uso porque es poco comun en nombres de equipos.
- actualizar estadisticas,recibe un puntero 'Equipo' para modificar el objeto directamente.
- La tabla se ordena por puntos, luego diferencia de goles, luego goles a favor.
