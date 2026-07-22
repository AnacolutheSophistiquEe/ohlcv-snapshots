# 298040

**Generated** : 2026-07-22T21:52:15.636700+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2679000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩2679000.00 (+0.5% vs entrée) · entrée ₩2666255.18 · stop ₩2452954.76 · T1 ₩2753100.61 · R/R 0.41  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.123 _(réel 5 s)_ (GBM -0.112) · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2653510.36–₩2679000.00 (mid ₩2666255.18)
- Spot actuel : ₩2679000.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : ₩2452954.76 (stop swing_plan-based (-4.49%))
- Targets : T1 ₩2753100.61 · R/R 0.41 | T2 ₩2839946.05 · R/R 0.81 | T3 ₩2926791.48 · R/R 1.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2452954.76


## Edge, scénarios & sizing

- EV/risk : -0.112 | EV/share : ₩-23868.748 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.124 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.9 | bear 78.2 | side 14.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.478% → cible +3.257% / stop −8.0%, p_fill 95%, n_eff≈38.6) : P(cible|rempli) **38%** · **EV/risk -0.123** (×p_fill ; si rempli -1.03% du capital)
  - **swing** (entrée dip −0.88% → cible +7.283% / stop −3.642%, p_fill 96%, n_eff≈37.8) : P(cible|rempli) **26%** · **EV/risk -0.245** (×p_fill ; si rempli -0.93% du capital)
  - **deep** (entrée dip −1.181% → cible +10.3% / stop −5.15%, p_fill 93%, n_eff≈35.4) : P(cible|rempli) **24%** · **EV/risk -0.337** (×p_fill ; si rempli -1.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→64% · +2.0%→52% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 6.88% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.225% vs midi 1.041% vs clôture 1.134% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; mean-reverting — autocorr -0.09)_ ; drift intra méd. -1.605% ; recovery-V 32%
- **σ réalisé intraday** 5.288% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 69% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 2619350.0 (VA 2532650.0–2619350.0 ; dernier close 2572000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 92% · **stop −5.21%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=136) : méd. 0.52% · baisse 40% (gap-down >1% 25% · >2% 17%)
- Excursion ouverture 5min (n=137) : bas méd −1.29% (p90 −3.44%) · haut méd +0.81% · range méd 2.69%
- Excursion ouverture 15min (n=137) : bas méd −1.95% (p90 −4.76%) · haut méd +1.11% · range méd 3.74%
- Excursion ouverture 30min (n=137) : bas méd −2.46% (p90 −4.91%) · haut méd +1.12% · range méd 4.12%
- Excursion ouverture 60min (n=137) : bas méd −2.58% (p90 −5.31%) · haut méd +1.36% · range méd 4.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2572000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (94/136) · gap 34% · délai 0.0min · rebond 60% (58/94) (MFE +1.39%)
   - −1.0% : fill 30min 57% · séance 69% (86/136) · gap 25% · délai 0.9min · rebond 59% (53/86) (MFE +1.56%)
   - −1.5% : fill 30min 49% · séance 61% (77/136) · gap 21% · délai 1.3min · rebond 54% (47/77) (MFE +1.44%)
   - −2.0% : fill 30min 44% · séance 58% (68/136) · gap 17% · délai 3.2min · rebond 52% (37/68) (MFE +1.33%)
   - −3.0% : fill 30min 33% · séance 47% (55/136) · gap 8% · délai 5.4min · rebond 56% (31/55) (MFE +1.27%)
   - −4.0% : fill 30min 23% · séance 43% (47/136) · gap 5% · délai 23.9min · rebond 76% (36/47) (MFE +1.91%)
   - −5.0% : fill 30min 19% · séance 34% (35/136) · gap 4% · délai 22.9min · rebond 92% (30/35) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.27%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.82% (p90 −4.2%) → stop au-delà de −2.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −4.2%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=726 jambes) : jambe baissière méd −1.43% (p90 −3.46%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 100% (48/48) · rebond 60% (30/48)
      · −2.0% : fill 87% (40/48) · rebond 54% (22/40)
      · −3.0% : fill 83% (38/48) · rebond 55% (21/38)
      · −4.0% : fill 79% (33/48) · rebond 80% (25/33)
      · −5.0% : fill 66% (27/48) · rebond 90% (22/27)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 45% (28/73) · rebond 59% (16/28)
      · −2.0% : fill 34% (21/73) · rebond 42% (10/21)
      · −3.0% : fill 23% (13/73) · rebond 43% (6/13)
      · −4.0% : fill 17% (10/73) · rebond 71% (8/10)
      · −5.0% : fill 12% (6/73) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 39% en base · 62% si les 15 1res min sont vertes (55 cas) · 28% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=137) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 81% si début vert vs 14% si rouge (base 39% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **81%** · continue >prix actuel 52% ; creux résiduel méd -1.5% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.9% → **scale +1.55% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **14%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.98%** (au-delà de la MAE q10 -4.98%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-4.44% .. +4.28%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=137) : retour [-5.26% .. +4.88%] · haut q95 +6.55% · bas q05 -5.93%
   - 2h (n=137) : retour [-7.26% .. +4.53%] · haut q95 +7.13% · bas q05 -8.17%
   - 4h (n=137) : retour [-7.6% .. +5.34%] · haut q95 +7.93% · bas q05 -9.49%
   - 6h (n=137) : retour [-7.53% .. +5.11%] · haut q95 +8.4% · bas q05 -9.35%
   - session (n=137) : retour [-6.67% .. +5.38%] · haut q95 +8.4% · bas q05 -9.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.88%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 26.3  _(survente)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -28606.574  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 45.7%
- **ATR** : 273857.14 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.197  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 40.2  _(transition)_
- **MA** : MA20 3005950.0 · MA50 3434520.0 · MA200 2607323.14  _(prix < MA20)_
- **Dist MA** : MA20 -10.9% · MA50 -22.0% · MA200 +2.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84782 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
