# 005930

**Generated** : 2026-07-15T00:14:57.694902+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩263000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩263000.00 (+0.9% vs entrée) · entrée ₩260540.90 · stop ₩250314.71 · T1 ₩280993.27 · R/R 2.0  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.084 _(réel 5 s)_ (GBM 0.587) · ¼-Kelly 0.027 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -56 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩258081.79–₩263000.00 (mid ₩260540.90)
- Spot actuel : ₩263000.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩250314.71 (stop swing_plan-based (-4.82%))
- Targets : T1 ₩280993.27 · R/R 2.0 | T2 ₩301445.64 · R/R 4.0 | T3 ₩321898.01 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩250314.71


## Edge, scénarios & sizing

- EV/risk : 0.587 | EV/share : ₩5997.852 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.108 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.4 | bear 31.0 | side 58.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.502% → cible +3.511% / stop −3.124%, p_fill 85%, n_eff≈32.8) : P(cible|rempli) **27%** · **EV/risk -0.182** (×p_fill ; si rempli -0.67% du capital)
  - **swing** (entrée dip −0.932% → cible +7.85% / stop −3.925%, p_fill 84%, n_eff≈32.8) : P(cible|rempli) **31%** · **EV/risk -0.084** (×p_fill ; si rempli -0.39% du capital)
  - **deep** (entrée dip −1.27% → cible +11.102% / stop −5.551%, p_fill 83%, n_eff≈32.3) : P(cible|rempli) **27%** · **EV/risk -0.221** (×p_fill ; si rempli -1.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→70% · +2.0%→48% · +3.0%→31% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.38% (p90 9.32%) · excursion haute méd. +1.96% / basse méd. −2.22%
- Profil de vol intra : ouverture 2.646% vs midi 1.121% vs clôture 1.334% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (129 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓2% ; spike-down 62% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. -0.51% ; recovery-V 19%
- **σ réalisé intraday** 4.317% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 73% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 262237.5 (VA 256487.5–266262.5 ; dernier close 263800.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 74% · **stop −6.56%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.26 (high win-rate)
- Gaps overnight (n=128) : méd. 0.0% · baisse 47% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=129) : bas méd −0.48% (p90 −1.34%) · haut méd +0.72% · range méd 1.35%
- Excursion ouverture 15min (n=129) : bas méd −0.85% (p90 −2.35%) · haut méd +1.12% · range méd 2.06%
- Excursion ouverture 30min (n=129) : bas méd −1.03% (p90 −2.77%) · haut méd +1.22% · range méd 2.41%
- Excursion ouverture 60min (n=129) : bas méd −1.27% (p90 −3.39%) · haut méd +1.4% · range méd 3.0%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 263800.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 66% (78/128) · gap 39% · délai 0.0min · rebond 55% (42/78) (MFE +1.49%)
   - −1.0% : fill 30min 49% · séance 63% (73/128) · gap 36% · délai 0.0min · rebond 60% (42/73) (MFE +1.33%)
   - −1.5% : fill 30min 46% · séance 57% (65/128) · gap 26% · délai 0.3min · rebond 60% (39/65) (MFE +1.66%)
   - −2.0% : fill 30min 42% · séance 53% (59/128) · gap 25% · délai 0.5min · rebond 60% (35/59) (MFE +1.86%)
   - −3.0% : fill 30min 31% · séance 47% (50/128) · gap 19% · délai 2.3min · rebond 65% (34/50) (MFE +2.41%)
   - −4.0% : fill 30min 21% · séance 38% (39/128) · gap 12% · délai 25.8min · rebond 68% (28/39) (MFE +2.42%)
   - −5.0% : fill 30min 11% · séance 30% (29/128) · gap 6% · délai 83.9min · rebond 74% (21/29) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.96%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −2.65%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −2.36%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=547 jambes) : jambe baissière méd −1.29% (p90 −3.17%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 97% (53/55) · rebond 52% (28/53)
      · −2.0% : fill 88% (46/55) · rebond 48% (24/46)
      · −3.0% : fill 84% (41/55) · rebond 59% (27/41)
      · −4.0% : fill 72% (33/55) · rebond 63% (23/33)
      · −5.0% : fill 59% (25/55) · rebond 70% (17/25)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (60 séances) :
      · −1.0% : fill 31% (13/60) · rebond 81% (10/13)
      · −2.0% : fill 22% (9/60) · rebond 94% (8/9)
      · −3.0% : fill 11% (5/60) · rebond 89% (4/5)
      · −4.0% : fill 11% (4/60) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/60) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=129) : 44% en base · 63% si les 15 1res min sont vertes (66 cas) · 22% si rouges (63 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=129) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 80% si début vert vs 10% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **80%** · continue >prix actuel 54% ; creux résiduel méd -1.39% (q20 -4.38%) → **SL/trailing à −4.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.82% → **scale +1.72% / runner +3.82%**, sortie à la clôture
  - **si ROUGE au coude** (n=58) : edge inversé — récupère vert seulement **10%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.27%** (au-delà de la MAE q10 -7.27%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=129) : retour [-2.42% .. +2.86%] · haut q95 +3.7% · bas q05 -3.1%
   - 60min (n=129) : retour [-2.76% .. +4.9%] · haut q95 +5.49% · bas q05 -3.8%
   - 2h (n=129) : retour [-4.74% .. +4.85%] · haut q95 +6.27% · bas q05 -5.13%
   - 4h (n=129) : retour [-5.36% .. +5.58%] · haut q95 +6.88% · bas q05 -7.72%
   - 6h (n=129) : retour [-6.78% .. +6.44%] · haut q95 +8.05% · bas q05 -8.26%
   - session (n=129) : retour [-6.27% .. +7.22%] · haut q95 +8.05% · bas q05 -9.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.71%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 33.3  _(momentum baissier)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist -8852.255  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 42.3%
- **ATR** : 27250.0 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.047  _(neutre)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 315200.0 · MA50 304730.0 · MA200 182922.34  _(prix < MA20)_
- **Dist MA** : MA20 -16.6% · MA50 -13.7% · MA200 +43.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82570 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
