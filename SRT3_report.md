# SRT3

**Generated** : 2026-08-07T21:37:31.390514+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €232.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €232.20 (+2.4% vs entrée) · entrée €226.81 · stop €214.72 · T1 €234.55 · R/R 0.64  
> ↳ P(T1 av. stop) 70 % _(réel 5 s)_ · EV/risk 0.074 _(réel 5 s)_ (GBM 0.049) · ¼-Kelly 0.023 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €225.26–€228.36 (mid €226.81)
- Spot actuel : €232.20 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €214.72 (stop swing_plan-based (-7.53%))
- Targets : T1 €234.55 · R/R 0.64 | T2 €242.30 · R/R 1.28 | T3 €250.04 · R/R 1.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €214.72


## Edge, scénarios & sizing

- EV/risk : 0.049 | EV/share : €0.586 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 27 % | T3 9 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.1 | bear 67.3 | side 13.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 232.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.058% → cible +1.527% / stop −1.579%, p_fill 55%, n_eff≈24.0) : P(cible|rempli) **31%** · **EV/risk -0.139** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −2.322% → cible +3.414% / stop −5.332%, p_fill 51%, n_eff≈20.4) : P(cible|rempli) **70%** · **EV/risk +0.074** (×p_fill ; si rempli +0.77% du capital)
  - **deep** (entrée dip −3.588% → cible +4.828% / stop −8.103%, p_fill 55%, n_eff≈18.6) : P(cible|rempli) **57%** · **EV/risk -0.031** (×p_fill ; si rempli -0.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→49% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.63% (p90 7.16%) · excursion haute méd. +1.96% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.122% vs midi 0.936% vs clôture 1.037% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.07% ; recovery-V 27%
- **σ réalisé intraday** 2.771% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 74% / whipsaw 48%
- POC intraday (dernière séance, temps-au-prix) : 231.9688 (VA 231.3587–233.3413 ; dernier close 229.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 73% · **stop −2.45%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. 0.08% · baisse 48% (gap-down >1% 14% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.36% (p90 −2.02%) · haut méd +0.57% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −2.1%) · haut méd +0.66% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.57% (p90 −2.56%) · haut méd +0.82% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.81%) · haut méd +0.87% · range méd 1.84%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 229.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 79% (125/159) · gap 27% · délai 0.3min · rebond 57% (66/125) (MFE +1.2%)
   - −1.0% : fill 30min 43% · séance 67% (105/159) · gap 14% · délai 2.1min · rebond 60% (61/105) (MFE +1.35%)
   - −1.5% : fill 30min 35% · séance 58% (94/159) · gap 7% · délai 4.7min · rebond 73% (61/94) (MFE +1.68%)
   - −2.0% : fill 30min 22% · séance 42% (73/159) · gap 4% · délai 24.1min · rebond 65% (45/73) (MFE +1.67%)
   - −3.0% : fill 30min 7% · séance 19% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 11% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.24%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.2% (p90 −2.42%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.8%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=426 jambes) : jambe baissière méd −1.05% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 86% (59/71) · rebond 68% (38/59)
      · −2.0% : fill 55% (42/71) · rebond 64% (27/42)
      · −3.0% : fill 32% (28/71) · rebond 48% (15/28)
      · −4.0% : fill 15% (15/71) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/71) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 62% (20/34) · rebond 56% (10/20)
      · −2.0% : fill 46% (15/34) · rebond 55% (7/15)
      · −3.0% : fill 18% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 14% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 14% (4/34) · rebond 24% (2/4)
   - **gap-up** (54 séances) :
      · −1.0% : fill 52% (26/54) · rebond 50% (13/26)
      · −2.0% : fill 26% (16/54) · rebond 77% (11/16)
      · −3.0% : fill 7% (6/54) · rebond 78% (4/6)
      · −4.0% : fill 5% (2/54) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 56% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 70% si début vert vs 24% si rouge (base 49% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **70%** · continue >prix actuel 48% ; creux résiduel méd -1.15% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.11% / q75 +2.25% → **scale +1.11% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.03% .. +2.07%] · haut q95 +2.65% · bas q05 -3.55%
   - 60min (n=160) : retour [-3.18% .. +2.31%] · haut q95 +2.69% · bas q05 -3.85%
   - 2h (n=160) : retour [-2.25% .. +2.57%] · haut q95 +3.0% · bas q05 -3.89%
   - 4h (n=160) : retour [-2.62% .. +2.39%] · haut q95 +3.32% · bas q05 -4.52%
   - 6h (n=160) : retour [-2.69% .. +3.2%] · haut q95 +3.82% · bas q05 -5.83%
   - session (n=160) : retour [-3.73% .. +4.21%] · haut q95 +5.76% · bas q05 -5.83%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.1  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 0.433  _(bullish_recent)_
- **BB** : %B 0.52 · largeur 19.9%
- **ATR** : 12.09 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 56.3  _(transition)_
- **MA** : MA20 231.29 · MA50 230.72 · MA200 231.96  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 +0.6% · MA200 +0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93058 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
