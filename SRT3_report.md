# SRT3

**Generated** : 2026-07-10T00:03:17.248802+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €231.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €231.10 (+1.3% vs entrée) · entrée €228.07 · stop €221.23 · T1 €231.41 · R/R 0.49  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.085 _(réel 5 s)_ (GBM 0.041) · ¼-Kelly 0.041 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €227.40–€228.74 (mid €228.07)
- Spot actuel : €231.10 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : €221.23 (stop swing_plan-based (-4.48%))
- Targets : T1 €231.41 · R/R 0.49 | T2 €234.76 · R/R 0.98 | T3 €238.10 · R/R 1.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €221.23


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : €0.281 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.165 | ¼-Kelly 0.041 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 48.8 | bear 8.2 | side 42.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 462.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.309% → cible +1.466% / stop −3.0%, p_fill 53%, n_eff≈23.4) : P(cible|rempli) **30%** · **EV/risk -0.085** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −2.888% → cible +3.279% / stop −1.639%, p_fill 33%, n_eff≈14.8) : P(cible|rempli) **50%** · **EV/risk +0.143** (×p_fill ; si rempli +0.70% du capital)
  - **deep** (entrée dip −4.455% → cible +4.637% / stop −2.318%, p_fill 35%, n_eff≈15.2) : P(cible|rempli) **28%** · **EV/risk -0.056** (×p_fill ; si rempli -0.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→45% · +3.0%→24% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.61% (p90 6.59%) · excursion haute méd. +1.89% / basse méd. −1.84%
- Profil de vol intra : ouverture 2.016% vs midi 0.882% vs clôture 1.0% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 53% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr 0.028)_ ; drift intra méd. -0.077% ; recovery-V 25%
- **σ réalisé intraday** 2.331% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 64% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 226.8594 (VA 225.1494–227.5006 ; dernier close 222.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 64% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.27% (p90 −1.71%) · haut méd +0.57% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.87%) · haut méd +0.68% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.0%) · haut méd +0.83% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.29%) · haut méd +0.94% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 222.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 76% (123/159) · gap 28% · délai 0.2min · rebond 52% (57/123) (MFE +1.07%)
   - −1.0% : fill 30min 42% · séance 63% (104/159) · gap 17% · délai 1.1min · rebond 56% (58/104) (MFE +1.15%)
   - −1.5% : fill 30min 31% · séance 57% (91/159) · gap 10% · délai 15.3min · rebond 64% (54/91) (MFE +1.5%)
   - −2.0% : fill 30min 21% · séance 43% (70/159) · gap 6% · délai 33.7min · rebond 56% (43/70) (MFE +1.26%)
   - −3.0% : fill 30min 6% · séance 22% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 7% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.8%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.88%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −2.09%) → stop au-delà de −1.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=409 jambes) : jambe baissière méd −1.05% (p90 −2.38%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 81% (62/76) · rebond 68% (39/62)
      · −2.0% : fill 58% (42/76) · rebond 65% (28/42)
      · −3.0% : fill 38% (29/76) · rebond 56% (17/29)
      · −4.0% : fill 20% (16/76) · rebond 71% (12/16)
      · −5.0% : fill 10% (7/76) · rebond 92% (6/7)
   - **flat** (35 séances) :
      · −1.0% : fill 62% (21/35) · rebond 35% (9/21)
      · −2.0% : fill 48% (15/35) · rebond 38% (7/15)
      · −3.0% : fill 18% (6/35) · rebond 49% (4/6)
      · −4.0% : fill 11% (3/35) · rebond 44% (2/3)
      · −5.0% : fill 11% (3/35) · rebond 44% (2/3)
   - **gap-up** (48 séances) :
      · −1.0% : fill 43% (21/48) · rebond 52% (10/21)
      · −2.0% : fill 22% (13/48) · rebond 55% (8/13)
      · −3.0% : fill 6% (5/48) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/48) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/48) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 61% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 77% si début vert vs 28% si rouge (base 53% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 53% ; creux résiduel méd -0.98% (q20 -2.15%) → **SL/trailing à −2.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.94% → **scale +1.18% / runner +1.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **28%** (continue à baisser 52%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.12% .. +2.1%] · haut q95 +2.63% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.46% .. +2.31%] · haut q95 +2.73% · bas q05 -3.11%
   - 2h (n=160) : retour [-2.25% .. +2.59%] · haut q95 +3.07% · bas q05 -3.18%
   - 4h (n=160) : retour [-2.63% .. +2.43%] · haut q95 +3.33% · bas q05 -3.54%
   - 6h (n=160) : retour [-2.69% .. +3.39%] · haut q95 +3.87% · bas q05 -3.85%
   - session (n=160) : retour [-3.73% .. +4.15%] · haut q95 +5.58% · bas q05 -4.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.22%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.0  _(momentum haussier)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist 0.508  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 12.0%
- **ATR** : 8.99 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.107  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 62.0  _(marche en range (choppy))_
- **MA** : MA20 225.13 · MA50 227.18 · MA200 230.13  _(prix > MA20)_
- **Dist MA** : MA20 +2.6% · MA50 +1.7% · MA200 +0.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94234 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
