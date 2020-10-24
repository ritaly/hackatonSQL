# 1. Ludzkie czy psie imię?

Do analizy otrzymujesz bazę, która posiada 2 tabele z informacjami na temat nadawania imion psom.

1. Baza 100 najpopularniejszych imion dziecięcych nadawnych w południowej Australii w 2019
2. Baza wszystkich imion psich nadawanych na Słonecznym Wybrzeżu (Queensland, Australia 2019)

Rostrzgnijmy hipotetyczne pytanie są imiona bardziej odpowiednie dla psów lub dla zwierząt.


### Ustawienia:

1. W pliku `dog_baby_names.sql` znajduje się kod tworzący bazę startową - `DOG_BABY_NAMES_DB`.
2. Uruchom plik w programie Workbench i wykonaj kod (tylko raz - [instrukcja z 2 zajęć](https://youtu.be/so7xe0pO-bE?t=101) )
3. W lewym pasku nawigacji, w zakładce schema pojawi się nowa baza

Aby używać tabeli z bazy konieczne jest wskazanie, którą z baz chcemy wkorzystywać albo jako przedrostek przed nazwą tabeli lub poprzez instrukcję `use <nazwa_bazy>;` .

Wszystkie pośrednie kroki / zapytania, które będziesz wykonywać w tym zadaniu zapisz jako `solution_task_1.sql` i prześlij mi na koniec. Swój tok myślenia możesz również zanotować w formie komentarzy do kodu.


### Zadanie

Celem zadania jest stwierdzenie czy wybrane imię jest bardziej popularne u ludzi czy u psów?
Na warsztat weźmiemy imię **Max** oraz **Jess**.

Zbierz informacje wstępne o nowym zbiorze danych. Pytania potraktuj jak podpowiedzi. 

1. Odpowiednim poleceniem wyświetl informacje o tabelach
2. Wyświetl tabele i wstępnie przejrzyj otrzymane dane.
3. Ile rekordów jest w każdej z tych baz?

Zastanów się w jaki sposób wyciągnąć dane o powyższych imionach? 
Wszystkie imiona związane z zadanymi imionami dla psów jak i dla dzieci.

1. Ile psów nosi imię zawierające imię Max / Jess? 
2. Czy te wariacje będą dla nas się liczyć?
3. Ile dzieci nosi powyższe imiona i ich wariacje?
4. Czy te liczby da się w prosty sposób porównać? Dlaczego tak / dlaczego nie?

Zbadaj proporcje częstotliwości występowania przez wyliczenie udziału procentowego imienia w całym zbiorze danych.

- Czy imię Max jest bardziej popularne u ludzi czy u zwierząt?
- Czy imię Jess jest bardziej popularne u ludzi czy u zwierząt?

Inspirację z rozwiązaniem tego zadania znajdziesz na YT: https://youtu.be/GrCnVH8Aswg

##### Łączenie danych

Znajdź imiona, które częściej pojawiają się w bazie zwierząt niż u ludzi.

Znajdź wśród tych imion takie, które są typowym imieniem zwierzęcym (znacznie częsciej takie imię nosi zwierze niż człowiek). Pamiętaj, że bazy różnią się wielkością.



