#  Wymagania niefunkcjonalne (NFR) – projekt Mini-bank

Dokument definiuje kluczowe **wymagania niefunkcjonalne (Non-Functional Requirements)** dla systemu Mini-bank.  
Opisują one jakość działania systemu – jego wydajność, bezpieczeństwo i dostępność.

---

##  Performance (wydajność)

| Obszar | Wymaganie | Metryka |
|---------|------------|---------|
| **Przelewy (API endpoint: POST /transfers)** | 95% operacji (P95) realizowanych w czasie ≤ 2 sekundy przy obciążeniu **50 RPS** (requests per second). | P95 ≤ 2 s |

 *Cel: zapewnienie płynnego działania aplikacji i pozytywnego doświadczenia użytkownika (UX).*

---

##  Security (bezpieczeństwo)

| Obszar | Wymaganie | Metryka |
|---------|------------|---------|
| **Logowanie** | Wymagane **uwierzytelnianie dwuskładnikowe (2FA)**. | 100% prób logowania z 2FA |
| **Dane osobowe (PII)** | Wszystkie dane osobowe muszą być **szyfrowane „at rest”** (w bazie danych). | AES-256 lub równoważny standard szyfrowania |

 *Cel: ochrona danych klientów i zgodność z przepisami RODO/AML.*

---

##  Availability (dostępność)

| Obszar | Wymaganie | Metryka |
|---------|------------|---------|
| **System (MVP)** | Dostępność systemu na poziomie **≥ 99.5% miesięcznie** (z wyłączeniem okien serwisowych). | 99.5% uptime |

 *Cel: zapewnienie stabilności i zaufania klientów do systemu bankowego.*

---

📚 *Dokument opracowany w ramach etapu „Requirements” projektu Mini-bank (02-requirements/nfr.md).*

