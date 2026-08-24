# 267260

**Generated** : 2026-08-24T21:52:07.878054+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩716000.00  

> 🟡 **WAIT-FOR-DIP** — spot +3.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩716000.00 (+3.5% vs entrée) · entrée ₩691826.22 · stop ₩636480.13 · T1 ₩739394.55 · R/R 0.86  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk 0.015 _(réel 5 s)_ (GBM -0.194) · ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩686504.85–₩697147.60 (mid ₩691826.22)
- Spot actuel : ₩716000.00 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : ₩636480.13 (stop swing_plan-based (-13.43%))
- Targets : T1 ₩739394.55 · R/R 0.86 | T2 ₩755399.74 · R/R 1.15 | T3 ₩771404.92 · R/R 1.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩636480.13


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.43 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.638 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2436** [0.1843 ; 0.3114] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4612** [0.4092 ; 0.5139] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4988** [0.4463 ; 0.5513] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.7 pt), swing (39.9 pt), deep (33.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.39 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.99 % contre 5.18 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.79 % vs -11.89 % si l'on extrapolait par √5 _(rapport 0.907 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0429** (β de hausse 0.8223, asymétrie 1.2683) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.194 | EV/share : ₩-10730.225 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 71.3 | bear 6.0 | side 22.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.38% → cible +6.876% / stop −8.0%, p_fill 57%, n_eff≈26.6) : P(cible|rempli) **11%** · **EV/risk +0.015** (×p_fill ; si rempli +0.22% du capital)
  - **swing** (entrée dip −7.432% → cible +8.574% / stop −6.48%, p_fill 31%, n_eff≈19.9) : P(cible|rempli) **31%** · **EV/risk -0.075** (×p_fill ; si rempli -1.56% du capital)
  - **deep** (entrée dip −11.483% → cible +12.125% / stop −10.165%, p_fill 34%, n_eff≈17.1) : P(cible|rempli) **10%** · **EV/risk -0.255** (×p_fill ; si rempli -7.65% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→44% · +3.0%→36% · +5.0%→11% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.6% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.417% vs midi 1.21% vs clôture 1.27% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -1.505% ; recovery-V 27%
- **σ réalisé intraday** 4.396% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 65% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 718850.0 (VA 715350.0–720950.0 ; dernier close 719000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 83% · **stop −5.04%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.55 (high win-rate)
- Gaps overnight (n=158) : méd. 1.14% · baisse 37% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=159) : bas méd −1.87% (p90 −4.01%) · haut méd +0.95% · range méd 2.93%
- Excursion ouverture 15min (n=159) : bas méd −2.09% (p90 −4.63%) · haut méd +1.04% · range méd 3.47%
- Excursion ouverture 30min (n=159) : bas méd −2.31% (p90 −4.97%) · haut méd +1.06% · range méd 3.81%
- Excursion ouverture 60min (n=159) : bas méd −2.67% (p90 −5.52%) · haut méd +1.12% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 719000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 74% (113/158) · gap 30% · délai 0.0min · rebond 54% (63/113) (MFE +1.16%)
   - −1.0% : fill 30min 54% · séance 70% (105/158) · gap 21% · délai 0.2min · rebond 59% (63/105) (MFE +1.24%)
   - −1.5% : fill 30min 47% · séance 64% (91/158) · gap 15% · délai 0.4min · rebond 62% (58/91) (MFE +1.27%)
   - −2.0% : fill 30min 43% · séance 60% (83/158) · gap 12% · délai 0.7min · rebond 70% (57/83) (MFE +1.61%)
   - −3.0% : fill 30min 32% · séance 48% (65/158) · gap 7% · délai 1.8min · rebond 74% (45/65) (MFE +1.68%)
   - −4.0% : fill 30min 24% · séance 39% (53/158) · gap 5% · délai 7.9min · rebond 79% (42/53) (MFE +2.09%)
   - −5.0% : fill 30min 15% · séance 31% (41/158) · gap 3% · délai 37.5min · rebond 83% (32/41) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.32%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −3.32%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.63% (p90 −4.83%) → stop au-delà de −3.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.22% (p90 −3.34%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 49% (28/53)
      · −2.0% : fill 94% (46/54) · rebond 64% (28/46)
      · −3.0% : fill 87% (40/54) · rebond 74% (27/40)
      · −4.0% : fill 76% (35/54) · rebond 78% (28/35)
      · −5.0% : fill 63% (27/54) · rebond 84% (21/27)
   - **flat** (19 séances) :
      · −1.0% : fill 92% (16/19) · rebond 63% (9/16)
      · −2.0% : fill 85% (14/19) · rebond 69% (10/14)
      · −3.0% : fill 70% (12/19) · rebond 66% (8/12)
      · −4.0% : fill 55% (8/19) · rebond 76% (6/8)
      · −5.0% : fill 41% (7/19) · rebond 89% (6/7)
   - **gap-up** (85 séances) :
      · −1.0% : fill 48% (36/85) · rebond 70% (26/36)
      · −2.0% : fill 34% (23/85) · rebond 81% (19/23)
      · −3.0% : fill 22% (13/85) · rebond 80% (10/13)
      · −4.0% : fill 15% (10/85) · rebond 82% (8/10)
      · −5.0% : fill 10% (7/85) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 34% en base · 48% si les 15 1res min sont vertes (69 cas) · 27% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 69% si début vert vs 12% si rouge (base 34% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -1.87% (q20 -3.48%) → **SL/trailing à −3.48%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.35% → **scale +1.46% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **12%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.26%** (au-delà de la MAE q10 -5.26%), cible rebond +1.52% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-5.07% .. +2.68%] · haut q95 +3.91% · bas q05 -5.58%
   - 60min (n=159) : retour [-5.64% .. +2.6%] · haut q95 +4.36% · bas q05 -6.01%
   - 2h (n=159) : retour [-6.77% .. +3.66%] · haut q95 +4.93% · bas q05 -7.35%
   - 4h (n=159) : retour [-6.94% .. +3.76%] · haut q95 +5.24% · bas q05 -8.41%
   - 6h (n=159) : retour [-7.61% .. +3.71%] · haut q95 +6.2% · bas q05 -9.23%
   - session (n=159) : retour [-7.47% .. +3.89%] · haut q95 +6.26% · bas q05 -9.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 57.7  _(momentum haussier)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist 5580.801  _(pas de croisement recent)_
- **BB** : %B 0.44 · largeur 34.1%
- **ATR** : 42949.28 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.047  _(neutre)_
- **Vol ratio** : 0.24  _(volume atone)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 730786.12 · MA50 847907.44 · MA200 923702.72  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 -15.6% · MA200 -22.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763957 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
