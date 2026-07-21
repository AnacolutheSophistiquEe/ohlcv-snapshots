# RGTI

**Generated** : 2026-07-21T22:04:04.969517+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $15.28  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $15.28 (+1.2% vs entrée) · entrée $15.10 · stop $14.73 · T1 $15.49 · R/R 1.05  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.029 _(réel 5 s)_ (GBM 0.096) · ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.03–$15.18 (mid $15.10)
- Spot actuel : $15.28 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $14.73 (stop swing_plan-based (-5.32%))
- Targets : T1 $15.49 · R/R 1.05 | T2 $15.87 · R/R 2.08 | T3 $16.26 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.73


## Edge, scénarios & sizing

- EV/risk : 0.096 | EV/share : $0.036 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.066 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 22.0 | side 73.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.16% → cible +2.55% / stop −2.499%, p_fill 88%, n_eff≈35.6) : P(cible|rempli) **46%** · **EV/risk -0.029** (×p_fill ; si rempli -0.08% du capital)
  - **swing** (entrée dip −2.541% → cible +5.703% / stop −2.851%, p_fill 76%, n_eff≈29.7) : P(cible|rempli) **13%** · **EV/risk -0.451** (×p_fill ; si rempli -1.69% du capital)
  - **deep** (entrée dip −3.926% → cible +8.065% / stop −4.033%, p_fill 82%, n_eff≈30.7) : P(cible|rempli) **29%** · **EV/risk -0.126** (×p_fill ; si rempli -0.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→71% · +3.0%→55% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.21% (p90 13.36%) · excursion haute méd. +3.44% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.311% vs midi 1.694% vs clôture 1.883% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr 0.009)_ ; drift intra méd. -0.597% ; recovery-V 39%
- **σ réalisé intraday** 4.981% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 60% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 14.3763 (VA 14.2548–14.4437 ; dernier close 14.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 64% · rebond 74% · **stop −7.07%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.54% · baisse 57% (gap-down >1% 45% · >2% 31%)
- Excursion ouverture 5min (n=160) : bas méd −1.25% (p90 −2.89%) · haut méd +1.07% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.53% (p90 −4.22%) · haut méd +1.49% · range méd 3.55%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −5.67%) · haut méd +1.88% · range méd 4.63%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −6.47%) · haut méd +2.19% · range méd 5.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 85% (136/159) · gap 51% · délai 0.0min · rebond 65% (88/136) (MFE +2.32%)
   - −1.0% : fill 30min 70% · séance 82% (132/159) · gap 45% · délai 0.0min · rebond 65% (85/132) (MFE +2.04%)
   - −1.5% : fill 30min 65% · séance 76% (124/159) · gap 40% · délai 0.0min · rebond 64% (81/124) (MFE +2.27%)
   - −2.0% : fill 30min 61% · séance 72% (116/159) · gap 31% · délai 0.0min · rebond 63% (75/116) (MFE +2.43%)
   - −3.0% : fill 30min 53% · séance 64% (99/159) · gap 13% · délai 1.2min · rebond 74% (72/99) (MFE +2.55%)
   - −4.0% : fill 30min 40% · séance 49% (79/159) · gap 4% · délai 4.7min · rebond 74% (57/79) (MFE +2.34%)
   - −5.0% : fill 30min 23% · séance 42% (66/159) · gap 1% · délai 21.8min · rebond 68% (49/66) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.77% (p90 −2.85%) → stop au-delà de −1.87% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.29% (p90 −4.03%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.31% (p90 −4.22%) → stop au-delà de −2.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1178 jambes) : jambe baissière méd −1.33% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 62% (50/83)
      · −2.0% : fill 91% (79/84) · rebond 64% (53/79)
      · −3.0% : fill 84% (71/84) · rebond 70% (51/71)
      · −4.0% : fill 67% (57/84) · rebond 72% (41/57)
      · −5.0% : fill 57% (49/84) · rebond 67% (38/49)
   - **flat** (14 séances) :
      · −1.0% : fill 89% (12/14) · rebond 88% (10/12)
      · −2.0% : fill 63% (10/14) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/14) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 58% (37/61) · rebond 64% (25/37)
      · −2.0% : fill 45% (27/61) · rebond 62% (15/27)
      · −3.0% : fill 37% (23/61) · rebond 87% (18/23)
      · −4.0% : fill 23% (17/61) · rebond 82% (13/17)
      · −5.0% : fill 19% (12/61) · rebond 66% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 62% si les 15 1res min sont vertes (79 cas) · 36% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 89% si début vert vs 16% si rouge (base 49% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **89%** · continue >prix actuel 56% ; creux résiduel méd -2.12% (q20 -3.44%) → **SL/trailing à −3.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.83% / q75 +4.43% → **scale +2.83% / runner +4.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.71%** (au-delà de la MAE q10 -5.71%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.37% .. +4.75%] · haut q95 +7.3% · bas q05 -6.65%
   - 60min (n=160) : retour [-6.06% .. +6.92%] · haut q95 +8.65% · bas q05 -7.09%
   - 2h (n=160) : retour [-7.47% .. +7.83%] · haut q95 +9.21% · bas q05 -8.2%
   - 4h (n=160) : retour [-8.17% .. +6.37%] · haut q95 +9.21% · bas q05 -9.74%
   - 6h (n=160) : retour [-8.44% .. +8.04%] · haut q95 +9.53% · bas q05 -10.33%
   - session (n=160) : retour [-7.76% .. +9.09%] · haut q95 +10.65% · bas q05 -10.36%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.65%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.1  _(survente)_
- **ADX** : 28.6  _(tendance etablie)_
- **MACD** : hist -0.21  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 47.5%
- **ATR** : 1.16 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.235  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 35.8  _(marche directionnel)_
- **MA** : MA20 17.12 · MA50 19.74 · MA200 23.13  _(prix < MA20)_
- **Dist MA** : MA20 -10.7% · MA50 -22.6% · MA200 -33.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83136 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
