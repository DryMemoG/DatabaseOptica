-- --------------------------------------------------------
-- Host:                         127.0.0.1
-- VersiÃ³n del servidor:         10.1.38-MariaDB - mariadb.org binary distribution
-- SO del servidor:              Win64
-- HeidiSQL VersiÃ³n:             10.2.0.5599
-- --------------------------------------------------------

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET NAMES utf8 */;
/*!50503 SET NAMES utf8mb4 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;


-- Volcando estructura de base de datos para optica
CREATE DATABASE IF NOT EXISTS `optica` /*!40100 DEFAULT CHARACTER SET utf8 COLLATE utf8_spanish_ci */;
USE `optica`;

-- Volcando estructura para tabla optica.agudezavisuallejos
CREATE TABLE IF NOT EXISTS `agudezavisuallejos` (
  `codav` int(11) NOT NULL,
  `av` double NOT NULL DEFAULT '0',
  `tipoav` int(11) NOT NULL DEFAULT '0',
  `phae` double NOT NULL DEFAULT '0',
  `avc` double NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL,
  `codec` int(11) NOT NULL,
  PRIMARY KEY (`codav`),
  KEY `FK_agudezavisuallejos_ojo` (`codojo`),
  KEY `FK_agudezavisuallejos_tipoav` (`tipoav`),
  KEY `FK_agudezavisuallejos_examenclinico` (`codec`),
  CONSTRAINT `FK_agudezavisuallejos_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_agudezavisuallejos_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`),
  CONSTRAINT `FK_agudezavisuallejos_tipoav` FOREIGN KEY (`tipoav`) REFERENCES `tipoav` (`codtipoav`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Agudeza visual de un ojo Lejos';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.antecedente
CREATE TABLE IF NOT EXISTS `antecedente` (
  `codantecedente` int(11) NOT NULL,
  `tipoAntecedente` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  `Descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  `codhistoriaclinica` int(11) NOT NULL,
  PRIMARY KEY (`codantecedente`),
  KEY `FK_antecedente_historiaclinica` (`codhistoriaclinica`),
  CONSTRAINT `FK_antecedente_historiaclinica` FOREIGN KEY (`codhistoriaclinica`) REFERENCES `historiaclinica` (`codhistoriaclinica`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Antecedentes MÃ©dicos, oftalmicos, quirugicos, familiares y alergicos del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.camaraant
CREATE TABLE IF NOT EXISTS `camaraant` (
  `codcam` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codcam`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de la cÃ¡mara anterior del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.categoria
CREATE TABLE IF NOT EXISTS `categoria` (
  `codcategoria` int(11) NOT NULL,
  `Nombre` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `Descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `Descuento` double NOT NULL DEFAULT '0',
  PRIMARY KEY (`codcategoria`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Categoria del paciente (alumno, pariente de alumno etc.)';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.conjuntiva
CREATE TABLE IF NOT EXISTS `conjuntiva` (
  `codconj` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codconj`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Saludo ocular de la conuntiva del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.convergencia
CREATE TABLE IF NOT EXISTS `convergencia` (
  `codconvergencia` int(11) NOT NULL,
  `tipoconvergencia` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `descripcion` text COLLATE utf8_spanish_ci,
  `foto` varchar(50) COLLATE utf8_spanish_ci DEFAULT NULL,
  PRIMARY KEY (`codconvergencia`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='convergencias en el Ojo';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.cornea
CREATE TABLE IF NOT EXISTS `cornea` (
  `codcornea` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codcornea`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Saludo ocular de la cornea del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.correccionactual
CREATE TABLE IF NOT EXISTS `correccionactual` (
  `codca` int(11) NOT NULL,
  `esfera` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '0',
  `cilindro` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '0',
  `eje` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '0',
  `avcc` double NOT NULL DEFAULT '0',
  `addeje` double NOT NULL DEFAULT '0',
  `addavcc` double NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL DEFAULT '0',
  `codec` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codca`),
  KEY `FK_correccionactual_ojo` (`codojo`),
  KEY `FK_correccionactual_examenclinico` (`codec`),
  CONSTRAINT `FK_correccionactual_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_correccionactual_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Correccion actual del paciente en caso usara lentes';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.cristalino
CREATE TABLE IF NOT EXISTS `cristalino` (
  `codcristalino` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codcristalino`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular del cristalino del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.duccion
CREATE TABLE IF NOT EXISTS `duccion` (
  `codduccion` int(11) NOT NULL AUTO_INCREMENT,
  `tipoduccion` varchar(100) COLLATE utf8_spanish_ci NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci,
  `foto` varchar(100) COLLATE utf8_spanish_ci DEFAULT NULL,
  PRIMARY KEY (`codduccion`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Ducciones en el Ojo';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.empleado
CREATE TABLE IF NOT EXISTS `empleado` (
  `nombre1emp` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  `nombre2emp` varchar(100) COLLATE utf8_spanish_ci DEFAULT NULL,
  `apellido1emp` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  `apellido2emp` varchar(100) COLLATE utf8_spanish_ci DEFAULT NULL,
  `apellido3emp` varchar(100) COLLATE utf8_spanish_ci DEFAULT NULL,
  `telefono1emp` varchar(20) COLLATE utf8_spanish_ci NOT NULL,
  `telefono2emp` varchar(20) COLLATE utf8_spanish_ci DEFAULT NULL,
  `cuiemp` varchar(15) COLLATE utf8_spanish_ci DEFAULT NULL,
  `direccion` varchar(100) COLLATE utf8_spanish_ci NOT NULL,
  `codpuesto` int(11) NOT NULL,
  `codempleado` int(11) NOT NULL AUTO_INCREMENT,
  PRIMARY KEY (`codempleado`),
  KEY `empleado_fk` (`codpuesto`),
  CONSTRAINT `empleado_fk` FOREIGN KEY (`codpuesto`) REFERENCES `puesto` (`codpuesto`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci;

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.esclera
CREATE TABLE IF NOT EXISTS `esclera` (
  `codesclera` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codesclera`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Saludo ocular de la Esclera del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.examenclinico
CREATE TABLE IF NOT EXISTS `examenclinico` (
  `codec` int(11) NOT NULL,
  PRIMARY KEY (`codec`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Examen clÃ­nico completo de ojos';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.examenfinal
CREATE TABLE IF NOT EXISTS `examenfinal` (
  `codexfinal` int(11) NOT NULL,
  `codrf` int(11) NOT NULL,
  `lenterecomendado` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `uso` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `proximacita` date NOT NULL DEFAULT '0000-00-00',
  `icdx` text COLLATE utf8_spanish_ci NOT NULL,
  `tx` text COLLATE utf8_spanish_ci NOT NULL,
  `codec` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codexfinal`),
  KEY `FK_ExamenFinal_refraccionfinal` (`codrf`),
  KEY `FK_examenfinal_examenclinico` (`codec`),
  CONSTRAINT `FK_ExamenFinal_refraccionfinal` FOREIGN KEY (`codrf`) REFERENCES `refraccionfinal` (`codrf`),
  CONSTRAINT `FK_examenfinal_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Examen final dado por el optometrista';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.fichamedica
CREATE TABLE IF NOT EXISTS `fichamedica` (
  `codficha` int(11) NOT NULL,
  `codpaciente` int(11) NOT NULL,
  `fecha` date NOT NULL DEFAULT '0000-00-00',
  `codantecedente` int(11) NOT NULL,
  `codec` int(11) NOT NULL,
  PRIMARY KEY (`codficha`),
  KEY `FK_FichaMedica_paciente` (`codpaciente`),
  KEY `FK_FichaMedica_antecedente` (`codantecedente`),
  KEY `FK_FichaMedica_examenclinico` (`codec`),
  CONSTRAINT `FK_FichaMedica_antecedente` FOREIGN KEY (`codantecedente`) REFERENCES `antecedente` (`codantecedente`),
  CONSTRAINT `FK_FichaMedica_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_FichaMedica_paciente` FOREIGN KEY (`codpaciente`) REFERENCES `paciente` (`codpaciente`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Ficha mÃ©dica del paciente de la optica';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.foria
CREATE TABLE IF NOT EXISTS `foria` (
  `codForia` int(11) NOT NULL,
  `tipoForia` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `Descripcion` text COLLATE utf8_spanish_ci,
  `Foto` varchar(50) COLLATE utf8_spanish_ci DEFAULT '',
  PRIMARY KEY (`codForia`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Forias en el Ojo';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.historiaclinica
CREATE TABLE IF NOT EXISTS `historiaclinica` (
  `codhistoriaclinica` int(11) NOT NULL,
  `motivoconsulta` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codhistoriaclinica`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Historia clinica del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.iris
CREATE TABLE IF NOT EXISTS `iris` (
  `codiris` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codiris`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular del iris del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.lagrimayvialagrimal
CREATE TABLE IF NOT EXISTS `lagrimayvialagrimal` (
  `codlag` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codlag`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de la LÃ¡grima y via lagrimal del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.motilidadocular
CREATE TABLE IF NOT EXISTS `motilidadocular` (
  `codmotocular` int(11) NOT NULL,
  `movmuscfij` text COLLATE utf8_spanish_ci NOT NULL,
  `codforia` int(11) NOT NULL DEFAULT '0',
  `codtropia` int(11) NOT NULL DEFAULT '0',
  `codduccion` int(11) NOT NULL DEFAULT '0',
  `codversion` int(11) NOT NULL DEFAULT '0',
  `codconvergencia` int(11) NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL DEFAULT '0',
  `codec` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codmotocular`),
  KEY `FK1codForia` (`codforia`),
  KEY `FK2codtropia` (`codtropia`),
  KEY `FK3codduccion` (`codduccion`),
  KEY `FK4codversion` (`codversion`),
  KEY `FK5codconvergencia` (`codconvergencia`),
  KEY `FK6codojo` (`codojo`),
  KEY `FK_motilidadocular_examenfinal` (`codec`),
  CONSTRAINT `FK1codForia` FOREIGN KEY (`codforia`) REFERENCES `foria` (`codForia`),
  CONSTRAINT `FK2codtropia` FOREIGN KEY (`codtropia`) REFERENCES `tropia` (`codtropia`),
  CONSTRAINT `FK3codduccion` FOREIGN KEY (`codduccion`) REFERENCES `duccion` (`codduccion`),
  CONSTRAINT `FK4codversion` FOREIGN KEY (`codversion`) REFERENCES `version` (`codversion`),
  CONSTRAINT `FK5codconvergencia` FOREIGN KEY (`codconvergencia`) REFERENCES `convergencia` (`codconvergencia`),
  CONSTRAINT `FK6codojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`),
  CONSTRAINT `FK_motilidadocular_examenfinal` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Evaluacion sobre la motilidad ocular';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.nerviooptico
CREATE TABLE IF NOT EXISTS `nerviooptico` (
  `codnerv` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codnerv`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular del nervio optico del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.ojo
CREATE TABLE IF NOT EXISTS `ojo` (
  `codojo` int(11) NOT NULL,
  `Descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  PRIMARY KEY (`codojo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Especifica el tipo de ojo 1 Izquierdo 2 derecho';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.orbitasycejas
CREATE TABLE IF NOT EXISTS `orbitasycejas` (
  `codorb` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codorb`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Saludo ocular de las orbitas y cejas';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.paciente
CREATE TABLE IF NOT EXISTS `paciente` (
  `codpaciente` int(11) NOT NULL,
  `nombre1` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `nombre2` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `apellido1` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `apellido2` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `apellido3` varchar(50) COLLATE utf8_spanish_ci DEFAULT '',
  `telefono1` varchar(12) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `telefono2` varchar(12) COLLATE utf8_spanish_ci DEFAULT '',
  `fechanac` date NOT NULL DEFAULT '0000-00-00',
  `direccion` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `cui` varchar(13) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `nit` varchar(13) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `profesion` varchar(13) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `codcategoria` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codpaciente`),
  KEY `FK_paciente_categoria` (`codcategoria`),
  CONSTRAINT `FK_paciente_categoria` FOREIGN KEY (`codcategoria`) REFERENCES `categoria` (`codcategoria`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='paciente de la consulta a la optica';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.parpadosypestanias
CREATE TABLE IF NOT EXISTS `parpadosypestanias` (
  `codparp` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codparp`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de los Parpados y PestaÃ±as del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.puesto
CREATE TABLE IF NOT EXISTS `puesto` (
  `codpuesto` int(11) NOT NULL AUTO_INCREMENT,
  `nombrepuesto` varchar(100) COLLATE utf8_spanish_ci NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codpuesto`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci;

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.pupila
CREATE TABLE IF NOT EXISTS `pupila` (
  `codpupila` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codpupila`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de la puila del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.refraccionfinal
CREATE TABLE IF NOT EXISTS `refraccionfinal` (
  `codrf` int(11) NOT NULL,
  `esfera` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `cilindro` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `avcc` double NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL DEFAULT '0',
  `codtipoav` int(11) NOT NULL DEFAULT '0',
  `descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '0',
  PRIMARY KEY (`codrf`),
  KEY `FK_refraccionfinal_ojo` (`codojo`),
  KEY `FK_refraccionfinal_tipoav` (`codtipoav`),
  CONSTRAINT `FK_refraccionfinal_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`),
  CONSTRAINT `FK_refraccionfinal_tipoav` FOREIGN KEY (`codtipoav`) REFERENCES `tipoav` (`codtipoav`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='refraccion Final despues del examen';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.refraccionobjetiva
CREATE TABLE IF NOT EXISTS `refraccionobjetiva` (
  `codro` int(11) NOT NULL,
  `esfera` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `cilindro` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `eje` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `avcc` double NOT NULL DEFAULT '0',
  `autorefraccion` double NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL DEFAULT '0',
  `codec` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codro`),
  KEY `FK_refraccionobjetiva_ojo` (`codojo`),
  KEY `FK_refraccionobjetiva_examenclinico` (`codec`),
  CONSTRAINT `FK_refraccionobjetiva_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_refraccionobjetiva_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Refraccion Objetiva del ojo del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.refraccionsubjetiva
CREATE TABLE IF NOT EXISTS `refraccionsubjetiva` (
  `codrs` int(11) NOT NULL,
  `esfera` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `cilindro` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `eje` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `avcc` double NOT NULL DEFAULT '0',
  `codojo` int(11) NOT NULL DEFAULT '0',
  `codec` int(11) NOT NULL DEFAULT '0',
  PRIMARY KEY (`codrs`),
  KEY `FK_refraccionsubjetiva_ojo` (`codojo`),
  KEY `FK_refraccionsubjetiva_examenclinico` (`codec`),
  CONSTRAINT `FK_refraccionsubjetiva_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_refraccionsubjetiva_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Refraccion Subjetiva del ojo del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.retinaperiferica
CREATE TABLE IF NOT EXISTS `retinaperiferica` (
  `codretp` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codretp`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de la retina periferica del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.retinappost
CREATE TABLE IF NOT EXISTS `retinappost` (
  `codret` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codret`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular de la retina del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.saludocular
CREATE TABLE IF NOT EXISTS `saludocular` (
  `codsaludocular` int(11) NOT NULL,
  `codorb` int(11) NOT NULL,
  `codlag` int(11) NOT NULL,
  `codparp` int(11) NOT NULL,
  `codconj` int(11) NOT NULL,
  `codesclera` int(11) NOT NULL,
  `codcornea` int(11) NOT NULL,
  `codcam` int(11) NOT NULL,
  `codiris` int(11) NOT NULL,
  `codpupila` int(11) NOT NULL,
  `codcristalino` int(11) NOT NULL,
  `codvitreo` int(11) NOT NULL,
  `codnerv` int(11) NOT NULL,
  `codret` int(11) NOT NULL,
  `codretp` int(11) NOT NULL,
  `codojo` int(11) NOT NULL,
  `codec` int(11) NOT NULL,
  PRIMARY KEY (`codsaludocular`),
  KEY `FK_saludocular_orbitasycejas` (`codorb`),
  KEY `FK_saludocular_lagrimayvialagrimal` (`codlag`),
  KEY `FK_saludocular_parpadosypestanias` (`codparp`),
  KEY `FK_saludocular_conjuntiva` (`codconj`),
  KEY `FK_saludocular_esclera` (`codesclera`),
  KEY `FK_saludocular_cornea` (`codcornea`),
  KEY `FK_saludocular_camaraant` (`codcam`),
  KEY `FK_saludocular_iris` (`codiris`),
  KEY `FK_saludocular_pupila` (`codpupila`),
  KEY `FK_saludocular_cristalino` (`codcristalino`),
  KEY `FK_saludocular_vitreo` (`codvitreo`),
  KEY `FK_saludocular_nerviooptico` (`codnerv`),
  KEY `FK_saludocular_retinappost` (`codret`),
  KEY `FK_saludocular_retinaperiferica` (`codretp`),
  KEY `FK_saludocular_ojo` (`codojo`),
  KEY `FK_saludocular_examenclinico` (`codec`),
  CONSTRAINT `FK_saludocular_camaraant` FOREIGN KEY (`codcam`) REFERENCES `camaraant` (`codcam`),
  CONSTRAINT `FK_saludocular_conjuntiva` FOREIGN KEY (`codconj`) REFERENCES `conjuntiva` (`codconj`),
  CONSTRAINT `FK_saludocular_cornea` FOREIGN KEY (`codcornea`) REFERENCES `cornea` (`codcornea`),
  CONSTRAINT `FK_saludocular_cristalino` FOREIGN KEY (`codcristalino`) REFERENCES `cristalino` (`codcristalino`),
  CONSTRAINT `FK_saludocular_esclera` FOREIGN KEY (`codesclera`) REFERENCES `esclera` (`codesclera`),
  CONSTRAINT `FK_saludocular_examenclinico` FOREIGN KEY (`codec`) REFERENCES `examenclinico` (`codec`),
  CONSTRAINT `FK_saludocular_iris` FOREIGN KEY (`codiris`) REFERENCES `iris` (`codiris`),
  CONSTRAINT `FK_saludocular_lagrimayvialagrimal` FOREIGN KEY (`codlag`) REFERENCES `lagrimayvialagrimal` (`codlag`),
  CONSTRAINT `FK_saludocular_nerviooptico` FOREIGN KEY (`codnerv`) REFERENCES `nerviooptico` (`codnerv`),
  CONSTRAINT `FK_saludocular_ojo` FOREIGN KEY (`codojo`) REFERENCES `ojo` (`codojo`),
  CONSTRAINT `FK_saludocular_orbitasycejas` FOREIGN KEY (`codorb`) REFERENCES `orbitasycejas` (`codorb`),
  CONSTRAINT `FK_saludocular_parpadosypestanias` FOREIGN KEY (`codparp`) REFERENCES `parpadosypestanias` (`codparp`),
  CONSTRAINT `FK_saludocular_pupila` FOREIGN KEY (`codpupila`) REFERENCES `pupila` (`codpupila`),
  CONSTRAINT `FK_saludocular_retinaperiferica` FOREIGN KEY (`codretp`) REFERENCES `retinaperiferica` (`codretp`),
  CONSTRAINT `FK_saludocular_retinappost` FOREIGN KEY (`codret`) REFERENCES `retinappost` (`codret`),
  CONSTRAINT `FK_saludocular_vitreo` FOREIGN KEY (`codvitreo`) REFERENCES `vitreo` (`codvitreo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud Ocular del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.tipoav
CREATE TABLE IF NOT EXISTS `tipoav` (
  `codtipoav` int(11) NOT NULL,
  `Descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codtipoav`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Tipo de Agudeza visual para los lentes';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.tropia
CREATE TABLE IF NOT EXISTS `tropia` (
  `codtropia` int(11) NOT NULL,
  `tipotropia` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `Descripcion` text COLLATE utf8_spanish_ci,
  `Foto` varchar(50) COLLATE utf8_spanish_ci DEFAULT NULL,
  PRIMARY KEY (`codtropia`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Tropias en el Ojo';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.version
CREATE TABLE IF NOT EXISTS `version` (
  `codversion` int(11) NOT NULL,
  `tipoversion` varchar(50) COLLATE utf8_spanish_ci NOT NULL DEFAULT '',
  `descripcion` text COLLATE utf8_spanish_ci,
  `foto` varchar(50) COLLATE utf8_spanish_ci DEFAULT NULL,
  PRIMARY KEY (`codversion`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='versiones en el Ojo';

-- La exportaciÃ³n de datos fue deseleccionada.

-- Volcando estructura para tabla optica.vitreo
CREATE TABLE IF NOT EXISTS `vitreo` (
  `codvitreo` int(11) NOT NULL,
  `descripcion` text COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`codvitreo`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci COMMENT='Salud ocular del vitreo del paciente';

-- La exportaciÃ³n de datos fue deseleccionada.

/*!40101 SET SQL_MODE=IFNULL(@OLD_SQL_MODE, '') */;
/*!40014 SET FOREIGN_KEY_CHECKS=IF(@OLD_FOREIGN_KEY_CHECKS IS NULL, 1, @OLD_FOREIGN_KEY_CHECKS) */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
