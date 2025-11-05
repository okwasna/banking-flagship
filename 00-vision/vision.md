#  Vision – Mini-bank: konto osobiste + przelewy krajowe (MVP)

##  Cel i kontekst projektu

Projekt **Mini-bank** ma na celu zaprojektowanie uproszczonego systemu bankowego dla klientów detalicznych w Polsce.  
System pozwala na **szybkie i bezpieczne wykonywanie przelewów krajowych**, podgląd salda oraz historię transakcji, przy zachowaniu wysokich standardów bezpieczeństwa i zgodności z przepisami RODO.

---

##  Dla kogo

- Klient detaliczny korzystający z usług bankowych online  
- Użytkownik oczekujący prostoty, szybkości działania i przejrzystości  
- Osoby wykonujące podstawowe operacje bankowe: przelewy, sprawdzanie salda, reklamacje  

---

##  Wartość biznesowa 

- Zapewnienie **intuicyjnego kanału online** dla obsługi podstawowych operacji bankowych  
- Skrócenie czasu realizacji przelewów i reklamacji  
- Zwiększenie satysfakcji klientów poprzez dostępność 24/7  
- Wzmocnienie bezpieczeństwa i przejrzystości operacji  

---

##  Zakres funkcjonalny (MVP)

### Zakres v1.0:
1. **Założenie konta (KYC light)** – uproszczona weryfikacja danych i aktywacja konta  
2. **Logowanie i podgląd salda** – dostęp do podstawowych informacji finansowych  
3. **Przelew krajowy** – z limitem dziennym i kontrolą salda  
4. **Historia transakcji** – dostęp do listy i szczegółów operacji  
5. **Reklamacja przelewu** – zgłoszenie reklamacji i śledzenie statusu  

### Poza zakresem (v1.0):
- Przelewy zagraniczne   
- Karty płatnicze i kredyty  
- Lokaty i oszczędności  
- Powiadomienia push 

---

##  Ryzyka projektowe

| Ryzyko | Opis |
|---------|------|
| Zgodność z RODO | konieczność ochrony danych osobowych klientów |
| Limity antyfraudowe | ryzyko błędnych blokad lub nieautoryzowanych transakcji |
| Awaria operatora rozliczeń | opóźnienia w realizacji przelewów i reklamacji |
| Błędne mapowanie danych KYC | ryzyko błędnej identyfikacji użytkownika |

---

##  Założenia techniczne i operacyjne

| Obszar | Założenie |
|--------|------------|
| Wydajność | system obsługuje ≤ 50 zapytań na minutę |
| Klient | jeden klient może wykonać ≤ 20 przelewów dziennie |
| Bezpieczeństwo | logowanie z 2FA |
| Dostępność | system działa 24/7 z dostępnością ≥ 99,5% miesięcznie |

---

##  Oczekiwany rezultat

- Gotowy model analityczny systemu bankowego (procesy, diagramy, reguły)  
- Dokumentacja wymagań funkcjonalnych i niefunkcjonalnych  
- Podstawowe modele UML (Use Case, Activity, Class, Sequence)  
- Podstawowy model danych SQL z przykładowymi zapytaniami  

---

📚 *Dokument stanowi punkt wyjścia do dalszej analizy wymagań i modelowania procesów biznesowych (BPMN).*

