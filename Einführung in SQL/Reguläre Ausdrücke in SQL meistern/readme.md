# Reguläre Ausdrücke in SQL meistern

Reguläre Ausdrücke (engl. *Regular Expressions*, kurz **Regex**) sind leistungsstarke Werkzeuge, um **Textmuster** zu erkennen, zu filtern oder zu validieren. In SQL bieten viele Datenbanksysteme Unterstützung für Regex, um komplexe **Suchbedingungen** effizient umzusetzen.

## 🔍 Was sind reguläre Ausdrücke?

Ein regulärer Ausdruck ist ein Suchmuster, das aus Zeichen, Symbolen und Regeln besteht, um bestimmte Zeichenfolgen zu erkennen.

Beispiele:
- `^A` → beginnt mit A
- `a$` → endet mit a
- `a.*b` → enthält ein „a“ gefolgt von einem „b“
- `[0-9]{3}` → exakt drei Ziffern

## 🛠️ Regex in SQL verwenden

Je nach Datenbanksystem variiert die Syntax leicht.

### ✅ In **PostgreSQL**:

```sql
SELECT * 
FROM Kunden
WHERE Name ~ '^[A-Za-z]{3,}$';

~ steht für "entspricht dem regulären Ausdruck". Obige Abfrage findet Namen mit mindestens 3 Buchstaben.

SELECT * 
FROM Kunden
WHERE Name REGEXP '^A.*a$';

REGEXP ist der Operator für reguläre Ausdrücke in MySQL.

✅ In SQLite:
SQLite unterstützt standardmäßig keine regulären Ausdrücke, aber man kann eigene Funktionen einbinden oder Workarounds nutzen.

🎯 Praxisbeispiel: Namen mit genau zwei „A“

SELECT * 
FROM Kunden
WHERE LOWER(Name) REGEXP '^[^aA]*[aA][^aA]*[aA][^aA]*$';

Diese Abfrage sucht nach genau zwei „a“ oder „A“ im Namen (Groß-/Kleinschreibung wird ignoriert).

🧠 Warum Regex in SQL nützlich ist
Datenvalidierung (z. B. E-Mails, Telefonnummern)

Erkennung von Mustern in Textdaten

Flexible Textsuche in unstrukturierten Daten

Kombinierbar mit LIKE, REPLACE, SUBSTRING, CASE usw.

🚀 Fazit
Die Beherrschung von regulären Ausdrücken in SQL erweitert deine Möglichkeiten bei der Datenanalyse erheblich.
Sie ermöglichen komplexe Textabfragen, die mit einfachen LIKE-Operatoren nicht möglich wären.

🔗 Tipp: Übe mit Tools wie regex101.com und kombiniere SQL-Abfragen mit Mustertests!






