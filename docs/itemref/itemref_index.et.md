# Seadistused

## Ostu seadistus

Ostuga seotud seadistused on „Ostude ja ostuv. seadistus" lehel plokis „Suno kauba viited"

![][1]

### Kaubakood ostudokumendil

![][2]

### Kauba viitenumber ostutellimusel

![][3]

## Müügi seadistus

Müügiga seotud seadistused on „Müügi ja müügivõlgade seadistus" lehel plokis „Suno kauba viited"

![][4]

### Kaubakood müügidokumendil

![][5]

### Kauba viitenumber müügitellimusel

![][6]

## Hankija seadistus

Hankijaga seotud seadistused on hankija kaardil plokis „Suno kauba viited".

![][7]

## Kliendi seadistus

Kliendiga seotud seadistused on kliendi kaardil plokis „Suno kauba viited".

![][8]

# Funktsionaalsused

Kasutatavad funktsionaalsused on seotud järgneva tabeli ja väljadega. Tabeli „Kaubaviidete loend" kirjetega.

![][9]

Kaubakaardil olevate väljadega „Hankija kauba nr."

![][10]

Hankija ja kliendi kaardil rippmenüüs „Kaubakood ostu(kliendi kaardil müügi)dokumendil"

![][11]

## Kaubakood ostu- või müügidokumendil 

Erinevate kaubakoodide kasutamine ostu- või müügidokumentide väljatrükil. Laiendus ei mõjuta Microsoft Base väljatrükke ja kasutamiseks tuleb vastavale väljatrüki laiendusele(näiteks Suno Base) lisada sõltuvus Suno Item Ref'ile. Väljatrüki näide, kus muudetakse kaubakoodi väljatrükil.

![][12]

Võimalik on valida 5 erineva võimaluse vahel ostu või müügi seadistustes: Tühi (BC standard), Kaup, Vöötkood/hankija/Kaup, Hankija/vöötkood/kaup, Hankija kauba nr./kaup. Müügidokumentide puhul on Hankija asemel Klient.

![][13]

Võimalik on valida 5 erineva võimaluse vahel hankija või kliendi kaardil: Tühi (BC standard), Kaup, Vöötkood/hankija/Kaup, Hankija/vöötkood/kaup, Hankija kauba nr./kaup. Kliendi kaardi puhul on Hankija asemel Klient.

![][14]

Kehtib üldine loogika, et kui hankija või kliendi kaardil on mingi valik valitud, siis kehtib see ainult antud kliendi või hankija dokumentide puhul ja ühtlasi ei sõltu sellest, et mis on määratud ostu või müügi seadistustes.

Kõikide valikute puhul kehtib loogika, et iga valiku puhul kasutatakse järjekorras esimest leitud vastet. Näiteks: Vöötkood/hankija/kaup.

![][15]

![][16]

Sellise ostutellimuse puhul kasutatakse dokumentide väljatrükkide puhul tabelis „Kaubaviidete loend" leitud vöötkoodi viitenumbrit. Kui seda väärtust ei oleks tabelist leitud, siis oleks otsitud kaubaga seotud hankija koodi ja kui seda ei oleks ka leitud, siis oleks kasutatud kauba peal määratud kaubakoodi. Kui ükski neist otsingutest ei anna tulemust, siis lisatakse BC standard väärtus.

## Kauba viitenumber ostu- või müügitellimusel 

Erinevate viitenumbrite kasutamine ostu- või müügitellimusel. Näide ostutellimuse välja Kauba viitenr. kohta.

![][17]

Võimalik on valida 4 erineva võimaluse vahel ostu või müügi seadistustes: Tühi (BC standard), Hankija/Vöötkood, Hankija/Vöötkood/Määramata, Vöötkood/Hankija. Müügitellimuste puhul on Hankija asemel Klient.

![][18]

Kõikide valikute puhul kehtib loogika, et iga valiku puhul kasutatakse järjekorras esimest leitud vastet. Näiteks: Hankija/Vöötkood/Määramata.

![][19]

![][20]

Sellise ostutellimuse puhul kasutatakse ostutellimuse real välja „Kauba viitenr." puhul tabelis „Kaubaviidete loend" leitud hankija viitenumbrit. Kui seda väärtust ei oleks tabelist leitud, siis oleks otsitud kaubaga seotud vöötkoodi ja kui seda ei oleks ka leitud, siis oleks otsitud tabelist määramata välja „Viite liik" seotud kaubakoodi. Kui ükski neist otsingutest ei anna tulemust, siis lisatakse BC standardi väärtus.

  [1]: ./media/image1ee.png
  [2]: ./media/image2ee.png
  [3]: ./media/image3ee.png
  [4]: ./media/image4ee.png
  [5]: ./media/image5ee.png
  [6]: ./media/image6ee.png
  [7]: ./media/image7ee.png
  [8]: ./media/image8ee.png
  [9]: ./media/image9ee.png
  [10]: ./media/image10ee.png
  [11]: ./media/image11ee.png
  [12]: ./media/image12ee.png
  [13]: ./media/image13ee.png
  [14]: ./media/image14ee.png
  [15]: ./media/image15ee.png
  [16]: ./media/image16ee.png
  [17]: ./media/image17ee.png
  [18]: ./media/image18ee.png
  [19]: ./media/image18ee.png
  [20]: ./media/image18ee.png