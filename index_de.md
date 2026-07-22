
# Reinbold Saunabau KI-Assistenten-Suite: Erste Schritte

[🇬🇧 Read in English](index.md)

Herzlich willkommen! Dieses System bietet Ihnen automatisierte, rund um die Uhr verfügbare KI-Assistenten, die Ihren Kunden helfen, ihre ideale Sauna zu entwerfen und Beratungsgespräche mit Ihrem Team zu buchen.

Da wir im Hintergrund fortschrittliche Datenweiterleitung nutzen, benötigen Sie keinerlei Programmierkenntnisse, um dieses System zu bedienen. Dieser Leitfaden führt Sie durch unsere zwei Hauptwerkzeuge: den **Konfigurator** und die **Raumplanung**.

---

## 1. Der Konfigurator: Automatisierte Sauna-Planung

Der Konfigurator ist darauf ausgelegt, mit Ihren Kunden zu kommunizieren, genau herauszufinden, was sie möchten, und diese Informationen sofort in einer übersichtlichen Tabelle für Ihr Verkaufsteam zu organisieren.

### Wie Ihre Kunden ihn nutzen
Anstatt ein herkömmliches Webformular auszufüllen, chatten Ihre Kunden ganz natürlich mit der KI. Der Assistent ist darauf trainiert, sie sanft durch alle notwendigen Entscheidungen zu führen, einschließlich:
* **Raummaße:** Erfassung von Breite und Tiefe des verfügbaren Platzes.
* **Materialien & Beleuchtung:** Abfrage der Vorlieben für Holzarten (wie z. B. Zirbe) und Beleuchtungskonzepte.
* **Konformität & Struktur:** Prüfung, ob spezifische elektrische Standards (wie VDE-Konformität) oder Anpassungen an Außenwänden erforderlich sind.

### Wo die Daten landen (Ihr Google Sheet)
Sie müssen nichts kopieren und einfügen. Sobald der Kunde den Chat beendet, verpackt der Assistent die Antworten automatisch und sendet sie direkt an Ihr hinterlegtes Google Sheet (Tabelle).
* Jedes Mal, wenn ein neuer Kunde eine Sitzung abschließt, erscheint sofort eine **neue Zeile** in Ihrer Tabelle.
* **Tipp zur Fehlerbehebung:** Wenn keine neue Zeile erscheint, stellen Sie sicher, dass Sie sich das *Live*-Google-Sheet ansehen und keine Offline-Kopie!

---

## 2. Die Raumplanung: Raum- und Layout-Mapping

Der Raumplanungs-Assistent erfüllt einen völlig anderen Zweck. Anstatt Materialien auszuwählen, hilft dieses Tool Ihren Kunden, sich vorzustellen und zu messen, wie eine Sauna physisch in ihr Zuhause passt.

### Wie Ihre Kunden ihn nutzen
Der Assistent hilft den Kunden, die Logistik ihres Installationsraums zu durchdenken. Er führt sie durch:
* **Grundflächenberechnung:** Hilft zu verstehen, wie viel Netto-Platz im Verhältnis zu den Brutto-Raummaßen benötigt wird.
* **Decken- & Dachschrägen:** Berücksichtigung spezifischer architektonischer Besonderheiten, wie z. B. der Kniestockhöhe bei Dachgeschossinstallationen.
* **Zugang & Freiräume:** Sicherstellung, dass genügend Platz für das Öffnen von Türen und eine ordnungsgemäße Belüftung um die Kabine herum vorhanden ist.

*(Hinweis: Das Raumplanungs-Tool ist rein beratend und bereitet den Kunden auf einen hochproduktiven Vor-Ort-Termin mit Ihrem Installationsteam vor.)*

---

## 3. Terminbuchung (Kalender-Integration)

Sobald ein Kunde entweder den Konfigurator- oder den Raumplanungsprozess abgeschlossen hat, bietet die KI an, ein Echtzeit-Beratungsgespräch mit Ihrem Team zu buchen.

* **Wie es funktioniert:** Der Assistent stellt dem Kunden einen direkten, sicheren Link zu Ihrem Buchungskalender zur Verfügung.
* **Was der Kunde sieht:** Er sieht Ihre verfügbaren Daten und Zeiten, wählt einen passenden Termin und bestätigt diesen.
* Sie erhalten sofort eine E-Mail-Benachrichtigung über den neuen Termin, und er erscheint in Ihrem Hauptkalender.

---

## 4. Datenschutz & Datensicherheit

Wir nehmen die Daten Ihrer Kunden ernst.
* Das System erfasst nur die Informationen, die für die Planung der Sauna und die Buchung des Termins erforderlich sind (Name, Kontaktinformationen und Raumspezifikationen).
* Wir erfassen über den Chat keine Zahlungsinformationen.
* Alle Daten werden über sichere, verschlüsselte Verbindungen direkt an Ihre private Unternehmenstabelle weitergeleitet.

---

## Nächste Schritte zur Implementierung

Um Ihr spezifisches System einzurichten, benötigt unser Team Folgendes:
1. **Tabellen-Zugriff:** Zugang zu dem Google-Konto, in dem Ihre Haupttabelle gehostet werden soll.
2. **Kalender-Link:** Den öffentlichen Link zu Ihrer Planungssoftware (wie Google Calendar oder Calendly).

Sobald diese vorliegen, verknüpfen wir die Schnittstellen im Hintergrund, und Ihre maßgeschneiderten Assistenten sind bereit für den Einsatz bei Ihren Kunden!