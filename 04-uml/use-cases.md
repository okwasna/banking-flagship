#  Lista przypadków użycia – projekt Mini-bank

Dokument zawiera opis głównych **przypadków użycia (Use Cases)** w systemie Mini-bank.  
Każdy przypadek został oznaczony unikalnym identyfikatorem (UC-ID) i opisuje kluczową funkcjonalność aplikacji z perspektywy użytkownika.

---

## UC-01: Załóż konto (onboarding / KYC)

**Aktorzy:** Klient, Moduł KYC/AML  
**Cel:** Utworzenie nowego konta bankowego po weryfikacji tożsamości użytkownika.  

**Główny przebieg:**
1. Klient wypełnia formularz rejestracyjny i podaje dane osobowe.  
2. System przesyła dane do modułu KYC/AML.  
3. Moduł weryfikuje dane i zwraca wynik pozytywny.  
4. Konto zostaje aktywowane i klient otrzymuje powiadomienie.

**Alternatywy:**
- KYC odrzucone → system wyświetla komunikat i instrukcję dosłania dokumentów.  
- Błąd połączenia z modułem KYC → komunikat o niedostępności i prośba o ponowną próbę.

**Powiązania:** BR-04 (KYC gate)

---

## UC-02: Zaloguj i zobacz saldo

**Aktorzy:** Klient, System logowania (2FA), Backend bankowy  
**Cel:** Uzyskanie dostępu do konta i podglądu salda.  

**Główny przebieg:**
1. Klient wprowadza login i hasło.  
2. System wysyła kod 2FA (SMS / e-mail).  
3. Klient wprowadza kod i zostaje zalogowany.  
4. System wyświetla saldo i listę ostatnich transakcji.

**Alternatywy:**
- Niepoprawny kod 2FA → komunikat o błędzie.  
- Po N nieudanych próbach → konto zablokowane czasowo.

**Powiązania:** NFR – Security (2FA)

---

## UC-03: Wyślij przelew krajowy

**Aktorzy:** Klient, Backend bankowy, Operator rozliczeń ELIXIR  
**Cel:** Wykonanie przelewu krajowego na rachunek odbiorcy.  

**Główny przebieg:**
1. Klient wprowadza dane odbiorcy i kwotę przelewu.  
2. System weryfikuje saldo i dzienny limit.  
3. System przesyła zlecenie do operatora rozliczeń.  
4. Klient otrzymuje potwierdzenie przelewu.

**Alternatywy:**
- Kwota przekracza limit → komunikat (BR-02).  
- Brak środków → odrzucenie transakcji (BR-03).  
- Timeout operatora → status „pending” i komunikat (BR-07).

**Powiązania:** BR-01, BR-02, BR-03, BR-07, NFR – Performance

---

## UC-04: Zobacz historię transakcji

**Aktorzy:** Klient, Backend bankowy  
**Cel:** Przegląd i filtrowanie historii transakcji.  

**Główny przebieg:**
1. Klient wybiera zakładkę „Historia”.  
2. System pobiera dane z bazy i wyświetla transakcje.  
3. Klient filtruje dane po dacie, typie lub statusie.  
4. Wyniki wyświetlane są z paginacją (np. po 20 rekordów).

**Alternatywy:**
- Brak danych w wybranym zakresie → komunikat „Brak wyników”.

**Powiązania:** NFR – Performance

---

## UC-05: Zgłoś reklamację przelewu

**Aktorzy:** Klient, Konsultant, Backend bankowy  
**Cel:** Zgłoszenie i obsługa reklamacji dotyczącej przelewu.  

**Główny przebieg:**
1. Klient wybiera transakcję z historii.  
2. Wypełnia formularz reklamacyjny i podaje opis problemu.  
3. System generuje numer sprawy i status „Nowa”.  
4. Konsultant otrzymuje zgłoszenie i nadaje status „W trakcie”.

**Alternatywy:**
- Termin reklamacji przekroczony (BR-05) → komunikat „Reklamacja po terminie”.  
- Brak połączenia z systemem obsługi → komunikat o błędzie.

**Powiązania:** BR-05, NFR – Auditability, KPI-04 (czas odpowiedzi ≤ 48 h)

---



---

📚 *Dokument opracowany w ramach etapu „UML – Use Cases” projektu Mini-bank (04-uml/use-cases.md).*
