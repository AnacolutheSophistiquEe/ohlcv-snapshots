# 267260

**Generated** : 2026-07-24T21:50:31.972513+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩810000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩810000.00 (+2.2% vs entrée) · entrée ₩792663.72 · stop ₩729250.62 · T1 ₩832775.15 · R/R 0.63  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.022 _(réel 5 s)_ (GBM -0.172) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩788095.16–₩797232.29 (mid ₩792663.72)
- Spot actuel : ₩810000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩729250.62 (stop swing_plan-based (-7.77%))
- Targets : T1 ₩832775.15 · R/R 0.63 | T2 ₩846879.84 · R/R 0.85 | T3 ₩860984.54 · R/R 1.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩729250.62


## Edge, scénarios & sizing

- EV/risk : -0.172 | EV/share : ₩-10914.979 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.5 | bear 39.5 | side 48.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.141% → cible +5.06% / stop −8.0%, p_fill 83%, n_eff≈33.6) : P(cible|rempli) **20%** · **EV/risk -0.022** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −4.709% → cible +6.424% / stop −3.212%, p_fill 70%, n_eff≈27.0) : P(cible|rempli) **25%** · **EV/risk -0.178** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −7.278% → cible +9.085% / stop −4.543%, p_fill 75%, n_eff≈26.3) : P(cible|rempli) **28%** · **EV/risk -0.164** (×p_fill ; si rempli -0.99% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→46% · +3.0%→30% · +5.0%→10% · +8.0%→5%
- Range intraday médian 6.16% (p90 10.49%) · excursion haute méd. +1.84% / basse méd. −3.53%
- Profil de vol intra : ouverture 4.012% vs midi 1.061% vs clôture 1.145% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. -1.596% ; recovery-V 20%
- **σ réalisé intraday** 4.783% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 73% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 822837.5 (VA 810812.5–826537.5 ; dernier close 793000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 84% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.39% · R/R 0.57 (high win-rate)
- Gaps overnight (n=137) : méd. 0.76% · baisse 39% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=138) : bas méd −1.57% (p90 −3.73%) · haut méd +0.94% · range méd 2.69%
- Excursion ouverture 15min (n=138) : bas méd −1.79% (p90 −4.66%) · haut méd +1.06% · range méd 3.35%
- Excursion ouverture 30min (n=138) : bas méd −2.18% (p90 −4.9%) · haut méd +1.12% · range méd 3.67%
- Excursion ouverture 60min (n=138) : bas méd −2.56% (p90 −5.62%) · haut méd +1.33% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 793000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (97/137) · gap 31% · délai 0.0min · rebond 53% (54/97) (MFE +1.19%)
   - −1.0% : fill 30min 55% · séance 69% (90/137) · gap 24% · délai 0.3min · rebond 53% (52/90) (MFE +1.01%)
   - −1.5% : fill 30min 48% · séance 62% (77/137) · gap 15% · délai 0.5min · rebond 66% (50/77) (MFE +1.28%)
   - −2.0% : fill 30min 43% · séance 58% (70/137) · gap 10% · délai 0.8min · rebond 67% (47/70) (MFE +1.7%)
   - −3.0% : fill 30min 32% · séance 49% (55/137) · gap 6% · délai 5.1min · rebond 77% (38/55) (MFE +1.76%)
   - −4.0% : fill 30min 24% · séance 42% (46/137) · gap 3% · délai 14.8min · rebond 80% (37/46) (MFE +2.33%)
   - −5.0% : fill 30min 15% · séance 35% (36/137) · gap 2% · délai 46.8min · rebond 84% (28/36) (MFE +2.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −3.5%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.37%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −4.8%) → stop au-delà de −3.54% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=677 jambes) : jambe baissière méd −1.32% (p90 −3.59%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 98% (46/47) · rebond 46% (24/46)
      · −2.0% : fill 91% (39/47) · rebond 60% (23/39)
      · −3.0% : fill 80% (33/47) · rebond 76% (22/33)
      · −4.0% : fill 71% (29/47) · rebond 83% (24/29)
      · −5.0% : fill 60% (22/47) · rebond 85% (17/22)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (73 séances) :
      · −1.0% : fill 47% (30/73) · rebond 64% (21/30)
      · −2.0% : fill 34% (19/73) · rebond 71% (15/19)
      · −3.0% : fill 24% (11/73) · rebond 73% (8/11)
      · −4.0% : fill 22% (10/73) · rebond 82% (8/10)
      · −5.0% : fill 16% (7/73) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 34% en base · 48% si les 15 1res min sont vertes (65 cas) · 24% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=138) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 72% si début vert vs 10% si rouge (base 34% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **72%** · continue >prix actuel 42% ; creux résiduel méd -1.63% (q20 -3.72%) → **SL/trailing à −3.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.55% → **scale +1.21% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +1.64% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-5.16% .. +2.91%] · haut q95 +4.36% · bas q05 -5.64%
   - 60min (n=138) : retour [-5.58% .. +3.22%] · haut q95 +4.55% · bas q05 -6.02%
   - 2h (n=138) : retour [-6.92% .. +3.67%] · haut q95 +5.38% · bas q05 -7.4%
   - 4h (n=138) : retour [-6.94% .. +4.23%] · haut q95 +5.52% · bas q05 -8.14%
   - 6h (n=138) : retour [-6.92% .. +3.8%] · haut q95 +7.39% · bas q05 -8.83%
   - session (n=138) : retour [-7.05% .. +3.92%] · haut q95 +7.39% · bas q05 -9.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.8  _(momentum baissier)_
- **ADX** : 24.5  _(pas de tendance nette)_
- **MACD** : hist 4707.132  _(bullish_recent)_
- **BB** : %B 0.33 · largeur 35.5%
- **ATR** : 63928.57 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.063  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 50.5  _(transition)_
- **MA** : MA20 861750.0 · MA50 987600.0 · MA200 919727.1  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -18.0% · MA200 -11.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83860 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
