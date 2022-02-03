# Krajské a obecní úřední desky

Podle specifikace https://datatracker.ietf.org/doc/html/rfc4287

Inspirováno pražským Geoportálem http://opendata.iprpraha.cz/feed.xml

## Idea

Obsah úředních desek by se mohl sdílet pomocí ATOM feedů. Obce by mohly svůj
obsah přebírat z krajů automatizovaně. 

Obce by na svých deskách mohly odkazovat na krajské nástěnky. 

ATOM je jednoduchý, dobře se parseruje, většina systémů pro něj má podporu. ATOM
je podobný RSS (ale modernější a navržený otevřeným způsobem).

## Schema

```
+---------------+
| Krajská deska |
+---------------+--+
|                  |
| * Oznámení 1     |
| * Oznámení 2     |
| * Oznámení 3     |
| * ...            |
+------------------+
       ^
       |
       | ATOM
       |
+--------------+
| Obecní deska |
+--------------+------------+
| * Odkaz na Krajskou desku |
| * Oznámení Obce 1         |
| * Oznámení Obce 2         |
| * Oznámení Obce 2         |
| * ...                     |
+---------------------------+
```

Příklady obsahu úředních desek dostupných ve formátu ATOM:

* [Kraj](sample/kraj1.xml)
* [Obec](sample/obec1.xml)
