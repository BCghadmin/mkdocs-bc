# KMD aruande saatmine Maksuametisse X-tee liidese kaudu

Lahendus võimaldab Dynamics 365 Business Centrali kaudu saata elektrooniliselt käibedeklaratsiooni Maksu ja Tolliametisse X-Tee kaudu.

Eesti äriregistris registreeritud ettevõtete ja asutuste juhid saavad X-teega liituda läbi [X-tee iseteeninduskeskkonna].

Business Centralis funktsionaalsuse kasutamiseks peab teenus olema Maksu- ja Tolliameti poolt avatud - <https://www.emta.ee/ariklient/e-teenused-koolitused/e-teenuste-kasutamine/x-tee-teenused>

## Seadistus

Lehel **XTee seadistus** saab üles laadida sertifikaadi: Toiminigud \> Lae sertifikaat üles. Sertifikaadi parool sisestada väljale Parool ja vajutada ENTER.

Välja "**Esitaja isikukood**" lisada MTA-s deklaratsiooni esitamise õigust omava kasutaja isikukood.

Selleks, et saata EMTA-sse kinnitatud KMD tuleb XTee seadistus lehel valida **KMD saadetakse kinnitatuna:**

# ![Pilt, millel on kujutatud tekst, kuvatõmmis, number, Font Tehisintellekti genereeritud sisu ei pruugi olla õige.]

## Funktsionaalsuse kasutamine

KMD moodustatakse vastavalt Eesti lokalisatsioonile lehel **KM tagastused (KMD).**

Kui deklaratsiooni read on loodud ja kontrollitud, siis **Vabasta** dokument.

Deklaratsiooni saatmine käivitatakse: Avaleht -\> **Saada X-Tee kaudu EMTA-sse**:

![Pilt, millel on kujutatud tekst, Font, järjekord, tarkvara Tehisintellekti genereeritud sisu ei pruugi olla õige.]

Oleku jälgimiseks on loodud väljad:

- XTee logi kande nr. -- täidetakse kande numbriga peale saatmist

- XTee seisund -- kuvatakse seisundid:

- Saadetud -- KMD on saadetud EMTA-sse

- Vastuvõetud -- BC-s kinnitamata KMD on EMTA poolt vastu võetud

- Kinnitatud -- BC-s kinnitatud KMD on EMTA poolt vastu võetud

- Viga -- EMTA on KMD vigade tõttu tagasi lükanud

Tööjärjekorra kanne „24014760 ∙**Uuenda XTee sõnumite seisundid**" pärib MTA-st vastused.

## Sõnumilogid

Klikkides XTee logi kande nr. väljas olevale numbrile avaneb **Xtee sõnumilogi**

Saab vaadata nii Päringu- kui ka Vastussõnumeid klikkides vastavas veerus olevale Jah -le.![Pilt, millel on kujutatud tekst, kuvatõmmis, number, tarkvara Tehisintellekti genereeritud sisu ei pruugi olla õige.]

**Ava sõnumiseisundilogi** avab lehe Xtee sõnumiseisundilogi. Siin saab avada nii Päringusõnumeid kui ka Vastussõnumeid text formaadis

![Pilt, millel on kujutatud tekst, Font, kuvatõmmis, järjekord Tehisintellekti genereeritud sisu ei pruugi olla õige.]

MTA-st vastuste päringu saab käivitada ka käsitsi klikkides lehel XTee sõnumiseisundilogi „**Küsi vastust**". Kommentaar „Ootel sõnumeid ei leitud" tähendab, et kõik MTA vastussõnumid on kätte saadud.

# ![Pilt, millel on kujutatud tekst, number, Font, järjekord Tehisintellekti genereeritud sisu ei pruugi olla õige.]

# 

# TSD aruande edastamine X-tee liidese kaudu

## Ülevaade

Lahendus võimaldab Dynamics 365 Business Centrali kaudu saata elektrooniliselt tulu- ja sotsiaalmaksu deklaratsiooni (TSD) faili XML formaadis Maksu ja Tolliametisse X-Tee kaudu. Lahendus võimaldab küsida tagasiside failis sisalduvate vigade ja hoiatuste kohta ning kinnitada esitatud faili ja tervet deklaratsiooni.

Teenuse kasutamiseks peab ettevõte olema liitunud X-tee'ga.

## X-tee seadistused

Seadistused tehakse lehel XTee seadistus. Deklaratsioonide edastamisega seotud seadistused tehakse paanil „Üldine". TSD'ga seotud lisaseadistused on paanil „TSD":

![A screenshot of a computer AI-generated content may be incorrect.]

## TSD aruandefaili saatmine

### TSD aruanne -\> Toimingud

![A screenshot of a computer AI-generated content may be incorrect.][1]

**TSD XML üleslaadimine** -- Valmis TSD faili üleslaadimine (kuna hetkel programmis faili ei tekki, tulevikus kaob vajadus ära)

**TSD faili edastamine** -- TSD faili saatmine Maksuametisse läbi uploadMime teenuse.

**TSD kinnitamine** -- TSD kinnitamine läbi confirmTsd teenuse.

**TSD faili või kinnituse staatuse küsimine** -- faili või kinnituse staatuse küsimise teenus.

**TSD tagasiside küsimine** -- TSD tagasiside küsimine läbi getTsdStatus teenuse.

**TSD sõnumilogi** -- avab TSD Xtee sõnumilogi.

### TSD XML üleslaadimine

Avaneb aken, kus saab lisada TSD XML faili:

![A screenshot of a computer error AI-generated content may be incorrect.]

Kui fail on lisatud, TSD aruande tabelis veerus „Üles laaditud XML" on „Jah":

![A screenshot of a computer AI-generated content may be incorrect.][2]

Nüüd saab TSD faili edastada.

### TSD faili edastamine

Vali lintmenüült Toimingud - \> TSD faili edastamine. Kui fail on edastatud muutub TSD seisund „Saadetud" ja Faili ID veergu tekib maksuametist saadetud faili ID, mis on vajalik ka järgmiste päringute tegemiseks.

![][3]

TSD Xtee logi:

![][4]

Kui faili ID ei tulnud, siis TSD staatus on „Viga". Põhjus on tehnilist laadi ja ei puuduta faili sisu.

![A close up of a screen AI-generated content may be incorrect.]

Vaata üle, kas vajalikud X-tee seadistused on olemas või võta ühendust lahenduse administraatoriga.

### TSD kinnitamine

Saab valida, kas toimub terve TSD või ainult üles laaditud faili kinnitamine. Terve TSD kinnitamine eeldab, et kõik TSD lisad on ootusepäraselt täidetud.

Vali lintmenüült Toimingud - \> TSD kinnitamine.

Kui kinnitamis saatmine õnnestus, TSD seisund on „Kinnitatud", TSD Xtee sõnumilogi:

![][5]

Kui kinnitamist ei toimunud, on seisund „ Viga", TSD Xtee sõnumilogis näeb vea kirjeldust:

![][6]

### TSD faili või kinnituse staatuse küsimine

Päringuga küsitakse faili või kinnituse staatust, kas fail/kinnitus ootab töötlemist, töödeldud või viga töötlemisel.

![A screenshot of a computer AI-generated content may be incorrect.][7]

Kinnitatud deklaratsioon:

![A screenshot of a computer AI-generated content may be incorrect.][8]

### TSD tagasiside küsimine

Päringut teostatakse, siis, kui faili seisund on „Töödeldud", et selgitada välja, kas failis oli vigu/hoiatusi.

Kui failis on vigu, seisund on „Viga" ja veerus tagasiside vead näeb nende arvu.

![A close up of a screen AI-generated content may be incorrect.][9]

Klõpsates vigade arvul, avaneb tabel TSD tagasiside vead, kust näeb millisel TSD lisal, milliste isikute ridadega on probleeme. Veatüübid:

ERROR -- viga, maksukohustust ei saa õigesti välja arvutada, deklaratsiooni ei saa kinnitada;

WARNING -- hoiatus, ennetav teade, deklaratsiooni on võimalik ära kinnitada.

![A screenshot of a computer AI-generated content may be incorrect.][10]

Kui failis/deklaratsioonis vigu ei esine, saab seda ära kinnitada.

  [X-tee iseteeninduskeskkonna]: https://x-tee.ee/
  [Pilt, millel on kujutatud tekst, kuvatõmmis, number, Font Tehisintellekti genereeritud sisu ei pruugi olla õige.]: ./media/image1.png {width="6.270833333333333in" height="2.5208333333333335in"}
  [Pilt, millel on kujutatud tekst, Font, järjekord, tarkvara Tehisintellekti genereeritud sisu ei pruugi olla õige.]: ./media/image2.png {width="5.927083333333333in" height="1.8541666666666667in"}
  [Pilt, millel on kujutatud tekst, kuvatõmmis, number, tarkvara Tehisintellekti genereeritud sisu ei pruugi olla õige.]: ./media/image3.png {width="6.270833333333333in" height="3.1979166666666665in"}
  [Pilt, millel on kujutatud tekst, Font, kuvatõmmis, järjekord Tehisintellekti genereeritud sisu ei pruugi olla õige.]: ./media/image4.png {width="6.270833333333333in" height="1.1041666666666667in"}
  [Pilt, millel on kujutatud tekst, number, Font, järjekord Tehisintellekti genereeritud sisu ei pruugi olla õige.]: ./media/image5.png {width="6.270833333333333in" height="1.3020833333333333in"}
  [A screenshot of a computer AI-generated content may be incorrect.]: ./media/image6.png {width="6.3in" height="3.8555555555555556in"}
  [1]: ./media/image7.png {width="6.3in" height="1.9375in"}
  [A screenshot of a computer error AI-generated content may be incorrect.]: ./media/image8.png {width="4.561417322834646in" height="2.58792104111986in"}
  [2]: ./media/image9.png {width="4.274004811898513in" height="1.18332895888014in"}
  [3]: ./media/image10.png {width="6.3in" height="0.7125in"}
  [4]: ./media/image11.png {width="5.994343832020998in" height="0.6468755468066492in"}
  [A close up of a screen AI-generated content may be incorrect.]: ./media/image12.png {width="4.701733377077865in" height="0.9391021434820648in"}
  [5]: ./media/image13.png {width="6.3in" height="0.7145833333333333in"}
  [6]: ./media/image14.png {width="6.3in" height="0.71875in"}
  [7]: ./media/image15.png {width="6.3in" height="1.0493055555555555in"}
  [8]: ./media/image16.png {width="6.3in" height="1.0659722222222223in"}
  [9]: ./media/image17.png {width="6.3in" height="1.0in"}
  [10]: ./media/image18.png {width="6.3in" height="1.1104166666666666in"}
