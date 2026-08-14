# SMR

**Generated** : 2026-08-14T00:29:36.013693+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.85  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $9.85 (+0.5% vs entrée) · entrée $9.80 · stop $9.58 · T1 $10.10 · R/R 1.36  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk 0.106 _(réel 5 s)_ (GBM 0.071) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.17% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 228 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.74–$9.85 (mid $9.80)
- Spot actuel : $9.85 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $9.58 (stop swing_plan-based (-8.4%))
- Targets : T1 $10.10 · R/R 1.36 | T2 $10.40 · R/R 2.73 | T3 $10.71 · R/R 4.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.58


## Edge, scénarios & sizing

- EV/risk : 0.071 | EV/share : $0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 33 % | T3 33 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.5 | bear 8.7 | side 63.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 286.0 (= 29 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.542% → cible +3.102% / stop −2.17%, p_fill 89%, n_eff≈36.0) : P(cible|rempli) **46%** · **EV/risk +0.106** (×p_fill ; si rempli +0.26% du capital)
  - **swing** (entrée dip −1.206% → cible +6.936% / stop −7.282%, p_fill 86%, n_eff≈34.9) : P(cible|rempli) **50%** · **EV/risk -0.017** (×p_fill ; si rempli -0.14% du capital)
  - **deep** (entrée dip −1.769% → cible +9.81% / stop −10.985%, p_fill 89%, n_eff≈34.5) : P(cible|rempli) **41%** · **EV/risk -0.226** (×p_fill ; si rempli -2.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→60% · +5.0%→40% · +8.0%→15%
- Range intraday médian 7.65% (p90 12.61%) · excursion haute méd. +3.55% / basse méd. −3.15%
- Profil de vol intra : ouverture 4.951% vs midi 1.5% vs clôture 1.86% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. 0.392% ; recovery-V 46%
- **σ réalisé intraday** 4.821% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 9.6103 (VA 9.5147–9.6677 ; dernier close 9.92)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 49% · rebond 79% · **stop −5.56%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 56% (gap-down >1% 38% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −2.94%) · haut méd +1.15% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.38% (p90 −3.74%) · haut méd +1.65% · range méd 3.66%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.69%) · haut méd +2.25% · range méd 4.43%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.78%) · haut méd +2.62% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (129/159) · gap 48% · délai 0.0min · rebond 67% (81/129) (MFE +2.04%)
   - −1.0% : fill 30min 65% · séance 76% (124/159) · gap 38% · délai 0.0min · rebond 70% (84/124) (MFE +2.23%)
   - −1.5% : fill 30min 61% · séance 73% (117/159) · gap 34% · délai 0.0min · rebond 75% (87/117) (MFE +2.31%)
   - −2.0% : fill 30min 55% · séance 66% (109/159) · gap 26% · délai 0.3min · rebond 70% (79/109) (MFE +2.44%)
   - −3.0% : fill 30min 44% · séance 55% (97/159) · gap 10% · délai 3.1min · rebond 73% (78/97) (MFE +2.59%)
   - −4.0% : fill 30min 34% · séance 49% (85/159) · gap 6% · délai 9.2min · rebond 79% (67/85) (MFE +2.56%)
   - −5.0% : fill 30min 24% · séance 38% (63/159) · gap 2% · délai 19.5min · rebond 72% (46/63) (MFE +2.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −2.69%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.72%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.31%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1190 jambes) : jambe baissière méd −1.36% (p90 −3.21%) · ~14.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 70% (57/84)
      · −2.0% : fill 95% (80/84) · rebond 74% (61/80)
      · −3.0% : fill 83% (74/84) · rebond 75% (61/74)
      · −4.0% : fill 75% (67/84) · rebond 83% (56/67)
      · −5.0% : fill 58% (48/84) · rebond 76% (37/48)
   - **flat** (11 séances) :
      · −1.0% : fill 79% (8/11) · rebond 54% (5/8)
      · −2.0% : fill 68% (6/11) · rebond 18% (2/6)
      · −3.0% : fill 68% (6/11) · rebond 46% (3/6)
      · −4.0% : fill 68% (6/11) · rebond 56% (3/6)
      · −5.0% : fill 57% (5/11) · rebond 79% (4/5)
   - **gap-up** (64 séances) :
      · −1.0% : fill 46% (32/64) · rebond 78% (22/32)
      · −2.0% : fill 28% (23/64) · rebond 71% (16/23)
      · −3.0% : fill 18% (17/64) · rebond 80% (14/17)
      · −4.0% : fill 14% (12/64) · rebond 67% (8/12)
      · −5.0% : fill 10% (10/64) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 64% si les 15 1res min sont vertes (73 cas) · 35% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 87% si début vert vs 11% si rouge (base 49% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **87%** · continue >prix actuel 50% ; creux résiduel méd -1.86% (q20 -3.54%) → **SL/trailing à −3.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.83% / q75 +3.39% → **scale +1.83% / runner +3.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **11%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.41% .. +4.91%] · haut q95 +6.25% · bas q05 -5.94%
   - 60min (n=160) : retour [-5.89% .. +5.68%] · haut q95 +6.79% · bas q05 -7.14%
   - 2h (n=160) : retour [-7.04% .. +5.92%] · haut q95 +9.67% · bas q05 -8.08%
   - 4h (n=160) : retour [-7.38% .. +7.49%] · haut q95 +10.39% · bas q05 -9.48%
   - 6h (n=160) : retour [-7.4% .. +8.76%] · haut q95 +11.09% · bas q05 -9.59%
   - session (n=160) : retour [-7.47% .. +9.48%] · haut q95 +11.28% · bas q05 -10.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.0%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 64.4  _(momentum haussier)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist 0.201  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 32.5%
- **ATR** : 0.71 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.132  _(accumulation)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 8.85 · MA50 9.5 · MA200 14.95  _(prix > MA20)_
- **Dist MA** : MA20 +11.3% · MA50 +3.7% · MA200 -34.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85634 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
