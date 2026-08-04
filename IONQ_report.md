# IONQ

**Generated** : 2026-08-04T22:03:26.050238+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $41.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)  
> ↳ spot $41.72 (+1.7% vs entrée) · entrée $41.01 · stop $39.33 · T1 $44.37 · R/R 2.0  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.142 _(réel 5 s)_ (GBM -0.024) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.1% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $40.76–$41.26 (mid $41.01)
- Spot actuel : $41.72 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $39.33 (stop swing_plan-based (-10.46%))
- Targets : T1 $44.37 · R/R 2.0 | T2 $44.56 · R/R 2.11 | T3 $44.75 · R/R 2.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.33


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.040 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.112 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 65.7 | bear 26.7 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 125.0 (= 3 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.704% → cible +8.191% / stop −4.096%, p_fill 68%, n_eff≈30.1) : P(cible|rempli) **7%** · **EV/risk -0.142** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −3.744% → cible +6.8% / stop −6.977%, p_fill 76%, n_eff≈29.4) : P(cible|rempli) **51%** · **EV/risk -0.044** (×p_fill ; si rempli -0.40% du capital)
  - **deep** (entrée dip −5.787% → cible +9.616% / stop −10.692%, p_fill 73%, n_eff≈28.3) : P(cible|rempli) **21%** · **EV/risk -0.412** (×p_fill ; si rempli -6.04% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→62% · +5.0%→32% · +8.0%→18%
- Range intraday médian 7.83% (p90 12.75%) · excursion haute méd. +3.72% / basse méd. −2.98%
- Profil de vol intra : ouverture 5.322% vs midi 1.576% vs clôture 1.709% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; momentum — autocorr 0.035)_ ; drift intra méd. -0.369% ; recovery-V 26%
- **σ réalisé intraday** 4.764% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 66% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 39.9767 (VA 39.5147–39.9767 ; dernier close 38.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.36% · baisse 55% (gap-down >1% 39% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.9%) · haut méd +1.19% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.15%) · haut méd +1.34% · range méd 3.68%
- Excursion ouverture 30min (n=160) : bas méd −1.87% (p90 −5.26%) · haut méd +1.85% · range méd 4.52%
- Excursion ouverture 60min (n=160) : bas méd −2.43% (p90 −5.93%) · haut méd +2.4% · range méd 5.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 38.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 82% (134/159) · gap 46% · délai 0.0min · rebond 69% (92/134) (MFE +1.89%)
   - −1.0% : fill 30min 70% · séance 78% (127/159) · gap 39% · délai 0.0min · rebond 74% (93/127) (MFE +2.36%)
   - −1.5% : fill 30min 67% · séance 76% (122/159) · gap 33% · délai 0.0min · rebond 67% (83/122) (MFE +2.62%)
   - −2.0% : fill 30min 58% · séance 68% (112/159) · gap 19% · délai 0.2min · rebond 67% (76/112) (MFE +2.6%)
   - −3.0% : fill 30min 47% · séance 57% (92/159) · gap 9% · délai 7.8min · rebond 72% (66/92) (MFE +2.79%)
   - −4.0% : fill 30min 30% · séance 45% (73/159) · gap 5% · délai 16.5min · rebond 72% (55/73) (MFE +2.21%)
   - −5.0% : fill 30min 19% · séance 39% (63/159) · gap 2% · délai 31.1min · rebond 83% (54/63) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.87%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −3.48%) → stop au-delà de −2.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −2.86%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1121 jambes) : jambe baissière méd −1.31% (p90 −3.18%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 74% (56/75)
      · −2.0% : fill 95% (71/75) · rebond 72% (53/71)
      · −3.0% : fill 80% (60/75) · rebond 70% (44/60)
      · −4.0% : fill 60% (45/75) · rebond 69% (34/45)
      · −5.0% : fill 54% (39/75) · rebond 77% (31/39)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 52% (39/68) · rebond 71% (28/39)
      · −2.0% : fill 36% (29/68) · rebond 52% (17/29)
      · −3.0% : fill 31% (23/68) · rebond 78% (17/23)
      · −4.0% : fill 25% (20/68) · rebond 79% (17/20)
      · −5.0% : fill 22% (17/68) · rebond 100% (17/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 52% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 78% si début vert vs 17% si rouge (base 43% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -2.33% (q20 -3.54%) → **SL/trailing à −3.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.82% / q75 +2.96% → **scale +1.82% / runner +2.96%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.24%** (au-delà de la MAE q10 -4.24%), cible rebond +2.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +7.17%] · haut q95 +8.25% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.15% .. +7.32%] · haut q95 +9.24% · bas q05 -6.69%
   - 2h (n=160) : retour [-6.37% .. +8.73%] · haut q95 +11.38% · bas q05 -7.26%
   - 4h (n=160) : retour [-7.24% .. +8.01%] · haut q95 +11.96% · bas q05 -8.26%
   - 6h (n=160) : retour [-7.48% .. +7.96%] · haut q95 +11.99% · bas q05 -8.51%
   - session (n=160) : retour [-7.31% .. +8.45%] · haut q95 +11.99% · bas q05 -8.51%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 2.0% / p90 2.73%) · ~4.0 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **79%** (reprise méd 15.0 min, n=42)
   - −1.0% → **69%** (reprise méd 27.77 min, n=26)
   - −1.5% → **47%** (reprise méd 38.13 min, n=13)
   - −2.0% → **37%** (reprise méd 31.37 min, n=9)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.73%** (p90, défaut prudent ; serré/agressif −2.0%) ; extension open→close méd +8.22% (q75 +9.41% / q95 +18.2%), MFE méd +10.74% / q90 +15.71%
   - Échelle scale-out : +10.74% (33%) / +12.6% (33%) / +15.71% (34%)
- **DÉSARMER** : repli > **−2.73%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.71% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 68% du temps (retour médian dernière heure +0.5%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 58.8  _(momentum haussier)_
- **ADX** : 34.6  _(tendance etablie)_
- **MACD** : hist 1.233  _(bullish_recent)_
- **BB** : %B 0.79 · largeur 41.4%
- **ATR** : 2.8 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.203  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 37.21 · MA50 50.05 · MA200 45.95  _(prix > MA20)_
- **Dist MA** : MA20 +12.1% · MA50 -16.6% · MA200 -9.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93228 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
