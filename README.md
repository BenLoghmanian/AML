# 📄 Contract Entity Recognition (German) – Labeling Instructions

## 🎯 Projektziel

Ziel dieser Labeling-Aufgabe ist es, **deutschsprachige Verträge** (z. B. aus den Bereichen Versicherung, Due Diligence, erneuerbare Energien) mit spezifischen Metadatenfeldern zu annotieren. Diese Annotationsdaten dienen dem Training eines Named Entity Recognition (NER) Modells, das künftig automatisch Vertragsdaten in ein SharePoint-basiertes Vertragsmanagementsystem überträgt.

Ihre Aufgabe ist es, relevante Informationen aus unstrukturiertem Vertragstext gemäß den unten stehenden Richtlinien zu kennzeichnen.

---

## 🔟 Zu kennzeichnende Entitäten

| Entitätslabel (Deutsch)      | Beschreibung                                                                 | Beispiele |
|------------------------------|------------------------------------------------------------------------------|-----------|
| `Gesellschaft`               | Die juristische Person, die Vertragspartei ist (z. B. Tochterunternehmen)   | „Tion Services GmbH“, „Windkraft Nord GmbH“ |
| `Anlage`                     | Name oder Bezeichnung einer Energieerzeugungsanlage (z. B. Windpark, PV)    | „Windpark Nordsee 3“, „Solaranlage Main-Tauber“ |
| `Vertragspartner`            | Gegenpartei des Vertrags                                                     | „Versicherung AG“, „Stadtwerke Bremen“ |
| `Vertragsbeginn`             | Datum, an dem der Vertrag gültig wird                                       | „01. Januar 2024“, „zum 01.01.2024“ |
| `Vertragsende`               | Datum, an dem der Vertrag endet oder ausläuft                               | „31. Dezember 2025“, „bis zum 31.12.2025“ |
| `Verlängerungsart`           | Art und Weise der Vertragsverlängerung                                      | „automatische Verlängerung“, „auf unbestimmte Zeit“ |
| `Kündigungsfrist`            | Zeitraum, in dem eine Kündigung vor Ablauf erfolgen muss                    | „3 Monate zum Jahresende“, „30 Tage Frist“ |
| `Gesamtvertragswert`         | Gesamter finanzieller Vertragswert                                          | „120.000 EUR“, „1,2 Mio. EUR“ |
| `JährlicherVertragswert`     | Jährliche Zahlung oder Einnahme laut Vertrag                                | „jährlich 50.000 EUR“, „pro Jahr 75.000 EUR“ |
| `WesentlicheVerpflichtungen` | Konkrete Pflichten oder Leistungen, die aus dem Vertrag hervorgehen         | „monatliche Wartung“, „jährliche Berichterstattung“ |

---

## ✅ Kennzeichnungsrichtlinien

- Markieren Sie **den vollständigen Ausdruck**, inkl. Währungen, Einheiten oder Datenformaten.
- Eine Entität soll bei **mehrmaligem Auftreten auch mehrfach** gekennzeichnet werden.
- Nur **explizit genannte Informationen** kennzeichnen – keine Vermutungen treffen.
- **Keine Standardklauseln oder rechtliche Floskeln** markieren, wenn sie nicht spezifisch sind.
- Bei Unsicherheit bitte **das Dokument zur Prüfung markieren**, nicht raten.

---

## 📌 Beispiele

### Beispiel 1
> „Der Vertrag beginnt am **01.01.2024** und endet am **31.12.2025**. Vertragspartner ist **Versicherung AG**. Die **Kündigungsfrist** beträgt **drei Monate** zum Jahresende.“

**Labels:**
- `Vertragsbeginn`: 01.01.2024  
- `Vertragsende`: 31.12.2025  
- `Vertragspartner`: Versicherung AG  
- `Kündigungsfrist`: drei Monate zum Jahresende

---

### Beispiel 2
> „Die **Tion Services GmbH** betreibt die **Solaranlage Main-Tauber**. Die Vertragslaufzeit beträgt 5 Jahre mit einer **automatischen Verlängerung** um jeweils ein Jahr.“

**Labels:**
- `Gesellschaft`: Tion Services GmbH  
- `Anlage`: Solaranlage Main-Tauber  
- `Verlängerungsart`: automatische Verlängerung

---

## 🚫 Nicht markieren:

- Allgemeine rechtliche Textbausteine ohne Bezug zu den Metafeldern
- Formatierungen, Kommentare oder Anmerkungen im Text
- Inhalte, die **nicht explizit im Text stehen**

---

## ℹ️ Rückfragen

Bitte wenden Sie sich an den Projektverantwortlichen, wenn:
- eine Entität nicht klar definierbar ist
- das Dokumentformat vom Standard abweicht
- Unstimmigkeiten oder Regelabweichungen auftreten

---

**Vielen Dank für Ihre Mitarbeit! Ihre präzise Kennzeichnung ist ein zentraler Beitrag zur Entwicklung eines intelligenten Vertragsmanagementsystems.**
