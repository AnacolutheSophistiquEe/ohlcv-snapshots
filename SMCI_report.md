# SMCI

**Generated** : 2026-07-09T00:17:39.056985+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $28.17  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $28.17 (+2.5% vs entrée) · entrée $27.49 · stop $26.50 · T1 $29.48 · R/R 2.01  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.16 _(réel 5 s)_ (GBM 0.054) · ¼-Kelly 0.043 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.62% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $27.20–$27.78 (mid $27.49)
- Spot actuel : $28.17 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $26.50 (stop swing_plan-based (-16.66%))
- Targets : T1 $29.48 · R/R 2.01 | T2 $30.66 · R/R 3.2 | T3 $31.84 · R/R 4.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.50


## Edge, scénarios & sizing

- EV/risk : 0.054 | EV/share : $0.054 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.172 | ¼-Kelly 0.043 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.3 | bear 62.9 | side 15.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.406% → cible +7.243% / stop −3.621%, p_fill 61%, n_eff≈22.5) : P(cible|rempli) **1%** · **EV/risk -0.160** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −5.296% → cible +31.212% / stop −12.0%, p_fill 54%, n_eff≈18.7) : P(cible|rempli) **0%** · **EV/risk -0.208** (×p_fill ; si rempli -4.64% du capital)
  - **deep** (entrée dip −8.173% → cible +16.678% / stop −8.339%, p_fill 43%, n_eff≈14.2) : P(cible|rempli) **29%** · **EV/risk -0.103** (×p_fill ; si rempli -2.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→65% · +3.0%→48% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.47% (p90 11.21%) · excursion haute méd. +2.83% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.821% vs midi 1.271% vs clôture 1.507% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.143 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.487% ; recovery-V 20%
- **σ réalisé intraday** 4.387% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 70% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 26.4688 (VA 25.8912–26.4688 ; dernier close 26.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 68% · **stop −4.65%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 45% (gap-down >1% 31% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.2%) · haut méd +0.91% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −3.2%) · haut méd +1.24% · range méd 2.61%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −3.77%) · haut méd +1.46% · range méd 3.47%
- Excursion ouverture 60min (n=160) : bas méd −1.58% (p90 −4.4%) · haut méd +1.71% · range méd 4.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 77% (126/159) · gap 41% · délai 0.0min · rebond 55% (72/126) (MFE +1.19%)
   - −1.0% : fill 30min 58% · séance 71% (114/159) · gap 31% · délai 0.0min · rebond 57% (64/114) (MFE +1.14%)
   - −1.5% : fill 30min 49% · séance 66% (99/159) · gap 26% · délai 1.1min · rebond 63% (60/99) (MFE +1.45%)
   - −2.0% : fill 30min 44% · séance 58% (88/159) · gap 22% · délai 1.1min · rebond 66% (56/88) (MFE +1.59%)
   - −3.0% : fill 30min 28% · séance 50% (68/159) · gap 16% · délai 18.8min · rebond 57% (40/68) (MFE +1.77%)
   - −4.0% : fill 30min 20% · séance 40% (49/159) · gap 12% · délai 22.8min · rebond 67% (30/49) (MFE +1.49%)
   - −5.0% : fill 30min 16% · séance 32% (40/159) · gap 7% · délai 22.7min · rebond 68% (26/40) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.39%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −2.74%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.71%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=814 jambes) : jambe baissière méd −1.22% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (67/68) · rebond 51% (37/67)
      · −2.0% : fill 90% (59/68) · rebond 58% (33/59)
      · −3.0% : fill 83% (51/68) · rebond 55% (29/51)
      · −4.0% : fill 71% (40/68) · rebond 69% (25/40)
      · −5.0% : fill 57% (33/68) · rebond 66% (21/33)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 46% (33/75) · rebond 63% (17/33)
      · −2.0% : fill 29% (19/75) · rebond 85% (16/19)
      · −3.0% : fill 26% (15/75) · rebond 60% (9/15)
      · −4.0% : fill 16% (8/75) · rebond 56% (4/8)
      · −5.0% : fill 14% (7/75) · rebond 75% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 66% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:11** → P(séance verte=clôture>ouverture) 77% si début vert vs 14% si rouge (base 45% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.46% (q20 -2.99%) → **SL/trailing à −2.99%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.9% → **scale +1.8% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.51%** (au-delà de la MAE q10 -6.51%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +4.68%] · haut q95 +6.05% · bas q05 -4.49%
   - 60min (n=160) : retour [-4.42% .. +5.28%] · haut q95 +6.58% · bas q05 -5.81%
   - 2h (n=160) : retour [-4.88% .. +6.65%] · haut q95 +8.11% · bas q05 -5.84%
   - 4h (n=160) : retour [-6.5% .. +7.42%] · haut q95 +8.66% · bas q05 -7.45%
   - 6h (n=160) : retour [-6.61% .. +7.46%] · haut q95 +9.14% · bas q05 -8.96%
   - session (n=160) : retour [-7.96% .. +8.49%] · haut q95 +9.42% · bas q05 -9.42%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 12% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.7  _(neutre)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist -0.487  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 44.1%
- **ATR** : 2.5 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.119  _(distribution)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 30.42 · MA50 33.39 · MA200 34.75  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -15.6% · MA200 -18.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88768 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
