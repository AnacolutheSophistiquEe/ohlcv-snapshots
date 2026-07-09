# ENR

**Generated** : 2026-07-09T21:40:53.002772+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €156.24  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €156.24 (+0.7% vs entrée) · entrée €155.12 · stop €142.71 · T1 €158.23 · R/R 0.25  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.082 _(réel 5 s)_ (GBM -0.026) · ¼-Kelly 0.075 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €154.49–€155.74 (mid €155.12)
- Spot actuel : €156.24 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €142.71 (stop swing_plan-based (-3.79%))
- Targets : T1 €158.23 · R/R 0.25 | T2 €161.34 · R/R 0.5 | T3 €164.46 · R/R 0.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €142.71


## Edge, scénarios & sizing

- EV/risk : -0.026 | EV/share : €-0.326 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 16 % | T3 10 %
- Kelly (position) : f* 0.299 | ¼-Kelly 0.075 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.5 | bear 30.3 | side 62.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 156.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.717% → cible +2.008% / stop −8.0%, p_fill 77%, n_eff≈30.6) : P(cible|rempli) **22%** · **EV/risk -0.082** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −1.581% → cible +4.49% / stop −2.245%, p_fill 72%, n_eff≈30.3) : P(cible|rempli) **24%** · **EV/risk -0.237** (×p_fill ; si rempli -0.74% du capital)
  - **deep** (entrée dip −2.453% → cible +6.349% / stop −3.175%, p_fill 81%, n_eff≈31.6) : P(cible|rempli) **23%** · **EV/risk -0.279** (×p_fill ; si rempli -1.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→61% · +2.0%→46% · +3.0%→24% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.34% (p90 6.09%) · excursion haute méd. +1.5% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.178% vs midi 0.952% vs clôture 1.196% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.478% ; recovery-V 23%
- **σ réalisé intraday** 2.62% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 64% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 152.7935 (VA 152.4365–153.6265 ; dernier close 152.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 67% · **stop −2.92%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 39% (gap-down >1% 22% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −2.12%) · haut méd +0.45% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.23%) · haut méd +0.59% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +0.6% · range méd 1.86%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.69% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 152.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 73% (115/159) · gap 28% · délai 0.4min · rebond 53% (59/115) (MFE +1.19%)
   - −1.0% : fill 30min 50% · séance 68% (103/159) · gap 22% · délai 1.3min · rebond 57% (60/103) (MFE +1.34%)
   - −1.5% : fill 30min 40% · séance 60% (89/159) · gap 19% · délai 10.5min · rebond 62% (56/89) (MFE +1.53%)
   - −2.0% : fill 30min 26% · séance 45% (65/159) · gap 13% · délai 6.2min · rebond 61% (39/65) (MFE +1.38%)
   - −3.0% : fill 30min 17% · séance 33% (48/159) · gap 6% · délai 25.5min · rebond 67% (35/48) (MFE +1.5%)
   - −4.0% : fill 30min 9% · séance 26% (37/159) · gap 4% · délai 285.2min · rebond 60% (25/37) (MFE +1.23%)
   - −5.0% : fill 30min 3% · séance 17% (21/159) · gap 1% · délai 203.6min · rebond 67% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.91%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.22%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.52%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.04% (p90 −2.51%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 96% (45/46) · rebond 54% (25/45)
      · −2.0% : fill 73% (33/46) · rebond 62% (22/33)
      · −3.0% : fill 62% (28/46) · rebond 61% (20/28)
      · −4.0% : fill 52% (23/46) · rebond 55% (16/23)
      · −5.0% : fill 38% (15/46) · rebond 63% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 72% (20/27) · rebond 69% (14/20)
      · −2.0% : fill 35% (9/27) · rebond 56% (4/9)
      · −3.0% : fill 18% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 16% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 10% (2/27) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 49% (38/86) · rebond 55% (21/38)
      · −2.0% : fill 31% (23/86) · rebond 60% (13/23)
      · −3.0% : fill 20% (15/86) · rebond 73% (12/15)
      · −4.0% : fill 12% (10/86) · rebond 67% (7/10)
      · −5.0% : fill 6% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 86% si les 15 1res min sont vertes (76 cas) · 23% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 23% si rouge (base 49% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **86%** · continue >prix actuel 73% ; creux résiduel méd -1.09% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.3% → **scale +2.05% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **23%** (continue à baisser 64%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.28% .. +2.02%] · haut q95 +2.68% · bas q05 -2.96%
   - 60min (n=160) : retour [-2.31% .. +2.11%] · haut q95 +2.75% · bas q05 -3.22%
   - 2h (n=160) : retour [-2.84% .. +2.43%] · haut q95 +3.14% · bas q05 -3.64%
   - 4h (n=160) : retour [-2.87% .. +2.65%] · haut q95 +4.09% · bas q05 -3.81%
   - 6h (n=160) : retour [-3.15% .. +3.77%] · haut q95 +4.7% · bas q05 -4.43%
   - session (n=160) : retour [-5.26% .. +4.38%] · haut q95 +5.52% · bas q05 -5.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -0.464  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 15.1%
- **ATR** : 7.79 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.032  _(neutre)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 59.9  _(transition)_
- **MA** : MA20 161.44 · MA50 166.02 · MA200 140.85  _(prix < MA20)_
- **Dist MA** : MA20 -3.2% · MA50 -5.9% · MA200 +10.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94619 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
