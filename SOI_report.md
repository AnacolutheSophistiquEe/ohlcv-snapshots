# SOI

**Generated** : 2026-08-04T00:09:22.062327+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €109.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €109.40 (+0.7% vs entrée) · entrée €108.65 · stop €104.10 · T1 €117.75 · R/R 2.0  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.17 _(réel 5 s)_ (GBM 0.119) · ¼-Kelly 0.067 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.19% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -47 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €107.90–€109.40 (mid €108.65)
- Spot actuel : €109.40 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €104.10 (stop swing_plan-based (-11.54%))
- Targets : T1 €117.75 · R/R 2.0 | T2 €120.44 · R/R 2.59 | T3 €123.12 · R/R 3.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €104.10


## Edge, scénarios & sizing

- EV/risk : 0.119 | EV/share : €0.541 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 45 % | T3 45 %
- Kelly (position) : f* 0.268 | ¼-Kelly 0.067 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 69.1 | side 25.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 219.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.691% → cible +8.377% / stop −4.188%, p_fill 89%, n_eff≈35.9) : P(cible|rempli) **9%** · **EV/risk -0.170** (×p_fill ; si rempli -0.80% du capital)
  - **swing** (entrée dip −1.523% → cible +18.809% / stop −10.172%, p_fill 83%, n_eff≈34.9) : P(cible|rempli) **18%** · **EV/risk -0.249** (×p_fill ; si rempli -3.04% du capital)
  - **deep** (entrée dip −2.214% → cible +27.221% / stop −15.366%, p_fill 95%, n_eff≈37.0) : P(cible|rempli) **26%** · **EV/risk -0.193** (×p_fill ; si rempli -3.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→59% · +5.0%→45% · +8.0%→22%
- Range intraday médian 9.57% (p90 16.36%) · excursion haute méd. +3.99% / basse méd. −3.56%
- Profil de vol intra : ouverture 6.009% vs midi 1.678% vs clôture 2.594% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.084)_ ; drift intra méd. -0.675% ; recovery-V 34%
- **σ réalisé intraday** 5.72% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 110.825 (VA 108.935–112.985 ; dernier close 103.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 43% · rebond 78% · **stop −7.29%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.38 (high win-rate)
- Gaps overnight (n=144) : méd. 0.09% · baisse 49% (gap-down >1% 33% · >2% 24%)
- Excursion ouverture 5min (n=145) : bas méd −1.23% (p90 −3.79%) · haut méd +0.99% · range méd 2.98%
- Excursion ouverture 15min (n=145) : bas méd −1.52% (p90 −5.14%) · haut méd +1.54% · range méd 3.81%
- Excursion ouverture 30min (n=145) : bas méd −1.68% (p90 −5.57%) · haut méd +1.82% · range méd 4.35%
- Excursion ouverture 60min (n=145) : bas méd −1.82% (p90 −5.88%) · haut méd +1.91% · range méd 4.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 103.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (114/144) · gap 39% · délai 0.0min · rebond 64% (74/114) (MFE +1.93%)
   - −1.0% : fill 30min 62% · séance 75% (108/144) · gap 33% · délai 0.1min · rebond 71% (78/108) (MFE +1.83%)
   - −1.5% : fill 30min 58% · séance 72% (99/144) · gap 30% · délai 0.2min · rebond 74% (73/99) (MFE +2.18%)
   - −2.0% : fill 30min 54% · séance 65% (91/144) · gap 24% · délai 0.2min · rebond 77% (72/91) (MFE +2.73%)
   - −3.0% : fill 30min 40% · séance 57% (76/144) · gap 17% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 32% · séance 47% (61/144) · gap 8% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 24% · séance 43% (53/144) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.71%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −2.89%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.97% (p90 −3.19%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1273 jambes) : jambe baissière méd −1.34% (p90 −3.16%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 98% (56/57) · rebond 61% (35/56)
      · −2.0% : fill 94% (54/57) · rebond 72% (42/54)
      · −3.0% : fill 86% (46/57) · rebond 74% (37/46)
      · −4.0% : fill 74% (40/57) · rebond 81% (33/40)
      · −5.0% : fill 67% (35/57) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (70 séances) :
      · −1.0% : fill 47% (35/70) · rebond 86% (29/35)
      · −2.0% : fill 30% (22/70) · rebond 85% (18/22)
      · −3.0% : fill 27% (19/70) · rebond 83% (15/19)
      · −4.0% : fill 20% (13/70) · rebond 55% (9/13)
      · −5.0% : fill 18% (10/70) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 50% en base · 69% si les 15 1res min sont vertes (68 cas) · 29% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=145) : COUDE à **47min** → P(séance verte=clôture>ouverture) 82% si début vert vs 24% si rouge (base 50% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **82%** · continue >prix actuel 60% ; creux résiduel méd -2.36% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.17% / q75 +5.16% → **scale +3.17% / runner +5.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **24%** (continue à baisser 57%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.54%** (au-delà de la MAE q10 -8.54%), cible rebond +2.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-5.26% .. +7.09%] · haut q95 +7.71% · bas q05 -6.65%
   - 60min (n=145) : retour [-5.97% .. +7.29%] · haut q95 +9.3% · bas q05 -7.13%
   - 2h (n=145) : retour [-6.1% .. +9.99%] · haut q95 +12.53% · bas q05 -8.02%
   - 4h (n=145) : retour [-7.03% .. +10.28%] · haut q95 +14.28% · bas q05 -8.24%
   - 6h (n=145) : retour [-8.05% .. +11.29%] · haut q95 +14.31% · bas q05 -9.96%
   - session (n=145) : retour [-11.46% .. +13.86%] · haut q95 +16.02% · bas q05 -13.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 54.0  _(neutre)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist 2.131  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 32.0%
- **ATR** : 10.96 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.132  _(distribution)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 100.22 · MA50 121.17 · MA200 71.35  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 -9.7% · MA200 +53.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (99076 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
