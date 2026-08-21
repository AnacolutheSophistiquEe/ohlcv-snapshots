# MSTR

**Generated** : 2026-08-21T22:00:00.787031+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $119.25  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $119.25 (+0.5% vs entrée) · entrée $118.71 · stop $113.96 · T1 $121.79 · R/R 0.65  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk 0.043 _(réel 5 s)_ (GBM -0.038) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23215 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.7 > 70 (surachat) ; %B 1.28 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.17–$119.25 (mid $118.71)
- Spot actuel : $119.25 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $113.96 (stop swing_plan-based (-8.63%))
- Targets : T1 $121.79 · R/R 0.65 | T2 $124.86 · R/R 1.29 | T3 $127.94 · R/R 1.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.96


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.63 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1254).
   - exécution **2.769 pt plus bas** dans le cas TYPIQUE (médiane), 18.107 au p90, **18.742 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0418 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.428 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1563** [0.1081 ; 0.2159] _(largeur 10.8 pt, n_eff 173.1)_
   - swing : **0.5484** [0.4957 ; 0.6003] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5736** [0.521 ; 0.6249] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.0 pt), swing (30.8 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.92 %** | CVaR **-10.5 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.37 % contre 4.79 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.76 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3312** (β de hausse 1.8634, asymétrie 1.2511) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 113.1949 sur support (0.47 ATR, 5.078 %) — p(stop avant cible) 0.7326 [0.68 ; 0.78], R/R 3.365, perte reelle 8.128 % (gap inclus), CVaR 5.187 %, EV -2.889 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.4718 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.733, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 5.19 % > budget 3.70 %
- Budget de queue : **3.7 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.47 ATR (stop 5.078 %) — p(stop avant cible) 0.7326 [0.68 ; 0.78], R/R 3.365, perte reelle 8.128 % (gap inclus), EV -2.889 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.733, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.19 % > budget 3.70 %
      - ⚠ support DETECTE a 0.30 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 5.1 % x 27.35 % + P(rien) 21.6 % x 7.67 % ne couvrent pas P(stop) 73.3 % x 8.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.679 %) — p(stop avant cible) 0.5877 [0.54 ; 0.64], R/R 2.311, perte reelle 11.838 % (gap inclus), EV -3.4031 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.73 % > budget 3.70 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.40 %) : P(cible) 6.2 % x 27.35 % + P(rien) 35.0 % x 5.30 % ne couvrent pas P(stop) 58.8 % x 11.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.47 ATR (stop 15.333 %) — p(stop avant cible) 0.2913 [0.25 ; 0.34], R/R 1.014, perte reelle 26.975 % (gap inclus), EV -5.2069 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.35 % > budget 3.70 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.21 %) : P(cible) 6.5 % x 27.35 % + P(rien) 64.3 % x 1.34 % ne couvrent pas P(stop) 29.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.92 ATR (stop 27.878 %) — p(stop avant cible) 0.0694 [0.05 ; 0.10], R/R 0.981, perte reelle 27.878 % (gap inclus), EV -2.3298 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.88 % > budget 3.70 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.33 %) : P(cible) 6.6 % x 27.35 % + P(rien) 86.5 % x -2.55 % ne couvrent pas P(stop) 6.9 % x 27.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.038 | EV/share : $-0.180 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.4 | bear 10.4 | side 11.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 238.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.448% → cible +2.591% / stop −4.0%, p_fill 91%, n_eff≈40.3) : P(cible|rempli) **49%** · **EV/risk +0.043** (×p_fill ; si rempli +0.19% du capital)
  - **swing** (entrée dip −1.001% → cible +15.413% / stop −7.707%, p_fill 88%, n_eff≈36.0) : P(cible|rempli) **15%** · **EV/risk +0.048** (×p_fill ; si rempli +0.42% du capital)
  - **deep** (entrée dip −1.471% → cible +8.193% / stop −7.794%, p_fill 85%, n_eff≈37.7) : P(cible|rempli) **54%** · **EV/risk +0.078** (×p_fill ; si rempli +0.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→57% · +3.0%→41% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.47% (p90 9.85%) · excursion haute méd. +2.46% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.384% vs midi 1.218% vs clôture 1.366% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.001)_ ; drift intra méd. 0.298% ; recovery-V 24%
- **σ réalisé intraday** 3.727% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 78% / bas 63% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 111.7125 (VA 110.9625–112.4625 ; dernier close 112.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 77% · **stop −4.68%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 51% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.89% (p90 −2.05%) · haut méd +0.75% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.82%) · haut méd +1.2% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.47%) · haut méd +1.42% · range méd 3.15%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −3.7%) · haut méd +1.78% · range méd 3.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (125/159) · gap 44% · délai 0.0min · rebond 50% (62/125) (MFE +1.03%)
   - −1.0% : fill 30min 59% · séance 71% (119/159) · gap 38% · délai 0.0min · rebond 57% (69/119) (MFE +1.08%)
   - −1.5% : fill 30min 52% · séance 65% (110/159) · gap 31% · délai 0.0min · rebond 59% (65/110) (MFE +1.52%)
   - −2.0% : fill 30min 46% · séance 58% (99/159) · gap 25% · délai 0.0min · rebond 62% (63/99) (MFE +1.4%)
   - −3.0% : fill 30min 31% · séance 46% (77/159) · gap 14% · délai 2.0min · rebond 60% (47/77) (MFE +1.66%)
   - −4.0% : fill 30min 22% · séance 38% (64/159) · gap 5% · délai 18.1min · rebond 63% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.7min · rebond 77% (34/47) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.28%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.68%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.95% (p90 −2.54%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=969 jambes) : jambe baissière méd −1.14% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (77/78) · rebond 53% (39/77)
      · −2.0% : fill 91% (70/78) · rebond 60% (41/70)
      · −3.0% : fill 80% (62/78) · rebond 60% (37/62)
      · −4.0% : fill 66% (52/78) · rebond 65% (34/52)
      · −5.0% : fill 50% (40/78) · rebond 80% (30/40)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (15/18) · rebond 74% (11/15)
      · −2.0% : fill 52% (11/18) · rebond 61% (8/11)
      · −3.0% : fill 22% (5/18) · rebond 55% (3/5)
      · −4.0% : fill 14% (4/18) · rebond 7% (1/4)
      · −5.0% : fill 11% (3/18) · rebond 9% (1/3)
   - **gap-up** (63 séances) :
      · −1.0% : fill 35% (27/63) · rebond 63% (19/27)
      · −2.0% : fill 19% (18/63) · rebond 71% (14/18)
      · −3.0% : fill 13% (10/63) · rebond 57% (7/10)
      · −4.0% : fill 11% (8/63) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/63) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 55% si les 15 1res min sont vertes (81 cas) · 36% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 80% si début vert vs 14% si rouge (base 46% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **80%** · continue >prix actuel 46% ; creux résiduel méd -1.49% (q20 -3.26%) → **SL/trailing à −3.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.54% → **scale +1.59% / runner +2.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **14%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.67%** (au-delà de la MAE q10 -4.67%), cible rebond +1.65% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.38% .. +3.62%] · haut q95 +3.97% · bas q05 -3.87%
   - 60min (n=160) : retour [-4.72% .. +4.13%] · haut q95 +5.47% · bas q05 -5.08%
   - 2h (n=160) : retour [-4.39% .. +5.63%] · haut q95 +6.55% · bas q05 -5.25%
   - 4h (n=160) : retour [-5.7% .. +8.07%] · haut q95 +9.08% · bas q05 -6.93%
   - 6h (n=160) : retour [-5.9% .. +6.93%] · haut q95 +9.92% · bas q05 -7.31%
   - session (n=160) : retour [-5.17% .. +6.28%] · haut q95 +9.92% · bas q05 -7.8%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.22% (p75 2.61% / p90 4.03%) · ~3.12 replis/séance, durée méd 49.07 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=30)
   - −1.0% → **57%** (reprise méd 38.91 min, n=17)
   - −1.5% → **43%** (reprise méd 74.97 min, n=13)
   - −2.0% → **28%** (reprise méd 89.44 min, n=8)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−4.03%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.28% (q75 +9.94% / q95 +16.06%), MFE méd +11.04% / q90 +15.91%
   - Échelle scale-out : +11.04% (33%) / +12.88% (33%) / +15.91% (34%)
- **DÉSARMER** : repli > **−4.03%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.91% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 98% du temps (retour médian dernière heure +0.79%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 71.7  _(surachat)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 2.723  _(pas de croisement recent)_
- **BB** : %B 1.28 · largeur 26.7%
- **ATR** : 6.11 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.168  _(accumulation)_
- **Vol ratio** : 2.16  _(volume au-dessus de la moyenne)_
- **Choppiness** : 39.4  _(transition)_
- **MA** : MA20 98.57 · MA50 99.78 · MA200 143.95  _(prix > MA20)_
- **Dist MA** : MA20 +21.0% · MA50 +19.5% · MA200 -17.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (649998 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
