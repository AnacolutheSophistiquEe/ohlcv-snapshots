# 267260

**Generated** : 2026-07-16T21:51:57.707721+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩785000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩785000.00 (+1.4% vs entrée) · entrée ₩773913.71 · stop ₩712000.62 · T1 ₩832775.15 · R/R 0.95  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.139 _(réel 5 s)_ (GBM -0.183) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.250 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩769963.63–₩777863.80 (mid ₩773913.71)
- Spot actuel : ₩785000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩712000.62 (stop swing_plan-based (-6.11%))
- Targets : T1 ₩832775.15 · R/R 0.95 | T2 ₩832880.30 · R/R 0.95 | T3 ₩832985.46 · R/R 0.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩712000.62


## Edge, scénarios & sizing

- EV/risk : -0.183 | EV/share : ₩-11322.358 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 75.6 | side 17.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.413% → cible +7.606% / stop −8.0%, p_fill 87%, n_eff≈35.0) : P(cible|rempli) **5%** · **EV/risk -0.139** (×p_fill ; si rempli -1.27% du capital)
  - **swing** (entrée dip −3.104% → cible +5.689% / stop −3.102%, p_fill 87%, n_eff≈32.5) : P(cible|rempli) **31%** · **EV/risk -0.146** (×p_fill ; si rempli -0.52% du capital)
  - **deep** (entrée dip −4.8% → cible +8.046% / stop −4.023%, p_fill 76%, n_eff≈27.7) : P(cible|rempli) **24%** · **EV/risk -0.244** (×p_fill ; si rempli -1.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→66% · +2.0%→45% · +3.0%→29% · +5.0%→9% · +8.0%→5%
- Range intraday médian 5.91% (p90 10.49%) · excursion haute méd. +1.85% / basse méd. −3.37%
- Profil de vol intra : ouverture 3.931% vs midi 1.031% vs clôture 1.098% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.017)_ ; drift intra méd. -1.937% ; recovery-V 18%
- **σ réalisé intraday** 4.822% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 77% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 827862.5 (VA 821262.5–838587.5 ; dernier close 820000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 41% · rebond 77% · **stop −5.2%** sous le fill (sous le bruit) · cible +2.29% · R/R 0.44 (high win-rate)
- Gaps overnight (n=132) : méd. 1.12% · baisse 37% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=133) : bas méd −1.6% (p90 −3.89%) · haut méd +0.88% · range méd 2.68%
- Excursion ouverture 15min (n=133) : bas méd −1.88% (p90 −4.69%) · haut méd +1.04% · range méd 3.33%
- Excursion ouverture 30min (n=133) : bas méd −2.21% (p90 −4.95%) · haut méd +1.06% · range méd 3.69%
- Excursion ouverture 60min (n=133) : bas méd −2.59% (p90 −5.66%) · haut méd +1.11% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 820000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 71% (93/132) · gap 28% · délai 0.1min · rebond 53% (52/93) (MFE +1.18%)
   - −1.0% : fill 30min 55% · séance 68% (86/132) · gap 20% · délai 0.3min · rebond 53% (50/86) (MFE +1.01%)
   - −1.5% : fill 30min 47% · séance 60% (73/132) · gap 13% · délai 0.6min · rebond 65% (47/73) (MFE +1.26%)
   - −2.0% : fill 30min 42% · séance 56% (66/132) · gap 9% · délai 1.0min · rebond 66% (44/66) (MFE +1.61%)
   - −3.0% : fill 30min 30% · séance 48% (52/132) · gap 7% · délai 5.7min · rebond 74% (35/52) (MFE +1.5%)
   - −4.0% : fill 30min 23% · séance 41% (43/132) · gap 3% · délai 16.5min · rebond 77% (34/43) (MFE +2.29%)
   - −5.0% : fill 30min 12% · séance 33% (33/132) · gap 2% · délai 58.7min · rebond 81% (25/33) (MFE +1.84%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −3.32%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.56%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −5.2%) → stop au-delà de −3.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=634 jambes) : jambe baissière méd −1.34% (p90 −3.76%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 97% (43/44) · rebond 49% (23/43)
      · −2.0% : fill 89% (36/44) · rebond 59% (21/36)
      · −3.0% : fill 76% (30/44) · rebond 70% (19/30)
      · −4.0% : fill 65% (26/44) · rebond 78% (21/26)
      · −5.0% : fill 52% (19/44) · rebond 78% (14/19)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 47% (29/71) · rebond 61% (20/29)
      · −2.0% : fill 33% (18/71) · rebond 68% (14/18)
      · −3.0% : fill 26% (11/71) · rebond 73% (8/11)
      · −4.0% : fill 24% (10/71) · rebond 82% (8/10)
      · −5.0% : fill 17% (7/71) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 35% en base · 56% si les 15 1res min sont vertes (62 cas) · 22% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=133) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 75% si début vert vs 12% si rouge (base 35% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **75%** · continue >prix actuel 42% ; creux résiduel méd -1.63% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.28% → **scale +1.21% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.37%** (au-delà de la MAE q10 -5.37%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-5.35% .. +3.02%] · haut q95 +4.44% · bas q05 -5.73%
   - 60min (n=133) : retour [-5.63% .. +3.39%] · haut q95 +4.66% · bas q05 -6.06%
   - 2h (n=133) : retour [-7.04% .. +3.68%] · haut q95 +5.99% · bas q05 -7.53%
   - 4h (n=133) : retour [-6.95% .. +3.39%] · haut q95 +5.59% · bas q05 -8.33%
   - 6h (n=133) : retour [-7.03% .. +4.3%] · haut q95 +7.79% · bas q05 -8.89%
   - session (n=133) : retour [-7.23% .. +3.96%] · haut q95 +7.79% · bas q05 -9.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.2  _(momentum baissier)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist -9476.264  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 37.9%
- **ATR** : 78642.86 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.245  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 45.9  _(transition)_
- **MA** : MA20 908300.0 · MA50 1044833.59 · MA200 914306.1  _(prix < MA20)_
- **Dist MA** : MA20 -13.6% · MA50 -24.9% · MA200 -14.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83445 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
