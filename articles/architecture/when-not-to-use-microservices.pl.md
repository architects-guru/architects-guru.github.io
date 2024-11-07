---
layout: default
---

# Kiedy nie warto budować architektury w oparciu o mikroserwisy?

W ostatnich latach *mikroserwisy* zyskały dużą popularność dzięki wielu zaletom, a do najważniejszych należą:
- skalowalność - selektywna zmiana zasobów, np. liczby instancji konkretnych serwisów i ich zależności (np. baz danych)
- optymalizacja kosztów - szczególnie w usługach typu cloud
- elastyczność - wdrażanie poszczególnych składowych systemu (serwisów), rozproszony development
- niższa podatność na awarie, łatwiejsza redundancja

*Wszystko to jednak ma swój koszt i nierzadko koszt wytworzenia nowego systemu może się okazać początkowo bardzo duży.* 

Pracując przez ostatnie lata przy wielu nowych projektach, zauważyłem, że mimo tak wielu zalet nie zawsze wybór tej architektury to dobre rozwiązanie. Założmy, że *mamy do wytworzenia nowy projekt*, całkiem od podstaw, np. typowy "proof of concept", gdzie chcemy upewnić się czy jakaś idea ma sens. Nie znamy jeszcze dokładnie domeny biznesowej, funkcjonalności niejako będą się wyłaniać z czasem.

*Jeśli nasz system od początku nie musi być super skalowany, a zazwyczaj tak nie będzie, może to być pierwszą wskazówką do nie użycia mikroserwisów.*

Czy w takim przypadku już na tym etapie szukanie odpowiedzialności i wydzielanie poszczególnych serwisów, przy tak potencjalnie dużej zmienności wymagań ma sens? Według mnie - nie ma. Dużo łatwiej będzie początkową implemetację zrobić jako klasyczny *monolit*.

Zdecydowanie się na typ etapie na architekturę opartą o mikroserwisy mogłoby spowodować spory narzut czasowy, a w rezultacie brak dostarczania wartości biznesowej, z powodu złożoności tej architektury na wielu płaszczyznach. Będzie to widoczne zwłaszcza w mniejszych zespołach, gdzie zamiast skupić się na dostarczeniu funkcjonalności biznesowej, wypalamy czas z powodu złożoności architektury. 

*Warto się zatem zastanowić, czy mikroserowisy nie wprowadzą niepotrzebnej złożności, zamiast oczekiwanych korzyści.*