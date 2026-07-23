# RGTI

**Generated** : 2026-07-23T00:25:12.587920+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $15.23  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $15.23 (+1.1% vs entrée) · entrée $15.07 · stop $14.69 · T1 $15.45 · R/R 1.0  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.025 _(réel 5 s)_ (GBM 0.093) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.99–$15.14 (mid $15.07)
- Spot actuel : $15.23 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $14.69 (stop swing_plan-based (-5.15%))
- Targets : T1 $15.45 · R/R 1.0 | T2 $15.83 · R/R 2.0 | T3 $16.22 · R/R 3.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.69


## Edge, scénarios & sizing

- EV/risk : 0.093 | EV/share : $0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.1 | side 75.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.077% → cible +2.552% / stop −2.5%, p_fill 85%, n_eff≈35.8) : P(cible|rempli) **46%** · **EV/risk -0.025** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −2.365% → cible +5.705% / stop −2.852%, p_fill 80%, n_eff≈31.3) : P(cible|rempli) **16%** · **EV/risk -0.409** (×p_fill ; si rempli -1.45% du capital)
  - **deep** (entrée dip −3.664% → cible +8.068% / stop −4.034%, p_fill 83%, n_eff≈31.0) : P(cible|rempli) **28%** · **EV/risk -0.160** (×p_fill ; si rempli -0.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→71% · +3.0%→55% · +5.0%→38% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.44% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.321% vs midi 1.667% vs clôture 1.882% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.0)_ ; drift intra méd. -0.406% ; recovery-V 38%
- **σ réalisé intraday** 4.914% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 57% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 15.2875 (VA 15.1634–15.3407 ; dernier close 15.285)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 74% · **stop −7.08%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.5% · baisse 56% (gap-down >1% 44% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.87%) · haut méd +1.11% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.53% (p90 −4.18%) · haut méd +1.54% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −5.51%) · haut méd +1.91% · range méd 4.57%
- Excursion ouverture 60min (n=160) : bas méd −2.08% (p90 −6.42%) · haut méd +2.22% · range méd 5.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.285 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (135/159) · gap 50% · délai 0.0min · rebond 65% (88/135) (MFE +2.32%)
   - −1.0% : fill 30min 69% · séance 81% (131/159) · gap 44% · délai 0.0min · rebond 65% (85/131) (MFE +2.04%)
   - −1.5% : fill 30min 64% · séance 75% (123/159) · gap 39% · délai 0.0min · rebond 64% (81/123) (MFE +2.28%)
   - −2.0% : fill 30min 60% · séance 70% (115/159) · gap 30% · délai 0.0min · rebond 63% (75/115) (MFE +2.44%)
   - −3.0% : fill 30min 52% · séance 62% (98/159) · gap 12% · délai 1.2min · rebond 74% (71/98) (MFE +2.56%)
   - −4.0% : fill 30min 39% · séance 48% (78/159) · gap 4% · délai 4.8min · rebond 74% (56/78) (MFE +2.34%)
   - −5.0% : fill 30min 23% · séance 41% (65/159) · gap 1% · délai 21.7min · rebond 68% (48/65) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.82%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.23% (p90 −3.96%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.29% (p90 −4.18%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.32% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 62% (50/82)
      · −2.0% : fill 91% (78/83) · rebond 64% (53/78)
      · −3.0% : fill 84% (70/83) · rebond 70% (50/70)
      · −4.0% : fill 67% (56/83) · rebond 71% (40/56)
      · −5.0% : fill 57% (48/83) · rebond 67% (37/48)
   - **flat** (14 séances) :
      · −1.0% : fill 89% (12/14) · rebond 88% (10/12)
      · −2.0% : fill 63% (10/14) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/14) · rebond 87% (3/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 55% (37/62) · rebond 64% (25/37)
      · −2.0% : fill 43% (27/62) · rebond 62% (15/27)
      · −3.0% : fill 35% (23/62) · rebond 87% (18/23)
      · −4.0% : fill 22% (17/62) · rebond 82% (13/17)
      · −5.0% : fill 18% (12/62) · rebond 66% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 63% si les 15 1res min sont vertes (80 cas) · 36% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 89% si début vert vs 16% si rouge (base 50% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **89%** · continue >prix actuel 57% ; creux résiduel méd -2.08% (q20 -3.24%) → **SL/trailing à −3.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.75% / q75 +4.34% → **scale +2.75% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.71%** (au-delà de la MAE q10 -5.71%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.35% .. +4.71%] · haut q95 +7.21% · bas q05 -6.61%
   - 60min (n=160) : retour [-6.05% .. +6.81%] · haut q95 +8.5% · bas q05 -7.07%
   - 2h (n=160) : retour [-7.41% .. +7.78%] · haut q95 +9.2% · bas q05 -8.2%
   - 4h (n=160) : retour [-8.09% .. +6.36%] · haut q95 +9.2% · bas q05 -9.61%
   - 6h (n=160) : retour [-8.44% .. +7.97%] · haut q95 +9.53% · bas q05 -10.3%
   - session (n=160) : retour [-7.73% .. +8.94%] · haut q95 +10.63% · bas q05 -10.34%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.65%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.0  _(survente)_
- **ADX** : 29.0  _(tendance etablie)_
- **MACD** : hist -0.114  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 43.3%
- **ATR** : 1.13 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.241  _(distribution)_
- **Vol ratio** : 1.35  _(volume normal)_
- **Choppiness** : 34.9  _(marche directionnel)_
- **MA** : MA20 16.82 · MA50 19.66 · MA200 23.03  _(prix < MA20)_
- **Dist MA** : MA20 -9.4% · MA50 -22.5% · MA200 -33.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83461 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
