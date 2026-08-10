# SMR

**Generated** : 2026-08-10T00:29:26.663526+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.82  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $9.82 (+0.5% vs entrée) · entrée $9.77 · stop $9.56 · T1 $10.09 · R/R 1.52  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk 0.079 _(réel 5 s)_ (GBM 0.067) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.12% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 188 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 0.99 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.72–$9.82 (mid $9.77)
- Spot actuel : $9.82 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $9.56 (stop swing_plan-based (-8.2%))
- Targets : T1 $10.09 · R/R 1.52 | T2 $10.41 · R/R 3.05 | T3 $10.73 · R/R 4.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.56


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.6 | bear 73.9 | side 8.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 29 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.528% → cible +3.281% / stop −2.123%, p_fill 88%, n_eff≈35.9) : P(cible|rempli) **42%** · **EV/risk +0.079** (×p_fill ; si rempli +0.19% du capital)
  - **swing** (entrée dip −1.159% → cible +7.337% / stop −7.124%, p_fill 90%, n_eff≈35.0) : P(cible|rempli) **47%** · **EV/risk -0.033** (×p_fill ; si rempli -0.26% du capital)
  - **deep** (entrée dip −1.695% → cible +29.774% / stop −14.887%, p_fill 88%, n_eff≈34.2) : P(cible|rempli) **1%** · **EV/risk -0.247** (×p_fill ; si rempli -4.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→65% · +3.0%→60% · +5.0%→40% · +8.0%→15%
- Range intraday médian 7.65% (p90 12.61%) · excursion haute méd. +3.55% / basse méd. −3.15%
- Profil de vol intra : ouverture 4.937% vs midi 1.507% vs clôture 1.875% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. 0.421% ; recovery-V 45%
- **σ réalisé intraday** 4.905% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 64% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 9.8475 (VA 9.7342–9.9769 ; dernier close 9.83)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 49% · rebond 78% · **stop −5.8%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.46% · baisse 56% (gap-down >1% 39% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.01%) · haut méd +1.14% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.38% (p90 −3.51%) · haut méd +1.65% · range méd 3.66%
- Excursion ouverture 30min (n=160) : bas méd −1.76% (p90 −4.55%) · haut méd +2.25% · range méd 4.32%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.57%) · haut méd +2.89% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.83 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 81% (130/159) · gap 49% · délai 0.0min · rebond 68% (82/130) (MFE +2.09%)
   - −1.0% : fill 30min 66% · séance 78% (125/159) · gap 39% · délai 0.0min · rebond 72% (85/125) (MFE +2.25%)
   - −1.5% : fill 30min 61% · séance 74% (118/159) · gap 35% · délai 0.0min · rebond 77% (89/118) (MFE +2.35%)
   - −2.0% : fill 30min 55% · séance 66% (110/159) · gap 27% · délai 0.2min · rebond 72% (81/110) (MFE +2.52%)
   - −3.0% : fill 30min 44% · séance 56% (97/159) · gap 10% · délai 2.4min · rebond 76% (79/97) (MFE +2.9%)
   - −4.0% : fill 30min 33% · séance 49% (84/159) · gap 6% · délai 9.1min · rebond 78% (66/84) (MFE +2.67%)
   - −5.0% : fill 30min 23% · séance 38% (62/159) · gap 3% · délai 19.7min · rebond 71% (45/62) (MFE +2.16%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.7%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.73%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.13% (p90 −3.32%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1188 jambes) : jambe baissière méd −1.37% (p90 −3.22%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 72% (57/83)
      · −2.0% : fill 95% (79/83) · rebond 77% (61/79)
      · −3.0% : fill 82% (73/83) · rebond 78% (61/73)
      · −4.0% : fill 74% (66/83) · rebond 82% (55/66)
      · −5.0% : fill 56% (47/83) · rebond 74% (36/47)
   - **flat** (12 séances) :
      · −1.0% : fill 80% (9/12) · rebond 52% (5/9)
      · −2.0% : fill 68% (7/12) · rebond 20% (3/7)
      · −3.0% : fill 67% (6/12) · rebond 46% (3/6)
      · −4.0% : fill 67% (6/12) · rebond 56% (3/6)
      · −5.0% : fill 56% (5/12) · rebond 79% (4/5)
   - **gap-up** (64 séances) :
      · −1.0% : fill 49% (33/64) · rebond 78% (23/33)
      · −2.0% : fill 30% (24/64) · rebond 71% (17/24)
      · −3.0% : fill 20% (18/64) · rebond 80% (15/18)
      · −4.0% : fill 14% (12/64) · rebond 67% (8/12)
      · −5.0% : fill 10% (10/64) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (74 cas) · 33% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 87% si début vert vs 12% si rouge (base 49% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **87%** · continue >prix actuel 48% ; creux résiduel méd -2.02% (q20 -3.56%) → **SL/trailing à −3.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.81% / q75 +3.15% → **scale +1.81% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **12%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.61%** (au-delà de la MAE q10 -4.61%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +4.91%] · haut q95 +6.35% · bas q05 -5.79%
   - 60min (n=160) : retour [-6.06% .. +5.68%] · haut q95 +6.82% · bas q05 -7.32%
   - 2h (n=160) : retour [-7.34% .. +6.22%] · haut q95 +9.73% · bas q05 -8.12%
   - 4h (n=160) : retour [-7.44% .. +7.53%] · haut q95 +10.78% · bas q05 -9.57%
   - 6h (n=160) : retour [-7.44% .. +8.76%] · haut q95 +11.16% · bas q05 -9.6%
   - session (n=160) : retour [-7.56% .. +9.59%] · haut q95 +11.32% · bas q05 -10.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.01%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 0.255  _(pas de croisement recent)_
- **BB** : %B 0.99 · largeur 29.4%
- **ATR** : 0.69 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.059  _(accumulation)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 8.57 · MA50 9.76 · MA200 15.49  _(prix > MA20)_
- **Dist MA** : MA20 +14.5% · MA50 +0.6% · MA200 -36.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87956 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
