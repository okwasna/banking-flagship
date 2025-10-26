#  UC-03 – Wyślij przelew  

Dokument zawiera zestaw **User Stories** opisujących przypadek użycia *UC-03 – Wyślij przelew krajowy*  
w systemie **Mini-bank**. Historie obejmują zarówno scenariusz sukcesu, jak i warianty błędów oraz działania audytowe.

---

##  Story 1 – Wysłanie poprawnego przelewu  

**Jako** klient banku  
**chcę** móc wysłać przelew krajowy z aplikacji,  
**aby** zapłacić odbiorcy w prosty i szybki sposób.  

**Opis:**  
Klient loguje się do aplikacji bankowej, wprowadza dane przelewu (IBAN, kwota, tytuł) i zatwierdza operację.  
System weryfikuje saldo oraz dzienny limit, a następnie przesyła zlecenie przelewu do operatora ELIXIR.  
Po otrzymaniu potwierdzenia system aktualizuje saldo i informuje klienta o sukcesie.  

**Rezultat:**  
- Przelew został zrealizowany.  
- Saldo oraz historia konta są zaktualizowane.  

---

##  Story 2 – Brak wystarczających środków  

**Jako** klient banku  
**chcę** otrzymać informację, że nie mogę wykonać przelewu z powodu braku środków,  
**aby** wiedzieć, dlaczego transakcja się nie powiodła.  

**Opis:**  
Podczas wysyłania przelewu system sprawdza saldo konta.  
Jeżeli kwota przelewu przekracza dostępne środki, transakcja jest odrzucana.  
Aplikacja informuje użytkownika o błędzie, nie wysyłając żądania do operatora.  

**Rezultat:**  
- Przelew nie zostaje wykonany.  
- Saldo i limit pozostają bez zmian.  
- Wyświetlany jest komunikat: **„Brak wystarczających środków na koncie”**.  

---

##  Story 3 – Przekroczony limit dzienny  

**Jako** klient banku  
**chcę** otrzymać informację, że przekroczyłem dzienny limit przelewów,  
**aby** móc zaplanować przelew w innym terminie.  

**Opis:**  
System weryfikuje, czy po dodaniu aktualnej kwoty przelewu limit dzienny nie zostanie przekroczony.  
Jeśli tak się stanie, przelew nie jest zrealizowany, a użytkownik otrzymuje informację o przekroczeniu limitu.  

**Rezultat:**  
- Przelew nie zostaje wysłany do operatora.  
- Użytkownik widzi komunikat: **„Limit dzienny przekroczony”**.  

---

##  Story 4 – Aktualizacja salda i historii po przelewie  

**Jako** klient banku  
**chcę** widzieć odświeżone saldo i historię po wysłaniu przelewu,  
**aby** mieć pewność, że operacja została poprawnie zaksięgowana.  

**Opis:**  
Po potwierdzeniu przelewu przez system bankowy, aplikacja automatycznie aktualizuje saldo konta oraz dodaje nową pozycję w historii transakcji.  
Zmiana widoczna jest natychmiast po powrocie do ekranu głównego.  

**Rezultat:**  
- Saldo zostało pomniejszone o kwotę przelewu.  
- Historia zawiera nową pozycję z bieżącą datą i statusem „Wysłany”.  

---


##  Powiązane reguły biznesowe  

| ID | Nazwa reguły | Opis |
|----|---------------|------|
| **BR-02** | Limit dzienny | Kwota przelewów w ciągu dnia nie może przekroczyć ustalonego limitu. |
| **BR-03** | Saldo konta | Przelew może być wykonany tylko, jeśli saldo jest wystarczające. |

