# sql-codes
-- MySQL dump 10.13  Distrib 8.0.36, for Win64 (x86_64)
--
-- Host: 127.0.0.1    Database: cadastro
-- ------------------------------------------------------
-- Server version	5.5.5-10.4.28-MariaDB

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;


CREATE TABLE `cursos` (
  `idcurso` int(11) NOT NULL DEFAULT 0,
  `nome` varchar(30) NOT NULL,
  `descricao` text DEFAULT NULL,
  `carga` int(10) UNSIGNED DEFAULT NULL,
  `totaulas` int(10) UNSIGNED DEFAULT NULL,
  `ano` year(4) DEFAULT 2016
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Despejando dados para a tabela `cursos`
--

INSERT INTO `cursos` (`idcurso`, `nome`, `descricao`, `carga`, `totaulas`, `ano`) VALUES
(1, 'HTML5', 'Curso de HTML5', 40, 37, '2014'),
(2, 'Algoritmos', 'Lógica de Programação', 20, 15, '2014'),
(3, 'pphotoshop', 'Dicas de Photoshop CC', 10, 8, '2014'),
(4, 'PHP', 'Curso de PHP para iniciantes', 40, 20, '2015'),
(5, 'Java', 'Introdução à Linguagem Java', 40, 29, '2015'),
(6, 'MySQL', 'Bancos de Dados MySQL', 30, 15, '2016'),
(7, 'Word', 'Curso completo de Word', 40, 30, '2016'),
(8, 'Python', 'Curso de Python', 40, 18, '2017'),
(10, 'Excel', 'Curso completo de Excel', 40, 30, '2017'),
(11, 'Responsividade', 'Curso de Responsividade', 30, 15, '2018'),
(12, 'C++', 'Curso de C++ com Orientação a Objetos', 40, 25, '2017'),
(13, 'C#', 'Curso de C#', 30, 12, '2017'),
(14, 'Android', 'Curso de Desenvolvimento de Aplicativos para Android', 60, 30, '2018'),
(15, 'JavaScript', 'Curso de JavaScript', 35, 18, '2017'),
(16, 'PowerPoint', 'Curso completo de PowerPoint', 30, 12, '2018'),
(17, 'Swift', 'Curso de Desenvolvimento de Aplicativos para iOS', 60, 30, '2019'),
(18, 'Hardware', 'Curso de Montagem e Manutenção de PCs', 30, 12, '2017'),
(19, 'Redes', 'Curso de Redes para Iniciantes', 40, 15, '2016'),
(20, 'Segurança', 'Curso de Segurança', 15, 8, '2018'),
(21, 'SEO', 'Curso de Otimização de Sites', 30, 12, '2017'),
(22, 'Premiere', 'Curso de Edição de Vídeos com Premiere', 20, 10, '2017'),
(23, 'After Effects', 'Curso de Efeitos em Vídeos com After Effects', 20, 10, '2018'),
(24, 'WordPress', 'Curso de Criação de Sites com WordPress', 60, 30, '2019'),
(25, 'Joomla', 'Curso de Criação de Sites com Joomla', 60, 30, '2019'),
(26, 'Magento', 'Curso de Criação de Lojas Virtuais com Magento', 50, 25, '2019'),
(27, 'Modelagem de Dados', 'Curso de Modelagem de Dados', 30, 12, '2020'),
(29, 'PHP7', 'Curso de PHP, versão 7.0', 40, 20, '2020'),
(30, 'PHP4', 'Curso de PHP, versão 4.0', 30, 11, '2010');

-- --------------------------------------------------------

--
-- Estrutura para tabela `family`
--

CREATE TABLE `family` (
  `codigo` int(11) DEFAULT NULL,
  `id` int(11) NOT NULL,
  `nome` varchar(30) NOT NULL,
  `prof` varchar(20) DEFAULT NULL,
  `nascimento` date DEFAULT NULL,
  `sexo` enum('M','F') DEFAULT NULL,
  `peso` decimal(5,2) DEFAULT NULL,
  `altura` decimal(3,2) DEFAULT NULL,
  `nacionalidade` varchar(20) DEFAULT 'Brasil'
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Despejando dados para a tabela `family`
--

INSERT INTO `family` (`codigo`, `id`, `nome`, `prof`, `nascimento`, `sexo`, `peso`, `altura`, `nacionalidade`) VALUES
(NULL, 4, 'diogo', '', '2002-01-16', 'F', 90.90, 1.68, 'americano'),
(NULL, 5, 'felipe', '', '2002-01-16', 'F', 68.50, 1.68, 'americano'),
(NULL, 6, 'henrry', '', '1993-01-16', 'M', 68.50, 1.68, 'americano'),
(NULL, 7, 'MAE', '', '1993-01-16', 'F', 68.50, 1.68, 'braisl'),
(NULL, 8, 'MAE', '', '1993-01-16', 'F', 68.50, 1.68, 'braisl'),
(NULL, 9, 'JEOGE', '', '1993-01-16', 'F', 68.50, 1.68, 'italia'),
(NULL, 10, 'obama', '', '2000-02-02', 'M', 20.00, 9.99, 'pportugal'),
(NULL, 11, 'janaina', '', '1990-01-01', 'F', 10.00, 9.99, 'inglaterra');

-- --------------------------------------------------------

--
-- Estrutura para tabela `gafanhotos`
--

CREATE TABLE `gafanhotos` (
  `id` int(11) NOT NULL,
  `nome` varchar(30) NOT NULL,
  `profissao` varchar(20) DEFAULT NULL,
  `nascimento` date DEFAULT NULL,
  `sexo` enum('M','F') DEFAULT NULL,
  `peso` decimal(5,2) DEFAULT NULL,
  `altura` decimal(3,2) DEFAULT NULL,
  `nacionalidade` varchar(20) DEFAULT 'Brasil',
  `cursopreferido` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Despejando dados para a tabela `gafanhotos`
--

INSERT INTO `gafanhotos` (`id`, `nome`, `profissao`, `nascimento`, `sexo`, `peso`, `altura`, `nacionalidade`, `cursopreferido`) VALUES
(1, 'Daniel Morais', 'Auxiliar Administrat', '1984-01-02', 'M', 78.50, 1.83, 'Brasil', 6),
(2, 'Talita Nascimento', 'Farmacêutico', '1999-12-30', 'F', 55.20, 1.65, 'Portugal', 22),
(3, 'Emerson Gabriel', 'Programador', '1920-12-30', 'M', 50.20, 1.65, 'Moçambique', 12),
(4, 'Lucas Damasceno', 'Auxiliar Administrat', '1930-11-02', 'M', 63.20, 1.75, 'Irlanda', 7),
(5, 'Leila Martins', 'Farmacêutico', '1975-04-22', 'F', 99.00, 2.15, 'Brasil', 1),
(6, 'Letícia Neves', 'Programador', '1999-12-03', 'F', 87.00, 2.00, 'Brasil', 8),
(7, 'Janaína Couto', 'Auxiliar Administrat', '1987-11-12', 'F', 75.40, 1.66, 'EUA', 4),
(8, 'Carlisson Rosa', 'Professor', '2010-08-01', 'M', 78.22, 1.98, 'Brasil', 5),
(9, 'Jackson Telles', 'Programador', '1999-01-23', 'M', 55.75, 1.33, 'Portugal', 3),
(10, 'Danilo Araujo', 'Dentista', '1975-12-10', 'M', 99.21, 1.87, 'EUA', 30),
(11, 'Andreia Delfino', 'Auxiliar Administrat', '1975-07-01', 'F', 48.64, 1.54, 'Irlanda', 22),
(12, 'Valter Vilmerson', 'Ator', '1985-10-12', 'M', 88.55, 2.03, 'Brasil', 6),
(13, 'Allan Silva', 'Programador', '1993-11-11', 'M', 76.99, 1.55, 'Brasil', 6),
(14, 'Rosana Kunz', 'Professor', '1935-01-16', 'F', 55.24, 1.87, 'Brasil', 1),
(15, 'Josiane Dutra', 'Empreendedor', '1950-01-20', 'F', 98.70, 1.04, 'Portugal', 6),
(16, 'Elvis Schwarz', 'Dentista', '2011-05-07', 'M', 66.69, 1.76, 'EUA', 6),
(17, 'Paulo Narley', 'Auxiliar Administrat', '1997-03-17', 'M', 120.10, 2.22, 'Brasil', 6),
(18, 'Joade Assis', 'Médico', '1930-12-01', 'M', 65.88, 1.78, 'França', 6),
(19, 'Nara Matos', 'Programador', '1978-03-17', 'F', 65.90, 1.33, 'Brasil', 6),
(20, 'Marcos Dissotti', 'Empreendedor', '2010-01-01', 'M', 53.79, 1.54, 'Portugal', 6),
(21, 'Ana Carolina Mendes', 'Ator', '2000-12-15', 'F', 88.30, 1.54, 'Brasil', 6),
(22, 'Guilherme de Sousa', 'Dentista', '2001-05-18', 'M', 132.70, 1.97, 'Moçambique', 6),
(23, 'Bruno Torres', 'Auxiliar Administrat', '2000-01-30', 'M', 44.65, 1.65, 'Brasil', 6),
(24, 'Yuji Homa', 'Empreendedor', '1996-12-25', 'M', 33.90, 1.22, 'Japão', 6),
(25, 'Raian Porto', 'Programador', '1989-05-05', 'M', 54.89, 1.54, 'Brasil', 6),
(26, 'Paulo Batista', 'Ator', '1999-03-15', 'M', 110.12, 1.87, 'Portugal', 6),
(27, 'Monique Precivalli', 'Auxiliar Administrat', '2013-12-30', 'F', 48.20, 1.22, 'Brasil', 6),
(28, 'Herisson Silva', 'Auxiliar Administrat', '1965-10-10', 'M', 74.65, 1.56, 'EUA', 6),
(29, 'Tiago Ulisses', 'Dentista', '1993-04-22', 'M', 150.30, 2.35, 'Brasil', 6),
(30, 'Anderson Rafael', 'Programador', '1989-12-01', 'M', 64.22, 1.44, 'Irlanda', 6),
(31, 'Karine Ribeiro', 'Empreendedor', '1988-10-01', 'F', 42.10, 1.65, 'Brasil', 6),
(32, 'Roberto Luiz Debarba', 'Ator', '2007-01-09', 'M', 77.44, 1.56, 'Brasil', 6),
(33, 'Jarismar Andrade', 'Dentista', '2000-06-23', 'F', 63.70, 1.33, 'Brasil', 6),
(34, 'Janaina Oliveira', 'Professor', '1955-03-12', 'F', 52.90, 1.76, 'Canadá', 6),
(35, 'Márcio Mello', 'Programador', '2011-11-20', 'M', 54.11, 1.55, 'EUA', 6),
(36, 'Robson Rodolpho', 'Auxiliar Administrat', '2000-08-08', 'M', 110.10, 1.76, 'Brasil', 6),
(37, 'Daniele Moledo', 'Empreendedor', '2006-08-11', 'F', 101.30, 1.99, 'Brasil', 6),
(38, 'Neto Sophiate', 'Ator', '1996-05-17', 'M', 59.28, 1.65, 'Portugal', 6),
(39, 'Neriton Dias', 'Auxiliar Administrat', '2009-10-30', 'M', 48.99, 1.29, 'Brasil', 6),
(40, 'André Schmidt', 'Programador', '1993-07-26', 'M', 55.37, 1.22, 'Angola', 6),
(41, 'Isaias Buscarino', 'Dentista', '2001-01-07', 'M', 99.90, 1.55, 'Moçambique', 6),
(42, 'Rafael Guimma', 'Empreendedor', '1968-04-11', 'M', 88.88, 1.54, 'Brasil', 6),
(43, 'Ana Carolina Hernandes', 'Ator', '1970-10-11', 'F', 65.40, 2.08, 'EUA', 6),
(44, 'Luiz Paulo', 'Professor', '1984-11-01', 'M', 75.12, 1.38, 'Portugal', 6),
(45, 'Bruna Teles', 'Programador', '1980-11-07', 'F', 55.10, 1.86, 'Brasil', 6),
(46, 'Diogo Padilha', 'Auxiliar Administrat', '2000-03-03', 'M', 54.34, 1.88, 'Angola', 6),
(47, 'Bruno Miltersteiner', 'Dentista', '1986-02-19', 'M', 77.45, 1.65, 'Alemanha', 6),
(48, 'Elaine Nunes', 'Programador', '1998-08-15', 'F', 35.90, 2.00, 'Canadá', 6),
(49, 'Silvio Ricardo', 'Programador', '2012-03-12', 'M', 65.99, 1.23, 'EUA', 6),
(50, 'Denilson Barbosa da Silva', 'Empreendedor', '2000-01-08', 'M', 97.30, 2.00, 'Brasil', 6),
(51, 'Jucinei Teixeira', 'Professor', '1977-11-22', 'F', 44.80, 1.76, 'Portugal', 6),
(52, 'Bruna Santos', 'Auxiliar Administrat', '1991-12-01', 'F', 76.30, 1.45, 'Canadá', 6),
(53, 'André Vitebo', 'Médico', '1970-07-01', 'M', 44.11, 1.55, 'Brasil', 6),
(54, 'Andre Santini', 'Programador', '1991-08-15', 'M', 66.00, 1.76, 'Itália', 6),
(55, 'Ruan Valente', 'Programador', '1998-03-19', 'M', 101.90, 1.76, 'Canadá', 6),
(56, 'Nailton Mauricio', 'Médico', '1992-04-25', 'M', 86.01, 1.43, 'EUA', 6),
(57, 'Rita Pontes', 'Professor', '1999-09-02', 'F', 54.10, 1.35, 'Angola', 6),
(58, 'Carlos Camargo', 'Programador', '2005-02-22', 'M', 124.65, 1.33, 'Brasil', 6),
(59, 'Philppe Oliveira', 'Auxiliar Administrat', '2000-05-23', 'M', 105.10, 2.19, 'Brasil', 6),
(60, 'Dayana Dias', 'Professor', '1993-05-30', 'F', 88.30, 1.66, 'Angola', 6),
(61, 'Silvana Albuquerque', 'Programador', '1999-05-22', 'F', 56.00, 1.50, 'Brasil', 6);

-- --------------------------------------------------------

--
-- Estrutura para tabela `gafanhoto_assiste_curso`
--![diagram](https://github.com/felipe6819/sql-codes/assets/128556670/9a21b365-37b8-4f66-92f9-f9154c95f776)




CREATE TABLE `gafanhoto_assiste_curso` (
  `id` int(11) NOT NULL,
  `data` date DEFAULT NULL,
  `idgafanhoto` int(11) DEFAULT NULL,
  `idcurso` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

--
-- Despejando dados para a tabela `gafanhoto_assiste_curso`
--

INSERT INTO `gafanhoto_assiste_curso` (`id`, `data`, `idgafanhoto`, `idcurso`) VALUES
(1, '2014-03-01', 1, 2),
(2, '2015-12-22', 3, 6),
(3, '2014-01-01', 22, 12),
(4, '2016-05-12', 1, 19);

--
-- Índices para tabelas despejadas
--

--
-- Índices de tabela `cursos`
--
ALTER TABLE `cursos`
  ADD PRIMARY KEY (`idcurso`),
  ADD UNIQUE KEY `nome` (`nome`);

--
-- Índices de tabela `family`
--
ALTER TABLE `family`
  ADD PRIMARY KEY (`id`);

--
-- Índices de tabela `gafanhotos`
--
ALTER TABLE `gafanhotos`
  ADD PRIMARY KEY (`id`),
  ADD KEY `cursopreferido` (`cursopreferido`);

--
-- Índices de tabela `gafanhoto_assiste_curso`
--
ALTER TABLE `gafanhoto_assiste_curso`
  ADD PRIMARY KEY (`id`),
  ADD KEY `idgafanhoto` (`idgafanhoto`),
  ADD KEY `idcurso` (`idcurso`);

--
-- AUTO_INCREMENT para tabelas despejadas
--

--
-- AUTO_INCREMENT de tabela `family`
--
ALTER TABLE `family`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=12;

--
-- AUTO_INCREMENT de tabela `gafanhotos`
--
ALTER TABLE `gafanhotos`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=62;

--
-- AUTO_INCREMENT de tabela `gafanhoto_assiste_curso`
--
ALTER TABLE `gafanhoto_assiste_curso`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5;

--
-- Restrições para tabelas despejadas
--

--
-- Restrições para tabelas `gafanhotos`
--
ALTER TABLE `gafanhotos`
  ADD CONSTRAINT `gafanhotos_ibfk_1` FOREIGN KEY (`cursopreferido`) REFERENCES `cursos` (`idcurso`);

--
-- Restrições para tabelas `gafanhoto_assiste_curso`
--
ALTER TABLE `gafanhoto_assiste_curso`
  ADD CONSTRAINT `gafanhoto_assiste_curso_ibfk_1` FOREIGN KEY (`idgafanhoto`) REFERENCES `gafanhotos` (`id`),
  ADD CONSTRAINT `gafanhoto_assiste_curso_ibfk_2` FOREIGN KEY (`idcurso`) REFERENCES `cursos` (`idcurso`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
