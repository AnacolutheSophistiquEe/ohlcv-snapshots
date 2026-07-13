# RHM

**Generated** : 2026-07-13T00:01:56.883521+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €992.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €992.00 (+1.6% vs entrée) · entrée €976.20 · stop €956.68 · T1 €1006.00 · R/R 1.53  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.122 _(réel 5 s)_ (GBM 0.003) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €970.24–€982.16 (mid €976.20)
- Spot actuel : €992.00 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €956.68 (stop swing_plan-based (-6.8%))
- Targets : T1 €1006.00 · R/R 1.53 | T2 €1035.81 · R/R 3.05 | T3 €1065.61 · R/R 4.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €956.68


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : €0.067 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.014 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.6 | bear 5.0 | side 64.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.592% → cible +3.053% / stop −2.0%, p_fill 60%, n_eff≈22.2) : P(cible|rempli) **19%** · **EV/risk -0.122** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −3.506% → cible +6.827% / stop −3.413%, p_fill 31%, n_eff≈12.9) : P(cible|rempli) **14%** · **EV/risk -0.162** (×p_fill ; si rempli -1.78% du capital)
  - **deep** (entrée dip −5.414% → cible +9.654% / stop −4.827%, p_fill 40%, n_eff≈16.5) : P(cible|rempli) **7%** · **EV/risk -0.225** (×p_fill ; si rempli -2.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→61% · +2.0%→48% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.65%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.577% vs midi 0.902% vs clôture 1.013% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.645% ; recovery-V 36%
- **σ réalisé intraday** 2.83% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 74% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 994.9175 (VA 989.9125–1004.9275 ; dernier close 990.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 32% · rebond 61% · **stop −3.26%** sous le fill (sous le bruit) · cible +1.31% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 41% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −1.53%) · haut méd +0.5% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −1.97%) · haut méd +0.67% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −2.59%) · haut méd +0.87% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.77%) · haut méd +1.0% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 990.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (120/159) · gap 28% · délai 0.3min · rebond 56% (63/120) (MFE +1.19%)
   - −1.0% : fill 30min 49% · séance 72% (107/159) · gap 14% · délai 5.6min · rebond 59% (61/107) (MFE +1.41%)
   - −1.5% : fill 30min 31% · séance 56% (80/159) · gap 8% · délai 22.3min · rebond 48% (40/80) (MFE +0.9%)
   - −2.0% : fill 30min 22% · séance 47% (69/159) · gap 6% · délai 30.7min · rebond 60% (40/69) (MFE +1.27%)
   - −3.0% : fill 30min 10% · séance 32% (46/159) · gap 3% · délai 118.9min · rebond 61% (29/46) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 22% (27/159) · gap 2% · délai 152.5min · rebond 54% (15/27) (MFE +1.23%)
   - −5.0% : fill 30min 2% · séance 13% (16/159) · gap 2% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −1.53%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.68%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −1.64%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=465 jambes) : jambe baissière méd −1.1% (p90 −2.63%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 93% (47/49) · rebond 59% (25/47)
      · −2.0% : fill 78% (37/49) · rebond 62% (23/37)
      · −3.0% : fill 50% (26/49) · rebond 61% (17/26)
      · −4.0% : fill 33% (14/49) · rebond 61% (9/14)
      · −5.0% : fill 21% (9/49) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 79% (37/50) · rebond 67% (24/37)
      · −2.0% : fill 36% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 24% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 22% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 14% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 48% (23/60) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/60) · rebond 46% (7/14)
      · −3.0% : fill 22% (9/60) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/60) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 67% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 79% si début vert vs 22% si rouge (base 48% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **79%** · continue >prix actuel 48% ; creux résiduel méd -1.37% (q20 -2.38%) → **SL/trailing à −2.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.87% → **scale +1.19% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.99%** (au-delà de la MAE q10 -4.99%), cible rebond +1.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +3.13%] · haut q95 +3.83% · bas q05 -2.94%
   - 60min (n=160) : retour [-3.63% .. +3.1%] · haut q95 +4.04% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.7% .. +2.86%] · haut q95 +4.15% · bas q05 -4.99%
   - 4h (n=160) : retour [-4.07% .. +3.02%] · haut q95 +4.54% · bas q05 -5.17%
   - 6h (n=160) : retour [-4.78% .. +3.4%] · haut q95 +4.54% · bas q05 -5.79%
   - session (n=160) : retour [-6.42% .. +4.23%] · haut q95 +4.76% · bas q05 -6.89%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 33.8  _(momentum baissier)_
- **ADX** : 23.9  _(pas de tendance nette)_
- **MACD** : hist 1.988  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 33.2%
- **ATR** : 60.05 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.136  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 1078.69 · MA50 1168.16 · MA200 1524.94  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -15.1% · MA200 -34.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92262 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
