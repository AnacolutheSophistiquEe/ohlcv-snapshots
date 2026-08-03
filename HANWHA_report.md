# 012450

**Generated** : 2026-08-03T00:16:15.020240+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩917000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩917000.00 (+2.0% vs entrée) · entrée ₩898827.20 · stop ₩826921.03 · T1 ₩971115.65 · R/R 1.01  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.075 _(réel 5 s)_ (GBM -0.154) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩893283.78–₩904370.63 (mid ₩898827.20)
- Spot actuel : ₩917000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩826921.03 (stop swing_plan-based (-12.83%))
- Targets : T1 ₩971115.65 · R/R 1.01 | T2 ₩976421.15 · R/R 1.08 | T3 ₩981726.65 · R/R 1.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩826921.03


## Edge, scénarios & sizing

- EV/risk : -0.154 | EV/share : ₩-11073.551 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.078 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.4 | bear 8.5 | side 78.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.978% → cible +8.043% / stop −8.0%, p_fill 77%, n_eff≈32.4) : P(cible|rempli) **6%** · **EV/risk -0.075** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −4.355% → cible +6.874% / stop −8.861%, p_fill 62%, n_eff≈25.8) : P(cible|rempli) **38%** · **EV/risk -0.172** (×p_fill ; si rempli -2.47% du capital)
  - **deep** (entrée dip −6.738% → cible +9.722% / stop −13.631%, p_fill 71%, n_eff≈26.1) : P(cible|rempli) **52%** · **EV/risk +0.032** (×p_fill ; si rempli +0.60% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→41% · +3.0%→24% · +5.0%→14% · +8.0%→2%
- Range intraday médian 5.96% (p90 9.06%) · excursion haute méd. +1.85% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.245% vs midi 1.179% vs clôture 1.191% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 86% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -1.169% ; recovery-V 38%
- **σ réalisé intraday** 4.806% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 57% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 905950.0 (VA 898350.0–915450.0 ; dernier close 923000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 36% · rebond 82% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.4 (high win-rate)
- Gaps overnight (n=148) : méd. 0.71% · baisse 33% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=149) : bas méd −1.76% (p90 −4.05%) · haut méd +0.8% · range méd 2.9%
- Excursion ouverture 15min (n=149) : bas méd −2.13% (p90 −4.7%) · haut méd +1.12% · range méd 3.49%
- Excursion ouverture 30min (n=149) : bas méd −2.2% (p90 −5.11%) · haut méd +1.25% · range méd 4.1%
- Excursion ouverture 60min (n=149) : bas méd −2.45% (p90 −5.57%) · haut méd +1.4% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 923000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (106/148) · gap 22% · délai 0.1min · rebond 48% (53/106) (MFE +0.73%)
   - −1.0% : fill 30min 56% · séance 69% (102/148) · gap 19% · délai 0.9min · rebond 52% (59/102) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 65% (95/148) · gap 12% · délai 1.3min · rebond 61% (55/95) (MFE +1.26%)
   - −2.0% : fill 30min 46% · séance 58% (79/148) · gap 10% · délai 3.1min · rebond 65% (49/79) (MFE +1.6%)
   - −3.0% : fill 30min 32% · séance 46% (58/148) · gap 2% · délai 3.4min · rebond 71% (40/58) (MFE +1.58%)
   - −4.0% : fill 30min 22% · séance 36% (44/148) · gap 2% · délai 9.6min · rebond 82% (36/44) (MFE +2.07%)
   - −5.0% : fill 30min 14% · séance 26% (32/148) · gap 1% · délai 8.7min · rebond 79% (26/32) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.34%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.79% (p90 −2.69%) → stop au-delà de −2.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.44% (p90 −2.69%) → stop au-delà de −2.64% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=721 jambes) : jambe baissière méd −1.25% (p90 −3.31%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 100% (33/33) · rebond 40% (14/33)
      · −2.0% : fill 94% (30/33) · rebond 67% (18/30)
      · −3.0% : fill 90% (27/33) · rebond 75% (19/27)
      · −4.0% : fill 77% (24/33) · rebond 89% (20/24)
      · −5.0% : fill 50% (16/33) · rebond 88% (14/16)
   - **flat** (19 séances) :
      · −1.0% : fill 88% (18/19) · rebond 41% (9/18)
      · −2.0% : fill 78% (15/19) · rebond 48% (7/15)
      · −3.0% : fill 60% (9/19) · rebond 37% (3/9)
      · −4.0% : fill 60% (9/19) · rebond 48% (5/9)
      · −5.0% : fill 58% (8/19) · rebond 52% (4/8)
   - **gap-up** (96 séances) :
      · −1.0% : fill 52% (51/96) · rebond 66% (36/51)
      · −2.0% : fill 39% (34/96) · rebond 72% (24/34)
      · −3.0% : fill 26% (22/96) · rebond 86% (18/22)
      · −4.0% : fill 13% (11/96) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/96) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 37% en base · 67% si les 15 1res min sont vertes (50 cas) · 20% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **49min** → P(séance verte=clôture>ouverture) 86% si début vert vs 9% si rouge (base 37% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=50) : tient le vert **86%** · continue >prix actuel 55% ; creux résiduel méd -1.6% (q20 -3.63%) → **SL/trailing à −3.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.52% / q75 +3.75% → **scale +2.52% / runner +3.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **9%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.48%** (au-delà de la MAE q10 -6.48%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-5.38% .. +4.67%] · haut q95 +5.79% · bas q05 -6.31%
   - 60min (n=149) : retour [-5.29% .. +5.32%] · haut q95 +7.1% · bas q05 -6.92%
   - 2h (n=149) : retour [-7.56% .. +5.61%] · haut q95 +7.1% · bas q05 -8.31%
   - 4h (n=149) : retour [-7.19% .. +5.81%] · haut q95 +7.85% · bas q05 -9.18%
   - 6h (n=149) : retour [-6.98% .. +6.0%] · haut q95 +8.32% · bas q05 -10.2%
   - session (n=149) : retour [-7.4% .. +5.96%] · haut q95 +8.32% · bas q05 -10.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.53%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 46.0  _(neutre)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist 1040.2  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 41.7%
- **ATR** : 77714.29 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.165  _(distribution)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 53.2  _(transition)_
- **MA** : MA20 953250.0 · MA50 1051140.0 · MA200 1139016.26  _(prix < MA20)_
- **Dist MA** : MA20 -3.8% · MA50 -12.8% · MA200 -19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83829 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
