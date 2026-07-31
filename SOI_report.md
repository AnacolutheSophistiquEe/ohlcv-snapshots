# SOI

**Generated** : 2026-07-31T00:08:08.583795+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €105.05  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €105.05 (+5.9% vs entrée) · entrée €99.20 · stop €95.17 · T1 €107.27 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.115 _(réel 5 s)_ (GBM 0.147) · ¼-Kelly 0.069 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.07% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -68 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €98.32–€100.09 (mid €99.20)
- Spot actuel : €105.05 (+5.9% au-dessus de la zone — repli à attendre)
- Stop : €95.17 (stop swing_plan-based (-22.78%))
- Targets : T1 €107.27 · R/R 2.0 | T2 €109.86 · R/R 2.65 | T3 €112.44 · R/R 3.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €95.17


## Edge, scénarios & sizing

- EV/risk : 0.147 | EV/share : €0.595 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 45 % | T3 45 %
- Kelly (position) : f* 0.275 | ¼-Kelly 0.069 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.1 | bear 65.0 | side 20.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 315.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.571% → cible +8.132% / stop −4.066%, p_fill 36%, n_eff≈15.2) : P(cible|rempli) **2%** · **EV/risk -0.115** (×p_fill ; si rempli -1.31% du capital)
  - **swing** (entrée dip −12.25% → cible +27.732% / stop −12.0%, p_fill 21%, n_eff≈9.0) : P(cible|rempli) **6%** · **EV/risk +0.049** (×p_fill ; si rempli +2.79% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→69% · +3.0%→59% · +5.0%→45% · +8.0%→22%
- Range intraday médian 9.52% (p90 17.62%) · excursion haute méd. +3.99% / basse méd. −3.47%
- Profil de vol intra : ouverture 6.006% vs midi 1.694% vs clôture 2.597% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -0.789% ; recovery-V 33%
- **σ réalisé intraday** 5.691% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 62% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 97.1089 (VA 95.8909–98.1746 ; dernier close 95.83)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 78% · **stop −7.29%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.38 (high win-rate)
- Gaps overnight (n=142) : méd. -0.07% · baisse 50% (gap-down >1% 34% · >2% 24%)
- Excursion ouverture 5min (n=143) : bas méd −1.23% (p90 −3.82%) · haut méd +0.99% · range méd 3.12%
- Excursion ouverture 15min (n=143) : bas méd −1.53% (p90 −5.2%) · haut méd +1.39% · range méd 3.81%
- Excursion ouverture 30min (n=143) : bas méd −1.71% (p90 −5.64%) · haut méd +1.72% · range méd 4.35%
- Excursion ouverture 60min (n=143) : bas méd −1.95% (p90 −5.94%) · haut méd +1.82% · range méd 4.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.83 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (112/142) · gap 41% · délai 0.0min · rebond 64% (73/112) (MFE +1.93%)
   - −1.0% : fill 30min 64% · séance 76% (107/142) · gap 34% · délai 0.1min · rebond 70% (77/107) (MFE +1.87%)
   - −1.5% : fill 30min 61% · séance 72% (98/142) · gap 32% · délai 0.1min · rebond 74% (72/98) (MFE +2.26%)
   - −2.0% : fill 30min 56% · séance 68% (91/142) · gap 24% · délai 0.2min · rebond 77% (72/91) (MFE +2.73%)
   - −3.0% : fill 30min 42% · séance 59% (76/142) · gap 18% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 33% · séance 49% (61/142) · gap 8% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 25% · séance 45% (53/142) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.75%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −2.98%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.19%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1257 jambes) : jambe baissière méd −1.33% (p90 −3.17%) · ~18.0 jambes/séance
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
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (34/68) · rebond 85% (28/34)
      · −2.0% : fill 33% (22/68) · rebond 85% (18/22)
      · −3.0% : fill 30% (19/68) · rebond 83% (15/19)
      · −4.0% : fill 22% (13/68) · rebond 55% (9/13)
      · −5.0% : fill 20% (10/68) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 50% en base · 68% si les 15 1res min sont vertes (67 cas) · 30% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=143) : COUDE à **47min** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 50% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **86%** · continue >prix actuel 63% ; creux résiduel méd -2.3% (q20 -5.35%) → **SL/trailing à −5.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.28% / q75 +5.31% → **scale +3.28% / runner +5.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.57%** (au-delà de la MAE q10 -8.57%), cible rebond +2.44% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-5.28% .. +7.13%] · haut q95 +7.84% · bas q05 -6.66%
   - 60min (n=143) : retour [-5.99% .. +7.37%] · haut q95 +9.35% · bas q05 -7.18%
   - 2h (n=143) : retour [-6.32% .. +10.03%] · haut q95 +12.59% · bas q05 -8.07%
   - 4h (n=143) : retour [-7.12% .. +10.29%] · haut q95 +14.28% · bas q05 -8.31%
   - 6h (n=143) : retour [-8.24% .. +11.56%] · haut q95 +14.32% · bas q05 -10.12%
   - session (n=143) : retour [-11.59% .. +13.88%] · haut q95 +16.14% · bas q05 -13.8%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.3% des séances sont trend-up (mild 0% / strong 6.3%) · base = 9 séances trend-up (n_eff 5.7)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 54.3  _(neutre)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 1.867  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 37.6%
- **ATR** : 10.47 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.092  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 43.6  _(transition)_
- **MA** : MA20 101.39 · MA50 124.0 · MA200 70.67  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 -15.3% · MA200 +48.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98977 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
