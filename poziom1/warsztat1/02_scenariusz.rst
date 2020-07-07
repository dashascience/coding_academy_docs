Scenariusz warsztatu 1 - poziom początkujący
############################################

Intro - O co chodzi z programowaniem
************************************

Definicje
=========

* **Język programowania** to sposób komunikacji programisty z komputerem

    * "normalni ludzie" używają interfejsu uzytkownika
    * programiści piszą kod

* **Programowanie** to tworzenie zadań / poleceń dla komputera za pomocą języka programowania.
* **Program** to dla komputera przepis na wykonanie jakiejś pracy (jak przepis na ciasto)

    * program podobnie jak przepis składa się z kroków do wykonania. Te kroki to **instrukcje**.

Języki programowania
====================

* Niskopoziomowe - kod niezrozumiały dla człowieka, szybkie, bliskie kodu maszynowego. [np Assembler]
* Wysokopoziomowe - operują na zmiennych, obiektach, funkcjach, dlatego są możliwe do używania przez ludzi.
  [np Python, Java, C#]

* Kompilowane - aby uruchomić program konieczna jest kompilacja tzn zamiana instrukcji zrozumiałych dla człowieka na
  takie zrozumiałe dla komputera.
* Interpretowane - kompilacja dzieje się w locie (w trakcie uruchamiania).

Dlaczego wybraliśmy Pythona?
============================

* niski próg wejścia (łatwo się go nauczyć)
* wysokiego poziomu (kod jest zrozumiały dla człowieka)
* ogólnego zastosowania (można używać go do stworzenia wielu różnych rzeczy np. aplikacja webowa, desktopowa, skrypty)
* popularny (łatwo znaleźć odpowiedź na pytania)

   .. figure:: images/popular.png
      :width: 400

      Popularność języków programowania wg github.com


Zainstalowaliśmy środowisko, jak z niego korzystać - prezentacja możliwości
===========================================================================

* repl.it

    * pojedyncze komendy w REPL (Read-Eval-Print Loop)
    * pliki .py i uruchamianie z terminala

* pyCharm

B01 - Python: elementy składni języka
*************************************

Składnia - zmienne
==================

* Zmienne służą do przechowywania wartości (np wyniku obliczeń, ciągu znaków lub obiektu)
* zmienna ma nazwę i typ, natomiast typu nie trzeba jawnie deklarować - python jest dynamicznie typowany, więc domyśli
  się jakiego typu powinna być
  zmienna na podstawie wyrażenia z prawej strony instrukcji przypisania (=)
* Przypisywanie wartości do zmiennej (mechanizm i pokazanie co dzieje się w pamięci operacyjnej)

.. code-block:: python

   nazwa_zmiennej = <wartosc / wyrazenie>

Wyświetlanie wartości zmiennej
==============================

Do wyświetlenia wartości zmiennej używamy funkcji ```print()```. Wewnątrz nawiasów umieszczamy to, co chcemy wyświetlić.
Jeśli argumentem fukcji print będzie zmienne, to wyświetlona zostanie jej wartość. Jeli argumentem będzie literał,
to wyświetlony zostanie literał. Zobacz przykład:

.. code-block:: python

   imie = 'Jacek'
   nazwisko = 'Kowalski'
   print(imie)
   print('imie')
   # Zauważ, że argumentem funkcji print() może być wyrażenie, wówczas wyświetlony zostanie wynik wyrażenia:
   print(2+4)
   print(imie + ' ' + nazwisko)

.. note::
   | Ćwiczenie
   | Do zmiennych o nazwach imie, nazwisko, wiek przypisz odpowiedni swoje imię, nazwisko i wiek.
   | Wyświetl na akranie zdanie: **Nazywam się <imie> <nazwisko>, mam <wiek> lat.**

Znak końca linii
================

Znak ```\n``` oznacza koniec linii. Gdy istnieje konieczność zwrócenia wielu linii jedną komendą ```print()``` należy zastosować właśnie taki znak.

.. code-block:: python

   linia1 = 'To jest linia 1'
   linia2 = 'To jest linia 2'
   print(linia1 + linia2)
   print(linia1 + '\n' + linia2)

Operatory arytmetyczne
======================

    * operatory (+ - * /)
    * operatory ** i %
    * wyrażenia
    * wartości
    * kolejność operatorów
    * składnia, co to jest SyntaxError

.. note::
   | Ćwiczenie 1
   | Za pomocą REPL wykonaj operacje arytmetyczne:

   .. code-block::

      128*256
      100/33
      2 do potęgi 16
      reszta z dzielenia 100 przez 8

   | Ćwiczenie 2
   | Wykonaj te same operacje w pliku main.py. Zwróć wyniki na ekran używając funkcji print()

Operatory logiczne
==================

    * Zmienna typu boolean może przyjmować tylko 2 wartości: True, False
    * Każdy obiekt posiada wartość typu boolean.

        * Jako False rozwiązane zostaną: None, False, 0, puste kolekcje ("", (), [], {})
        * Wszystkie inne obiekty zostaną rozwiązane jako True
        * Gdy klasa zawiera implementację metod __len__(self) lub __nonzero__(self), to te metody wpływają na wynik
          (nie ma co tego bardziej rozwijać na tym poziomie, warto wspomnieć, że można ręcznie sterować

    * Operatory powównania (<, <=, >, >=, ==, !=)

Type annotatnions
=================

* Typy danych (pokaż podział i opowiedz)

   .. figure:: images/python_data_types.jpg
      :width: 400

      Typy danych w języku Python

B02 - Python: numeryczne typy danych
************************************

int - liczby całkowite
======================

float - liczby zmiennoprzecinkowe
=================================

B03 - Python: logiczne typy danych
**********************************

bool
====

None
====

B04 - Python: łańcuchy znaków
*****************************

string
======

Operacje na danych typu string (znakowych) - metody
===================================================

.. code-block:: python

   # Operacje na zmiennych znakowych (string)
   imie = 'Michał'
   nazwisko = 'Kowalski'
   # Operator '+' w przypadku zmiennych znakowych łączy dane
   print(imie+nazwisko)
   # Pamiętajmy o spacji pomiędzy
   print(imie+' '+nazwisko)
   # Długość imienia
   print(len(imie))

Pobieranie danych od użytkownika - funkcja input()
==================================================

Funkcja input() po wywołaniu oczekuje na znaki wpisane z klawiatury. Po wprowadzeniu znaków zwraca wpisany przez
uzytkownika ciąg znaków. Można go wtedy np przypisać do zmiennej. Pamiętać należy, że funkcja input() zawsze zwraca
zmienną typu string!

.. code-block:: python

   imie = input('Podaj imie: ')
   wiek = input('Podaj wiek: ')
   print('Masz na imie ' + imie)
   print('Masz ' + wiek + ' lat.')
   print('Zmienna imie jest typu ' + str(type(imie)))
   print('Zmienna wiek jest typu ' + str(type(wiek)))

Zwróć uwagę na konstrukcję ```str(type(imie))```. To jest rzutowanie typów. Zajmiemy się nim teraz.

B05 - Python: sekwencje
***********************

W języku Python występują dwa główne typy reprezentujące sekwencje obiektów: listy (ang. list) i krotki (ang. tuple).
Sekwencja obiektów to taki obiekt który przechowuje inne obiekty. Obiekty te mają zdefiniowaną kolejność.

tuple
=====

Krotki tworzymy poprzez proste wylistowanie obiektów oddzielonych przecinkiem. Krotka może mieścić w sobie elementy
dowolnego typu. Członkami tej samej krotki mogą nawet być obiekty różnych typów.

.. code-block:: python

    # Współrzędne GPS budynku ING na Sokolskiej 34 w Katowicach
    >>> sokolska_34_gps = 50.265196, 19.018155
    >>> sokolska_34_gps
    (50.265196, 19.018155)

    # Współrzędne konia na planszy szachowej
    >>> chess_knight_location = "B", 5
    >>> chess_knight_location
    ('B', 5)


Często spotykaną praktyką przy tworzeniu krotki jest umieszczanie listy elementów krotki w okrągłych nawiasach. Widzimy
nawet, że taka reprezentacja krotki jest stosowana domyślnie przez konsolę REPL. Stosowanie nawiasów poprawia czytelność
kodu, jednak trzeba pamiętać, że podobnie jak w znanych nam wyrażeniach matematycznych, tak i tu nie są one wymagane.

.. code-block:: python

    # Poniższe dwa sposoby tworzenia krotek są sobie równoważne
    >>> tuple_1 = 1, 2, 3, 4, 5
    >>> tuple_1
    (1, 2, 3, 4, 5)

    >>> tuple_2 = (1, 2, 3, 4, 5)
    >>> tuple_2
    (1, 2, 3, 4, 5)

Aby utworzyć krotkę pustą lub jednoelementową, trzeba posłużyć się specjalnymi elementami składni. Krotka pusta tworzona
jest poprzez wykorzystanie konstruktora ``tuple``, natomiast krotka jednoelementowa wymaga postawienia przecinka za
wartością wchodzącą w jej skład.

.. code-block:: python

    # Krotka pusta
    >>> tuple()
    ()

    # Krotka z jednego elementu
    >>> 3,
    (3,)

    # Przecinek można też postawić na końcu dowolnie długiej krotki
    >>> 2, 3, 5, 7, 11,
    (2, 3, 5, 7, 11)


list
====

Listę obiektów, podobnie jak krotkę, tworzymy poprzez wylistowanie elementów oddzielonych przecinkami, całość obejmując
jednak nawiasami kwadratowymi. Listy również mogą mieścić w sobie elementy dowolnych typów. Mogą to być liczby
całkowite, mogą to być napisy, oraz inne typy obiektów. Każdy element tej samej listy może być innego typu.

.. code-block:: python

    # Lista wyników totolotka
    >>> lotto_numbers = [3, 17, 19, 23, 27, 31]
    >>> lotto_numbers
    [3, 17, 19, 23, 27, 31]

    # Lista angielskich dni tygodnia
    >>> days_of_week = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
    >>> days_of_week
    ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']

    # Lista zawierająca imię, nazwisko (napisy) oraz wiek (liczba) jednego pracownika.
    >>> employee = ['Jan', 'Kowalski', 24]
    >>> employee
    ['Jan', 'Kowalski', 24]

    # Pusta lista
    >>> []
    []
    >>> list()
    []

    # Przecinek za ostatnim elementem listy jest również dozwolony
    >>> [3, 2, 1,]
    [3, 2, 1]

Aby odwołać się do poszczególnych elementów krotki lub listy również wykorzystujemy nawiasy kwadratowe. Tym razem
podajemy w nich indeks danego elementu. Indeksem jest numer pozycji licząc od 0. Można również liczyć pozycję od
ostatniego elementu używając indeksów ujemnych.

.. code-block:: python

    # Składowe pola na planszy szachowej
    >>> chess_knight_location = ("B", 5)
    >>> chess_knight_location[0] # kolumna
    'B'
    >>> chess_knight_location[1] # rząd
    5

    # Pierwsza, druga i ostatnia liczba wyniku totolotka licząc od początku
    >>> lotto_numbers = [3, 17, 19, 23, 27, 31]
    >>> lotto_numbers[0] # pierwsza liczba
    3
    >>> lotto_numbers[1] # druga liczba
    17
    >>> lotto_numbers[5] # szósta liczba
    31

    # Pierwsza, druga i ostatnia liczba wyniku totolotka licząc od końca
    >>> lotto_numbers[-6] # pierwsza liczba
    3
    >>> lotto_numbers[-5] # druga liczba
    17
    >>> lotto_numbers[-1] # szósta liczba
    31

    # Dane pracownika
    >>> employee = ['Jan', 'Kowalski', 24]
    >>> first_name = employee[0]
    >>> last_name = employee[1]
    >>> age = employee[2]
    >>> print(first_name, last_name, age, "lata")
    Jan Kowalski 24 lata

Mając krotkę lub listę możemy również sprawdzić liczbę elementów przez użycie funkcji wbudowanej ``len``, sprawdzić czy
dana wartość występuje w sekwencji poprzez operator ``in``, wyszukać indeks elementu o zadanej wartości za pomocą metody
``index`` oraz policzyć liczbę wystąpień zadanej wartości za pomocą metody ``count``.

.. code-block:: python

    >>> numbers = (1, 4, 5, 3, 4, 1, 6)
    >>> len(numbers) # liczba elementów krotki
    7
    >>> 4 in numbers # sprawdzenie czy wartość 4 występuje w sekwencji
    True
    >>> numbers.index(4) # pozycja pierwszego wystąpienia wartości 4
    1
    >>> numbers.count(4) # liczba wystąpień wartości 4 w sekwencji
    2

    # Ten same operacje dostępne są również na liście
    >>> numbers = [1, 4, 5, 3, 4, 1, 6]
    >>> len(numbers) # liczba elementów krotki
    7
    >>> 4 in numbers # sprawdzenie czy wartość 4 występuje w sekwencji
    True
    >>> numbers.index(4) # pozycja pierwszego wystąpienia wartości 4
    1
    >>> numbers.count(4) # liczba wystąpień wartości 4 w sekwencji
    2

Dwie listy lub dwie krotki możemy skleić ze sobą za pomocą operatora dodawania. Taka operacja nazywasię konkatenacja.
Typy sekwencji sklejanych muszą się zgadzać, czyli nie możemy skleić listy z krotką.

.. code-block:: python

    >>> (5, 2, 4) + (2, 4, 1)
    (5, 2, 4, 2, 4, 1)

    >>> ['Alicja', 'Monika', 'Natalia'] + ['Jerzy', 'Mateusz', 'Robert']
    ['Alicja', 'Monika', 'Natalia', 'Jerzy', 'Mateusz', 'Robert']

Możemy stworzyć krotkę bądź listę złożoną z powtórzonej sekwencji elementów wykorzystując operator mnożenia przez liczbę
całkowitą.

.. code-block:: python

    >>> [0, 1] * 5
    [0, 1, 0, 1, 0, 1, 0, 1, 0, 1]

    >>> (0,) * 10
    (0, 0, 0, 0, 0, 0, 0, 0, 0, 0)

Skoro zarówno krotka jak i lista są sekwencjami obiektów to jaka jest podstawowa różnica pommiędzy nimi?
Odpowiedź jest prosta. Krotka nie może zostać zmodyfikowana, lista natomiast może. O obiektach, któryh wartość nie
zmienia się mówimy, że są niemutowalne (ang. immutable). Obiekty których wartość może po utworzeniu ulec zmianie są
mutowalne (ang. mutable). Obiekty niemutowalne mają wiele zalet nad swoimi mutowalnymi odpowiednikami. Jedną z głównych
zalet jest możliwość łatwiejszego wykorzystania w obliczeniach współbieżnych.

Zobaczmy jednak w jaki sposób elementy listy mogą być zmieniane. Najprostszymi operacjami modyfikacji listy jest
dodawanie i usuwanie pojedynczych jej elementów jak również wymiana wartości znajdujących się na określonej pozycji.
Aby to zobaczyć odwiedźmy hinduską restaurację.

.. code-block:: python

    # Zacznijmy od pustej listy
    >>> ordered_dishes = []
    >>> ordered_dishes
    []

    # Na początek weźmy jakieś przekąski
    >>> ordered_dishes.append('Bakłażan w cieście')
    >>> ordered_dishes.append('Samosa wegetariańska') #  to dla dziewczyny
    >>> print(ordered_dishes)
    ['Bakłażan w cieście', 'Samosa wegetariańska']

    # Po 15 minutach miłej rozmowy samosy jakoś szybko zniknęły
    >>> del ordered_dishes[1]
    >>> print(ordered_dishes)
    ['Bakłażan w cieście']

    #  Czas na zupę, może coś na ostro?
    >>> ordered_dishes.insert(0, 'Pikantna Zupa Masala')
    >>> print(ordered_dishes)
    ['Pikantna Zupa Masala', 'Bakłażan w cieście']

    # ... o nie to zbyt palące, może zamiast tego jednak coś bezpieczniejszego?
    >>> ordered_dishes[0] = 'Krem z krewetkami'
    >>> print(ordered_dishes)
    ['Krem z krewetkami', 'Bakłażan w cieście']

    # Bakłażan już zimny raczej nikt go nie dokończy, idzie na straty
    >>> ordered_dishes.remove('Bakłażan w cieście')
    >>> print(ordered_dishes)
    ['Krem z krewetkami']

    # No i wreszcie wołowinka, od razu w dwóch odsłonach
    >>> ordered_dishes.extend(['Wołowina Kolhapuri', 'Wołowina Kadai'])
    >>> print(ordered_dishes)
    ['Krem z krewetkami', 'Wołowina Kolhapuri', 'Wołowina Kadai']

    # Było pyszne, trzeba tu wrócić.
    >>> ordered_dishes.clear()
    >>> print(ordered_dishes)
    []

Nowy element możemy dodać na koniec listy za pomocą metody ``apped``, lub wstawić go przed element o podanej pozycji za
pomocą metody ``insert``. Metoda ``insert`` przyjmuje najpierw pozycję elementu istniejącego, a następnie element
wstawiany. Jeżeli chcemy dodać na koniec listy kilka elementów jednocześnie to do tego używamy metody ``extend``.

Aby zmienić element, znajdujący się na danej pozycji na nowy, po prostu przypisujemy nową wartość do elementu listy
o konkretnym indeksie.

Jeżeli znamy pozycję elementu, możemy usunąć go z listy używając słowa kluczowego ``del``. Metoda ``remove`` usuwa
natomiast z listy elementy o podanej wartości. Jeżeli chcemy wyczyścić wszystkie elementy listy możemy użyć metody
``clear``.

.. TODO: cloning, explain shallow clone, sorting and reversing

set
===

zagnieżdżone sekwencje
======================

indeksowanie, slicing, rozpakowywanie
=====================================

B06 - Python: słowniki
**********************

dict
====

zip, enumerate
==============

zagnieżdżone słowniki
=====================

Przykład użycia różnych typów danych
====================================

.. code-block:: python

   # Typy proste
   numeric_integer_variable = 123
   numeric_float_variable = 123.456
   string_variable = 'Some sample string'
   boolean_variable = True

   # Typu złożone
   set_variable = {1,2,3,'a'}
   list_variable = ['Some', 'sample', 'list', 1, 2, 3]
   tuple_variable = (111, 'This', 'is', 'a', 'tuple', False)
   dictionary_variable = {'key1':'value1', 'key2':1234, 3:'value3'}

Zauważyć tu należy 2 rzeczy:

* Linie zaczynające się od znaku ```#``` to komentarze. Python ich nie wykonuje, mają znaczenie czysto informacyjne.
  Dobrym zwyczajem jest zostawianie komentarzy w miejscach gdzie kod jest zawiły, aby programista czytający ten kod
  kiedyś mógł łatwiej zrozumieć nasze intencje.
* Ciekawą cechę wynikającą z faktu, że Python jest dynamicznie typowany: typ zmiennej może się zmieniać w trakcie
  działania programu. Zobacz przykład:

.. code-block:: python

   >>> var_a = 1
   >>> type(var_a)
   <class 'int'>
   >>> var_a = 1.2
   >>> type(var_a)
   <class 'float'>
   >>> var_a = 'test'
   >>> type(var_a)
   <class 'str'>

.. note::
   | Ćwiczenie 3
   | Zadanie polega na zaproponowaniu użycia konkretnego typu danych dla zmiennych które chcemy przechować. Zastanów się
     jakiego typu danych użyjesz w każdym z przypadków. Przypisz przykładowe wartości do zmiennych w pliku .py
     i zwróć je na ekran.
   | Hint: Typy można sprawdzić poleceniem type(zmienna).

   .. code-block:: python

      Imię
      Nazwisko
      Numer dowodu osobistego
      Wiek
      Wzrost (w metrach)
      Numery kart kredytowych

Rzutowanie typów
================

Służy do zmiany jednego typu w drugi.
Typy numeryczne rzutujemy bez problemu na dowolny inny typ:

.. code-block:: python

   >>> integer_variable = 123
   >>> float(integer_variable)
   123.0
   >>> str(integer_variable)
   '123'
   >>> bool(integer_variable)
   True

Typy znakowe też, ale tylko gdy ma to sens (nie da się np. zamienić ciągu liter na liczbę).

.. code-block::

   >>> string_value = '123'
   >>> int(string_value)
   123
   >>> float(string_value)
   123.0
   >>> bool(string_value)
   True

   # string będzie dało się rzutować na boolean
   # pusty ciąg znaków albo None zwróci False
   # wszystko inne zwróci True
   >>> another_String_value = 'abc'
   >>> bool(another_String_value)
   True
   # nie wszystkie stringi da się rzutować na typy numeryczne
   >>> int(another_String_value)
   Traceback (most recent call last):
   File "<input>", line 1, in <module>
   ValueError: invalid literal for int() with base 10: 'abc'

.. note::
   | Ćwiczenie 4a
   | Wklej poniższy fragment kodu do edytora, uruchom i przetestuj działanie.

   .. code-block:: python

      liczba1 = input('Podaj liczbę 1 :')
      liczba2 = input('Podaj liczbę 2 :')
      print(liczba1 + liczba2)

   | Czy działa dobrze? Podyskutujmy o tym co się tam zadziało.
   |
   | Ćwiczenie 4b
   | Pobierz od użytkownika 2 liczby całkowite i zwróc na ekran ich sumę, różnicę, iloczyn i iloraz. Pamiętaj, że
     wynikiem działania komendy input() jest typ string.
   | Hint: Konieczne będzie rzutowanie typu pobranych danych!

B07 - Python: instrukcje warunkowe
**********************************

operatory kolejność
===================

if, else, elif
==============

in, is, not, and, or
====================

B08 - Python: pętle
*******************

while
=====

for
===

iterowanie
==========
