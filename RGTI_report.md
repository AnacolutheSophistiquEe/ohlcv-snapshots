# RGTI

**Generated** : 2026-07-02T21:54:32.648029+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.94  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $17.94 (+2.5% vs entrée) · entrée $17.51 · stop $16.97 · T1 $18.11 · R/R 1.11  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.141 _(réel 5 s)_ (GBM 0.022) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.12% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.40–$17.63 (mid $17.51)
- Spot actuel : $17.94 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $16.97 (stop swing_plan-based (-8.79%))
- Targets : T1 $18.11 · R/R 1.11 | T2 $18.70 · R/R 2.2 | T3 $19.29 · R/R 3.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.97


## Edge, scénarios & sizing

- EV/risk : 0.022 | EV/share : $0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.2 | bear 73.2 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.367% → cible +3.373% / stop −3.117%, p_fill 62%, n_eff≈25.1) : P(cible|rempli) **34%** · **EV/risk -0.141** (×p_fill ; si rempli -0.71% du capital)
  - **swing** (entrée dip −5.216% → cible +7.543% / stop −3.771%, p_fill 64%, n_eff≈23.2) : P(cible|rempli) **31%** · **EV/risk -0.081** (×p_fill ; si rempli -0.48% du capital)
  - **deep** (entrée dip −8.067% → cible +10.667% / stop −5.333%, p_fill 45%, n_eff≈17.4) : P(cible|rempli) **23%** · **EV/risk -0.125** (×p_fill ; si rempli -1.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→52% · +5.0%→36% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.31% / basse méd. −3.0%
- Profil de vol intra : ouverture 5.126% vs midi 1.692% vs clôture 1.954% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 49%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; momentum — autocorr 0.065)_ ; drift intra méd. 0.34% ; recovery-V 54%
- **σ réalisé intraday** 5.644% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 47% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 19.4734 (VA 19.1225–19.6084 ; dernier close 18.685)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 66% · rebond 78% · **stop −7.39%** sous le fill (sous le bruit) · cible +2.86% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. -0.64% · baisse 59% (gap-down >1% 47% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.44% (p90 −2.97%) · haut méd +1.01% · range méd 2.63%
- Excursion ouverture 15min (n=160) : bas méd −1.64% (p90 −4.55%) · haut méd +1.54% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.17%) · haut méd +1.92% · range méd 4.57%
- Excursion ouverture 60min (n=160) : bas méd −2.3% (p90 −6.53%) · haut méd +2.29% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.685 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 80% · séance 85% (136/159) · gap 54% · délai 0.0min · rebond 69% (91/136) (MFE +2.41%)
   - −1.0% : fill 30min 73% · séance 82% (132/159) · gap 47% · délai 0.0min · rebond 68% (88/132) (MFE +2.32%)
   - −1.5% : fill 30min 68% · séance 78% (124/159) · gap 40% · délai 0.0min · rebond 69% (84/124) (MFE +2.59%)
   - −2.0% : fill 30min 62% · séance 72% (114/159) · gap 30% · délai 0.0min · rebond 68% (76/114) (MFE +2.9%)
   - −3.0% : fill 30min 55% · séance 66% (99/159) · gap 14% · délai 1.3min · rebond 78% (74/99) (MFE +2.86%)
   - −4.0% : fill 30min 39% · séance 49% (78/159) · gap 6% · délai 3.8min · rebond 76% (58/78) (MFE +2.81%)
   - −5.0% : fill 30min 26% · séance 42% (66/159) · gap 2% · délai 15.0min · rebond 71% (51/66) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.09% (p90 −3.48%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −4.24%) → stop au-delà de −2.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.44% (p90 −4.47%) → stop au-delà de −2.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1188 jambes) : jambe baissière méd −1.29% (p90 −3.43%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 65% (50/82)
      · −2.0% : fill 92% (78/83) · rebond 68% (53/78)
      · −3.0% : fill 88% (71/83) · rebond 78% (53/71)
      · −4.0% : fill 67% (57/83) · rebond 77% (43/57)
      · −5.0% : fill 58% (50/83) · rebond 74% (41/50)
   - **flat** (14 séances) :
      · −1.0% : fill 86% (12/14) · rebond 84% (10/12)
      · −2.0% : fill 53% (9/14) · rebond 89% (7/9)
      · −3.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −4.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −5.0% : fill 30% (4/14) · rebond 77% (2/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 56% (38/62) · rebond 71% (28/38)
      · −2.0% : fill 43% (27/62) · rebond 61% (16/27)
      · −3.0% : fill 38% (24/62) · rebond 84% (19/24)
      · −4.0% : fill 25% (17/62) · rebond 78% (13/17)
      · −5.0% : fill 20% (12/62) · rebond 55% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 67% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:06** → P(séance verte=clôture>ouverture) 91% si début vert vs 20% si rouge (base 54% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **91%** · continue >prix actuel 58% ; creux résiduel méd -2.44% (q20 -3.69%) → **SL/trailing à −3.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.94% / q75 +4.92% → **scale +2.94% / runner +4.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **20%** (continue à baisser 50%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.66%** (au-delà de la MAE q10 -6.66%), cible rebond +2.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-6.07% .. +5.97%] · haut q95 +8.39% · bas q05 -7.1%
   - 60min (n=160) : retour [-6.09% .. +7.34%] · haut q95 +9.76% · bas q05 -7.34%
   - 2h (n=160) : retour [-7.66% .. +8.99%] · haut q95 +10.05% · bas q05 -8.4%
   - 4h (n=160) : retour [-8.88% .. +7.33%] · haut q95 +10.25% · bas q05 -10.51%
   - 6h (n=160) : retour [-8.83% .. +8.61%] · haut q95 +11.03% · bas q05 -10.51%
   - session (n=160) : retour [-8.04% .. +9.96%] · haut q95 +11.38% · bas q05 -10.51%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.86% / p90 2.67%) · ~4.0 replis/séance, durée méd 36.72 min. P(nouveau plus-haut après repli) :
   - −0.5% → **93%** (reprise méd 13.54 min, n=48)
   - −1.0% → **90%** (reprise méd 30.0 min, n=29)
   - −1.5% → **82%** (reprise méd 45.0 min, n=13)
   - −2.0% → **70%** (reprise méd 125.91 min, n=9)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.86%) ; extension open→close méd +8.41% (q75 +9.94% / q95 +11.6%), MFE méd +9.22% / q90 +12.07%
   - Échelle scale-out : +9.22% (33%) / +10.54% (33%) / +12.07% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **74%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.07% : P(retournement après) 0% (mèche méd 0.62%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.98%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist -0.386  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 30.5%
- **ATR** : 1.82 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.212  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 54.7  _(transition)_
- **MA** : MA20 20.33 · MA50 20.16 · MA200 23.88  _(prix < MA20)_
- **Dist MA** : MA20 -11.8% · MA50 -11.0% · MA200 -24.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90596 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
