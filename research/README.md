Forschungsdaten
===============

Die Dateien enthalten sämtliche Informationen zu Forschungen.

Dateiname
---------

Der Dateiname folgt dem Schema "ID_NAME.json", wobei der Name ohne Leerzeichen, Sonderzeichen, etc. geschrieben werden muss
und nur Kleinbuchstaben enthalten darf (z.B. `905101_phasenkonverterfabrik.json`)

Struktur
--------

Die Struktur ist
immer gleich und wie folgt aufgebaut:

```metadata json
{
    "id": 1001, // Eindeutige ID der Forschung
    "name": "Basisforschung Föderation", // Name der Forschung
    "description": "Grundforschung der Föderation um weitere Forschungen zu beginnen", // Beschreibung der Forschung
    "sort_order": 1, // Position in der Sortierungsreihenfolge
    "commodity_id": 1701, // ID der Ware/des Effekts, die zur Forschung benötigt werden
    "points": 0, // Anzahl an Punkten (also z.B. Waren, Effekte) die diese Forschung benötigt
    "ship_rump_id": 0, // ID des Schiff-Rumpfs, der durch diese Forschung freigeschaltet wird
    "database_entry_ids": [], // Datenbank-Einträge, die durch diese Forschung freigeschaltet werden
    "raise_planetlimit": 1, // Erhöhung des Planetenlimits durch diese Forschung
    "raise_moonlimit": 0, // Erhöhrung des Mondlimits durch diese Forschung
    "dependencies": {
        "requires": [
            [
                1234 // ID der Forschungen, die zwingend benötigt werden
	    ]
        ],
        "requires_one_of": [
            [
                5678, // ID der Forschungen, von denen mindestens eine benötigt wird
                9012,
	    ]
        ],
        "excludes": [
            [
                3456 // ID der Forschungen, die von dieser Forschung ausgeschlossen werden
	    ]
        ]
    }
}
```
