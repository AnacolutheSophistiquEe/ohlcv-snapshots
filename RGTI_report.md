# RGTI

**Generated** : 2026-07-20T00:27:15.806124+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $14.11  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $14.11 (+2.9% vs entrée) · entrée $13.71 · stop $13.29 · T1 $14.57 · R/R 2.05  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.328 _(réel 5 s)_ (GBM 0.158) · ¼-Kelly 0.036 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.13% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -32 % hors [0,100] (R² max 0.44). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $13.65–$13.78 (mid $13.71)
- Spot actuel : $14.11 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $13.29 (stop swing_plan-based (-8.75%))
- Targets : T1 $14.57 · R/R 2.05 | T2 $14.65 · R/R 2.24 | T3 $14.73 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $13.29


## Edge, scénarios & sizing

- EV/risk : 0.158 | EV/share : $0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.144 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 45.1 | side 49.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.795% → cible +6.265% / stop −3.132%, p_fill 54%, n_eff≈22.0) : P(cible|rempli) **6%** · **EV/risk -0.328** (×p_fill ; si rempli -1.91% du capital)
  - **swing** (entrée dip −6.157% → cible +5.493% / stop −2.763%, p_fill 56%, n_eff≈20.6) : P(cible|rempli) **43%** · **EV/risk +0.104** (×p_fill ; si rempli +0.51% du capital)
  - **deep** (entrée dip −9.515% → cible +7.768% / stop −3.884%, p_fill 45%, n_eff≈17.5) : P(cible|rempli) **18%** · **EV/risk -0.213** (×p_fill ; si rempli -1.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→70% · +3.0%→55% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.21% (p90 13.36%) · excursion haute méd. +3.44% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.336% vs midi 1.701% vs clôture 1.892% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr 0.013)_ ; drift intra méd. -0.597% ; recovery-V 41%
- **σ réalisé intraday** 5.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 58% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 14.1885 (VA 13.9275–14.5365 ; dernier close 14.115)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 65% · rebond 74% · **stop −7.07%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.58% · baisse 58% (gap-down >1% 46% · >2% 31%)
- Excursion ouverture 5min (n=160) : bas méd −1.28% (p90 −2.9%) · haut méd +1.04% · range méd 2.6%
- Excursion ouverture 15min (n=160) : bas méd −1.56% (p90 −4.26%) · haut méd +1.48% · range méd 3.65%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −5.83%) · haut méd +1.8% · range méd 4.68%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.5%) · haut méd +2.17% · range méd 5.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.115 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 86% (137/159) · gap 52% · délai 0.0min · rebond 65% (89/137) (MFE +2.32%)
   - −1.0% : fill 30min 72% · séance 84% (133/159) · gap 46% · délai 0.0min · rebond 65% (86/133) (MFE +2.03%)
   - −1.5% : fill 30min 66% · séance 78% (125/159) · gap 41% · délai 0.0min · rebond 64% (82/125) (MFE +2.27%)
   - −2.0% : fill 30min 62% · séance 73% (117/159) · gap 31% · délai 0.0min · rebond 63% (76/117) (MFE +2.44%)
   - −3.0% : fill 30min 54% · séance 65% (100/159) · gap 13% · délai 1.2min · rebond 74% (73/100) (MFE +2.56%)
   - −4.0% : fill 30min 40% · séance 50% (80/159) · gap 4% · délai 4.8min · rebond 74% (58/80) (MFE +2.34%)
   - −5.0% : fill 30min 24% · séance 42% (67/159) · gap 1% · délai 21.7min · rebond 68% (50/67) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.77% (p90 −2.88%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.3% (p90 −4.04%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.31% (p90 −4.22%) → stop au-delà de −2.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.34% (p90 −3.35%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 98% (84/85) · rebond 62% (51/84)
      · −2.0% : fill 91% (80/85) · rebond 64% (54/80)
      · −3.0% : fill 84% (72/85) · rebond 70% (52/72)
      · −4.0% : fill 67% (58/85) · rebond 72% (42/58)
      · −5.0% : fill 57% (50/85) · rebond 67% (39/50)
   - **flat** (14 séances) :
      · −1.0% : fill 89% (12/14) · rebond 88% (10/12)
      · −2.0% : fill 63% (10/14) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/14) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 61% (37/60) · rebond 64% (25/37)
      · −2.0% : fill 47% (27/60) · rebond 62% (15/27)
      · −3.0% : fill 38% (23/60) · rebond 87% (18/23)
      · −4.0% : fill 24% (17/60) · rebond 82% (13/17)
      · −5.0% : fill 20% (12/60) · rebond 66% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 64% si les 15 1res min sont vertes (78 cas) · 36% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 89% si début vert vs 17% si rouge (base 50% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 177min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **89%** · continue >prix actuel 56% ; creux résiduel méd -2.12% (q20 -3.44%) → **SL/trailing à −3.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.83% / q75 +4.43% → **scale +2.83% / runner +4.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.73%** (au-delà de la MAE q10 -5.73%), cible rebond +1.78% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.4% .. +4.79%] · haut q95 +7.38% · bas q05 -6.69%
   - 60min (n=160) : retour [-6.07% .. +7.02%] · haut q95 +8.8% · bas q05 -7.11%
   - 2h (n=160) : retour [-7.5% .. +7.88%] · haut q95 +9.22% · bas q05 -8.2%
   - 4h (n=160) : retour [-8.25% .. +6.38%] · haut q95 +9.22% · bas q05 -9.87%
   - 6h (n=160) : retour [-8.45% .. +8.11%] · haut q95 +9.53% · bas q05 -10.35%
   - session (n=160) : retour [-7.79% .. +9.23%] · haut q95 +10.67% · bas q05 -10.38%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.65%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.0  _(survente)_
- **ADX** : 26.4  _(tendance etablie)_
- **MACD** : hist -0.372  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 50.1%
- **ATR** : 1.22 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.168  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 17.78 · MA50 19.92 · MA200 23.28  _(prix < MA20)_
- **Dist MA** : MA20 -20.6% · MA50 -29.2% · MA200 -39.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82856 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
