# nationsTableSQL
Tabelas das Nações em SQL

# 🌍 Base de Dados Nation (SQL)

Este repositório contém o script completo de criação e povoamento da base de dados relacional **Nation**. É uma estrutura em MySQL / MariaDB ideal para estudos, testes de desempenho, consultas complexas, criação de dashboards e modelagem de dados geográficos e demográficos.

---

## 📌 Conteúdo da Base de Dados

A base de dados é composta por **7 tabelas interligadas** por chaves estrangeiras (`FOREIGN KEY`):

* **`continents`**: Registra os continentes mundiais.
* **`regions`**: Divisão regional associada a um continente (`continent_id`).
* **`countries`**: Informações dos países (código ISO2, ISO3, área total, data nacional e região).
* **`languages`**: Catálogo de línguas faladas ao redor do mundo.
* **`country_languages`**: Tabela de associação (N:M) relacionando países e idiomas, indicando se é o idioma oficial.
* **`country_stats`**: Séries históricas demográficas e econômicas por país e ano (População e PIB / GDP).
* **`region_areas`**: Registro de área por nome de região.

---

## 🗂️ Modelo Relacional (Estrutura Resumida)

[continents] 1 ─── N [regions] 1 ─── N [countries] 1 ─── N [country_stats]
│
1
│
N
[country_languages] N ─── 1 [languages]
