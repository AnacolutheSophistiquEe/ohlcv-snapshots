# SMR

**Generated** : 2026-07-23T22:04:11.807832+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.81  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $8.81 (+7.7% vs entrée) · entrée $8.18 · stop $7.99 · T1 $8.37 · R/R 1.0  
> ↳ P(T1 av. stop) 51 % · EV/risk 0.023 · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.31% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.14–$8.22 (mid $8.18)
- Spot actuel : $8.81 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : $7.99 (stop swing_plan-based (-16.49%))
- Targets : T1 $8.37 · R/R 1.0 | T2 $8.56 · R/R 2.0 | T3 $8.75 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.99


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : $0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 66.4 | bear 25.0 | side 8.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→59% · +5.0%→39% · +8.0%→18%
- Range intraday médian 7.73% (p90 12.61%) · excursion haute méd. +3.65% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.042% vs midi 1.539% vs clôture 1.753% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.085% ; recovery-V 28%
- **σ réalisé intraday** 4.754% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 63% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 8.5413 (VA 8.5206–8.7281 ; dernier close 8.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 53% · rebond 78% · **stop −6.09%** sous le fill (sous le bruit) · cible +2.52% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 58% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.33%) · haut méd +1.07% · range méd 2.75%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −3.81%) · haut méd +1.4% · range méd 3.5%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −4.74%) · haut méd +1.96% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −6.0%) · haut méd +2.62% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (131/159) · gap 49% · délai 0.0min · rebond 68% (82/131) (MFE +1.75%)
   - −1.0% : fill 30min 68% · séance 78% (125/159) · gap 41% · délai 0.0min · rebond 68% (83/125) (MFE +2.08%)
   - −1.5% : fill 30min 62% · séance 76% (119/159) · gap 38% · délai 0.0min · rebond 74% (87/119) (MFE +2.22%)
   - −2.0% : fill 30min 57% · séance 69% (112/159) · gap 28% · délai 0.2min · rebond 68% (80/112) (MFE +2.38%)
   - −3.0% : fill 30min 46% · séance 60% (100/159) · gap 10% · délai 2.2min · rebond 75% (81/100) (MFE +2.57%)
   - −4.0% : fill 30min 35% · séance 53% (85/159) · gap 5% · délai 9.6min · rebond 78% (66/85) (MFE +2.52%)
   - −5.0% : fill 30min 24% · séance 41% (63/159) · gap 3% · délai 19.5min · rebond 67% (45/63) (MFE +1.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.7%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.77% (p90 −2.72%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.9%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1175 jambes) : jambe baissière méd −1.39% (p90 −3.2%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 69% (55/83)
      · −2.0% : fill 94% (79/83) · rebond 75% (59/79)
      · −3.0% : fill 83% (74/83) · rebond 77% (61/74)
      · −4.0% : fill 75% (65/83) · rebond 84% (54/65)
      · −5.0% : fill 58% (46/83) · rebond 69% (35/46)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 58% si les 15 1res min sont vertes (71 cas) · 32% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 83% si début vert vs 8% si rouge (base 44% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **83%** · continue >prix actuel 43% ; creux résiduel méd -2.28% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.27% → **scale +1.69% / runner +3.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **8%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.5% .. +4.91%] · haut q95 +6.59% · bas q05 -6.03%
   - 60min (n=160) : retour [-6.55% .. +5.57%] · haut q95 +7.84% · bas q05 -7.85%
   - 2h (n=160) : retour [-7.76% .. +7.68%] · haut q95 +11.18% · bas q05 -8.87%
   - 4h (n=160) : retour [-8.58% .. +7.83%] · haut q95 +11.16% · bas q05 -10.71%
   - 6h (n=160) : retour [-8.08% .. +8.49%] · haut q95 +11.39% · bas q05 -10.71%
   - session (n=160) : retour [-8.1% .. +10.34%] · haut q95 +11.56% · bas q05 -10.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.2  _(momentum baissier)_
- **ADX** : 22.3  _(pas de tendance nette)_
- **MACD** : hist 0.06  _(bullish_recent)_
- **BB** : %B 0.43 · largeur 36.8%
- **ATR** : 0.63 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.015  _(neutre)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 42.0  _(transition)_
- **MA** : MA20 9.03 · MA50 10.33 · MA200 17.41  _(prix < MA20)_
- **Dist MA** : MA20 -2.4% · MA50 -14.7% · MA200 -49.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83458 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
