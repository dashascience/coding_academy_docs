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
Wartości logiczne to stałe przyporządkowujące prawdę albo fałsz do danego wyrażenia logicznego.
W Pythonie występują jako **True** - gdy wyrażenie jest prawdziwe oraz **False** - gdy wyrażenie jest fałszywe.
W logice matematycznej zazwyczaj prezentowane są przez liczby 1 oraz 0.
Zmienne, które mogą przechowywać tego typu wartości są typu **bool**. Nazwa ta wywodzi się od nazwiska angielskiego
matematyka George'a Boola, który zajmował się logiką.

Dla przypomnienia - wyrażenia logiczne budujemy korzystając z poznanych wcześniej operatorów porównania:
    * **a<b** - a mniejsze od b
    * **a<=b** - a mniejsze lub równe od b
    * **a>b** - a większe od b
    * **a>=b** - a większe lub równe b
    * **a==b** a równe b
    * **a!=b** - a różne od b
..
oraz operatorów logicznych:
    * **a and b** - koniunkcja, warunek jest prawdziwy jeśli wyrażenia a oraz b są prawdziwe
    * **a or b** - alternatywa, warunek jest prawdziwy jeśli conajmniej jedno wyrażenie a lub b jest prawdziwe
    * **a in b** - warunek prawdziwy jeżeli a zawiera się w b (np 'abc' in 'abcd')
    * **a is b** - warunek sprawdza, czy zmienne wskazują ten sam obszar w pamięci komputera
    * **not a** - warunek oznacza zaprzeczenie wyrażenia a
..
Warto również przypomnieć że **not a and not b** możemy zastąpić wyrażeniem ** not(a or b)

Za pomocą metody ```bool()``` możemy sprawdzić wartość logiczną danego wyrażenia logicznego albo obiektu.
Oznacza to, że bool(x) zwarca wartość True albo False.
W poniższym przykładzie sprawdzimy, czy liczba 673 jest liczbą parzystą oraz czy dwa podane ciągi znaków
się od siebie różnią.

.. code-block:: python

    # x % y -> działanie modulo, zwraca resztę z dzielenia liczby x przez liczbę y
    # gdy reszta z dzielenia jest równa zero mamy do czynienia z liczbą podzielną przez y
    print(bool(673 % 2 == 0)) #False
    print(bool('Ala ma kota' != 'kot ma Alę')) #True
..

Typ zmiennych możemy sprawdzić za pomocą metody ```type()```. W przypadku zmiennych logicznych **False** oraz **True**
jako wynik zawsze otrzymamy typ **bool**.

.. code-block:: python

    print(type(False)) #bool
    print(type(3>=1)) #bool
..

Warto również pamiętać, że każdy z obiektów ma w Pythonie przyporządkowaną do siebie wartość logiczną
(co nie oznacza, że sam musi być typu bool)
    * None, False, 0, puste kolekcje ("", (), [], {}) ma wartość **False**
    * Wszystkie inne obiekty wartość **True**
..
.. note::
   | Ćwiczenie
   | Za pomocą metod: bool() oraz type() sprawdź jaką wartość logiczną oraz jaki typ/ klasę przezentują poniższe przykłady:
   | 1) x = "0"
   | 2) x = [()]
   | 3) x = False
   | 3) x = None
   | 4) x = {None}
   | print("wartość logczina: ", bool(x),"\n", "typ: ", type(x))
..


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

list
====

tuple
=====

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
