# SOFI

**Generated** : 2026-07-03T22:00:18.869508+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $18.24  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $18.24 (+7.6% vs entrée) · entrée $16.95 · stop $16.64 · T1 $17.58 · R/R 2.03  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.051 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 359 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
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
- Entry (zone de repli) : $16.82–$17.08 (mid $16.95)
- Spot actuel : $18.24 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : $16.64 (stop swing_plan-based (-8.8%))
- Targets : T1 $17.58 · R/R 2.03 | T2 $18.22 · R/R 4.1 | T3 $18.85 · R/R 6.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.64


## Edge, scénarios & sizing

- EV/risk : -0.051 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 34.2 | bear 26.8 | side 39.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 383.0 (= 21 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.209% → cible +1.668% / stop −4.0%, p_fill 30%, n_eff≈10.2) : P(cible|rempli) **53%** · **EV/risk +0.069** (×p_fill ; si rempli +0.92% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.38% (p90 7.29%) · excursion haute méd. +1.89% / basse méd. −2.15%
- Profil de vol intra : ouverture 2.985% vs midi 0.947% vs clôture 1.01% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; neutre — autocorr 0.006)_ ; drift intra méd. 0.048% ; recovery-V 26%
- **σ réalisé intraday** 3.23% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 55% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 18.1049 (VA 17.9639–18.1754 ; dernier close 18.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 50% · rebond 75% · **stop −3.33%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 49% (gap-down >1% 26% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.88%) · haut méd +0.65% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.18%) · haut méd +0.99% · range méd 2.37%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.2%) · haut méd +1.2% · range méd 2.75%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.39%) · haut méd +1.45% · range méd 3.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 79% (124/159) · gap 33% · délai 0.0min · rebond 59% (69/124) (MFE +1.38%)
   - −1.0% : fill 30min 50% · séance 70% (112/159) · gap 26% · délai 0.4min · rebond 67% (72/112) (MFE +1.44%)
   - −1.5% : fill 30min 43% · séance 64% (101/159) · gap 18% · délai 1.6min · rebond 68% (65/101) (MFE +1.88%)
   - −2.0% : fill 30min 35% · séance 50% (75/159) · gap 10% · délai 2.8min · rebond 75% (52/75) (MFE +2.21%)
   - −3.0% : fill 30min 19% · séance 32% (53/159) · gap 3% · délai 11.1min · rebond 74% (38/53) (MFE +1.86%)
   - −4.0% : fill 30min 9% · séance 21% (36/159) · gap 2% · délai 55.6min · rebond 61% (22/36) (MFE +1.4%)
   - −5.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 58.5min · rebond 47% (10/20) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.8%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.71%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.71%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=665 jambes) : jambe baissière méd −1.11% (p90 −2.76%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 96% (66/68) · rebond 68% (42/66)
      · −2.0% : fill 79% (52/68) · rebond 72% (38/52)
      · −3.0% : fill 59% (40/68) · rebond 74% (29/40)
      · −4.0% : fill 40% (27/68) · rebond 65% (19/27)
      · −5.0% : fill 22% (14/68) · rebond 47% (8/14)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (30/67) · rebond 73% (20/30)
      · −2.0% : fill 26% (14/67) · rebond 87% (9/14)
      · −3.0% : fill 8% (7/67) · rebond 84% (5/7)
      · −4.0% : fill 4% (6/67) · rebond 62% (3/6)
      · −5.0% : fill 3% (4/67) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 51% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 69% si début vert vs 22% si rouge (base 43% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **69%** · continue >prix actuel 45% ; creux résiduel méd -1.98% (q20 -3.99%) → **SL/trailing à −3.99%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.54% → **scale +1.55% / runner +2.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **22%** (continue à baisser 53%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.74%** (au-delà de la MAE q10 -3.74%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.91% .. +3.66%] · haut q95 +4.01% · bas q05 -3.72%
   - 60min (n=160) : retour [-3.22% .. +3.67%] · haut q95 +4.48% · bas q05 -4.04%
   - 2h (n=160) : retour [-3.85% .. +3.82%] · haut q95 +5.06% · bas q05 -5.08%
   - 4h (n=160) : retour [-3.86% .. +4.61%] · haut q95 +5.68% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.16% .. +3.87%] · haut q95 +5.71% · bas q05 -5.34%
   - session (n=160) : retour [-4.02% .. +5.14%] · haut q95 +5.71% · bas q05 -5.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 66.1  _(momentum haussier)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist 0.114  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 17.0%
- **ATR** : 0.94 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.02  _(neutre)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 17.26 · MA50 16.87 · MA200 22.33  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 +8.1% · MA200 -18.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87638 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
