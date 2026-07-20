# PRY

**Generated** : 2026-07-20T21:46:54.771625+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €125.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €125.00 (+1.8% vs entrée) · entrée €122.74 · stop €120.89 · T1 €124.48 · R/R 0.94  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.197 _(réel 5 s)_ (GBM 0.088) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €122.39–€123.09 (mid €122.74)
- Spot actuel : €125.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €120.89 (stop swing_plan-based (-5.51%))
- Targets : T1 €124.48 · R/R 0.94 | T2 €126.23 · R/R 1.89 | T3 €127.98 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €120.89


## Edge, scénarios & sizing

- EV/risk : 0.088 | EV/share : €0.163 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 32 % | T3 14 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.4 | bear 52.1 | side 21.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 125.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.815% → cible +1.423% / stop −1.502%, p_fill 46%, n_eff≈17.6) : P(cible|rempli) **19%** · **EV/risk -0.197** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −3.983% → cible +3.182% / stop −1.591%, p_fill 38%, n_eff≈14.6) : P(cible|rempli) **34%** · **EV/risk -0.019** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −6.159% → cible +4.499% / stop −2.25%, p_fill 33%, n_eff≈11.6) : P(cible|rempli) **45%** · **EV/risk +0.105** (×p_fill ; si rempli +0.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→45% · +3.0%→34% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.02% (p90 6.32%) · excursion haute méd. +1.82% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.27% vs midi 0.82% vs clôture 1.121% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr 0.01)_ ; drift intra méd. -0.441% ; recovery-V 15%
- **σ réalisé intraday** 2.653% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 64% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 124.7053 (VA 124.3708–125.7088 ; dernier close 125.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 36% · rebond 61% · **stop −2.89%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.55 (high win-rate)
- Gaps overnight (n=134) : méd. 0.14% · baisse 44% (gap-down >1% 21% · >2% 14%)
- Excursion ouverture 5min (n=135) : bas méd −0.61% (p90 −2.22%) · haut méd +0.38% · range méd 1.3%
- Excursion ouverture 15min (n=135) : bas méd −0.77% (p90 −2.83%) · haut méd +0.65% · range méd 1.69%
- Excursion ouverture 30min (n=135) : bas méd −0.9% (p90 −2.98%) · haut méd +0.78% · range méd 1.84%
- Excursion ouverture 60min (n=135) : bas méd −1.08% (p90 −3.22%) · haut méd +0.9% · range méd 2.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 125.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (98/134) · gap 28% · délai 0.2min · rebond 59% (61/98) (MFE +1.16%)
   - −1.0% : fill 30min 51% · séance 64% (83/134) · gap 21% · délai 0.2min · rebond 55% (49/83) (MFE +1.46%)
   - −1.5% : fill 30min 35% · séance 54% (71/134) · gap 18% · délai 0.4min · rebond 52% (39/71) (MFE +1.07%)
   - −2.0% : fill 30min 27% · séance 44% (57/134) · gap 14% · délai 3.8min · rebond 55% (35/57) (MFE +1.2%)
   - −3.0% : fill 30min 16% · séance 36% (42/134) · gap 5% · délai 72.3min · rebond 61% (28/42) (MFE +1.6%)
   - −4.0% : fill 30min 4% · séance 21% (22/134) · gap 2% · délai 160.8min · rebond 62% (15/22) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 13% (15/134) · gap 2% · délai 332.6min · rebond 84% (12/15) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.2% (p90 −1.67%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.28% (p90 −1.6%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.57%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.11% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 88% (44/49) · rebond 49% (25/44)
      · −2.0% : fill 69% (35/49) · rebond 63% (24/35)
      · −3.0% : fill 59% (27/49) · rebond 66% (20/27)
      · −4.0% : fill 33% (14/49) · rebond 53% (9/14)
      · −5.0% : fill 28% (11/49) · rebond 89% (9/11)
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
- **P(clôture VERTE) selon le drive 15min** (n=135) : 51% en base · 78% si les 15 1res min sont vertes (64 cas) · 28% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=135) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 85% si début vert vs 23% si rouge (base 51% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **85%** · continue >prix actuel 65% ; creux résiduel méd -1.26% (q20 -2.15%) → **SL/trailing à −2.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.65% → **scale +1.59% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **23%** (continue à baisser 60%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-2.9% .. +2.73%] · haut q95 +3.46% · bas q05 -3.38%
   - 60min (n=135) : retour [-2.94% .. +2.54%] · haut q95 +3.93% · bas q05 -3.49%
   - 2h (n=135) : retour [-3.61% .. +3.54%] · haut q95 +4.11% · bas q05 -3.7%
   - 4h (n=135) : retour [-3.46% .. +3.69%] · haut q95 +4.6% · bas q05 -4.48%
   - 6h (n=135) : retour [-3.72% .. +3.8%] · haut q95 +5.21% · bas q05 -4.69%
   - session (n=135) : retour [-4.41% .. +4.89%] · haut q95 +6.12% · bas q05 -5.71%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.2% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.6  _(survente)_
- **ADX** : 24.3  _(pas de tendance nette)_
- **MACD** : hist -1.604  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 21.1%
- **ATR** : 6.15 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.234  _(distribution)_
- **Vol ratio** : 1.44  _(volume normal)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 138.93 · MA50 144.67 · MA200 108.84  _(prix < MA20)_
- **Dist MA** : MA20 -10.0% · MA50 -13.6% · MA200 +14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93488 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
