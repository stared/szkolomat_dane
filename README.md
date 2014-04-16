Dane projektu Szkołomat
-----------------------

Otwarte dane związane ze stroną [Szkołomat - automat do wyszukiwania szkół](http://szkolomat.pl/) fundacji [Projekt: Polska](http://centrumcyfrowe.pl/).


## Informacje


Informacje pochodzą z następujących źródeł:

* [Centralna Komisja Egzaminacyjna (CKE)](http://www.cke.edu.pl/)
* Okręgowa Komisje Egzaminacyjne (OKE)
* [Instytut Badań Edukacyjnych (IBE)](http://www.ibe.edu.pl/)
* [System Informacji Oświatowej (SIO)](http://cie.men.gov.pl/index.php/sio-wykaz-szkol-i-placowek.html)
* [The Google Geocoding API](https://developers.google.com/maps/documentation/geocoding/)

Przestawione dane ze sprawdzianów i egzaminów są znormalizowanymi danymi - tj. tak przeskalowanymi danymi, by:

* średnia uczniów wynosiła 100,
* odchylenie standardowe wynosiło 15,
* rozkład wyników był rozkładem normalnym.

Dalsze informacje, oraz motywacja takiego podejścia, znajdują się w prezentacji:

* Tomasz Żółtak, [Skalowanie wyników egzaminacyjnych](http://ewd.edu.pl/szkoly-ewd/jesienna-2013/skalowanie.pdf), Jesienna Szkoła EWD, Warszawa 17.10.2013

Dalsze informacje związane z [Edukacyjną Wartością Dodaną](http://ewd.edu.pl/) (plik `gimn_egz_2002do2013.csv`) znajdują się w raporcie:

* Tomasz Żółtak, [Statystyczne modelowanie wskaźników edukacyjnej wartości dodanej - podsumowanie polskich doświadczeń](http://www.ibe.edu.pl/images/publikacje/ibe-raport-modelowanie-wskaznikow-ewd.pdf), Analizy IBE/02/2013

W przypadku wykorzystania danych związanych z Edukacyjną Wartością Dodaną prosimy o cytowanie w/w artykułu.


## Licencja

Dane zawarte w pliku `gimn_wskazniki_2013.csv` są udostępnione na wolnej licencji [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/), przez [Instytut Badań Edukacyjnych](http://www.ibe.edu.pl/).

Pozostałe dane te nie są przejawem twórczej działalności o indywidualnym charakterze zatem, zgodnie z polskim prawem, nie podlegają prawu autorskiemu.


## Opis danych

* `szkoly_ibe_2013.csv`
	* `id_szkoly`
	* `nazwa`
	* `adres`
	* `miejscowosc`
	* `kod_pocztowy`
	* `poczta` - miejscowość związana z pocztą
	* `typ_szkoly`
		* `SP` - szkoła podstawowa 
		* `gimn.` -  gimnazjum
	* `publiczna`
	* `dla_doroslych`
	* `specjalna`
	* `przyszpitalna`
	* `wojewodztwo`
	* `powiat`
	* `gmina`
	* `id_wojewodztwa`
	* `id_powiatu`
	* `id_gminy`
* `szkoly_ibe_sio_dowiazanie.csv` - dane IBE dowiązane do [danych SIO z roku 2013](http://cie.men.gov.pl/index.php/sio-wykaz-szkol-i-placowek/27-wykaz-wg-typow.html)
	* `id_szkoly`
	* `lp_sio`
	- identyfikator (pole `Lp.` w wykazie szkół SIO z roku 2013)
	* `odl_dop`
	* `telefon`
	* `fax`
	* `www`
	* `oddzialy`
	* `liczba_uczniow`
	* `specjalna`
	* `publiczna`
* `szkoly_geolokalizacja.csv
- wyszukania za [Google Geocoding API](https://developers.google.com/maps/documentation/geocoding/)
	* `id_szkoly`
	* `lat`
	- szerokość geograficzna
	* `lng`
	- długość geograficzna
	* `geolocalizer_count`
	- liczba wyszukań (jeśli więcej niż 1 - lokalizacja niepewna) 
	* `location_type`
	- typ lokacji (`ROOFTOP` znaczy, że dokładnie ten budynek)
* `sp_spr_2002do2013.csv`
	* `id_szkoly`
	* `wyn_norm_sr`
	* `wyn_norm_std`
	* `probka`
	* `rok`
	* `czesc`
* `sp_wskazniki_2013.csv`
	* `id_szkoly`
	* `gwiazdki_pow`
* `gimn_egz_2002do2013.csv`
	* `id_szkoly`
	* `egz_norm_sr` - średnia znormalizowanych wyników
	* `egz_norm_std` - odchylenie standardowe znormalizowanych wyników 
	* `probka` - liczba uczniów uwzględnionych w próbce
	* `rok`
	* `czesc`
		* `gh` - humanistyczna i j. polski (do 2011)
		* `gm` - matematyczno-przyrodnicza (do 2011)
		* `gh_h` - humanistyczna (od 2012)
		* `gh_p` - j. polski (od 2012)
		* `gm_p` - przyrodnicza (od 2012)
		* `gm_m` - matematyczna
* `gimn_wskazniki_2013.csv`
	* `id_szkoly`
	* `egz_norm_sr_hum`
	* `egz_norm_std_hum`
	* `ewd_min90_hum` - dolna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części humanistycznej
	* `ewd_max90_hum` - górna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części humanistycznej
	* `egz_norm_sr_mp`
	* `egz_norm_std_mp`
	* `ewd_min90_mp` - dolna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części matematyczno-przyrodniczej
	* `ewd_max90_mp` - górna granica 90% przedziału ufności dla Edukacyjnej Wartości Dodanej dla części matematyczno-przyrodniczej
	* `gwiazdki_pow`