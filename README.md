# Latentti GPTs - Käyttöohje

**Versio:** 4.0
**Päivitetty:** 20.12.2025
**Tekijä:** Ari Hietamäki / Latentti.fi

---

## Mikä on Custom GPT?

Custom GPT on OpenAI:n ChatGPT:ssä räätälöity AI-assistentti, jolla on:
- Oma rooli ja asiantuntemus (esim. strategiakonsultti, talousanalyytikko)
- Valmiit viitekehykset ja metodit
- Johdonmukainen tyyli kaikissa keskusteluissa
- **Erikoisominaisuudet:** Web-haku, koodin suoritus, kuvien luonti, tiedostot

**Hyöty:** Saat asiantuntija-avun ilman, että sinun tarvitsee selittää kontekstia joka kerta uudelleen.

---

## Kansiorakenne

```
Latentti GPTs/
├── README.md                              ← Tämä ohje
├── Business-Strategy-Consultant-GPT.md    ← GPT:n määrittelyt
├── Financial-Analyst-GPT.md
├── HR-Advisor-GPT.md
├── Marketing-Strategist-GPT.md
├── Executive-Command-Center-GPT.md        ← UUSI: Johtoryhmä-GPT
└── Knowledge/                             ← Ladattavat tietokannat
    ├── Business-Strategy-Frameworks-KB.md
    ├── Financial-Analysis-Toolkit-KB.md
    ├── HR-Finnish-Employment-Law-KB.md
    ├── Marketing-Metrics-Benchmarks-KB.md
    └── Executive-Leadership-KB.md         ← UUSI: Johtoryhmän viitekehykset
```

**Rakenne selitettynä:**
- **GPT.md-tiedostot:** Sisältävät Instructions-osion (< 8000 merkkiä), joka kopioidaan ChatGPT:hen
- **Knowledge/-kansio:** Sisältävät yksityiskohtaiset tietokannat, jotka ladataan GPT:n Knowledge-osioon

---

## Saatavilla olevat GPT:t

| GPT | Instructions | Knowledge-tiedosto | Käyttötarkoitus |
|-----|--------------|-------------------|-----------------|
| **Business Strategy Consultant** | 3 629 merkkiä | `Business-Strategy-Frameworks-KB.md` | Strateginen suunnittelu, kilpailija-analyysi, SWOT, Porter's Five Forces |
| **Financial Analyst** | 3 939 merkkiä | `Financial-Analysis-Toolkit-KB.md` | Talousennusteet, arvonmääritys, unit economics, ROI-analyysi |
| **HR Advisor** | 3 940 merkkiä | `HR-Finnish-Employment-Law-KB.md` | Henkilöstöstrategia, suorituksen johtaminen, työlainsäädäntö, TES |
| **Marketing Strategist** | 4 460 merkkiä | `Marketing-Metrics-Benchmarks-KB.md` | Go-to-market, growth hacking, brand positioning, AARRR-metriikat |
| **Executive Command Center** | ~7 000 merkkiä | `Executive-Leadership-KB.md` | **Johtoryhmän komentokeskus** - päätöksenteko, toteutusseuranta, hallitustyö |

**Huom:** Kaikki Instructions-osiot ovat alle ChatGPT:n 8 000 merkin rajan.

---

## GPT-hierarkia ja käyttötarkoitukset

```
┌─────────────────────────────────────────────────────────────────┐
│                 EXECUTIVE COMMAND CENTER                        │
│     Johtoryhmän strateginen komentokeskus                       │
│  • Orkestrointi   • Päätöksenteko   • Toteutusseuranta          │
│  • Hallitustyö    • Sidosryhmäviestintä                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐           │
│  │  STRATEGY    │  │   FINANCE    │  │      HR      │           │
│  │  Consultant  │  │   Analyst    │  │   Advisor    │           │
│  │              │  │              │  │              │           │
│  │ • SWOT       │  │ • DCF        │  │ • Työlaki    │           │
│  │ • Porter     │  │ • Unit econ  │  │ • OKR        │           │
│  │ • Blue Ocean │  │ • Budjetit   │  │ • TES        │           │
│  └──────────────┘  └──────────────┘  └──────────────┘           │
│                                                                  │
│  ┌──────────────┐                                               │
│  │  MARKETING   │                                               │
│  │  Strategist  │                                               │
│  │              │                                               │
│  │ • GTM        │                                               │
│  │ • AARRR      │                                               │
│  │ • Kampanjat  │                                               │
│  └──────────────┘                                               │
└─────────────────────────────────────────────────────────────────┘
```

**Käyttöperiaate:**
- **Funktionaalinen asiantuntijatyö** → Käytä erikoistuneita GPT:itä (Strategy, Finance, HR, Marketing)
- **Johtoryhmätason päätöksenteko** → Käytä Executive Command Center -GPT:tä

---

## UUSI: Executive Command Center - Johtoryhmän GPT

### Miksi erillinen johtoryhmä-GPT?

**Ongelma:** 70% strategisista päätöksistä epäonnistuu toteutuksessa (McKinsey). Suurin syy on **Execution Gap** - päätökset tehdään, mutta ne eivät muutu teoiksi.

**Ratkaisu:** Executive Command Center -GPT on suunniteltu ratkaisemaan tämä ongelma:

| Perinteiset GPT:t | Executive Command Center |
|-------------------|--------------------------|
| Yksi funktio | Koko liiketoiminta holistisesti |
| Syväanalyysit | Executive summaries (max 1-2 sivua) |
| Päätöksenteon tuki | **Päätöksenteko + Toteutuksen seuranta** |
| Operatiivinen fokus | Strateginen ja governance-fokus |

### Neljä ydintoimintoa

| # | Moottori | Mitä tekee |
|---|----------|------------|
| 1 | **Decision Engine** | Päätösvalmistelut, trade-off -analyysit, skenaariot |
| 2 | **Execution Engine** | Päätösrekisteri, seuranta, vastuuttaminen, eskalaatiot |
| 3 | **Communication Engine** | Sama päätös eri yleisöille (hallitus, keskijohto, henkilöstö) |
| 4 | **Governance Engine** | Hallitusraportit, CEO/CFO-esitykset, riskikartta |

### Kenelle sopii?

| Organisaatio | Sopivuus | Huomiot |
|--------------|----------|---------|
| **Keskisuuri (50-250 hlö)** | Erinomainen | Sparrauskumppani, ketteryyttä |
| **Suuri (250+ hlö)** | Erinomainen | Tiedon aggregointi, governance |
| **Pieni (<50 hlö)** | Osittain | Voi olla liian raskas, käytä funktionaalisia GPT:itä |

---

## Johtoryhmä-GPT:n käyttöopas

### Vaihe 1: Valmistelu (ennen GPT:n luomista)

Kerää nämä dokumentit valmiiksi:

| # | Dokumentti | Miksi tärkeä | Esimerkki |
|---|------------|--------------|-----------|
| 1 | **Strategiadokumentti** | GPT linjaa kaiken strategiaan | 3-5 vuoden strategia, visio, missio |
| 2 | **Päätösrekisteri** | Seuranta ja jatkuvuus | Excel aiemmista johtoryhmän päätöksistä |
| 3 | **Budjetti & KPI:t** | Resurssikonteksti | Vuosibudjetti, tavoitteet |
| 4 | **Organisaatiokaavio** | Vastuuttaminen | Kuka vastaa mistäkin |
| 5 | **Hallituksen päätökset** | Governance-linjaukset | Viimeisimmät hallituspäätökset |

**Vinkki:** Jos päätösrekisteriä ei ole, luo se nyt! Käytä Knowledge-tiedoston mallia.

### Vaihe 2: GPT:n asennus

1. Seuraa normaalia asennusohjetta (alla)
2. Lataa Knowledge-tiedostot:
   - `Executive-Leadership-KB.md` (viitekehykset)
   - Omat yritysdokumentit (yllä listatut)
3. Ota käyttöön: Web Browsing + Code Interpreter

### Vaihe 3: Käyttöönotto johtoryhmässä

#### Ensimmäinen kokous: Esittely ja käyttöönotto

**Agenda:**
1. Miksi olemme ottamassa tämän käyttöön (Execution Gap -ongelma)
2. Mitä GPT tekee ja mitä ei
3. Päätösrekisterin käyttöönotto
4. Pelisäännöt

**Pelisäännöt (esimerkkejä):**
- Jokainen strateginen päätös rekisteröidään
- Jokaisella päätöksellä on henkilökohtainen omistaja (ei "johtoryhmä")
- Status päivitetään joka kokouksessa
- GPT:tä käytetään kokousten valmisteluun

#### Jatkuva käyttö: Tyypillinen viikko

| Päivä | Käyttötapa | Esimerkki |
|-------|------------|-----------|
| **Ma** | Viikon valmistelu | "Listaa tämän viikon päätösten statukset" |
| **Ti-To** | Ad hoc -analyysit | "Analysoi vaihtoehto A vs. B" |
| **Pe** | Jory-kokous valmistelu | "Valmistele maanantain jory-kokouksen agenda" |
| **Jory** | Reaaliaikainen tuki | "Rekisteröi tämä päätös: X, omistaja: Y" |
| **Jälkeen** | Seuranta | "Lähetä päätösten yhteenveto keskijohdolle" |

### Vaihe 4: Tyypilliset käyttötapaukset

#### A) Päätöksenteko

```
Käyttäjä: "Analysoi vaihtoehdot: pysymmekö nykymarkkinoilla vai
         laajennummeko Ruotsiin"

GPT tekee:
1. Executive summary tilannekuvasta
2. Trade-off -analyysi (hyödyt/haitat molemmissa)
3. Skenaarioanalyysi (Base/Bull/Bear)
4. Riskiarvio
5. Suositus perusteluineen
6. Päätöksen rekisteröintilomake
```

#### B) Toteutuksen seuranta

```
Käyttäjä: "Mitä Q4:lle päätettyjä toimenpiteitä on yhä kesken?"

GPT tekee:
1. Hakee päätösrekisteristä Q4:n päätökset
2. Listaa kesken olevat (Vihreä/Keltainen/Punainen)
3. Tunnistaa myöhässä olevat
4. Ehdottaa eskalaatiotoimenpiteitä
5. Päivittää dashboardin
```

#### C) Hallitusraportointi

```
Käyttäjä: "Valmistele Q3-kvartaalikatsaus hallitukselle"

GPT tekee:
1. CEO:n tilanneyhteenveto (1 sivu)
2. Talousluvut vs. budjetti (1 sivu)
3. Strategisten aloitteiden status (1 sivu)
4. Top-riskit ja toimenpiteet
5. Päätösesitykset (jos on)
```

#### D) Sidosryhmäviestintä

```
Käyttäjä: "Sama päätös kolmelle yleisölle: hallitus, keskijohto, henkilöstö"

GPT tekee:
1. Hallitusversio: Strateginen perustelu, riskit, governance (2 sivua)
2. Keskijohtoversio: Toteutus, vastuut, aikataulu (1 sivu)
3. Henkilöstöversio: Miksi, mitä tarkoittaa heille (0.5 sivua)
```

### Vaihe 5: Parhaat käytännöt

#### Mikä toimii:

| Käytäntö | Miksi toimii |
|----------|--------------|
| Päätösrekisterin säännöllinen päivitys | Seuranta pysyy ajantasalla |
| Henkilökohtainen omistajuus | Vastuu selkeä, ei "jory vastaa" |
| Executive summary -pakko | Tieto on päätösvalmista |
| Kokousten valmistelu GPT:llä | Kokoukset tehokkaita |
| Status-tarkistus joka kokouksessa | Ongelmat nousevat ajoissa |

#### Mitä välttää:

| Virhe | Seuraus | Ratkaisu |
|-------|---------|----------|
| "Johtoryhmä vastaa" | Kukaan ei vastaa | Nimeä yksi henkilö |
| Päätös ilman deadlinea | Ei koskaan valmistu | Pakota deadline |
| Liian monta prioriteettia | Mikään ei toteudu | Max 3-5 strategista fokusta |
| Seurannan laiminlyönti | Päätökset unohtuvat | Vakioagenda: status review |
| Vain päätöksenteko, ei seuranta | Execution Gap | Käytä Execution Engineä |

### Vaihe 6: Mittaa onnistumista

Seuraa näitä mittareita:

| Mittari | Tavoite | Miten mitataan |
|---------|---------|----------------|
| Päätösten toteutuma | >80% | Valmiit / Kaikki |
| Päätösten läpimenoaika | <30 pv mediaani | Päätös → Valmis |
| Eskalaatioiden määrä | <10% | Punaiset / Kaikki |
| Aikataulussa pysyminen | >90% | Ajallaan / Kaikki |

---

## Knowledge-tiedostojen sisältö

### Business-Strategy-Frameworks-KB.md
- Porter's Five Forces (täydellinen analyysimatriisi)
- SWOT/TOWS Matrix (sisäinen/ulkoinen + strategiset yhdistelmät)
- STEEPLE Analysis (makroympäristö)
- BCG Growth-Share Matrix
- Ansoff Growth Matrix
- Blue Ocean Strategy (Four Actions Framework)
- Business Model Canvas (9 lohkoa)
- Value Proposition Canvas
- VRIO Analysis
- Balanced Scorecard, McKinsey 7S
- TAM/SAM/SOM -laskentataulukko

### Financial-Analysis-Toolkit-KB.md
- Kaikki talousmittarit kaavoilla (kannattavuus, likviditeetti, tehokkuus, velkaantuneisuus)
- SaaS/Unit Economics -metriikat (CAC, LTV, MRR, NRR, Churn)
- DCF-arvonmääritys vaihe vaiheelta
- Comparable Company Analysis
- Industry benchmarks (SaaS, E-commerce, B2B Services, Manufacturing)
- 3-Statement Model -rakenne
- Skenaarioanalyysi-kehys

### HR-Finnish-Employment-Law-KB.md
- **Työsopimuslaki 55/2001:** Koeaika, irtisanomisajat, työsopimuksen muoto
- **Työaikalaki 872/2019:** Työajat, ylityökorvaukset, lepoajat, liukuva työaika
- **Vuosilomalaki 162/2005:** Lomakertymä, lomapalkan laskenta, lomaraha
- **YT-laki 1333/2021:** Neuvotteluajat, sisältö, henkilöstön edustajat
- **Yhdenvertaisuuslaki & Tasa-arvolaki:** Syrjintäkielto, palkkatasa-arvo
- HR-frameworkit (OKR, 9-Box Grid, Succession Planning)
- HR-mittarit (vaihtuvuus, rekrytointi, sitoutuminen, palkitseminen)
- TES-yleistietoa

### Marketing-Metrics-Benchmarks-KB.md
- AARRR täydellinen (Acquisition, Activation, Retention, Referral, Revenue)
- Kanavabenchmarkit (Email, Social Media, Paid Ads, SEO)
- Conversion funnelit (B2B SaaS, E-commerce, B2B Services)
- ROI & Attribution -mallit
- Industry benchmarks toimialoittain ja kasvuvaiheittain
- Seasonal & timing benchmarks

### Executive-Leadership-KB.md (UUSI)
- **Execution Engine:** Päätösrekisterimalli, status-määritelmät, seurantarytmi
- **Decision Engine:** RAPID-malli, päätösmatriisi, trade-off -analyysi, skenaariot
- **Governance Engine:** Hallituksen vuosikello, materiaalimalli, CEO/CFO-raportit
- **Communication Engine:** Cascade-viestintämalli, kriisiviestintä
- **Strategic Frameworks:** Balanced Scorecard, OKR, riskikartta
- **Finnish Business Context:** Osakeyhtiölaki, YT-laki, suomalainen johtamiskulttuuri

---

## Custom GPT:n asentaminen

### Vaihe 1: Avaa ChatGPT
1. Mene osoitteeseen **chat.openai.com**
2. Kirjaudu OpenAI-tililläsi
3. **Huom:** Tarvitset ChatGPT Plus -tilauksen Custom GPT:iden luomiseen

### Vaihe 2: Avaa GPT Builder
1. Klikkaa vasemmasta sivupalkista **Explore GPTs**
2. Klikkaa oikeassa yläkulmassa **+ Create**
3. Valitse **Configure**-välilehti (ei Create-välilehteä)

### Vaihe 3: Määritä GPT:n perustiedot
1. **Name:** Anna GPT:lle nimi (esim. "Executive Command Center")
2. **Description:** Kopioi lyhyt kuvaus tiedostosta (GPT Description -osio)

### Vaihe 4: Kopioi Instructions
1. Avaa haluamasi GPT.md-tiedosto
2. Etsi osio **## GPT Instructions (Copy to ChatGPT)**
3. Kopioi KAIKKI teksti ``` merkkien välistä (älä kopioi ``` merkkejä)
4. Liitä **Instructions**-kenttään ChatGPT:ssä

### Vaihe 5: Lataa Knowledge-tiedosto (TÄRKEÄ!)
1. Scrollaa alas **Knowledge**-osioon
2. Klikkaa **Upload files**
3. Lataa vastaava Knowledge-tiedosto `Knowledge/`-kansiosta:
   - Business Strategy → `Business-Strategy-Frameworks-KB.md`
   - Financial Analyst → `Financial-Analysis-Toolkit-KB.md`
   - HR Advisor → `HR-Finnish-Employment-Law-KB.md`
   - Marketing Strategist → `Marketing-Metrics-Benchmarks-KB.md`
   - **Executive Command Center** → `Executive-Leadership-KB.md` + omat yritysdokumentit

**Miksi tämä on tärkeää?**
- Instructions kertoo GPT:lle *miten toimia* (rooli, prosessi, tyylit)
- Knowledge-tiedosto antaa *yksityiskohtaisen tiedon* (kaavat, taulukot, benchmarkit)
- GPT hakee automaattisesti tarvittavat tiedot Knowledge-tiedostosta

### Vaihe 6: Määritä Capabilities
1. Scrollaa **Capabilities**-osioon
2. Laita päälle tarvittavat ominaisuudet (ks. alla oleva taulukko)

### Vaihe 7: Lisää Conversation Starters (valinnainen)
1. Kopioi esimerkkikysymykset GPT.md-tiedoston **Conversation Starters** -osiosta
2. Lisää 4-5 aloituskehotetta

### Vaihe 8: Tallenna
1. Klikkaa **Save** oikeassa yläkulmassa
2. Valitse näkyvyys:
   - **Only me** - Vain sinä näet
   - **Anyone with a link** - Kaikki linkin saaneet voivat käyttää
3. GPT on nyt käyttövalmis!

---

## Suositellut Capabilities per GPT

| GPT | Web Browsing | Code Interpreter | DALL-E | Knowledge |
|-----|:------------:|:----------------:|:------:|:---------:|
| **Business Strategy Consultant** | **KRIITTINEN** | Suositeltu | - | **KRIITTINEN** |
| **Financial Analyst** | Suositeltu | **KRIITTINEN** | - | **KRIITTINEN** |
| **Marketing Strategist** | **KRIITTINEN** | Suositeltu | **KRIITTINEN** | **KRIITTINEN** |
| **HR Advisor** | **KRIITTINEN** | Suositeltu | - | **KRIITTINEN** |
| **Executive Command Center** | **KRIITTINEN** | **KRIITTINEN** | Suositeltu | **KRIITTINEN** |

### Miksi nämä valinnat?

**Executive Command Center:**
- **Web Browsing KRIITTINEN** → Markkinaseuranta, kilpailijauutiset, regulaatiomuutokset
- **Code Interpreter KRIITTINEN** → KPI-dashboardit, skenaariolaskelmat, Excel-analyysit
- **Knowledge KRIITTINEN** → Viitekehykset + yrityksen omat dokumentit
- DALL-E Suositeltu → Presentaatiovisuaalit, infograafit

**Business Strategy Consultant:**
- **Web Browsing KRIITTINEN** → Reaaliaikainen kilpailija- ja markkinatutkimus
- **Knowledge KRIITTINEN** → Frameworkit (Porter, SWOT, BCG, Blue Ocean jne.)
- Code Interpreter → Data-analyysi, visualisoinnit

**Financial Analyst:**
- **Code Interpreter KRIITTINEN** → Talousmallit, DCF, laskelmat, Excel-analyysit
- **Knowledge KRIITTINEN** → Metriikat, kaavat, industry benchmarks
- Web Browsing → Markkinadata, osakehinnat

**Marketing Strategist:**
- **Web Browsing KRIITTINEN** → Trendit, kilpailijat, Meta Ad Library
- **DALL-E KRIITTINEN** → Kampanjakuvat, some-materiaalit
- **Knowledge KRIITTINEN** → AARRR, benchmarkit, conversion rates
- Code Interpreter → Markkinointianalytiikka

**HR Advisor:**
- **Web Browsing KRIITTINEN** → Finlex-lainsäädäntö, TES-haku
- **Knowledge KRIITTINEN** → Työlainsäädäntö, pykälät, HR-frameworkit
- Code Interpreter → HR-metriikat, palkka-analyysit

---

## Lisää omia Knowledge-tiedostoja

Voit ladata GPT:n käyttöön myös omia tiedostoja:

**Suositellut tiedostot per GPT:**

| GPT | Omat tiedostot |
|-----|----------------|
| **Business Strategy** | Strategiadokumentit, aiemmat analyysit, toimialaraportit |
| **Financial Analyst** | Tilinpäätökset, budjetit, KPI-raportit, rahoitusdokumentit |
| **Marketing Strategist** | Brändiohjeistus, asiakaspersoonat, kampanjahistoria |
| **HR Advisor** | HR-käsikirja, sovellettavat TES:it, henkilöstöpolitiikat |
| **Executive Command Center** | Strategia, päätösrekisteri, budjetti, organisaatiokaavio, hallituspäätökset |

**Tuetut tiedostomuodot:**
- PDF, Word (.docx), Excel (.xlsx), CSV
- PowerPoint (.pptx)
- Tekstitiedostot (.txt, .md)

---

## Custom GPT:n käyttäminen

### Aloita keskustelu
1. Klikkaa vasemmasta sivupalkista **My GPTs** (tai GPT:n nimellä)
2. Valitse haluamasi GPT
3. Kirjoita pyyntösi normaalisti

### Esimerkkejä keskustelun aloituksesta

**Executive Command Center:**
- "Valmistele seuraavan johtoryhmän kokouksen agenda"
- "Mitä strategisia päätöksiä on kesken ja mikä on niiden status?"
- "Analysoi vaihtoehdot: orgaaninen kasvu vs. yritysosto"
- "Laadi kvartaalikatsaus hallitukselle"
- "Sama päätös kolmelle yleisölle: hallitus, keskijohto, henkilöstö"

**Business Strategy Consultant:**
- "Analyze the competitive landscape for [toimiala]"
- "Help me develop a market entry strategy for [markkina]"
- "Conduct a SWOT analysis for [yritys]"
- "Apply Porter's Five Forces to [toimiala]"

**Financial Analyst:**
- "Create a 3-year financial projection for [yritys]"
- "Analyze the unit economics of [liiketoimintamalli]"
- "Calculate the valuation of [yritys] using DCF"
- "Build a sensitivity analysis for our revenue assumptions"

**Marketing Strategist:**
- "Develop a go-to-market strategy for [tuote]"
- "Help me define customer segments for [palvelu]"
- "Create a growth strategy to scale from X to Y customers"
- "Analyze our AARRR metrics and suggest improvements"

**HR Advisor:**
- "Suunnittele perehdytysohjelma uusille työntekijöille"
- "Miten toteutetaan YT-neuvottelut oikein?"
- "Laadi suorituksen johtamisen järjestelmä OKR-mallilla"
- "Mikä on koeajan enimmäispituus työsopimuslain mukaan?"

### Vinkkejä tehokkaaseen käyttöön

| Vinkki | Esimerkki |
|--------|-----------|
| **Anna konteksti** | "We are a B2B SaaS company with 50 employees..." |
| **Määritä tavoite** | "I need this for investor presentation" |
| **Pyydä tiettyä viitekehystä** | "Use Porter's Five Forces to analyze..." |
| **Pyydä formaattia** | "Present this as a table" / "Give me bullet points" |
| **Pyydä Knowledge-hakua** | "Check the knowledge base for exact metrics" |
| **Executive-taso** | "Give me a 1-page executive summary" |

---

## Custom GPT vs. Gemini Gems

Molemmat alustat tarjoavat kattavat ominaisuudet:

| Ominaisuus | ChatGPT GPT | Gemini Gem | Huomiot |
|------------|:-----------:|:----------:|---------|
| **Code Execution** | Python | Python | Molemmat tukevat |
| **File Upload** | Kyllä | Kyllä | PDF, Excel, Word, CSV |
| **Web Search** | Web Browsing | Sisäänrakennettu | Molemmat hakevat netistä |
| **Image Generation** | DALL-E | Imagen (rajoitettu) | GPT:ssä parempi |
| **Deep Research** | Ei | Kyllä (10/kk) | Vain Geminissä |
| **Google Workspace** | Actions | Natiivi (@Gmail, @Drive) | Geminissä parempi |
| **Jakaminen** | Linkki + GPT Store | Ei suoraa jakoa | GPT:ssä parempi |
| **Konteksti-ikkuna** | 128K tokens | 1M tokens | Geminissä suurempi |
| **Instructions-raja** | 8 000 merkkiä | Suurempi | Gemini sallivampi |

**Valitse ChatGPT GPT kun:**
- Tarvitset DALL-E kuvanluontia
- Haluat jakaa GPT:n muille
- Tarvitset custom API-integraatioita

**Valitse Gemini Gem kun:**
- Käytät Google Workspacea intensiivisesti
- Tarvitset Deep Research -tutkimuksia
- Käsittelet erittäin pitkiä dokumentteja

---

## Usein kysytyt kysymykset

### Miksi Knowledge-tiedosto pitää ladata erikseen?
ChatGPT:n Instructions-osion raja on 8 000 merkkiä. Laajat frameworkit, taulukot ja benchmarkit eivät mahdu siihen. Knowledge-tiedosto on ratkaisu: GPT osaa hakea sieltä tarvitsemansa tiedon automaattisesti.

### Kuinka monta GPT:tä voin luoda?
ChatGPT Plus -tilauksella voit luoda useita GPT:itä. Jokainen toimii itsenäisesti.

### Muistaako GPT aiemmat keskustelut?
GPT muistaa keskustelun sisällä, mutta jokainen uusi keskustelu alkaa puhtaalta pöydältä. GPT kuitenkin noudattaa aina samoja ohjeita ja Knowledge-tiedostoa.

### Voinko muokata GPT:tä?
Kyllä. Avaa GPT → **Edit GPT** (kolme pistettä -valikosta) → muokkaa ohjeita → **Save**.

### Voinko lisätä omia tiedostoja?
Kyllä! Knowledge-osioon voi ladata useita tiedostoja. Lisää esim. yrityksesi strategiadokumentit, tilinpäätökset tai HR-käsikirja.

### Miksi GPT ei löydä tietoa Knowledge-tiedostosta?
- Varmista että tiedosto on ladattu
- Pyydä eksplisiittisesti: "Check the knowledge base for..."
- Tarkista, että tiedosto on oikeassa muodossa (.md, .pdf, .docx)

### Miten Executive Command Center eroaa muista GPT:istä?
Executive Command Center on suunniteltu johtoryhmätason työskentelyyn:
- **Orkestrointi:** Yhdistää eri funktioiden näkökulmia
- **Execution-fokus:** Seuraa päätösten toteutumista
- **Governance:** Hallitusraportointi ja sidosryhmäviestintä
- **Executive summaries:** Kaikki output on max 1-2 sivua

### Miten aloitan Executive Command Centerin käytön?
1. Kerää dokumentit (strategia, budjetti, organisaatio)
2. Luo päätösrekisteri (tai ota käyttöön Knowledge-tiedoston malli)
3. Asenna GPT ja lataa dokumentit
4. Aloita kokousten valmisteluista
5. Rekisteröi jokainen strateginen päätös

---

## Ongelmanratkaisu

| Ongelma | Ratkaisu |
|---------|----------|
| GPT ei vastaa odotetulla tavalla | Pyydä eksplisiittisesti haluamaasi viitekehystä |
| GPT ei käytä Knowledge-tiedostoa | Lisää pyyntöön: "Reference the uploaded knowledge base" |
| Vastaukset liian pitkiä | Lisää pyyntöön: "Be concise" tai "Max 3 bullet points" |
| Instructions ei mahdu | Varmista että kopioit vain ``` merkkien välisen osan |
| Knowledge-tiedosto ei lataudu | Tarkista tiedoston koko (max 512 MB) ja muoto |
| "Custom GPTs" ei näy | Varmista ChatGPT Plus -tilaus |
| Päätösrekisteri ei päivity | Lataa uusi versio Knowledge-tiedostona säännöllisesti |

---

## Resurssit

- [ChatGPT](https://chat.openai.com)
- [OpenAI GPT Builder Guide](https://help.openai.com/en/articles/8554397-creating-a-gpt)
- [GPT Store](https://chat.openai.com/gpts)
- [Finlex - Suomen lainsäädäntö](https://www.finlex.fi)

---

## Versiohistoria

| Versio | Päivämäärä | Muutokset |
|--------|------------|-----------|
| 4.0 | 20.12.2025 | Executive Command Center -GPT lisätty, johtoryhmän käyttöopas |
| 3.0 | 20.12.2025 | Alkuperäinen versio 4:llä funktionaalisella GPT:llä |

---

*Latentti.fi - AI-avusteinen liiketoiminnan kehittäminen*
