# 000660

**Generated** : 2026-07-15T21:49:46.111906+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2116000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2116000.00 (+1.1% vs entrée) · entrée ₩2091958.31 · stop ₩2014751.16 · T1 ₩2187297.52 · R/R 1.23  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.212 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.69% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2072890.46–₩2111026.15 (mid ₩2091958.31)
- Spot actuel : ₩2116000.00 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2014751.16 (stop swing_plan-based (-7.47%))
- Targets : T1 ₩2187297.52 · R/R 1.23 | T2 ₩2282636.74 · R/R 2.47 | T3 ₩2377975.96 · R/R 3.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2014751.16


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : ₩-1292.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.1 | bear 62.3 | side 8.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.131% → cible +4.557% / stop −3.691%, p_fill 78%, n_eff≈28.8) : P(cible|rempli) **24%** · **EV/risk -0.212** (×p_fill ; si rempli -1.00% du capital)
  - **swing** (entrée dip −2.502% → cible +10.191% / stop −5.095%, p_fill 71%, n_eff≈24.9) : P(cible|rempli) **27%** · **EV/risk -0.160** (×p_fill ; si rempli -1.15% du capital)
  - **deep** (entrée dip −3.862% → cible +14.412% / stop −7.206%, p_fill 59%, n_eff≈19.2) : P(cible|rempli) **31%** · **EV/risk -0.099** (×p_fill ; si rempli -1.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→81% · +2.0%→56% · +3.0%→38% · +5.0%→22% · +8.0%→12%
- Range intraday médian 6.05% (p90 10.58%) · excursion haute méd. +2.25% / basse méd. −2.5%
- Profil de vol intra : ouverture 2.798% vs midi 1.143% vs clôture 1.385% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑3%/↓0% ; spike-down 64% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.083% ; recovery-V 28%
- **σ réalisé intraday** 4.754% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 66% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 2203700.0 (VA 2196900.0–2251300.0 ; dernier close 2197500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 46% · rebond 84% · **stop −7.45%** sous le fill (sous le bruit) · cible +2.69% · R/R 0.36 (high win-rate)
- Gaps overnight (n=133) : méd. 0.02% · baisse 50% (gap-down >1% 36% · >2% 28%)
- Excursion ouverture 5min (n=134) : bas méd −0.47% (p90 −1.31%) · haut méd +0.99% · range méd 1.49%
- Excursion ouverture 15min (n=134) : bas méd −0.77% (p90 −2.12%) · haut méd +1.18% · range méd 2.03%
- Excursion ouverture 30min (n=134) : bas méd −1.04% (p90 −3.02%) · haut méd +1.3% · range méd 2.64%
- Excursion ouverture 60min (n=134) : bas méd −1.28% (p90 −3.49%) · haut méd +1.71% · range méd 3.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2197500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 65% (82/133) · gap 40% · délai 0.0min · rebond 56% (43/82) (MFE +1.35%)
   - −1.0% : fill 30min 54% · séance 61% (75/133) · gap 36% · délai 0.0min · rebond 66% (47/75) (MFE +1.8%)
   - −1.5% : fill 30min 48% · séance 57% (67/133) · gap 33% · délai 0.0min · rebond 69% (43/67) (MFE +1.84%)
   - −2.0% : fill 30min 39% · séance 50% (60/133) · gap 28% · délai 0.0min · rebond 67% (40/60) (MFE +1.85%)
   - −3.0% : fill 30min 38% · séance 46% (52/133) · gap 21% · délai 6.1min · rebond 84% (40/52) (MFE +2.69%)
   - −4.0% : fill 30min 25% · séance 37% (39/133) · gap 11% · délai 12.3min · rebond 77% (30/39) (MFE +2.75%)
   - −5.0% : fill 30min 10% · séance 28% (30/133) · gap 8% · délai 32.1min · rebond 74% (23/30) (MFE +2.41%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −2.71%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −3.04%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −3.27%) → stop au-delà de −1.74% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=653 jambes) : jambe baissière méd −1.29% (p90 −3.39%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (55/57) · rebond 56% (30/55)
      · −2.0% : fill 85% (46/57) · rebond 64% (28/46)
      · −3.0% : fill 79% (41/57) · rebond 81% (30/41)
      · −4.0% : fill 68% (34/57) · rebond 73% (25/34)
      · −5.0% : fill 53% (27/57) · rebond 70% (20/27)
   - **flat** (11 séances) :
      · −1.0% : fill 88% (8/11) · rebond 81% (6/8)
      · −2.0% : fill 70% (6/11) · rebond 80% (5/6)
      · −3.0% : fill 60% (5/11) · rebond 100% (5/5)
      · −4.0% : fill 31% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 14% (1/11) · rebond 100% (1/1)
   - **gap-up** (65 séances) :
      · −1.0% : fill 24% (12/65) · rebond 98% (11/12)
      · −2.0% : fill 15% (8/65) · rebond 75% (7/8)
      · −3.0% : fill 13% (6/65) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/65) · rebond 100% (3/3)
      · −5.0% : fill 5% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 48% en base · 55% si les 15 1res min sont vertes (72 cas) · 38% si rouges (62 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=134) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 73% si début vert vs 20% si rouge (base 48% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 48% ; creux résiduel méd -1.44% (q20 -4.98%) → **SL/trailing à −4.98%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +3.53% → **scale +1.28% / runner +3.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=60) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.16%** (au-delà de la MAE q10 -6.16%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-2.94% .. +3.07%] · haut q95 +3.72% · bas q05 -3.65%
   - 60min (n=134) : retour [-3.38% .. +5.76%] · haut q95 +5.84% · bas q05 -4.92%
   - 2h (n=134) : retour [-4.12% .. +5.86%] · haut q95 +8.06% · bas q05 -5.6%
   - 4h (n=134) : retour [-5.08% .. +7.25%] · haut q95 +8.65% · bas q05 -7.18%
   - 6h (n=134) : retour [-6.2% .. +7.84%] · haut q95 +9.92% · bas q05 -8.54%
   - session (n=134) : retour [-5.34% .. +8.16%] · haut q95 +9.92% · bas q05 -8.65%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.7% des séances sont trend-up (mild 0% / strong 6.7%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 30.8  _(momentum baissier)_
- **ADX** : 26.9  _(tendance etablie)_
- **MACD** : hist -80455.209  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 52.8%
- **ATR** : 257357.14 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.111  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 2422200.0 · MA50 2182841.78 · MA200 1100299.57  _(prix < MA20)_
- **Dist MA** : MA20 -12.6% · MA50 -3.1% · MA200 +92.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86904 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
