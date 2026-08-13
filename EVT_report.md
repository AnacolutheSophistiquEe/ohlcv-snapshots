# EVT

**Generated** : 2026-08-13T00:03:30.006798+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.76  

> 🟡 **WAIT-FOR-DIP** — spot +4.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.76 (+4.2% vs entrée) · entrée €3.61 · stop €3.56 · T1 €3.66 · R/R 1.0  
> ↳ P(T1 av. stop) 59 % · EV/risk 0.318 · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.260 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.60–€3.62 (mid €3.61)
- Spot actuel : €3.76 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : €3.56 (stop swing_plan-based (-11.86%))
- Targets : T1 €3.66 · R/R 1.0 | T2 €3.71 · R/R 2.0 | T3 €3.75 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.56


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : €-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 26 % | T3 11 %
- Kelly (position) : f* 0.021 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.1 | bear 6.2 | side 79.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 42 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→46% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.26%) · excursion haute méd. +1.77% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.687% vs midi 1.216% vs clôture 1.209% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.076 ; mean-reverting — autocorr -0.133)_ ; drift intra méd. -0.092% ; recovery-V 30%
- **σ réalisé intraday** 3.193% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 66% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 3.7329 (VA 3.6867–3.7527 ; dernier close 3.698)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 66% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.59% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 42% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −2.32%) · haut méd +0.68% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.63%) · haut méd +0.89% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.96% (p90 −2.77%) · haut méd +1.05% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.93%) · haut méd +1.06% · range méd 2.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.698 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 80% (130/159) · gap 26% · délai 0.3min · rebond 68% (85/130) (MFE +1.49%)
   - −1.0% : fill 30min 46% · séance 66% (113/159) · gap 18% · délai 0.6min · rebond 67% (71/113) (MFE +1.59%)
   - −1.5% : fill 30min 33% · séance 52% (94/159) · gap 13% · délai 2.7min · rebond 59% (58/94) (MFE +1.31%)
   - −2.0% : fill 30min 24% · séance 42% (77/159) · gap 8% · délai 14.9min · rebond 64% (50/77) (MFE +1.43%)
   - −3.0% : fill 30min 13% · séance 27% (53/159) · gap 4% · délai 31.1min · rebond 68% (39/53) (MFE +1.65%)
   - −4.0% : fill 30min 7% · séance 15% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −2.18%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.7%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.88%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=810 jambes) : jambe baissière méd −1.05% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 95% (55/58) · rebond 71% (32/55)
      · −2.0% : fill 64% (41/58) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/58) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/58) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/58) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 61% (30/43) · rebond 67% (22/30)
      · −2.0% : fill 42% (19/43) · rebond 68% (13/19)
      · −3.0% : fill 31% (12/43) · rebond 73% (9/12)
      · −4.0% : fill 13% (5/43) · rebond 20% (1/5)
      · −5.0% : fill 7% (3/43) · rebond 27% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 43% (28/58) · rebond 59% (17/28)
      · −2.0% : fill 21% (17/58) · rebond 70% (12/17)
      · −3.0% : fill 12% (12/58) · rebond 57% (9/12)
      · −4.0% : fill 5% (5/58) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 64% si les 15 1res min sont vertes (76 cas) · 40% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 39% si rouge (base 52% · écart 27 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.43% → **scale +1.56% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **39%** (continue à baisser 46%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.41%** (au-delà de la MAE q10 -4.41%), cible rebond +2.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.44% .. +2.38%] · haut q95 +3.5% · bas q05 -3.4%
   - 60min (n=160) : retour [-2.97% .. +2.7%] · haut q95 +4.09% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.46% .. +3.03%] · haut q95 +4.17% · bas q05 -4.13%
   - 4h (n=160) : retour [-2.83% .. +3.53%] · haut q95 +4.17% · bas q05 -4.26%
   - 6h (n=160) : retour [-3.28% .. +3.64%] · haut q95 +5.34% · bas q05 -4.93%
   - session (n=160) : retour [-4.1% .. +5.21%] · haut q95 +6.86% · bas q05 -5.51%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 74.9  _(surachat)_
- **ADX** : 34.8  _(tendance etablie)_
- **MACD** : hist 0.079  _(pas de croisement recent)_
- **BB** : %B 1.17 · largeur 10.8%
- **ATR** : 0.12 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.265  _(distribution)_
- **Vol ratio** : 0.23  _(volume atone)_
- **Choppiness** : 56.0  _(transition)_
- **MA** : MA20 3.51 · MA50 4.31 · MA200 5.18  _(prix > MA20)_
- **Dist MA** : MA20 +7.3% · MA50 -12.7% · MA200 -27.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89356 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
