# AL2SI

**Generated** : 2026-07-08T00:08:45.668088+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €36.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €36.48 (+2.5% vs entrée) · entrée €35.58 · stop €31.31 · T1 €50.24 · R/R 3.43  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk -0.014 _(réel 5 s)_ (GBM 0.441) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €34.68–€36.48 (mid €35.58)
- Spot actuel : €36.48 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €31.31 (stop swing_plan-based (-14.17%))
- Targets : T1 €50.24 · R/R 3.43 | T2 €53.22 · R/R 4.13 | T3 €56.20 · R/R 4.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €31.31


## Edge, scénarios & sizing

- EV/risk : 0.441 | EV/share : €1.885 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 3 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.3 | bear 64.3 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 365.0 (= 10 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.119% → cible +18.496% / stop −8.0%, p_fill 81%, n_eff≈32.3) : P(cible|rempli) **2%** · **EV/risk -0.062** (×p_fill ; si rempli -0.61% du capital)
  - **swing** (entrée dip −2.466% → cible +41.217% / stop −12.0%, p_fill 71%, n_eff≈27.2) : P(cible|rempli) **11%** · **EV/risk -0.014** (×p_fill ; si rempli -0.24% du capital)
  - **deep** (entrée dip −3.61% → cible +70.492% / stop −18.0%, p_fill 64%, n_eff≈23.6) : P(cible|rempli) **7%** · **EV/risk -0.243** (×p_fill ; si rempli -6.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→76% · +3.0%→66% · +5.0%→42% · +8.0%→24%
- Range intraday médian 7.94% (p90 17.21%) · excursion haute méd. +4.29% / basse méd. −3.05%
- Profil de vol intra : ouverture 5.606% vs midi 1.686% vs clôture 1.938% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 73% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.161 ; neutre — autocorr -0.02)_ ; drift intra méd. 1.415% ; recovery-V 36%
- **σ réalisé intraday** 8.392% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 38.9688 (VA 37.5973–39.7073 ; dernier close 39.22)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 88% · **stop −6.02%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.47 (high win-rate)
- Gaps overnight (n=141) : méd. 0.21% · baisse 38% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=142) : bas méd −1.0% (p90 −5.38%) · haut méd +1.04% · range méd 3.0%
- Excursion ouverture 15min (n=142) : bas méd −1.5% (p90 −5.86%) · haut méd +1.55% · range méd 4.03%
- Excursion ouverture 30min (n=142) : bas méd −1.58% (p90 −5.86%) · haut méd +2.06% · range méd 4.71%
- Excursion ouverture 60min (n=142) : bas méd −2.05% (p90 −6.97%) · haut méd +2.69% · range méd 5.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 78% (108/141) · gap 29% · délai 0.3min · rebond 68% (72/108) (MFE +3.15%)
   - −1.0% : fill 30min 57% · séance 76% (103/141) · gap 22% · délai 0.4min · rebond 72% (72/103) (MFE +2.62%)
   - −1.5% : fill 30min 48% · séance 70% (93/141) · gap 13% · délai 1.5min · rebond 68% (60/93) (MFE +1.85%)
   - −2.0% : fill 30min 41% · séance 61% (80/141) · gap 9% · délai 3.1min · rebond 67% (53/80) (MFE +1.79%)
   - −3.0% : fill 30min 30% · séance 50% (64/141) · gap 6% · délai 9.1min · rebond 80% (52/64) (MFE +2.37%)
   - −4.0% : fill 30min 24% · séance 42% (54/141) · gap 6% · délai 13.0min · rebond 76% (42/54) (MFE +2.91%)
   - −5.0% : fill 30min 19% · séance 37% (46/141) · gap 5% · délai 18.8min · rebond 88% (43/46) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −5.68%) → stop au-delà de −3.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −5.7%) → stop au-delà de −4.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −3.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1349 jambes) : jambe baissière méd −1.24% (p90 −3.25%) · ~19.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (46/50) · rebond 68% (31/46)
      · −2.0% : fill 85% (39/50) · rebond 56% (24/39)
      · −3.0% : fill 82% (35/50) · rebond 76% (28/35)
      · −4.0% : fill 69% (30/50) · rebond 71% (24/30)
      · −5.0% : fill 60% (27/50) · rebond 77% (24/27)
   - **flat** (30 séances) :
      · −1.0% : fill 81% (23/30) · rebond 79% (18/23)
      · −2.0% : fill 64% (17/30) · rebond 86% (13/17)
      · −3.0% : fill 42% (11/30) · rebond 92% (10/11)
      · −4.0% : fill 42% (11/30) · rebond 94% (10/11)
      · −5.0% : fill 34% (9/30) · rebond 100% (9/9)
   - **gap-up** (61 séances) :
      · −1.0% : fill 56% (34/61) · rebond 73% (23/34)
      · −2.0% : fill 40% (24/61) · rebond 69% (16/24)
      · −3.0% : fill 29% (18/61) · rebond 80% (14/18)
      · −4.0% : fill 22% (13/61) · rebond 70% (8/13)
      · −5.0% : fill 20% (10/61) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 52% en base · 69% si les 15 1res min sont vertes (69 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=142) : COUDE à **31min** → P(séance verte=clôture>ouverture) 76% si début vert vs 27% si rouge (base 52% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 59% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.09% → **scale +3.7% / runner +6.09%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.52%** (au-delà de la MAE q10 -8.52%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-4.84% .. +9.25%] · haut q95 +9.85% · bas q05 -7.69%
   - 60min (n=142) : retour [-5.94% .. +10.71%] · haut q95 +10.86% · bas q05 -7.87%
   - 2h (n=142) : retour [-5.57% .. +10.51%] · haut q95 +11.83% · bas q05 -8.03%
   - 4h (n=142) : retour [-7.59% .. +13.11%] · haut q95 +13.92% · bas q05 -10.63%
   - 6h (n=142) : retour [-7.18% .. +15.24%] · haut q95 +20.84% · bas q05 -11.21%
   - session (n=142) : retour [-9.79% .. +21.18%] · haut q95 +23.4% · bas q05 -14.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.24%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.9  _(momentum baissier)_
- **ADX** : 22.3  _(pas de tendance nette)_
- **MACD** : hist 0.927  _(bullish_recent)_
- **BB** : %B 0.52 · largeur 106.0%
- **ATR** : 6.11 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.008  _(neutre)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 48.9  _(transition)_
- **MA** : MA20 35.83 · MA50 40.78 · MA200 23.34  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 -10.5% · MA200 +56.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94560 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
