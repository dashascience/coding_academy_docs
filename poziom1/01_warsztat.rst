.. Coding Academy documentation master file, created by
   sphinx-quickstart on Sun Apr  5 22:55:20 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Warsztat 1
##########

Wszystkie nasze warsztaty będą składały się z części do samodzielnego wykonania i takiej nad którą popracujemy w czasie
zajęć. Do samodzielnego wykonania przed pierwszymi zajęciami są sekcje :ref:`sprzet` i :ref:`jakzbudowac`. Przyjdź na
zajęcia z przygotowanym środowiskiem, aby nie tracić czasu na instalację oprogramowania w czasie zajęć!

.. _sprzet:

Sprzęt - czego potrzebuję?
**************************
Potrzebujesz komputera. Nie musi to być najnowszy model za pięciocyfrową kwotę, natomiast powinien być wystarczająco
wydajny, ale nauka programowania nie powodowała frustracji natury sprzętowej.

Komputer, ale jaki?
===================
Dla naszych potrzeb chyba najlepiej sprawdzi się laptop. Większość maszyn wyprodukowanych po 2012 roku i spełniające
poniższe wymagania powinna być OK.

- **procesor intel i5 lub i7**
- **pamięć operacyjna (RAM)** min. 8GB
- **dysk SSD** - nie jest niezbędny, ale mając go, wszystko będzie działało szybciej
- **Windows 10** - na takim systemie operacyjnym będziemy wykonywać ćwiczenia. Windows 7 lub 8 też da radę.
  Windows XP sie nie nadaje, bo nie zainstalujemy na nim najnowszego pythona!

Sprzęt nie musi być nowy. Jeśli nie masz komputera i zamierzasz go kupić, to dobrym pomysłem może okazać się poszukanie
sprzętu używanego.

.. _jakzbudowac:

Jak zbudować sobie środowisko?
******************************
Czym jest środowisko? Środowisko, to zainstalowany zestaw oprogramowania, który pozwoli nam pisać i uruchamiać kod.
Aby uczyć się programowania w języku Python potrzebujemy 4 rzeczy. Wszystkie są dostępne za darmo:

- Python - zestaw narzędzi niezbędnych do uruchamiania programów napisanych w Pythonie `https://www.python.org <https://www.python.org/ftp/python/3.8.2/python-3.8.2.exe>`_
- PyCharm community - zintegrowane środowisko programistyczne `https://www.jetbrains.com/pycharm
  <https://download.jetbrains.com/python/pycharm-community-2020.1.exe>`_
- git - oprogramowanie do kontroli wersji `https://git-scm.com/download/win
  <https://github.com/git-for-windows/git/releases/download/v2.26.0.windows.1/Git-2.26.0-64-bit.exe>`_
- sourceTree - przyjazny interfejs użytkownika dla gita `https://sourcetreeapp.com
  <https://product-downloads.atlassian.com/software/sourcetree/windows/ga/SourceTreeSetup-3.3.8.exe>`_

.. note:: Ściągnij wersje instalacyjne oprogramowania korzystając z powyższych linków.
   W dalszej części artykułu pokażę na co zwrócić uwagę przy instalacji.

Po pobraniu powyższych powinniśmy mieć następujące pliki:

.. image:: images/files.png

No to instalujemy
=================

Python
------
- Uruchamiamy plik **python-3.8.2.exe**
- Na pierwszym ekranie zaznaczamy "Add Python 3.8 to PATH" i wybieramy **Install now**.

   .. image:: images/python1.png
      :width: 400

   .. note::
      Dobrze jest zapamiętac ścieżkę, w której Python się nam instaluje - przyda się w kolejnych krokach.

      Domyślna ścieżka: **C:\\Users\\<nazwa_usera>\\AppData\\Local\\Programs\\Python\\Python38-32**

- Po udanej instalacji klikamy **Close**.

   .. image:: images/python2.png
      :width: 400

- Weryfikacja: po poprawnej instalacji wykonanie w Wierszu polecenia:

  ``python --version``

  powinno zwrócić wersję Pythona.

   .. image:: images/python3.png
      :width: 400


PyCharm
-------
- Uruchamiamy plik **pycharm-community-2020.1.exe**

  .. image:: images/pycharm1.png
     :width: 400

- Jedyna rzecz, którą zmieniamy podczes instalacji, to zaznaczenie opcji **Create Desktop Shortcut -> 64-bit launcher**

  .. image:: images/pycharm2.png
     :width: 400

- Po udanej instalacji klikamy **Finish**

  .. image:: images/pycharm3.png
     :width: 400

- Na desktopie pojawi się ikona.

  .. image:: images/pycharm4.png

- Uruchamiamy PyCharm. Wybieramy **Do not import settings**

  .. image:: images/pycharm5.png
     :width: 400

- Wybieramy motyw kolorystyczny i ** Next - Featured plugins**

  .. image:: images/pycharm6.png
     :width: 400

- Tu nic nie zmieniamy i klikamy **Start using PyCharm**.

  .. image:: images/pycharm7.png
     :width: 400

- Po uruchomieniu PyCharm powinniśmy dostać takie okienko:

  .. image:: images/pycharm8.png
     :width: 400

git
---
- Uruchamiamy instalator **Git-2.26.0-64-bit.exe**
- Instalujemy z domyślnymi opcjami. Niczego nie trzeba zmieniać.
- Weryfikacja:

  * po poprawnej instalacji wykonanie w Wierszu polecenia:

    ``git --version``

    powinno zwrócić wersję gita.

    .. image:: images/git1.png
       :width: 400

  * menu kontekstowe powinno zostać rozszerzone o nowe opcje:

     .. image:: images/git2.png


SourceTree
----------
- Uruchamiamy instalator **SourceTreeSetup-3.3.8.exe**
- Jeśli nie masz konta na bitbucket.org, to teraz należy je założyć i zalogować się na to konto po wybraniu opcji
  **Bitbucket**

  .. image:: images/sourcetree1.png
     :width: 400

- Pozostałe parametry instalacji pozostawiamy bez zmian.
- Sourcetree instaluje się na ścieżce ``C:\Users\<username>\AppData\Local\SourceTree``
- Należy zrobić sobie skrót do pliku SourceTree.exe na desktopie.

O co chodzi z programowaniem?
*****************************

Podstawy GITa.
**************



