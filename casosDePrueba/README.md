# Validar los campos del formulario que contengan hasta 50 caracteres

### Precondicion
Estar en el editor SQL
Tablas medicos, pacientes y turnos creadas

### Datos de entrada
Nada

### Pasos
1- Escribir  consulta especifica para cada campo

### Descripción
Se deberia poder escribir hasta 50 caracteres por campo (nombre_paciente, nombre_medico, especialidad)

### Resultado obtenido
Al escribir mas de 50 caracteres nos devuelve un error. Solo nos deja cargar 50 caracteres.
### Imagen
![Pacientes](/casosDePrueba/images\Pacientes1.png)
![Especialidad](/casosDePrueba/images\especialidad-nombre.png)

=============

# Validar campos requeridos

### Precondicion
Tabla existente donde se van a validar los campos

### Datos de entrada
Nada

### Pasos
1- Verificar la existencia de la condicion ‘NOT NULL' y ‘CHECK’, ‘INT’, 'STRING’ al realizar la consulta

### Descripción
Se debería cumplir con la restriccion de cada campo en especifico
![](/casosDePrueba/images\validar-campos-requeridos.png)

### Resultado obtenido
Se cumple con las normas de cada tipo de dato.

=============

# Validar que el campo de edad acepte solo 2 digitos

### Precondicion
Tabla existente de pacientes con campo edad en el editor sql

### Datos de entrada
UPDATE pacientes SET edad = 101 where id_paciente = 1

### Pasos
1- Hacer click en “RUN SQL“

### Descripción
Se espera que me devuelva un error al querer actualizar una edad que no aplica con el requirimiento de solo dos digitos.

### Resultado obtenido
Error: CHECK constraint failed: LENGTH(edad) = 2 AND edad >= 1 AND edad <= 99

### Imagen
![](/casosDePrueba/images/Edad.png)

=============

# Validar que el campo del numero de asociado de obra social se registre correctamente

### Precondicion
Tener una tabla existente en la base de datos donde se almacene el número de asociado de obra social.
Estar dentro del sistema del hospital, registrando los dantos de un paciente

### Datos de entrada
la columna destinada para el número de asociado de obra social esté definida con el tipo de dato y longitud adecuados INT(20), se esperan solo numeros.

### Pasos
1- Registrar el numero de obra social que cumpla con el formato y logitud esperado

### Descripción
El número de asociado de obra social se registra sin problemas y se almacena en la base de datos según el formato y longitud esperados.

### Resultado obtenido
El número de asociado de obra social se ingresa sin errores en la base de datos, cumpliendo con la restricción de longitud y formato

### Imagen
![](/casosDePrueba/images/tablaPaciente.png)
![](/casosDePrueba/images/obraSocial.png)