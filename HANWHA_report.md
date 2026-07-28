# 012450

**Generated** : 2026-07-28T21:52:53.769018+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩875000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩875000.00 (+2.0% vs entrée) · entrée ₩858119.85 · stop ₩829454.78 · T1 ₩915449.98 · R/R 2.0  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.32 _(réel 5 s)_ (GBM 0.07) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩846653.82–₩869585.88 (mid ₩858119.85)
- Spot actuel : ₩875000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩829454.78 (stop swing_plan-based (-5.21%))
- Targets : T1 ₩915449.98 · R/R 2.0 | T2 ₩972780.11 · R/R 4.0 | T3 ₩1030110.25 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩829454.78


## Edge, scénarios & sizing

- EV/risk : 0.07 | EV/share : ₩1993.920 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 12 % | T3 5 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 18.9 | bear 62.4 | side 18.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.88% → cible +2.988% / stop −8.0%, p_fill 90%, n_eff≈36.9) : P(cible|rempli) **37%** · **EV/risk -0.144** (×p_fill ; si rempli -1.28% du capital)
  - **swing** (entrée dip −1.934% → cible +6.681% / stop −3.34%, p_fill 88%, n_eff≈35.5) : P(cible|rempli) **22%** · **EV/risk -0.320** (×p_fill ; si rempli -1.21% du capital)
  - **deep** (entrée dip −2.977% → cible +9.448% / stop −4.724%, p_fill 89%, n_eff≈34.4) : P(cible|rempli) **18%** · **EV/risk -0.476** (×p_fill ; si rempli -2.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→57% · +2.0%→40% · +3.0%→24% · +5.0%→12% · +8.0%→2%
- Range intraday médian 5.9% (p90 8.67%) · excursion haute méd. +1.66% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.132% vs midi 1.117% vs clôture 1.133% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 87% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -1.608% ; recovery-V 32%
- **σ réalisé intraday** 4.629% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 59% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 898162.5 (VA 879087.5–906337.5 ; dernier close 901000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 80% · **stop −4.98%** sous le fill (sous le bruit) · cible +1.93% · R/R 0.39 (high win-rate)
- Gaps overnight (n=144) : méd. 0.71% · baisse 31% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=145) : bas méd −1.78% (p90 −4.06%) · haut méd +0.77% · range méd 2.83%
- Excursion ouverture 15min (n=145) : bas méd −2.13% (p90 −4.91%) · haut méd +1.02% · range méd 3.43%
- Excursion ouverture 30min (n=145) : bas méd −2.2% (p90 −5.37%) · haut méd +1.08% · range méd 3.99%
- Excursion ouverture 60min (n=145) : bas méd −2.44% (p90 −5.9%) · haut méd +1.29% · range méd 4.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 901000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (104/144) · gap 20% · délai 0.2min · rebond 51% (53/104) (MFE +1.05%)
   - −1.0% : fill 30min 56% · séance 70% (100/144) · gap 17% · délai 1.0min · rebond 55% (59/100) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 66% (93/144) · gap 9% · délai 1.5min · rebond 59% (53/93) (MFE +1.26%)
   - −2.0% : fill 30min 45% · séance 59% (77/144) · gap 7% · délai 3.6min · rebond 63% (47/77) (MFE +1.55%)
   - −3.0% : fill 30min 30% · séance 46% (56/144) · gap 2% · délai 6.6min · rebond 69% (38/56) (MFE +1.5%)
   - −4.0% : fill 30min 22% · séance 35% (42/144) · gap 2% · délai 9.6min · rebond 80% (34/42) (MFE +1.93%)
   - −5.0% : fill 30min 13% · séance 26% (31/144) · gap 1% · délai 17.3min · rebond 77% (25/31) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.61%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −2.8%) → stop au-delà de −2.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.56% (p90 −2.77%) → stop au-delà de −2.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=685 jambes) : jambe baissière méd −1.26% (p90 −3.23%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 100% (31/31) · rebond 47% (14/31)
      · −2.0% : fill 93% (28/31) · rebond 61% (16/28)
      · −3.0% : fill 88% (25/31) · rebond 70% (17/25)
      · −4.0% : fill 73% (22/31) · rebond 87% (18/22)
      · −5.0% : fill 50% (15/31) · rebond 85% (13/15)
   - **flat** (19 séances) :
      · −1.0% : fill 88% (18/19) · rebond 41% (9/18)
      · −2.0% : fill 78% (15/19) · rebond 48% (7/15)
      · −3.0% : fill 60% (9/19) · rebond 37% (3/9)
      · −4.0% : fill 60% (9/19) · rebond 48% (5/9)
      · −5.0% : fill 58% (8/19) · rebond 52% (4/8)
   - **gap-up** (94 séances) :
      · −1.0% : fill 55% (51/94) · rebond 66% (36/51)
      · −2.0% : fill 41% (34/94) · rebond 72% (24/34)
      · −3.0% : fill 27% (22/94) · rebond 86% (18/22)
      · −4.0% : fill 14% (11/94) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/94) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 34% en base · 61% si les 15 1res min sont vertes (47 cas) · 20% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 7% si rouge (base 34% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=49) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -2.08% (q20 -3.38%) → **SL/trailing à −3.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.5% → **scale +2.05% / runner +3.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **7%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.78%** (au-delà de la MAE q10 -5.78%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-5.5% .. +3.83%] · haut q95 +5.43% · bas q05 -6.31%
   - 60min (n=145) : retour [-5.29% .. +4.71%] · haut q95 +6.74% · bas q05 -7.06%
   - 2h (n=145) : retour [-7.83% .. +4.53%] · haut q95 +6.94% · bas q05 -8.4%
   - 4h (n=145) : retour [-7.31% .. +5.61%] · haut q95 +7.19% · bas q05 -9.67%
   - 6h (n=145) : retour [-7.24% .. +4.86%] · haut q95 +7.6% · bas q05 -10.31%
   - session (n=145) : retour [-7.65% .. +4.91%] · haut q95 +7.6% · bas q05 -10.31%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 30.7  _(momentum baissier)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -580.1  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 40.3%
- **ATR** : 80285.71 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.184  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 52.3  _(transition)_
- **MA** : MA20 983750.0 · MA50 1073880.0 · MA200 1142249.91  _(prix < MA20)_
- **Dist MA** : MA20 -11.1% · MA50 -18.5% · MA200 -23.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83462 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
