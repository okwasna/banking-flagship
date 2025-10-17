# Mini-Bank – projekt analityczny

Ten projekt to symulacja pracy **analityka biznesowo-systemowego** w branży bankowej.  
Przedstawia proces tworzenia systemu obsługującego **konto osobiste oraz przelewy krajowe** — od pomysłu, przez analizę procesów biznesowych, aż po model danych i testy akceptacyjne.

Projekt został stworzony jako element portfolio i pokazuje pełny przekrój pracy analityka:  
modelowanie procesów (BPMN), analizę wymagań (UML, user stories), tworzenie struktur danych (SQL) i przygotowanie scenariuszy testowych (UAT).

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

1. Zakładanie konta (proces KYC)  
2. Logowanie i podgląd salda  
3. Wykonanie przelewu krajowego  
4. Historia transakcji  
5. Reklamacja przelewu  

Poza zakresem: przelewy zagraniczne, karty płatnicze, lokaty, pożyczki.

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

📅 Projekt w trakcie realizacji (etap: modelowanie UML- pozostale UC + diagram klas dla UC3).  
Repozytorium będzie uzupełniane etapami – każdy folder odpowiada kolejnemu krokowi w analizie systemu bankowego.

---

##  Autor

**Oliwia Kwaśna**  
Project & Business/ System  Analysis Enthusiast  
📍 Polska  
🔗 [LinkedIn](https://www.linkedin.com/in/oliwiakwa%C5%9Bna/)  

---

