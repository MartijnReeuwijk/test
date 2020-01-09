# Afbakeren en orienteren

### Probleem omschrijving:

Post-traumatic stress disorder \(PTSD\) is een aandoening die mensen kunnen krijgen na een traumatische ervaring. Mensen die hier last van hebben slapen vaak slecht omdat ze terug gaan naar dat moment als een nachtmerrie, KNGF heeft hier steeds reclame om puppy sponsors te werven. De kosten voor een geleiden hond zijn erg hoog ongeveer 20.000 euro\[1\], en ze zijn niet voor iedereen beschikbaar. Voor de mensen met PTSD wil een een PWA \([Progresive web app](https://en.wikipedia.org/wiki/Progressive_web_application)\) ontwikkelen, deze app moet de basis taken van een hond vervangen. De PWA zal mensen helpen die nu tijdelijk geen hond hebben of geen hond kunnen krijgen.

#### Hoe gaat het ongeveer werken?

Met een fitbit kunnen we het slaap ritme uitlezen, met deze data kunnen we detecteren wanneer iemand een nachtmerrie heeft. Zo kan ik met de PWA clasieke muziek spelen\[[bron](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5744879/)\] wat helpt met nachtmerries en PTSD wanneer dit niet werkt gaan we de lichten besturen op deze manier kunnen we een natuurlijk wakker worden simuleren. Wakker maken uit een nachtmerrie is normaal wat een hond doet.

#### Wat heb ik nodig?

* Fitbit / smartwatch
* Wifi connected lampen
* Speakers
* Spotify API
* Classic music playlist
* Web interface
* Web api / backend

**Wie**?

Deze app is voor mensen die tijdelijk geen hond hebben of voor mensen die niet in aanmerking komen voor een hond maar wel last hebben van PTSD.

**Wat**?

PWA voor mensen met PTSD. De PWA monitort mensen tijdens mij nachtrust, wanneer zij in hun REM slaap zitten en last krijgen van nachtmerries zal de app kalmerende muziek afspelen wanneer dit niet werkt spreekt de PWA de lampen aan en zal het natuurlijk wakker worden proces worden gestart.

**Waar**?

Het systeem is gebaseerd in de slaap kamers maar de fitbit heb je opzak en de app kan je op alles aansluiten

**Wanneer**?

Het probleem komt voor na een traumatische ervaring en dat manifesteert zich dan in de avond tijdens de REM\[4\] slaap

**Waarom**?

De redenen dat mensen hier last van PTSD zijn diverse maar het is altijd door een traumatische ervaring. Er zijn dus verschillende oorzaken van PTSD en ik moet nog onderzoeken of de verschillende oorzaken verschillende behandel methodes hebben zo kan de PWA het besten functioneren.

**Hoe**?

Er zijn veel app die je kunnen ondersteunen met het slapen hier onder een lijst.

1. Sleepio. Sleepio.
2. Relax Melodies. IPNOS Relax Melodies.
3. Nature Sounds Relax & Sleep. Nature Sounds Relax & Sleep.
4. Sleep Genius. Sleep Genuis.
5. Pzizz. Pzizz.
6. Inscape. Inscape.
7. Sleep Time. Sleep Time.
8. Sleep By Headspace. Headspace.

Deze apps zijn meer gericht op het in slaap vallen en het beter manage van slaap, zo als een nap timer en of kalmerende muziek.

#### PTSD apps

Voor PTSD zijn er ook apps op de markt, deze zijn vooral gericht op oorlogs veteranen en niet de anderen vormen van PTSD. Hier wil ik zelf nog meer onderzoek naar doen om de anderen mensen met PTSD te helpen met hun slaap problemen.

Van de PTSD app die ik heb gezien zijn ze niet erg interactive en of op slaap gericht. CBT-I is de een van de app die ik heb gevonden die op slaap ritmes gericht zijn, maar deze app is meer gericht op het verbeteren van je slaap routine en heeft geen muziek, licht en fitbit integratie.\[7\]

#### Wat valt op?

Wat me opvalt aan de app is dat ze alles proberen te doen voor het slapen terwijl met de technologie van vandaag ook mensen kunnen monitoren tijdens het slapen, op deze manier kunnen we mensen 24 uur per dag helpen met het verwerken van een traumatische ervaring.

**Hoeveel**?

_"Tussen 2004 en 2005 heeft naar schatting 7,4% van de Nederlandse bevolking in de leeftijd van 18 tot 80 jaar ooit in zijn of haar leven een posttraumatische stressstoornis -afgekort_ [_PTSS_](https://www.volksgezondheidenzorg.info/afkortingen#PTSS)_- \(gehad\)."_

_"Ongeveer 14% ontwikkelt in reactie hierop een_ [_PTSS_](https://www.volksgezondheidenzorg.info/afkortingen#PTSS) _\(_[_de Vries & Olff, 2009_](https://www.volksgezondheidenzorg.info/onderwerp/posttraumatische-stressstoornis/cijfers-context/huidige-situatie#11155)_;_ [_Darves-Bornoz et al., 2008_](https://www.volksgezondheidenzorg.info/onderwerp/posttraumatische-stressstoornis/cijfers-context/huidige-situatie#11156)_;_ [_Bronner et al., 2009_](https://www.volksgezondheidenzorg.info/onderwerp/posttraumatische-stressstoornis/cijfers-context/huidige-situatie#11157)_\). "_

In Nederland heeft hebben ongeveer 60.000 mensen last van PTSS / PTSD. 

### Ontwerp opdracht.

Als ontwerp opdracht heb ik het verbeteren van de slaap ervaring voor mensen met PTSD met het gebruik van een PWA, dit houdt in dat het als een soort app zal werken. De app is verbonden met speakers in de gebruikers kamer en met de fitbit van de gebruiker. De fitbit stuurt data naar de app de app analyseert dan de ontvangen data en zal hier een conclusie uit trekken of de gebruiker in REM slaap zit en een nachtmerrie heeft. Wanneer dit het geval is zal de app proberen om de gebruiker te kalmeren en zo zijn/haar slaap te verbeteren als dit niet werkt zal de App proberen de gebruiker rustig tewekken.

#### Te maken ontwerpen.

* API
* UX design
* Context scenario
* Visual design
* PWA front-end
* PWA back-end
* Mogelijke back-end integratie
* Extra hulp methodes voor PTSD

#### Design challengers

1. Hoe maak ik het design simpel in gebruik
   1. De mensen die de app gebruiken, kunnen net wakker zijn hier moet ik rekening me houden.
2. Hoe maak ik het design context aanpasbaar?
   1. Het design moet overzichtelijk zijn, zo wel op de app als op de fitbit
3. Hoe bereken ik het volumen van de speakers de app moet niet de gebruikers zijn buren wakker maken
   1. Hoe map ik een duidelijk schets van de kamer zodat de pwa het juiste volumen gebruikt.
4. Hoe maak ik de interactie zo "smooth" mogelijk zo dat de gebruiker niet door heeft dat het een PWA is en geen native app.
   1. Hoe gebruik ik OS gespecificeerde animaties
   2. Hoe werkt de app offline?
5. Design een uitleg hoe de gebruiker makelijk zijn of haar fitbit connect met de PWA?
   1. De gebruikers kunnen ook ouderen zijn of mensen die niet erg goed overweg kunnen met computers.
6. Toegankelijkheid van de PWA.
   1. Hoe werkt de app als we een gebruiker hebben die een hand mist?
   2. Hoe werkt de app als we een gebruiker hebben die een aantal vingers mist?
   3. Hoe werkt de app als de gebruiker blind of doof is?
7. Design challenge  API
   1. Hoe maak ik een duidelijke API architectuur zo dat anderen developers aan dit project kunnen werken?



#### Bronnen en artikelen

1. [Kosten honden](https://speakdogtricities.com/uncategorized/training-a-service-dog-for-public-access-privileges/)
2. [Muziek en PTSD](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5744879/)
3. [Philips lights](https://www.philips.nl/c-p/HF3650_01/somneo-sleep-wake-up-light-met-relaxbreathe-om-in-slaap-te-vallen)
4. [Rem slaap en PTSD](http://www.tijdschriftvoorpsychiatrie.nl/assets/articles/articles_1662pdf.pdf)
5. [Slaap ap](https://www.bustle.com/p/8-apps-for-insomnia-that-can-help-you-go-to-sleep-12197789)ps
6. [PTSD apps](https://www.brainline.org/article/have-you-seen-these-apps-ptsd)
7. [CBT-i](https://apps.apple.com/us/app/cbt-i-coach/id655918660)



## Bron vermelding

\[ 1 \]Training a Service Dog for Public Access Privileges. \(z.d.\). Geraadpleegd op 3 januari 2020, van [https://speakdogtricities.com/uncategorized/training-a-service-dog-for-public-access-privileges/](https://speakdogtricities.com/uncategorized/training-a-service-dog-for-public-access-privileges/)

\[ 2 \]Landis-shack, N., J. Heinz, A., & Bonn-Miller, M. O. \(2017\). Music Therapy for Posttraumatic Stress in Adults: A Theoretical Review. Music Therapy for Posttraumatic Stress in Adults: A Theoretical Review, 27\(4\). Geraadpleegd van [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5744879/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5744879/)

\[ 3 \]Philips. \(z.d.\). De Philips Somneo Sleep & Wake-up Light HF3650/01 Sleep & Wake-up Light kopen. Geraadpleegd op 4 januari 2020, van [https://www.philips.nl/c-p/HF3650\_01/somneo-sleep-wake-up-light-met-relaxbreathe-om-in-slaap-te-vallen](https://www.philips.nl/c-p/HF3650_01/somneo-sleep-wake-up-light-met-relaxbreathe-om-in-slaap-te-vallen)

\[ 4 \]van liempt, S., Vermetten, E., & De groen, J. H. M. \(2007\). Slaapafwijkingen bij posttraumatische stressstoornis \(49 \(2007\) 9\). Geraadpleegd van [http://www.tijdschriftvoorpsychiatrie.nl/assets/articles/articles\_1662pdf.pdf](http://www.tijdschriftvoorpsychiatrie.nl/assets/articles/articles_1662pdf.pdf)

\[ 5 \]de Lorenzo, C. \(2018, 13 oktober\). 8 Apps For Insomnia That Can Help You Go To Sleep. Geraadpleegd op 4 januari 2020, van [https://www.bustle.com/p/8-apps-for-insomnia-that-can-help-you-go-to-sleep-12197789](https://www.bustle.com/p/8-apps-for-insomnia-that-can-help-you-go-to-sleep-12197789)

\[ 6 \]BrainLine . \(2018, 21 februari\). Have You Seen These Apps for PTSD? Geraadpleegd op 4 januari 2020, van [https://www.brainline.org/article/have-you-seen-these-apps-ptsd](https://www.brainline.org/article/have-you-seen-these-apps-ptsd)

\[ 7 \]‎CBT-i Coach. \(2013, 4 juni\). \[Mobiele app\]. Geraadpleegd op 4 januari 2020, van [https://apps.apple.com/us/app/cbt-i-coach/id655918660](https://apps.apple.com/us/app/cbt-i-coach/id655918660)







