CREATE TABLE curso (
	codigo INT PRIMARY KEY NOT NULL,
    nombre varchar(20) NOT NULL,
    descripcion varchar(50),
    turno varchar(10) NOT NULL
)

ALTER TABlE curso
ADD COLUMN cupo INT

INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
VALUES (101, 'Algoritmos','Algoritmos y Estructuras de Datos','Mañana',35)

INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
VALUES (102, 'Matemática Discreta','','Tarde',30)

INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
VALUES (103, null,'','Tarde',30)

INSERT INTO curso (codigo, nombre, descripcion, turno, cupo)
VALUES (102, '','','Tarde',30)

UPDATE curso
SET cupo = 25

DELETE FROM curso
WHERE nombre = 'Algoritmos'
