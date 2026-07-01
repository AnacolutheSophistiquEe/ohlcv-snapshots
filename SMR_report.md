# SMR

**Generated** : 2026-07-01T21:58:53.367554+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.15  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $10.15 (+1.2% vs entrée) · entrée $10.03 · stop $9.53 · T1 $11.03 · R/R 2.0  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.118 _(réel 5 s)_ (GBM 0.033) · ¼-Kelly 0.054 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.97% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.96–$10.10 (mid $10.03)
- Spot actuel : $10.15 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $9.53 (stop swing_plan-based (-12.32%))
- Targets : T1 $11.03 · R/R 2.0 | T2 $11.06 · R/R 2.06 | T3 $11.10 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.53


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : $0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.215 | ¼-Kelly 0.054 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.5 | bear 54.2 | side 26.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.192% → cible +9.934% / stop −4.967%, p_fill 66%, n_eff≈28.3) : P(cible|rempli) **1%** · **EV/risk -0.118** (×p_fill ; si rempli -0.89% du capital)
  - **swing** (entrée dip −2.633% → cible +19.9% / stop −9.949%, p_fill 69%, n_eff≈29.3) : P(cible|rempli) **7%** · **EV/risk -0.090** (×p_fill ; si rempli -1.29% du capital)
  - **deep** (entrée dip −4.063% → cible +30.37% / stop −15.184%, p_fill 69%, n_eff≈29.3) : P(cible|rempli) **7%** · **EV/risk -0.138** (×p_fill ; si rempli -3.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→65% · +3.0%→51% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.11% (p90 12.61%) · excursion haute méd. +3.05% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.812% vs midi 1.552% vs clôture 1.815% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr 0.009)_ ; drift intra méd. 0.411% ; recovery-V 22%
- **σ réalisé intraday** 5.267% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 45% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 9.8725 (VA 9.8275–10.0225 ; dernier close 10.01)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 63% · rebond 78% · **stop −6.55%** sous le fill (sous le bruit) · cible +2.96% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 62% (gap-down >1% 44% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.37% (p90 −3.54%) · haut méd +1.11% · range méd 2.87%
- Excursion ouverture 15min (n=160) : bas méd −1.75% (p90 −3.98%) · haut méd +1.38% · range méd 3.8%
- Excursion ouverture 30min (n=160) : bas méd −2.07% (p90 −5.58%) · haut méd +1.94% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −6.08%) · haut méd +2.45% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (132/159) · gap 55% · délai 0.0min · rebond 65% (81/132) (MFE +1.75%)
   - −1.0% : fill 30min 71% · séance 79% (126/159) · gap 44% · délai 0.0min · rebond 68% (83/126) (MFE +2.01%)
   - −1.5% : fill 30min 69% · séance 76% (120/159) · gap 40% · délai 0.0min · rebond 74% (86/120) (MFE +2.31%)
   - −2.0% : fill 30min 64% · séance 71% (115/159) · gap 29% · délai 0.2min · rebond 71% (84/115) (MFE +2.74%)
   - −3.0% : fill 30min 52% · séance 63% (103/159) · gap 14% · délai 2.1min · rebond 78% (84/103) (MFE +2.96%)
   - −4.0% : fill 30min 41% · séance 56% (87/159) · gap 7% · délai 8.2min · rebond 76% (67/87) (MFE +2.92%)
   - −5.0% : fill 30min 26% · séance 42% (64/159) · gap 4% · délai 14.8min · rebond 72% (47/64) (MFE +2.25%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.92%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.77% (p90 −3.67%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −3.85%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1197 jambes) : jambe baissière méd −1.36% (p90 −3.17%) · ~15.0 jambes/séance
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
      · −1.0% : fill 50% (32/62) · rebond 60% (21/32)
      · −2.0% : fill 43% (27/62) · rebond 62% (19/27)
      · −3.0% : fill 31% (20/62) · rebond 76% (16/20)
      · −4.0% : fill 27% (15/62) · rebond 67% (10/15)
      · −5.0% : fill 20% (13/62) · rebond 43% (7/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 63% si les 15 1res min sont vertes (64 cas) · 36% si rouges (96 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 75% si début vert vs 17% si rouge (base 48% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -2.63% (q20 -4.57%) → **SL/trailing à −4.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.49% / q75 +5.63% → **scale +2.49% / runner +5.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **17%** (continue à baisser 58%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.66%** (au-delà de la MAE q10 -7.66%), cible rebond +1.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.72% .. +4.49%] · haut q95 +6.59% · bas q05 -6.86%
   - 60min (n=160) : retour [-6.49% .. +5.92%] · haut q95 +8.77% · bas q05 -7.98%
   - 2h (n=160) : retour [-8.03% .. +9.67%] · haut q95 +11.42% · bas q05 -9.43%
   - 4h (n=160) : retour [-8.95% .. +8.43%] · haut q95 +11.42% · bas q05 -10.95%
   - 6h (n=160) : retour [-8.68% .. +8.76%] · haut q95 +11.66% · bas q05 -11.07%
   - session (n=160) : retour [-8.65% .. +10.94%] · haut q95 +11.74% · bas q05 -11.09%


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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.0  _(momentum haussier)_
- **ADX** : 11.0  _(pas de tendance nette)_
- **MACD** : hist -0.013  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 30.1%
- **ATR** : 0.88 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.209  _(distribution)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 57.0  _(transition)_
- **MA** : MA20 10.49 · MA50 11.46 · MA200 19.71  _(prix < MA20)_
- **Dist MA** : MA20 -3.2% · MA50 -11.4% · MA200 -48.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91268 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
