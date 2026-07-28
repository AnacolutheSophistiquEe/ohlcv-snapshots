# 326030

**Generated** : 2026-07-28T21:55:26.143025+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩79500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩79500.00 (+4.0% vs entrée) · entrée ₩76475.00 · stop ₩75094.64 · T1 ₩79235.72 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk 0.034 _(réel 5 s)_ (GBM -0.1) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩75922.86–₩77027.14 (mid ₩76475.00)
- Spot actuel : ₩79500.00 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : ₩75094.64 (stop swing_plan-based (-5.54%))
- Targets : T1 ₩79235.72 · R/R 2.0 | T2 ₩81996.45 · R/R 4.0 | T3 ₩84757.17 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩75094.64


## Edge, scénarios & sizing

- EV/risk : -0.1 | EV/share : ₩-137.893 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.2 | bear 28.8 | side 25.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.728% → cible +3.424% / stop −1.712%, p_fill 51%, n_eff≈24.8) : P(cible|rempli) **9%** · **EV/risk -0.220** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −3.804% → cible +3.61% / stop −1.805%, p_fill 47%, n_eff≈19.1) : P(cible|rempli) **37%** · **EV/risk +0.034** (×p_fill ; si rempli +0.13% du capital)
  - **deep** (entrée dip −5.877% → cible +5.105% / stop −2.553%, p_fill 54%, n_eff≈18.8) : P(cible|rempli) **38%** · **EV/risk +0.069** (×p_fill ; si rempli +0.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→45% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.17% (p90 7.23%) · excursion haute méd. +1.65% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.696% vs midi 0.791% vs clôture 0.797% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑1%/↓2% ; spike-down 56% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. -0.147% ; recovery-V 26%
- **σ réalisé intraday** 3.377% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 58% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 81812.5 (VA 81217.5–82067.5 ; dernier close 81800.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 45% · rebond 64% · **stop −3.86%** sous le fill (sous le bruit) · cible +1.43% · R/R 0.37 (high win-rate)
- Gaps overnight (n=140) : méd. 0.1% · baisse 41% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=141) : bas méd −0.75% (p90 −2.23%) · haut méd +0.68% · range méd 1.93%
- Excursion ouverture 15min (n=141) : bas méd −0.86% (p90 −2.97%) · haut méd +0.78% · range méd 2.2%
- Excursion ouverture 30min (n=141) : bas méd −1.02% (p90 −2.99%) · haut méd +1.14% · range méd 2.59%
- Excursion ouverture 60min (n=141) : bas méd −1.2% (p90 −3.19%) · haut méd +1.38% · range méd 2.95%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 81800.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 79% (103/140) · gap 26% · délai 0.3min · rebond 52% (44/103) (MFE +1.22%)
   - −1.0% : fill 30min 54% · séance 69% (92/140) · gap 16% · délai 1.8min · rebond 55% (44/92) (MFE +1.06%)
   - −1.5% : fill 30min 39% · séance 53% (69/140) · gap 9% · délai 3.2min · rebond 58% (35/69) (MFE +1.22%)
   - −2.0% : fill 30min 26% · séance 45% (57/140) · gap 7% · délai 16.4min · rebond 64% (32/57) (MFE +1.43%)
   - −3.0% : fill 30min 10% · séance 33% (37/140) · gap 3% · délai 89.7min · rebond 56% (16/37) (MFE +1.32%)
   - −4.0% : fill 30min 7% · séance 20% (25/140) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 15% (19/140) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.0%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.6%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.62%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=467 jambes) : jambe baissière méd −1.12% (p90 −2.43%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 94% (41/42) · rebond 66% (22/41)
      · −2.0% : fill 64% (28/42) · rebond 61% (14/28)
      · −3.0% : fill 42% (18/42) · rebond 49% (7/18)
      · −4.0% : fill 35% (15/42) · rebond 65% (8/15)
      · −5.0% : fill 28% (12/42) · rebond 85% (8/12)
   - **flat** (37 séances) :
      · −1.0% : fill 70% (26/37) · rebond 42% (10/26)
      · −2.0% : fill 51% (18/37) · rebond 74% (12/18)
      · −3.0% : fill 39% (11/37) · rebond 71% (6/11)
      · −4.0% : fill 28% (8/37) · rebond 39% (3/8)
      · −5.0% : fill 20% (6/37) · rebond 79% (4/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (25/61) · rebond 53% (12/25)
      · −2.0% : fill 26% (11/61) · rebond 56% (6/11)
      · −3.0% : fill 20% (8/61) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/61) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 41% en base · 70% si les 15 1res min sont vertes (52 cas) · 18% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=141) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 77% si début vert vs 6% si rouge (base 41% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 202min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **77%** · continue >prix actuel 38% ; creux résiduel méd -1.45% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.22% / q75 +1.92% → **scale +1.22% / runner +1.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.0%** (au-delà de la MAE q10 -4.0%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-2.77% .. +2.81%] · haut q95 +3.59% · bas q05 -4.0%
   - 60min (n=141) : retour [-3.76% .. +3.64%] · haut q95 +4.42% · bas q05 -4.38%
   - 2h (n=141) : retour [-3.44% .. +3.77%] · haut q95 +4.67% · bas q05 -4.55%
   - 4h (n=141) : retour [-3.85% .. +4.67%] · haut q95 +6.16% · bas q05 -5.7%
   - 6h (n=141) : retour [-4.54% .. +4.11%] · haut q95 +6.83% · bas q05 -5.93%
   - session (n=141) : retour [-4.65% .. +4.06%] · haut q95 +6.83% · bas q05 -5.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.3  _(momentum baissier)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 463.141  _(bullish_recent)_
- **BB** : %B 0.38 · largeur 18.1%
- **ATR** : 4042.86 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.223  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 60.4  _(transition)_
- **MA** : MA20 81205.0 · MA50 86446.0 · MA200 106506.5  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 -8.0% · MA200 -25.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83489 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
