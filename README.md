# 📄 Contract Entity Recognition (German) – Labeling Instructions

## 🎯 Project Objective

The purpose of this labeling task is to annotate **German-language contracts** (e.g., insurance, due diligence, and renewable energy documents) with specific metadata fields. These annotations will train a Named Entity Recognition (NER) model to automatically populate metadata fields in a SharePoint-based contract management system.

Your role is to label occurrences of contract-related entities from unstructured text according to the guidelines below.

---

## 🔟 Entity Labels and Definitions

| Entity Label          | Description                                                                 | Examples (German)                                            |
|-----------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------|
| `Entity`              | The legal entity (usually a subsidiary or business unit) issuing the contract | E.g., "Tion Services GmbH", "Windkraft Nord GmbH"                   |
| `Plant`               | Name of a renewable energy installation (e.g., wind or solar plant)         | E.g., "Windpark Nordsee 3", "Solaranlage Main-Tauber"       |
| `Counterparty`        | The contract’s opposing party                                               | E.g., "Versicherung AG", "Stadtwerke Bremen"                |
| `StartDate`           | The contract’s start or effective date                                      | E.g., "01. Januar 2024", "zum 01.01.2024"                    |
| `EndDate`             | The date the contract ends or expires                                       | E.g., "31. Dezember 2025", "bis zum 31.12.2025"             |
| `RenewalType`         | How the contract renews (if at all)                                         | E.g., "automatische Verlängerung", "auf unbestimmte Zeit"   |
| `NoticePeriod`        | The required cancellation notice timeframe                                  | E.g., "Kündigungsfrist von 3 Monaten", "30 Tage Frist"      |
| `TotalContractValue`  | Full monetary value of the contract                                         | E.g., "Gesamtwert: 120.000 EUR", "1,2 Mio. EUR"             |
| `AnnualContractValue` | The annual payment amount specified in the contract                         | E.g., "jährlich 50.000 EUR", "pro Jahr 75.000 EUR"          |
| `KeyObligations`      | Explicit deliverables, responsibilities, or services the entity must fulfill | E.g., "monatliche Wartung", "jährliche Berichterstattung"   |

---

## ✅ Labeling Guidelines

- Label **entire phrases** including dates, currency symbols, and context (e.g., not just "EUR").
- Label an entity **each time it appears**, even if it occurs multiple times.
- Only label data that is **explicitly stated** — do not infer or guess.
- **Avoid labeling boilerplate** or legal filler that isn’t specific to the document's metadata.
- When in doubt, **flag the sample** for review instead of guessing.

---

## 📌 Examples

### Example 1
> "Der Vertrag beginnt am **01.01.2024** und endet am **31.12.2025**. Vertragspartner ist **Versicherung AG**. Die **Kündigungsfrist** beträgt **drei Monate** zum Jahresende."

**Labels:**
- `StartDate`: 01.01.2024  
- `EndDate`: 31.12.2025  
- `Counterparty`: Versicherung AG  
- `NoticePeriod`: drei Monate zum Jahresende

---

### Example 2
> "Die **Tion Services GmbH** betreibt die **Solaranlage Main-Tauber**. Die Vertragslaufzeit beträgt **5 Jahre** mit einer **automatischen Verlängerung** um jeweils ein Jahr."

**Labels:**
- `Entity`: Tion Services GmbH  
- `Plant`: Solaranlage Main-Tauber  
- `RenewalType`: automatische Verlängerung

---

## 🚫 Do Not Label

- General legal references not tied to this contract
- Internal comments or formatting artifacts
- Implied or indirect content not explicitly written

---

## ℹ️ Questions?

Please contact the project administrator if:
- You’re unsure about an entity type
- You encounter non-standard document formats
- You identify inconsistencies in annotation policies

---

**Thank you for contributing to this project! Your accuracy ensures a high-quality AI system for contract management.**
