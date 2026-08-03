# PLTR

**Generated** : 2026-08-03T00:22:27.248250+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $123.06  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-03 — PLTR earnings (J-0 sess · earnings)  
> ↳ spot $123.06 (+3.5% vs entrée) · entrée $118.89 · stop $115.92 · T1 $120.83 · R/R 0.65  
> ↳ P(T1 av. stop) 60 % · EV/risk 0.022 · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.50–$119.28 (mid $118.89)
- Spot actuel : $123.06 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $115.92 (stop swing_plan-based (-12.81%))
- Targets : T1 $120.83 · R/R 0.65 | T2 $122.77 · R/R 1.31 | T3 $124.71 · R/R 1.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.92


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : $0.069 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 20 % | T3 7 %
- Kelly (position) : f* 0.076 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.2 | bear 11.1 | side 75.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.395% → cible +1.631% / stop −2.5%, p_fill 24%, n_eff≈10.2) : P(cible|rempli) **34%** · **EV/risk -0.043** (×p_fill ; si rempli -0.45% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→48% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.89% (p90 6.93%) · excursion haute méd. +1.9% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.978% vs midi 0.729% vs clôture 0.854% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 55% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.009)_ ; drift intra méd. 0.141% ; recovery-V 32%
- **σ réalisé intraday** 2.753% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 50% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 122.5012 (VA 121.8538–123.2412 ; dernier close 123.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 51% · **stop −3.07%** sous le fill (sous le bruit) · cible +1.01% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 58% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.1%) · haut méd +0.93% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −1.04% (p90 −3.02%) · haut méd +1.14% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.55%) · haut méd +1.18% · range méd 2.76%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.02%) · haut méd +1.35% · range méd 3.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 123.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (120/159) · gap 41% · délai 0.0min · rebond 55% (66/120) (MFE +1.07%)
   - −1.0% : fill 30min 60% · séance 68% (109/159) · gap 31% · délai 0.0min · rebond 60% (63/109) (MFE +1.3%)
   - −1.5% : fill 30min 49% · séance 60% (94/159) · gap 25% · délai 0.1min · rebond 69% (59/94) (MFE +1.57%)
   - −2.0% : fill 30min 43% · séance 53% (79/159) · gap 16% · délai 1.3min · rebond 63% (49/79) (MFE +1.57%)
   - −3.0% : fill 30min 23% · séance 35% (55/159) · gap 9% · délai 5.2min · rebond 50% (25/55) (MFE +0.99%)
   - −4.0% : fill 30min 18% · séance 25% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 11% · séance 20% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.02%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.14%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.38%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=545 jambes) : jambe baissière méd −1.04% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 92% (67/72) · rebond 61% (40/67)
      · −2.0% : fill 79% (56/72) · rebond 62% (36/56)
      · −3.0% : fill 56% (39/72) · rebond 47% (18/39)
      · −4.0% : fill 44% (30/72) · rebond 51% (14/30)
      · −5.0% : fill 36% (23/72) · rebond 58% (12/23)
   - **flat** (29 séances) :
      · −1.0% : fill 81% (24/29) · rebond 44% (12/24)
      · −2.0% : fill 62% (13/29) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/29) · rebond 57% (5/10)
      · −4.0% : fill 25% (7/29) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/29) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 32% (18/58) · rebond 72% (11/18)
      · −2.0% : fill 17% (10/58) · rebond 69% (5/10)
      · −3.0% : fill 7% (6/58) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/58) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/58) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 68% si les 15 1res min sont vertes (79 cas) · 35% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 76% si début vert vs 28% si rouge (base 52% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.55% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.58% → **scale +1.42% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 44%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.23%** (au-delà de la MAE q10 -3.23%), cible rebond +1.53% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.03% .. +3.47%] · haut q95 +3.8% · bas q05 -4.25%
   - 60min (n=160) : retour [-3.89% .. +3.66%] · haut q95 +4.5% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.11% .. +4.48%] · haut q95 +4.76% · bas q05 -4.8%
   - 4h (n=160) : retour [-4.46% .. +5.02%] · haut q95 +5.63% · bas q05 -5.86%
   - 6h (n=160) : retour [-5.06% .. +4.72%] · haut q95 +5.77% · bas q05 -6.31%
   - session (n=160) : retour [-4.98% .. +4.54%] · haut q95 +5.77% · bas q05 -6.31%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-0 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-0 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-0 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist -0.692  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 14.8%
- **ATR** : 6.58 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.2  _(accumulation)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 59.8  _(transition)_
- **MA** : MA20 129.05 · MA50 130.72 · MA200 152.89  _(prix < MA20)_
- **Dist MA** : MA20 -4.6% · MA50 -5.9% · MA200 -19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88301 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
