# EVT

**Generated** : 2026-08-19T00:04:41.734223+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.34  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.34 (+1.2% vs entrée) · entrée €3.30 · stop €3.25 · T1 €3.38 · R/R 1.6  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk 0.053 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.360 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.29–€3.31 (mid €3.30)
- Spot actuel : €3.34 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €3.25 (stop swing_plan-based (-7.44%))
- Targets : T1 €3.38 · R/R 1.6 | T2 €3.42 · R/R 2.4 | T3 €3.45 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.25


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : €-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 15 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 38.9 | bear 6.0 | side 55.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.26% → cible +2.362% / stop −1.499%, p_fill 62%, n_eff≈25.0) : P(cible|rempli) **22%** · **EV/risk +0.053** (×p_fill ; si rempli +0.13% du capital)
  - **swing** (entrée dip −2.763% → cible +3.411% / stop −4.81%, p_fill 32%, n_eff≈16.8) : P(cible|rempli) **60%** · **EV/risk +0.024** (×p_fill ; si rempli +0.36% du capital)
  - **deep** (entrée dip −4.275% → cible +4.82% / stop −7.329%, p_fill 37%, n_eff≈18.2) : P(cible|rempli) **31%** · **EV/risk -0.129** (×p_fill ; si rempli -2.54% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→72% · +2.0%→46% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.57%) · excursion haute méd. +1.77% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.684% vs midi 1.23% vs clôture 1.2% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.084 ; mean-reverting — autocorr -0.134)_ ; drift intra méd. -0.53% ; recovery-V 30%
- **σ réalisé intraday** 3.24% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 70% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 3.5171 (VA 3.4587–3.5547 ; dernier close 3.434)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 68% · rebond 70% · **stop −3.2%** sous le fill (sous le bruit) · cible +1.65% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 41% (gap-down >1% 17% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.29%) · haut méd +0.68% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.73%) · haut méd +0.86% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −2.81%) · haut méd +0.98% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −3.16%) · haut méd +1.09% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.434 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 81% (131/159) · gap 25% · délai 0.3min · rebond 70% (87/131) (MFE +1.57%)
   - −1.0% : fill 30min 46% · séance 68% (114/159) · gap 17% · délai 1.2min · rebond 70% (73/114) (MFE +1.65%)
   - −1.5% : fill 30min 33% · séance 53% (94/159) · gap 12% · délai 9.1min · rebond 62% (59/94) (MFE +1.5%)
   - −2.0% : fill 30min 22% · séance 43% (78/159) · gap 8% · délai 23.6min · rebond 58% (49/78) (MFE +1.32%)
   - −3.0% : fill 30min 12% · séance 29% (55/159) · gap 4% · délai 51.4min · rebond 66% (40/55) (MFE +1.36%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 53.0min · rebond 60% (20/32) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 9% (18/159) · gap 1% · délai 56.0min · rebond 60% (12/18) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.13%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.7%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.32% (p90 −1.89%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=820 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 95% (55/58) · rebond 71% (32/55)
      · −2.0% : fill 64% (41/58) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/58) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/58) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/58) · rebond 57% (9/13)
   - **flat** (42 séances) :
      · −1.0% : fill 63% (29/42) · rebond 70% (22/29)
      · −2.0% : fill 45% (19/42) · rebond 59% (12/19)
      · −3.0% : fill 36% (13/42) · rebond 77% (10/13)
      · −4.0% : fill 18% (6/42) · rebond 46% (2/6)
      · −5.0% : fill 6% (3/42) · rebond 27% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 49% (30/59) · rebond 67% (19/30)
      · −2.0% : fill 24% (18/59) · rebond 56% (12/18)
      · −3.0% : fill 16% (13/59) · rebond 40% (9/13)
      · −4.0% : fill 10% (6/59) · rebond 90% (4/6)
      · −5.0% : fill 6% (2/59) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 64% si les 15 1res min sont vertes (75 cas) · 39% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 38% si rouge (base 51% · écart 28 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.43% → **scale +1.55% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **38%** (continue à baisser 49%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.7% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.36%] · haut q95 +3.45% · bas q05 -3.84%
   - 60min (n=160) : retour [-4.57% .. +2.7%] · haut q95 +3.84% · bas q05 -5.49%
   - 2h (n=160) : retour [-5.05% .. +2.91%] · haut q95 +4.08% · bas q05 -5.98%
   - 4h (n=160) : retour [-3.59% .. +3.43%] · haut q95 +4.08% · bas q05 -6.95%
   - 6h (n=160) : retour [-4.02% .. +3.59%] · haut q95 +5.21% · bas q05 -6.95%
   - session (n=160) : retour [-4.64% .. +4.58%] · haut q95 +6.75% · bas q05 -7.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 44.4  _(momentum baissier)_
- **ADX** : 32.7  _(tendance etablie)_
- **MACD** : hist 0.038  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 13.4%
- **ATR** : 0.16 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.358  _(distribution)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 3.49 · MA50 4.16 · MA200 5.09  _(prix < MA20)_
- **Dist MA** : MA20 -4.3% · MA50 -19.6% · MA200 -34.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90190 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
