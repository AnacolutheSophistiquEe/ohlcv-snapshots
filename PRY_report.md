# PRY

**Generated** : 2026-07-17T21:48:04.355517+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €125.35  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €125.35 (+4.3% vs entrée) · entrée €120.18 · stop €118.24 · T1 €124.06 · R/R 2.0  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.033 _(réel 5 s)_ (GBM 0.181) · ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -207 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €119.41–€120.95 (mid €120.18)
- Spot actuel : €125.35 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : €118.24 (stop swing_plan-based (-5.67%))
- Targets : T1 €124.06 · R/R 2.0 | T2 €127.93 · R/R 3.99 | T3 €131.81 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €118.24


## Edge, scénarios & sizing

- EV/risk : 0.181 | EV/share : €0.352 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 19 % | T3 4 %
- Kelly (position) : f* 0.057 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.7 | bear 36.1 | side 44.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 125.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.872% → cible +1.442% / stop −1.526%, p_fill 43%, n_eff≈17.4) : P(cible|rempli) **18%** · **EV/risk -0.210** (×p_fill ; si rempli -0.74% du capital)
  - **swing** (entrée dip −4.124% → cible +3.224% / stop −1.612%, p_fill 39%, n_eff≈14.3) : P(cible|rempli) **33%** · **EV/risk -0.033** (×p_fill ; si rempli -0.13% du capital)
  - **deep** (entrée dip −6.375% → cible +4.56% / stop −2.28%, p_fill 29%, n_eff≈11.2) : P(cible|rempli) **52%** · **EV/risk +0.160** (×p_fill ; si rempli +1.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→44% · +3.0%→34% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.02% (p90 6.32%) · excursion haute méd. +1.67% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.259% vs midi 0.822% vs clôture 1.112% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.389% ; recovery-V 16%
- **σ réalisé intraday** 2.659% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 62% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 130.213 (VA 128.725–130.585 ; dernier close 130.46)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 68% · **stop −3.45%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.39 (high win-rate)
- Gaps overnight (n=133) : méd. 0.2% · baisse 43% (gap-down >1% 20% · >2% 12%)
- Excursion ouverture 5min (n=134) : bas méd −0.67% (p90 −2.28%) · haut méd +0.38% · range méd 1.3%
- Excursion ouverture 15min (n=134) : bas méd −0.79% (p90 −2.85%) · haut méd +0.61% · range méd 1.67%
- Excursion ouverture 30min (n=134) : bas méd −0.91% (p90 −3.03%) · haut méd +0.74% · range méd 1.82%
- Excursion ouverture 60min (n=134) : bas méd −1.07% (p90 −3.23%) · haut méd +0.89% · range méd 2.08%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 130.46 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (97/133) · gap 27% · délai 0.2min · rebond 60% (61/97) (MFE +1.25%)
   - −1.0% : fill 30min 50% · séance 64% (82/133) · gap 20% · délai 0.3min · rebond 57% (49/82) (MFE +1.56%)
   - −1.5% : fill 30min 34% · séance 53% (70/133) · gap 17% · délai 0.4min · rebond 50% (38/70) (MFE +0.94%)
   - −2.0% : fill 30min 25% · séance 43% (56/133) · gap 12% · délai 4.0min · rebond 53% (34/56) (MFE +1.15%)
   - −3.0% : fill 30min 14% · séance 34% (41/133) · gap 5% · délai 76.5min · rebond 58% (27/41) (MFE +1.57%)
   - −4.0% : fill 30min 4% · séance 19% (21/133) · gap 2% · délai 182.7min · rebond 68% (15/21) (MFE +1.36%)
   - −5.0% : fill 30min 2% · séance 11% (14/133) · gap 2% · délai 274.5min · rebond 81% (11/14) (MFE +1.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.17% (p90 −1.69%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.57%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=405 jambes) : jambe baissière méd −1.1% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 87% (43/48) · rebond 52% (25/43)
      · −2.0% : fill 67% (34/48) · rebond 60% (23/34)
      · −3.0% : fill 56% (26/48) · rebond 62% (19/26)
      · −4.0% : fill 30% (13/48) · rebond 63% (9/13)
      · −5.0% : fill 24% (10/48) · rebond 86% (8/10)
   - **flat** (25 séances) :
      · −1.0% : fill 60% (13/25) · rebond 59% (8/13)
      · −2.0% : fill 30% (6/25) · rebond 75% (4/6)
      · −3.0% : fill 28% (5/25) · rebond 40% (2/5)
      · −4.0% : fill 13% (3/25) · rebond 59% (2/3)
      · −5.0% : fill 7% (2/25) · rebond 25% (1/2)
   - **gap-up** (60 séances) :
      · −1.0% : fill 47% (26/60) · rebond 62% (16/26)
      · −2.0% : fill 28% (16/60) · rebond 30% (7/16)
      · −3.0% : fill 20% (10/60) · rebond 59% (6/10)
      · −4.0% : fill 14% (5/60) · rebond 81% (4/5)
      · −5.0% : fill 3% (2/60) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 52% en base · 78% si les 15 1res min sont vertes (64 cas) · 28% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=134) : COUDE à **1:04** → P(séance verte=clôture>ouverture) 86% si début vert vs 23% si rouge (base 52% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **86%** · continue >prix actuel 66% ; creux résiduel méd -1.22% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.51% → **scale +1.68% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **23%** (continue à baisser 61%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.07%** (au-delà de la MAE q10 -4.07%), cible rebond +1.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-2.91% .. +2.74%] · haut q95 +3.46% · bas q05 -3.38%
   - 60min (n=134) : retour [-2.94% .. +2.59%] · haut q95 +3.93% · bas q05 -3.5%
   - 2h (n=134) : retour [-3.61% .. +3.58%] · haut q95 +4.12% · bas q05 -3.71%
   - 4h (n=134) : retour [-3.47% .. +3.7%] · haut q95 +4.61% · bas q05 -4.49%
   - 6h (n=134) : retour [-3.72% .. +3.81%] · haut q95 +5.3% · bas q05 -4.7%
   - session (n=134) : retour [-4.52% .. +4.93%] · haut q95 +6.13% · bas q05 -5.75%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.2% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.38%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.9  _(survente)_
- **ADX** : 23.2  _(pas de tendance nette)_
- **MACD** : hist -1.465  _(pas de croisement recent)_
- **BB** : %B -0.01 · largeur 21.0%
- **ATR** : 6.26 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.162  _(distribution)_
- **Vol ratio** : 2.51  _(volume au-dessus de la moyenne)_
- **Choppiness** : 44.3  _(transition)_
- **MA** : MA20 140.42 · MA50 145.31 · MA200 108.63  _(prix < MA20)_
- **Dist MA** : MA20 -10.7% · MA50 -13.7% · MA200 +15.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92987 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
