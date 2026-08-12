# 000660

**Generated** : 2026-08-12T00:12:03.482206+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1425000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩1425000.00 (+3.2% vs entrée) · entrée ₩1380250.00 · stop ₩1326142.86 · T1 ₩1451408.34 · R/R 1.32  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk -0.083 _(réel 5 s)_ (GBM -0.134) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.92% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1366018.33–₩1394481.67 (mid ₩1380250.00)
- Spot actuel : ₩1425000.00 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1326142.86 (stop swing_plan-based (-18.08%))
- Targets : T1 ₩1451408.34 · R/R 1.32 | T2 ₩1522566.68 · R/R 2.63 | T3 ₩1593725.02 · R/R 3.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1326142.86


## Edge, scénarios & sizing

- EV/risk : -0.134 | EV/share : ₩-7253.565 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.055 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 62.2 | side 30.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.143% → cible +5.155% / stop −3.92%, p_fill 72%, n_eff≈26.7) : P(cible|rempli) **15%** · **EV/risk -0.083** (×p_fill ; si rempli -0.45% du capital)
  - **swing** (entrée dip −6.909% → cible +11.528% / stop −12.0%, p_fill 60%, n_eff≈20.7) : P(cible|rempli) **19%** · **EV/risk -0.285** (×p_fill ; si rempli -5.67% du capital)
  - **deep** (entrée dip −10.683% → cible +16.303% / stop −18.0%, p_fill 53%, n_eff≈18.2) : P(cible|rempli) **12%** · **EV/risk -0.313** (×p_fill ; si rempli -10.66% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→52% · +3.0%→38% · +5.0%→28% · +8.0%→14%
- Range intraday médian 7.08% (p90 11.62%) · excursion haute méd. +2.08% / basse méd. −3.04%
- Profil de vol intra : ouverture 3.298% vs midi 1.411% vs clôture 1.613% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (154 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑2%/↓0% ; spike-down 74% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -2.133% ; recovery-V 22%
- **σ réalisé intraday** 5.353% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 78% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 1425400.0 (VA 1415800.0–1435000.0 ; dernier close 1421000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 70% · **stop −8.33%** sous le fill (sous le bruit) · cible +2.6% · R/R 0.31 (high win-rate)
- Gaps overnight (n=153) : méd. 0.04% · baisse 48% (gap-down >1% 36% · >2% 30%)
- Excursion ouverture 5min (n=154) : bas méd −0.73% (p90 −2.09%) · haut méd +0.85% · range méd 1.7%
- Excursion ouverture 15min (n=154) : bas méd −0.86% (p90 −2.86%) · haut méd +1.05% · range méd 2.34%
- Excursion ouverture 30min (n=154) : bas méd −1.53% (p90 −4.01%) · haut méd +1.23% · range méd 2.94%
- Excursion ouverture 60min (n=154) : bas méd −1.78% (p90 −4.94%) · haut méd +1.42% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1421000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 70% (98/153) · gap 41% · délai 0.0min · rebond 53% (51/98) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 66% (90/153) · gap 36% · délai 0.0min · rebond 61% (55/90) (MFE +1.74%)
   - −1.5% : fill 30min 48% · séance 62% (81/153) · gap 34% · délai 0.0min · rebond 65% (51/81) (MFE +1.83%)
   - −2.0% : fill 30min 42% · séance 57% (74/153) · gap 30% · délai 0.0min · rebond 63% (48/74) (MFE +1.94%)
   - −3.0% : fill 30min 40% · séance 51% (64/153) · gap 26% · délai 0.1min · rebond 65% (44/64) (MFE +2.1%)
   - −4.0% : fill 30min 31% · séance 44% (51/153) · gap 16% · délai 3.5min · rebond 72% (38/51) (MFE +2.39%)
   - −5.0% : fill 30min 18% · séance 38% (42/153) · gap 10% · délai 30.4min · rebond 70% (31/42) (MFE +2.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.71%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −3.29%) → stop au-delà de −2.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −4.01%) → stop au-delà de −2.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=829 jambes) : jambe baissière méd −1.33% (p90 −3.64%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (64/66) · rebond 49% (33/64)
      · −2.0% : fill 90% (55/66) · rebond 53% (31/55)
      · −3.0% : fill 86% (50/66) · rebond 64% (33/50)
      · −4.0% : fill 78% (43/66) · rebond 65% (30/43)
      · −5.0% : fill 68% (36/66) · rebond 62% (25/36)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (75 séances) :
      · −1.0% : fill 33% (17/75) · rebond 88% (15/17)
      · −2.0% : fill 24% (12/75) · rebond 90% (11/12)
      · −3.0% : fill 19% (9/75) · rebond 59% (6/9)
      · −4.0% : fill 16% (6/75) · rebond 100% (6/6)
      · −5.0% : fill 14% (5/75) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=154) : 40% en base · 50% si les 15 1res min sont vertes (79 cas) · 31% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=154) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 72% si début vert vs 18% si rouge (base 40% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.96% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.36% → **scale +1.31% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **18%** (continue à baisser 63%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.23%** (au-delà de la MAE q10 -7.23%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=154) : retour [-3.62% .. +3.04%] · haut q95 +3.69% · bas q05 -4.7%
   - 60min (n=154) : retour [-4.31% .. +5.3%] · haut q95 +5.82% · bas q05 -5.83%
   - 2h (n=154) : retour [-6.14% .. +5.3%] · haut q95 +8.02% · bas q05 -7.41%
   - 4h (n=154) : retour [-6.8% .. +6.73%] · haut q95 +8.44% · bas q05 -8.34%
   - 6h (n=154) : retour [-7.53% .. +7.5%] · haut q95 +8.97% · bas q05 -9.14%
   - session (n=154) : retour [-7.4% .. +7.86%] · haut q95 +8.97% · bas q05 -9.14%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.8% des séances sont trend-up (mild 0% / strong 5.8%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 32.8  _(tendance etablie)_
- **MACD** : hist -8051.503  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 50.9%
- **ATR** : 180357.14 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.191  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 1666300.0 · MA50 2088960.0 · MA200 1212645.28  _(prix < MA20)_
- **Dist MA** : MA20 -14.5% · MA50 -31.8% · MA200 +17.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87426 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
