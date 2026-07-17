# 326030

**Generated** : 2026-07-17T21:58:16.259570+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩79400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩79400.00 (+6.4% vs entrée) · entrée ₩74592.86 · stop ₩73150.71 · T1 ₩76261.06 · R/R 1.16  
> ↳ P(T1 av. stop) 33 % · EV/risk -0.192 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.93% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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
- Stop : ₩73150.71 (stop swing_plan-based (-14.31%))
- Targets : T1 ₩76261.06 · R/R 1.16 | T2 ₩77929.26 · R/R 2.31 | T3 ₩79597.47 · R/R 3.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩73150.71


## Edge, scénarios & sizing

- EV/risk : -0.192 | EV/share : ₩-277.224 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 9 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.0 | bear 57.7 | side 31.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→41% · +3.0%→25% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.23%) · excursion haute méd. +1.47% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.65% vs midi 0.755% vs clôture 0.786% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 16% · trend ↑2%/↓2% ; spike-down 60% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; mean-reverting — autocorr -0.039)_ ; drift intra méd. -0.571% ; recovery-V 19%
- **σ réalisé intraday** 3.341% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 65% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 78842.5 (VA 78162.5–80457.5 ; dernier close 79100.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=133) : méd. 0.12% · baisse 41% (gap-down >1% 14% · >2% 8%)
- Excursion ouverture 5min (n=134) : bas méd −0.77% (p90 −2.19%) · haut méd +0.64% · range méd 1.85%
- Excursion ouverture 15min (n=134) : bas méd −0.94% (p90 −2.95%) · haut méd +0.7% · range méd 2.15%
- Excursion ouverture 30min (n=134) : bas méd −1.09% (p90 −2.99%) · haut méd +0.85% · range méd 2.56%
- Excursion ouverture 60min (n=134) : bas méd −1.27% (p90 −3.33%) · haut méd +1.07% · range méd 2.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 79100.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 78% (97/133) · gap 24% · délai 0.6min · rebond 50% (40/97) (MFE +0.95%)
   - −1.0% : fill 30min 54% · séance 68% (87/133) · gap 14% · délai 2.3min · rebond 51% (40/87) (MFE +1.01%)
   - −1.5% : fill 30min 39% · séance 55% (66/133) · gap 8% · délai 4.8min · rebond 54% (32/66) (MFE +1.06%)
   - −2.0% : fill 30min 26% · séance 48% (55/133) · gap 8% · délai 17.4min · rebond 61% (30/55) (MFE +1.16%)
   - −3.0% : fill 30min 12% · séance 35% (36/133) · gap 4% · délai 81.8min · rebond 54% (15/36) (MFE +1.15%)
   - −4.0% : fill 30min 8% · séance 23% (25/133) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 17% (19/133) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −2.87%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.0%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.41%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=427 jambes) : jambe baissière méd −1.15% (p90 −2.55%) · ~8.2 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (39 séances) :
      · −1.0% : fill 100% (39/39) · rebond 61% (20/39)
      · −2.0% : fill 71% (27/39) · rebond 58% (13/27)
      · −3.0% : fill 51% (18/39) · rebond 49% (7/18)
      · −4.0% : fill 42% (15/39) · rebond 65% (8/15)
      · −5.0% : fill 33% (12/39) · rebond 85% (8/12)
   - **flat** (34 séances) :
      · −1.0% : fill 70% (24/34) · rebond 30% (8/24)
      · −2.0% : fill 55% (17/34) · rebond 70% (11/17)
      · −3.0% : fill 41% (10/34) · rebond 66% (5/10)
      · −4.0% : fill 35% (8/34) · rebond 39% (3/8)
      · −5.0% : fill 25% (6/34) · rebond 79% (4/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (24/60) · rebond 58% (12/24)
      · −2.0% : fill 28% (11/60) · rebond 56% (6/11)
      · −3.0% : fill 21% (8/60) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/60) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 36% en base · 68% si les 15 1res min sont vertes (47 cas) · 16% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=134) : COUDE à **13min** → P(séance verte=clôture>ouverture) 72% si début vert vs 15% si rouge (base 36% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=46) : tient le vert **72%** · continue >prix actuel 61% ; creux résiduel méd -1.17% (q20 -2.85%) → **SL/trailing à −2.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.97% / q75 +3.13% → **scale +1.97% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **15%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-2.91% .. +2.55%] · haut q95 +3.68% · bas q05 -4.05%
   - 60min (n=134) : retour [-3.85% .. +2.56%] · haut q95 +4.26% · bas q05 -4.55%
   - 2h (n=134) : retour [-3.5% .. +3.96%] · haut q95 +4.56% · bas q05 -4.74%
   - 4h (n=134) : retour [-4.27% .. +5.39%] · haut q95 +6.32% · bas q05 -5.83%
   - 6h (n=134) : retour [-4.72% .. +4.3%] · haut q95 +7.13% · bas q05 -6.05%
   - session (n=134) : retour [-4.81% .. +4.82%] · haut q95 +7.13% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.29%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80936 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
