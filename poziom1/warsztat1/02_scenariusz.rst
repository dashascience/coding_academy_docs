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


Operacje arytmetyczne na liczbach całkowitych (integer)
=======================================================

    * operatory (+ - * /)
    * operatory ** i %
    * wyrażenia
    * wartości
    * kolejność operatorów
    * składnia, co to jest SyntaxError

.. note:: Ćwiczenie 1
   Za pomocą REPL wykonaj operacje arytmetyczne:

   .. code-block:: python

      128*256
      2 do potęgi 16
      reszta z dzielenia 100 przez 8

   Wykonaj te same operacje w pliku main.py. Zwróć wynik na ekran używając funkcji print()


Zmienne
=======

* Zmienne służą do przechowywania wartości (np wyniku obliczeń, ciągu znaków lub obiektu)
* zmienna ma nazwę i typ, natomiast typu nie trzeba jawnie deklarować - python domyśli się jakiego typu powinna być
  zmienna na podstawie wyrażenia z prawej strony instrukcji przypisania (=)
* Przypisywanie wartości do zmiennej (mechanizm i pokazanie co dzieje się w pamięci operacyjnej
* Kolejne typy zmiennych (poprzednio były liczby całkowite): zmiennoprzecinkowe
* operator / vs //

* Pobieranie danych od użytkownika - funkcja input()
* Zwracanie danych na ekran - funkcja print()
* Ćwiczenia do samodzielnego wykonania