Dane projektu Szkołomat
-----------------------

## Opis danych

* `szkoly_ibe_2013.csv`
	* `id_szkoly`
	* `nazwa`
	* `adres`
	* `miejscowosc`
	* `kod_pocztowy`
	* `poczta`
	* `typ_szkoly`
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
* `szkoly_ibe_sio_dowiazanie.csv`
	* `id_szkoly`
	* `lp_sio`
	* `odl_dop`
	* `telefon`
	* `fax`
	* `www`
	* `oddzialy`
	* `liczba_uczniow`
	* `specjalna`
	* `publiczna`
* `szkoly_geolokalizacja.csv
	* `id_szkoly`
	* `lat`
	* `lng`
	* `geolocalizer_count`
	* `location_type`
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


## Informacje

Przestawione dane ze sprawdzianów i egzaminów są znormalizowanymi danymi - tj. tak przeskalowanymi danymi.

Dalsze informacje, oraz motywacja takiego podejścia, znajdują się w prezentacji:

* Tomasz Żółtak, [Skalowanie wyników egzaminacyjnych](http://ewd.edu.pl/szkoly-ewd/jesienna-2013/skalowanie.pdf), Jesienna Szkoła EWD, Warszawa 17.10.2013

Dalsze informacje związane z [Edukacyjną Wartością Dodaną](http://ewd.edu.pl/) (plik `gimn_egz_2002do2013.csv`) znajdują się w raporcie:

* Tomasz Żółtak, [Statystyczne modelowanie wskaźników edukacyjnej wartości dodanej - podsumowanie polskich doświadczeń](http://www.ibe.edu.pl/images/publikacje/ibe-raport-modelowanie-wskaznikow-ewd.pdf), Analizy IBE/02/2013

W przypadku wykorzystania danych związanych z Edukacyjną Wartością Dodaną prosimy o cytowanie w/w artykułu.

## Licencja

Dane zawarte w pliku `gimn_wskazniki_2013.csv` są udostępnione na wolnej licencji [Creative Commons Attribution](http://creativecommons.org/licenses/by/3.0/), przez [Instytut Badań Edukacyjnych](http://www.ibe.edu.pl/).

Pozostałe dane te nie są przejawem twórczej działalności o indywidualnym charakterze zatem, zgodnie z polskim prawem, nie podlegają prawu autorskiemu.
