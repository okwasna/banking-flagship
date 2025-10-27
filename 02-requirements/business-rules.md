#  Reguły biznesowe v1 – projekt Mini-bank

Dokument zawiera zestaw podstawowych **reguł biznesowych (Business Rules)** obowiązujących w systemie Mini-bank.  
Każda reguła posiada unikalny identyfikator (BR-ID), opis działania oraz uzasadnienie biznesowe (cel).

---

##  Lista reguł biznesowych

| ID | Nazwa / Obszar | Opis reguły | Cel biznesowy |
|----|----------------|--------------|----------------|
| **BR-01** | Limits | Domyślny dzienny limit przelewów wynosi **20 000 PLN**. | Kontrola ryzyka i zapobieganie nadużyciom finansowym. |
| **BR-02** | Over limit | Jeśli kwota przelewu przekracza ustalony limit → transakcja jest blokowana, a użytkownik otrzymuje komunikat z instrukcją zwiększenia limitu. | Transparentność i bezpieczeństwo transakcji. |
| **BR-03** | Funds | Jeśli na koncie nie ma wystarczających środków → transakcja zostaje odrzucona z komunikatem pokazującym brakującą kwotę. | Ochrona użytkownika i zapobieganie błędnym transakcjom. |
| **BR-04** | KYC gate | Konto użytkownika staje się **aktywne dopiero po pozytywnej weryfikacji KYC**. | Zgodność z regulacjami bankowymi i AML. |
| **BR-05** | Claim window | Reklamację można złożyć **w ciągu 30 dni** od daty wykonania transakcji. | Uporządkowanie procesu reklamacyjnego i archiwizacji danych. |
| **BR-07** | Timeout sesji / Przelewy, Logowanie | System automatycznie przerywa operację, jeśli użytkownik nie potwierdzi działania (np. przelewu lub logowania) w ciągu **60 sekund**. Po przekroczeniu limitu czasu system wyświetla komunikat: *„Przekroczono limit czasu – spróbuj ponownie.”* | Zapewnienie bezpieczeństwa sesji oraz stabilności systemu poprzez unikanie zablokowania zasobów przy długotrwałej bezczynności użytkownika. |
---

##  Uwagi

- Reguły obowiązują w wersji **MVP (v1.0)** systemu Mini-bank.  
- Każda reguła może być rozszerzana o warunki, wyjątki i powiązane procesy BPMN.  

---

📚 *Dokument opracowany w ramach etapu „Requirements” projektu Mini-bank (02-requirements/business-rules.md).*

