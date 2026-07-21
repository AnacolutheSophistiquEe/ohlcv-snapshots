# 267260

**Generated** : 2026-07-21T21:41:44.479925+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩778000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩778000.00 (+1.2% vs entrée) · entrée ₩768663.71 · stop ₩707170.62 · T1 ₩788860.54 · R/R 0.33  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.095 _(réel 5 s)_ (GBM -0.167) · ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.02). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩764624.35–₩772703.08 (mid ₩768663.71)
- Spot actuel : ₩778000.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : ₩707170.62 (stop swing_plan-based (-5.57%))
- Targets : T1 ₩788860.54 · R/R 0.33 | T2 ₩809057.36 · R/R 0.66 | T3 ₩829254.19 · R/R 0.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩707170.62


## Edge, scénarios & sizing

- EV/risk : -0.167 | EV/share : ₩-10276.540 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.6 | bear 76.1 | side 17.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.196% → cible +2.628% / stop −8.0%, p_fill 91%, n_eff≈36.6) : P(cible|rempli) **46%** · **EV/risk -0.095** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −2.639% → cible +5.875% / stop −3.01%, p_fill 90%, n_eff≈34.0) : P(cible|rempli) **32%** · **EV/risk -0.103** (×p_fill ; si rempli -0.34% du capital)
  - **deep** (entrée dip −4.085% → cible +8.309% / stop −4.154%, p_fill 84%, n_eff≈30.7) : P(cible|rempli) **20%** · **EV/risk -0.383** (×p_fill ; si rempli -1.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→44% · +3.0%→28% · +5.0%→9% · +8.0%→5%
- Range intraday médian 5.91% (p90 10.49%) · excursion haute méd. +1.84% / basse méd. −3.45%
- Profil de vol intra : ouverture 3.971% vs midi 1.044% vs clôture 1.137% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. -1.897% ; recovery-V 15%
- **σ réalisé intraday** 4.837% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 80% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 753137.5 (VA 746687.5–760662.5 ; dernier close 756000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 83% · **stop −4.21%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.48 (high win-rate)
- Gaps overnight (n=135) : méd. 0.75% · baisse 38% (gap-down >1% 23% · >2% 11%)
- Excursion ouverture 5min (n=136) : bas méd −1.57% (p90 −3.82%) · haut méd +0.9% · range méd 2.67%
- Excursion ouverture 15min (n=136) : bas méd −1.79% (p90 −4.68%) · haut méd +1.06% · range méd 3.32%
- Excursion ouverture 30min (n=136) : bas méd −2.18% (p90 −4.93%) · haut méd +1.07% · range méd 3.67%
- Excursion ouverture 60min (n=136) : bas méd −2.56% (p90 −5.63%) · haut méd +1.25% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 756000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (96/135) · gap 30% · délai 0.0min · rebond 52% (53/96) (MFE +1.08%)
   - −1.0% : fill 30min 55% · séance 70% (89/135) · gap 23% · délai 0.3min · rebond 52% (51/89) (MFE +1.01%)
   - −1.5% : fill 30min 48% · séance 62% (76/135) · gap 16% · délai 0.6min · rebond 65% (49/76) (MFE +1.27%)
   - −2.0% : fill 30min 43% · séance 59% (69/135) · gap 11% · délai 0.9min · rebond 66% (46/69) (MFE +1.61%)
   - −3.0% : fill 30min 32% · séance 49% (54/135) · gap 6% · délai 5.6min · rebond 76% (37/54) (MFE +1.68%)
   - −4.0% : fill 30min 23% · séance 42% (45/135) · gap 3% · délai 16.5min · rebond 79% (36/45) (MFE +2.29%)
   - −5.0% : fill 30min 14% · séance 35% (35/135) · gap 2% · délai 58.7min · rebond 83% (27/35) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.71% (p90 −3.59%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.56%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −5.2%) → stop au-delà de −3.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=662 jambes) : jambe baissière méd −1.35% (p90 −3.61%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 98% (45/46) · rebond 43% (23/45)
      · −2.0% : fill 91% (38/46) · rebond 57% (22/38)
      · −3.0% : fill 79% (32/46) · rebond 75% (21/32)
      · −4.0% : fill 69% (28/46) · rebond 82% (23/28)
      · −5.0% : fill 57% (21/46) · rebond 83% (16/21)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 49% (30/72) · rebond 64% (21/30)
      · −2.0% : fill 35% (19/72) · rebond 71% (15/19)
      · −3.0% : fill 25% (11/72) · rebond 73% (8/11)
      · −4.0% : fill 23% (10/72) · rebond 82% (8/10)
      · −5.0% : fill 16% (7/72) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 33% en base · 50% si les 15 1res min sont vertes (64 cas) · 22% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=136) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 75% si début vert vs 10% si rouge (base 33% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **75%** · continue >prix actuel 42% ; creux résiduel méd -1.63% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.28% → **scale +1.21% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +1.64% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-5.24% .. +2.99%] · haut q95 +4.39% · bas q05 -5.68%
   - 60min (n=136) : retour [-5.6% .. +3.29%] · haut q95 +4.59% · bas q05 -6.04%
   - 2h (n=136) : retour [-7.0% .. +3.67%] · haut q95 +5.53% · bas q05 -7.43%
   - 4h (n=136) : retour [-6.94% .. +3.29%] · haut q95 +5.55% · bas q05 -8.22%
   - 6h (n=136) : retour [-6.94% .. +4.03%] · haut q95 +7.46% · bas q05 -8.85%
   - session (n=136) : retour [-7.12% .. +3.93%] · haut q95 +7.46% · bas q05 -9.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.4  _(survente)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist -7677.18  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 35.9%
- **ATR** : 76000.0 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.16  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 40.3  _(transition)_
- **MA** : MA20 879850.0 · MA50 1019547.22 · MA200 916140.57  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -23.7% · MA200 -15.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84130 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
