# SOFI

**Generated** : 2026-07-10T00:34:01.099229+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $18.62  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $18.62 (+3.8% vs entrée) · entrée $17.94 · stop $16.68 · T1 $18.75 · R/R 0.64  
> ↳ P(T1 av. stop) 15 % · EV/risk -0.003 · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −7.0% cohérent avec le bruit 5 s (EV-optimal ≈ −7.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 628 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.88–$18.00 (mid $17.94)
- Spot actuel : $18.62 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $16.68 (stop swing_plan-based (-9.68%))
- Targets : T1 $18.75 · R/R 0.64 | T2 $18.77 · R/R 0.66 | T3 $18.80 · R/R 0.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.68


## Edge, scénarios & sizing

- EV/risk : -0.003 | EV/share : $-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 14 % | T3 12 %
- Kelly (position) : f* 0.121 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.4 | bear 14.9 | side 55.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 279.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.656% → cible +4.505% / stop −7.0%, p_fill 24%, n_eff≈8.2) : P(cible|rempli) **7%** · **EV/risk +0.034** (×p_fill ; si rempli +0.97% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→69% · +2.0%→48% · +3.0%→34% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.964% vs midi 0.948% vs clôture 1.013% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 65% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.012% ; recovery-V 29%
- **σ réalisé intraday** 3.176% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 57% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 17.4569 (VA 17.3061–17.6244 ; dernier close 17.74)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 73% · **stop −3.18%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 26% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.8%) · haut méd +0.72% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −3.17%) · haut méd +1.01% · range méd 2.34%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.2%) · haut méd +1.25% · range méd 2.82%
- Excursion ouverture 60min (n=160) : bas méd −1.41% (p90 −3.58%) · haut méd +1.46% · range méd 3.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 78% (124/159) · gap 33% · délai 0.0min · rebond 58% (68/124) (MFE +1.31%)
   - −1.0% : fill 30min 51% · séance 70% (113/159) · gap 26% · délai 0.4min · rebond 66% (72/113) (MFE +1.39%)
   - −1.5% : fill 30min 44% · séance 64% (102/159) · gap 19% · délai 1.7min · rebond 67% (65/102) (MFE +1.81%)
   - −2.0% : fill 30min 37% · séance 51% (76/159) · gap 12% · délai 2.7min · rebond 73% (52/76) (MFE +2.1%)
   - −3.0% : fill 30min 18% · séance 34% (55/159) · gap 3% · délai 17.4min · rebond 72% (39/55) (MFE +1.86%)
   - −4.0% : fill 30min 8% · séance 21% (37/159) · gap 2% · délai 47.4min · rebond 64% (23/37) (MFE +1.84%)
   - −5.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 58.5min · rebond 47% (10/20) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.75%) → stop au-delà de −1.43% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.71%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.71%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=669 jambes) : jambe baissière méd −1.08% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 96% (66/68) · rebond 69% (42/66)
      · −2.0% : fill 80% (52/68) · rebond 74% (38/52)
      · −3.0% : fill 61% (41/68) · rebond 76% (30/41)
      · −4.0% : fill 38% (27/68) · rebond 65% (19/27)
      · −5.0% : fill 21% (14/68) · rebond 47% (8/14)
   - **flat** (25 séances) :
      · −1.0% : fill 64% (17/25) · rebond 33% (10/17)
      · −2.0% : fill 42% (10/25) · rebond 39% (5/10)
      · −3.0% : fill 32% (7/25) · rebond 34% (4/7)
      · −4.0% : fill 22% (4/25) · rebond 64% (1/4)
      · −5.0% : fill 3% (2/25) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 44% (30/66) · rebond 73% (20/30)
      · −2.0% : fill 25% (14/66) · rebond 87% (9/14)
      · −3.0% : fill 8% (7/66) · rebond 84% (5/7)
      · −4.0% : fill 4% (6/66) · rebond 62% (3/6)
      · −5.0% : fill 3% (4/66) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 55% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 71% si début vert vs 21% si rouge (base 44% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **71%** · continue >prix actuel 45% ; creux résiduel méd -1.99% (q20 -3.9%) → **SL/trailing à −3.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.79% / q75 +2.47% → **scale +1.79% / runner +2.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **21%** (continue à baisser 55%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.74%** (au-delà de la MAE q10 -3.74%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.85% .. +3.63%] · haut q95 +4.01% · bas q05 -3.47%
   - 60min (n=160) : retour [-3.21% .. +3.61%] · haut q95 +4.4% · bas q05 -4.04%
   - 2h (n=160) : retour [-3.85% .. +3.78%] · haut q95 +4.97% · bas q05 -5.06%
   - 4h (n=160) : retour [-3.83% .. +4.6%] · haut q95 +5.68% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +3.86%] · haut q95 +5.71% · bas q05 -5.21%
   - session (n=160) : retour [-4.15% .. +4.92%] · haut q95 +5.71% · bas q05 -5.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.9  _(momentum haussier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 0.048  _(pas de croisement recent)_
- **BB** : %B 0.87 · largeur 16.1%
- **ATR** : 0.92 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.02  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 62.4  _(marche en range (choppy))_
- **MA** : MA20 17.58 · MA50 16.84 · MA200 22.13  _(prix > MA20)_
- **Dist MA** : MA20 +5.9% · MA50 +10.6% · MA200 -15.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85820 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
