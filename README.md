# CPU-16-Instrucciones en logisim

# Introducción
Este proyecto busca aplicar los conceptos de arquitectura de computadoras, microinstrucciones y memoria a través del diseño de un CPU en Logisim capaz de ejecutar hasta 16 instrucciones, incluyendo operaciones aritméticas, lógicas y saltos condicionales.

La idea es comprender cómo se coordinan los distintos componentes de un procesador y visualizar de forma práctica cómo se ejecutan las instrucciones a nivel de hardware.

# Marco teórico
Para este proyecto se estudiaron los principales bloques que forman un CPU:

Registros: almacenan datos de forma temporal.

Decodificadores: permiten seleccionar operaciones y gestionar instrucciones.

ALU (Unidad Aritmética Lógica): realiza operaciones aritméticas y lógicas.

Memoria (ROM y RAM): para guardar instrucciones y datos.

Además, se utilizaron microinstrucciones para controlar los ciclos de ejecución y el flujo de datos entre los registros, la memoria y la ALU, permitiendo entender cómo un CPU ejecuta instrucciones de forma ordenada.

# Diseño del CPU
El CPU se construyó en Logisim con:

Compuertas lógicas y multiplexores para el control del flujo de datos.

Registros para manejar datos e instrucciones.

Un decodificador para las señales de control.

Una ALU capaz de realizar:

AND, OR, XOR, NOT

ADD, SUB

ROM para las instrucciones y RAM para los datos.

# Instrucciones implementadas
El CPU puede ejecutar las siguientes instrucciones:

NO OP

Operaciones lógicas: AND, OR, XOR, NOT

Operaciones aritméticas: ADD, SUB

Manejo de memoria: LOAD, STORE

Carga y almacenamiento inmediato: LOADI, STOREI

Saltos: JMP, BEQ, BB

SHIFT

COMPARE

# Pruebas realizadas
Para comprobar el funcionamiento del CPU, se cargaron las siguientes instrucciones de prueba en la memoria:

css
Copy
Edit
4041    STOREI inmediato a la posición 1
4022    STOREI inmediato a la posición 2
1101    LOAD de memoria 1 al registro 1
1202    LOAD de memoria 2 al registro 2
E124    SUB del registro 2 al 1, resultado en el registro 4
9126    AND del registro 1 y 2, resultado en el registro 9
600F    Salto a la instrucción 15
A127    OR del registro 1 y 2, resultado en el registro 7
B128    XOR del registro 1 y 2, resultado en el registro 8
C129    NOT del registro 1, resultado en el registro 9
F120    SHIFT del registro 1, 2 bits a la izquierda
5120    COMPARE del registro 1 y 2
7000    BIGGER BRANCH, salta a la línea 0

# ¿Qué necesitas para probarlo?
Tener Logisim (o Logisim Evolution) instalado.

Descargar este repositorio y abrir el archivo .circ en Logisim.

Cargar las instrucciones de prueba o agregar nuevas para simular el CPU.

# Cómo utilizarlo
Abre el archivo del proyecto en Logisim.

Carga las instrucciones en la ROM usando el editor de memoria.

Ejecuta paso a paso para observar cómo cambian los registros y las señales de control.

Analiza cómo cada instrucción se ejecuta a nivel de hardware.

# ¿Por qué es útil este proyecto?
Con este proyecto podrás:

✅ Comprender cómo funcionan las instrucciones dentro de un CPU.
✅ Visualizar en tiempo real el flujo de datos y las señales de control.
✅ Reforzar los conceptos de registros, ALU y memoria en arquitectura de computadoras.
✅ Practicar el diseño de circuitos digitales en Logisim.

# Estructura del repositorio
bash
Copy
Edit
/cpu-logisim/
│
├── cpu16.circ         # Proyecto de Logisim
└── README.md          # Este archivo
