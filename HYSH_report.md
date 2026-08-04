# 298040

**Generated** : 2026-08-04T00:16:45.369148+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2495000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2495000.00 (+0.8% vs entrée) · entrée ₩2475568.51 · stop ₩2377852.77 · T1 ₩2671000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.344 _(réel 5 s)_ (GBM -0.185) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2456137.02–₩2495000.00 (mid ₩2475568.51)
- Spot actuel : ₩2495000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2377852.77 (stop swing_plan-based (-13.51%))
- Targets : T1 ₩2671000.00 · R/R 2.0 | T2 ₩2753613.56 · R/R 2.85 | T3 ₩2836227.12 · R/R 3.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2377852.77


## Edge, scénarios & sizing

- EV/risk : -0.185 | EV/share : ₩-18100.553 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.7 | bear 68.5 | side 24.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.784% → cible +7.894% / stop −3.947%, p_fill 92%, n_eff≈37.1) : P(cible|rempli) **5%** · **EV/risk -0.344** (×p_fill ; si rempli -1.48% du capital)
  - **swing** (entrée dip −1.719% → cible +23.994% / stop −11.997%, p_fill 92%, n_eff≈37.3) : P(cible|rempli) **0%** · **EV/risk -0.408** (×p_fill ; si rempli -5.32% du capital)
  - **deep** (entrée dip −2.506% → cible +15.357% / stop −16.959%, p_fill 93%, n_eff≈35.6) : P(cible|rempli) **16%** · **EV/risk -0.475** (×p_fill ; si rempli -8.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→52% · +3.0%→39% · +5.0%→24% · +8.0%→8%
- Range intraday médian 7.03% (p90 10.49%) · excursion haute méd. +2.14% / basse méd. −4.06%
- Profil de vol intra : ouverture 4.417% vs midi 1.152% vs clôture 1.202% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 25% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.148 ; mean-reverting — autocorr -0.09)_ ; drift intra méd. -1.874% ; recovery-V 28%
- **σ réalisé intraday** 5.475% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 67% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 2343812.5 (VA 2305687.5–2389562.5 ; dernier close 2416000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 84% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.37 (high win-rate)
- Gaps overnight (n=144) : méd. 0.51% · baisse 38% (gap-down >1% 25% · >2% 16%)
- Excursion ouverture 5min (n=145) : bas méd −1.29% (p90 −3.39%) · haut méd +0.86% · range méd 2.76%
- Excursion ouverture 15min (n=145) : bas méd −2.09% (p90 −4.39%) · haut méd +1.11% · range méd 3.88%
- Excursion ouverture 30min (n=145) : bas méd −2.51% (p90 −4.92%) · haut méd +1.12% · range méd 4.28%
- Excursion ouverture 60min (n=145) : bas méd −2.58% (p90 −5.32%) · haut méd +1.36% · range méd 4.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2416000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (99/144) · gap 33% · délai 0.0min · rebond 60% (61/99) (MFE +1.27%)
   - −1.0% : fill 30min 58% · séance 68% (91/144) · gap 25% · délai 0.6min · rebond 59% (56/91) (MFE +1.55%)
   - −1.5% : fill 30min 51% · séance 61% (82/144) · gap 22% · délai 1.3min · rebond 52% (49/82) (MFE +1.29%)
   - −2.0% : fill 30min 45% · séance 58% (73/144) · gap 16% · délai 4.2min · rebond 54% (40/73) (MFE +1.29%)
   - −3.0% : fill 30min 34% · séance 50% (60/144) · gap 8% · délai 10.1min · rebond 53% (33/60) (MFE +1.03%)
   - −4.0% : fill 30min 23% · séance 46% (52/144) · gap 6% · délai 26.4min · rebond 65% (37/52) (MFE +1.62%)
   - −5.0% : fill 30min 20% · séance 36% (39/144) · gap 5% · délai 28.8min · rebond 84% (32/39) (MFE +2.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.11%) → stop au-delà de −2.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.94%) → stop au-delà de −2.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −4.19%) → stop au-delà de −2.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=784 jambes) : jambe baissière méd −1.43% (p90 −3.66%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 59% (31/50)
      · −2.0% : fill 89% (42/50) · rebond 54% (23/42)
      · −3.0% : fill 85% (40/50) · rebond 54% (22/40)
      · −4.0% : fill 81% (35/50) · rebond 70% (25/35)
      · −5.0% : fill 69% (29/50) · rebond 84% (23/29)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (78 séances) :
      · −1.0% : fill 44% (30/78) · rebond 58% (17/30)
      · −2.0% : fill 35% (23/78) · rebond 53% (12/23)
      · −3.0% : fill 26% (15/78) · rebond 45% (7/15)
      · −4.0% : fill 21% (12/78) · rebond 64% (9/12)
      · −5.0% : fill 13% (7/78) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 37% en base · 60% si les 15 1res min sont vertes (59 cas) · 25% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **57min** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 37% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **77%** · continue >prix actuel 44% ; creux résiduel méd -2.22% (q20 -4.81%) → **SL/trailing à −4.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +3.36% → **scale +1.84% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **15%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.79%** (au-delà de la MAE q10 -5.79%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-4.72% .. +4.61%] · haut q95 +6.28% · bas q05 -5.3%
   - 60min (n=145) : retour [-5.25% .. +5.33%] · haut q95 +7.65% · bas q05 -6.19%
   - 2h (n=145) : retour [-7.56% .. +4.83%] · haut q95 +7.95% · bas q05 -8.73%
   - 4h (n=145) : retour [-8.0% .. +5.47%] · haut q95 +8.51% · bas q05 -10.2%
   - 6h (n=145) : retour [-8.03% .. +5.87%] · haut q95 +8.99% · bas q05 -10.2%
   - session (n=145) : retour [-7.0% .. +5.92%] · haut q95 +8.99% · bas q05 -10.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.5% des séances sont trend-up (mild 0% / strong 5.5%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 22% vs absente 0% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -11554.841  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 45.1%
- **ATR** : 275000.0 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.16  _(distribution)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 2625300.0 · MA50 3193160.0 · MA200 2649466.34  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -21.9% · MA200 -5.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88056 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
