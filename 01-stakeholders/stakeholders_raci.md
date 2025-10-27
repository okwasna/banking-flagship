#  Interesariusze – projekt Mini-bank

Dokument definiuje interesariuszy projektu **Mini-bank** oraz ich role i odpowiedzialności w ramach systemu.  
Zawiera listę aktorów (zewnętrznych i wewnętrznych).

---

##  Aktorzy systemu (zewnętrzni)

| Nazwa | Typ | Opis |
|--------|------|------|
| **Klient (użytkownik aplikacji)** | Osoba fizyczna | Korzysta z aplikacji bankowej: zakłada konto, loguje się, wykonuje przelewy, składa reklamacje. |
| **Aplikacja bankowa (frontend)** | System | Interfejs użytkownika – umożliwia logowanie, podgląd salda i wykonywanie przelewów. |
| **System bankowy (backend)** | System | Warstwa serwerowa – odpowiada za logikę biznesową, przetwarzanie danych i komunikację z modułami. |
| **Zewnętrzny operator rozliczeń (np. ELIXIR)** | System zewnętrzny | Realizuje przekazy pieniężne między bankami. W systemie Mini-bank jest traktowany abstrakcyjnie. |
| **Moduł KYC/AML** | System zewnętrzny / usługa | Odpowiada za weryfikację tożsamości użytkownika i sprawdzanie ryzyka prania pieniędzy. |
| **Konsultant (obsługa klienta)** | Osoba | Pracownik banku odpowiedzialny za przyjmowanie reklamacji i kontakt z klientem. |

---

##  Aktorzy wewnętrzni (projektowi)

| Nazwa | Typ | Opis |
|--------|------|------|
| **Analityk biznesowo-systemowy** | Rola projektowa | Odpowiada za analizę wymagań, modelowanie procesów i dokumentację. |
| **Product Owner (PO)** | Rola projektowa | Reprezentuje biznes, zatwierdza wymagania i priorytety. |
| **Zespół deweloperski (Frontend + Backend)** | Rola techniczna | Tworzy i utrzymuje kod systemu. |
| **Tester / QA** | Rola projektowa | Weryfikuje poprawność działania systemu i testuje wymagania. |
| **Administrator / DevOps** | Rola techniczna | Dba o wdrożenie, bezpieczeństwo i wydajność środowiska. |


---

📚 *Dokument opracowany w ramach etapu „Stakeholders” projektu Mini-bank (01-stakeholders/stakeholders_raci.md).*
