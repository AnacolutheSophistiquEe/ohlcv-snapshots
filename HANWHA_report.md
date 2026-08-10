# 012450

**Generated** : 2026-08-10T00:18:02.476483+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1097000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩1097000.00 (+3.8% vs entrée) · entrée ₩1056525.98 · stop ₩972003.90 · T1 ₩1087659.87 · R/R 0.37  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.048 _(réel 5 s)_ (GBM -0.125) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 131 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 1.09 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1050299.20–₩1062752.76 (mid ₩1056525.98)
- Spot actuel : ₩1097000.00 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : ₩972003.90 (stop swing_plan-based (-14.62%))
- Targets : T1 ₩1087659.87 · R/R 0.37 | T2 ₩1118793.76 · R/R 0.74 | T3 ₩1149927.65 · R/R 1.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩972003.90


## Edge, scénarios & sizing

- EV/risk : -0.125 | EV/share : ₩-10582.359 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 18 % | T3 18 %
- Kelly (position) : f* 0.11 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.4 | bear 7.4 | side 40.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.685% → cible +2.947% / stop −8.0%, p_fill 35%, n_eff≈20.6) : P(cible|rempli) **20%** · **EV/risk -0.048** (×p_fill ; si rempli -1.12% du capital)
  - **swing** (entrée dip −8.115% → cible +6.589% / stop −7.079%, p_fill 34%, n_eff≈13.0) : P(cible|rempli) **40%** · **EV/risk -0.065** (×p_fill ; si rempli -1.34% du capital)
  - **deep** (entrée dip −12.543% → cible +9.319% / stop −11.157%, p_fill 31%, n_eff≈10.9) : P(cible|rempli) **51%** · **EV/risk +0.007** (×p_fill ; si rempli +0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→62% · +2.0%→45% · +3.0%→28% · +5.0%→18% · +8.0%→4%
- Range intraday médian 5.99% (p90 9.34%) · excursion haute méd. +1.88% / basse méd. −2.69%
- Profil de vol intra : ouverture 4.315% vs midi 1.219% vs clôture 1.23% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (154 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 82% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.173% ; recovery-V 39%
- **σ réalisé intraday** 4.606% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 45% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1075487.5 (VA 1070187.5–1083437.5 ; dernier close 1097000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 32% · rebond 82% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.4 (high win-rate)
- Gaps overnight (n=153) : méd. 0.57% · baisse 33% (gap-down >1% 18% · >2% 9%)
- Excursion ouverture 5min (n=154) : bas méd −1.69% (p90 −4.02%) · haut méd +0.97% · range méd 2.94%
- Excursion ouverture 15min (n=154) : bas méd −1.98% (p90 −4.63%) · haut méd +1.28% · range méd 3.61%
- Excursion ouverture 30min (n=154) : bas méd −2.13% (p90 −4.92%) · haut méd +1.39% · range méd 4.04%
- Excursion ouverture 60min (n=154) : bas méd −2.15% (p90 −5.42%) · haut méd +1.57% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1097000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (109/153) · gap 20% · délai 0.1min · rebond 52% (56/109) (MFE +1.13%)
   - −1.0% : fill 30min 54% · séance 66% (104/153) · gap 18% · délai 0.8min · rebond 55% (61/104) (MFE +1.01%)
   - −1.5% : fill 30min 50% · séance 61% (96/153) · gap 11% · délai 1.3min · rebond 62% (56/96) (MFE +1.36%)
   - −2.0% : fill 30min 41% · séance 53% (79/153) · gap 9% · délai 3.1min · rebond 65% (49/79) (MFE +1.6%)
   - −3.0% : fill 30min 29% · séance 42% (58/153) · gap 2% · délai 3.4min · rebond 71% (40/58) (MFE +1.58%)
   - −4.0% : fill 30min 20% · séance 32% (44/153) · gap 2% · délai 9.6min · rebond 82% (36/44) (MFE +2.07%)
   - −5.0% : fill 30min 13% · séance 24% (32/153) · gap 1% · délai 8.7min · rebond 79% (26/32) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.16%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.78% (p90 −2.69%) → stop au-delà de −2.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.69%) → stop au-delà de −2.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=750 jambes) : jambe baissière méd −1.2% (p90 −3.17%) · ~12.0 jambes/séance
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
   - **gap-up** (98 séances) :
      · −1.0% : fill 52% (52/98) · rebond 68% (37/52)
      · −2.0% : fill 36% (34/98) · rebond 72% (24/34)
      · −3.0% : fill 24% (22/98) · rebond 86% (18/22)
      · −4.0% : fill 13% (11/98) · rebond 100% (11/11)
      · −5.0% : fill 8% (8/98) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=154) : 41% en base · 72% si les 15 1res min sont vertes (54 cas) · 19% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=154) : COUDE à **35min** → P(séance verte=clôture>ouverture) 85% si début vert vs 10% si rouge (base 41% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **85%** · continue >prix actuel 56% ; creux résiduel méd -1.83% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.84% / q75 +4.3% → **scale +2.84% / runner +4.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **10%** (continue à baisser 50%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.94%** (au-delà de la MAE q10 -5.94%), cible rebond +1.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=154) : retour [-5.22% .. +4.25%] · haut q95 +5.71% · bas q05 -6.3%
   - 60min (n=154) : retour [-5.29% .. +5.03%] · haut q95 +7.04% · bas q05 -6.59%
   - 2h (n=154) : retour [-7.2% .. +6.22%] · haut q95 +7.7% · bas q05 -8.18%
   - 4h (n=154) : retour [-6.99% .. +6.1%] · haut q95 +8.12% · bas q05 -8.72%
   - 6h (n=154) : retour [-6.83% .. +6.54%] · haut q95 +8.59% · bas q05 -9.7%
   - session (n=154) : retour [-7.06% .. +6.73%] · haut q95 +8.59% · bas q05 -9.7%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 69.3  _(momentum haussier)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist 28802.063  _(pas de croisement recent)_
- **BB** : %B 1.09 · largeur 29.6%
- **ATR** : 71357.14 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.061  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 934800.0 · MA50 1027700.0 · MA200 1139528.17  _(prix > MA20)_
- **Dist MA** : MA20 +17.4% · MA50 +6.7% · MA200 -3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85276 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
