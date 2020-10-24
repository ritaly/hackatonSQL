# 2. Analiza klientów banku

Wyobraź sobie, że dołączasz do zespołu analitków pewnego banku. Twoim zadaniem jest uzyskanie jak największej ilości informacji przydatych dla twojego pracodawcy.


### Ustawienia:

1. W pliku `royal_bank_db.sql` znajduje się kod tworzący bazę startową - `ROYAL_BANK_DB`.
2. Uruchom plik w programie Workbench i wykonaj kod (tylko raz - [instrukcja z 2 zajęć](https://youtu.be/so7xe0pO-bE?t=101) )
3. W lewym pasku nawigacji, w zakładce schema pojawi się nowa baza

Aby używać tabeli z bazy konieczne jest wskazanie, którą z baz chcemy wkorzystywać albo jako przedrostek przed nazwą tabeli lub poprzez instrukcję `use <nazwa_bazy>;` .

Wszystkie pośrednie kroki / zapytania, które będziesz wykonywać w tym zadaniu zapisz jako `solution_task_2.sql` i prześlij mi na koniec. Swój tok myślenia możesz również zanotować w formie komentarzy do kodu.


Zapoznaj się z bazą danych

- Załóżmy, że jesteś nowym analitykiem danych w Royal Banku. Ktoś wprowadza Cię do twoich codziennych obowiązków przez filmik wideo https://youtu.be/LZULKsbt0yg (od 2:40). Aby łatwo rozpocząć przeglądanie wszystkich danych, napisz listę zapytań, aby wyświetlić wszystkie dane banku (uruchamiane tylko raz).

- W celu łatwiejszej analizy możesz wykonać diagram EER (Reversed Engineering). Jeżeli go wykonasz dołącz screenshot dorozwiązania.

# Zadania

Dział marketingu zastanwia się, gdzie i komu najlepiej reklamować nasz bank, w którym stanie Australii mamy szansę na największy zysk z samej prowizji posiadacza konta (tj. revenue). Oferujesz swoją pomoc - znajdziesz profile idealnego kandydata do pokazywania reklamy - kandydatów na bazie wiedzy o obecnych klientach. 


#### Wstęp - klienci banku
Na początek przyjrzyj się tabeli klientów. Znajdź najlepiej zarabiających klientów. Z sumuj ich miesięczne wypłaty. Czy jesteś wstanie wskazać sumarycznie najlepiej zarabiający stan? 
Czy o takie wynik chodziło działowi marketingu? Popraw swoją dotyczasową analizę i porównaj sumy nie tylko dochodu, ale również revenue jakie otrzymuje firma w każdym stanie. Zbierz również informacje, która forma korzystania z konta jest najczęściej aktywowana przez klientów.


#### Zapoznanie z transakcjami
Kolejnym ważnym aspektem są transakcje - gdzie i jak się odbywają? W stolicy czy raczej poza nią?
Jak często występują różne typy transakcji (TRAN_TYPE)? Czy karty Debetowe są popularniejsze od zwykłych? Ile w systemie mamy transakcji na kwotę powyżej 150$. Jak często są to transakcje wykonywane na przyjemności lub jedzenie na wynos?

Wskaż transakcje za nawyższe kwoty. Znajdź klienta, który wykonuje transakcje za najwyższe kwoty.
Wyszukaj transakcje, które są wykonywane na kredyt (negatywny balans konta). Wskaż klienta, który ma największe zdłużenie.
Jaki wniosek wynika z tej częsci analizy?

##### Hazard
Załóżmy, że twoją uwagę przyciągneli klienci hazardowi, szczególnie ci którzy dużo obstawiają. Znajdź transakcje na rzecz betEASY oraz bet365, które są wykonywane na kwoty powyżej 100$. Przyjrzyj się również transakcjom z 3 ostatnich dni 2017 roku, jakie kategorie transakcji pojawiają się najczęsciej?

#### Wyzwanie: Raport finansowy.
Załóżmy, że Departament Strategii i Finansów pisze raport z badań ekonomicznych dla dyrektora generalnego, więc zwrócił się do zespołu analityki danych. Prezes musi zobaczyć szerszy kontekst ekonomiczny stojący za sprawozdaniami finansowymi firmy, które widział od stycznia 2018 r. W szczególności jest zaniepokojony tym, jak australijska gospodarka odbudowuje się od sezonu wakacyjnego.
- Znajdź wszystkie wydatki od 1 stycznia 2018 
- Ponieważ usługim handel i ogólnie w większości zamyka się w Nowy Rok, decydujesz się usunąć tę datę z wyników.
- W szczególności zespół ds. Badań ekonomicznych jest najbardziej zainteresowany wydatkami gastronomicznymi, ponieważ ta branża jest najbardziej narażona na recesję gospodarczą. Jako przykład znajdź wszystkie wydatki na jedzenie na wynos w tym samym okresie, aby lepiej zrozumieć wyzwania stojące przed australijskimi restauracjami.
- Proszą również o konkretny przykład restauracji i listę wydatków w ciągu roku. Zdobądź listę transakcji dla wszystkich wydatków w Tony's Pizza. Sprawdź również sumę wydatków.

#### Wyzwanie: Program lojalnościowy. 
Załóżmy, że badamy, komu możemy zaoferować pakiety lojalnościowe. Chcemy wynagrodzić długi staż i wysoką wartość dla banku. Musimy jednak uważać na wielkość inwestycji i wskazać jak najmniejszą grupę klientów, która spełnia rozsądną definicję klienta lojalnego.

1. W jednym zapytaniu znajdź klientów, którzy spełniają którykolwiek z poniższych warunków:
	- który dołączył do banku ponad 50 lat temu (1970)
    - którzy są użytkownikami oddziałów (branch users) i dołączyli do banku ponad 30 lat temu (1990)

2. Widoczna liczba klientów jest zdecydowanie za duża. Załóżmy, że klienci muszą przynosić bankowi co najmniej 2 tys.$ przychodu rocznie.

3. Być może jest to niesprawiedliwe dla klientów, którzy dołączyli do banku 50 lat temu, których powinniśmy nagradzać niezależnie od ich aktualnej wartości dla banku (czyli w podziękowaniu za przeszłą wartość, długą współpracę)
Popraw query tak, aby warunek dochodu w wysokości 2000$ miał zastosowanie tylko do tych, którzy dołączyli ponad 30 lat temu.

