Scenariusz warsztatu 1 - poziom początkujący
############################################

O co chodzi z programowaniem
****************************

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


Operacje arytmetyczne
=====================

    * operatory (+ - * /)
    * operatory ** i %
    * wyrażenia
    * wartości
    * kolejność operatorów
    * składnia, co to jest SyntaxError

.. note::
   | Ćwiczenie 1
   | Za pomocą REPL wykonaj operacje arytmetyczne:

   .. code-block:: python

      128*256
      100/33
      2 do potęgi 16
      reszta z dzielenia 100 przez 8

   | Ćwiczenie 2
   | Wykonaj te same operacje w pliku main.py. Zwróć wyniki na ekran używając funkcji print()


Zmienne
=======

* Zmienne służą do przechowywania wartości (np wyniku obliczeń, ciągu znaków lub obiektu)
* zmienna ma nazwę i typ, natomiast typu nie trzeba jawnie deklarować - python jest dynamicznie typowany, więc domyśli
  się jakiego typu powinna być
  zmienna na podstawie wyrażenia z prawej strony instrukcji przypisania (=)
* Przypisywanie wartości do zmiennej (mechanizm i pokazanie co dzieje się w pamięci operacyjnej)

.. code-block:: python

   nazwa_zmiennej = <wartosc / wyrazenie>

* Typy danych (pokaż podział i opowiedz)

   .. figure:: images/python_data_types.jpg
      :width: 400

      Typy danych w języku Python

Przykład użycia różnych typów
=============================

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

.. note::
   | Ćwiczenie 3
   | Zadanie polega na zaproponowaniu użycia konkretnego typu zmiennej dla danych które chcemy przechować. Zastanów się
     jakiego typu zmiennych użyjesz w każdym z przypadków. Przypisz przykładowe wartości do zmiennych w pliku .py
     i zwróć je na ekran.

   .. code-block:: python

      Imię
      Nazwisko
      Numer dowodu osobistego
      Wiek
      Wzrost (w metrach)
      Numery kart kredytowych

Operacje na danych typu string (znakowych)
==========================================

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

Rzutowanie typów
================

Służy do zmiany jednego typu w drugi.