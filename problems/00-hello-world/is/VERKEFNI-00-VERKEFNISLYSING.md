# Hello World

**Verkefni 00** · Einstaklingsverkefni · Áætlaður tími: 2–4 klst. · Engin reynsla krafist

> *Hugmynd og hönnun: Magnús Smári Smárason*
> *Alpha v1 — Til prófunar á fúsum tilraunakanínum*

> **Nafn nemanda:** ___________________________
>
> **Dagsetning hafin:** ___________________________
>
> **Gervigreind notuð:** ___________________________

---

## Þú

Þú hefur aldrei notað terminal. Þú hefur aldrei skrifað kóða. Þú veist kannski ekki hvað GitHub er. Það er alveg í lagi.

Þetta er ekki próf. Þetta er uppsetningarleiðbeining í búningi verkefnis. Þegar þú ert búin/n muntu hafa virkt þróunarumhverfi, GitHub reikning með fyrstu geymslunni þinni og fyrstu commit-ið þitt. Þú munt hafa gert þetta allt með gervigreind sem leiðsögumann.

Líttu á þetta sem æfingaborðið. Alvöru verkefnin hefjast á eftir.

---

## Staðan

Þú hefur skráð þig í nám sem krefst þess að þú vinnir með kóða, gögn og gervigreindarverkfæri. Áður en þú getur gert eitthvað af þessu þarftu að setja upp tölvuna þína.

Þetta hljómar leiðinlegt. Þetta er algengasta ástæðan fyrir því að fólk gefst upp á tæknilegri vinnu — það kemst ekki yfir uppsetninguna. Í dag breytir gervigreind þessu. Þú munt nota gervigreindaraðstoðara til að leiðbeina þér í hverju skrefi, og í lokin muntu hafa virka uppsetningu sem ber þig í gegnum restina af náminu.

Þú munt líka laga litla bilaða vefsíðu. Ekkert skelfilegt — bara nóg til að sanna að verkfærin virka og þú vitir hvernig á að nota þau.

---

## Hvað þú þarft

1. **Tölvu** (Mac, Windows eða Linux)
2. **Nettengingu**
3. **Gervigreindaraðstoðara** — allir þessir virka, allir eru með ókeypis aðgang:
   - [ChatGPT](https://chat.openai.com) (ókeypis aðgangur)
   - [Claude](https://claude.ai) (ókeypis aðgangur)
   - [Gemini](https://gemini.google.com) (ókeypis aðgangur)
   - [GitHub Copilot](https://github.com/features/copilot) (ókeypis fyrir nemendur)
   - Eða hvaða annan gervigreindaraðstoðara sem er

Það er allt. Allt annað setjum við upp saman.

---

## Skref 0: Kynntu þig fyrir gervigreindinni

Áður en þú setur upp nokkuð, skulum við ganga úr skugga um að þú og gervigreindin skilið hvort annað.

Opnaðu gervigreindaraðstoðarann þinn og skrifaðu nákvæmlega þetta:

> *"I am a university student with no programming experience. I need to set up my computer for software development. I am on [Mac/Windows/Linux]. I need to install: Git, Node.js, and Visual Studio Code. I also need to create a GitHub account. Please walk me through each step, one at a time, in plain language. After each step, I will tell you what happened before we move to the next one."*

**Skiptu út `[Mac/Windows/Linux]` fyrir stýrikerfið þitt.** Ef þú veist ekki hvaða stýrikerfi þú ert á, spurðu gervigreindina: *"How do I find out what operating system my computer is running?"*

Þetta er fyrsta samtal þitt við gervigreindina. Skráðu það í dagbókina neðst í þessu skjali.

### Fyrsta samtalið þitt

| Reitur | Þín færsla |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Virkaði þetta?** | |
| **Hvað ég lærði** | |

---

## Verkefnið þitt

### Áfangi 1: Settu upp verkfærin (60–90 mín.)

Fylgdu leiðbeiningum gervigreindarinnar til að setja upp þessi verkfæri. Eftir hvert og eitt, staðfestu að það virki.

#### 1. Visual Studio Code (VS Code)

VS Code er textaritill fyrir kóða. Hann er ókeypis og flestir þróunaraðilar í heiminum nota hann.

- Spurðu gervigreindina: *"How do I install Visual Studio Code on [stýrikerfið mitt]?"*
- Sæktu og settu upp
- Opnaðu hann. Þú ættir að sjá velkomsskjá.

**Staðfestu:** Opnaðu VS Code. Sérðu glugga með dökku þema og Welcome-flipa?

#### 2. Terminal

Terminal er textamiðað viðmót til að tala við tölvuna þína. Þú skrifar skipanir, hún gerir hlutina.

- **Mac:** Þú ert nú þegar með. Spurðu gervigreindina: *"How do I open the terminal on Mac?"* (Hún heitir Terminal og er í Applications > Utilities. VS Code er líka með innbyggðan terminal.)
- **Windows:** Spurðu gervigreindina: *"How do I set up Windows Terminal with WSL2?"* Þetta gefur þér Linux-umhverfi innan Windows, sem er svona sem atvinnuþróunaraðilar vinna á Windows.
- **Linux:** Þú ert nú þegar með. Spurðu gervigreindina: *"How do I open the terminal on [Linux-dreifing þín]?"*

**Staðfestu:** Opnaðu terminal. Skrifaðu `echo "hello"` og ýttu á Enter. Þú ættir að sjá `hello` prentast.

#### 3. Git

Git er verkfæri sem rekur breytingar á skrám. Hugsaðu um það sem "afturkalla-sögu" fyrir allt verkefnið þitt, deilt með heiminum.

- Spurðu gervigreindina: *"How do I install Git on [stýrikerfið mitt]?"*
- Eftir uppsetningu, stilltu:
  ```
  git config --global user.name "Nafnið þitt"
  git config --global user.email "netfangið.þitt@example.com"
  ```

**Staðfestu:** Í terminal, skrifaðu `git --version`. Þú ættir að sjá eitthvað á borð við `git version 2.43.0` (talan skiptir ekki máli, svo lengi sem hún sýnir útgáfunúmer).

#### 4. GitHub reikningur

GitHub er þar sem þróunaraðilar geyma og deila kóða. Hugsaðu um það sem "Google Drive fyrir kóða, með ofurkröftum."

- Farðu á [github.com](https://github.com) og búðu til ókeypis reikning
- **Mikilvægt:** Ef þú ert nemandi, sóttu um [GitHub Education pack](https://education.github.com/pack) — það gefur þér ókeypis aðgang að mörgum verkfærum þar á meðal GitHub Copilot

Eftir að hafa búið til reikninginn, settu upp GitHub CLI (skipanalínuverkfæri):

- Spurðu gervigreindina: *"How do I install and set up the GitHub CLI (gh) on [stýrikerfið mitt]?"*
- Auðkenndu þig síðan: `gh auth login` og fylgdu leiðbeiningunum

**Staðfestu:** Í terminal, skrifaðu `gh auth status`. Þú ættir að sjá notandanafnið þitt og að þú sért innskráð/ur.

#### 5. Node.js

Node.js gerir þér kleift að keyra JavaScript á tölvunni þinni (ekki bara í vafra). Mörg vefforrit nota það.

- Spurðu gervigreindina: *"What is the best way to install Node.js in 2026? Should I use nvm, fnm, or install it directly?"*
- Fylgdu ráðleggingum gervigreindarinnar. (Flestar munu mæla með `fnm` eða `nvm` — þessi leyfa þér að stjórna mörgum útgáfum auðveldlega.)
- Settu upp **Node.js 22** (núverandi LTS — Long Term Support — útgáfuna)

**Staðfestu:** Í terminal, skrifaðu `node --version`. Þú ættir að sjá `v22.x.x` (einhver útgáfa sem byrjar á 22). Skrifaðu líka `npm --version` — þú ættir að sjá útgáfunúmer.

#### Eftirlitsstaðan

Fylltu út þessa töflu til að staðfesta að allt virki:

| Verkfæri | Skipun til staðfestingar | Vænt úttak | Þín niðurstaða | Virkar? (J/N) |
|----------|--------------------------|------------|----------------|---------------|
| VS Code | Opna forritið | Velkomsskjár birtist | | |
| Terminal | `echo "hello"` | Prentar `hello` | | |
| Git | `git --version` | Útgáfunúmer | | |
| GitHub CLI | `gh auth status` | Notandanafn, innskráð/ur | | |
| Node.js | `node --version` | `v22.x.x` | | |
| npm | `npm --version` | Útgáfunúmer | | |

**Ef eitthvað virkar ekki:** Ekki örvænta. Afritaðu nákvæmlega villuskilaboðin og límdu þau til gervigreindarinnar: *"I tried [skipun] and got this error: [villa]. What's wrong and how do I fix it?"* Þetta er nákvæmlega svona sem þróunaraðilar leysa vandamál. Villuskilaboðin eru vísbendingar.

---

### Áfangi 2: Fyrsta geymslan þín (30–45 mín.)

Nú muntu búa til fyrsta verkefnið þitt og ýta því á GitHub.

#### 1. Náðu í byrjunarskrárnar

Byrjunarverkefnið er í `starter/` möppunni í þessu verkefni. Það inniheldur litla bilaða vefsíðu. Þitt hlutverk er að laga hana.

Afritaðu `starter/` möppuna í þitt eigið vinnusvæði:

```
cp -r starter/ ~/hello-world
cd ~/hello-world
```

Eða spurðu gervigreindina: *"How do I copy a folder to my home directory?"*

#### 2. Skoðaðu hvað þú ert með

Opnaðu `hello-world` möppuna í VS Code:

```
code ~/hello-world
```

Þú ættir að sjá þrjár skrár:
- `package.json` — lýsir verkefninu og pökkum þess
- `server.js` — þjónninn sem keyrir vefsíðuna
- `public/index.html` — vefsíðan sjálf

**Lestu hverja skrá.** Spurðu gervigreindina: *"Explain this file to me line by line: [límdu inn innihald skráarinnar]"*

#### 3. Reyndu að keyra

Í terminal (vertu viss um að þú sért í `hello-world` möppunni):

```
npm install
npm start
```

Opnaðu vafrann þinn og farðu á: `http://localhost:3000`

Eitthvað er að. Síðan lítur ekki rétt út. **Þetta er viljandi.**

#### 4. Finndu og lagaðu villurnar

Það eru nákvæmlega **3 litlar villur** í byrjunarskránum. Þetta eru ekki öryggisgallar eða flókin vandamál — þetta eru byrjendavillur sem gervigreindin þín getur hjálpað þér að finna og laga.

Spurðu gervigreindina: *"I'm running a simple Node.js web app. Here's my server.js: [límdu]. Here's my index.html: [límdu]. The page isn't working correctly. Can you spot what's wrong?"*

**Fyrir hverja villu sem þú finnur:**
1. Skildu hvað er að (spurðu gervigreindina)
2. Lagaðu hana
3. Staðfestu að lagfæringin virki (endurnýjaðu vafrann)
4. Vistaðu skrána

#### 5. Gerðu fyrstu commit-in þín

Eftir að hafa lagað hverja villu, vistaðu verkið þitt með git:

```
git init
git add .
git commit -m "fix: [lýstu hvað þú lagaðir]"
```

Spurðu gervigreindina: *"What does git init do? What does git add do? What does git commit do?"*

**Gerðu sér commit fyrir hverja lagfæringu.** Ekki eitt stórt commit í lokin. Þetta er venja sem þú munt nota alla námsleiðina.

#### 6. Ýttu á GitHub

Búðu til geymslu á GitHub og ýttu verkinu þínu:

```
gh repo create hello-world --public --source=. --push
```

Eða spurðu gervigreindina: *"How do I create a new GitHub repository and push my local code to it?"*

**Staðfestu:** Farðu á `github.com/[notandanafnið-þitt]/hello-world` í vafranum. Þú ættir að sjá skrárnar þínar og commit-sögu.

---

### Áfangi 3: Sannaðu að þetta virki (15–30 mín.)

Taktu skjáskot af eftirfarandi og hafðu þau með í skiluninni (eða lýstu hvað þú sérð):

1. **Terminal** sem sýnir `node --version` og `npm --version`
2. **Lagaða vefsíðuna** í gangi í vafranum á `localhost:3000`
3. **GitHub geymsluna þína** sem sýnir commit-in þín

---

## Reglur

### 1. Notaðu gervigreind í allt

Þú átt **að nota** gervigreind í hverju skrefi. Að spyrja "hvað er terminal?" er ekki heimsk spurning — þetta er verkefnið. Að spyrja "útskýrðu þessi villuskilaboð" er ekki svindl — þetta er svona sem maður lærir.

### 2. Haltu dagbók

Í hvert skipti sem þú spyrð gervigreindina eitthvað, skráðu það. Hvað þú spurðir, hvað hún sagði, hvort það hjálpaði. Þessi dagbók er mikilvægasti hluti skilunarinnar.

### 3. Gervigreindin mun hafa rangt fyrir sér

Jafnvel í einföldu uppsetningarverkefni getur gervigreindin gefið þér úreltar leiðbeiningar, rangar slóðir, eða skipanir sem virka ekki á þínu tiltekna kerfi. Þegar þetta gerist, skráðu það. Þetta er ekki mistök — þetta er námstækifæri.

### 4. Þú berð ábyrgðina

Ef gervigreindin leggur til eitthvað sem þú skilur ekki, biddu hana um útskýringu. Ekki afrita-líma skipanir í blindni í terminal án þess að vita hvað þær gera. Þú ert stjórnandinn.

### 5. Villuskilaboð eru vísbendingar, ekki veggiur

Sérhver villuskilaboð segja þér eitthvað ákveðið. Afritaðu þau. Límdu þau til gervigreindarinnar. Spurðu hvað þau þýða. Þetta er mikilvægasta villuleitarfærnin í allri hugbúnaðarþróun.

### 6. Enginn tímapressu

Þetta er uppsetningarverkefnið. Taktu þér þann tíma sem þú þarft. Ef eitthvað tekur 4 klukkustundir í stað 2, þá er það í lagi. Ef þú þarft að koma aftur á morgun, þá er það í lagi. Eina mistökin eru að klára ekki.

---

## Verkið þitt

### Uppsetningardagbók

> Skráðu hvað þú settir upp og hvaða vandamál komu upp.

| Skref | Verkfæri | Hvað gerðist | Vandamál? | Hvernig þú leystir þau |
|-------|----------|-------------|-----------|------------------------|
| 1 | VS Code | | | |
| 2 | Terminal | | | |
| 3 | Git | | | |
| 4 | GitHub + CLI | | | |
| 5 | Node.js | | | |

### Villuleiðréttingadagbók

> Skráðu villurnar 3 sem þú fannst og lagaðir.

| # | Hvað var að | Hvernig þú fannst hana | Hvernig þú lagaðir | Commit-skilaboð |
|---|------------|----------------------|--------------------|--------------------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

### Samskiptadagbók við gervigreind

> Skráðu mikilvæg samskipti þín við gervigreindina. Vertu heiðarleg/ur — ruglingslegu samskiptin eru dýrmætust.

#### Samskipti 1

| Reitur | Þín færsla |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti ég, eða hafnaði ég?** | |
| **Hvers vegna?** | |

#### Samskipti 2

| Reitur | Þín færsla |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti ég, eða hafnaði ég?** | |
| **Hvers vegna?** | |

#### Samskipti 3

| Reitur | Þín færsla |
|--------|-----------|
| **Hvað ég spurði** | |
| **Hvað gervigreindin sagði** (samantekt) | |
| **Notaði ég, breytti ég, eða hafnaði ég?** | |
| **Hvers vegna?** | |

*(Afritaðu þetta snið fyrir hvert mikilvægt samskipti. Stefndu á 5+ færslur.)*

### Ákvarðanadagbók

> Fyrir hverja ákvörðun sem þú tókst (jafnvel smáar), skráðu hana hér.

#### Ákvörðun 1

| Reitur | Þín færsla |
|--------|-----------|
| **Hver var ákvörðunin?** | |
| **Hvaða valkosti íhugaðir þú?** | |
| **Hvað mælti gervigreindin með?** | |
| **Hvað valdir þú og hvers vegna?** | |

*(Afritaðu þetta snið fyrir hverja ákvörðun. Stefndu á 3+ færslur.)*

### Þegar gervigreindin hafði rangt fyrir sér

> Jafnvel í einföldu verkefni getur gervigreindin gefið úreltar eða rangar leiðbeiningar. Skráðu slíkt hér.

| # | Hvað gervigreindin sagði | Hvers vegna það var rangt | Hvernig þú komst að því |
|---|-------------------------|--------------------------|-------------------------|
| 1 | | | |
| 2 | | | |

---

## Hvað þú skilar

1. **GitHub geymslu** (`hello-world`) með lögðum kóða og commit-sögu
2. **Þessari útfylltri verkefnislýsingu** með öllum dagbókum
3. **Skjáskotum** (eða lýsingum) af virku umhverfi
4. **Stuttri endurskoðun** (hér að neðan)

---

## Endurskoðun

> Skrifaðu 100–200 orð. Vertu heiðarleg/ur.

**Hvað var erfiðast við að setja upp umhverfið?**

> _______________________________________________________________
>
> _______________________________________________________________

**Hvar hjálpaði gervigreindin mest?**

> _______________________________________________________________
>
> _______________________________________________________________

**Var augnablik þar sem þú varst villtur/villt? Hvað gerðir þú?**

> _______________________________________________________________
>
> _______________________________________________________________

**Finnst þér þú vera tilbúin/n í stærri áskoranir?**

> _______________________________________________________________
>
> _______________________________________________________________

---

## Einkunnagjöf

| Viðmið | Vægi | Hvað við leitum að |
|--------|------|-------------------|
| **Virkt umhverfi** | 30% | Öll verkfæri uppsett og staðfest. Eftirlitstaðan er útfyllt. |
| **Lagað byrjunarverkefni** | 20% | Allar 3 villur fundnar og lagaðar. Vefsíðan virkar. |
| **Git og GitHub** | 20% | Geymsla til. Mörg commit (ekki eitt). Kóði á GitHub. |
| **Samskiptadagbók við gervigreind** | 20% | Heiðarleg, ítarleg dagbók yfir samskipti. Sýnir nám. |
| **Endurskoðun** | 10% | Ígrundað mat á upplifuninni. |

Athugið: **Samskiptadagbók við gervigreind** vegur jafn mikið og tæknilega verkið. Virkt umhverfi án dagbókar er minna virði en ruglingslegt umhverfi með ítarlegri, heiðarlegri dagbók um hvernig þú komst þangað.

---

## Vísbendingar

Þú færð þrjár. Hver ein er vísvitandi óljós — biddu gervigreindina um hjálp við að skilja hvað þær þýða.

1. **"Gervigreindin talar tungumál stýrikerfisins þíns."** — Segðu gervigreindinni alltaf hvaða stýrikerfi þú notar. Leiðbeiningar fyrir Mac, Windows og Linux eru oft algjörlega ólíkar. Ef gervigreindin gefur þér skipun sem virkar ekki gæti hún verið að gefa þér leiðbeiningar fyrir rangt kerfi.

2. **"Lestu villuna, ekki óttastu villuna."** — Þegar eitthvað mistekst segja villuskilaboðin næstum alltaf nákvæmlega hvað fór úrskeiðis. Afritaðu öll villuskilaboðin og límdu þau til gervigreindarinnar. Ekki reyna að draga saman sjálf/ur — smáatriðin skipta máli.

3. **"Villurnar þrjár eru ekki í felum."** — Villurnar í byrjunarverkefninu eru sýnilegar. Ein er í HTML, ein í þjóninum og ein í stillingunni. Þú þarft ekki að vera klár/klárt til að finna þær. Lestu bara kóðann vandlega (með gervigreindinni) og reyndu að skilja hvað hver lína gerir.

---

## Áður en þú byrjar

Opnaðu gervigreindaraðstoðarann þinn og skrifaðu:

> *"I am a complete beginner. I have never used a terminal or written code. I need to set up my computer for software development. I am on [Mac/Windows/Linux]. Can you walk me through installing Visual Studio Code, Git, Node.js, and the GitHub CLI? Please go one step at a time and wait for me to confirm each step works before moving on."*

Fylgdu svo leiðbeiningunum. Þegar eitthvað er óskiljanlegt, spurðu aftur. Þegar eitthvað bilar, límdu villuskilaboðin og spurðu hvað fór úrskeiðis.

Þú getur þetta.

---

## Athugasemd um gremju

Þetta er uppsetningarverkefni, en það þýðir ekki að það verði auðvelt. Uppsetning umhverfis er sannarlega einn erfiðasti hluti hugbúnaðarþróunar — ekki vegna þess að það er vitsmunalega erfitt, heldur vegna þess að sérhver tölva er aðeins öðruvísi og hlutirnir bila á ófyrirsjáanlegan hátt.

Ef þú eyðir 30 mínútum í að villuleita hvers vegna Node.js vill ekki setjast upp, þá er það ekki mistök. Þetta er fermingarathöfn sem allir þróunaraðilar hafa gengið í gegnum. Munurinn er sá að þú hefur gervigreind til að hjálpa þér.

Ef eitthvað tekur lengri tíma en búist var við, taktu hlé. Komdu aftur. Spurðu gervigreindina aftur með meiri smáatriðum. Þú munt komast í gegnum þetta.

Og þegar þú gerir — þegar terminal sýnir `v22.x.x` og kóðinn þinn er á GitHub og vefsíðan hleðst í vafranum — þá hefur þú gert eitthvað sem flestir gera aldrei. Þú hefur sett upp faglegt þróunarumhverfi frá grunni.

Restin af náminu byggir á þessu. Allt sem kemur á eftir gerir ráð fyrir að þú getir opnað terminal, keyrt skipun og ýtt á GitHub. Þetta verkefni gefur þér þann grunn.

Farðu.

---

*"Þegar gervigreind sér um verkin, verða mennirnir að eiga ákvarðanirnar."*
*— Agentic Resilience Manifesto*
