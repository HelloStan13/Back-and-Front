# Back-and-Front
Back and Front SpringBoot, Thymeleaf, Bootstrap++

### By Adryan Ynfante

## Tabla de contenido

- [Pasos para Ejecutar](#Pasos-para-Ejecutar).
- [MySQL](#MySQL).
- [Ejecutar en Intellij](#Ejecutar-en-Intellij).
- [Abrir localhost](#Abrir-localhost).
- [CRUD Vista](#CRUD-Vista).
- [Contacto](#Contacto).

### Pasos para Ejecutar
### Descargar o Clonar
https://github.com/HelloStan13/Back-and-Front.git

### Copiar carpeta de video juegos en C:/
C:/Videojuegos/imagenes/

### MySQL

### Base de Datos creación 
Ir a MySQl y seguir pasos:

Crear y usar Base 
1. CREATE DATABASE `videojuegos`;
2. USE `videojuegos`;

3.Crear tabla de categorías
 CREATE TABLE `categorias` (
  `id` bigint(20) NOT NULL AUTO_INCREMENT,
  `activo` bit(1) NOT NULL,
  `nombre` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

4.Información tabla categorías
 insert  into `categorias`(`id`,`activo`,`nombre`) values (1,'','Sandbox'),(2,'','Aventura'),(3,'\0','Terror');

5.Crear tabla estudios
 CREATE TABLE `estudios` (
  `id` bigint(20) NOT NULL AUTO_INCREMENT,
  `activo` bit(1) NOT NULL,
  `nombre` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

6. Información tabla estudios
insert  into `estudios`(`id`,`activo`,`nombre`) values (1,'','Estudio 1'),(2,'','Estudio 2'),(3,'\0','Estudio Test');

7.Creación tabla video juegos
 CREATE TABLE `videojuegos` (
  `id` bigint(20) NOT NULL AUTO_INCREMENT,
  `activo` bit(1) NOT NULL,
  `descripcion` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  `fecha_lanzamiento` datetime DEFAULT NULL,
  `imagen` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  `precio` float NOT NULL,
  `stock` int(11) NOT NULL,
  `titulo` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  `fk_categoria` bigint(20) NOT NULL,
  `fk_estudio` bigint(20) NOT NULL,
  PRIMARY KEY (`id`),
  KEY `FK54ev8cdsfhbdfxufd9wc8g23x` (`fk_categoria`),
  KEY `FKev9v8m1hnvqlpne73pgko027c` (`fk_estudio`),
  CONSTRAINT `FK54ev8cdsfhbdfxufd9wc8g23x` FOREIGN KEY (`fk_categoria`) REFERENCES `categorias` (`id`),
  CONSTRAINT `FKev9v8m1hnvqlpne73pgko027c` FOREIGN KEY (`fk_estudio`) REFERENCES `estudios` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=13 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

### Insertar video juegos
#### Recuerde copiar la carpeta video juegos de lo contratio las imagenes no se van a  ver

8. INSERT INTO `videojuegos`.`videojuegos` (`id`, `activo`, `descripcion`, `fecha_lanzamiento`, `imagen`, `precio`, `stock`, `titulo`, `fk_categoria`, `fk_estudio`) 
VALUES (1, 1, 'Aventuras y mas', '2021-09-06 21:50:17', '3.png', 150, 2, 'Spiderman 1', 1, 2);

9. INSERT INTO `videojuegos`.`videojuegos` (`id`, `activo`, `descripcion`, `fecha_lanzamiento`, `imagen`, `precio`, `stock`, `titulo`, `fk_categoria`, `fk_estudio`) 
VALUES (2, 1, 'El mejor Juego', '2021-09-06 21:50:17', '0243323.jpg', 250, 9, 'Spiderman 2', 1, 2);

10. INSERT INTO `videojuegos`.`videojuegos` (`id`, `activo`, `descripcion`, `fecha_lanzamiento`, `imagen`, `precio`, `stock`, `titulo`, `fk_categoria`, `fk_estudio`) 
VALUES (3, 1, 'Aventuras', '2021-09-06 21:50:17', '3.png', 130, 7, 'Spiderman 2', 1, 2);

10. INSERT INTO `videojuegos`.`videojuegos` (`id`, `activo`, `descripcion`, `fecha_lanzamiento`, `imagen`, `precio`, `stock`, `titulo`, `fk_categoria`, `fk_estudio`) 
VALUES (4, 1, 'Joker vs Batman', '2021-09-06 21:50:17', '1646696338282.jpg', 80, 9, 'Batman  vs joker', 1, 2);

### Ejecutar en Intellij

### Abrir localhost
http://localhost:9090
Muestra una bienvenida super sencilla

#### Ir a http://localhost:9090/inicio --> Aca hay acceso a todos los videoJ uegos y tambien al CRUD
![image](https://user-images.githubusercontent.com/92740455/157151543-be2b0e5c-100a-41e1-a1b7-beb2d7ce752a.png)

#### Acciones 
![image](https://user-images.githubusercontent.com/92740455/157151618-b91f7362-3ce2-4e67-9fc0-d6be9abad606.png)

#### CRUD Vista
![image](https://user-images.githubusercontent.com/92740455/157151669-e633dd43-08b6-4143-80ba-7fc1580dbfd5.png)

### Agregar nuevo
![image](https://user-images.githubusercontent.com/92740455/157151722-a1d6c19d-43ac-4daa-becc-814e9853dbf8.png)

### Contacto
#### Adryan Ynfante --> adryanynfante@gmail.com
