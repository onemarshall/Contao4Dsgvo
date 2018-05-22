# Contao4Dsgvo

Dieses Modul erzeugt eine neue Checkbox mit dem Namen "dsgvo". Ein Javascript im Frontend versteckt die Checkbox und fügt stattdessen ein Modal ein. Das Modal erscheit sobald alle Required-Felder ausgefüllt wurden und der Senden-Button geklickt wird.

Das Formular wird allerdings erst abgesendet, nachdem der Benutzer im Modal den Datenschutz zur Kentniss genommen hat.

## UX

Das Modal öffnet sich aus dem Sende-Button heraus. Der Benutzer bekommt nicht das unwohle Gefühl eines Werbe-Popups/Overlay sondern eine direkt zusammenhängende Information. Dadurch ist der Benutzer gezwungen, die Informationen zur kenntniss zu nehmen und kann den Vorgang abbrechen oder akzektieren, indem er fortfährt.

Der Vorgang wirkt weniger abschreckend, als eine Checkbox-Wüste und kann bequem weitergeklickt werden.

## Installation

- (Contao Manager) Suche nach `sioweb/dsgvo`
- (Oder über Console) `composer require sioweb/dsgvo`
- Lege das Eingabefeld `DSGVO Feld` in deinem Formular an
- Name kann/darf nicht geändert werden
- Pflichtfeld-Checkbox muss aktiviert werden (Wird ohne Javascript ausgegeben)
- In das erste Optionen-Feld [JA] und [DATENSCHUTZTEXT EINFÜGEN] einfügen
- Fülle die DSGVO-Einstellungen aus (Es sind inserttags erlaubt!)
- Den Absende-Button des Formulares umbenennen in z.B. `Prüfen und Absenden`
- Testen (Es müssen alle Pflichtfelder aktiviert werden!)
    - GGf. funktioniert die Validierung nicht mehr richtig
    
## Hintergrund

Die DSGVO setzt vorraus, dass der Absender ausreichend über Zweck und Dauer der Datenerhebung aufgeklärt wird. Idealerweise sollte die Einwilligung zu Beweiszwecken dokumentiert werden. Dieses Modul verhindert, dass der Benutzer das Formular ohne Kentnissnahme absenden kann indem es den Absender in einem zweiten Schritt explizit auf den Datenschutz hinweist.

Die Checkbox wird im Hintergrund vor dem Absenden aktiv gesetzt und kann im E-Mail-Template hinterlegt und somit auch dokumentiert werden.

Sollte `kein Javascript` aktiviert sein, wird die Checkbox ausgegeben. Daher ist es Ratsam das Formular mit Javascript und einmal mit deaktiviertem Javascript (Developer Tools) zu testen.

## Rechtliches

1. Es wird keine Gewährleistung gegeben, dass dieses Modul rechtssicher eingesetzt werden kann. Jeder Benutzer ist selbst, für die Rechtsicherheit verantwortlich und muss sich durch einen Rechtsexperten / Berater beraten und absichern lassen.

2. Das Modul legitimiert keine dauerhafte Speicherung der erhobenen Daten und ist nicht gedacht, die Gesetze zu umgehen oder auszuhebeln. Dieses Modul bietet lediglich eine alternative zu Checkboxen.

3. Das Modul wurde erstellt mit der Ansicht, dass eine explizite Information, mit erneutem Auffordern zum Absenden, die gleiche Gewichtung wie eine explizite Checkbox zum Anhaken besitzt.

4. Das Modul ist nicht als Newsletter-Anmeldung geeignet.
