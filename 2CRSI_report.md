# AL2SI

**Generated** : 2026-08-14T00:09:48.154945+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.80 (+10.5% vs entrée) · entrée €25.15 · stop €23.14 · T1 €26.92 · R/R 0.88  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk -0.051 _(réel 5 s)_ (GBM 0.194) · ¼-Kelly 0.028 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.170 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.80–€25.51 (mid €25.15)
- Spot actuel : €27.80 (+10.5% au-dessus de la zone — repli à attendre)
- Stop : €23.14 (stop swing_plan-based (-16.77%))
- Targets : T1 €26.92 · R/R 0.88 | T2 €28.69 · R/R 1.76 | T3 €30.46 · R/R 2.64
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.14


## Edge, scénarios & sizing

- EV/risk : 0.194 | EV/share : €0.392 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 33 % | T3 21 %
- Kelly (position) : f* 0.111 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.3 | bear 9.5 | side 5.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 389.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.322% → cible +3.143% / stop −2.276%, p_fill 53%, n_eff≈24.2) : P(cible|rempli) **28%** · **EV/risk -0.047** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −9.511% → cible +7.028% / stop −8.022%, p_fill 39%, n_eff≈17.5) : P(cible|rempli) **54%** · **EV/risk -0.051** (×p_fill ; si rempli -1.05% du capital)
  - **deep** (entrée dip −14.702% → cible +9.939% / stop −12.765%, p_fill 38%, n_eff≈16.7) : P(cible|rempli) **47%** · **EV/risk -0.081** (×p_fill ; si rempli -2.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→71% · +3.0%→61% · +5.0%→44% · +8.0%→20%
- Range intraday médian 8.23% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −4.2%
- Profil de vol intra : ouverture 5.652% vs midi 1.758% vs clôture 1.925% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. -0.126% ; recovery-V 29%
- **σ réalisé intraday** 6.876% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 69% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 27.8588 (VA 27.7162–28.0012 ; dernier close 28.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 41% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −4.8%) · haut méd +1.04% · range méd 3.09%
- Excursion ouverture 15min (n=160) : bas méd −1.61% (p90 −5.71%) · haut méd +1.92% · range méd 4.12%
- Excursion ouverture 30min (n=160) : bas méd −1.74% (p90 −5.85%) · haut méd +2.33% · range méd 4.86%
- Excursion ouverture 60min (n=160) : bas méd −2.29% (p90 −6.82%) · haut méd +2.73% · range méd 6.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 81% (124/159) · gap 28% · délai 0.3min · rebond 67% (83/124) (MFE +3.03%)
   - −1.0% : fill 30min 60% · séance 80% (120/159) · gap 21% · délai 0.4min · rebond 67% (82/120) (MFE +2.59%)
   - −1.5% : fill 30min 52% · séance 76% (110/159) · gap 15% · délai 1.1min · rebond 67% (72/110) (MFE +1.99%)
   - −2.0% : fill 30min 43% · séance 67% (95/159) · gap 9% · délai 5.8min · rebond 61% (60/95) (MFE +1.64%)
   - −3.0% : fill 30min 34% · séance 58% (80/159) · gap 5% · délai 10.8min · rebond 78% (65/80) (MFE +2.05%)
   - −4.0% : fill 30min 26% · séance 50% (69/159) · gap 3% · délai 27.7min · rebond 77% (54/69) (MFE +2.49%)
   - −5.0% : fill 30min 17% · séance 42% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.9% (p90 −5.17%) → stop au-delà de −2.78% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.21% (p90 −5.28%) → stop au-delà de −3.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.27% (p90 −5.37%) → stop au-delà de −3.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1558 jambes) : jambe baissière méd −1.29% (p90 −3.42%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 99% (52/55) · rebond 66% (34/52)
      · −2.0% : fill 85% (44/55) · rebond 55% (26/44)
      · −3.0% : fill 80% (41/55) · rebond 77% (33/41)
      · −4.0% : fill 72% (36/55) · rebond 82% (30/36)
      · −5.0% : fill 55% (31/55) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 81% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 63% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 50% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 44% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 39% (12/35) · rebond 100% (12/12)
   - **gap-up** (69 séances) :
      · −1.0% : fill 65% (40/69) · rebond 61% (26/40)
      · −2.0% : fill 56% (30/69) · rebond 55% (18/30)
      · −3.0% : fill 46% (24/69) · rebond 76% (19/24)
      · −4.0% : fill 38% (19/69) · rebond 64% (12/19)
      · −5.0% : fill 34% (17/69) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:00** → P(séance verte=clôture>ouverture) 73% si début vert vs 17% si rouge (base 46% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -2.28% (q20 -5.7%) → **SL/trailing à −5.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.23% / q75 +5.96% → **scale +3.23% / runner +5.96%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **17%** (continue à baisser 47%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.01%** (au-delà de la MAE q10 -8.01%), cible rebond +2.69% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.52% .. +6.61%] · haut q95 +8.17% · bas q05 -7.58%
   - 60min (n=160) : retour [-5.89% .. +7.65%] · haut q95 +9.46% · bas q05 -7.79%
   - 2h (n=160) : retour [-6.12% .. +9.8%] · haut q95 +10.2% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.47% .. +9.59%] · haut q95 +12.22% · bas q05 -10.71%
   - 6h (n=160) : retour [-6.77% .. +10.38%] · haut q95 +14.48% · bas q05 -11.03%
   - session (n=160) : retour [-8.26% .. +13.02%] · haut q95 +14.65% · bas q05 -11.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.3  _(neutre)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist 0.639  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 20.9%
- **ATR** : 2.02 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.17  _(distribution)_
- **Vol ratio** : 0.28  _(volume atone)_
- **Choppiness** : 55.0  _(transition)_
- **MA** : MA20 26.73 · MA50 32.79 · MA200 25.27  _(prix > MA20)_
- **Dist MA** : MA20 +4.0% · MA50 -15.2% · MA200 +10.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93500 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
