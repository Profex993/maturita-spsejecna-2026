# **Relační databázové systémy \- popis architektury klient-server, komponenty a jejich činnost, multitasking, rozdíl mezi relačním a nerelačním DBS, porovnání struktury a způsob ukládání** {#relační-databázové-systémy---popis-architektury-klient-server,-komponenty-a-jejich-činnost,-multitasking,-rozdíl-mezi-relačním-a-nerelačním-dbs,-porovnání-struktury-a-způsob-ukládání}

[**Relační databázové systémy \- popis architektury klient-server, komponenty a jejich činnost, multitasking, rozdíl mezi relačním a nerelačním DBS, porovnání struktury a způsob ukládání	1**](#relační-databázové-systémy---popis-architektury-klient-server,-komponenty-a-jejich-činnost,-multitasking,-rozdíl-mezi-relačním-a-nerelačním-dbs,-porovnání-struktury-a-způsob-ukládání)

[Architektura klient-server	2](#architektura-klient-server)

[Klient	2](#klient)

[Server	2](#server)

[RDBMS (Relational Database Management System)	2](#rdbms-\(relational-database-management-system\))

[Datové úložiště (Storage / Data files)	2](#datové-úložiště-\(storage-/-data-files\))

[Síťová vrstva	2](#síťová-vrstva)

[Jaké jsou DB servery	2](#jaké-jsou-db-servery)

[Multitasking v databázovém serveru	3](#multitasking-v-databázovém-serveru)

[Relační vs. nerelační databázové systémy	3](#relační-vs.-nerelační-databázové-systémy)

[Porovnání struktury a způsobu ukládání	3](#porovnání-struktury-a-způsobu-ukládání)

## 

## Architektura klient-server {#architektura-klient-server}

* Architektura klient–server znamená oddělení databázových služeb od klienta  
  * klient posílá požadavky (SQL dotazy) a server je zpracovává a vrací výsledky.

### Klient {#klient}

* aplikace, která odesílá SQL dotazy na databázový server  
* (program, se kterým pracuje uživatel)  
* nepracuje přímo s daty – jen požaduje jejich zpracování  
* může být grafické prostředí nebo jiná aplikace  
* např. SQL Developer, phpMyAdmin, MS Access, webová aplikace

### Server {#server}

* databázový systém, který dotazy zpracovává

#### RDBMS (Relational Database Management System) {#rdbms-(relational-database-management-system)}

* To je software, který řídí přístup k datům.  
* Zajišťuje např.:  
  * zpracování SQL dotazů (parser, optimalizátor, plánovač)  
  * řízení transakcí (BEGIN, COMMIT, ROLLBACK)  
  * zajištění konzistence a integrity dat (PRIMARY KEY, FOREIGN KEY, CHECK)  
  * řízení přístupu uživatelů (role, práva)  
  * řízení pořadí a plánování dotazů  
  * zpracování uzamykání (locků) při více přístupech zároveň  
  * správu paměti, cache, indexů

#### Datové úložiště (Storage / Data files) {#datové-úložiště-(storage-/-data-files)}

* fyzická část serveru, kde jsou uložena data, indexy, logy, metadata  
* RDBMS k nim přistupuje a zajišťuje jejich správu  
* může být na disku nebo v paměti

#### Síťová vrstva {#síťová-vrstva}

* přenos dat mezi klientem a serverem  
* často přes TCP/IP  
* zajišťuje komunikaci v architektuře klient–server

### Jaké jsou DB servery {#jaké-jsou-db-servery}

| Název | Typ | Popis / použití |
| ----- | ----- | ----- |
| **Oracle Database** | Komerční | Výkonný podnikový databázový server, často v bankách a velkých firmách |
| **Microsoft SQL Server** | Komerční | Používaný v prostředí Windows, dobrá integrace s MS nástroji |
| **MySQL / MariaDB** | Open-source | Oblíbený pro webové aplikace (WordPress, PHP, atd.) |
| **PostgreSQL** | Open-source | Velmi pokročilý, univerzální, často označovaný jako „open-source Oracle“ |
| **SQLite** | Embedded | Malý databázový systém pro mobilní nebo lokální aplikace, běží přímo u klienta |

### Multitasking v databázovém serveru {#multitasking-v-databázovém-serveru}

* Databázový server umožňuje současný přístup více klientů díky multitaskingu a řízení přístupu.

## Relační vs. nerelační databázové systémy {#relační-vs.-nerelační-databázové-systémy}

| Vlastnost | Relační DB (RDBMS) | Nerelační DB (NoSQL) |
| ----- | ----- | ----- |
| Struktura dat | Tabulky (řádky, sloupce) | Dokumenty, klíč–hodnota, grafy, kolekce |
| Jazyk | SQL | Různé (např. Mongo Query Language, Gremlin) |
| Schéma | Pevně dané (nutno definovat atributy) | Flexibilní (lze měnit strukturu dat) |
| Integrita dat | Silná (PRIMARY, FOREIGN KEY, transakce) | Slabší, často bez vazeb |
| Vhodné pro | Finanční systémy, evidence, přesná data | Velká nestrukturovaná data, webové aplikace |
| Příklady | Oracle, MySQL, PostgreSQL | MongoDB, Cassandra, Redis |

### Porovnání struktury a způsobu ukládání {#porovnání-struktury-a-způsobu-ukládání}

| Oblast | Relační DB | Nerelační DB |
| ----- | ----- | ----- |
| **Ukládání dat** | Do tabulek, řádky \= záznamy, sloupce \= atributy | Do dokumentů, objektů nebo klíč–hodnota párů |
| **Vazby mezi daty** | Pomocí cizích klíčů (relace) | Vazby často neexistují nebo se ukládají uvnitř dokumentu |
| **Transakce** | Ano (ACID – Atomicity, Consistency, Isolation, Durability) | Často částečné nebo asynchronní |
| **Normalizace** | Ano (odstranění redundance) | Ne, často duplikace dat kvůli výkonu |
| **Rychlost** | Stabilní, ale pomalejší u velkých dat | Rychlejší při práci s velkými nestrukturovanými daty |

# 

# 

# 

# 

# 

# 

