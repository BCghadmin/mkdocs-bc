## Pangaga gateway otsekanali lepingu sõlmimine

Business Centralis pangaliidese kasutamiseks on vajalik oma pangas sõlmida *gateway* otsekanali leping ning tellida sertifikaat. Sertifikaadi tellimise juhise saadab pank pärast lepingu sõlmimist. Sertifikaadi faili formaat peab olema .p12 parooliga kaitstud.

### Swedbank

<https://www.swedbank.ee/business/d2d/ebanking/gateway>

Toetatud teenused:

-   Maksete edastamine panka (allkirjastamata maksed)

-   Konto väljavõte -- automaatselt päritav eelmise päeva väljavõte

-   Jooksva päeva kontoväljavõtte päring

### LHV

<https://www.lhv.ee/et/connect>

Toetatud teenused:

-   Maksete edastamine panka (allkirjastamata maksed)

-   Konto väljavõte -- automaatselt päritav eelmise päeva väljavõte

### SEB

<https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway>

Toetatud teenused:

-   Maksete edastamine panka (allkirjastamata maksed)

-   Jooksva päeva kontoväljavõtte päring (tööjärjekorra kanne tuleb seadistada piisava sagedusega, et päeva lõpust ei jääks mõni tehing pangast pärimata)

### COOP Pank

<https://www.cooppank.ee/gateway>

Toetatud teenused:

-   Maksete edastamine panka (allkirjastamata maksed)

-   Konto väljavõte -- automaatselt päritav eelmise päeva väljavõte

### Turvasertifikaat

Business Centralis tuleb pangaliidese kasutamiseks seadistada turvasertifikaat. Pärast lepingu sõlmimist saadab pank teile juhiseid sertifikaadi tellimiseks. Tegemist on tehniliste sammudega, mistõttu soovitame abi paluda oma IT osakonnast või pöörduda oma BC partneri poole, kes teid abistab.

Vajalik on:

-   Sertifikaadipäringu koostamine, sertifikaadi tellimiseks.

-   Sertifikaadi- ja privaatvõtmefaili liitmine pfx/p12 failiks ja parooli genereerimine.

-   pfx/p12 faili ja parooli seadistamine BC-s.

Swedbank juhend:\
<http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf>\
<https://www.swedbank.com/openbanking/swedbank-gateway-go-live.html>

LHV juhend:\
<https://partners.lhv.ee/en/connect/#certificates>

SEB juhend:\
<https://developer.baltics.sebgroup.com/bgw/documentation/authentication>

Coop Pank juhend:\
<https://www.cooppank.ee/s3fs-public/juhendid/Gateway_votmete_genereerimise_juhend.pdf>

## Pangaliidese seadistamine

Ava Business Centralis Pangaliidese seaded ning vali liidestatav pank Panga kanalid blokist. Seadistatavad väljad on pankadel erinevad.

![Conf Bank Interface][13]

**SWED SGW** puhul täida Lepingu ID, API võti (Kliendi ID), Parool väljad ning seejärel lae üles sertifikaat kasutades menüüribal nuppu Lisa sertifikaat:

![SWED SGW configuration example][1]

**SEB BGW** puhul täida lepingu ID väli ja lisa sertifikaat.

**LHV CONNECT** puhul tuleb ainult lisada sertifikaat.

**COOP CPGW** selgub hiljem :)

### Pangakonto seadistus

Ava Pangakontod loend ning ava liidestatava pangakonto kaart, täida OIXIO Pangaliides blokis Panga kanal:

![Bank account configuration example][2]

Pangakonto kaardil peavad olema täidetud järgmised väljad:

-   Maksekorralduste sõnumite numbrid

-   Pangakonto konteeringurühm

-   SWIFT tähis

-   IBAN

-   Panga väljavõtte impordi vorming

-   Makse ekspordi vorming

### Tööjärjekorra kanded

Pane vastava panga tööjärjekorra kanded valmis olekusse.

![Queue entry example][3]

## Maksete eksportimine panka

Maksežurnaali töölehel tuleb märkida Luba maksete eksporti, et saaks maksefaili panka saata ja Kontrolli makse staatuseid enne konteerimist, et konteerimisel toimuks kontroll, kas mõni makse on tühistatud.

![Payment Journal example][4]

Täida maksežurnaal sooritatavate maksetega kas käsitsi või soovitades makseid hankijale.

Maksefaili panka saatmiseks vali menüüribalt Pank -- Saada Panka...

![Send to Bank example][5]

Maksed liiguvad panka kinnitamata olekus. Need tuleb pangas eraldi kinnitada ja sooritada tehingud.

Pärast maksefaili panka saatmist ilmub mõne aja pärast maksežurnaali factboxi info makse oleku kohta:

![Payment status example][6]

Makse olek näitab, mis seisus makse pangas on.

Võimalikud makse olekud:

RJCT -- tagasi lükatud -- makse pangas tagasi lükatud

ACTC -- Ootel - ootab pangas makse kinnitamist ja sooritamist

PDNG -- Ootel - makse kinnituse ootel

PART - Osaliselt kinnitatud -vähemalt üks makse on kinnitatud

ACSP -- Kinnitatud -- makse on kinnitatud, kuid ülekanne veel tegemata

ACSC -- Teostatud -- makse on sooritatud

ACWC - Aktsepteeritud koos muudatusega -- tehtud mõned muudatused ja aktsepteeritud, kuid ülekanne veel tegemata

Ootel -- makse impordifaili kontrollitakse (SEB)

Faili kontroll edukas -makse impordifaili kontroll edukas (SEB)

Tagasi lükatud -- makse impordifaili kontroll ei olnud edukas (SEB)

## Pangaväljavõtte import

### Käsitsi importimine

Maksete sobitamise žurnaalis vali Pangaliidese maksete importimine:

![Import Payments example][7]

Avanevas aknas vali, millise panga millist väljavõtte tüüpi soovid importida:

![Statement type selection][8]

**Päevalõpu väljavõte** -- saad määrata ainult lõppkuupäeva. BC-sse päritakse kõik selleks kuupäevaks importimata pangatehingud.

**Väljavõte** -- saad määrata perioodi, mille kohta pangaväljavõte päritakse BC-sse

**Päevasisene väljavõte** -- päritakse BC töökuupäeva väljavõte

Pärast filtrite määramist tuleb teade:

![Import query notification][14]

See tähendab, et päring on panga saadetud ja läheb natukene aega enne kui pangaväljavõte BC-sse ilmub. SEB väljavõte tekib kohe.

## Pangaväljavõtte automaatne import

Eelmise päeva kohta automaatselt imporditava pangaväljavõtte saamiseks tuleb seadistada Tööjärjekorra kanded all automaatne töö.

Mine Tööjärjekorra kanded ja vajuta Uus

Täida Käivitatava objekti liik Aruanne ja Käivitatava objekti ID 79901, Varaseim alustamise kuup/kl:

![Queue entry configuration example][9]

Varaseim alustamise kuup/kl täida sellega, millal soovid, et eelmise päeva väljavõte BC-sse päritakse.

Seejärel vajuta sisse marker Aruande päringuakna valikud:

![Report request options example][10]

Avaneb sama vaade, mis maksete sobitamise žurnaalis Pangaliidese maksete importimine nupu vajutamisel.

Täida Pank, mille väljavõtet automaatselt importida soovid ja Väljavõtte tüüp lahtrist vali Päevalõpu väljavõte. Algkuupäev ja Lõppkuupäev väljad jäta tühjaks.

![Automatic import configuration example][11]

Täida Korduvus blokis, mis päeviti päring teostatakse ja Minutite arv käivitamise vahel määra 1440, et kord päevas toimuks pangaväljavõtte päring:

![Recurrence settings example][12]

Iga pangakonto kohta tuleb teha eraldi tööjärjekorra kanne.

  [1]: ./media/image2.png
  [2]: ./media/image3.png
  [3]: ./media/image4.png
  [4]: ./media/image5.png
  [5]: ./media/image6.png
  [6]: ./media/image7.png
  [7]: ./media/image8.png
  [8]: ./media/image9.png 
  [9]: ./media/image11.png
  [10]: ./media/image12.png
  [11]: ./media/image13.png
  [12]: ./media/image14.png
  [13]: ./media/image1.png
  [14]: ./media/image10.png
