# Mini-Bank – projekt analityczny

Ten projekt to symulacja pracy **analityka biznesowo-systemowego** w branży bankowej.  
Przedstawia proces tworzenia systemu obsługującego **konto osobiste oraz przelewy krajowe** — od pomysłu, przez analizę procesów biznesowych, aż po model danych.

Projekt został stworzony jako element portfolio i pokazuje przekrój pracy analityka:  
modelowanie procesów (BPMN), analizę wymagań (UML, user stories) i tworzenie struktur danych (SQL).

---

## Cel projektu

Celem jest zaprezentowanie umiejętności analitycznych w kontekście systemów finansowych:
- zrozumienie potrzeb biznesowych użytkownika banku,  
- odwzorowanie procesów biznesowych (np. przelew, reklamacja, weryfikacja klienta),  
- zaprojektowanie podstawowego modelu danych,  
- pokazanie przepływu informacji między systemami,  
- zdefiniowanie reguł biznesowych i wymagań niefunkcjonalnych.

---

## Zakres funkcjonalny (MVP)
W ramach MVP system obejmuje następujące funkcjonalności:
Zakładanie konta (proces KYC) – możliwość utworzenia nowego konta użytkownika z weryfikacją tożsamości.
Logowanie i podgląd salda – uwierzytelnianie użytkownika oraz wyświetlanie aktualnego stanu konta i podstawowych danych klienta.
Wykonanie przelewu krajowego – inicjacja i realizacja przelewów pomiędzy kontami krajowymi.
Historia transakcji – dostęp do listy wykonanych operacji wraz z filtrowaniem po dacie, kwocie i statusie.
Reklamacja przelewu – możliwość zgłoszenia błędnej lub nieautoryzowanej transakcji.
Poza zakresem MVP (out of scope):
Przelewy zagraniczne,
Karty płatnicze,
Lokaty i rachunki oszczędnościowe,
Pożyczki i kredyty.

---

## Struktura repozytorium

| Folder | Zawartość |
|---------|------------|
| `00-vision` | wizja projektu, cele, KPI i słowniczek pojęć |
| `01-stakeholders` | lista interesariuszy i opis ról |
| `02-requirements` | reguły biznesowe i wymagania niefunkcjonalne |
| `03-bpmn` | diagramy procesów biznesowych |
| `04-uml` | przypadki użycia, diagramy klas i sekwencji |
| `05-stories` | user stories oraz kryteria akceptacji |
| `06-data-sql` | model danych i zapytania SQL |
| `07-uat` | plan testów i scenariusze UAT |
| `99-demo` | podsumowanie projektu (screeny, wideo) |

---

##  Użyte narzędzia

- **Draw.io** – modelowanie BPMN i UML  
- **Figma** – makiety interfejsu użytkownika  
- **PostgreSQL** – baza danych i zapytania SQL  
- **Markdown / Confluence / GitHub** – dokumentacja projektu  

---

##  Status projektu

📅 Projekt w trakcie realizacji (etap: modelowanie BPMN).  
Repozytorium będzie uzupełniane etapami – każdy folder odpowiada kolejnemu krokowi w analizie systemu bankowego.

---

##  Autor

**Oliwia Kwaśna**  
Project & Business/ System  Analysis Enthusiast  
📍 Polska  
🔗 [LinkedIn](https://www.linkedin.com/in/oliwiakwa%C5%9Bna/)  

---

