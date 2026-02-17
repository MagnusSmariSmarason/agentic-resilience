# Forritarinn sem hvarf

**Verkefni 01** · Einstaklingsverkefni · Áætlaður tími 6–10 klukkustundir · Engin reynsla af forritun nauðsynleg

> *Hugmynd og hönnun: Magnús Smári Smárason*
> *Alpha útgáfa 1 — Til prófunar á fúsum fólki*

> **Nafn nemanda:** ___________________________
>
> **Upphafsdagsetning:** ___________________________
>
> **Gervigreindaraðstoð sem notuð var:** ___________________________

---

## Þú

Þú hefur aldrei skrifað línu af kóða. Þú veist ekki hvað „server" er. Þú veist ekki hvað „Node.js" þýðir. Það er í lagi. Það er einmitt tilgangurinn.

Þú hefur eitthvað betra en reynslu: þú hefur aðgang að gervigreind.

Þetta er ekki forritunarnámskeið. Þetta er próf á því hvort þú getir **notað gervigreind til aðleysa raunverulegt vandamál sem þú skilur ekki ennþá**. Gervigreindin verður kennari þinn, samstarfsfélagi þinn og verkfæri þitt. En hún mun líka stundum hafa rangt fyrir sér og mun ekki alltaf vita hvað skiptir máli. Þú munt læra að greina muninn.

---

## Aðstæðurnar

**Sigga Björnsdóttir** rekur **Sky Tours ehf.**, lítið ferðaþjónustufyrirtæki á Húsavík á Íslandi — hvalaskoðun, norðurljós, jöklar.

Forritari þeirra, **Jón**, byggði upp allt bókunarkerfi fyrirtækisins. Síðasta þriðjudag sendi Jón þennan tölvupóst:

> *„Ég get ekki lengur gert þetta. Kóðinn er í repo-inu. Fyrirgefðu vegna bókunar-CSV-skrárinnar. Gangi þér vel."*
>
> *— Jón*

Síminn hans er slökkt. Hann er horfinn. Ferðamannatímabilið hefst eftir 8 vikur.

Sigga hringdi í þig. Hún er í uppnámi. Hér er allt sem hún sagði þér:

> *„Viðskiptavinalistinn er skrítin — sum nöfn vantar og ég held að það séu tvítekningar. Síða 1 af viðskiptavinayfirlitinu er alltaf tóm, þú verður að smella á síðu 2. Bókanirnar birtast alls ekki síðan Jón breytti einhverju í síðasta mánuði. Aha, og einhver þýskur ferðamaður komst að því hvernig á að fá ókeypis ferðir með kóða — ég veit ekki hvernig á að slökkva á því. Líka er þetta hægt. Og frændi Jóns, Bjarki, sagði eitthvað um að 'leitin væri hættuleg' en ég veit ekki hvað hann átti við."*

Þetta er allt sem þú færð. Afganginn verður þú að átta þig á.

---

## Það sem þú þarft

1. **Tölvu** (Mac, Windows eða Linux)
2. **GitHub aðgang** (ókeypis — búðu til aðgang á github.com ef þú átt ekki slíkan)
3. **Gervigreindaraðstoð** — eitthvað af þessu virkar, öll með ókeypis möguleika:
   - [ChatGPT](https://chat.openai.com) (ókeypis útgáfa)
   - [Claude](https://claude.ai) (ókeypis útgáfa)
   - [Gemini](https://gemini.google.com) (ókeypis útgáfa)
   - [GitHub Copilot](https://github.com/features/copilot) (ókeypis fyrir nemendur)
   - Eða önnur gervigreindaraðstoð fyrir forritun

Það er allt. Engar kennslubækur. Engar leiðbeiningar. Enginn kennari sem fer með þig í gegnum það. Bara þú og gervigreindin þín.

**Geymslan:** https://github.com/MagnusSmariSmarason/skycrm

---

## Skref 0: Er þessi geymsla örugg?

**Áður en þú klónar neitt** berð þú ábyrgð. Jón hvarf. Þú hefur enga hugmynd um hvað er í þessum kóðagrunni. Hann gæti innihaldið spilliforrit, skilríkjaþjófa eða uppsetningarskriftur sem keyra sjálfkrafa.

Þetta er fyrsta afurð þín:

**Skrifaðu öryggisúttekt á geymslu** (1 síða). Áður en þú sækir eina einustu skrá á tölvuna þína skaltu meta geymsluna. Biddu gervigreindina þína um að hjálpa þér að svara:

- Hvaða skrár eru í geymslu? Geturðu lesið þær á GitHub án þess að klóna?
- Inniheldur `package.json` einhverjar grunsamlegar `preinstall` eða `postinstall` skriftur?
- Eru einhverjar skriftur sem keyra sjálfkrafa þegar þú keyrir `npm install`?
- Eru skrár sem ættu ekki að vera í kóðageymslu (tvíundarskrár, keyranlegar skrár, `.env` skrár með raunverulegum leyndarmálum)?
- Hvað segir `.gitignore` þér um það sem forritarinn taldi viðkvæmt?
- Hvað virðist kóðinn gera út frá sjónrænni skoðun?

**Skráðu niður það sem þú fannst.** Skrifaðu hvað þú athugaðir, hvað þú fannst og niðurstöðu þína: er öruggt að klóna og setja upp? Þetta er hvernig fagfólk metur óþekkta kóðagrunna. Ef þú sleppir þessu skrefi hefur þú þegar fallið á fyrstu raunverulegu prófinu.

Aðeins eftir öryggisúttekt þína ættir þú að halda áfram að klóna.

### Öryggisúttekt þín

> **Ljúktu við þennan hluta ÁÐUR EN þú klónar geymsluna.**

| Athugun | Niðurstaða þín | Öruggt? (J/N) |
|---------|----------------|---------------|
| Skrár sýnilegar á GitHub án þess að klóna | | |
| `package.json` — einhverjar `preinstall`/`postinstall` skriftur? | | |
| Einhverjar sjálfkeyrandi skriftur við `npm install`? | | |
| Skrár sem ættu ekki að vera í geymslu (tvíundarskrár, leyndarmál, `.env`)? | | |
| Hvað `.gitignore` leiðir í ljós um öryggismeðvitund forritunar | | |
| Sjónræn skoðun á kóða — hvað virðist hann gera? | | |

**Heildarniðurstaða — öruggt að klóna?**

> _Svar þitt:_ ___________________________
>
> _Rökstuðningur (2-3 setningar):_
>
> _______________________________________________________________
>
> _______________________________________________________________

---

## Verkefni þitt

### Vinnuflæðið

Þetta er hvernig faglegir forritarar vinna. Biddu gervigreindina þína um að útskýra hvert skref ef þú skilur það ekki.

1. **Fork-aðu** upprunalega `skycrm` geymsluna yfir á þinn eigin GitHub aðgang
2. **Klónaðu** fork-ið þitt á tölvuna þína
3. **Búðu til greinar** fyrir hverja lagfæringu: `fix/security-search-injection`, `fix/pagination-off-by-one`, o.s.frv.
4. **Vinnaðu í litlum commit-um** — hver commit ætti að gera eitt. Engir „lokacommit" risastórir urðningar.
5. **Opnaðu Pull Request** aftur inn í `main` grein fork-sins þíns
6. **CI verður að standast** áður en þú sameinaðir. Geymslan hefur GitHub Actions vinnuflæði — kóðinn þinn verður að standast linting, próf, öryggisathuganir og byggingu.
7. **Merktu innsendinguna þína**: `submission-v1`

Ef þú veist ekki hvað eitthvað af þessum orðum þýða er það eðlilegt. Spurðu gervigreindina þína: *„Hvað er fork á GitHub? Hvernig bý ég slíkan til?"*

### Afurðirnar

**Fáðu það til að keyra. Finndu hvað er rangt. Lagaðu það. Prófaðu það. Skráðu það. Afhenddu það.**

1. **Fáðu forritið til að keyra á tölvunni þinni.** Þú þarft að setja upp verkfæri sem þú hefur aldrei heyrt um. Spurðu gervigreindina þína hvernig.

2. **Finndu öll vandamál.** Það eru villur, öryggisveikleikar og gæðavandamál með gögnin. Mörg þeirra. Sigga sagði þér frá sumum. Afgangurinn felur sig. Búðu til forgangsraðaðan lista — hvað er hættulegt, hvað er bilað, hvað er ljótt?

3. **Lagaðu það sem skiptir máli — og sannaðu að það virki.** Lagfæring án prófs er þefja, ekki verkfræði. Fyrir hverja villu sem þú lagar skaltu skrifa próf sem sannar að lagfæringin virkar. Spurðu gervigreindina þína: *„Hvernig skrifa ég próf fyrir þetta?"* CI leiðslan mun keyra prófin þín sjálfkrafa — ef þau falla getur PR-ið þitt ekki sameinast.

4. **Skrifaðu skjölun.** Þegar þú ert búin/n á algjörlega ókunnugur einstaklingur að geta lesið skjölunina þína, sett upp verkefnið og skilið hvernig það virkar — án þess að tala við þig. Þetta kallast **Strætisvagnaprófið**: ef þú færð á þig strætisvagn á morgun, getur einhver annar tekið við?

5. **Sendu inn verkið þitt** sem GitHub geymslu með CI/CD að standast í grænu.

---

## Reglur

### 1. Notaðu gervigreind fyrir allt

Þess er **vænst** að þú notir gervigreind til að hjálpa þér með hvert skref í þessari verkefni. Að spyrja gervigreindina þína „hvað er Node.js og hvernig set ég það upp?" er ekki svindl — það er verkefnið. Að spyrja „útskýrðu þennan kóða fyrir mér línu fyrir línu" er ekki svindl — það er hvernig þú lærir.

**En þú verður að skilja hvað gervigreindin segir þér.** Ef hún stingur upp á lagfæringu ættir þú að geta útskýrt *af hverju* hún virkar. Ef þú getur ekki útskýrt það skilur þú það ekki ennþá. Spurðu fleiri spurninga.

### 2. Haltu skrá

Í hvert sinn sem þú spyrð gervigreindina þína um eitthvað mikilvægt skaltu skrifa það niður.

Skráðu:
- Hvað þú spurðir
- Hvað gervigreindin sagði
- Hvort þú notaðir, breyttir eða hafnaðir tillögunni
- **Af hverju** — ein setning er nóg

Þessi skrá er ekki gagnslaust verk. Hún er aðalsönnun náms þíns. Fullkomin lokaafurð án skrár er minna virði en óreiðuleg afurð með ítarlegri skrá.

### 3. Gervigreindin mun hafa rangt fyrir sér

Þetta er vissa, ekki möguleiki. Gervigreindin mun missa af villum. Hún mun stinga upp á lagfæringum sem brjóta annað. Hún mun fullvissulega segja þér að eitthvað sé öruggt þegar það er það ekki. Hún mun ekki skilja viðskipti Siggu.

Verk þitt er að grípa það sem gervigreindin missir af. Þegar þú gerir það skaltu skrifa það niður. Þegar þú grípur það ekki í tæka tíð skaltu skrifa það líka niður. Hvort tveggja er dýrmætt.

### 4. Þú átt ákvarðanirnar

Ef lokaafurðin hefur öryggisop er „en ChatGPT sagði að það væri í lagi" ekki vörn. Þú ert sá/sú sem ber ábyrgð. Gervigreindin er verkfærið. Þú ert notandinn.

### 5. Lagfæring án prófs er þefja

Þegar þú lagar villu verður þú líka að skrifa próf sem sannar að lagfæringin virkar. „Það lítur rétt út" er ekki staðfesting. Próf er það. Biddu gervigreindina þína um að hjálpa þér að skrifa próf — en skildu hvað prófið er að athuga og af hverju. CI leiðslan (`npm test`) mun keyra prófin þín sjálfkrafa. Ef þau falla geta breytingarnar þínar ekki sameinast.

### 6. CI verður að vera grænt

Geymslan inniheldur GitHub Actions vinnuflæði sem keyra sjálfkrafa við hverja push og pull request. Kóðinn þinn verður að standast:
- `npm test` — prófin þín verða að standast
- `npm audit` — engir alvarlegir öryggisveikleikar í dependency
- CodeQL — sjálfvirka öryggisskönnun

Ef eitthvað af þessu fellur er PR-ið þitt lokað. Þetta er hvernig raunveruleg hugbúnaðarteymi vinna. Biddu gervigreindina þína um að hjálpa þér að skilja villuboðin.

---

## Verk þitt

### Vandamálafinnsluskrá

> Listaðu öll vandamál sem þú finnur. Forgangsraðaðu: **Gagnrýnið** (öryggi/gagnatap), **Hátt** (bilaðir eiginleikar), **Miðlungs** (villur), **Lágt** (útlit/afköst).

| # | Lýsing á vandamáli | Forgangur | Hvernig þú fannst það | Staða |
|---|-------------------|-----------|----------------------|-------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |
| 10 | | | | |

*(Bættu við fleiri línum eftir þörfum)*

### Gervigreindsamskiptaskrá

> Skráðu mikilvæg samskipti þín við gervigreindina hér. Vertu heiðarlegur/heiðarleg — óreiðuleg samskipti eru verðmætustu.

#### Samskipti 1

| Reitur | Færsla þín |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti eða hafnaði því?** | |
| **Af hverju?** | |

#### Samskipti 2

| Reitur | Færsla þín |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti eða hafnaði því?** | |
| **Af hverju?** | |

#### Samskipti 3

| Reitur | Færsla þín |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti eða hafnaði því?** | |
| **Af hverju?** | |

*(Afritaðu þetta sniðmát fyrir hverja mikilvæga samskipti. Stefndu að 10+ færslum.)*

### Ákvörðunardagbók

> Fyrir hverja mikilvæga ákvörðun sem þú tókst skaltu skrá hana hér.

#### Ákvörðun 1

| Reitur | Færsla þín |
|--------|-----------|
| **Hver var ákvörðunin?** | |
| **Hvaða valkosti íhugaðir þú?** | |
| **Hvað mælti gervigreindin með?** | |
| **Hvað valdir þú og af hverju?** | |
| **Hvað gerðist?** | |

#### Ákvörðun 2

| Reitur | Færsla þín |
|--------|-----------|
| **Hver var ákvörðunin?** | |
| **Hvaða valkosti íhugaðir þú?** | |
| **Hvað mælti gervigreindin með?** | |
| **Hvað valdir þú og af hverju?** | |
| **Hvað gerðist?** | |

*(Afritaðu þetta sniðmát fyrir hverja lykilákvörðun. Stefndu að 5+ færslum.)*

### Öryggisniðurstöður

> Skráðu öll öryggismál sem þú uppgötvaðir.

| # | Veikleiki | Alvarleiki | Skrá og lína | Hvað gæti farið úrskeiðis? | Lagfært? | Hvernig? |
|---|----------|-----------|-------------|--------------------------|---------|---------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |

### Lagfæringamælir

> Fyrir hverja lagfæringu skaltu tengja greinina, PR og prófið.

| # | Hvað þú lagaðir | Nafn greinar | PR # | Prófskrá | CI grænt? |
|---|----------------|-------------|------|---------|----------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |

### Skipti sem gervigreindin hafði rangt fyrir sér

> Þessi hluti er virði auka einkunna. Að grípa mistök gervigreindar sýnir alvöru dómgreind.

| # | Hvað gervigreindin sagði | Af hverju það var rangt | Hvernig þú grípst það | Hvað gerðir þú í staðinn |
|---|-------------------------|------------------------|----------------------|-------------------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

---

## Það sem þú sendir inn

**GitHub geymslu** (fork-ið þitt) sem inniheldur:

1. **Lagfærði kóðagrunninn** — með mörgum litlum commit-um sem sýna ferlið þitt, á feature greinum sameinuðum í gegnum PR
2. **CI/CD að standast** — öll GitHub Actions vinnuflæði græn á `main`
3. **Öryggisúttekt geymslu** — mat þitt á geymslu *áður en* þú klónaðir hana (Skref 0 hér að ofan)
4. **README.md** — sem stenst strætisvagnaprófið
5. **Þessa útfylltu verkefnislýsingu** — með öllum hlutum útfylltum
6. **SECURITY.md** — hvaða öryggismál þú fannst, hvað þú lagaðir, hvað eftir stendur
7. **Próf** — fyrir hverja lagfæringu, próf sem sannar að það virkar
8. **Aftursýn** (hér að neðan)

**Innsending:** Merktu lokastöðu þína sem `submission-v1` og gefðu upp slóð fork-sins þíns.

> **Slóð fork-sins þíns:** ___________________________

---

## Aftursýn

> Skrifaðu 300–500 orð. Vertu heiðarlegur/heiðarleg.

**Hvað var erfiðara en búist var við?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Hvar hjálpaði gervigreindin mest?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Hvar brást gervigreindin þér?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Hvað veist þú núna sem þú vissir ekki þegar þú byrjaðir?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

**Ef þú þyrftir að gera þetta aftur, hvað myndir þú gera öðruvísi?**

> _______________________________________________________________
>
> _______________________________________________________________
>
> _______________________________________________________________

---

## Mat

| Viðmið | Vægi | Það sem við leitum að |
|--------|------|--------------------|
| **Öryggi** | 20% | Fannstu og lokaðiru gagnrýnu veikleikana? Skildir þú *af hverju* þeir voru hættulegir? Var öryggisúttektin þín ítarleg? |
| **Skjölun** | 20% | Getur ókunnugur einstaklingur sett upp og skilið verkefnið út frá skjölunum þínum einum? |
| **Dómgreind og ferli** | 25% | Forgangsraðaðir þú skynsamlega? Er gervigreindaskráin þín heiðarleg og ítarleg? Grípstu mistök gervigreindar? Er öryggisúttektin þín hugsuð? |
| **Virkni og próf** | 20% | Virka kjarnaeiginleikarnir? Hefur hver lagfæring próf? Stenst CI? |
| **Gæði gagna** | 5% | Eru gögnin hreinsuð og staðfest? |
| **Git hreinlæti** | 10% | Litlir efnisbundnir commit? Feature greinar? PR? Öryggislagfæringar lenda snemma? Commit skilaboð eru skýr? |

Athugaðu: **Dómgreind og ferli** er viðmiðið með mesta vægi. Vel íhuguð, vel skjöluð tilraun sem lagar ekki allt mun skora hærra en fullkomin lagfæring án skráar og án rökstuðnings.

### Það sem við metum út frá git sögunni þinni

- Litlir, efnisbundnir commit (hver með skýra ætlun)
- Öryggislagfæringar lenda snemma (dómgreind um forgang)
- Próf bætt við samhliða lagfæringum (ekki kramin í endann)
- Commit skilaboð nota skýrar venjur: `fix:`, `security:`, `docs:`, `test:`
- Afturköllun er útskýrð (þroski)
- Skjöl þróast með kerfinu (README/SECURITY uppfærð um leið og þú heldur áfram, ekki allt í lokin)

---

## Vísbendingar

Þú færð þrjár. Notaðu þær skynsamlega. Hver einasta er vísvitandi óljós — biddu gervigreindina þína um að hjálpa þér að skilja hvað þær þýða.

1. **„Jón skildi lykilana undir dyraþrepinu."** — Skoðaðu frumkóðann. Sumt sem ætti að vera leyndarmál er það ekki.

2. **„Aldrei treysta inntaki notenda."** — Það eru staðir í þessum kóða þar sem hvað sem notandi slær inn er keyrt beint. Þetta er afar hættulegt. Spurðu gervigreindina þína um `eval()`.

3. **„Gögnin ljúga."** — Viðskiptavinalisti, bókunarskrá og ferðabirgðir innihalda allt villur. Sumar eru augljósar. Sumar eru lúmskar. Ekki treysta neinum tölum fyrr en þú hefur staðfest þær.

---

## Áður en þú byrjar

Þú veist líklega ekki hvernig á að gera neitt af þessu ennþá. Það er eðlilegt. Hér er fyrsta skrefið þitt:

Opnaðu gervigreindaraðstoðina þína og skrifaðu:

> *„Mér hefur verið gefin GitHub geymsla sem inniheldur Node.js verkefni sem heitir SkyCRM. Áður en ég klóna hana á tölvuna mína þarf ég að meta hvort hún sé örugg. Ég hef aldrei forritað áður. Hvernig skoða ég geymslu á GitHub án þess að hlaða henni niður? Hvað ætti ég að leita að til að ákvarða hvort öruggt sé að klóna og setja upp?"*

Eftir öryggisúttektina þína ætti önnur fyrirspurnin þín að vera:

> *„Ég hef ákveðið að geymsluna sé öruggt að vinna með. Ég þarf að fork-a hana, klóna hana og fá hana til að keyra á tölvunni minni. Ég er á [Mac/Windows/Linux] og hef aldrei notað terminal áður. Farðu með mig í gegnum allt, skref fyrir skref."*

Fylgdu svo leidbeiningum. Þegar eitthvað er óljóst skaltu spyrja aftur. Þegar eitthvað bilar skaltu líma villuboðin og spyrja hvað fór úrskeiðis.

Þannig virkar allt verkefnið. Þú spyrð. Þú lærir. Þú ákveður. Þú gerir.

---

## Athugasemd um vonbrigði

Þetta mun vera pirrandi. Þú munt lenda í veggjum. Hlutirnir munu bila. Villuboð munu vera óskiljanlegt. Þú munt laga eitt og brjóta annað. CI mun verða rautt. Próf munu falla.

Það er ekki bilun í æfingunni. Það er æfingin.

Raunveruleg vandamál koma ekki með skref-fyrir-skref leiðbeiningar. Raunveruleg gervigreindarverkfæri gefa ekki alltaf rétt svör. Færnin sem þú ert að byggja upp hér — getan til að sigla um óvissu með gervigreind sem félaga þinn — er færnin sem skiptir máli.

Taktu hlé. Biddu um hjálp þegar þú ert fastur/föst (frá gervigreind eða samnemendum). En gefðu ekki upp.

Sigga treystir á þig. Ferðamennirnir koma eftir 8 vikur.

Áfram.

---

*„Þegar gervigreind sér um að gera hlutina verða manneskjur að eiga ákvarðanirnar."*
*— Agentic Resilience Manifesto*

*"When AI handles the doing, humans must own the deciding."*
*— Agentic Resilience Manifesto*
