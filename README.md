# Rowerek - Aplikacja do wypożyczania rowerów

## Opis aplikacji

**Rowerek** to aplikacja służąca do wypożyczania rowerów, podzielona na pięć głównych modułów. Każdy moduł odpowiada za inny obszar funkcjonalności obsługiwany przez różne „role” (aktorów):

* **Customer** – zarządzanie danymi klientów.
* **Bike** – szczegóły dotyczące rowerów, w tym ustalanie cen (obsługiwane przez firmę zarządzającą zasobami).
* **Maintenance** – usługi serwisowe i naprawcze rowerów (realizowane przez zewnętrzną firmę).
* **Restriction** – regulacje prawne lub ograniczenia konkurencyjne nakładane przez miasto lub inne organy.
* **Reservation** – proces rezerwacji dokonywany przez klientów.

## Implementacja funkcjonalności

W tej chwili brakuje implementacji metody [ReservationService#reserve](./src/main/java/pl/rowerek/reservation/ReservationService.java), która odpowiada za dokonanie rezerwacji roweru.

Po jej zaimplementowaniu wszystkie testy w klasie [ReservationServiceTest](./src/test/java/pl/rowerek/reservation/ReservationServiceTest.java) powinny przechodzić poprawnie. ✅

### Wymagania dotyczące rezerwacji

Podczas rezerwacji należy uwzględnić następujące zasady:

* 🚫 Nie można zarezerwować roweru, jeśli jest już zarezerwowany.
* 🚫 Nie można zarezerwować roweru, jeśli nałożono na niego restrykcję.
* 🚫 Nie można zarezerwować roweru, jeśli aktualnie prowadzone są na nim prace serwisowe.

### Ważne informacje

* W tym zadaniu **nie korzystamy z fasady** – wywołujemy serwisy innych modułów bezpośrednio (serwis jest fasadą :)).
* Metody potrzebne do obsługi powyższych scenariuszy są już dostępne w odpowiednich serwisach – wystarczy je wykorzystać w implementacji.
