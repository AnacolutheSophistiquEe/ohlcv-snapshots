# 012450

**Generated** : 2026-08-07T00:17:54.475046+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1054000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1054000.00 (+2.9% vs entrée) · entrée ₩1024275.98 · stop ₩942333.90 · T1 ₩1056374.61 · R/R 0.39  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.067 _(réel 5 s)_ (GBM -0.153) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 1.05 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1017856.26–₩1030695.71 (mid ₩1024275.98)
- Spot actuel : ₩1054000.00 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : ₩942333.90 (stop swing_plan-based (-13.08%))
- Targets : T1 ₩1056374.61 · R/R 0.39 | T2 ₩1088473.23 · R/R 0.78 | T3 ₩1120571.86 · R/R 1.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩942333.90


## Edge, scénarios & sizing

- EV/risk : -0.153 | EV/share : ₩-12522.505 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 15 % | T3 15 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.0 | bear 14.1 | side 33.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.815% → cible +3.134% / stop −8.0%, p_fill 44%, n_eff≈25.0) : P(cible|rempli) **25%** · **EV/risk -0.067** (×p_fill ; si rempli -1.22% du capital)
  - **swing** (entrée dip −6.209% → cible +7.007% / stop −7.326%, p_fill 53%, n_eff≈20.6) : P(cible|rempli) **42%** · **EV/risk -0.055** (×p_fill ; si rempli -0.76% du capital)
  - **deep** (entrée dip −9.593% → cible +9.91% / stop −11.401%, p_fill 34%, n_eff≈16.8) : P(cible|rempli) **38%** · **EV/risk -0.071** (×p_fill ; si rempli -2.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→42% · +3.0%→25% · +5.0%→15% · +8.0%→4%
- Range intraday médian 5.99% (p90 9.34%) · excursion haute méd. +1.85% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.311% vs midi 1.209% vs clôture 1.203% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 85% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.657% ; recovery-V 39%
- **σ réalisé intraday** 4.676% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 50% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 1005800.0 (VA 1003400.0–1009000.0 ; dernier close 1011000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 34% · rebond 82% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.4 (high win-rate)
- Gaps overnight (n=151) : méd. 0.63% · baisse 31% (gap-down >1% 18% · >2% 9%)
- Excursion ouverture 5min (n=152) : bas méd −1.75% (p90 −4.05%) · haut méd +0.87% · range méd 2.91%
- Excursion ouverture 15min (n=152) : bas méd −2.04% (p90 −4.64%) · haut méd +1.15% · range méd 3.44%
- Excursion ouverture 30min (n=152) : bas méd −2.15% (p90 −4.99%) · haut méd +1.28% · range méd 4.04%
- Excursion ouverture 60min (n=152) : bas méd −2.21% (p90 −5.44%) · haut méd +1.47% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1011000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (108/151) · gap 21% · délai 0.1min · rebond 51% (55/108) (MFE +1.06%)
   - −1.0% : fill 30min 56% · séance 69% (104/151) · gap 18% · délai 0.8min · rebond 55% (61/104) (MFE +1.01%)
   - −1.5% : fill 30min 52% · séance 63% (96/151) · gap 12% · délai 1.3min · rebond 62% (56/96) (MFE +1.36%)
   - −2.0% : fill 30min 43% · séance 55% (79/151) · gap 9% · délai 3.1min · rebond 65% (49/79) (MFE +1.6%)
   - −3.0% : fill 30min 30% · séance 44% (58/151) · gap 2% · délai 3.4min · rebond 71% (40/58) (MFE +1.58%)
   - −4.0% : fill 30min 21% · séance 34% (44/151) · gap 2% · délai 9.6min · rebond 82% (36/44) (MFE +2.07%)
   - −5.0% : fill 30min 13% · séance 24% (32/151) · gap 1% · délai 8.7min · rebond 79% (26/32) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.18%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.82% (p90 −2.69%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.51% (p90 −2.69%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=736 jambes) : jambe baissière méd −1.23% (p90 −3.22%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 100% (33/33) · rebond 40% (14/33)
      · −2.0% : fill 94% (30/33) · rebond 67% (18/30)
      · −3.0% : fill 90% (27/33) · rebond 75% (19/27)
      · −4.0% : fill 77% (24/33) · rebond 89% (20/24)
      · −5.0% : fill 50% (16/33) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (98 séances) :
      · −1.0% : fill 52% (52/98) · rebond 68% (37/52)
      · −2.0% : fill 36% (34/98) · rebond 72% (24/34)
      · −3.0% : fill 24% (22/98) · rebond 86% (18/22)
      · −4.0% : fill 13% (11/98) · rebond 100% (11/11)
      · −5.0% : fill 8% (8/98) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 39% en base · 70% si les 15 1res min sont vertes (52 cas) · 19% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **35min** → P(séance verte=clôture>ouverture) 83% si début vert vs 10% si rouge (base 39% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=52) : tient le vert **83%** · continue >prix actuel 51% ; creux résiduel méd -2.02% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.75% / q75 +3.76% → **scale +2.75% / runner +3.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **10%** (continue à baisser 50%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.94%** (au-delà de la MAE q10 -5.94%), cible rebond +1.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-5.28% .. +4.46%] · haut q95 +5.77% · bas q05 -6.3%
   - 60min (n=152) : retour [-5.29% .. +5.19%] · haut q95 +7.07% · bas q05 -6.72%
   - 2h (n=152) : retour [-7.35% .. +6.23%] · haut q95 +7.83% · bas q05 -8.24%
   - 4h (n=152) : retour [-7.09% .. +6.16%] · haut q95 +8.24% · bas q05 -8.82%
   - 6h (n=152) : retour [-6.84% .. +6.55%] · haut q95 +8.63% · bas q05 -9.9%
   - session (n=152) : retour [-7.2% .. +6.8%] · haut q95 +8.63% · bas q05 -9.9%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.2  _(momentum haussier)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist 23353.908  _(pas de croisement recent)_
- **BB** : %B 1.05 · largeur 25.0%
- **ATR** : 72428.57 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.126  _(distribution)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 927600.0 · MA50 1030640.0 · MA200 1138774.79  _(prix > MA20)_
- **Dist MA** : MA20 +13.6% · MA50 +2.3% · MA200 -7.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84592 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
