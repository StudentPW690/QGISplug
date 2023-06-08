# Informacje dotyczące projektu 

***Wtyczka QGIS - wymagania do jego uruchomienia***
<br> Przedstawiony program, został napisany dla programu QGIS-a wersja 3.28.5 - Firenze, za pomocą języka Python wersja 3.9.5. 
Został on napisany na systemie operacyjnym Windows 10, 64-bitowym.
Jeden z komputerów jest wyposażony w kartę graficzną NVIDIA GEFORCE GTX 1660Ti, procesor AMD Ryzen 7 4800H with Radeon Graphics oraz
pamięć RAM o wielkości 16 GB.
<br> Drugi komputer wykorzystany do napisania projektu posiada system operacyjny Windows 10, 64-bitowy, pamięć RAM 16 GB,
procesor Intel CORE i7 oraz kartę graficzną NVIDIA GEFORCE GTX 1660Ti.

<br>Aby skorzystać z jednego z programów należy uruchomić wyżej wymieniony program QGIS na komputerze użytkownika, na pasku poleceń 
skorzystać z opcji "Wtyczki" następnie "Zarządzanie wtyczkami" i .......

***Funkcjonalność i posługiwanie się programami*** 
<br>Aby skorzystać z funkcji obliczającej różnice wysokosci pomiędzy punktami, należy wybrać narzędzie do zaznaczania obiektów prostokątem 
lub kliknięciem; zaznaczyć interesujące punkty oraz uruchomić wtyczkę (w tym celu wybrać z paska poleceń "Wtyczki", następnie "testowa"). 
Pokaże się wyskakujące okno, na którym zaprezentowana jest warstwa, a poniżej należy kliknąć przycisk "Oblicz różnice wysokości". 
Obliczone różnice wyświetlą się na poniższej konsoli wraz z odpowiednią jednostką - [m]. Warto zaznaczyć, iż jeśli użytkownik zaznaczy
więcej niż 2 elementy, program zwróci komunikat o błędzie, gdyż różnice obliczane są dla dwóch punktów. To samo tyczy się zaznaczenia
zbyt małej liczby elementów. 
<br>
<br>Aby skorzystać z funkcji obliczającej pola powierzchni pomiędzy punktami, należy wybrać narzędzie do zaznaczania obiektów prostokątem 
lub kliknięciem; zaznaczyć interesujące punkty oraz uruchomić wtyczkę (w tym celu wybrać z paska poleceń "Wtyczki", następnie "testowa"). 
Pokaże się wyskakujące okno, na którym zaprezentowana jest warstwa, a poniżej należy kliknąć przycisk "Oblicz pole powierzchni". 
Obliczona wartość wyświetli się na poniższej konsoli wraz z odpowiednią jednostką - [*m<sup>2</sup>*]. Warto zaznaczyć, iż jeśli użytkownik zaznaczy
zbyt małą liczbę elementów, program zwróci komunikat o tym fakcie. Dlatego należy wybrać więcej niż 2 punkty. Program liczy pole powierzchni 
metodą Gaussa, czy metodą opierającą się na różnicach współrzędnych.
<br>
<br> ***Program został przetestowany i nie prezentuje innych nietypowych zachowań, o ile jest użytkowany zgodnie z powyższą instrukcją.***