# SOFI

**Generated** : 2026-07-09T00:27:13.864329+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $17.73  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $17.73 (+6.0% vs entrée) · entrée $16.72 · stop $16.44 · T1 $17.28 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.137 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 156 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.61–$16.83 (mid $16.72)
- Spot actuel : $17.73 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : $16.44 (stop swing_plan-based (-7.29%))
- Targets : T1 $17.28 · R/R 2.0 | T2 $17.84 · R/R 4.0 | T3 $18.40 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.44


## Edge, scénarios & sizing

- EV/risk : -0.137 | EV/share : $-0.039 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.9 | bear 24.2 | side 47.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 390.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.584% → cible +1.499% / stop −4.0%, p_fill 45%, n_eff≈17.0) : P(cible|rempli) **52%** · **EV/risk +0.045** (×p_fill ; si rempli +0.40% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.39% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.994% vs midi 0.946% vs clôture 1.013% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr 0.007)_ ; drift intra méd. -0.101% ; recovery-V 25%
- **σ réalisé intraday** 3.197% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 55% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 18.129 (VA 17.921–18.181 ; dernier close 17.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 50% · rebond 72% · **stop −3.25%** sous le fill (sous le bruit) · cible +2.11% · R/R 0.65 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 49% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.84%) · haut méd +0.71% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.17%) · haut méd +0.98% · range méd 2.36%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.2%) · haut méd +1.2% · range méd 2.85%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.63%) · haut méd +1.45% · range méd 3.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 78% (124/159) · gap 31% · délai 0.0min · rebond 60% (69/124) (MFE +1.34%)
   - −1.0% : fill 30min 50% · séance 69% (112/159) · gap 24% · délai 0.5min · rebond 65% (71/112) (MFE +1.42%)
   - −1.5% : fill 30min 43% · séance 63% (101/159) · gap 18% · délai 6.0min · rebond 66% (64/101) (MFE +1.83%)
   - −2.0% : fill 30min 35% · séance 50% (75/159) · gap 10% · délai 3.3min · rebond 72% (51/75) (MFE +2.11%)
   - −3.0% : fill 30min 19% · séance 33% (54/159) · gap 3% · délai 12.3min · rebond 70% (38/54) (MFE +1.63%)
   - −4.0% : fill 30min 8% · séance 22% (37/159) · gap 2% · délai 47.4min · rebond 64% (23/37) (MFE +1.84%)
   - −5.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 58.5min · rebond 47% (10/20) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.77%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.71%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.71%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=665 jambes) : jambe baissière méd −1.11% (p90 −2.77%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 96% (65/67) · rebond 68% (41/65)
      · −2.0% : fill 79% (51/67) · rebond 72% (37/51)
      · −3.0% : fill 59% (40/67) · rebond 74% (29/40)
      · −4.0% : fill 40% (27/67) · rebond 65% (19/27)
      · −5.0% : fill 22% (14/67) · rebond 47% (8/14)
   - **flat** (25 séances) :
      · −1.0% : fill 64% (17/25) · rebond 33% (10/17)
      · −2.0% : fill 42% (10/25) · rebond 39% (5/10)
      · −3.0% : fill 32% (7/25) · rebond 34% (4/7)
      · −4.0% : fill 22% (4/25) · rebond 64% (1/4)
      · −5.0% : fill 3% (2/25) · rebond 0% (0/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 44% (30/67) · rebond 73% (20/30)
      · −2.0% : fill 25% (14/67) · rebond 87% (9/14)
      · −3.0% : fill 8% (7/67) · rebond 84% (5/7)
      · −4.0% : fill 4% (6/67) · rebond 62% (3/6)
      · −5.0% : fill 3% (4/67) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 53% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 70% si début vert vs 21% si rouge (base 43% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -1.74% (q20 -3.93%) → **SL/trailing à −3.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +2.5% → **scale +1.7% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 55%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.74%** (au-delà de la MAE q10 -3.74%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.87% .. +3.64%] · haut q95 +4.01% · bas q05 -3.48%
   - 60min (n=160) : retour [-3.21% .. +3.64%] · haut q95 +4.43% · bas q05 -4.04%
   - 2h (n=160) : retour [-3.85% .. +3.79%] · haut q95 +4.99% · bas q05 -5.07%
   - 4h (n=160) : retour [-3.84% .. +4.61%] · haut q95 +5.68% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +3.86%] · haut q95 +5.71% · bas q05 -5.25%
   - session (n=160) : retour [-4.18% .. +4.96%] · haut q95 +5.71% · bas q05 -5.5%


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

- **RSI** : 50.2  _(neutre)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 0.023  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 16.2%
- **ATR** : 0.95 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.054  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 63.7  _(marche en range (choppy))_
- **MA** : MA20 17.48 · MA50 16.84 · MA200 22.19  _(prix > MA20)_
- **Dist MA** : MA20 +1.5% · MA50 +5.3% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87025 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
