# RGTI

**Generated** : 2026-08-14T00:26:53.835225+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.62  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $18.62 (+4.1% vs entrée) · entrée $17.88 · stop $16.22 · T1 $21.19 · R/R 1.99  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.129 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $17.62–$18.13 (mid $17.88)
- Spot actuel : $18.62 (+4.1% au-dessus de la zone — repli à attendre)
- Stop : $16.22 (stop swing_plan-based (-12.9%))
- Targets : T1 $21.19 · R/R 1.99 | T2 $21.44 · R/R 2.14 | T3 $21.69 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.22


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 15 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.1 | bear 28.1 | side 66.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 391.0 (= 21 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.816% → cible +3.052% / stop −2.5%, p_fill 60%, n_eff≈24.9) : P(cible|rempli) **40%** · **EV/risk -0.022** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −3.991% → cible +18.559% / stop −9.279%, p_fill 57%, n_eff≈25.3) : P(cible|rempli) **8%** · **EV/risk -0.129** (×p_fill ; si rempli -2.09% du capital)
  - **deep** (entrée dip −6.172% → cible +10.064% / stop −10.922%, p_fill 69%, n_eff≈27.2) : P(cible|rempli) **46%** · **EV/risk -0.065** (×p_fill ; si rempli -1.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→71% · +3.0%→55% · +5.0%→40% · +8.0%→14%
- Range intraday médian 8.01% (p90 13.36%) · excursion haute méd. +3.52% / basse méd. −2.65%
- Profil de vol intra : ouverture 5.398% vs midi 1.592% vs clôture 1.852% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.395% ; recovery-V 40%
- **σ réalisé intraday** 4.729% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 49% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 17.6822 (VA 17.6097–18.0084 ; dernier close 18.085)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 75% · **stop −6.39%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 55% (gap-down >1% 43% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.71%) · haut méd +1.19% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.47% (p90 −4.05%) · haut méd +1.76% · range méd 3.76%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −5.27%) · haut méd +2.09% · range méd 4.63%
- Excursion ouverture 60min (n=160) : bas méd −2.11% (p90 −6.04%) · haut méd +2.4% · range méd 5.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.085 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (134/159) · gap 48% · délai 0.0min · rebond 66% (88/134) (MFE +2.44%)
   - −1.0% : fill 30min 67% · séance 75% (127/159) · gap 43% · délai 0.0min · rebond 68% (84/127) (MFE +2.13%)
   - −1.5% : fill 30min 61% · séance 70% (120/159) · gap 36% · délai 0.0min · rebond 66% (80/120) (MFE +2.32%)
   - −2.0% : fill 30min 57% · séance 64% (113/159) · gap 28% · délai 0.0min · rebond 68% (77/113) (MFE +2.39%)
   - −3.0% : fill 30min 49% · séance 57% (96/159) · gap 13% · délai 1.2min · rebond 73% (70/96) (MFE +2.47%)
   - −4.0% : fill 30min 36% · séance 44% (76/159) · gap 3% · délai 5.7min · rebond 75% (56/76) (MFE +2.32%)
   - −5.0% : fill 30min 19% · séance 34% (61/159) · gap 1% · délai 21.5min · rebond 67% (46/61) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.23%) → stop au-delà de −1.67% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.04% (p90 −2.77%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −3.42%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1180 jambes) : jambe baissière méd −1.29% (p90 −3.16%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 64% (51/82)
      · −2.0% : fill 90% (78/83) · rebond 67% (53/78)
      · −3.0% : fill 84% (70/83) · rebond 68% (49/70)
      · −4.0% : fill 67% (56/83) · rebond 72% (40/56)
      · −5.0% : fill 52% (46/83) · rebond 65% (35/46)
   - **flat** (16 séances) :
      · −1.0% : fill 94% (14/16) · rebond 94% (12/14)
      · −2.0% : fill 64% (11/16) · rebond 81% (9/11)
      · −3.0% : fill 38% (6/16) · rebond 84% (4/6)
      · −4.0% : fill 38% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 24% (5/16) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (31/60) · rebond 63% (21/31)
      · −2.0% : fill 32% (24/60) · rebond 63% (15/24)
      · −3.0% : fill 26% (20/60) · rebond 89% (17/20)
      · −4.0% : fill 16% (14/60) · rebond 84% (12/14)
      · −5.0% : fill 13% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 72% si les 15 1res min sont vertes (80 cas) · 31% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 86% si début vert vs 18% si rouge (base 53% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 58% ; creux résiduel méd -2.4% (q20 -3.99%) → **SL/trailing à −3.99%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.64% / q75 +5.55% → **scale +2.64% / runner +5.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **18%** (continue à baisser 60%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +2.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.46% .. +4.97%] · haut q95 +6.61% · bas q05 -6.46%
   - 60min (n=160) : retour [-5.61% .. +6.55%] · haut q95 +6.89% · bas q05 -6.94%
   - 2h (n=160) : retour [-6.42% .. +7.41%] · haut q95 +9.18% · bas q05 -7.69%
   - 4h (n=160) : retour [-7.48% .. +7.59%] · haut q95 +9.18% · bas q05 -8.07%
   - 6h (n=160) : retour [-7.59% .. +8.43%] · haut q95 +9.54% · bas q05 -8.75%
   - session (n=160) : retour [-7.57% .. +8.78%] · haut q95 +10.28% · bas q05 -8.75%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.69% / p90 2.67%) · ~4.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 13.25 min, n=41)
   - −1.0% → **77%** (reprise méd 55.8 min, n=26)
   - −1.5% → **78%** (reprise méd 94.96 min, n=15)
   - −2.0% → **79%** (reprise méd 109.11 min, n=8)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.69%) ; extension open→close méd +7.29% (q75 +9.11% / q95 +9.99%), MFE méd +9.12% / q90 +10.34%
   - Échelle scale-out : +9.12% (33%) / +10.23% (33%) / +10.34% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **33%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.34% : P(retournement après) 0% (mèche méd 1.02%)
- **CONTEXTE** : la dernière heure tient les gains 59% du temps (retour médian dernière heure +0.5%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 69.1  _(momentum haussier)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist 0.539  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 41.3%
- **ATR** : 1.27 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.031  _(neutre)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 39.8  _(transition)_
- **MA** : MA20 15.93 · MA50 17.9 · MA200 20.73  _(prix > MA20)_
- **Dist MA** : MA20 +16.9% · MA50 +4.0% · MA200 -10.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89924 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
