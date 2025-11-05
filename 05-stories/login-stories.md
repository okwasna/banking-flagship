#  UC-02 – Zaloguj się do systemu (z uwierzytelnieniem 2FA)

Dokument zawiera zestaw **User Stories** opisujących przypadek użycia *UC-02 – Logowanie użytkownika*  
w systemie **Mini-bank**. Historie obejmują scenariusz sukcesu oraz warianty błędów i blokady konta.

---

##  Story 1 – Prawidłowe logowanie z 2FA

**Jako** klient banku  
**chcę** móc zalogować się do aplikacji w bezpieczny sposób,  
**aby** uzyskać dostęp do mojego konta.

**Opis:**  
Użytkownik podaje login i hasło. System weryfikuje poprawność danych oraz sprawdza, czy konto nie jest zablokowane.  
Następnie aplikacja wymusza drugą metodę uwierzytelnienia (kod SMS lub powiadomienie push).  
Po potwierdzeniu tożsamości system tworzy sesję i wyświetla ekran główny.

**Rezultat:**  
- Użytkownik uzyskuje dostęp do systemu.  
- Licznik nieudanych prób logowania zostaje zresetowany.  

---

##  Story 2 – Niepoprawny login lub hasło

**Jako** klient banku  
**chcę** otrzymać informację, że dane logowania są nieprawidłowe,  
**aby** wiedzieć, dlaczego nie mogę wejść do systemu.

**Opis:**  
Po podaniu błędnego loginu lub hasła system zwiększa licznik nieudanych prób.  
Użytkownik otrzymuje komunikat o błędzie i wraca do ekranu logowania.

**Rezultat:**  
- Brak dostępu do systemu.  
- Licznik prób logowania rośnie.  
- Wyświetlany jest komunikat: **„Nieprawidłowy login lub hasło”**.

---

##  Story 3 – Blokada konta po zbyt wielu błędach

**Jako** klient banku  
**chcę** wiedzieć, że moje konto zostało czasowo zablokowane po serii błędów,  
**aby** rozumieć powód braku dostępu.

**Opis:**  
Jeżeli liczba nieudanych prób logowania przekroczy limit (np. 5), system blokuje konto na ustalony czas.  
Użytkownik widzi komunikat o blokadzie i nie może kontynuować logowania.

**Rezultat:**  
- System uniemożliwia dalsze próby logowania.  
- Wyświetlany jest komunikat: **„Konto zostało tymczasowo zablokowane”**.  

---

##  Story 4 – Błędna weryfikacja drugiego etapu (2FA)

**Jako** klient banku  
**chcę** otrzymać informację o nieudanej weryfikacji kodu,  
**aby** móc spróbować ponownie lub wybrać inną metodę.

**Opis:**  
Po podaniu niewłaściwego kodu SMS lub odrzuceniu powiadomienia push  
system informuje użytkownika o błędzie i zwraca go do ekranu logowania.

**Rezultat:**  
- Logowanie nie zostaje zakończone.  
- Wyświetlany jest komunikat: **„Niepoprawne uwierzytelnienie 2FA”**.

---

##  Story 5 – Reset licznika po udanym logowaniu

**Jako** klient banku  
**chcę** aby system zapominał o poprzednich błędnych próbach,  
**aby** moje konto nie było zagrożone blokadą mimo prawidłowego logowania.

**Opis:**  
Po poprawnym uwierzytelnieniu 2FA system usuwa historię nieudanych prób.  
Mechanizm ten zapobiega przypadkowym blokadom w przyszłości.

**Rezultat:**  
- Licznik prób logowania = 0.  
- Konto działa bez ograniczeń.

---

##  Powiązane reguły biznesowe

| ID | Nazwa reguły | Opis |
|----|--------------|------|
| **BR-01** | Walidacja danych logowania | System sprawdza poprawność loginu i hasła. |
| **BR-02** | Limit prób logowania | Po X nieudanych próbach konto zostaje zablokowane. |
| **BR-03** | Wymuszony 2FA | Każde logowanie wymaga dodatkowego potwierdzenia. |
| **BR-04** | Obsługa błędnego 2FA | Nieudane potwierdzenie skutkuje powrotem do logowania. |
| **BR-05** | Reset licznika | Po sukcesie licznik nieudanych prób wraca do zera. |

---
