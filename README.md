# Mini-Bank – projekt analityczny

Ten projekt to symulacja pracy **analityka biznesowo-systemowego** w branży bankowej.  
Przedstawia proces tworzenia systemu obsługującego **konto osobiste oraz przelewy krajowe** — od pomysłu, przez analizę procesów biznesowych, aż po model danych.

Projekt został stworzony jako element portfolio i pokazuje przekrój pracy analityka:  
modelowanie procesów (BPMN), analizę wymagań (UML, user stories).

---

## Cel projektu

Celem jest zaprezentowanie umiejętności analitycznych w kontekście systemów finansowych:
- zrozumienie potrzeb biznesowych użytkownika banku,  
- odwzorowanie procesów biznesowych (np. przelew, reklamacja, weryfikacja klienta),  
- zaprojektowanie podstawowego modelu danych,  
- pokazanie przepływu informacji między systemami,  
- zdefiniowanie reguł biznesowych i wymagań funkcjonalnych oraz niefunkcjonalnych.

---

## Zakres funkcjonalny (MVP)
W ramach MVP system obejmuje następujące funkcjonalności:
- Zakładanie konta (proces KYC) – możliwość utworzenia nowego konta użytkownika z weryfikacją tożsamości.
- Logowanie 2FA i podgląd salda – uwierzytelnianie użytkownika oraz wyświetlanie aktualnego stanu konta i podstawowych danych klienta.
- Wykonanie przelewu krajowego – inicjacja i realizacja przelewów pomiędzy kontami krajowymi.
- Historia transakcji – dostęp do listy wykonanych operacji wraz z filtrowaniem po dacie, kwocie i statusie.
- Reklamacja przelewu – możliwość zgłoszenia błędnej lub nieautoryzowanej transakcji.

Poza zakresem MVP (out of scope):
- Przelewy zagraniczne,
- Karty płatnicze,
- Lokaty i rachunki oszczędnościowe,
- Pożyczki i kredyty.

---

## Struktura repozytorium

| Folder | Zawartość |
|---------|------------|
| `00-vision` | wizja projektu, cele, KPI i słowniczek pojęć |
| `01-stakeholders` | lista interesariuszy i opis ról |
| `02-requirements` | reguły biznesowe i wymagania funkcjonalne oraz niefunkcjonalne |
| `03-bpmn` | diagramy procesów biznesowych |
| `04-uml` | przypadki użycia, diagramy klas i sekwencji |
| `05-stories` | user stories oraz kryteria akceptacji |


---

##  Użyte narzędzia

- **Draw.io** – modelowanie BPMN i UML  
- **Markdown / Confluence / GitHub** – dokumentacja projektu  

---
## Standardy notacyjne
- BPMN 2.0 (swimlanes, message flows, event types)
- UML (Use Case, Activity, Sequence, Class, Component)

##  Status projektu

📅 Projekt w trakcie realizacji   
Repozytorium będzie uzupełniane etapami – każdy folder odpowiada kolejnemu krokowi w analizie systemu bankowego.
Jak korzystać z repozytorium

## Jeśli chcesz szybko zrozumieć projekt:
1. Zacznij od folderu `00-vision` – kontekst biznesowy i cel projektu.
2. Przejdź do `02-requirements` – zobacz wymagania i reguły biznesowe.
3. Następnie `03-bpmn` – wizualizacja procesów end-to-end.
4. `04-uml` – logika systemowa, interakcje komponentów i model danych.
5. `05-stories` – przypadki użycia z perspektywy użytkownika.

---

##  Autor

**Oliwia Kwaśna**  
Project & Business/ System  Analysis Enthusiast  
📍 Polska  
🔗 [LinkedIn](https://www.linkedin.com/in/oliwiakwa%C5%9Bna/)  

---

