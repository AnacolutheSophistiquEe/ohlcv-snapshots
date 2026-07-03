# SMR

**Generated** : 2026-07-03T00:22:04.368407+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.76  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $9.76 (+0.5% vs entrée) · entrée $9.71 · stop $9.28 · T1 $10.03 · R/R 0.74  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.016 _(réel 5 s)_ (GBM 0.015) · ¼-Kelly 0.035 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.67–$9.76 (mid $9.71)
- Spot actuel : $9.76 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $9.28 (stop swing_plan-based (-4.61%))
- Targets : T1 $10.03 · R/R 0.74 | T2 $10.35 · R/R 1.49 | T3 $10.66 · R/R 2.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.28


## Edge, scénarios & sizing

- EV/risk : 0.015 | EV/share : $0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.138 | ¼-Kelly 0.035 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.4 | bear 18.3 | side 63.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.482% → cible +3.266% / stop −4.5%, p_fill 81%, n_eff≈34.4) : P(cible|rempli) **50%** · **EV/risk +0.016** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −0.995% → cible +7.301% / stop −3.651%, p_fill 82%, n_eff≈34.2) : P(cible|rempli) **22%** · **EV/risk -0.306** (×p_fill ; si rempli -1.37% du capital)
  - **deep** (entrée dip −1.442% → cible +10.325% / stop −5.162%, p_fill 76%, n_eff≈34.8) : P(cible|rempli) **43%** · **EV/risk +0.196** (×p_fill ; si rempli +1.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→65% · +3.0%→51% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.11% (p90 12.61%) · excursion haute méd. +3.05% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.801% vs midi 1.554% vs clôture 1.8% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr 0.018)_ ; drift intra méd. 0.371% ; recovery-V 20%
- **σ réalisé intraday** 5.208% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 43% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 10.3516 (VA 10.2203–10.4828 ; dernier close 10.15)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 78% · **stop −6.54%** sous le fill (sous le bruit) · cible +3.03% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 61% (gap-down >1% 43% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.39% (p90 −3.51%) · haut méd +1.1% · range méd 2.87%
- Excursion ouverture 15min (n=160) : bas méd −1.77% (p90 −3.97%) · haut méd +1.35% · range méd 3.77%
- Excursion ouverture 30min (n=160) : bas méd −2.04% (p90 −5.56%) · haut méd +1.91% · range méd 4.29%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −6.05%) · haut méd +2.56% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.15 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 81% (131/159) · gap 54% · délai 0.0min · rebond 66% (81/131) (MFE +1.76%)
   - −1.0% : fill 30min 70% · séance 78% (125/159) · gap 43% · délai 0.0min · rebond 68% (83/125) (MFE +2.01%)
   - −1.5% : fill 30min 68% · séance 74% (119/159) · gap 39% · délai 0.0min · rebond 74% (86/119) (MFE +2.31%)
   - −2.0% : fill 30min 63% · séance 70% (114/159) · gap 29% · délai 0.2min · rebond 71% (84/114) (MFE +2.74%)
   - −3.0% : fill 30min 51% · séance 62% (102/159) · gap 14% · délai 2.1min · rebond 78% (84/102) (MFE +3.03%)
   - −4.0% : fill 30min 40% · séance 55% (86/159) · gap 7% · délai 8.1min · rebond 76% (67/86) (MFE +2.94%)
   - −5.0% : fill 30min 26% · séance 41% (63/159) · gap 4% · délai 14.5min · rebond 72% (46/63) (MFE +2.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.9%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −3.56%) → stop au-delà de −2.19% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.06% (p90 −3.83%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1192 jambes) : jambe baissière méd −1.36% (p90 −3.18%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 72% (55/84)
      · −2.0% : fill 92% (80/84) · rebond 76% (60/80)
      · −3.0% : fill 86% (77/84) · rebond 81% (64/77)
      · −4.0% : fill 76% (66/84) · rebond 79% (54/66)
      · −5.0% : fill 58% (47/84) · rebond 81% (37/47)
   - **flat** (13 séances) :
      · −1.0% : fill 71% (10/13) · rebond 55% (7/10)
      · −2.0% : fill 55% (8/13) · rebond 43% (5/8)
      · −3.0% : fill 50% (6/13) · rebond 42% (4/6)
      · −4.0% : fill 50% (6/13) · rebond 57% (3/6)
      · −5.0% : fill 34% (4/13) · rebond 51% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 47% (31/62) · rebond 60% (21/31)
      · −2.0% : fill 41% (26/62) · rebond 63% (19/26)
      · −3.0% : fill 29% (19/62) · rebond 77% (16/19)
      · −4.0% : fill 26% (14/62) · rebond 68% (10/14)
      · −5.0% : fill 19% (12/62) · rebond 42% (6/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 63% si les 15 1res min sont vertes (64 cas) · 35% si rouges (96 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 82% si début vert vs 14% si rouge (base 47% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 185min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **82%** · continue >prix actuel 50% ; creux résiduel méd -1.93% (q20 -3.95%) → **SL/trailing à −3.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.77% / q75 +4.27% → **scale +2.77% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **14%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.92%** (au-delà de la MAE q10 -5.92%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.71% .. +4.46%] · haut q95 +6.59% · bas q05 -6.85%
   - 60min (n=160) : retour [-6.46% .. +5.9%] · haut q95 +8.67% · bas q05 -7.98%
   - 2h (n=160) : retour [-8.01% .. +9.51%] · haut q95 +11.41% · bas q05 -9.38%
   - 4h (n=160) : retour [-8.92% .. +8.43%] · haut q95 +11.41% · bas q05 -10.92%
   - 6h (n=160) : retour [-8.67% .. +8.76%] · haut q95 +11.65% · bas q05 -11.05%
   - session (n=160) : retour [-8.61% .. +10.92%] · haut q95 +11.74% · bas q05 -11.08%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0.6% / strong 4.4%) · base = 8 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **12%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.19% (p75 1.56% / p90 2.99%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=44)
   - −1.0% → **81%** (reprise méd 19.98 min, n=26)
   - −1.5% → **72%** (reprise méd 40.32 min, n=11)
   - −2.0% → **89%** (reprise méd 49.41 min, n=8)
   - −3.0% → **100%** (reprise méd 84.35 min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.99%** (p90, défaut prudent ; serré/agressif −1.56%) ; extension open→close méd +11.04% (q75 +11.76% / q95 +11.9%), MFE méd +12.98% / q90 +13.48%
   - Échelle scale-out : +12.98% (33%) / +13.38% (33%) / +13.48% (34%)
- **DÉSARMER** : repli > **−2.99%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.48% : P(retournement après) 0% (mèche méd 2.37%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 51.5  _(neutre)_
- **ADX** : 11.0  _(pas de tendance nette)_
- **MACD** : hist -0.03  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 26.4%
- **ATR** : 0.92 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.197  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 66.1  _(marche en range (choppy))_
- **MA** : MA20 10.37 · MA50 11.42 · MA200 19.56  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -14.6% · MA200 -50.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89040 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
