# SOI

**Generated** : 2026-07-17T21:45:01.890493+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €87.34  

> 🟡 **WAIT-FOR-DIP** — spot +6.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €87.34 (+6.8% vs entrée) · entrée €81.80 · stop €79.12 · T1 €84.77 · R/R 1.11  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.025 · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.27% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -428 % hors [0,100] (R² max 0.63). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €81.20–€82.39 (mid €81.80)
- Spot actuel : €87.34 (+6.8% au-dessus de la zone — repli à attendre)
- Stop : €79.12 (stop swing_plan-based (-17.46%))
- Targets : T1 €84.77 · R/R 1.11 | T2 €87.74 · R/R 2.22 | T3 €90.71 · R/R 3.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €79.12


## Edge, scénarios & sizing

- EV/risk : 0.025 | EV/share : €0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.0 | bear 39.4 | side 52.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 87.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.346% → cible +3.633% / stop −3.272%, p_fill 31%, n_eff≈11.7) : P(cible|rempli) **12%** · **EV/risk -0.117** (×p_fill ; si rempli -1.25% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→76% · +2.0%→66% · +3.0%→56% · +5.0%→42% · +8.0%→21%
- Range intraday médian 9.09% (p90 17.62%) · excursion haute méd. +3.52% / basse méd. −3.47%
- Profil de vol intra : ouverture 5.777% vs midi 1.726% vs clôture 2.553% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.84% ; recovery-V 36%
- **σ réalisé intraday** 5.605% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 65% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 90.749 (VA 89.519–90.995 ; dernier close 89.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 66% · rebond 78% · **stop −8.53%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.31 (high win-rate)
- Gaps overnight (n=133) : méd. 0.09% · baisse 48% (gap-down >1% 32% · >2% 23%)
- Excursion ouverture 5min (n=134) : bas méd −1.27% (p90 −3.58%) · haut méd +1.1% · range méd 3.19%
- Excursion ouverture 15min (n=134) : bas méd −1.55% (p90 −4.96%) · haut méd +1.35% · range méd 4.11%
- Excursion ouverture 30min (n=134) : bas méd −1.75% (p90 −5.58%) · haut méd +1.94% · range méd 4.44%
- Excursion ouverture 60min (n=134) : bas méd −2.09% (p90 −5.89%) · haut méd +2.01% · range méd 4.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 89.56 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (105/133) · gap 40% · délai 0.0min · rebond 63% (68/105) (MFE +2.0%)
   - −1.0% : fill 30min 62% · séance 75% (100/133) · gap 32% · délai 0.2min · rebond 70% (72/100) (MFE +1.97%)
   - −1.5% : fill 30min 57% · séance 71% (91/133) · gap 29% · délai 0.2min · rebond 74% (67/91) (MFE +2.18%)
   - −2.0% : fill 30min 52% · séance 66% (84/133) · gap 23% · délai 0.2min · rebond 78% (67/84) (MFE +2.67%)
   - −3.0% : fill 30min 39% · séance 56% (69/133) · gap 17% · délai 0.9min · rebond 72% (54/69) (MFE +2.81%)
   - −4.0% : fill 30min 31% · séance 46% (55/133) · gap 8% · délai 4.4min · rebond 71% (43/55) (MFE +2.13%)
   - −5.0% : fill 30min 25% · séance 43% (48/133) · gap 2% · délai 14.1min · rebond 77% (40/48) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.81%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.59%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.21%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1174 jambes) : jambe baissière méd −1.34% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 97% (51/52) · rebond 61% (32/51)
      · −2.0% : fill 93% (49/52) · rebond 75% (39/49)
      · −3.0% : fill 82% (41/52) · rebond 72% (33/41)
      · −4.0% : fill 73% (36/52) · rebond 76% (29/36)
      · −5.0% : fill 68% (32/52) · rebond 84% (27/32)
   - **flat** (16 séances) :
      · −1.0% : fill 100% (16/16) · rebond 76% (13/16)
      · −2.0% : fill 96% (14/16) · rebond 80% (11/14)
      · −3.0% : fill 64% (10/16) · rebond 59% (7/10)
      · −4.0% : fill 50% (7/16) · rebond 54% (5/7)
      · −5.0% : fill 50% (7/16) · rebond 70% (6/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 48% (33/65) · rebond 84% (27/33)
      · −2.0% : fill 33% (21/65) · rebond 82% (17/21)
      · −3.0% : fill 29% (18/65) · rebond 80% (14/18)
      · −4.0% : fill 20% (12/65) · rebond 68% (9/12)
      · −5.0% : fill 18% (9/65) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 51% en base · 69% si les 15 1res min sont vertes (61 cas) · 34% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=134) : COUDE à **48min** → P(séance verte=clôture>ouverture) 82% si début vert vs 24% si rouge (base 51% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **82%** · continue >prix actuel 54% ; creux résiduel méd -2.38% (q20 -6.26%) → **SL/trailing à −6.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.71% / q75 +5.08% → **scale +2.71% / runner +5.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 59%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.77%** (au-delà de la MAE q10 -8.77%), cible rebond +2.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-5.36% .. +6.9%] · haut q95 +7.26% · bas q05 -6.44%
   - 60min (n=134) : retour [-6.16% .. +7.66%] · haut q95 +8.95% · bas q05 -6.8%
   - 2h (n=134) : retour [-6.94% .. +10.23%] · haut q95 +12.18% · bas q05 -8.29%
   - 4h (n=134) : retour [-7.24% .. +11.88%] · haut q95 +13.65% · bas q05 -8.6%
   - 6h (n=134) : retour [-8.79% .. +12.28%] · haut q95 +14.45% · bas q05 -10.57%
   - session (n=134) : retour [-12.26% .. +13.98%] · haut q95 +16.69% · bas q05 -13.99%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.0% des séances sont trend-up (mild 0% / strong 6.0%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 7% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.19% (p75 2.41% / p90 3.18%) · ~5.56 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **91%** (reprise méd 20.0 min, n=51)
   - −1.0% → **89%** (reprise méd 25.0 min, n=30)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.41%) ; extension open→close méd +13.56% (q75 +14.42% / q95 +17.52%), MFE méd +14.58% / q90 +18.51%
   - Échelle scale-out : +14.58% (33%) / +17.98% (33%) / +18.51% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.51% : P(retournement après) 0% (mèche méd 1.28%)
- **CONTEXTE** : la dernière heure tient les gains 91% du temps (retour médian dernière heure +3.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.2  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -1.174  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 41.5%
- **ATR** : 8.92 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.12  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 40.6  _(transition)_
- **MA** : MA20 107.69 · MA50 133.05 · MA200 68.01  _(prix < MA20)_
- **Dist MA** : MA20 -18.9% · MA50 -34.4% · MA200 +28.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (97837 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
