# Urlaubs-Recap-Dashboard — Prompt zum Kopieren (Deutsch)

Ein Prompt für Copilot Cowork, Claude Cowork und Microsoft Scout, der nach längerer Abwesenheit automatisch ein interaktives HTML-Dashboard erstellt: E-Mails, Meetings, Teams, Dateien, offene Entscheidungen und Prioritäten — mit Checkboxen zum Abhaken, Dark-Mode und Filtern.

Läuft ohne Rückfragen vollständig durch. Ergebnis ist eine einzelne HTML-Datei, die auch offline funktioniert.

---

## Was du anpassen musst

| Stelle im Prompt | Was dort hinein muss | Pflicht? |
|---|---|---|
| **WER ICH BIN** | Deine Rolle, dein Unternehmen bzw. Bereich und deine Verantwortungsbereiche. Je präziser, desto besser die Priorisierung. | Ja |
| **ZEITRAUM** | Dauer deiner Abwesenheit. Standard sind drei Wochen. | Nur bei Abweichung |
| **MEINE SCHWERPUNKTE** | Deine 3–5 wichtigsten Projekte und Themen. | Nein — siehe unten |
| **GESTALTUNG** | Firmenlogo an die Aufgabe anhängen, dann werden die Farben daraus übernommen. Ohne Logo greift ein neutrales Schema. | Nein |

**Wenn du die Schwerpunkte leer lässt**, läuft der Prompt im Standardmodus: Er leitet deine Themen selbst aus deinem Rollenprofil, deiner Personalisierung und dem tatsächlichen Aufkommen im Zeitraum ab — und kennzeichnet sie im Dashboard als „automatisch erkannt", damit du sie einmal prüfen kannst.

## So nutzt du ihn

1. Prompt vollständig kopieren
2. In Copilot Cowork, Claude Cowork oder Microsoft Scout eine neue Aufgabe starten
3. Optional das Firmenlogo anhängen
4. Abschicken — die Auswertung dauert einige Minuten, das Fenster darf zu

**Hinweis für Claude Cowork und Microsoft Scout:** Damit die Schritte zu E-Mail, Kalender, Teams und Dateien funktionieren, müssen die entsprechenden Microsoft-365-Verbindungen (Connectoren) eingerichtet sein. Fehlt eine Quelle, weist der Prompt das im Dashboard offen aus, statt zu raten.

---

## Der Prompt

```text
ARBEITSWEISE (WICHTIG, ZUERST LESEN)
Führe diese Aufgabe vollständig und selbstständig aus. Stelle mir keine Rückfragen. Warte nicht auf Bestätigungen. Arbeite alle Schritte der Reihe nach ab und stoppe erst, wenn das fertige Dashboard erstellt ist. Wenn eine Information fehlt, triff eine sinnvolle Annahme, kennzeichne sie im Ergebnis und mache weiter. Erfinde keine Fakten: Was du nicht in meinen Daten findest, weist du als Lücke aus. Du arbeitest ausschließlich lesend: Du änderst, versendest oder löschst nichts.

WER ICH BIN
Ich bin [DEINE ROLLE, Z. B. MITGLIED DER GESCHÄFTSLEITUNG] bei [UNTERNEHMEN ODER BEREICH]. Ich verantworte [DEINE VERANTWORTUNGSBEREICHE, Z. B. PERSONAL, EINKAUF, PRODUKTION, BUDGET, FREIGABEN, ESKALATIONEN]. Ich war [ZEITRAUM, Z. B. DREI WOCHEN] im Urlaub und komme heute zurück.

DEINE AUFGABE
Erstelle mir einen vollständigen Überblick darüber, was ich in meiner Abwesenheit verpasst habe, und sage mir klar, wo ich handeln muss. Nutze dafür alle dir verbundenen Datenquellen (E-Mail, Kalender, Teams/Chats, SharePoint und OneDrive). Ist eine Quelle nicht verfügbar oder nicht verbunden, überspringe den betreffenden Schritt nicht kommentarlos, sondern weise die fehlende Quelle im Dashboard ausdrücklich als Lücke aus.

ZEITRAUM
Meine gesamte Abwesenheit bis heute, mindestens die letzten drei Wochen. Nenne im Dashboard das konkrete Start- und Enddatum, das du verwendest.

MEINE SCHWERPUNKTE
- Projekte und Themen: [OPTIONAL: 3-5 WICHTIGSTE PROJEKTE EINTRAGEN]
- Interne Themen, die ich verfolgen will: [OPTIONAL: WEITERE THEMEN EINTRAGEN]

WENN DIESE FELDER LEER SIND ODER NOCH DIE PLATZHALTER ENTHALTEN:
Frage nicht nach. Arbeite automatisch im Standardmodus. Leite meine Schwerpunkte dann selbst ab aus:
- meiner hinterlegten Personalisierung, meinem Rollen- und Führungsprofil sowie meinen gespeicherten Anweisungen,
- meinen Verantwortungsbereichen,
- den Themen, die im Zeitraum tatsächlich das höchste Aufkommen, die meisten Beteiligten oder die größte Dringlichkeit hatten.
Weise die so ermittelten Schwerpunkte im Dashboard sichtbar als "automatisch erkannt" aus, damit ich sie prüfen kann.

SCHRITT 1 - E-MAILS
Sichte meinen Posteingang des Zeitraums. Sortiere jede relevante Mail in genau eine dieser Stufen ein:
1. DRINGEND - Handlungsbedarf sofort (Freigaben, Eskalationen, Fristen, Reklamationen, offene Entscheidungen, direkte Fragen an mich)
2. MITTEL - diese Woche erledigen
3. NIEDRIG - kann warten, aber nicht vergessen
4. KEIN HANDLUNGSBEDARF - nur zur Kenntnis
Als irrelevant aussortieren und nur zahlenmäßig zusammenfassen: Newsletter, Werbung, Systemmeldungen, automatische Benachrichtigungen und Bestätigungen.
Gib je Mail an: Absender, Betreff, Datum, eine Zeile Zusammenfassung, was von mir erwartet wird, und einen direkten Link zur Mail.
Markiere besonders: Vorgänge, die in meiner Abwesenheit jemand anderes übernommen hat, und solche, die liegengeblieben sind.

SCHRITT 2 - TERMINE UND MEETINGS
Prüfe meinen Kalender im Zeitraum. Liste die Termine auf, die stattgefunden haben und für mich relevant sind - insbesondere meine Regeltermine und Jour fixes.
Prüfe zu jedem Termin, ob ein Transkript, eine Aufzeichnung oder ein Protokoll vorliegt.
- Wenn ja: Fasse die Highlights in maximal fünf Stichpunkten zusammen - besprochene Themen, getroffene Entscheidungen, vereinbarte Aufgaben mit Verantwortlichen und Terminen sowie offene Punkte. Verlinke die Quelle.
- Wenn nein: Schreibe ausdrücklich "kein Transkript vorhanden" und nenne mir, wen ich für eine Nachbereitung ansprechen sollte.

SCHRITT 3 - MICROSOFT TEAMS
Prüfe meine Teams-Chats und Kanäle im Zeitraum.
- Welche ungelesenen Nachrichten und Kanal-Beiträge habe ich?
- Priorisiere die Kolleginnen und Kollegen, mit denen ich am häufigsten zusammenarbeite, sowie Nachrichten, in denen ich namentlich erwähnt oder direkt angesprochen wurde.
- Fasse je Person und Kanal kurz zusammen, worum es ging, und markiere alles, was eine Antwort von mir erwartet.

SCHRITT 4 - DATEIEN IN SHAREPOINT UND ONEDRIVE
Prüfe, welche für mich relevanten Dokumente im Zeitraum neu erstellt oder geändert wurden.
Nenne je Datei: Name, wer sie zuletzt bearbeitet hat, wann, warum sie relevant sein könnte, plus Link. Ordne sie meinen Schwerpunkten zu, wenn möglich.

SCHRITT 5 - WAS ICH SCHULDE UND WER AUF MICH WARTET
- Wer wartet auf eine Antwort, eine Freigabe oder eine Entscheidung von mir? Sortiere nach Wartedauer.
- Welche Fristen sind in meiner Abwesenheit verstrichen? Was hat das zur Folge?
- Welche Zusagen habe ich vor dem Urlaub gemacht, die jetzt fällig sind?
- Gibt es neue Aufgaben, die mir zugewiesen wurden?

SCHRITT 6 - WAS IN MEINEM NAMEN PASSIERT IST
- Welche Entscheidungen wurden in meiner Abwesenheit getroffen, die in meinen Verantwortungsbereich fallen?
- Wurde etwas vertretungsweise für mich freigegeben oder entschieden? Was davon muss ich nachvollziehen oder bestätigen?
- Gibt es Themen aus dem Zeitraum, die ich als Führungskraft kennen muss?

SCHRITT 7 - WAS HEUTE UND DIESE WOCHE ANSTEHT
- Meine Termine heute mit Uhrzeit, Teilnehmern und - falls vorhanden - dem Ergebnis des jeweils letzten gleichen Termins.
- Meine Termine für den Rest der Woche.
- Wo muss ich mich vorbereiten? Nenne konkret, was ich vorher lesen oder entscheiden sollte.

SCHRITT 8 - DIE VERDICHTUNG
Leite aus allem oben ab:
- Die fünf wichtigsten Dinge, die ich heute anfassen muss - in der Reihenfolge, in der ich sie angehen sollte, mit Begründung.
- Die wichtigsten Entscheidungen, die jetzt von mir erwartet werden.
- Offene Zusagen und Fristen, die in den nächsten zehn Tagen fällig werden.
- Alles, was nach Risiko, Eskalation oder Konflikt aussieht - auch wenn es nur angedeutet wurde.
- Ausdrücklich auch: Was ich guten Gewissens ignorieren oder löschen kann. Entlastung ist genauso wertvoll wie eine Aufgabenliste.

SCHRITT 9 - DENK SELBST WEITER
Überlege eigenständig, was für ein wirklich gutes Urlaubs-Recap in meiner Rolle noch fehlt, und ergänze es sinnvoll. Denke dabei an Dinge wie: auffällige Häufungen eines Themas, Stimmungslagen in Konflikten, angekündigte aber nicht erfolgte Rückmeldungen, Kunden oder Partner, von denen ungewöhnlich viel oder ungewöhnlich wenig kam, sowie Chancen, die liegen geblieben sind. Kennzeichne alles, was du selbst ergänzt hast, klar als eigenen Vorschlag.

AUSGABE - DAS DASHBOARD
Erstelle das Ergebnis als eigenständige HTML-Datei zum Öffnen im Browser. Aufbau in dieser Reihenfolge:
1. Kopfbereich: Titel, Zeitraum, Erstellungsdatum und drei bis fünf Kennzahlen auf einen Blick (z. B. Anzahl Mails gesamt, davon relevant, offene Entscheidungen, verstrichene Fristen).
2. Executive Summary: Die Lage in maximal zehn Zeilen. Was ist das Wichtigste?
3. Meine Top-Prioritäten heute: die fünf wichtigsten Handlungen als Ampel-Block.
4. Danach die Detailabschnitte in dieser Reihenfolge, jeweils klar getrennt und mit der Anzahl im Abschnittstitel: E-Mails, Meetings, Teams, Dateien, Wer auf mich wartet, In meinem Namen entschieden, Heute und diese Woche, Deine Ergänzungen.

GESTALTUNG
- Modernes, helles, cleanes Layout. Viel Weißraum, klare Typografie, ruhige Struktur, gut lesbar auf Bildschirm und im Ausdruck.
- Das Firmenlogo ist dieser Aufgabe angehängt. Extrahiere daraus die Markenfarben und verwende sie konsequent für Kopfbereich, Überschriften, Akzente und Tabellenköpfe. Setze das Logo dezent in den Kopfbereich. Falls kein Logo anhängt, verwende ein zurückhaltendes, professionelles Blau-Grau-Schema.
- Statusfarben zusätzlich zur Markenfarbe: Rot gleich dringend, Gelb gleich mittel, Grün gleich erledigt oder ohne Handlungsbedarf.
- Nutze Karten und Tabellen statt langer Fließtexte. Jeder Eintrag bekommt einen direkten Link zur Quelle.
- Sprache: Deutsch, sachlich, kurz. Keine Floskeln, keine Wiederholungen.

INTERAKTIVE FUNKTIONEN (bitte vollständig einbauen)
1. Checkboxen: Jede Aufgabe, jede offene Entscheidung und jede zu beantwortende Nachricht bekommt eine Checkbox. Abgehakte Einträge werden sichtbar als erledigt dargestellt, zum Beispiel ausgegraut und durchgestrichen. Zeige oben einen Fortschrittsbalken mit der Anzahl erledigter von gesamten Aufgaben.
2. Dark-Mode: Ein gut sichtbarer Umschalter oben rechts zwischen hellem und dunklem Modus. Beide Varianten müssen durchgehend gut lesbar sein und ausreichend Kontrast haben.
3. Nicht relevant markieren: Jeder Eintrag, den du selbst vorgeschlagen oder abgeleitet hast, bekommt zusätzlich eine Schaltfläche "nicht relevant". Damit blende ich ihn aus der aktiven Liste aus. Ausgeblendete Einträge werden nicht gelöscht, sondern in einen einklappbaren Bereich "Als nicht relevant markiert" verschoben und lassen sich von dort wiederherstellen.
4. Zustand merken: Speichere den Zustand von Checkboxen, Dark-Mode und ausgeblendeten Einträgen im Browser, damit meine Auswahl beim erneuten Öffnen der Datei erhalten bleibt.
5. Zusätzlich hilfreich: eine einfache Filterleiste, mit der ich nur die dringenden Punkte oder nur die offenen Punkte anzeigen kann.
Die gesamte Datei muss ohne Internetverbindung funktionieren: HTML, CSS und JavaScript in einer einzigen Datei, keine externen Abhängigkeiten.

QUALITÄTSREGELN
- Kennzeichne sichtbar, wenn Informationen fehlen oder unsicher sind. Lieber eine Lücke ausweisen als eine Vermutung als Fakt darstellen.
- Trenne klar zwischen belegten Fakten aus meinen Daten und deinen eigenen Einschätzungen.
- Keine Rückfragen an mich. Arbeite durch, bis das Dashboard fertig ist.

Fasse mir zum Schluss im Chat in fünf Sätzen zusammen, was ich als Erstes tun sollte.
```

---

## Anpassungsideen

- **Kürzere Abwesenheit:** Zeitraum reduzieren, Schritt 6 kannst du dann meist streichen.
- **Andere Rolle:** In Schritt 1 die Dringlichkeitskriterien austauschen — bei Vertrieb etwa Angebote und Kundenanfragen, bei IT Störungen und Changes.
- **Wöchentlich statt nach Urlaub:** Zeitraum auf sieben Tage setzen und als wiederkehrende Aufgabe einplanen.
- **Ohne Teams oder SharePoint:** Den jeweiligen Schritt einfach löschen.

## Hinweise

- Der Prompt liest nur, was ohnehin für dich freigegeben ist. Er ändert nichts und versendet nichts.
- Ohne Transkript oder Protokoll kann kein Meeting zusammengefasst werden — das weist das Dashboard offen aus, statt zu raten.
- Ergebnisse immer gegenprüfen, bevor daraus Entscheidungen werden.
