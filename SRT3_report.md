# SRT3

**Generated** : 2026-07-29T21:37:25.362151+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €225.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €225.60 (+0.4% vs entrée) · entrée €224.79 · stop €221.07 · T1 €228.87 · R/R 1.1  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.195 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.66% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €223.98–€225.60 (mid €224.79)
- Spot actuel : €225.60 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €221.07 (stop swing_plan-based (-2.81%))
- Targets : T1 €228.87 · R/R 1.1 | T2 €232.95 · R/R 2.19 | T3 €237.03 · R/R 3.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €221.07


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : €0.065 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.4 | bear 74.6 | side 12.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.36% → cible +1.815% / stop −1.656%, p_fill 89%, n_eff≈35.2) : P(cible|rempli) **25%** · **EV/risk -0.195** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −0.797% → cible +4.059% / stop −2.029%, p_fill 80%, n_eff≈31.4) : P(cible|rempli) **17%** · **EV/risk -0.377** (×p_fill ; si rempli -0.95% du capital)
  - **deep** (entrée dip −1.205% → cible +5.74% / stop −2.87%, p_fill 74%, n_eff≈31.4) : P(cible|rempli) **26%** · **EV/risk -0.202** (×p_fill ; si rempli -0.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→48% · +3.0%→28% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.72% (p90 7.16%) · excursion haute méd. +1.94% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.197% vs midi 0.909% vs clôture 1.034% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.152% ; recovery-V 32%
- **σ réalisé intraday** 2.988% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 63% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 214.41 (VA 211.37–215.55 ; dernier close 222.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 62% · rebond 75% · **stop −2.5%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 52% (gap-down >1% 16% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −2.47%) · haut méd +0.5% · range méd 1.31%
- Excursion ouverture 15min (n=160) : bas méd −0.59% (p90 −2.51%) · haut méd +0.65% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.65% (p90 −2.79%) · haut méd +0.77% · range méd 1.77%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.81%) · haut méd +0.82% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 222.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 80% (126/159) · gap 30% · délai 0.2min · rebond 57% (65/126) (MFE +1.2%)
   - −1.0% : fill 30min 49% · séance 68% (106/159) · gap 16% · délai 0.4min · rebond 64% (65/106) (MFE +1.47%)
   - −1.5% : fill 30min 40% · séance 62% (93/159) · gap 8% · délai 3.2min · rebond 75% (61/93) (MFE +1.86%)
   - −2.0% : fill 30min 25% · séance 45% (72/159) · gap 4% · délai 17.5min · rebond 63% (44/72) (MFE +1.96%)
   - −3.0% : fill 30min 8% · séance 22% (40/159) · gap 2% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 5% · séance 12% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 9% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −2.39%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −2.44%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.8%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=429 jambes) : jambe baissière méd −1.05% (p90 −2.71%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 86% (63/75) · rebond 72% (43/63)
      · −2.0% : fill 57% (42/75) · rebond 64% (27/42)
      · −3.0% : fill 33% (28/75) · rebond 48% (15/28)
      · −4.0% : fill 16% (15/75) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/75) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 63% (19/34) · rebond 50% (9/19)
      · −2.0% : fill 53% (15/34) · rebond 55% (7/15)
      · −3.0% : fill 21% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 16% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 16% (4/34) · rebond 24% (2/4)
   - **gap-up** (50 séances) :
      · −1.0% : fill 52% (24/50) · rebond 60% (13/24)
      · −2.0% : fill 27% (15/50) · rebond 72% (10/15)
      · −3.0% : fill 9% (6/50) · rebond 78% (4/6)
      · −4.0% : fill 6% (2/50) · rebond 100% (2/2)
      · −5.0% : fill 5% (1/50) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 58% si les 15 1res min sont vertes (90 cas) · 42% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 67% si début vert vs 35% si rouge (base 50% · écart 32 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **67%** · continue >prix actuel 44% ; creux résiduel méd -1.27% (q20 -2.35%) → **SL/trailing à −2.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.51% → **scale +1.13% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **35%** (continue à baisser 50%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.74%** (au-delà de la MAE q10 -3.74%), cible rebond +1.55% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.14% .. +2.11%] · haut q95 +2.67% · bas q05 -3.6%
   - 60min (n=160) : retour [-3.41% .. +2.32%] · haut q95 +2.77% · bas q05 -3.97%
   - 2h (n=160) : retour [-2.33% .. +2.61%] · haut q95 +3.1% · bas q05 -4.5%
   - 4h (n=160) : retour [-2.74% .. +2.69%] · haut q95 +3.35% · bas q05 -5.91%
   - 6h (n=160) : retour [-2.76% .. +3.5%] · haut q95 +3.98% · bas q05 -7.4%
   - session (n=160) : retour [-3.79% .. +4.61%] · haut q95 +6.02% · bas q05 -7.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.7  _(momentum baissier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.945  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 19.9%
- **ATR** : 12.41 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.006  _(neutre)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 231.68 · MA50 231.61 · MA200 231.73  _(prix < MA20)_
- **Dist MA** : MA20 -2.6% · MA50 -2.6% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91727 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
