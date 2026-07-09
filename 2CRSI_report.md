# AL2SI

**Generated** : 2026-07-09T00:11:04.195979+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €32.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €32.40 (+2.8% vs entrée) · entrée €31.52 · stop €29.77 · T1 €35.02 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.152 _(réel 5 s)_ (GBM 0.491) · ¼-Kelly 0.016 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €30.82–€32.22 (mid €31.52)
- Spot actuel : €32.40 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €29.77 (stop swing_plan-based (-8.12%))
- Targets : T1 €35.02 · R/R 2.0 | T2 €42.74 · R/R 6.41 | T3 €49.97 · R/R 10.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €29.77


## Edge, scénarios & sizing

- EV/risk : 0.491 | EV/share : €0.860 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 5 % | T3 1 %
- Kelly (position) : f* 0.065 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 26.9 | bear 64.6 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 389.0 (= 12 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.232% → cible +3.188% / stop −4.888%, p_fill 81%, n_eff≈32.0) : P(cible|rempli) **49%** · **EV/risk -0.060** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −2.718% → cible +11.106% / stop −5.553%, p_fill 68%, n_eff≈26.8) : P(cible|rempli) **30%** · **EV/risk -0.152** (×p_fill ; si rempli -1.25% du capital)
  - **deep** (entrée dip −4.195% → cible +37.705% / stop −18.0%, p_fill 65%, n_eff≈23.4) : P(cible|rempli) **14%** · **EV/risk -0.304** (×p_fill ; si rempli -8.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→75% · +3.0%→65% · +5.0%→42% · +8.0%→24%
- Range intraday médian 8.12% (p90 17.21%) · excursion haute méd. +4.23% / basse méd. −3.14%
- Profil de vol intra : ouverture 5.611% vs midi 1.682% vs clôture 1.961% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 73% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.163 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. 1.006% ; recovery-V 34%
- **σ réalisé intraday** 8.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 64% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 38.1898 (VA 37.6287–38.6573 ; dernier close 36.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 88% · **stop −5.54%** sous le fill (sous le bruit) · cible +2.51% · R/R 0.45 (high win-rate)
- Gaps overnight (n=142) : méd. 0.23% · baisse 37% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=143) : bas méd −1.02% (p90 −5.33%) · haut méd +1.05% · range méd 3.01%
- Excursion ouverture 15min (n=143) : bas méd −1.53% (p90 −5.86%) · haut méd +1.58% · range méd 4.11%
- Excursion ouverture 30min (n=143) : bas méd −1.6% (p90 −5.86%) · haut méd +2.05% · range méd 4.78%
- Excursion ouverture 60min (n=143) : bas méd −2.14% (p90 −6.97%) · haut méd +2.64% · range méd 5.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 78% (109/142) · gap 28% · délai 0.3min · rebond 69% (73/109) (MFE +3.04%)
   - −1.0% : fill 30min 58% · séance 76% (104/142) · gap 22% · délai 0.4min · rebond 73% (73/104) (MFE +2.77%)
   - −1.5% : fill 30min 49% · séance 70% (94/142) · gap 13% · délai 1.9min · rebond 68% (61/94) (MFE +2.04%)
   - −2.0% : fill 30min 42% · séance 61% (81/142) · gap 8% · délai 3.8min · rebond 68% (54/81) (MFE +1.87%)
   - −3.0% : fill 30min 29% · séance 51% (65/142) · gap 6% · délai 10.6min · rebond 81% (53/65) (MFE +2.32%)
   - −4.0% : fill 30min 23% · séance 43% (55/142) · gap 5% · délai 15.0min · rebond 77% (43/55) (MFE +2.75%)
   - −5.0% : fill 30min 19% · séance 38% (47/142) · gap 5% · délai 29.3min · rebond 88% (44/47) (MFE +2.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −5.63%) → stop au-delà de −3.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −5.7%) → stop au-delà de −4.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −3.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1359 jambes) : jambe baissière méd −1.24% (p90 −3.25%) · ~20.0 jambes/séance
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
   - **gap-up** (62 séances) :
      · −1.0% : fill 58% (35/62) · rebond 75% (24/35)
      · −2.0% : fill 43% (25/62) · rebond 72% (17/25)
      · −3.0% : fill 32% (19/62) · rebond 83% (15/19)
      · −4.0% : fill 25% (14/62) · rebond 75% (9/14)
      · −5.0% : fill 24% (11/62) · rebond 100% (11/11)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 51% en base · 69% si les 15 1res min sont vertes (69 cas) · 36% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=143) : COUDE à **31min** → P(séance verte=clôture>ouverture) 76% si début vert vs 26% si rouge (base 51% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 59% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.09% → **scale +3.7% / runner +6.09%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **26%** (continue à baisser 59%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.34%** (au-delà de la MAE q10 -8.34%), cible rebond +2.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-4.82% .. +9.01%] · haut q95 +9.74% · bas q05 -7.68%
   - 60min (n=143) : retour [-5.94% .. +10.54%] · haut q95 +10.66% · bas q05 -7.86%
   - 2h (n=143) : retour [-5.54% .. +10.47%] · haut q95 +11.38% · bas q05 -8.03%
   - 4h (n=143) : retour [-7.42% .. +12.73%] · haut q95 +13.79% · bas q05 -10.52%
   - 6h (n=143) : retour [-7.03% .. +15.18%] · haut q95 +20.67% · bas q05 -11.2%
   - session (n=143) : retour [-9.65% .. +21.16%] · haut q95 +23.05% · bas q05 -13.81%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 60.0  _(momentum haussier)_
- **ADX** : 22.2  _(pas de tendance nette)_
- **MACD** : hist 0.677  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 102.8%
- **ATR** : 5.21 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.016  _(neutre)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 35.0 · MA50 40.68 · MA200 23.46  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -20.4% · MA200 +38.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95116 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
