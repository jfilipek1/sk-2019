# Zadanie 2

## Projekt sieci lokalnej dla jednostki dydaktycznej uniwersytetu

![budynek](budynek.svg)

### Cel Projektu
  Zaprojektowanie i weryfikacja działania sieci w środowisku testowym. 
  Rozwiązanie zapewnia dostęp do internetu dla wszystkich urządzeńw infrastrukturze.
  
### Założenia projektu

* Sieć zlokalizowana jest w budynku 3 kondygnacyjnym
* Na kążdej z kondygnacji znajdują się laboratoria komputerowe kolejno:
  * poziom 0 
    * 009, 013, 014
  * poziom 1
    * 115, 116, 117, 122
  * poziom 2
    * 201, 202, 203
* Każde z laboratoriów wyposażone jest w 35 stanowisk dla uczestników kursów
* Jednostka planuje otworzenie kolejnych laboratoriów 017 oraz 204
* Każda kondygnacja wyposażona jest w izolowaną sieć Wi-Fi, udostępniajacą sieć internet podłączonym gościom
  * Sieć Wi-Fi nie pozwala na bezposrednią komunikację z urządzeniami zlokalizowanymi w pozostałej części sieci,
    tj: laboratoria, serwery jednostki
  * Prognozowana maksymalna liczba jednoczesnych urządzeń podłączonych do sieci to ``800``
* Jednostka posiada przyłącze internetowe oraz dysponuje pulą adresów ``188.156.220.160/27``
* Jednostka posiada serwery udostępniajace zasoby do celów dydaktycznych i promocyjnych
  * serwery zlokalizowane są w osobnym pomieszczeniu
  * udostępniają zasoby w sieci publicznej z wykorzystaniem sieci ``188.156.220.160/27``
  * Jeden serwer pełni rolę bramy dla urządzań w sieci lokalnej ``LAN``

### Wstępne założenia

* Każde laboratorium posiada oddzielną podsieć pozwalającą efektywnie zidentyfikować urządzania
  * kondygnacja oraz sala
* Dla uniknięcia zbyt słabego zasięgu sieć WiFi zostanie wyposażona w 4 urządzenia nadawcze na każdej kondygnacji
 

#### zadanie - wymaganai

* Dokonaj podziału i projektu sieci w formie dokumentu w formacie ``MARKDOW`` zawierającego specyfikację tekstową oraz obrazkową
  projektowanej sieci
* Przygotuj prototyp rozwiązania z wykorzystaniem oprogramowania ``VirtualBox`` lub podobnego.
* W specyfikacji uwzględnij wielkości sieci oraz ich adresy
* W specyfikacji uwzględnij konfigurację tablicy routingu
* Dokumentację graficzną stworzonej architektury przygotuj w programie ``DIA`` lub podobnym


--------------
## Rozwiązanie

* sale - ``188.156.220.160/28`` ``10.0.0.0/16``
* WI-FI - ``188.156.220.176/28`` ``10.10.0.0/22``

### Poziom 0
  4 * 35 = 140 komputerów
  * 009
    *  ``10.0.9.0/26``
  * 013
    *  ``10.0.13.0/26``
  * 014
    *  ``10.0.14.0/26``
  * 017
    *  ``10.0.17.0/26``
    
### Poziom 1
  4 * 35 = 140 komputerów
  * 115
    * ``10.0.115.0/26``
  * 116
    * ``10.0.116.0/26``
  * 117
    * ``10.0.117.0/26``
  * 122
    * ``10.0.122.0/26``
    
### Poziom 2
  4 * 35 = 140 komputerów
  * 201
    * ``10.0.201.0/26``
  * 202
    * ``10.0.202.0/26``
  * 203
    * ``10.0.203.0/26``
  * 204
    * ``10.0.204.0/26``
  
3 * 140 = 420 komputerów w sumie  

![diagram](diagram.jpg)
