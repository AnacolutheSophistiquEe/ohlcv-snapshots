# 267260

**Generated** : 2026-08-31T00:17:07.956251+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩814000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩814000.00 (+2.3% vs entrée) · entrée ₩795348.65 · stop ₩731720.75 · T1 ₩835016.44 · R/R 0.62  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk 0.047 _(réel 5 s)_ (GBM -0.197) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 146 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩790780.40–₩799916.90 (mid ₩795348.65)
- Spot actuel : ₩814000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩731720.75 (stop swing_plan-based (-10.46%))
- Targets : T1 ₩835016.44 · R/R 0.62 | T2 ₩849340.60 · R/R 0.85 | T3 ₩863664.76 · R/R 1.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩731720.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.46 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1217).
   - exécution **1.255 pt plus bas** dans le cas TYPIQUE (médiane), 1.255 au p90, **1.255 au pire**
   - perte réelle **11.715 %** en moyenne _(tirée par la queue)_, jusqu'à **11.715 %** — au lieu des 10.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.001 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.639 % | p01 -4.805 % | pire -11.715 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.086** [0.051 ; 0.1347] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.4385** [0.3869 ; 0.4911] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.4076** [0.3567 ; 0.46] _(largeur 10.3 pt, n_eff 345.6)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 25.6 observations effectives », dont la borne haute a 95 % vaut environ 11.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.9 pt), swing (38.9 pt), deep (37.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.42 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.99 % contre 5.00 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.73 % vs -11.9 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0381** (β de hausse 0.8313, asymétrie 1.2488) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.197 | EV/share : ₩-12557.923 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 7.1 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.293% → cible +4.987% / stop −8.0%, p_fill 75%, n_eff≈35.8) : P(cible|rempli) **22%** · **EV/risk +0.047** (×p_fill ; si rempli +0.50% du capital)
  - **swing** (entrée dip −5.04% → cible +6.402% / stop −5.707%, p_fill 55%, n_eff≈22.9) : P(cible|rempli) **46%** · **EV/risk -0.030** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −7.79% → cible +9.054% / stop −8.816%, p_fill 52%, n_eff≈25.6) : P(cible|rempli) **48%** · **EV/risk -0.047** (×p_fill ; si rempli -0.79% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→42% · +3.0%→35% · +5.0%→12% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.58% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.485% vs midi 1.221% vs clôture 1.294% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. -0.819% ; recovery-V 35%
- **σ réalisé intraday** 4.24% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 811412.5 (VA 807737.5–818762.5 ; dernier close 815000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 36% · rebond 76% · **stop −5.3%** sous le fill (sous le bruit) · cible +2.16% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 35% (gap-down >1% 17% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.68% (p90 −3.95%) · haut méd +0.92% · range méd 2.89%
- Excursion ouverture 15min (n=160) : bas méd −1.98% (p90 −4.5%) · haut méd +1.03% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −2.22% (p90 −4.9%) · haut méd +1.05% · range méd 3.82%
- Excursion ouverture 60min (n=160) : bas méd −2.46% (p90 −5.2%) · haut méd +1.1% · range méd 4.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 814000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 73% (108/159) · gap 27% · délai 0.1min · rebond 54% (58/108) (MFE +1.15%)
   - −1.0% : fill 30min 54% · séance 70% (100/159) · gap 17% · délai 0.3min · rebond 62% (61/100) (MFE +1.43%)
   - −1.5% : fill 30min 48% · séance 64% (89/159) · gap 13% · délai 0.7min · rebond 68% (59/89) (MFE +1.44%)
   - −2.0% : fill 30min 39% · séance 58% (79/159) · gap 10% · délai 1.2min · rebond 75% (57/79) (MFE +1.78%)
   - −3.0% : fill 30min 31% · séance 47% (64/159) · gap 7% · délai 4.6min · rebond 76% (49/64) (MFE +2.09%)
   - −4.0% : fill 30min 21% · séance 36% (49/159) · gap 3% · délai 16.4min · rebond 76% (35/49) (MFE +2.16%)
   - −5.0% : fill 30min 14% · séance 28% (39/159) · gap 3% · délai 29.2min · rebond 74% (28/39) (MFE +2.32%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.7%) → stop au-delà de −2.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.19%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=828 jambes) : jambe baissière méd −1.22% (p90 −3.3%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 100% (48/48) · rebond 52% (25/48)
      · −2.0% : fill 96% (42/48) · rebond 74% (28/42)
      · −3.0% : fill 86% (37/48) · rebond 76% (27/37)
      · −4.0% : fill 73% (31/48) · rebond 74% (22/31)
      · −5.0% : fill 56% (25/48) · rebond 79% (19/25)
   - **flat** (18 séances) :
      · −1.0% : fill 96% (17/18) · rebond 74% (12/17)
      · −2.0% : fill 72% (13/18) · rebond 73% (11/13)
      · −3.0% : fill 56% (11/18) · rebond 50% (8/11)
      · −4.0% : fill 50% (8/18) · rebond 62% (4/8)
      · −5.0% : fill 50% (8/18) · rebond 73% (6/8)
   - **gap-up** (93 séances) :
      · −1.0% : fill 47% (35/93) · rebond 68% (24/35)
      · −2.0% : fill 33% (24/93) · rebond 78% (18/24)
      · −3.0% : fill 23% (16/93) · rebond 89% (14/16)
      · −4.0% : fill 13% (10/93) · rebond 92% (9/10)
      · −5.0% : fill 8% (6/93) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 48% si les 15 1res min sont vertes (68 cas) · 32% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 38% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **72%** · continue >prix actuel 42% ; creux résiduel méd -1.79% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.66% → **scale +1.57% / runner +2.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **17%** (continue à baisser 41%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.95%** (au-delà de la MAE q10 -4.95%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.07% .. +2.82%] · haut q95 +4.31% · bas q05 -5.47%
   - 60min (n=160) : retour [-5.63% .. +2.6%] · haut q95 +4.52% · bas q05 -6.01%
   - 2h (n=160) : retour [-6.5% .. +3.64%] · haut q95 +4.86% · bas q05 -7.23%
   - 4h (n=160) : retour [-6.91% .. +3.52%] · haut q95 +5.13% · bas q05 -8.37%
   - 6h (n=160) : retour [-7.21% .. +4.61%] · haut q95 +6.08% · bas q05 -9.02%
   - session (n=160) : retour [-7.38% .. +5.23%] · haut q95 +6.1% · bas q05 -9.48%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 17.2  _(pas de tendance nette)_
- **MACD** : hist 12356.66  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 21.6%
- **ATR** : 44116.69 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.265  _(accumulation)_
- **Vol ratio** : 1.55  _(volume au-dessus de la moyenne)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 752013.37 · MA50 818722.56 · MA200 921183.99  _(prix > MA20)_
- **Dist MA** : MA20 +8.2% · MA50 -0.6% · MA200 -11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (618715 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
