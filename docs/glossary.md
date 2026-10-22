# Słownik domenowy

| Pojęcie | Definicja |
|---|---|
| Użytkownik | Osoba, której grafik jest w aplikacji |
| Grafik | Struktura danych definiująca stan zajętości użytkownika w różnych przedziałach czasowych |
| Plan tygodniowy | Struktura danych definiująca wydarzenia powtarzające się co 7 dni |
| Wydarzenie | Blok czasowy ze zdefiniowanym początkiem, końcem (lub czasem trwania), stanem zajętości użytkownika i ewentualnie miejscem |
| Task | Zadanie do wykonania przez użytkownika zdefiniowane przez termin i czas potrzebny na wykonanie |
| Termin | Punkt w grafiku, przed którym dany task musi byc zakończony |
| Wolny | Stan zajętości, który jest dostępny do dodawania wydarzeń przez użytkownika i solver |
| Solver | Agent dodający wydarzenia związane z taskami do grafiku w czasie wolnym |
| Odpoczynek | Stan zajętości, który jest dostępny do dodawania wydarzeń tylko dla użytkownika |
| Zajęty | Stan zajętości, który nie jest wolnym ani odpoczynkiem. Zastąpienie takiego wydarzenia wymaga rekalkulacji grafiku |
| Rekalkulacja | Funkcja szukająca najlepszego rozwiązania grafiku. Jeśli takie nie istnieje może dać propozycję jakiejś zmiany lub odradzić zmianę |
| Rozwiązanie | Układ grafiku, w którym wszystkie terminy są zaspokojone i żadne wydarzenie użytkownika nie jest zmienione|

