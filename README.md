# Informacje dotyczące projektu 

"Testowa" to wtyczka QGIS, która umożliwia użytkownikom wykonywanie obliczeń związanych z wysokościami i polami powierzchni na podstawie
wybranych cech w warstwie. Wtyczka udostępnia okno dialogowe z różnymi funkcjami.

***Wtyczka QGIS - wymagania do jego uruchomienia***
<br> Przedstawiony program, został napisany dla programu QGIS-a wersja 3.28.5 - Firenze, za pomocą języka Python wersja 3.9.5 oraz QTDesigner wersja 5.15.3. 
Ponadto, został napisany na systemie operacyjnym Windows 10, 64-bitowym.
Jeden z komputerów jest wyposażony w kartę graficzną NVIDIA GEFORCE GTX 1660Ti, procesor AMD Ryzen 7 4800H with Radeon Graphics oraz
pamięć RAM o wielkości 16 GB.
<br> Drugi komputer wykorzystany do napisania projektu posiada system operacyjny Windows 10, 64-bitowy, pamięć RAM 16 GB,
procesor Intel CORE i7 oraz kartę graficzną NVIDIA GEFORCE GTX 1660Ti.

<br>Aby skorzystać z jednego z programów należy pobrać wtyczkę, uruchomić wyżej wymieniony program QGIS na komputerze użytkownika, na pasku poleceń 
skorzystać z opcji "Wtyczki" następnie "Zarządzanie wtyczkami" i pobrać wtyczkę o nazwie "testowa". Należy także wczytać warstwę z danymi współrzędnymi 
płaskimi i wysokościowymi. W tym celu należy wejść na stronę https://www.geoportal.gov.pl/uslugi/usluga-pobierania-wfs, a następnie skopiować link do
podstawowej osnowy geodezyjnej wysokościowej i wczytać ją do QGIS (w lewym oknie zadań wybrać usługę WFS i za pomocą nowego połączenia wgrać punkty). 
Ważnym elementem jest tabela atrybutów, która mówi użytkownikowi jakie elementy zawierają dane. W tym programie zostały wykorzystane kolumny 'h_plevrf2007nh'
do obliczenia wysokości oraz 'x1992', 'y1992' do obliczenia pola powierzchni. W tabeli atrybutów wymagany jest typ double NULL. 
Warto zaznaczyć, iż dane importowane do pliku QGIS muszą zawierać współrzędne płaskie (x,y) oraz wysokościowe (h) w układzie 1992. Program nie obsługuje 
innych układów. To, czy dane spełniają powyższy warunek można sprawdzić uruchamiając tabelę atrybutów.

***Funkcjonalność i posługiwanie się wtyczką*** 
***Liczenie przewyższenia***
<br>Aby skorzystać z funkcji obliczającej różnice wysokosci pomiędzy punktami, należy wybrać narzędzie do zaznaczania obiektów prostokątem 
lub kliknięciem; zaznaczyć interesujące punkty oraz uruchomić wtyczkę (w tym celu wybrać z paska poleceń "Wtyczki", następnie "testowa"). 
Pokaże się wyskakujące okno, na którym zaprezentowana jest warstwa, a poniżej należy kliknąć przycisk "Oblicz różnice wysokości". 
Obliczone różnice wyświetlą się na poniższej konsoli wraz z odpowiednią jednostką - [m]. Warto zaznaczyć, iż jeśli użytkownik zaznaczy
więcej niż 2 elementy, program zwróci komunikat o błędzie, gdyż różnice obliczane są dla dwóch punktów. To samo tyczy się zaznaczenia
zbyt małej liczby elementów. Dodano także zabezpieczenie obejmujące wybór warstwy. Jeżeli takowa nie została wybrana, wyświetli odpowiedni komunikat
na konsoli programu.
<br>
***Liczenie pola powierzchni***
<br>Aby skorzystać z funkcji obliczającej pola powierzchni pomiędzy punktami, należy wybrać narzędzie do zaznaczania obiektów prostokątem 
lub kliknięciem; zaznaczyć interesujące punkty oraz uruchomić wtyczkę (w tym celu wybrać z paska poleceń "Wtyczki", następnie "testowa"). 
Pokaże się wyskakujące okno, na którym zaprezentowana jest warstwa, a poniżej należy kliknąć przycisk "Oblicz pole powierzchni". 
Obliczona wartość wyświetli się na poniższej konsoli wraz z odpowiednią jednostką - [*m<sup>2</sup>*]. Warto zaznaczyć, iż jeśli użytkownik zaznaczy
zbyt małą lub zbyt dużą liczbę elementów, program zwróci komunikat o tym fakcie. Dlatego należy wybrać dokładnie 3 punkty. Program liczy pole powierzchni 
metodą Gaussa, czyli metodą opierającą się na różnicach współrzędnych.Dodano także zabezpieczenie obejmujące wybór warstwy. Jeżeli takowa nie została 
wybrana, wyświetli odpowiedni komunikat na konsoli programu.
<br>
<br> ***Program został przetestowany i nie prezentuje innych nietypowych zachowań, o ile jest użytkowany zgodnie z powyższą instrukcją.***