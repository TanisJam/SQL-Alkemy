1. Cree una tabla llamada CURSO con los atributos:
    1. Código de curso (clave primaria, entero no nulo)
    2. Nombre (varchar no nulo)
    3. Descripcion (varcha)
    4. Turno (varchar no nulo)

    `CREATE TABLE curso (
        codigo INT PRIMARY KEY NOT NULL,
        nombre varchar(20) NOT NULL,
        descripcion varchar(50),
        turno varchar(10) NOT NULL
    )`



2. Agregue un campo “cupo” de tipo numérico

    `ALTER TABlE curso
    ADD COLUMN cupo INT`



3. Inserte datos en la tabla:
    1. (101, “Algoritmos”,”Algoritmos y Estructuras de Datos”,”Mañana”,35)
    2. (102, “Matemática Discreta”,””,”Tarde”,30)

    `INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
    VALUES (101, 'Algoritmos','Algoritmos y Estructuras de Datos','Mañana',35)`

    `INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
    VALUES (102, 'Matemática Discreta','','Tarde',30)`



4. Intente ingresar un registro con el nombre nulo y verifique que no funciona

    `INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
    VALUES (103, null,'','Tarde',30)`



5. Intente ingresar un registro con la clave primaria repetida y verifique que no funciona

    `INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
    VALUES (102, '','','Tarde',30)`



6. Actualice, para todos los cursos, el cupo en 25

    `UPDATE curso
    SET cupo = 25`



7. Elimine el curso Algoritmos

    `DELETE FROM curso
    WHERE nombre = 'Algoritmos'`
