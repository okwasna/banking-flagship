### Sequence Diagram – UC-03: Wyślij przelew krajowy

Diagram przedstawia sekwencję komunikatów pomiędzy aktorami i systemami podczas realizacji przelewu krajowego w aplikacji **Mini-bank**.

#### Uczestnicy procesu:
-  **Klient** – inicjuje przelew, wprowadza dane (IBAN, kwotę, tytuł).
-  **Aplikacja bankowa (frontend)** – przekazuje dane do backendu i wyświetla komunikaty.
-  **System bankowy (backend)** – realizuje walidacje i integracje z zewnętrznym systemem rozliczeń.
-  **Operator ELIXIR** – zewnętrzny system rozliczeniowy realizujący przelewy międzybankowe.

---

#### Opis przebiegu głównego (ścieżka sukcesu)
1. Klient wprowadza dane przelewu (IBAN, kwota, tytuł).  
2. Aplikacja przesyła żądanie `POST /transfer` do Systemu bankowego.  
3. System bankowy wykonuje **walidację salda (BR-03)** – sprawdza, czy dostępne środki są wystarczające.  
4. Następnie wykonuje **walidację limitu dziennego (BR-02)** – weryfikuje, czy kwota nie przekracza dozwolonego limitu.  
5. Po pozytywnej walidacji system wysyła żądanie do **operatora ELIXIR** w celu realizacji przelewu.  
6. Operator ELIXIR zwraca status potwierdzenia transakcji.  
7. System aktualizuje saldo i limity, a następnie przekazuje potwierdzenie do aplikacji.  
8. Aplikacja wyświetla komunikat o udanej transakcji użytkownikowi.

---

#### Scenariusze alternatywne
-  **Saldo niewystarczające (BR-03)** – system odrzuca zlecenie i zwraca komunikat  
  *„Brak wystarczających środków na koncie”*.
-  **Limit przekroczony (BR-02)** – system zwraca komunikat  
  *„Limit dzienny został przekroczony”*.


---

#### Uwagi techniczne
- Diagram obejmuje reguły biznesowe: **BR-02, BR-03, BR-07**.  
- Strzałki przerywane oznaczają odpowiedzi (response), strzałki ciągłe – wywołania (request).  
- W Systemie bankowym zastosowano dwa wewnętrzne wywołania (*self-call*):  
  - `sprawdź saldo (BR-03)`  
  - `sprawdź limit (BR-02)`  
 

---

#### Diagram:
![Sequence Diagram – UC-03: Wyślij przelew](https://raw.githubusercontent.com/okwasna/banking-flagship/refs/heads/main/04-uml/sequence-transfer-uc03.drawio.png)

---

 *Diagram opracowany w notacji UML (Sequence Diagram) w narzędziu draw.io w ramach projektu Mini-bank.*

