---
title: "Den galne forskaren 1"
subtitle: "Fyra villkorade modellresultat med händelse-COP över 1.15"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-10"
lang: sv
abstract: |
  Fyra angivna händelsemodeller ger simulerat mottagararbete över 1.15 gånger
  den modellerade startenergin och den externa bruttoenergi som tillförs under
  händelsen. Representativa COP är 1.18827 för en fallviktsdriven hävarm,
  1.57080 för en kontaktlag med tredjederivata, 17.92044 för en port med
  residyer av olika tecken och 1.67992 för en impedansanpassning utan bivillkor.
  Vi utförde 201 nya integrationer med oberoende metoder, arbetskvadratur,
  slutpunktskonton och separata bekräftelsefall. Föreslagna instrumentbudgetar
  behåller en marginal över tröskeln. Resultaten skiljer mellan ytterligare
  fallhöjd, hypotetiska interna lagar och en approximation som avviker från
  sin passiva referens.
keywords:
  - händelse-COP
  - numerisk simulering
  - arbete och energi
  - dynamik av högre ordning
  - aktiv impedans
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-mad-scientist-1}\par
\noindent Svensk utgåva av \href{https://github.com/hobnilre/physics-mad-scientist-1/blob/main/physics-mad-scientist-1.md}{Mad Scientist 1}.\par
\endgroup

# Fyra förutsägelser att undersöka {-}

Målet är **händelse-COP större än 1.15**. Dividera nyttigt nettoarbete till
mottagaren med modellerad förberedd energi över en angiven referens, plus all
angiven extern bruttoenergi som tillförs under händelsen. Redovisa slutlagren
separat. Förberedelsens verkningsgrad, återställning och okända interna
komponentkonton förblir uttryckliga fortsatta frågor.

Ordningen prioriterar direkt mätning och tydlig modelltolkning, därefter de
större elektriska förutsägelserna. Det är en undersökningsordning, ingen
rangordning av sannolikheten att lyckas med en fysisk apparat.

1. **Fallviktsdriven hävarm:** ett belastat fall ger mer arbete än den ursprungliga
   höjdreferensen; den extra sänkningen redovisas. [OP-CT-HW-01]
2. **Kontakt med tredjederivata:** en antagen intern kraft upprätthåller
   motståndsarbete fram till första stoppet. [OP-LR34-02]
3. **Port med tecknade residyer:** en angiven aktiv portlag driver en mottagare
   och ökar de kvarvarande elektriska lagren. [OP-LR15-01]
4. **Impedansanpassning utan bivillkor:** en approximation över ett ändligt
   frekvensband förutsäger arbete som dess passiva referens inte ger. [OP-LR35-02]

Varje avsnitt utvecklar en angiven modell till en genomförd händelsestudie.
De tre sista använder hypotetiska interna lagar vars fysiska energikonton är
öppna. Anpassningens resultat gäller just den lagen; referensen beräknas
parallellt. Här finns konkreta signaler och modellskillnader att undersöka,
utan att någon uppmätt apparatprestanda förutsätts.

\newpage

# Den fallviktsdrivna hävarmen

En språngbräda omvandlar nedåtgående ankomster till ett uppåtriktat avstamp.
Tidsförlopp, benkompression och brädans böjlighet påverkar rörelsen ut ur
kontakten. Frågan börjar med en jämförelse mellan ändtillstånd och fortsätter
med vilket arbete hela kontaktförloppet faktiskt ger till en mottagare.

![Illustrativ avstampsjämförelse med lika massor. Fortsatt sänkning och deformation förbinder inkommande och utgående rörelseenergitermer.](figures/lever-observation.pdf){#fig:lever-observation width=98%}

För två inkommande massor och en utgående massa, vardera $70\,\mathrm{kg}$,
ger hastigheterna $5$ och $8\,\mathrm{m/s}$ värdena $K_{\rm in}=1750$ J och
$K_{\rm out}=2240$ J: kvoten $32/25$. Tyngdkraft, eftergivlighet och aktiva
krafter kan bidra under kontakten. En ideal fast vridpunkt ger impuls utan
arbete. Rörelseförloppet är därför den intressanta mätning som saknas.

## Ett beräknat belastat fall

Vår anpassning har två vertikala drivvikter på $1$ kg, kontaktarmar $a=-0.5$ m,
hävarmens tröghetsmoment $I=0.15\,\mathrm{kg\,m^2}$, vridstyvheten
$50\,\mathrm{N\,m/rad}$ och lagerdämpningen $0.1\,\mathrm{N\,m\,s}$.
Mottagararmen är $a_R=0.8$ m. Med höjder $y_i$ räknade uppåt, vinkeln $\phi$,
kompressionen $\delta_i=[a\sin\phi-y_i]_+$ och kontaktkraften $f_i=k\delta_i$
blir Newtons ekvationer under det fria förloppet
\begin{equation}
\begin{split}
m\ddot y_i&=-mg+f_i,\\
I\ddot\phi&=-\sum_i f_i a\cos\phi-50\phi-0.1\dot\phi
-b(a_R\cos\phi)^2\dot\phi.
\end{split}
\label{eq:lever-model}
\end{equation}
Här är $g=9.81\,\mathrm{m/s^2}$, $v_R=a_R\cos\phi\,\dot\phi$ och den
externa viskösa mottagarens effekt $P_R=bv_R^2$.

Händelsen börjar med samtidig frigöring från $y_1=y_2=0.30$ m,
$\phi=0$ och noll hastigheter. Den slutar $1.5$ s senare, strax före den
tidigare angivna återställningen. Det ursprungliga beredskapsplanet definierar
tyngdenergins nollnivå; vi behöll referensen och tidsfönstret. Ingen extern
aktuator verkar under händelsen, och $D_{\rm event}=2mgH=5.886$ J.
Oberoende beräknad lagrad energi är
\begin{equation}
U=\tfrac12m\sum_i\dot y_i^2+mg\sum_i y_i
+\tfrac12I\dot\phi^2+25\phi^2+\tfrac12k\sum_i\delta_i^2.
\label{eq:lever-store}
\end{equation}

![Genomförd hävarmssimulering och separat angivna bekräftelsefall. Lagret inkluderar tyngdenergi relativt det ursprungliga beredskapsplanet. Linjerna till höger förbinder beräknade slutvärden.](figures/lever-event.pdf){#fig:lever-event width=98%}

\FloatBarrier

Vid $k=500$ N/m och $b=32$ N s/m är mottagararbetet **6.994139 J**,
vilket ger **COP 1.188267**. Lagervärmen är $0.034598$ J. Slutlagret är
$-1.142737$ J: tyngdenergin $-2.244651$ J plus $1.101914$ J rörelseenergi
och elastisk energi. Drivvikterna slutar $0.114406$ m under beredskapsplanet.
Deras extra sänkning ger skillnaden mot startreferensen; det oberoende
beräknade kontot går numeriskt ihop.

| Kontakt $k$ (N/m) | Mottagare $b$ (N s/m) | Nyttigt arbete (J) | Händelse-COP |
| --: | --: | --: | --: |
| 500 | 32 | 6.994139 | 1.188267 |
| 450 | 30 | 7.013120 | 1.191492 |
| 450 | 34 | 7.017282 | 1.192199 |
| 550 | 30 | 6.974505 | 1.184931 |
| 550 | 34 | 6.978687 | 1.185642 |

Table: Representativ händelse och fyra separata bekräftelsefall, vart och ett körda med tre lösarinställningar.

**Gör marginalen synlig.** Våg och linjal bestämmer startenergin;
lastcell och lägesgivare ger $W_R=\int F_R\,ds_R$. Förutsagda toppvärden är
$52.40$ N och $1.637$ m/s, med $0.156$ m utslag vid mottagaren. Anta
kalibrerat 200 Hz-svar, 2 kHz sampling och högst $0.1$ ms kanalskevhet.
Budgeten för förstärkning, nollfel, tid, belastning och referens ger
$B_{\rm in}=0.02943$ J och $B_{\rm out}=0.06608$ J. Konservativt COP är
**1.171**, över 1.15; även alla fyra bekräftelsefall passerar.
Marginalen till tröskeln är $0.225239$ J. I det bevarade hela förloppet
kräver återställningen ytterligare $2.210180$ J bruttoinflöde; dess COP är $0.995077$.

\newpage

# En kontaktlag med tredjederivata

Massa, fjäder och motstånd ger en välbekant approximation av en stöt.
En utvidgning till högre ordning lägger till en intern kraft proportionell
mot ryck, accelerationens tidsderivata. Termen är dimensionellt möjlig;
dess fysiska realisering är den öppna frågan. Den ger ett precist sätt att
beräkna vilket motståndsarbete lagen förutsäger innan massan stannar.

![Angiven kraftmodell och mottagargräns, schematiskt visade. Det interna ryckelementet har en bestämd kraftlag; dess fysiska lagring och förberedelse är öppna frågor.](figures/cubic-observation.pdf){#fig:cubic-observation width=98%}

Låt förskjutningen vara $x$, hastigheten $v$, massan $m$, fjäderstyvheten $k$
och mottagarens motstånd $d$. Lägg till kraftlagen $F_X=Xx'''$, där
$X=\alpha md/k$ i kg s. Newtons lag blir
\begin{equation}
Xx'''+mx''+dx'+kx=0,\qquad P_R=dv^2,\qquad P_X=Xx'''v.
\label{eq:cubic-model}
\end{equation}
Tecknet hos $P_X$ anger arbete in i det interna elementet från den beräknade
rörelsen. Det beräknas från kraftlagen, oberoende av rörelseenergin och fjäderlagret.

Vid $\alpha=1$ faktoriseras operatorn som
$(dD+k)((m/k)D^2+1)$, där $D$ betecknar tidsderivering. Detta är också
gränsen mellan stabila och instabila rötter i den normaliserade kubiska
kontrollmodellen när $d^2=mk$. Rotstabilitet och fysisk realiserbarhet är skilda frågor.

## Från första kontakt till första stopp

Vi använde $m=0.5$ kg, $k=5000$ N/m, $x(0)=0$, $v(0)=1$ m/s och
$x''(0)=0$. Händelsen slutar vid det första nollstället för $v$ efter start.
Ingen yttre drivkraft anges. Förberedd rörelseenergi är $0.250$ J;
motståndsarbetet är nyttig utenergi. Permanent spikinträngning ingår inte
i denna fjäder- och motståndsmodell.

För $\alpha=1$ är den oberoende exakta referensen
\begin{equation}
\omega=\sqrt{k/m},\quad x=\frac{v_0}{\omega}\sin\omega t,
\quad t_*=\frac{\pi}{2\omega},\quad
\frac{W_R}{mv_0^2/2}=\frac{\pi d}{2\sqrt{mk}}.
\label{eq:cubic-exact}
\end{equation}
Det plottade arbetet kommer från simuleringen, inte enbart från insättning
i formeln. Vid $d=50$ N s/m nås första stoppet efter $15.708$ ms och
$10.000$ mm förflyttning. Mottagararbetet är **0.392699 J** och **COP 1.570796**.

![Beräknat arbete fram till första stoppet och jämförelse av derivatkoefficienter. Vid referenspunkten är summan av rörelse- och fjäderenergi 0.250 J medan mottagaren samlar arbete.](figures/cubic-results.pdf){#fig:cubic-results width=98%}

\FloatBarrier

| $\alpha$ | $d$ (N s/m) | Mottagararbete (J) | Händelse-COP |
| --: | --: | --: | --: |
| 0, vanlig kontroll | 50 | 0.175391 | 0.701564 |
| 0.5 | 50 | 0.307903 | 1.231611 |
| 1 | 50 | 0.392699 | 1.570796 |
| 2 | 50 | 0.510642 | 2.042569 |

Table: Fyra av de angivna jämförelserna. Alla fall och oberoende integrationer har bevarats.

Vid referensstoppet är rörelseenergin noll och fjäderenergin $0.250$ J.
Resttermen för kända lager, $\Delta U+W_R$, är $+0.392699$ J. Det oberoende
integrerade interna kraftarbetet är $W_X=-0.392699$ J. Detta lokaliserar den
modellerade överföringen utan att tilldela ett dolt lager eller en balanserande
extern källa. Vilket material eller reglerat system som kan realisera $F_X$ är öppet.

**En kort, mätbar puls.** Mottagarkraftens topp är $50$ N och inkommande
hastighet $1$ m/s. Lastcell, lägesgivare eller ljusgrindar och synkron
datainsamling kan upplösa dessa skalor. Den slutliga föreslagna specifikationen
använder karakteriserat 5 kHz kraftsvar, 40 kHz sampling och högst
$1\,\mu$s kanalskevhet. Givarens tillstånd före kontakt sattes till noll i modellen.
Ett tidigare 2 kHz-svar överskred sin budget i vissa fall och bevarades som
en underkänd instrumentjämförelse.

Med inenergins felgräns $0.005$ J och utarbetets felgräns $0.00841$ J blir konservativt COP
**1.507**. Fyra nya bekräftelsefall vid $\alpha=0.9,1.1$ och
$d=45,55$ N s/m ger COP $1.36188$--$1.79145$ och klarar samma kriterier.
Samtliga 14 angivna konfigurationer över båda stegen kördes med tre
lösarinställningar. Hur accelerationstillståndet förbereds och den interna
komponentens energikonto är konkreta frågor för nästa undersökning.

\newpage

# En elektrisk port med tecknade residyer

En portimpedans kan dölja flera interna relaxationsmoder. Positiva residyer
tillåter välbekanta resistor-kondensatorkonstruktioner. Residyer med olika
tecken utvidgar den matematiska familjen: vissa kombinationer förblir positivt
reella, andra förutsäger leverans från den interna porten. Frågan är om den
angivna lagen kan ge arbete till en uttryckligen modellerad mottagare.

![Impedansen med tecknade residyer och dess angivna belastade utvidgning. Området med negativ realdel växer med residyskalan. Gränsschemat visar det förberedda lagret och den externa mottagaren.](figures/signed-port-observation.pdf){#fig:signed-port-observation width=98%}

Portlagen med två tillstånd är
\begin{equation}
\begin{split}
\tau_j\dot z_j&=i-z_j,\qquad v_X=0.35i+R_1z_1+0.55z_2,\\
(\tau_1,\tau_2)&=(0.08,0.18)\ \mathrm{s},\qquad
R_1=-0.738869257399\alpha\ \Omega.
\end{split}
\label{eq:signed-port}
\end{equation}
Alltså är $Z(s)=0.35+R_1/(1+0.08s)+0.55/(1+0.18s)$ ohm.
Den numeriska gränsskalan är $\alpha=1$; strax under den är realdelen
icke-negativ vid alla frekvenser. Vi behöll denna kontroll och utvidgade den
uttryckligt tecknade lagen till dess aktiva område. Det är en villkorad
portmodell; interna komponentlager och fysisk realisering är ännu ospecificerade.

## Arbete till en belastning

Anslut porten i serie med $L=1$ H, $C=0.02$ F och en extern
mottagare $R_L$. Kirchhoffs lagar ger
\begin{equation}
\dot q=i,\qquad L\dot i=-q/C-R_Li-v_X,
\qquad P_R=R_Li^2,\qquad P_X=v_Xi.
\label{eq:electrical-event}
\end{equation}
Från början är $q=0.100$ C, $i=0$ och $z_1=z_2=0$. Den förberedda
kondensatorn innehåller $0.250$ J. Händelsen är det angivna intervallet
$0$--$10$ s och slutar före frånkoppling; ingen återställning eller extern
händelsematning anges. Känd elektrisk lagring är $U=q^2/(2C)+Li^2/2$.
Den interna portens fysiska energikonto förblir öppet och sätts inte till noll.

Vi körde sex residyskalor $\alpha=0.99,1,1.01,1.2,1.5,2$ och tre
mottagare $R_L=0.01,0.05,0.1\ \Omega$. Det representativa fallet
$\alpha=2$, $R_L=0.1\ \Omega$ ger **4.480110 J** nyttigt arbete och
**händelse-COP 17.920440**.

![Beräknat arbete, oberoende kända lager och leverans från den interna porten; mottagarjämförelserna använder samma 10 s-händelse. Den prickade linjen till höger anger COP 1.15.](figures/signed-port-results.pdf){#fig:signed-port-results width=98%}

\FloatBarrier

| Residyskala $\alpha$ | Mottagararbete (J) | Slutlager $L/C$ (J) | Händelse-COP |
| --: | --: | --: | --: |
| 0.99 | 0.150541 | 0.086090 | 0.602163 |
| 1 | 0.153998 | 0.090979 | 0.615992 |
| 1.5 | 0.643562 | 1.395023 | 2.574247 |
| 2 | 4.480110 | 21.075454 | 17.920440 |

Table: Genomförda residyjämförelser vid $R_L=0.1\ \Omega$. Kvarvarande lager hålls skilda från nyttig utenergi.

Det representativa förloppet slutar med $20.678461$ J i kondensatorn och
$0.396993$ J i induktorn. Direkt integration ger $W_X=-25.305564$ J.
Därmed är $\Delta U+W_R+W_X$ numeriskt liten, medan resttermen för det
partiella lagerkontot $\Delta U+W_R$ är $25.305564$ J. Båda värdena spelar
roll: beräkningen bestämmer den angivna portöverföringen och lämnar det
interna fysiska kontot att undersöka.

**Signaler på mätbänken.** Mottagaren når $0.603$ V och $6.032$ A;
kondensatorspänningen når $45.474$ V. Kalibrerad shunt, differentialspänningskanaler
och synkron datainsamling kan integrera mottagarens faktiska produkt av spänning
och ström. Anta karakteriserade 200 Hz-kanaler, 2 kHz insamling och högst
$0.1$ ms kanalskevhet. Inenergins felgräns $0.005$ J och utarbetets felgräns $0.09067$ J ger
konservativt COP **17.213**. Tröskelmarginalen är $4.192610$ J.
Fyra separata fall vid $\alpha=1.8,2.2$ och $R_L=0.08,0.12\ \Omega$
ger COP $7.24467$--$43.73809$ och klarar samma kontroller. Alla 22 konfigurationer
kördes med tre lösarinställningar. Nästa fysiska steg är att identifiera en
portrealisering och mäta dess egna energiöverföringar tillsammans med de redan angivna.

\newpage

# När en impedansanpassning levererar arbete

En modell kan anpassas till portmätningar och samtidigt ändra det förutsagda
arbetet. Undersökningen börjar med en angiven passiv referens och en
approximation med fyra poler utan bivillkor. Approximationen får ett band med
negativ real impedans. När båda lagarna kopplas till samma förberedda krets
blir denna spektrala skillnad en mätbar arbetsjämförelse.

![Beräknad real impedans hos den anpassade lagen och dess passiva referens. Negativa värden tillhör den anpassade lagen och tillskrivs inte referensen.](figures/fitted-port-observation.pdf){#fig:fitted-port-observation width=98%}

Referensen har tre parallella RLC-grenar i serie med $0.18\ \Omega$:
\begin{equation}
Z_{\rm ref}(s)=0.18+\sum_{j=1}^{3}
\frac{a_js}{s^2+2\zeta_j\omega_js+\omega_j^2},
\label{eq:fitted-reference}
\end{equation}
med $a=(0.90,0.60,0.35)\,\Omega/\mathrm{s}$, $\zeta=(0.08,0.15,0.30)$ och
$\omega=(0.7,2,6)\,\mathrm{rad/s}$. Varje term har icke-negativ realdel.
En reell minsta-kvadratanpassning utan bivillkor vid 321 logaritmiskt fördelade
frekvenser från $0.03$ till $4\,\mathrm{rad/s}$ använder polerna
$p=(-0.25,-0.8,-2.5,-8)\,\mathrm{s^{-1}}$ och ger
\begin{equation}
\dot z_j=p_jz_j+i,\qquad
v_X=D_0i+\sum_j c_jz_j,\qquad D_0=2.85295645\ \Omega,
\label{eq:fitted-law}
\end{equation}
där $c=(-0.24049188,-2.08682151,17.41370233,-49.90285714)$
i $\Omega/\mathrm{s}$. Beräkningarna behöll full precision.
Anpassningens relativa komplexa fel är $0.823897$ över anpassningsbandet.
Minsta samplade realimpedans är $-0.326217\ \Omega$ nära
$4.571\,\mathrm{rad/s}$. Detta ger en konkret förutsägelse att pröva,
med den angivna passiva referensen som oberoende kontroll.

## Samma koppling, två portlagar

Vi använde seriekretsen i \eqref{eq:electrical-event}, med $L=1$ H,
varierande $C$ och $R_L$, $0.250$ J från början i kondensatorn, noll ström
och interna nolltillstånd. Båda lagarna utvecklas under samma angivna
$10$ s-händelse utan extern händelsematning. Anpassningens tillstånd har
inga tilldelade fysiska lager; porteffekten $v_Xi$ integreras direkt.
Referensen har dessutom oberoende beräknade grenlager och resistorförluster.

För $C=0.05$ F och $R_L=0.1\ \Omega$ ger den anpassade lagen
**0.419981 J** mottagararbete och **COP 1.679922**. Motsvarande referens
ger **0.061818 J**, alltså **COP 0.247271**. Skillnaden är ett resultat
om dessa två modellagar. Den kan inte belägga prestanda över ett för den
passiva referensen.

![Genomförda arbets- och kapacitansjämförelser. Samma startenergi och mottagare används för båda portlagarna.](figures/fitted-port-results.pdf){#fig:fitted-port-results width=98%}

\FloatBarrier

| Lag | $C$ (F) | Mottagararbete (J) | Händelse-COP |
| :-- | --: | --: | --: |
| Anpassad | 0.03 | 0.330435 | 1.321742 |
| Anpassad | 0.05 | 0.419981 | 1.679922 |
| Anpassad | 0.08 | 0.245376 | 0.981502 |
| Referens | 0.05 | 0.061818 | 0.247271 |

Table: Beräknade belastade förlopp vid $R_L=0.1\ \Omega$, inklusive en anpassning under tröskeln och motsvarande referens.

Det representativa anpassade fallet lämnar $0.907188$ J i de kända
$L/C$-lagren och ger $W_X=-1.077168$ J genom direkt integration av
porteffekten. Referensen slutar med totalt $0.010018$ J lagrat och avger
$0.178164$ J genom övriga resistorer. De separata slutpunktskontona visar
exakt vilka överföringar varje lag anger.

**Mät skillnaden.** Förutsagda toppvärden för anpassningen är $0.1285$ V
vid mottagaren, $1.285$ A och $6.014$ V över kondensatorn. Samma föreslagna
krav på 200 Hz, 2 kHz och $0.1$ ms som ovan gäller. Inenergins felgräns $0.005$ J
och utarbetets felgräns $0.008958$ J ger konservativt COP **1.611**, med
tröskelmarginalen $0.132481$ J. Fyra separat angivna anpassade fall vid
$C=0.04,0.06$ F och $R_L=0.08,0.12\ \Omega$ ger COP $1.28211$--$1.83204$
och passerar. Alla 13 kretsar kördes för båda lagarna med tre lösarinställningar.
Mät en realiserad ports svar och energiförlopp tillsammans: det avgör vilken
lag som beskriver apparaten.

\newpage

# Ett gemensamt händelse- och mätkonto {-}

Varje modell utvecklades från sina kraft- eller kretslagar. Energikontot
kontrollerades därefter. Nämnare och mottagare bestäms före jämförelsen:
\begin{equation}
D_{\rm event}=E_{\rm start}+\sum_k\int_{t_0}^{t_1}
[P_{k,\rm external}]_+\,dt,\qquad
\mathrm{COP}_{\rm event}=\frac{W_{\rm useful}}{D_{\rm event}}.
\label{eq:event-account}
\end{equation}
Förberedda lager räknas en gång. Angivna externa källor bidrar med bruttoarbete
inåt; returer redovisas separat. Mottagarens återflöde dras från nyttig leverans;
ingen av de fyra valda lagarna har sådant återflöde. Indatagolvet är
$10^{-9}$ J. Alla representativa händelser har noll angivet externt inflöde,
med startlager och referenser angivna i respektive avsnitt.

| Representativ händelse | In (J) | Nyttigt arbete (J) | Händelse-COP | Konservativt COP |
| :-- | --: | --: | --: | --: |
| Hävarm | 5.886 | 6.994139 | 1.188267 | 1.171 |
| Kontakt med tredjederivata | 0.250 | 0.392699 | 1.570796 | 1.507 |
| Port med tecknade residyer | 0.250 | 4.480110 | 17.920440 | 17.213 |
| Anpassad port | 0.250 | 0.419981 | 1.679922 | 1.611 |

Table: Fyra villkorade modellförutsägelser. Konservativa kvoter använder samtidigt tillämpliga föreslagna in- och utgränser.

**Oberoende arbete och lagring.** Beräkna för ett angivet konto
$r_E=U(t_1)-U(t_0)-\int\sum_kP_k\,dt$, med effekter positiva inåt.
Hävarmen inkluderar tyngdenergi och elastiska lager. För varje hypotetisk
intern lag integreras kraft gånger hastighet eller spänning gånger ström
oberoende. Komponentens återstående fysiska konto är okänt. En reproducerbar
restterm i ett partiellt lagerkonto redovisas som sådan; den tilldelas varken
tyst en källa eller kallas integrationsfel. Händelseprestanda hålls också
skild från förberedelsens verkningsgrad, återställning och upprepbarhet.

**Numeriskt underlag.** Vi slutförde 201 integrationer över 67 angivna
konfigurationer, inklusive passiva kontroller och fall under tröskeln.
DOP853 och Radau ger oberoende metoder; strängare toleranser och mindre
maxsteg kontrollerar känsligheten. Gausskvadratur med 8 och 16 punkter per
accepterat steg kontrollerar de integrerade arbetstillstånden. Matrisexponentialer
kontrollerar oberoende alla tre linjära familjer; den kubiska referensen
stämmer också med sin exakta lösning till första stoppet. Slutpunkterna kommer
från de faktiska tillstånden. Varje familj klarade sina angivna numeriska krav;
förfining ger feluppskattningar, inte certifierade gränser eller osäkerhet i
fysikaliska lagar. Tidigare underkända givarsvar bevarades och följdes upp.

**Instrumentgränserna.** Hävarmens inenergi har 0.5% osäkerhet; övriga
startenergigränser är 2%. Hävarmens utbudget täcker 0.3% kraftförstärkning,
0.2% lägesförstärkning, 0.02 N kraftnollfel, samplade tidsfel,
0.2% bandbredd/belastning och 0.01 J för upplösning och händelsegräns.
Övriga utbudgetar avsätter vardera 0.5% för de två mätförstärkningarna,
bandbredd/belastning och tid/sampling, plus 0.5 mJ för nollfel/upplösning.
Förstärkningsfel kombineras multiplikativt. Filter- och synkroniseringskontroller
ryms inom dessa poster. För samtidiga gränser $B_{\rm in},B_{\rm out}$ krävs
$(W_{\rm useful}-B_{\rm out})/(D_{\rm event}+B_{\rm in})>1.15$.
Antagna kalibreringar måste visas i en apparat. Budgeten anger mätmålet
för varje villkorad förutsägelse.
