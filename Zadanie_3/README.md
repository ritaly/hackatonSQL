# 23. Wypożyczalnia DVD

Wyobraź sobie, że wraz ze znajomym kupiliście retro wypożyczalnie i teraz musisz się zająć zdobyciem wszelkiech informacji na jej temat, niczym prawdziwy Biznes Analityk. 


### Ustawienia:

1. W pliku `maven_movies.sql` znajduje się kod tworzący bazę startową.
2. Uruchom plik w programie Workbench i wykonaj kod (tylko raz - [instrukcja z 2 zajęć](https://youtu.be/so7xe0pO-bE?t=101) )
3. W lewym pasku nawigacji, w zakładce schema pojawi się nowa baza

Aby używać tabeli z bazy konieczne jest wskazanie, którą z baz chcemy wkorzystywać albo jako przedrostek przed nazwą tabeli lub poprzez instrukcję `use <nazwa_bazy>;` .

Wszystkie pośrednie kroki / zapytania, które będziesz wykonywać w tym zadaniu zapisz jako `solution_task_3.sql` i prześlij mi na koniec. Swój tok myślenia możesz również zanotować w formie komentarzy do kodu.

Zapoznaj się z bazą danych. Z jakimi danymi będziesz pracowac? Jakie tabele zawiera baza?

- W celu łatwiejszej analizy możesz wykonać diagram EER (Reversed Engineering). Jeżeli go wykonasz dołącz screenshot dorozwiązania.

### Zadania

1. Chcę wysłać maile, aby dać znać klientom o zmianie właściciela firmy i możliwość zgłoszenia uwag RODO. Wygeneruj pełną listę - imię nazwisko i email naszych klientów.

2. Hmmm... jeśli dobrze rozumiem, mamy tytuły, które wypożyczamy z zasady na 3, 5 lub 7 dni? Sprawdź w bazie czy jakiś film nie pasuje do tego schematu wypożyczania?

3. Chcemy przyjrzeć się rekordom płatności naszych lojalnych klientów, aby poznać ich wzorzec zachowań, jeśli chodzi o zakupy. Pobierzmy informacje o pierwszych 100 klientach (bazując na ID klienta). Następnie chcemy sprawdzić ich płatności powyżej 5$ od początku 2006.

4. Dobrze, zostało nam niewielu. W takim razie pobierz wszystkie płatności (niezależnie od daty) dla tych wybranych klientów, o ile płatność wynosiła ponad 5$, tak by zawsze wyświetlić ID klienta, ID wypozyczenia, kwotę oraz datę płatności.

5. Przyjrzyj się bazie filmów. Chcemy sprawdzić w jakich filmach mamy dodatki specjalne takie jak "Behind the Scene".

6. Musimy na szybko dowiedzieć się jak długo są wypożyczane nasze filmy. Czy możesz zdobyć dla mnie informację o liczbie tytułów pogrupowanych wg. czasu wypożyczenia? 

7. Zobaczmy jak dobrze są oceniane filmy w naszej bazie - wyświetl ocenę (`rating`) oraz liczę filmów o danej ocenie.

8. Niektóre płyty to klasyki trudnodostępne obecnie w wersji DVD. Zastanawiam się czy pobieramy wyższą opłatę, jeśli koszt zastąpienia uszkodzonej płyty jest dla nas wyższy (nasze ryzyko)
Czy możesz zliczyć liczbę filmów wraz z średnią, minimalną i maksymalną kwotą stawką wypożyczenia (`rental rate`) pogrupowane wg. kosztu zastąpienia (`replacemenet cost`)

9. Z tabeli wypożyczeń (`rental`) zlicz wszystkie wypożyczenia pogrupowane wg. ID klienta. Wyświetly tylko tam gdzie liczba wypożyczeń jest wyższa lub równa 30.

10. Warto by było porozmawiać z klientami, którzy byli u nas, ale nie wypożyczają za wiele filmów, co możemy zrobić lepiej? Znajdź ID klientów, którzy mają mniej niż 15 wypożyczeń.

11. Zbierzmy teraz trochę informacji o płatnościach. Wyświetl z bazy ID klienta, ID wypożyczenia, kwotę oraz datę płatności posortowane od najwyższej kwoty. Wynik ogranicz do pierwszy 5 wyników (zapoznaj się w google z klauzulą `LIMIT`).

12. Chcielibyśmy sprawdzić najdłuższy z filmów i jednocześnie najdroższy pod względem stawki wypożyczenia. Wyświetl wszystkie tytuły razem z długością trwania filmu i kwotą wypożyczenia w kolejności od najdłuższego do najkrótszego

13. Musimy sprawdzić do jakich sklepów chodzili nasi klienci i czy nadal są aktywnymi użytkownikami. Pobierz imię i nazwisko wszystkich klientów i nadaj im etykietę wg sklepu który odwiedzali np. - store 1 (active), store 1 (inactive), store 2 (active), store 2 (inactive). Skorzystaj z klauzuli `CASE/WHEN/THEN`

14. ⭐️ Te dane są bardzo wartościowe, trzeba jednak sprawdzić ilu mamy klientów nieaktywnych kontra aktywnych w każdym miejscu (lokalnym sklepie). Wyświetl liczbę klientów wg ID sklepu i liczbę aktywnych i nieaktywnych użytkowników (użyj `CASE/WHEN/THEN` oraz grupowania danych po store_id).

15. Czy możesz pobrać informacje o wszystkich filmach które mamy w magazynie? Chcemy zobaczyć tytuł, description oraz ID sklepu dla każdego DVD oraz ID magazynowe (`inventory_id`)

16. Jeden z naszych inwestorów jest zainteresowan naszymi filmami oraz informacją ilu aktorów wyświetlamy dla każdego tytułu. Czy możesz pobrać listę wszystkich tytułów oraz dowiedzieć się jak wielu aktorów wyświetlamy dla każdego tytułu? Wyświetl tytuł nawet jeśli nie mamy w bazie jego aktorów (użyj `LEFT JOIN`).

17. ⭐️ Klienci często pytają, w których filmach występuje ich ulubiony aktor. Przydatny byłby więc zestaw danych z listą wszystkich aktorów oraz tytułami filmów w jakich występują. Czy jesteś w stanie wyciągnąc te dane? [konieczne będzie skorzystanie z tabeli asocjacyjnej `film_actor`(*Associative entity/Bridging*)]

18. Manager w sklepie 2 (`store_id = 2`) proponuje zwiększenie kolekcji filmów. Dowiedz się jakie tytuły posiada na stanie razem z opisami.

19.  Chcemy urządzic wydarzenie firmowy, na które zaprosimy wszystkich członków zespołu (`staff`) oraz naszych doradców (`advisor`). 
Pobierz jako jedną tabelę imiona i nazwiska wszystkich członków zespołu i doradców z dodatkową kolumną, która poinformuje czy dany pracownik nalezy do typu `staff` czy `advisor`. Skorzystaj z klauzuli `UNION`.


