# SOI

**Generated** : 2026-07-21T21:44:07.739850+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €95.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €95.48 (+8.6% vs entrée) · entrée €87.90 · stop €85.28 · T1 €91.07 · R/R 1.21  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.009 · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.98% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -30 % hors [0,100] (R² max 0.12). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €87.27–€88.53 (mid €87.90)
- Spot actuel : €95.48 (+8.6% au-dessus de la zone — repli à attendre)
- Stop : €85.28 (stop swing_plan-based (-20.8%))
- Targets : T1 €91.07 · R/R 1.21 | T2 €94.25 · R/R 2.42 | T3 €97.42 · R/R 3.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €85.28


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : €0.024 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.9 | bear 33.4 | side 57.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→68% · +3.0%→56% · +5.0%→42% · +8.0%→21%
- Range intraday médian 9.09% (p90 17.62%) · excursion haute méd. +3.52% / basse méd. −3.47%
- Profil de vol intra : ouverture 5.775% vs midi 1.693% vs clôture 2.568% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.785% ; recovery-V 38%
- **σ réalisé intraday** 5.529% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 68% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 85.815 (VA 83.865–86.465 ; dernier close 85.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 79% · **stop −7.26%** sous le fill (sous le bruit) · cible +2.85% · R/R 0.39 (high win-rate)
- Gaps overnight (n=135) : méd. 0.04% · baisse 49% (gap-down >1% 33% · >2% 24%)
- Excursion ouverture 5min (n=136) : bas méd −1.27% (p90 −3.55%) · haut méd +1.1% · range méd 3.17%
- Excursion ouverture 15min (n=136) : bas méd −1.55% (p90 −4.93%) · haut méd +1.35% · range méd 3.9%
- Excursion ouverture 30min (n=136) : bas méd −1.75% (p90 −5.41%) · haut méd +1.94% · range méd 4.39%
- Excursion ouverture 60min (n=136) : bas méd −2.09% (p90 −5.88%) · haut méd +1.97% · range méd 4.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 85.66 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (107/135) · gap 40% · délai 0.0min · rebond 62% (69/107) (MFE +1.9%)
   - −1.0% : fill 30min 63% · séance 76% (102/135) · gap 33% · délai 0.1min · rebond 69% (73/102) (MFE +1.83%)
   - −1.5% : fill 30min 59% · séance 72% (93/135) · gap 30% · délai 0.2min · rebond 73% (68/93) (MFE +2.18%)
   - −2.0% : fill 30min 54% · séance 67% (86/135) · gap 24% · délai 0.2min · rebond 76% (68/86) (MFE +2.67%)
   - −3.0% : fill 30min 42% · séance 57% (71/135) · gap 18% · délai 1.0min · rebond 74% (56/71) (MFE +2.81%)
   - −4.0% : fill 30min 31% · séance 48% (57/135) · gap 7% · délai 4.5min · rebond 74% (45/57) (MFE +2.45%)
   - −5.0% : fill 30min 24% · séance 45% (50/135) · gap 2% · délai 18.3min · rebond 79% (42/50) (MFE +2.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −3.79%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −3.31%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.21%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1191 jambes) : jambe baissière méd −1.34% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 97% (52/53) · rebond 58% (32/52)
      · −2.0% : fill 93% (50/53) · rebond 72% (39/50)
      · −3.0% : fill 83% (42/53) · rebond 74% (34/42)
      · −4.0% : fill 74% (37/53) · rebond 77% (30/37)
      · −5.0% : fill 70% (33/53) · rebond 85% (28/33)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (65 séances) :
      · −1.0% : fill 48% (33/65) · rebond 84% (27/33)
      · −2.0% : fill 33% (21/65) · rebond 82% (17/21)
      · −3.0% : fill 29% (18/65) · rebond 80% (14/18)
      · −4.0% : fill 20% (12/65) · rebond 68% (9/12)
      · −5.0% : fill 18% (9/65) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 51% en base · 70% si les 15 1res min sont vertes (62 cas) · 32% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=136) : COUDE à **36min** → P(séance verte=clôture>ouverture) 78% si début vert vs 25% si rouge (base 51% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **78%** · continue >prix actuel 57% ; creux résiduel méd -2.59% (q20 -5.61%) → **SL/trailing à −5.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.46% / q75 +5.79% → **scale +2.46% / runner +5.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **25%** (continue à baisser 61%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.63%** (au-delà de la MAE q10 -8.63%), cible rebond +2.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-5.35% .. +6.84%] · haut q95 +7.23% · bas q05 -6.39%
   - 60min (n=136) : retour [-6.13% .. +7.43%] · haut q95 +8.75% · bas q05 -6.78%
   - 2h (n=136) : retour [-6.83% .. +10.2%] · haut q95 +12.1% · bas q05 -8.22%
   - 4h (n=136) : retour [-7.22% .. +11.49%] · haut q95 +13.35% · bas q05 -8.54%
   - 6h (n=136) : retour [-8.73% .. +12.15%] · haut q95 +14.26% · bas q05 -10.51%
   - session (n=136) : retour [-12.11% .. +13.9%] · haut q95 +16.55% · bas q05 -13.98%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.9% des séances sont trend-up (mild 0% / strong 5.9%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -0.549  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 40.4%
- **ATR** : 8.73 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 45.2  _(transition)_
- **MA** : MA20 104.29 · MA50 130.56 · MA200 68.47  _(prix < MA20)_
- **Dist MA** : MA20 -8.4% · MA50 -26.9% · MA200 +39.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95000 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
