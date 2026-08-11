# 207940

**Generated** : 2026-08-11T21:55:26.823585+00:00  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1614000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩1614000.00 (+0.9% vs entrée) · entrée ₩1600285.69 · stop ₩1472262.83 · T1 ₩1629690.71 · R/R 0.23  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM -0.058) · ¼-Kelly 0.062 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1062 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 70.5 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1594404.68–₩1606166.69 (mid ₩1600285.69)
- Spot actuel : ₩1614000.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩1472262.83 (stop swing_plan-based (-6.56%))
- Targets : T1 ₩1629690.71 · R/R 0.23 | T2 ₩1659095.73 · R/R 0.46 | T3 ₩1688500.75 · R/R 0.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1472262.83


## Edge, scénarios & sizing

- EV/risk : -0.058 | EV/share : ₩-7416.534 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 12 % | T3 6 %
- Kelly (position) : f* 0.249 | ¼-Kelly 0.062 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 42.8 | bear 10.9 | side 46.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.848% → cible +1.837% / stop −8.0%, p_fill 88%, n_eff≈36.7) : P(cible|rempli) **51%** · **EV/risk +0.009** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −1.869% → cible +4.109% / stop −4.78%, p_fill 78%, n_eff≈30.6) : P(cible|rempli) **59%** · **EV/risk +0.095** (×p_fill ; si rempli +0.58% du capital)
  - **deep** (entrée dip −2.894% → cible +5.811% / stop −7.246%, p_fill 71%, n_eff≈29.3) : P(cible|rempli) **71%** · **EV/risk +0.300** (×p_fill ; si rempli +3.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→54% · +2.0%→39% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.08% (p90 6.65%) · excursion haute méd. +1.08% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.56% vs midi 0.746% vs clôture 0.843% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 10% · trend ↑2%/↓3% ; spike-down 57% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.03)_ ; drift intra méd. 0.073% ; recovery-V 36%
- **σ réalisé intraday** 3.226% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 49% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 1523750.0 (VA 1502750.0–1531250.0 ; dernier close 1551000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 68% · **stop −2.28%** sous le fill (sous le bruit) · cible +1.74% · R/R 0.76 (high win-rate)
- Gaps overnight (n=149) : méd. 0.35% · baisse 32% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=150) : bas méd −0.87% (p90 −2.57%) · haut méd +0.5% · range méd 1.52%
- Excursion ouverture 15min (n=150) : bas méd −1.08% (p90 −2.97%) · haut méd +0.62% · range méd 2.1%
- Excursion ouverture 30min (n=150) : bas méd −1.25% (p90 −3.37%) · haut méd +0.74% · range méd 2.45%
- Excursion ouverture 60min (n=150) : bas méd −1.29% (p90 −3.57%) · haut méd +0.86% · range méd 2.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1551000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 76% (102/149) · gap 19% · délai 1.1min · rebond 56% (47/102) (MFE +1.15%)
   - −1.0% : fill 30min 46% · séance 60% (80/149) · gap 7% · délai 1.9min · rebond 56% (36/80) (MFE +1.28%)
   - −1.5% : fill 30min 39% · séance 50% (63/149) · gap 4% · délai 3.3min · rebond 56% (30/63) (MFE +1.51%)
   - −2.0% : fill 30min 29% · séance 41% (54/149) · gap 3% · délai 6.3min · rebond 67% (30/54) (MFE +1.42%)
   - −3.0% : fill 30min 11% · séance 27% (34/149) · gap 2% · délai 62.4min · rebond 62% (19/34) (MFE +1.4%)
   - −4.0% : fill 30min 4% · séance 16% (18/149) · gap 2% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 8% (10/149) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.33%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.07%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.18%) → stop au-delà de −1.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=383 jambes) : jambe baissière méd −1.12% (p90 −2.76%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (35 séances) :
      · −1.0% : fill 98% (34/35) · rebond 69% (18/34)
      · −2.0% : fill 84% (29/35) · rebond 68% (15/29)
      · −3.0% : fill 43% (15/35) · rebond 54% (8/15)
      · −4.0% : fill 31% (9/35) · rebond 76% (5/9)
      · −5.0% : fill 14% (5/35) · rebond 100% (5/5)
   - **flat** (43 séances) :
      · −1.0% : fill 59% (23/43) · rebond 31% (7/23)
      · −2.0% : fill 34% (10/43) · rebond 57% (5/10)
      · −3.0% : fill 26% (7/43) · rebond 97% (6/7)
      · −4.0% : fill 14% (4/43) · rebond 100% (4/4)
      · −5.0% : fill 6% (2/43) · rebond 89% (1/2)
   - **gap-up** (71 séances) :
      · −1.0% : fill 41% (23/71) · rebond 58% (11/23)
      · −2.0% : fill 24% (15/71) · rebond 72% (10/15)
      · −3.0% : fill 20% (12/71) · rebond 49% (5/12)
      · −4.0% : fill 9% (5/71) · rebond 33% (2/5)
      · −5.0% : fill 6% (3/71) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 42% en base · 70% si les 15 1res min sont vertes (52 cas) · 26% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **33min** → P(séance verte=clôture>ouverture) 77% si début vert vs 21% si rouge (base 42% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=55) : tient le vert **77%** · continue >prix actuel 43% ; creux résiduel méd -1.34% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.44% / q75 +2.42% → **scale +1.44% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **21%** (continue à baisser 52%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.45%** (au-delà de la MAE q10 -3.45%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-3.22% .. +3.43%] · haut q95 +3.79% · bas q05 -3.6%
   - 60min (n=150) : retour [-3.54% .. +2.78%] · haut q95 +4.22% · bas q05 -4.18%
   - 2h (n=150) : retour [-4.15% .. +3.45%] · haut q95 +4.72% · bas q05 -4.72%
   - 4h (n=150) : retour [-5.05% .. +3.94%] · haut q95 +5.1% · bas q05 -5.81%
   - 6h (n=150) : retour [-4.91% .. +4.11%] · haut q95 +5.38% · bas q05 -6.11%
   - session (n=150) : retour [-4.73% .. +3.73%] · haut q95 +5.38% · bas q05 -6.11%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 70.5  _(surachat)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist 12037.319  _(pas de croisement recent)_
- **BB** : %B 0.95 · largeur 21.9%
- **ATR** : 75714.29 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.236  _(accumulation)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 1469200.0 · MA50 1402580.0 · MA200 1607019.8  _(prix > MA20)_
- **Dist MA** : MA20 +9.9% · MA50 +15.1% · MA200 +0.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83596 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
