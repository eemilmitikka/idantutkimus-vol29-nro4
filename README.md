# idantutkimus-vol29-nro4

Replikaatiokoodit R-ohjelmointikielellä ja RStudiolla (versio: 2022.7.0.548) tehtyihin visualisointeihin ja data-analyyseihin Idäntutkimuksen "Ääni"-teemanumeroon kirjoitettuun artikkeliin. [r_replication_code.Rmd](https://github.com/eemilmitikka/idantutkimus-vol29-nro4/blob/main/docs/r_replication_code.Rmd) -tiedosto sisältää artikkelin visualisointien ja analyysien replikaatiokoodit. R-koodi yleisiin visuloisointeihin löytyy *Kuva 1*, *Kuva 2* ja *Kuva 3* alta, ja tilastollisiin malleihin *Kuva 4*, *Kuva 5* ja *Kuva 6* otsikoiden alla olevista osioista.

Dokumentti on koostettu siten, että parsimalla (*knit*) tiedoston kasaan koodien pitäisi toimia ja tuottaa haluttu tulos.

Tilastollisten mallien analyysit on tehty staattisten kyselytutkimusaineistojen pohjalta. Nämä aineistot ovat avoimesti ladattavissa seuraavista linkeistä (toimivuus tarkistettu 31.8.2022):

* Chronicles: projektin [GitHub-sivut](https://github.com/dorussianswantwar/research1)
* Russian Field: projektin nettisivut
  - [26–28 helmikuuta 2022 tehty sotakysely](https://drive.google.com/file/d/1JslJAa062JV60FVGKjYtcF_93SMXfQgD/view)
  - [5–7 maaliskuuta 2022 tehty sotakysely](https://drive.google.com/file/d/1EvOioLSvfiDi5SHsnYCbCcuPS8pgWTx0/view)
  - [13–16 maaliskuuta 2022 tehty sotakysely](https://drive.google.com/file/d/1IGNkysodMW9SyONXHO6yGOFPDE08IsXK/view)
  - [23–26 toukokuuta 2022 tehty sotakysely](https://drive.google.com/file/d/1bL6dwGZjtwTspdt_bPmUyxAwtuo91WOc/view)
* VTSIOM: kyselytutkimuslaitoksen nettisivut, suoralinkit tässä käytettyihin aineistoihin:
  - [Специальная военная операция в Украине: отношение и цели](https://wciom.ru/analytical-reviews/analiticheskii-obzor/specialnaja-voennaja-operacija-v-ukraine-otnoshenie-i-celi) ... Материалы ... Массив данных
  - [Специальная военная операция: мониторинг | 23 марта 2022](https://wciom.ru/analytical-reviews/analiticheskii-obzor/specialnaja-voennaja-operacija-monitoring) ... Материалы ... Массив данных
  - [Cпециальная военная операция: мониторинг | 30 марта 2022](https://wciom.ru/analytical-reviews/analiticheskii-obzor/cpecialnaja-voennaja-operacija-monitoring-20220330) ... Материалы ... Массив данных
  - [Cпециальная военная операция: мониторинг | 30 мая 2022](https://wciom.ru/analytical-reviews/analiticheskii-obzor/cpecialnaja-voennaja-operacija-monitoring) ... Материалы ... Массив данных
  - [Специальная военная операция: мониторинг | 30 июня 2022](https://wciom.ru/analytical-reviews/analiticheskii-obzor/specialnaja-voennaja-operacija-monitoring-20223006) ... Материалы ... Массив данных
  
Kaikki tässä käytetyt tilastolliset aineistot on tallennettu `data` nimiseen kansioon, jonka vuoksi työhakemisto (*working directory*) kulkee tässä käytetyn **here-paketin** logiikalla seuraavasti: `here("data/tiedostonimi.tiedostoformaatti")`, esim. `here("data/Полные Хроники 5.0.sav")`, jne. Replikaatioanalyysiä tehdessä tiedostopolku on määriteltävä oman paikallisen työhakemiston mukaan.

Tutkimuksen tilastollisissa malleissa käytettyjen muuttujien kuvaukset sekä muuttujien alkuperäiset kysymykset ja suomennokset löytyvät [täältä](https://github.com/eemilmitikka/idantutkimus-vol29-nro4/blob/main/docs/kyselyiden_kysymykset.pdf).