# Web Typography, 2020/2021

Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Leerdoelen

- Je kan de kennis over vormgeving die je hebt opgedaan tijdens de minor technisch toepassen met behulp van CSS
- Je kan verborgen nuance uit een audiotrack overtuigend vertalen naar visuele (typografische) beelden
- Je kan je typografische keuzes onderbouwen.
- Je hebt de exclusive design principles gebruikt.

## Oplevering

Je levert een werkende versie op, gemaakt met HTML, CSS en JavaScript. Deze staat op Github. In een duidelijke readme documenteer en onderbouw je je ontwerpkeuzes. Je developmentgeschiedenis is terug te vinden op GitHub.

Je levert ook een *screen recording* met audio op van je fragment. Dit is een video van de definitieve versie, gemaakt van jouw browserscherm.

De beoordeling is mondeling en volgt [de rubric uit het beoordelingsformulier](web-typografie-beoordeling.pdf).

## Typografische restricties

Je *moet* een van deze twee opties kiezen, en je keuze moet je onderbouwen. In je readme staat een uitleg over je overwegingen om de ene of de andere restrictie te kiezen.

### Optie 1: Systeemfont

De eerste optie is dat je gebruik maakt van het zogenaamde *systeemfont* van degene die naar jouw werk kijkt. Dit font verschilt per operating system, en het verschilt soms zelfs per versie van het operating system. Het is ook aan te passen door de gebruiker zelf. 

Je hebt dus geen controle over welk lettertype er precies gebruikt wordt. Het levert dus een onzeker, en beperkt typografisch palet op. Je hebt geen *light* versies, of *extrabold*. En ook geen serif en sans-serif versie van dezelfde familie. In dit geval heb je alleen de beschikking over normal, **bold** en _italic_. Dit heeft natuurlijk ook zijn voordelen!

### Optie 2: Brenner

Je kan er ook voor kiezen om gebruik te maken van de complete Brenner familie. Dit is een zeer uitgebreid en uiterst flexibel font. [Hier kan je je verdiepen in dit font](https://www.typotheque.com/blog/brenner_an_unusual_typeface_family_with_distinct_voices). Als je kiest voor dit font dan heb je de beschikking over een *sans serif*, een *condensed*, een *serif*, een *monotype*, een *slab*, een *display* en een *script* versie. En veel van deze versies hebben varianten van *light* tot *bold*, en allemaal zowel *bold* als *italic*.

Met Brenner zijn er natuurlijk veel en veel meer mogelijkheden dan met systeemfonts. Dat kan zowel een voordeel als een nadeel zijn. 

Voor een overzicht, zie [de brenner.pdf](brenner.pdf).

## Het fragment

Ik heb een fragment voorbereid. Het gaat om twee scenes uit *Blade Runner 2049*. De captions staan in de HTML, en ze verschijnen in sync met de video. [Kijk maar](closed-captions/index.html).

### De captions

De captions staan in de html, in het bestand index.html. Je kan aan elke paragraaf eventueel een of meer classes toevoegen. Bijvoorbeeld `voice1` of `voice2 soft`. Classes voeg je handmatig toe in de html.

Met JavaScript worden er een paar dingen extra gedaan: 

- er wordt aan elke paragraaf een unieke class toegevoegd (`p0`, `p1`, etc)
- Elk woord wordt in een aparte `span` gezet. Hierdoor kan je elk woord apart stylen, en eventueel ook [na elkaar laten verschijnen](https://github.com/cmda-minor-vid/web-typography-18-19/blob/master/closed-captions/css.css#L41).

### Tijdens het afspelen

Tijdens het afspeelen wordt er een class `on` op de caption gezet als hij moet verschijnen, en een class `off` als hij klaar is. *Zowel class `on` als class `off` blijft op de caption staan!*

De timimg van de captions kan je aanpassen in [closed-captions/captions.js](closed-captions/captions.js).

Er verschijnen ook classes op de body op momenten dat er geluiden worden afgespeeld, zoals `sound1` en `sound2`. Je kan geluiden toevoegen in [closed-captions/sounds.js](closed-captions/sounds.js).

*let op,* de geluiden zijn niet compleet, dit zal je zelf moeten aanvullen.

## Een eigen fragment (afgeraden, uitgebreide onderbouwing is nodig)

Je kan er ook voor kiezen om een eigen, *beter* fragment te gebruiken. Dit wordt afgeraden. De tijd die je besteedt aan het zoeken naar dat fragment kan je beter besteden aan het werken aan de opdracht. Bovendien blijkt dat er vaak fragmenten worden gekozen die niet goed voldoen aan de opdracht. Als je een ander fragment kiest dan *moet* je dit goed onderbouwd voorleggen aan je docent. De deadline hiervoor is vrijdagochtend in de eerste week.

### Waar moet je op letten bij het kiezen van een eigen fragment.
Lees de opdracht nog eens goed door. Waar gaat het ook al weer precies om? 

Voor een goede onderbouwing van je keuze voor een ander fragment moet je deze vragen in elk geval beantwoorden:

- Welke informatie zit er in de audio die echt niet zichtbaar is?
- Welke rol speelt de audio in het fragment?
- Werkt de scene nog zonder geluid?
- Waarom is dit fragment beter dan het aangeboden fragment?

Je kan dan de nodige HTML en JavaScript genereren door gebruik te maken van [caption generator](https://cmda-minor-vid.github.io/web-typography-18-19/generator/) (in Google Chrome). 

Als je de closed captions wil bewerken dan kan je een tool zoals [Amber Script](https://www.amberscript.com/en) gebruiken. Daar kan je exporteren als `.srt`, en die kan je weer door de generator halen.


### Onderbouwing geluid
Het eerste geluid heb ik ontworpen dat de video trilt, omdat de hoofdpersoon met een auto aan komt rijden en het geluid onheilspellend en spannend is.
Het tweede geluid is een (vergeleken met andere alarmen) rustig alarm. Deze heb ik ontworpen met een rood en blauwe box shadow.
Het derde geluid is een loeier. Deze heb ik iets groter en korter, maar dan in het wit gedaan ten opzichte van de vorige. 
Hierna volgt drie keer een vrij intens alarmgeluid. De derde echter het hardst, deze komt het meest binnen. Ik heb deze heftiger laten knipperen dan de eerste twee. 
Als laatste hoor je een aanzwellende piep van 41s. Ik vind deze piep heel irritant, ik heb een 'eye pain color palette' opgezocht en deze in 41s steeds sneller laten knipperen tot het irritant wordt in de vorm van een shadow. De achtergrond knippert net zo hard mee met de kleuren zwart en wit. Ik heb een moment van sound toegevoegd zodra de piep is afgelopen en de hoofdpersoon goed nieuws krijgt. Het scherm springt dan opeens op wit.

### Onderbouwing typografie
Ik heb gekozen voor Brenner, omdat ik het idee had hier veel meer vrijheid en speling had. Ik vond voice1 den vrij monotoon en robotachtige stem hebben. Vandaar de keuze voor mono. Hij komt vijandig over, dus de kleur rood. Hoofdpersoon oogt rustig, dus gekozen voor condensed en de kijker staat aan zijn kant, dus de kleur groen. Ik heb de kleur groen gekoppeld aan een wat grotere font-size, want de kijker staat dichterbij de hoofdpersoon dan de robotachtige stem, kleiner font-size. Pas op het eind bij het goede nieuws is deze robotachtige stem ook groen en zelfde font-size. De fuck-off skinjob heb ik wit ontworpen, het was wel aggressief, maar wel fluisterend. Vandaar de kleur wit, maar wel een gek font.

Ik heb de eerste paragraaf iets aangepast, zelfde font-family en weight.
De hoofdpersoon moet 3x iets herhalen, dit heb ik ook in de index zo aangepast dat dit te lezen is. Verder heeft de ondertiteling een zwarte achtergrond zodat het leesbaar genoeg is.

### Onderbouwing exclusive principles
Study situation

Normaal gesproken ontwerp je voor een zo'n breed mogelijke doelgroep. Bij deze opdracht gaat het specifiek om doven/slechthorenden (niet bij geboorte doof). Doordat het specifiek om deze doelgroep gaat, kon ik heel veel loslaten wat betreft ontwerpen en mij volledig focussen op het visuele. De geluiden moeten visueel zo ontworpen worden dat doven dezelfde ervaring hebben als kijkers met een gewoon gehoor.

Ignore conventions

Om consistentie in je designs toe te passen maak je normaal gesproken gebruik van conventies. Conventies zijn er zodat iedere gebruiker je ontwerp herkend door standaardisering. Bij closed captions is dit witte tekst op een zwarte balk. Deze conventies heb ik proberen te doorbreken door verschillende fonts, kleuren, weights en de geluiden visueel te ontwerpen.

Prioritise identity

In plaats van de content op de eerste plaats te zetten, zal ik hier de identiteit van de gebruiker op de eerste plek zetten. Dit is iemand die geluid niet kan oppakken. Het is daarom van belang dat de content, geluid dus minder belangrijk wordt. Om de identiteit van de gebruiker te achterhalen heb ik de video met en zonder geluid bestudeerd en geprobeerd het zo dicht mogelijk bij elkaar te brengen. Een aanzwellend piepgeluid vind ik heel irritant, hier hoort dan ook een beeld bij wat irritant is. Een alarm knippert, een loeigeluid als zwaailicht etc etc.

Add nonsense

Als ontwerper moet normaal gesproken alles van toegevoegde waarde zijn. Aangezien ik specifiek voor slechthorenden ontwerp kan ik dit loslaten. Ik vond het een leuke ervaring buiten richtlijnen om te ontwerpen. Het beeld wat beweegt, kleuren die pijn doen, knipperend licht, contrasten en dergelijke werken voor een normale gebruiker averechts. Voor doven heeft dit echter wel degelijk een toegevoegde waarde. 
