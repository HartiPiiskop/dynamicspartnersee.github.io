---
---
# Eesti e-arved - Kasutusjuhend

Eesti e-arve lahendus võimaldab teil vahetada e-arveid oma äripartneritega. Eeldusena peate olema sõlminud operaatorlepingu Finbite'ga või Unifiedpost'iga.

## Sisukord
  - [Teenuse seadistamine](#teenuse-seadistamine)
  - [Tööjärjekorra kanded](#tööjärjekorra-kanded)
  - [Andmevahetustegevuste logi](#andmevahetustegevuste-logi)
  - [E-arvete vastuvõtmine](#e-arvete-vastuvõtmine)
  - [E-arvete salvestamine ostuarveks](#e-arvete-salvestamine-ostuarveks)
  - [E-arvete saatmine](#e-arvete-saatmine)
  - [Põhiandmete saatmine Finbite](#põhiandmete-saatmine-Finbite)

## Teenuse seadistamine

Avage **Finbite (Omniva) dokumendivahetusteenuse seadistus** või **Unifiedpost (FitekIn) dokumendivahetusteenuse seadistus** ning seadistage järgnevad väljad:


Kiirkaart / Väli | Selgitus
|--|--|
**Üldine** | 
Lubatud | Aktiveerib teenuse ning loob automaatse andmevahetuse jaoks vajalikud **Tööjärjekorra kanded**.
Võtmekasutaja | Tema rollikeskuse teatistesse saadetakse automaatsete andmevahetustööde käigus tekkivad vead, mis vajavad lahendamist.
Tegevuse logimine | Määrab, millise detailsusega peetakse andmevahetuse tegevuste logi. Testperioodil on soovitav kasutada valikut „Tegevuse teade ja XML sõnumid“, et saada probleemide lahendamiseks maksimaalselt infot. Logitud teated ja sõnumid on vaadeldavad lehel Tegevuse logi.
**Ühendus** | Ühenduse vaikeväärtuste seadistamiseks saate kasutada tegevust Taasta URLide vaikeväärtused.
Teenuse URL | Finbite puhul leiate selle arvete halduse keskkonnast Üldinfo->Seaded->Andmevahetus ERP-ga.
Teenuse nimeruumi URL | Vaikeväärtust ei ole vaja üldjuhul muuta.
SOAP nimeruumi URL | Vaikeväärtust ei ole vaja üldjuhul muuta.
Autentimisfraas (Finbite puhul) | Leiate selle Finbite arvete halduse keskkonnast Üldinfo->Seaded->Andmevahetus ERP-ga.
Kasutajanimi  (Unifiedposti puhul) | Täpsustage Unifiedpost’ist.
Parool  (Unifiedposti puhul) | Täpsustage Unifiedpost’ist.
**Dokumendid**  (Finbite puhul) | 
Võta arved muudetud alates | Dokumendivahetuse sisemine järjehoida. Mittemuudetav.
Võta arved, mis on | Määrab, millise olekuga ostuarved laetakse BC-sse: <br> a) Töödeldud - st peale nende töötlemist Finbite arvehalduses. <br> b) Vastu võetud - st kohe peale arve saabumist Finbite-i. <br> c) Kinnitatud - st peale arve kinnitamist Finbites.
Võta arve manused | Määrab, kas võetakse e-arvega kaasasolevad manused. „Põhimanus“ on üljuhul arve PDF kujul.

Ühenduse testimiseks kasutage tegevust **Testi ühendust**.

<br>

## Tööjärjekorra kanded

Teenuse aktiveerimisel luuakse automaatse andmevahetuse jaoks Tööjärjekorra kanded. Tööjärjekorra kannete vaatamiseks klikkige teenuse seadistuses **Tööjärjekorra kanded**.

Andmevahetuse töö | Selgitus
|--|--|
Saada PR kontod | Saadab PR kontod, millel on märge **Saada Finbite**.
Saada dimensioonid | Saadab dimensioonid, millel on märge **Saada Finbite**.
Saada hankijad ja kliendid | Saadab hankijad ja kliendid, millel on märge **Saada Finbite**.
Võta ostuarved | Võtab operaatori serverist ostuarved ning salvestab need tabelisse Sissetulevad dokumendid.
Saada kont. ostuarvete nr. | Saadab konteeritud ostuarve numbri Finbitest tulnud sissetulevatele dokumentidele.
Saada järjek. müügiarved | Saadab müügiarved, mille **E-arve olek** on „Ootab saatmist“ või „Saatmise tõrge“. Kliendil peab olema **Dokumendi saatmise profiil**, millel on seadistatud **Eesti e-arve**.

Seadistage töödele soovitud sagedus ning aktiveerige iga töö tegevusega **Sea olekuks Valmis**. Käsitsi saab andmevahetuse tegevusi käivitada **Finbite (Omniva) dokumendivahetusteenuse seadistuse** või **Unifiedpost (FitekIn) dokumendivahetusteenuse seadistuse** toimingute ribalt.

<br>

## Andmevahetustegevuste logi

Kõik andmevahetuse tegevused logitakse. Tõrgete korral aitavad need teid probleemi lahendamisel. Andmevahetustegevuste logi sissekanded lingitakse andmetega järgnevalt:

Andmekirje / Leht | Andmevahetustegevus
|--|--|
Finbite (/Unifiedpost) dokumendivahetusteenuse seadistus | -Kontoplaani ja dimensioonide saatmine <br> -Hankijate ja klientide saatmine <br> -Ostuarvete paketi vastuvõtmine
Sissetulev dokument | -Ostuarvega seotud manuste vastuvõtmine <br> -Konteeritud ostuarve nr. saatmine
Konteeritud müügiarve ( või kreeditarve) | -Müügiarve saatmine

Logi sissekannete vaatamiseks klikkige seadistusel või dokumendil **Tegevuse logi**.

<br>

## E-arvete vastuvõtmine

E-arvete vastuvõtmine on tavaliselt seadistatud automaatseks tegevuseks. Selle kontrollimiseks avage **Finbite (/Unifiedpost) dokumendivahetusteenuse seadistus**, veenduge, et see on **Lubatud** ning klikkige **Tööjärjekorra kanded**. Avage töö „Võta ostuarved“ ning veenduge, et see on seadistatud ja töötab nii nagu soovite.

Juhul, kui soovite arvete vastuvõtmist kävitada käsitsi, saate seda teha teenuse seadistuse lehel tegevusega **Võta ostuarved**.

Vastu võetud e-arved salvestatakse tabelisse **Sissetulevad dokumendid**.

<br>

## E-arvete salvestamine ostuarveks

Lahenduse funktsionaalsust (sh ostuarveks salvestamisel ning loodud arve ridade info hoidmisel) saab juhtida **Ostude ja ostuv. seadistus** lehel:

![Ostude ja ostuv. seadistus](1-Ostu_ja_ostuv_seadistus.png "Punasega piiritletud väljad, mis mõjutavad lahenduse funktsionaalsust")

- Sektsioonis **Vaikekontod** saab seadistada pearaamatu konto, mida süsteem kasutab arveridadele konto määramisel (vt all loogika punkt 5)
- Sektsioonis Eesti e-arvete seaded saab:
  - Aktiveerida kaupade tuvastamise funktsionaalsuse (vt all loogika punkt 2)
  - Aktiveerida allahindluste tuvastamise funktsionaalsuse (vt all loogika punkt 7)
  - Teha osturea andmete säilitamise määrangud (vt all Osturea andmete säilitamise määrangud)


**Protsess:**

Avage **Sissetulevad dokumendid**. Valige saabunud e-arve, mille soovite salvestada ostuarveks ning klikkige **Loo dokument**.

Kui tegevus ebaõnnestus, siis vaadake **Sissetuleva dokumendi** kiirkaarti **Tõrked ja hoiatused**.

<br>

Automaatseks ostuarve loomiseks tuleks seadistada BC töövoog, kasutades malli **Sissetulevate dokumentide edastuse töövoog** (Incoming Document Exchange Workflow).

<br>

**E-arvest ostuarve loomisel kasutatakse järgnevat loogikat:**
1. Hankija tuvastatakse **Registreerimisnumbri** alusel. <br>
Hankija puudumisel on võimalus hankija automaatselt luua (eeldusel, et Riigid/regioonid tabelis on seadistatud Uue hankija mall) aga see ei ole soovituslik.
2. **Kaubad** tuvastatakse ainult juhul kui **Aktiveeri kaupade tuvastamine e-arvelt** on aktiveeritud **Ostu ja ostuv. seadistus** lehel. <br>
Kaubad tuvastatakse järgmises järjekorras: <br>
a) BC kauba nr. (BuyerProductId tagis oleva koodi alusel) <br>
b) EAN (esmalt GTIN kauba kaardil, seejärel vöötkood ristviidetes) <br>
c) Müüja kauba kood (esmalt ristviidetes, seejärel vaadatakse, kas vastavat BC kauba nr. leidub *(kuna Finbite-is käsitsi loodud kaubad saadetakse ka kui SellerProductId)*) <br>
3. **Kulukontod ja dimensioonid** võetakse e-arvest juhul, kui need on seal olemas – st. eelkonteerimine on tehtud operaatori arvehalduskeskkonnas.
4. Kui konto e-arvel puudub, siis kasutatakse **Vastenda tekst kontoks** funktsionaalsust, kust kõigepealt otsitakse e-arve rea kirjeldusele vastet ning kui seda ei leita, siis hankija nimele vastavat seadistust. **NB! Vastendamises on lubatud filtri kujul seadistused.**
5. Viimases järjekorras kasutatakse **Ostu ja ostuv. seadistus** lehel, **Vaikekontod** kiirkaardil määratud vaikekontosid.
6. **KM toote konteeringurühm** võetakse e-arvelt (juhul, kui see on seal olemas). Viimase puudumisel kasutatakse leitud kauba või PR konto vastavat määrangut. <br> NB! Kui e-arvel on väiksem KM %, kui kauba või PR konto KM toote konteeringurühmal, leiab süsteem esimese KM toote konteeringurühma (*kombinatsioonis hankija pealt tuleva KM äri konteeringurühmaga*), millel on sama KM % kui e-arve real, ning kasutab seda.
7. **Allahindlus** lisatakse arvereale ainult juhul kui **Aktiveeri allahindluste tuvastamine e-arvelt** on aktiveeritud **Ostu ja ostuv. seadistus** lehel ja kui e-arvel on allahindluse info leitav ning kui lisatud info läbib kontrollid (nt rea summa miinus rea allahindlus peab võrduma e-arve SumBeforeVAT summaga).

<br><br>

**Osturea andmete säilitamise määrangud**

Väli | Valikud ning selgitus
|--|--|
**Säilita kirjeldus ning ühiku hind** | Sellest määratlusest sõltub, kas peale muudatust ostuarve rea väljadel Nr. või Asukoha tähis säilitatakse muudatuse eelne info väljadel: <br> Kirjeldus/Märkus, Mõõtühiku tähis, Otsene ühikukulu, Rea hinnaalandi summa <br><br> a) Ei (BC Standardloogika) - st toimib Business Centrali standardloogika ehk nt PR Konto muutmisel kustub info ülaloetletud väljadelt. <br> b) e-arve ridadel - st kui arverida on XML-ist loodud, siis nt PR Konto muutmisel ei kao info ülaloetletud väljadelt. <br> c) kõikidel ridadel - st vahet pole, kas arverida pärineb e-arvelt või on käsitsi sisestatud, igal juhul ei kao info ülaloetletud väljadelt, kui muudetakse real välja Nr. või Asukoha tähis. <br><br> **NB!** Kui on tehtud valik b) või c), siis lahendus ei luba muuta rea tüüpi *(nt PR Konto asemele panna Kaup)*. Soovides rea tüüpi muuta, tuleks esmalt luua uus rida soovitud andmetega ning seejärel e-arvelt tekkinud rida kustutada.
**Rea dimensioonide muutmise loogika** | Sellest määratlusest sõltub, kuidas peale muudatust ostuarve rea väljadel Nr., Projekti nr, Projekti ülesande nr. muutuvad rea dimensioonid. <br><br> a) Vaikedimensioonid (BC Standard) - st toimib nagu seni, ehk real olevad dimensioonid sõltuvad sellest millised vaikedimensioonid reale tulevad. <br> b) Küsi kasutajalt - st iga muudatusega ülalloetletud väljadel kontrollitakse, kas dimensioonikogumi ID on muutunud ning kui on, siis küsitakse kasutajalt, kas muuta dimensioonid vastavalt vaikedimensioonide väärtustele. Kui kasutaja vastab Jah, siis muutuvad dimensioonid nagu valikuga a) ning kui vastab Ei, siis dimensioonid ei muutu. <br> c) Säilita e-arve ridadel - st juhul kui arverida on XML-ist loodud, siis lahendus säilitab enne muudatuse tegemist real olnud dimensiooniväärtused.

<br>

## E-arvete saatmine

Kui soovite kliendile saata arveid e-arvena, avage kliendi kaart ning määrake vastav **Dokumendi saatmise profiil**.

Kui e-arve profiil puudub, avage **Dokumendi saatmise profiilid** ning kirjeldage uus profiil:

Väli | Väärtus / Selgitus
|--|--|
Tähis | "E-ARVE"
Kirjeldus | "E-arve"
Eesti e-arve | Valige oma operaator
Saada Eesti e-arve automaatselt | Konteeritud arve E-arve olek saab väärtuse "Ootab saatmist" ja saadetakse Tööjärjekorra tööga "Saada järjekorras müügiarved"
Finbite kättetoimetamisviis | Valige sobiv (vaikeväärtus tühi tähendab, et kanali otsustab Finbite)
Finbite arvehaldus | Kas müügiarve läheb kohe kliendile või esmalt Finbite arvehaldusesse (viimases tuleb siis manuaalselt müügiarve kliendile edasi saata).

<br>

E-arve saatmiseks kasutage arvel tegevust **Konteeri ja saada** või juba konteeritud arvel tegevust **Saada**. <br>
*Kui kliendile on määratud dokumendi saatmise profiil, kus aktiveeritud "Saada Eesti e-arve automaatselt", siis saadetakse e-arved tööjärjekorraga ka lihtsalt tegevust **Konteeri** kasutades.*

<br>

Saatmise oleku kohta annab infot konteeritud arve väli **E-arve olek**:

Väärtus | Selgitus
|--|--|
Ootab saatmist | Dokumenti ei ole veel ära saadetud aga seda teeb hiljem tööjärjekord (kui viimane on aktiveeritud).
Saatmistõrge | Dokumendi saatmisel tekkis tõrge.
Saadetud Finbite | Dokument on saadetud e-arve operaatorile Finbite.
Saadetud Unifiedpost | Dokument on saadetud e-arve operaatorile Unifiedpost.

Saatmata e-arveid saadab perioodiliselt tööjärjekorra töö „Saada järjek. müügiarved“.

Töö saadab arveid, mis vastavad järgnevatele tingimustele:

-   arve **E-arve olek** on „Ootab saatmist“ või „Saatmise tõrge“
-   kliendi **Dokumendi saatmise profiili** valik **Eesti e-arve** on täidetud.

Juhul, kui arve saatmisel on tõrge, mida ei ole võimalik lahendada, siis on soovitav peatada arve saatmiskatsed. Selleks klikkige arve väljal **E-arve olek**, mis avab andmevahetustegevuste logi. Logi sulgemisel saate valida, kas soovite saatmise peatada.

<br>

## Põhiandmete saatmine Finbite

Finbite arvehaldusesse on võimalik saata järgmised põhiandmed:
- **PR kontod**
- **Dimensioonid**
- **Hankijad ja kliendid**

Vastavates registrites tuleb märkida on väli **Saada Finbite** nendele kirjetele, mida soovite Finbite-i edastada.
<br>
Andmete saatmiseks ühekordselt avage **Finbite dokumendivahetusteenuse seadistus** ning käivitage Toimingud -> Põhiandmed alt vastav tegevus:
- **Saada PR kontod**
- **Saada dimensioonid**
- **Saada hankijad ja kliendid**

 Andmeid saadetakse perioodiliselt, kui teil on seadistatud ja töötavad vastavad tööjärjekorra kanded.

----------

Täpsema info saamiseks, palun võtke ühendust ühega partneritest:

[http://www.dynamicspartners.ee](http://www.dynamicspartners.ee/)
