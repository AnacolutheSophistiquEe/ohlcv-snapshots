# AL2SI

**Generated** : 2026-08-12T00:09:32.437420+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €28.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €28.00 (+10.9% vs entrée) · entrée €25.24 · stop €22.76 · T1 €27.09 · R/R 0.75  
> ↳ P(T1 av. stop) 56 % _(réel 5 s)_ · EV/risk -0.056 _(réel 5 s)_ (GBM 0.18) · ¼-Kelly 0.031 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.190 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.88–€25.61 (mid €25.24)
- Spot actuel : €28.00 (+10.9% au-dessus de la zone — repli à attendre)
- Stop : €22.76 (stop swing_plan-based (-18.7%))
- Targets : T1 €27.09 · R/R 0.75 | T2 €28.93 · R/R 1.49 | T3 €30.78 · R/R 2.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.76


## Edge, scénarios & sizing

- EV/risk : 0.18 | EV/share : €0.446 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 33 % | T3 21 %
- Kelly (position) : f* 0.125 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 77.5 | bear 17.5 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 392.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.471% → cible +3.268% / stop −2.783%, p_fill 53%, n_eff≈24.9) : P(cible|rempli) **31%** · **EV/risk -0.109** (×p_fill ; si rempli -0.57% du capital)
  - **swing** (entrée dip −9.838% → cible +7.308% / stop −9.829%, p_fill 40%, n_eff≈16.8) : P(cible|rempli) **56%** · **EV/risk -0.056** (×p_fill ; si rempli -1.39% du capital)
  - **deep** (entrée dip −15.206% → cible +10.335% / stop −15.678%, p_fill 42%, n_eff≈16.6) : P(cible|rempli) **57%** · **EV/risk -0.049** (×p_fill ; si rempli -1.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→69% · +3.0%→60% · +5.0%→42% · +8.0%→19%
- Range intraday médian 8.37% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.64%
- Profil de vol intra : ouverture 5.666% vs midi 1.762% vs clôture 1.941% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -0.216% ; recovery-V 31%
- **σ réalisé intraday** 7.131% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 27.2107 (VA 27.0637–27.4312 ; dernier close 27.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 43% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.29% (p90 −4.83%) · haut méd +1.04% · range méd 3.13%
- Excursion ouverture 15min (n=160) : bas méd −1.69% (p90 −5.83%) · haut méd +1.56% · range méd 4.17%
- Excursion ouverture 30min (n=160) : bas méd −1.76% (p90 −5.86%) · haut méd +2.33% · range méd 4.86%
- Excursion ouverture 60min (n=160) : bas méd −2.29% (p90 −6.95%) · haut méd +2.73% · range méd 6.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 82% (124/159) · gap 27% · délai 0.3min · rebond 66% (82/124) (MFE +3.26%)
   - −1.0% : fill 30min 60% · séance 81% (120/159) · gap 21% · délai 0.4min · rebond 66% (82/120) (MFE +2.54%)
   - −1.5% : fill 30min 54% · séance 77% (110/159) · gap 16% · délai 1.0min · rebond 69% (73/110) (MFE +2.14%)
   - −2.0% : fill 30min 45% · séance 68% (95/159) · gap 10% · délai 4.2min · rebond 63% (61/95) (MFE +1.69%)
   - −3.0% : fill 30min 35% · séance 58% (79/159) · gap 5% · délai 9.4min · rebond 80% (65/79) (MFE +2.2%)
   - −4.0% : fill 30min 26% · séance 50% (68/159) · gap 4% · délai 23.4min · rebond 76% (53/68) (MFE +2.53%)
   - −5.0% : fill 30min 18% · séance 43% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.0% (p90 −5.35%) → stop au-delà de −3.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.36% (p90 −5.44%) → stop au-delà de −3.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.36% (p90 −5.44%) → stop au-delà de −3.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1561 jambes) : jambe baissière méd −1.29% (p90 −3.5%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (51/54) · rebond 64% (33/51)
      · −2.0% : fill 85% (43/54) · rebond 59% (26/43)
      · −3.0% : fill 79% (40/54) · rebond 83% (33/40)
      · −4.0% : fill 70% (35/54) · rebond 80% (29/35)
      · −5.0% : fill 58% (31/54) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 87% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 68% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 54% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 48% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 42% (12/35) · rebond 100% (12/12)
   - **gap-up** (70 séances) :
      · −1.0% : fill 66% (41/70) · rebond 61% (27/41)
      · −2.0% : fill 56% (31/70) · rebond 56% (19/31)
      · −3.0% : fill 45% (24/70) · rebond 76% (19/24)
      · −4.0% : fill 38% (19/70) · rebond 64% (12/19)
      · −5.0% : fill 34% (17/70) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (77 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:06** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 46% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **86%** · continue >prix actuel 58% ; creux résiduel méd -1.74% (q20 -3.87%) → **SL/trailing à −3.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.58% / q75 +5.8% → **scale +2.58% / runner +5.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **10%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.13%** (au-delà de la MAE q10 -8.13%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.62% .. +6.16%] · haut q95 +8.2% · bas q05 -7.62%
   - 60min (n=160) : retour [-5.91% .. +8.77%] · haut q95 +9.54% · bas q05 -7.82%
   - 2h (n=160) : retour [-6.15% .. +9.83%] · haut q95 +10.28% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.63% .. +9.63%] · haut q95 +12.3% · bas q05 -10.8%
   - 6h (n=160) : retour [-6.79% .. +10.53%] · haut q95 +14.67% · bas q05 -11.09%
   - session (n=160) : retour [-8.39% .. +13.46%] · haut q95 +14.97% · bas q05 -11.85%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.2  _(neutre)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist 0.702  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 20.8%
- **ATR** : 2.48 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.192  _(distribution)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 59.6  _(transition)_
- **MA** : MA20 26.69 · MA50 33.95 · MA200 25.14  _(prix > MA20)_
- **Dist MA** : MA20 +4.9% · MA50 -17.5% · MA200 +11.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94189 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
