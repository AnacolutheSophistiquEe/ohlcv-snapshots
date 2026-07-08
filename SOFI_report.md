# SOFI

**Generated** : 2026-07-08T00:24:02.554205+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $17.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $17.75 (+6.1% vs entrée) · entrée $16.73 · stop $16.44 · T1 $17.30 · R/R 1.97  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.146 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 142 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.62–$16.85 (mid $16.73)
- Spot actuel : $17.75 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : $16.44 (stop swing_plan-based (-7.38%))
- Targets : T1 $17.30 · R/R 1.97 | T2 $17.87 · R/R 3.93 | T3 $18.45 · R/R 5.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.44


## Edge, scénarios & sizing

- EV/risk : -0.146 | EV/share : $-0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 17 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 29.6 | bear 24.1 | side 46.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 390.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.614% → cible +1.528% / stop −4.0%, p_fill 42%, n_eff≈16.3) : P(cible|rempli) **59%** · **EV/risk +0.075** (×p_fill ; si rempli +0.71% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→70% · +2.0%→49% · +3.0%→36% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.39% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.993% vs midi 0.95% vs clôture 1.02% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓1% ; spike-down 65% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; neutre — autocorr 0.023)_ ; drift intra méd. 0.114% ; recovery-V 26%
- **σ réalisé intraday** 3.21% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 18.7446 (VA 18.5136–18.8986 ; dernier close 18.61)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 74% · **stop −3.33%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 48% (gap-down >1% 25% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.88%) · haut méd +0.68% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −3.17%) · haut méd +1.01% · range méd 2.4%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.2%) · haut méd +1.24% · range méd 2.81%
- Excursion ouverture 60min (n=160) : bas méd −1.41% (p90 −3.39%) · haut méd +1.46% · range méd 3.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.61 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 77% (123/159) · gap 32% · délai 0.0min · rebond 59% (68/123) (MFE +1.38%)
   - −1.0% : fill 30min 50% · séance 68% (111/159) · gap 25% · délai 0.4min · rebond 67% (71/111) (MFE +1.44%)
   - −1.5% : fill 30min 42% · séance 63% (100/159) · gap 18% · délai 1.7min · rebond 68% (64/100) (MFE +1.88%)
   - −2.0% : fill 30min 34% · séance 49% (74/159) · gap 10% · délai 2.7min · rebond 74% (51/74) (MFE +2.19%)
   - −3.0% : fill 30min 19% · séance 32% (53/159) · gap 3% · délai 11.1min · rebond 74% (38/53) (MFE +1.86%)
   - −4.0% : fill 30min 9% · séance 20% (36/159) · gap 2% · délai 55.6min · rebond 61% (22/36) (MFE +1.4%)
   - −5.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 58.5min · rebond 47% (10/20) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.77%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.71%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.71%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=666 jambes) : jambe baissière méd −1.11% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 96% (65/67) · rebond 68% (41/65)
      · −2.0% : fill 79% (51/67) · rebond 72% (37/51)
      · −3.0% : fill 59% (40/67) · rebond 74% (29/40)
      · −4.0% : fill 40% (27/67) · rebond 65% (19/27)
      · −5.0% : fill 22% (14/67) · rebond 47% (8/14)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 44% (30/68) · rebond 73% (20/30)
      · −2.0% : fill 25% (14/68) · rebond 87% (9/14)
      · −3.0% : fill 8% (7/68) · rebond 84% (5/7)
      · −4.0% : fill 4% (6/68) · rebond 62% (3/6)
      · −5.0% : fill 3% (4/68) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 53% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 70% si début vert vs 22% si rouge (base 44% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -1.74% (q20 -3.93%) → **SL/trailing à −3.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +2.5% → **scale +1.7% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **22%** (continue à baisser 53%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.74%** (au-delà de la MAE q10 -3.74%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.89% .. +3.65%] · haut q95 +4.01% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.21% .. +3.66%] · haut q95 +4.45% · bas q05 -4.04%
   - 2h (n=160) : retour [-3.85% .. +3.8%] · haut q95 +5.02% · bas q05 -5.08%
   - 4h (n=160) : retour [-3.85% .. +4.61%] · haut q95 +5.68% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.14% .. +3.87%] · haut q95 +5.71% · bas q05 -5.3%
   - session (n=160) : retour [-4.01% .. +5.11%] · haut q95 +5.71% · bas q05 -5.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.7  _(momentum haussier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 0.067  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 16.9%
- **ATR** : 0.97 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 64.5  _(marche en range (choppy))_
- **MA** : MA20 17.41 · MA50 16.85 · MA200 22.24  _(prix > MA20)_
- **Dist MA** : MA20 +1.9% · MA50 +5.3% · MA200 -20.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86568 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
