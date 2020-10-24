# 2. Wypożyczalnia DVD

Wyobraź sobie, że wraz ze znajomym kupiliście retro wypożyczalnie i teraz musisz się zająć zdobyciem wszelkiech informacji na jej temat, niczym prawdziwy Biznes Analityk. 


### Ustawienia:

1. W pliku `maven_movies.sql` znajduje się kod tworzący bazę startową.
2. Uruchom plik w programie Workbench i wykonaj kod (tylko raz - [instrukcja z 2 zajęć](https://youtu.be/so7xe0pO-bE?t=101) )
3. W lewym pasku nawigacji, w zakładce schema pojawi się nowa baza

Aby używać tabeli z bazy konieczne jest wskazanie, którą z baz chcemy wkorzystywać albo jako przedrostek przed nazwą tabeli lub poprzez instrukcję `use <nazwa_bazy>;` .

Wszystkie pośrednie kroki / zapytania, które będziesz wykonywać w tym zadaniu zapisz jako `solution_task_3.sql` i prześlij mi na koniec. Swój tok myślenia możesz również zanotować w formie komentarzy do kodu.


Zapoznaj się z bazą danych

- W celu łatwiejszej analizy możesz wykonać diagram EER (Reversed Engineering). Jeżeli go wykonasz dołącz screenshot dorozwiązania.

### Zadania

1. Chcę wysłać maile, aby dać znać klientom o zmianie właściciela firmy i możliwość zgłoszenia uwag RODO. Wygeneruj pełną listę - imię nazwisko i email naszych klientów.

2. Hmmm jeśli dobrze rozumiem, mamy tytuły, które wypożyczamy z zasady na 3, 5 lub 7 dni? Sprawdź w bazie czy jakiś film nie pasuje do tego schematu wypożyczania?

3. Chcemy przyjrzeć się rekordom płatności naszych lojalnych klientów, aby poznać ich wzorzec zachowań, jeśli chodzi o zakupy. Pobierzmy informacje o pierwszych 100 klientach (bazując na ID klienta). Następnie chcemy sprawdzić ich płatności powyżej 5$ od początku 2006.

4. Dobrze, zostało nam niewielu. W takim razie pobierz proszę wszystkie płatności (niezależnie od daty) dla tych wybranych klientów o ile płatność wynosiła ponad 5$, tak by zawsze wyświetlić ID klienta, ID najmowania, kwotę oraz datę płatności.

5. Przyjrzyj się bazie filmów. Chcemy sprawdzić w jakich filmach mamy dodatki specjalne takie jak "Behind the Scene".

6. Musimy na szybko dowiedzieć się jak długo są wypożyczane nasze filmy. Czy możesz zdobyć dla mnie informację o liczbie tytułów pogrupowanych wg. czasu wypożyczenia? 

7. Zobaczmy jak dobrze są oceniane filmy w naszej bazie - wyświetl ocenę (rating) oraz liczę filmów o danej ocenie.

8. Niektóre płyty to klasyki trudnodostępne obecnie w wersji DVD. Zastanawiam się czy pobieramy wyższą opłatę, jeśli koszt zastąpienia uszkodzonej płyty jest dla nas wyższy (nasze ryzyko) Czy możesz zliczyć liczbę filmów wraz z średnią, minimalną i maksymalną kwotą stawką wypożyczenia (rental rate) pogrupowane wg. kosztu zastąpienia (replacemenet cost)

9.

10.

11.
 


