# Wymagania

Wymagania (Requirements) określają, co system powinien robić oraz jakie właściwości i ograniczenia powinien spełniać.

Wymagania powinny być jednoznaczne, zrozumiałe i możliwe do zweryfikowania. Opisujemy oczekiwane zachowanie systemu, a nie sposób jego implementacji.

## Oznaczenia

**FR** (Functional Requirement) — wymaganie funkcjonalne, określające, co system powinien robić.

**NFR** (Non-Functional Requirement) — wymaganie niefunkcjonalne, określające, jakie właściwości lub ograniczenia powinien spełniać system.

Każde wymaganie posiada unikalny identyfikator, np. FR-01 lub NFR-01.

## Wymagania funkcjonalne

| ID | Wymaganie |
|---|---|
| FR-01 | System umożliwia użytkownikowi dodawanie, edycję i usuwanie wydarzeń jednorazowych i cyklicznych z godziną rozpoczęcia, czasem trwania i miejscem. |
| FR-02 | System umożliwia użytkownikowi dodawanie, edycję i usuwanie tasków (zadań) z szacowanym czasem, deadline'em (terminem) i priorytetem. |
| FR-03 | System automatycznie planuje bloki pracy dla tasków w czasie wolnym przed ich deadline'em, z pominięciem przedziałów chronionych. |
| FR-04 | System dzieli blok pracy na bloki skupienia zgodnie z preferencjami pracy użytkownika. |
| FR-05 | System uwzględnia czas przejścia między wydarzeniami w różnych miejscach. |
| FR-06 | System umożliwia użytkownikowi wysłanie promptu w języku naturalnym, który może zmienić plan. |
| FR-07 | System umożliwia użytkownikowi zapisanie checkpointu po zakończeniu bloku pracy. |
| FR-08 | System wykonuje rekalkulację po zmianie wydarzeń, tasków, postępu taska lub kontekstu dnia. |
| FR-09 | System informuje użytkownika, gdy nie istnieje plan dotrzymujący wszystkich deadline'ów, i proponuje zmianę. |
| FR-10 | System przy pierwszym uruchomieniu przeprowadza ankietę początkową ustalającą preferencje pracy użytkownika oraz umożliwia ich późniejszą zmianę. |
| FR-11 | System okresowo przeprowadza ankietę aktualizującą kontekst użytkownika. |
| FR-12 | System prezentuje kalendarz w widoku dnia, tygodnia i miesiąca z wyróżnionymi deadline'ami. |
| FR-13 | System umożliwia użytkownikowi oznaczenie przedziałów jako chronione (np. sen, weekendy, święta). |

## Wymagania niefunkcjonalne

| ID | Wymaganie |
|---|---|
| NFR-01 | System nigdy samodzielnie nie zmienia ani nie usuwa wydarzeń dodanych przez użytkownika. |
| NFR-02 | System nie udostępnia danych kalendarza, lokalizacji, kontekstu użytkownika ani kontekstu dnia podmiotom trzecim bez wyraźnej zgody użytkownika. |
| NFR-03 | Interfejs użytkownika działa na urządzeniach mobilnych i desktopowych. |
| NFR-04 | Interfejs użytkownika spełnia wymagania WCAG 2.2 na poziomie AA. |
| NFR-05 | System umożliwia przeglądanie wcześniej zapisanego kalendarza w trybie offline. |

## Pytania otwarte

- Skąd system pobiera dane do kontekstu dnia (pogoda, sen, aktywność fizyczna)? Ręcznie czy z integracji (np. smartwatch)?
- Czy checkpoint jest obowiązkowy? Co system zakłada, jeśli użytkownik go nie zapisze?
- Czy czas przejścia ma być pobierany automatycznie z zewnętrznego API map na podstawie lokalizacji, czy wprowadzany ręcznie?
- Czy użytkownik może ręcznie przesunąć lub zablokować blok pracy zaplanowany przez agenta?
- Jak często przeprowadzana jest ankieta okresowa?
- Co system robi, gdy przedział chroniony koliduje z blokiem pracy potrzebnym do dotrzymania deadline'u?
- Jak system planuje cele bez deadline'u (np. trening 3 razy w tygodniu)?
- Czy system ma się synchronizować z zewnętrznymi kalendarzami (np. Google Calendar)?
- Jakie konkretne zmiany w kalendarzu może wywołać prompt użytkownika (FR-06) i w jakiej postaci agent je zwraca?
- W jaki sposób priorytet taska wpływa na planowanie bloków pracy (FR-03)?
- Czy użytkownik musi zatwierdzić plan zaproponowany przez agenta, czy agent wprowadza go od razu?
- Jak system reaguje na nakładające się na siebie wydarzenia (konflikt w kalendarzu)?
- Czy system wysyła powiadomienia lub przypomnienia o rozpoczęciu bloku pracy?
- Czy system uczy się realnego tempa pracy użytkownika i automatycznie koryguje szacowany czas tasków?
