# 012450

**Generated** : 2026-07-10T00:18:39.291650+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩953000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)  
> ↳ spot ₩953000.00 (+3.2% vs entrée) · entrée ₩923686.26 · stop ₩894678.19 · T1 ₩981702.41 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.086 _(réel 5 s)_ (GBM 0.134) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩912083.03–₩935289.49 (mid ₩923686.26)
- Spot actuel : ₩953000.00 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : ₩894678.19 (stop swing_plan-based (-6.12%))
- Targets : T1 ₩981702.41 · R/R 2.0 | T2 ₩1039718.57 · R/R 4.0 | T3 ₩1097734.72 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩894678.19


## Edge, scénarios & sizing

- EV/risk : 0.134 | EV/share : ₩3881.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 5 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 32.6 | bear 16.1 | side 51.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.402% → cible +2.809% / stop −8.0%, p_fill 89%, n_eff≈35.9) : P(cible|rempli) **21%** · **EV/risk -0.131** (×p_fill ; si rempli -1.17% du capital)
  - **swing** (entrée dip −3.076% → cible +6.281% / stop −3.14%, p_fill 69%, n_eff≈27.7) : P(cible|rempli) **30%** · **EV/risk -0.086** (×p_fill ; si rempli -0.39% du capital)
  - **deep** (entrée dip −4.75% → cible +8.883% / stop −4.441%, p_fill 76%, n_eff≈27.9) : P(cible|rempli) **24%** · **EV/risk -0.242** (×p_fill ; si rempli -1.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→57% · +2.0%→39% · +3.0%→21% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.5% (p90 8.09%) · excursion haute méd. +1.58% / basse méd. −3.16%
- Profil de vol intra : ouverture 3.963% vs midi 1.021% vs clôture 1.1% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (129 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 86% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -1.978% ; recovery-V 16%
- **σ réalisé intraday** 4.47% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 30% / bas 65% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 956775.0 (VA 931575.0–972525.0 ; dernier close 952000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 80% · **stop −4.17%** sous le fill (sous le bruit) · cible +2.44% · R/R 0.59 (high win-rate)
- Gaps overnight (n=128) : méd. 0.81% · baisse 29% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=129) : bas méd −1.59% (p90 −4.05%) · haut méd +0.79% · range méd 2.64%
- Excursion ouverture 15min (n=129) : bas méd −1.96% (p90 −4.64%) · haut méd +0.86% · range méd 3.37%
- Excursion ouverture 30min (n=129) : bas méd −2.54% (p90 −5.0%) · haut méd +1.0% · range méd 4.06%
- Excursion ouverture 60min (n=129) : bas méd −2.61% (p90 −5.44%) · haut méd +1.12% · range méd 4.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 952000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (93/128) · gap 21% · délai 0.6min · rebond 47% (46/93) (MFE +0.73%)
   - −1.0% : fill 30min 56% · séance 72% (90/128) · gap 17% · délai 1.2min · rebond 56% (53/90) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 66% (83/128) · gap 10% · délai 3.3min · rebond 58% (46/83) (MFE +1.26%)
   - −2.0% : fill 30min 44% · séance 57% (68/128) · gap 6% · délai 4.9min · rebond 63% (41/68) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 46% (49/128) · gap 3% · délai 15.2min · rebond 70% (33/49) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 33% (37/128) · gap 3% · délai 14.3min · rebond 80% (30/37) (MFE +2.13%)
   - −5.0% : fill 30min 10% · séance 26% (28/128) · gap 2% · délai 49.2min · rebond 80% (23/28) (MFE +2.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.13%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.75% (p90 −2.69%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −2.9%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=582 jambes) : jambe baissière méd −1.31% (p90 −3.4%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (28 séances) :
      · −1.0% : fill 100% (28/28) · rebond 42% (12/28)
      · −2.0% : fill 90% (25/28) · rebond 60% (14/25)
      · −3.0% : fill 84% (22/28) · rebond 71% (15/22)
      · −4.0% : fill 74% (20/28) · rebond 83% (16/20)
      · −5.0% : fill 54% (14/28) · rebond 83% (12/14)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (83 séances) :
      · −1.0% : fill 55% (45/83) · rebond 69% (32/45)
      · −2.0% : fill 38% (29/83) · rebond 70% (20/29)
      · −3.0% : fill 27% (19/83) · rebond 82% (15/19)
      · −4.0% : fill 11% (9/83) · rebond 100% (9/9)
      · −5.0% : fill 8% (7/83) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=129) : 28% en base · 54% si les 15 1res min sont vertes (39 cas) · 15% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=129) : COUDE à **51min** → P(séance verte=clôture>ouverture) 75% si début vert vs 8% si rouge (base 28% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=39) : tient le vert **75%** · continue >prix actuel 46% ; creux résiduel méd -2.3% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.3% / q75 +2.41% → **scale +1.3% / runner +2.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **8%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.44%** (au-delà de la MAE q10 -4.44%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=129) : retour [-4.75% .. +4.08%] · haut q95 +5.67% · bas q05 -6.05%
   - 60min (n=129) : retour [-4.98% .. +4.5%] · haut q95 +6.4% · bas q05 -6.68%
   - 2h (n=129) : retour [-7.27% .. +3.75%] · haut q95 +6.4% · bas q05 -8.0%
   - 4h (n=129) : retour [-7.05% .. +5.53%] · haut q95 +7.09% · bas q05 -8.22%
   - 6h (n=129) : retour [-6.84% .. +4.35%] · haut q95 +7.17% · bas q05 -8.63%
   - session (n=129) : retour [-6.58% .. +4.66%] · haut q95 +7.17% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.8% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -282.67  _(bearish_recent)_
- **BB** : %B -0.01 · largeur 25.6%
- **ATR** : 89357.14 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.154  _(distribution)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 1096200.0 · MA50 1181400.0 · MA200 1147797.86  _(prix < MA20)_
- **Dist MA** : MA20 -13.1% · MA50 -19.3% · MA200 -17.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83329 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
