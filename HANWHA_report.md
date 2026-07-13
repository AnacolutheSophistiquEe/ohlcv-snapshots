# 012450

**Generated** : 2026-07-13T00:18:28.264165+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩967000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩967000.00 (+1.8% vs entrée) · entrée ₩950175.57 · stop ₩874161.53 · T1 ₩1023728.53 · R/R 0.97  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.084 _(réel 5 s)_ (GBM -0.133) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩945036.83–₩955314.32 (mid ₩950175.57)
- Spot actuel : ₩967000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩874161.53 (stop swing_plan-based (-6.73%))
- Targets : T1 ₩1023728.53 · R/R 0.97 | T2 ₩1025375.86 · R/R 0.99 | T3 ₩1027023.18 · R/R 1.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩874161.53


## Edge, scénarios & sizing

- EV/risk : -0.133 | EV/share : ₩-10128.872 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.075 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 35.0 | bear 34.8 | side 30.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.739% → cible +7.741% / stop −8.0%, p_fill 87%, n_eff≈34.0) : P(cible|rempli) **4%** · **EV/risk -0.084** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −3.831% → cible +6.028% / stop −3.014%, p_fill 66%, n_eff≈25.3) : P(cible|rempli) **30%** · **EV/risk -0.092** (×p_fill ; si rempli -0.42% du capital)
  - **deep** (entrée dip −5.92% → cible +8.525% / stop −4.263%, p_fill 66%, n_eff≈24.8) : P(cible|rempli) **32%** · **EV/risk -0.064** (×p_fill ; si rempli -0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→59% · +2.0%→40% · +3.0%→21% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.57% (p90 8.09%) · excursion haute méd. +1.67% / basse méd. −3.17%
- Profil de vol intra : ouverture 3.969% vs midi 1.031% vs clôture 1.098% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 86% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -1.803% ; recovery-V 21%
- **σ réalisé intraday** 4.395% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 34% / bas 62% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 971362.5 (VA 956787.5–971362.5 ; dernier close 966000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 80% · **stop −4.17%** sous le fill (sous le bruit) · cible +2.44% · R/R 0.59 (high win-rate)
- Gaps overnight (n=133) : méd. 0.79% · baisse 30% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=134) : bas méd −1.64% (p90 −4.05%) · haut méd +0.79% · range méd 2.64%
- Excursion ouverture 15min (n=134) : bas méd −1.98% (p90 −4.63%) · haut méd +0.85% · range méd 3.33%
- Excursion ouverture 30min (n=134) : bas méd −2.58% (p90 −4.96%) · haut méd +0.91% · range méd 4.04%
- Excursion ouverture 60min (n=134) : bas méd −2.61% (p90 −5.43%) · haut méd +1.23% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 966000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (96/133) · gap 21% · délai 0.5min · rebond 48% (48/96) (MFE +0.73%)
   - −1.0% : fill 30min 57% · séance 72% (93/133) · gap 17% · délai 1.2min · rebond 57% (56/93) (MFE +1.06%)
   - −1.5% : fill 30min 53% · séance 67% (86/133) · gap 9% · délai 2.6min · rebond 59% (49/86) (MFE +1.33%)
   - −2.0% : fill 30min 45% · séance 58% (70/133) · gap 6% · délai 4.5min · rebond 65% (43/70) (MFE +1.47%)
   - −3.0% : fill 30min 29% · séance 46% (51/133) · gap 3% · délai 9.3min · rebond 72% (35/51) (MFE +1.54%)
   - −4.0% : fill 30min 21% · séance 32% (37/133) · gap 2% · délai 14.3min · rebond 80% (30/37) (MFE +2.13%)
   - −5.0% : fill 30min 10% · séance 26% (28/133) · gap 2% · délai 49.2min · rebond 80% (23/28) (MFE +2.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.65% (p90 −2.54%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.84% (p90 −2.92%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.9%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=607 jambes) : jambe baissière méd −1.3% (p90 −3.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (29 séances) :
      · −1.0% : fill 100% (29/29) · rebond 47% (13/29)
      · −2.0% : fill 91% (26/29) · rebond 63% (15/26)
      · −3.0% : fill 86% (23/29) · rebond 74% (16/23)
      · −4.0% : fill 68% (20/29) · rebond 83% (16/20)
      · −5.0% : fill 50% (14/29) · rebond 83% (12/14)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (87 séances) :
      · −1.0% : fill 55% (47/87) · rebond 69% (34/47)
      · −2.0% : fill 38% (30/87) · rebond 70% (21/30)
      · −3.0% : fill 27% (20/87) · rebond 82% (16/20)
      · −4.0% : fill 11% (9/87) · rebond 100% (9/9)
      · −5.0% : fill 8% (7/87) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 30% en base · 55% si les 15 1res min sont vertes (42 cas) · 18% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=134) : COUDE à **51min** → P(séance verte=clôture>ouverture) 77% si début vert vs 8% si rouge (base 30% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=43) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -2.08% (q20 -3.42%) → **SL/trailing à −3.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.49% / q75 +2.41% → **scale +1.49% / runner +2.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **8%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.43%** (au-delà de la MAE q10 -4.43%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-4.68% .. +4.15%] · haut q95 +5.68% · bas q05 -6.03%
   - 60min (n=134) : retour [-4.95% .. +4.51%] · haut q95 +6.43% · bas q05 -6.54%
   - 2h (n=134) : retour [-7.2% .. +3.85%] · haut q95 +6.43% · bas q05 -7.99%
   - 4h (n=134) : retour [-6.86% .. +5.53%] · haut q95 +7.09% · bas q05 -8.03%
   - 6h (n=134) : retour [-6.83% .. +4.38%] · haut q95 +7.17% · bas q05 -8.52%
   - session (n=134) : retour [-6.57% .. +4.66%] · haut q95 +7.17% · bas q05 -8.52%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.0  _(momentum baissier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist -5237.47  _(bearish_recent)_
- **BB** : %B 0.09 · largeur 27.9%
- **ATR** : 88357.14 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.126  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 1090650.0 · MA50 1171660.0 · MA200 1147836.76  _(prix < MA20)_
- **Dist MA** : MA20 -11.3% · MA50 -17.5% · MA200 -15.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83966 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
