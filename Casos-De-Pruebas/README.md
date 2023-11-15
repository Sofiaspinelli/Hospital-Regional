# Casos de Pruebas

En este documento se describen tres casos de prueba para [Hospital Regional]. Cada caso de prueba incluirá una descripción breve y una imagen que ilustra el resultado esperado.

## Caso de Prueba 1: [Validar que se puedan asignar turnos a medicos]

### Descripción
Este caso de prueba verifica la capacidad del sistema para agregar un nuevo turno a la base de datos utilizando una sentencia SQL.

### Pasos
1. Ejecutar la siguiente sentencia SQL:
    ```sql
    INSERT INTO Turnos (id_turno, id_paciente, id_medico, nota, nombre_paciente, nombre_medico) VALUES
    (6, 1, 4, '19/04/2024 14.30hs', 'Dra Fernandez', 'Juan');
    ```
2. Hacer click en "Run SQL" para ejecutar la sentencia.

### Resultado Esperado
Se espera que el sistema registre el nuevo turno en la base de datos correctamente.

### Imagen
![Imagen del Caso de Prueba 1](/Casos-De-Pruebas/capshot1.png)
---

## Caso de Prueba 2: [Validar que se especifique el horario del turno medico]

### Descripción
[Se espera que en la tabla turnos en la columna nota se especifique el horario y fecha del turno medico a asistir por el paciente y el medico..]

### Pasos
1. [Ejecutar la siguiente sentencia SQL:
    ```sql
    INSERT INTO Turnos (id_turno, id_paciente, id_medico, nota, nombre_paciente, nombre_medico) VALUES
    (6, 1, 4, '19/04/2024 14.30hs', 'Dra Fernandez', 'Juan');.]


### Resultado Esperado
[Se espera que el sistema registre el nuevo turno en la base de datos correctamente.]

### Imagen
![Imagen del Caso de Prueba 2](/Casos-De-Pruebas/capshot2.png)

---

## Caso de Prueba 3: [Verificar que se pueda seleccionar la especialidad del medico al asignar un turno]

### Descripción
[Se espera que la tabla turnos tenga una columna llamada “especialidad“. Al no tenerla, se deberia hacer uso de INNER JOIN para unirla con la tabla medicos.]

### Pasos
1. Ejecutar la siguiente sentencia SQL:
    ```sql
    SELECT
        turnos.nota,
        pacientes.nombre_paciente,
        pacientes.edad,
        pacientes.numero_obra_social,
        medicos.nombre_medico,
        medicos.especialidad
    FROM turnos
    INNER JOIN pacientes ON turnos.id_paciente = pacientes.id_paciente
    INNER JOIN medicos ON turnos.id_medico = medicos.id_medico;
    ```
    2. Hacer click en "Run SQL" para ejecutar la sentencia.

### Resultado Esperado
[Se espera que el sistema devuelva correctamente la información detallada de turnos, pacientes y médicos.]

### Imagen
![Imagen del Caso de Prueba 3](/Casos-De-Pruebas/Capshot4.png)
