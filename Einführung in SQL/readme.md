
<!-- HTML for full-width image -->
<img src="introduction%20sql.png" alt="Introduction SQL" style="width:100%; display:block; margin: 0 auto;" />



# Einführung in SQL

SQL (Structured Query Language) ist die standardisierte Sprache zur Verwaltung und Abfrage von Datenbanken. Diese Sprache bildet das Herzstück nahezu aller modernen Datenbanksysteme und ist ein unverzichtbares Werkzeug für Datenanalysten, Entwickler und Systemadministratoren.

## Was ist SQL?

- SQL steht für **Structured Query Language**
- SQL ermöglicht den **Zugriff auf Datenbanken** sowie deren **Manipulation**
- SQL wurde **1986** vom ANSI (American National Standards Institute) und **1987** von der ISO (International Organization for Standardization) als Standard anerkannt

## Was kann SQL?

SQL bietet eine Vielzahl von Funktionen zur Datenbankverwaltung:

- Abfragen von Daten mit `SELECT`
- Einfügen neuer Datensätze mit `INSERT`
- Aktualisieren vorhandener Daten mit `UPDATE`
- Löschen von Datensätzen mit `DELETE`
- Erstellen neuer Datenbanken mit `CREATE DATABASE`
- Erstellen von Tabellen mit `CREATE TABLE`
- Anlegen von Views und gespeicherten Prozeduren (`VIEW`, `STORED PROCEDURE`)
- Verwalten von Benutzerrechten und Berechtigungen

## SQL ist ein Standard – aber...

Obwohl SQL ein ANSI/ISO-Standard ist, existieren verschiedene Versionen und Dialekte. Jeder Hersteller (z. B. MySQL, Oracle, SQL Server) implementiert zusätzliche **proprietäre Erweiterungen**.

✅ Die **Kernbefehle** wie `SELECT`, `UPDATE`, `DELETE`, `INSERT` und `WHERE` sind jedoch in fast allen SQL-Versionen gleich oder sehr ähnlich.

## SQL auf Websites verwenden

Um eine datenbankgestützte Website zu erstellen, benötigst du:

1. Ein RDBMS (z. B. MySQL, SQL Server, MS Access)
2. Eine serverseitige Scriptsprache (z. B. PHP, ASP)
3. SQL zur Datenabfrage
4. HTML und CSS zur Darstellung der Inhalte

## Was ist ein RDBMS?

RDBMS steht für **Relationales Datenbankmanagementsystem** und bildet die Grundlage für SQL.

### Merkmale eines RDBMS:

- Daten werden in **Tabellen** gespeichert
- Tabellen bestehen aus **Zeilen (Datensätzen)** und **Spalten (Felder)**
- Jedes Feld speichert **spezifische Informationen**

### Beispiel: Kunden-Tabelle

```sql
SELECT * FROM Customers;

Struktur:

CustomerID	CustomerName	ContactName	Address	City	PostalCode	Country

Eine Zeile (Datensatz) repräsentiert einen Kunden

Eine Spalte (Feld) enthält Informationen zu einem bestimmten Attribut (z. B. CustomerName)

Fazit
SQL ist eine mächtige Sprache, die in der modernen Datenwelt unverzichtbar ist. Mit SQL kannst du Daten abfragen, verändern und strukturieren – effizient, standardisiert und flexibel. Ganz gleich, ob du Webanwendungen entwickelst oder große Datenanalysen durchführst – SQL gehört zu den wichtigsten Werkzeugen, die du beherrschen solltest.

