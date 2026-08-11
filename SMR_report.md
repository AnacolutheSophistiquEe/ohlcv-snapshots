# SMR

**Generated** : 2026-08-11T00:30:20.450700+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.18  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $9.18 (+1.3% vs entrée) · entrée $9.06 · stop $8.10 · T1 $10.97 · R/R 1.99  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.018 _(réel 5 s)_ (GBM -0.096) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 120 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $8.93–$9.18 (mid $9.06)
- Spot actuel : $9.18 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $8.10 (stop swing_plan-based (-11.77%))
- Targets : T1 $10.97 · R/R 1.99 | T2 $11.00 · R/R 2.02 | T3 $11.02 · R/R 2.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.10


## Edge, scénarios & sizing

- EV/risk : -0.096 | EV/share : $-0.092 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.2 | bear 14.2 | side 58.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 31 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.607% → cible +5.924% / stop −2.961%, p_fill 88%, n_eff≈35.9) : P(cible|rempli) **25%** · **EV/risk +0.204** (×p_fill ; si rempli +0.69% du capital)
  - **swing** (entrée dip −1.334% → cible +21.153% / stop −10.577%, p_fill 85%, n_eff≈34.5) : P(cible|rempli) **10%** · **EV/risk -0.018** (×p_fill ; si rempli -0.22% du capital)
  - **deep** (entrée dip −1.964% → cible +10.233% / stop −11.41%, p_fill 88%, n_eff≈34.2) : P(cible|rempli) **39%** · **EV/risk -0.241** (×p_fill ; si rempli -3.15% du capital)
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
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 54.1  _(neutre)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist 0.217  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 29.8%
- **ATR** : 0.68 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.075  _(accumulation)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 8.61 · MA50 9.7 · MA200 15.35  _(prix > MA20)_
- **Dist MA** : MA20 +6.6% · MA50 -5.4% · MA200 -40.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85971 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
