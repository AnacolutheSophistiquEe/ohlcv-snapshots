# 012450

**Generated** : 2026-08-13T21:54:50.794378+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1181000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1181000.00 (+5.2% vs entrée) · entrée ₩1122109.60 · stop ₩1032340.83 · T1 ₩1153827.60 · R/R 0.35  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.03 _(réel 5 s)_ (GBM -0.125) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 173 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.1 < 20 (tendance pas encore confirmée) alors que Choppiness 34.7 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 0.96 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1115766.00–₩1128453.20 (mid ₩1122109.60)
- Spot actuel : ₩1181000.00 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1032340.83 (stop swing_plan-based (-17.47%))
- Targets : T1 ₩1153827.60 · R/R 0.35 | T2 ₩1185545.61 · R/R 0.71 | T3 ₩1217263.61 · R/R 1.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1032340.83


## Edge, scénarios & sizing

- EV/risk : -0.125 | EV/share : ₩-11216.485 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 18 % | T3 18 %
- Kelly (position) : f* 0.101 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 58.4 | bear 6.5 | side 35.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.989% → cible +2.827% / stop −8.0%, p_fill 31%, n_eff≈14.5) : P(cible|rempli) **19%** · **EV/risk -0.030** (×p_fill ; si rempli -0.77% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→46% · +3.0%→29% · +5.0%→18% · +8.0%→4%
- Range intraday médian 6.12% (p90 9.34%) · excursion haute méd. +1.91% / basse méd. −2.81%
- Profil de vol intra : ouverture 4.413% vs midi 1.239% vs clôture 1.245% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (156 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 81% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -0.327% ; recovery-V 37%
- **σ réalisé intraday** 4.621% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 46% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1084000.0 (VA 1079200.0–1108000.0 ; dernier close 1097000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 80% · **stop −5.31%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.42 (high win-rate)
- Gaps overnight (n=155) : méd. 0.64% · baisse 32% (gap-down >1% 17% · >2% 8%)
- Excursion ouverture 5min (n=156) : bas méd −1.69% (p90 −4.06%) · haut méd +0.97% · range méd 3.05%
- Excursion ouverture 15min (n=156) : bas méd −1.98% (p90 −4.9%) · haut méd +1.28% · range méd 3.64%
- Excursion ouverture 30min (n=156) : bas méd −2.13% (p90 −5.36%) · haut méd +1.39% · range méd 4.12%
- Excursion ouverture 60min (n=156) : bas méd −2.15% (p90 −5.71%) · haut méd +1.57% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1097000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 70% (110/155) · gap 20% · délai 0.1min · rebond 51% (56/110) (MFE +1.06%)
   - −1.0% : fill 30min 54% · séance 66% (105/155) · gap 17% · délai 0.9min · rebond 53% (61/105) (MFE +1.01%)
   - −1.5% : fill 30min 50% · séance 60% (97/155) · gap 11% · délai 1.3min · rebond 60% (56/97) (MFE +1.26%)
   - −2.0% : fill 30min 42% · séance 53% (80/155) · gap 8% · délai 3.5min · rebond 66% (50/80) (MFE +1.58%)
   - −3.0% : fill 30min 30% · séance 42% (59/155) · gap 2% · délai 4.4min · rebond 72% (41/59) (MFE +1.77%)
   - −4.0% : fill 30min 19% · séance 33% (45/155) · gap 2% · délai 14.9min · rebond 77% (36/45) (MFE +1.98%)
   - −5.0% : fill 30min 12% · séance 25% (33/155) · gap 1% · délai 26.0min · rebond 80% (27/33) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.15%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.69%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.81% (p90 −2.69%) → stop au-delà de −2.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=760 jambes) : jambe baissière méd −1.2% (p90 −3.2%) · ~11.6 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (35 séances) :
      · −1.0% : fill 86% (33/35) · rebond 40% (14/33)
      · −2.0% : fill 80% (30/35) · rebond 67% (18/30)
      · −3.0% : fill 77% (27/35) · rebond 75% (19/27)
      · −4.0% : fill 66% (24/35) · rebond 89% (20/24)
      · −5.0% : fill 43% (16/35) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (100 séances) :
      · −1.0% : fill 51% (53/100) · rebond 64% (37/53)
      · −2.0% : fill 37% (35/100) · rebond 74% (25/35)
      · −3.0% : fill 26% (23/100) · rebond 87% (19/23)
      · −4.0% : fill 15% (12/100) · rebond 80% (11/12)
      · −5.0% : fill 11% (9/100) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=156) : 42% en base · 74% si les 15 1res min sont vertes (55 cas) · 18% si rouges (101 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=156) : COUDE à **35min** → P(séance verte=clôture>ouverture) 85% si début vert vs 10% si rouge (base 42% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=55) : tient le vert **85%** · continue >prix actuel 53% ; creux résiduel méd -1.63% (q20 -3.3%) → **SL/trailing à −3.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.78% / q75 +4.07% → **scale +2.78% / runner +4.07%**, sortie à la clôture
  - **si ROUGE au coude** (n=101) : edge inversé — récupère vert seulement **10%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.9%** (au-delà de la MAE q10 -5.9%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=156) : retour [-5.15% .. +4.04%] · haut q95 +5.65% · bas q05 -6.28%
   - 60min (n=156) : retour [-5.28% .. +4.86%] · haut q95 +6.99% · bas q05 -6.44%
   - 2h (n=156) : retour [-7.05% .. +6.2%] · haut q95 +7.56% · bas q05 -8.53%
   - 4h (n=156) : retour [-7.43% .. +6.04%] · haut q95 +7.99% · bas q05 -9.16%
   - 6h (n=156) : retour [-6.83% .. +6.53%] · haut q95 +8.54% · bas q05 -9.49%
   - session (n=156) : retour [-7.0% .. +6.66%] · haut q95 +8.54% · bas q05 -9.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 65.6  _(momentum haussier)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist 35019.405  _(pas de croisement recent)_
- **BB** : %B 0.96 · largeur 45.0%
- **ATR** : 76785.71 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.015  _(neutre)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 34.7  _(marche directionnel)_
- **MA** : MA20 978950.0 · MA50 1027820.0 · MA200 1143740.04  _(prix > MA20)_
- **Dist MA** : MA20 +20.6% · MA50 +14.9% · MA200 +3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85341 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
