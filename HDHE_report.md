# 267260

**Generated** : 2026-08-11T21:51:17.672499+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩738000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩738000.00 (+4.2% vs entrée) · entrée ₩708326.24 · stop ₩651660.14 · T1 ₩739394.58 · R/R 0.55  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.017 _(réel 5 s)_ (GBM -0.173) · ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩702507.67–₩714144.81 (mid ₩708326.24)
- Spot actuel : ₩738000.00 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : ₩651660.14 (stop swing_plan-based (-19.78%))
- Targets : T1 ₩739394.58 · R/R 0.55 | T2 ₩767367.47 · R/R 1.04 | T3 ₩795340.37 · R/R 1.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩651660.14


## Edge, scénarios & sizing

- EV/risk : -0.173 | EV/share : ₩-9796.486 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.005 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.1 | bear 65.0 | side 25.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.022% → cible +4.386% / stop −8.0%, p_fill 49%, n_eff≈21.8) : P(cible|rempli) **21%** · **EV/risk -0.017** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −8.841% → cible +24.419% / stop −12.0%, p_fill 35%, n_eff≈13.9) : P(cible|rempli) **4%** · **EV/risk -0.156** (×p_fill ; si rempli -5.42% du capital)
  - **deep** (entrée dip −13.672% → cible +12.949% / stop −16.18%, p_fill 33%, n_eff≈12.0) : P(cible|rempli) **21%** · **EV/risk -0.104** (×p_fill ; si rempli -5.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→46% · +3.0%→36% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.84% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.448% vs midi 1.208% vs clôture 1.254% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 81% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -1.673% ; recovery-V 24%
- **σ réalisé intraday** 4.917% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 71% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 747550.0 (VA 746450.0–755250.0 ; dernier close 765000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 82% · **stop −4.53%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.56 (high win-rate)
- Gaps overnight (n=149) : méd. 1.13% · baisse 39% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=150) : bas méd −1.74% (p90 −4.15%) · haut méd +1.03% · range méd 2.95%
- Excursion ouverture 15min (n=150) : bas méd −1.98% (p90 −4.7%) · haut méd +1.08% · range méd 3.61%
- Excursion ouverture 30min (n=150) : bas méd −2.34% (p90 −5.12%) · haut méd +1.28% · range méd 3.96%
- Excursion ouverture 60min (n=150) : bas méd −2.95% (p90 −5.71%) · haut méd +1.41% · range méd 4.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 765000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (105/149) · gap 31% · délai 0.0min · rebond 55% (59/105) (MFE +1.27%)
   - −1.0% : fill 30min 56% · séance 68% (98/149) · gap 22% · délai 0.2min · rebond 60% (59/98) (MFE +1.41%)
   - −1.5% : fill 30min 47% · séance 63% (85/149) · gap 16% · délai 0.4min · rebond 68% (56/85) (MFE +1.39%)
   - −2.0% : fill 30min 43% · séance 58% (77/149) · gap 12% · délai 0.7min · rebond 71% (53/77) (MFE +1.79%)
   - −3.0% : fill 30min 32% · séance 49% (61/149) · gap 7% · délai 2.8min · rebond 78% (43/61) (MFE +2.17%)
   - −4.0% : fill 30min 23% · séance 40% (50/149) · gap 4% · délai 15.0min · rebond 76% (39/50) (MFE +2.34%)
   - −5.0% : fill 30min 15% · séance 35% (40/149) · gap 1% · délai 39.2min · rebond 82% (31/40) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.6%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.68%) → stop au-delà de −2.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.26% (p90 −5.02%) → stop au-delà de −3.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=771 jambes) : jambe baissière méd −1.27% (p90 −3.56%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (51/52) · rebond 55% (28/51)
      · −2.0% : fill 93% (44/52) · rebond 66% (27/44)
      · −3.0% : fill 85% (38/52) · rebond 78% (26/38)
      · −4.0% : fill 73% (33/52) · rebond 75% (26/33)
      · −5.0% : fill 65% (26/52) · rebond 82% (20/26)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (80 séances) :
      · −1.0% : fill 46% (33/80) · rebond 71% (24/33)
      · −2.0% : fill 33% (21/80) · rebond 77% (17/21)
      · −3.0% : fill 22% (12/80) · rebond 77% (9/12)
      · −4.0% : fill 17% (10/80) · rebond 82% (8/10)
      · −5.0% : fill 12% (7/80) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 34% en base · 50% si les 15 1res min sont vertes (68 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 69% si début vert vs 11% si rouge (base 34% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **69%** · continue >prix actuel 42% ; creux résiduel méd -1.83% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.69% → **scale +1.38% / runner +2.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **11%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.38%** (au-delà de la MAE q10 -5.38%), cible rebond +1.77% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-5.46% .. +2.69%] · haut q95 +4.18% · bas q05 -5.79%
   - 60min (n=150) : retour [-5.67% .. +2.79%] · haut q95 +4.42% · bas q05 -6.25%
   - 2h (n=150) : retour [-7.04% .. +3.69%] · haut q95 +5.1% · bas q05 -7.69%
   - 4h (n=150) : retour [-6.95% .. +3.89%] · haut q95 +5.39% · bas q05 -8.69%
   - 6h (n=150) : retour [-8.2% .. +4.35%] · haut q95 +6.49% · bas q05 -9.39%
   - session (n=150) : retour [-7.63% .. +4.06%] · haut q95 +6.61% · bas q05 -9.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.4  _(neutre)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist 14691.884  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 39.1%
- **ATR** : 68722.43 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.007  _(neutre)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 40.4  _(transition)_
- **MA** : MA20 746889.82 · MA50 883239.68 · MA200 923443.92  _(prix < MA20)_
- **Dist MA** : MA20 -1.2% · MA50 -16.4% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83663 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
