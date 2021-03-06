Dane projektu Szkołomat
-----------------------

Otwarte dane związane ze stroną [Szkołomat - automat do wyszukiwania szkół](http://szkolomat.pl/) fundacji [Centrum Cyfrowe Projekt:Polska](http://centrumcyfrowe.pl/).


## Informacje


Informacje pochodzą z następujących źródeł:

* [Centralna Komisja Egzaminacyjna (CKE)](http://www.cke.edu.pl/)
* Okręgowa Komisje Egzaminacyjne (OKE)
* [Instytut Badań Edukacyjnych (IBE)](http://www.ibe.edu.pl/)
* [System Informacji Oświatowej (SIO)](http://cie.men.gov.pl/index.php/sio-wykaz-szkol-i-placowek.html)
* [The Google Geocoding API](https://developers.google.com/maps/documentation/geocoding/)

Wyniki egzaminów w plikach `sp_spr_2002do2013.csv`, `gimn_egz_2002do2013.csv` oraz `gimn_wskazniki_2013.csv` są wynikami znormalizowanymi, tj. przeskalowanymi tak,by:

* średni wynik w danym roku wynosił 100,
* odchylenie standardowe wyników w danym roku wynosiło 15,
* rozkład wyników w danym roku był rozkładem normalnym.

W wypadku plików `sp_spr_2002do2013.csv` oraz `gimn_egz_2002do2013.csv` użytko normalizacji ekwikwantylowej, natomiast w wypadku pliku `gimn_wskazniki_2013.csv` zastosowano modelowanie IRT.

Dalsze informacje, oraz motywacja takiego podejścia, znajdują się w prezentacji:

* Tomasz Żółtak, [Skalowanie wyników egzaminacyjnych](http://ewd.edu.pl/szkoly-ewd/jesienna-2013/skalowanie.pdf), Jesienna Szkoła EWD, Warszawa 17.10.2013

Dalsze informacje związane z [Edukacyjną Wartością Dodaną](http://ewd.edu.pl/) (plik `gimn_wskazniki_2013.csv`) znajdują się w raporcie:

* Tomasz Żółtak, [Statystyczne modelowanie wskaźników edukacyjnej wartości dodanej - podsumowanie polskich doświadczeń](http://www.ibe.edu.pl/images/publikacje/ibe-raport-modelowanie-wskaznikow-ewd.pdf), Analizy IBE/02/2013

W przypadku wykorzystania danych z pliku `gimn_wskazniki_2013.csv` prosimy o cytowanie w/w artykułu.


## Licencja

Dane zawarte w pliku `gimn_wskazniki_2013.csv` są udostępnione na wolnej licencji [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/), przez [Instytut Badań Edukacyjnych](http://www.ibe.edu.pl/).

Pozostałe dane te nie są przejawem twórczej działalności o indywidualnym charakterze zatem, zgodnie z polskim prawem, nie podlegają prawu autorskiemu.


## Opis danych

* `szkoly_ibe_2013.csv` - dane szkół z bazy IBE
	* `id_szkoly` - identyfikator z bazy IBE
	* `nazwa`
	* `adres` - ulica i nr domu
	* `miejscowosc` - miejscowość, pole często puste, wtedy należy korzystać z pola `poczta`
	* `kod_pocztowy`
	* `poczta` - miejscowość związana z pocztą
	* `typ_szkoly`
		* `SP` - szkoła podstawowa 
		* `gimn.` -  gimnazjum
	* `publiczna` - `True` lub `False`, dana tylko dla gimnazjów
	* `dla_doroslych` - `True` lub `False`, dana tylko dla gimnazjów
	* `specjalna` - `True` lub `False`, dana tylko dla gimnazjów
	* `przyszpitalna` - `True` lub `False`, dana tylko dla gimnazjów
	* `wojewodztwo`
	* `powiat`
	* `gmina`
	* `id_wojewodztwa`
	* `id_powiatu`
	* `id_gminy`
* `szkoly_ibe_sio_dowiazanie.csv` - dane szkół z [SIO z roku 2013](http://cie.men.gov.pl/index.php/sio-wykaz-szkol-i-placowek/27-wykaz-wg-typow.html) z dołączonym `id_szkoly` z bazy szkół IBE
	* `id_szkoly`
	* `lp_sio` - identyfikator (pole `Lp.` w wykazie szkół SIO z roku 2013)
	* `odl_dop` - czym niższa tym lepsze dopasowanie; gdy powyżej 2 dopasowanie może być obardzone pewnym ryzykiem
	* `telefon`
	* `fax`
	* `www`
	* `oddzialy`
	* `liczba_uczniow`
	* `specjalna` - `True` lub `False`
	* `publiczna` - `True` lub `False`
* `szkoly_geolokalizacja.csv` - wyszukania za [Google Geocoding API](https://developers.google.com/maps/documentation/geocoding/)
	* `id_szkoly`
	* `lat` - szerokość geograficzna
	* `lng` - długość geograficzna
	* `geolocalizer_count` - liczba wyszukań (jeśli więcej niż 1 - lokalizacja niepewna) 
	* `location_type` - typ lokacji (`ROOFTOP` znaczy, że dokładnie ten budynek)
* `sp_spr_2002do2013.csv` - wyniki egzaminacyjne szkół podstawowych
	* `id_szkoly`
	* `wyn_norm_sr` - średni znormalizowany wynik
	* `wyn_norm_std` - odchylenie standardowe znormalizowanych wyników 
	* `probka` - liczba uczniów uwzględnionych w próbce
	* `rok`
	* `czesc` - puste pole
* `sp_wskazniki_2013.csv` - wskaźniki dla szkół podstawowych
	* `id_szkoly`
	* `gwiazdki_pow` - liczba 1-5 w zależności od tego, jak średni wynik plasuje się w powiecie
* `gimn_egz_2002do2013.csv` - wyniki egzaminacyjne gimnazjów
	* `id_szkoly`
	* `egz_norm_sr` - średnia znormalizowanych wyników
	* `egz_norm_std` - odchylenie standardowe znormalizowanych wyników 
	* `probka` - liczba uczniów uwzględnionych w próbce
	* `rok`
	* `czesc` - część egzaminu gimnazjalnego
		* `gh` - humanistyczna (do 2011 r.)
		* `gm` - matematyczno-przyrodnicza (do 2011 r.)
		* `gh_h` - historia i WOS (od 2012 r.)
		* `gh_p` - j. polski (od 2012 r.)
		* `gm_p` - przyrodnicza (od 2012 r.)
		* `gm_m` - matematyczna (od 2012 r.)
* `gimn_wskazniki_2013.csv` - dane szkół zgodnie z [Statystyczne modelowanie wskaźników edukacyjnej wartości dodanej - podsumowanie polskich doświadczeń](http://www.ibe.edu.pl/images/publikacje/ibe-raport-modelowanie-wskaznikow-ewd.pdf)
	* `id_szkoly`
	* `egz_norm_sr_hum` - śr. wynik humanistyczny zgodnie z metodologią IBE
	* `egz_norm_std_hum` - odchylenie standardowe, j.w.
	* `ewd_min90_hum` - dolna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części humanistycznej
	* `ewd_max90_hum` - górna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części humanistycznej
	* `egz_norm_sr_mp` - śr. wynik matematyczno-przyrodniczy zgodnie z metodologią IBE
	* `egz_norm_std_mp`- odchylenie standardowe, j.w.
	* `ewd_min90_mp` - dolna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części matematyczno-przyrodniczej
	* `ewd_max90_mp` - górna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części matematyczno-przyrodniczej
	* `gwiazdki_pow` - liczba 1-5 w zależności od tego, jak średni wynik plasuje się w powiecie
