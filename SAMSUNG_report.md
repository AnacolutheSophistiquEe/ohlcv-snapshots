# 005930

**Generated** : 2026-09-01T21:51:32.383152+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩261000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩261000.00 (+6.1% vs entrée) · entrée ₩245984.21 · stop ₩229698.49 · T1 ₩259855.81 · R/R 0.85  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.133 _(réel 5 s)_ (GBM 0.291) · ¼-Kelly 0.038 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩243209.89–₩248758.53 (mid ₩245984.21)
- Spot actuel : ₩261000.00 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : ₩229698.49 (stop swing_plan-based (-11.99%))
- Targets : T1 ₩259855.81 · R/R 0.85 | T2 ₩273727.40 · R/R 1.7 | T3 ₩287599.00 · R/R 2.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩229698.49


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.99 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.401 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0526** [0.0265 ; 0.0935] _(largeur 6.7 pt, n_eff 173.1)_
   - swing : **0.2423** [0.1994 ; 0.2895] _(largeur 9.0 pt, n_eff 345.6)_
   - deep : **0.198** [0.1586 ; 0.2424] _(largeur 8.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.1 pt), swing (40.4 pt), deep (38.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.7 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.60 % contre 5.83 % aujourd'hui, rapport 0.45)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.36 % vs -7.04 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1701** (β de hausse 1.337, asymétrie 0.8751) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.291 | EV/share : ₩4742.047 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 28 % | T3 14 %
- Kelly (position) : f* 0.153 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 44.1 | bear 7.4 | side 48.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.62% → cible +3.445% / stop −8.0%, p_fill 52%, n_eff≈26.3) : P(cible|rempli) **13%** · **EV/risk -0.046** (×p_fill ; si rempli -0.71% du capital)
  - **swing** (entrée dip −5.75% → cible +5.639% / stop −6.621%, p_fill 43%, n_eff≈20.9) : P(cible|rempli) **35%** · **EV/risk -0.133** (×p_fill ; si rempli -2.04% du capital)
  - **deep** (entrée dip −8.89% → cible +7.975% / stop −10.273%, p_fill 52%, n_eff≈22.7) : P(cible|rempli) **58%** · **EV/risk +0.018** (×p_fill ; si rempli +0.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→48% · +3.0%→39% · +5.0%→25% · +8.0%→5%
- Range intraday médian 6.25% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.176% vs midi 1.378% vs clôture 1.58% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. -0.446% ; recovery-V 26%
- **σ réalisé intraday** 3.902% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 66% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 252662.5 (VA 249412.5–253962.5 ; dernier close 259000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.84% · baisse 44% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.65%) · haut méd +0.6% · range méd 1.56%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.35%) · haut méd +0.94% · range méd 2.15%
- Excursion ouverture 30min (n=160) : bas méd −1.24% (p90 −3.25%) · haut méd +1.07% · range méd 2.62%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −3.59%) · haut méd +1.32% · range méd 3.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 260000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 68% (97/159) · gap 37% · délai 0.0min · rebond 48% (49/97) (MFE +0.93%)
   - −1.0% : fill 30min 46% · séance 59% (88/159) · gap 36% · délai 0.0min · rebond 57% (49/88) (MFE +1.16%)
   - −1.5% : fill 30min 42% · séance 52% (76/159) · gap 29% · délai 0.0min · rebond 59% (44/76) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 49% (71/159) · gap 25% · délai 0.0min · rebond 62% (44/71) (MFE +1.67%)
   - −3.0% : fill 30min 30% · séance 45% (62/159) · gap 23% · délai 0.0min · rebond 54% (35/62) (MFE +1.14%)
   - −4.0% : fill 30min 23% · séance 34% (46/159) · gap 11% · délai 5.6min · rebond 53% (27/46) (MFE +1.24%)
   - −5.0% : fill 30min 14% · séance 26% (36/159) · gap 9% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.97%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.92%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.7%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=771 jambes) : jambe baissière méd −1.24% (p90 −3.02%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 96% (58/61) · rebond 49% (29/58)
      · −2.0% : fill 88% (50/61) · rebond 51% (27/50)
      · −3.0% : fill 86% (47/61) · rebond 48% (25/47)
      · −4.0% : fill 72% (37/61) · rebond 49% (21/37)
      · −5.0% : fill 57% (30/61) · rebond 41% (17/30)
   - **flat** (15 séances) :
      · −1.0% : fill 74% (12/15) · rebond 57% (6/12)
      · −2.0% : fill 49% (8/15) · rebond 82% (6/8)
      · −3.0% : fill 34% (6/15) · rebond 35% (3/6)
      · −4.0% : fill 24% (3/15) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/15) · rebond 100% (3/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 28% (18/83) · rebond 74% (14/18)
      · −2.0% : fill 20% (13/83) · rebond 85% (11/13)
      · −3.0% : fill 16% (9/83) · rebond 82% (7/9)
      · −4.0% : fill 9% (6/83) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/83) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 60% si les 15 1res min sont vertes (79 cas) · 20% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 84% si début vert vs 7% si rouge (base 40% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 74min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **84%** · continue >prix actuel 62% ; creux résiduel méd -0.97% (q20 -3.53%) → **SL/trailing à −3.53%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.83% / q75 +3.55% → **scale +2.83% / runner +3.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.77%** (au-delà de la MAE q10 -6.77%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +2.7%] · haut q95 +3.55% · bas q05 -3.71%
   - 60min (n=160) : retour [-3.12% .. +4.24%] · haut q95 +4.98% · bas q05 -4.86%
   - 2h (n=160) : retour [-4.54% .. +4.71%] · haut q95 +5.88% · bas q05 -5.62%
   - 4h (n=160) : retour [-5.97% .. +5.38%] · haut q95 +6.83% · bas q05 -7.54%
   - 6h (n=160) : retour [-6.93% .. +5.3%] · haut q95 +6.95% · bas q05 -7.75%
   - session (n=160) : retour [-6.48% .. +5.41%] · haut q95 +6.95% · bas q05 -8.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 57.5  _(momentum haussier)_
- **ADX** : 12.5  _(pas de tendance nette)_
- **MACD** : hist 1593.96  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 23.7%
- **ATR** : 16285.71 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.049  _(neutre)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 59.8  _(transition)_
- **MA** : MA20 255150.0 · MA50 271022.5 · MA200 209088.93  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 -3.7% · MA200 +24.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (500668 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
