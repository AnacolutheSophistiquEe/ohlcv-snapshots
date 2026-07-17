# 326030

**Generated** : 2026-07-17T00:21:53.697866+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩79400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩79400.00 (+6.4% vs entrée) · entrée ₩74592.86 · stop ₩68625.43 · T1 ₩76261.06 · R/R 0.28  
> ↳ P(T1 av. stop) 24 % · EV/risk -0.084 · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=53 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩74259.22–₩74926.50 (mid ₩74592.86)
- Spot actuel : ₩79400.00 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : ₩68625.43 (stop swing_plan-based (-14.31%))
- Targets : T1 ₩76261.06 · R/R 0.28 | T2 ₩77929.26 · R/R 0.56 | T3 ₩79597.47 · R/R 0.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩68625.43


## Edge, scénarios & sizing

- EV/risk : -0.084 | EV/share : ₩-502.810 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.13 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=53 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.0 | bear 57.7 | side 31.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 53 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→47% · +2.0%→32% · +3.0%→8% · +5.0%→2% · +8.0%→0%
- Range intraday médian 3.08% (p90 5.38%) · excursion haute méd. +0.9% / basse méd. −1.91%
- Profil de vol intra : ouverture 1.842% vs midi 0.618% vs clôture 0.589% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (53 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 13% · trend ↑0%/↓5% ; spike-down 63% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; neutre — autocorr -0.019)_ ; drift intra méd. -0.685% ; recovery-V 27%
- **σ réalisé intraday** 2.116% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 65% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 97020.0 (VA 96700.0–97580.0 ; dernier close 97000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 10% · **stop −3.88%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.14 (high win-rate)
- Gaps overnight (n=52) : méd. 0.3% · baisse 35% (gap-down >1% 19% · >2% 16%)
- Excursion ouverture 5min (n=53) : bas méd −0.5% (p90 −1.69%) · haut méd +0.2% · range méd 1.15%
- Excursion ouverture 15min (n=53) : bas méd −0.72% (p90 −2.21%) · haut méd +0.33% · range méd 1.33%
- Excursion ouverture 30min (n=53) : bas méd −1.03% (p90 −2.23%) · haut méd +0.41% · range méd 1.53%
- Excursion ouverture 60min (n=53) : bas méd −1.27% (p90 −2.48%) · haut méd +0.46% · range méd 2.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 63% (33/52) · gap 23% · délai 0.1min · rebond 23% (8/33) (MFE +0.42%)
   - −1.0% : fill 30min 41% · séance 56% (30/52) · gap 19% · délai 0.6min · rebond 32% (10/30) (MFE +0.5%)
   - −1.5% : fill 30min 34% · séance 44% (22/52) · gap 18% · délai 0.1min · rebond 45% (10/22) (MFE +0.64%)
   - −2.0% : fill 30min 25% · séance 36% (18/52) · gap 16% · délai 0.9min · rebond 41% (7/18) (MFE +0.84%)
   - −3.0% : fill 30min 11% · séance 20% (10/52) · gap 5% · délai 11.4min · rebond 8% (1/10) (MFE +0.16%)
   - −4.0% : fill 30min 9% · séance 16% (8/52) · gap 5% · délai 18.9min · rebond 10% (1/8) (MFE +0.53%)
   - −5.0% : fill 30min 5% · séance 15% (7/52) · gap 5% · délai 67.7min · rebond 26% (2/7) (MFE +0.77%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −1.55%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.28% (p90 −1.37%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=118 jambes) : jambe baissière méd −1.29% (p90 −3.17%) · ~5.1 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (16 séances) :
      · −1.0% : fill 100% (16/16) · rebond 31% (5/16)
      · −2.0% : fill 75% (12/16) · rebond 37% (4/12)
      · −3.0% : fill 43% (7/16) · rebond 12% (1/7)
      · −4.0% : fill 38% (6/16) · rebond 14% (1/6)
      · −5.0% : fill 32% (5/16) · rebond 15% (1/5)
   - **flat** (10 séances) :
      · −1.0% : fill 74% (7/10) · rebond 21% (2/7)
      · −2.0% : fill 58% (5/10) · rebond 59% (3/5)
      · −3.0% : fill 22% (2/10) · rebond 0% (0/2)
      · −4.0% : fill 13% (1/10) · rebond 0% (0/1)
      · −5.0% : fill 13% (1/10) · rebond 100% (1/1)
   - **gap-up** (26 séances) :
      · −1.0% : fill 24% (7/26) · rebond 43% (3/7)
      · −2.0% : fill 4% (1/26) · rebond 0% (0/1)
      · −3.0% : fill 4% (1/26) · rebond 0% (0/1)
      · −4.0% : fill 4% (1/26) · rebond 0% (0/1)
      · −5.0% : fill 4% (1/26) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=53) : 46% en base · 83% si les 15 1res min sont vertes (16 cas) · 29% si rouges (37 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=53) : COUDE à **2:43** → P(séance verte=clôture>ouverture) 96% si début vert vs 13% si rouge (base 46% · écart 83 pts) ; prédictivité sature ensuite (plafond brut 154min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=20) : tient le vert **96%** · continue >prix actuel 44% ; creux résiduel méd -0.86% (q20 -1.05%) → **SL/trailing à −1.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.3% / q75 +0.77% → **scale +0.3% / runner +0.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=33) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.89%** (au-delà de la MAE q10 -2.89%), cible rebond +0.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=53) : retour [-2.19% .. +1.24%] · haut q95 +2.14% · bas q05 -2.6%
   - 60min (n=53) : retour [-3.44% .. +1.68%] · haut q95 +3.41% · bas q05 -3.82%
   - 2h (n=53) : retour [-3.47% .. +1.79%] · haut q95 +3.44% · bas q05 -4.02%
   - 4h (n=53) : retour [-4.19% .. +2.18%] · haut q95 +3.44% · bas q05 -6.11%
   - 6h (n=53) : retour [-4.84% .. +2.16%] · haut q95 +3.44% · bas q05 -6.15%
   - session (n=53) : retour [-5.36% .. +2.3%] · haut q95 +3.44% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 1.81%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 45.1  _(neutre)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -474.457  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 19.1%
- **ATR** : 4807.14 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 83755.0 · MA50 89394.0 · MA200 107494.0  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -11.2% · MA200 -26.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (59150 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
