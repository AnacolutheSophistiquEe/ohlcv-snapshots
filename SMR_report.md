# SMR

**Generated** : 2026-07-23T00:27:38.670185+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $8.68 (+8.5% vs entrée) · entrée $8.00 · stop $7.80 · T1 $8.19 · R/R 0.95  
> ↳ P(T1 av. stop) 52 % · EV/risk 0.026 · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.55% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.96–$8.04 (mid $8.00)
- Spot actuel : $8.68 (+8.5% au-dessus de la zone — repli à attendre)
- Stop : $7.80 (stop swing_plan-based (-18.01%))
- Targets : T1 $8.19 · R/R 0.95 | T2 $8.38 · R/R 1.9 | T3 $8.57 · R/R 2.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.80


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : $0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 56.4 | bear 32.5 | side 11.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→65% · +3.0%→57% · +5.0%→39% · +8.0%→18%
- Range intraday médian 7.8% (p90 12.61%) · excursion haute méd. +3.65% / basse méd. −3.09%
- Profil de vol intra : ouverture 5.021% vs midi 1.529% vs clôture 1.745% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.102% ; recovery-V 24%
- **σ réalisé intraday** 4.751% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 61% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 8.5708 (VA 8.4995–8.685 ; dernier close 8.71)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 54% · rebond 78% · **stop −6.09%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 57% (gap-down >1% 42% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.15% (p90 −3.36%) · haut méd +1.03% · range méd 2.69%
- Excursion ouverture 15min (n=160) : bas méd −1.65% (p90 −3.81%) · haut méd +1.35% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.86% (p90 −4.76%) · haut méd +1.92% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −6.02%) · haut méd +2.57% · range méd 5.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.71 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 82% (131/159) · gap 50% · délai 0.0min · rebond 68% (82/131) (MFE +1.73%)
   - −1.0% : fill 30min 69% · séance 78% (125/159) · gap 42% · délai 0.0min · rebond 67% (83/125) (MFE +2.03%)
   - −1.5% : fill 30min 64% · séance 75% (119/159) · gap 38% · délai 0.0min · rebond 74% (87/119) (MFE +2.3%)
   - −2.0% : fill 30min 58% · séance 68% (112/159) · gap 29% · délai 0.1min · rebond 68% (80/112) (MFE +2.5%)
   - −3.0% : fill 30min 47% · séance 61% (101/159) · gap 10% · délai 2.1min · rebond 75% (82/101) (MFE +2.58%)
   - −4.0% : fill 30min 36% · séance 54% (86/159) · gap 5% · délai 9.5min · rebond 78% (67/86) (MFE +2.53%)
   - −5.0% : fill 30min 25% · séance 42% (64/159) · gap 3% · délai 19.5min · rebond 67% (46/64) (MFE +1.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.7%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −2.74%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.09% (p90 −2.94%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.39% (p90 −3.18%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 68% (55/83)
      · −2.0% : fill 94% (79/83) · rebond 74% (59/79)
      · −3.0% : fill 86% (75/83) · rebond 77% (62/75)
      · −4.0% : fill 78% (66/83) · rebond 84% (55/66)
      · −5.0% : fill 60% (47/83) · rebond 69% (36/47)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (11/14) · rebond 54% (7/11)
      · −2.0% : fill 69% (9/14) · rebond 22% (4/9)
      · −3.0% : fill 66% (7/14) · rebond 47% (4/7)
      · −4.0% : fill 66% (7/14) · rebond 55% (3/7)
      · −5.0% : fill 56% (6/14) · rebond 80% (5/6)
   - **gap-up** (62 séances) :
      · −1.0% : fill 47% (31/62) · rebond 70% (21/31)
      · −2.0% : fill 34% (24/62) · rebond 67% (17/24)
      · −3.0% : fill 26% (19/62) · rebond 80% (16/19)
      · −4.0% : fill 19% (13/62) · rebond 67% (9/13)
      · −5.0% : fill 14% (11/62) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 57% si les 15 1res min sont vertes (70 cas) · 32% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 78% si début vert vs 14% si rouge (base 43% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -2.25% (q20 -3.67%) → **SL/trailing à −3.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.38% / q75 +4.24% → **scale +2.38% / runner +4.24%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **14%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.51% .. +4.91%] · haut q95 +6.59% · bas q05 -6.03%
   - 60min (n=160) : retour [-6.6% .. +5.58%] · haut q95 +7.86% · bas q05 -7.88%
   - 2h (n=160) : retour [-7.79% .. +7.75%] · haut q95 +11.2% · bas q05 -8.87%
   - 4h (n=160) : retour [-8.6% .. +7.87%] · haut q95 +11.19% · bas q05 -10.71%
   - 6h (n=160) : retour [-8.09% .. +8.54%] · haut q95 +11.4% · bas q05 -10.72%
   - session (n=160) : retour [-8.12% .. +10.42%] · haut q95 +11.59% · bas q05 -10.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.3  _(momentum baissier)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist 0.012  _(bullish_recent)_
- **BB** : %B 0.38 · largeur 38.2%
- **ATR** : 0.68 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.064  _(distribution)_
- **Vol ratio** : 1.35  _(volume normal)_
- **Choppiness** : 36.2  _(marche directionnel)_
- **MA** : MA20 9.1 · MA50 10.42 · MA200 17.57  _(prix < MA20)_
- **Dist MA** : MA20 -4.6% · MA50 -16.7% · MA200 -50.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83427 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
