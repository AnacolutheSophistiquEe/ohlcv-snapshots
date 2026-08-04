# 000660

**Generated** : 2026-08-04T00:13:09.643314+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1567000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1567000.00 (+8.4% vs entrée) · entrée ₩1445079.89 · stop ₩1380172.74 · T1 ₩1522862.73 · R/R 1.2  
> ↳ P(T1 av. stop) 25 % · EV/risk -0.08 · ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.49% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1429523.32–₩1460636.45 (mid ₩1445079.89)
- Spot actuel : ₩1567000.00 (+8.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1380172.74 (stop swing_plan-based (-27.06%))
- Targets : T1 ₩1522862.73 · R/R 1.2 | T2 ₩1600645.58 · R/R 2.4 | T3 ₩1678428.43 · R/R 3.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1380172.74


## Edge, scénarios & sizing

- EV/risk : -0.08 | EV/share : ₩-5158.569 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.066 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.3 | bear 62.1 | side 30.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→80% · +2.0%→55% · +3.0%→40% · +5.0%→28% · +8.0%→14%
- Range intraday médian 6.8% (p90 11.62%) · excursion haute méd. +2.24% / basse méd. −2.8%
- Profil de vol intra : ouverture 3.19% vs midi 1.354% vs clôture 1.579% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 71% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.034)_ ; drift intra méd. -1.521% ; recovery-V 29%
- **σ réalisé intraday** 5.586% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 72% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 1716350.0 (VA 1643750.0–1716350.0 ; dernier close 1718000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 74% · **stop −8.65%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.32 (high win-rate)
- Gaps overnight (n=148) : méd. 0.0% · baisse 49% (gap-down >1% 35% · >2% 29%)
- Excursion ouverture 5min (n=149) : bas méd −0.68% (p90 −2.04%) · haut méd +0.91% · range méd 1.63%
- Excursion ouverture 15min (n=149) : bas méd −0.82% (p90 −2.81%) · haut méd +1.17% · range méd 2.33%
- Excursion ouverture 30min (n=149) : bas méd −1.33% (p90 −3.64%) · haut méd +1.3% · range méd 2.9%
- Excursion ouverture 60min (n=149) : bas méd −1.59% (p90 −4.7%) · haut méd +1.57% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1718000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 68% (94/148) · gap 41% · délai 0.0min · rebond 57% (50/94) (MFE +1.34%)
   - −1.0% : fill 30min 54% · séance 64% (86/148) · gap 35% · délai 0.0min · rebond 66% (54/86) (MFE +1.85%)
   - −1.5% : fill 30min 49% · séance 60% (77/148) · gap 33% · délai 0.0min · rebond 67% (49/77) (MFE +2.24%)
   - −2.0% : fill 30min 42% · séance 55% (70/148) · gap 29% · délai 0.0min · rebond 65% (46/70) (MFE +2.12%)
   - −3.0% : fill 30min 40% · séance 48% (60/148) · gap 24% · délai 0.0min · rebond 71% (43/60) (MFE +2.33%)
   - −4.0% : fill 30min 30% · séance 41% (47/148) · gap 13% · délai 3.4min · rebond 77% (36/47) (MFE +2.5%)
   - −5.0% : fill 30min 16% · séance 34% (38/148) · gap 11% · délai 30.3min · rebond 74% (29/38) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.75%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −3.29%) → stop au-delà de −2.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −4.01%) → stop au-delà de −2.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=795 jambes) : jambe baissière méd −1.36% (p90 −3.57%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (62/64) · rebond 53% (33/62)
      · −2.0% : fill 89% (53/64) · rebond 58% (31/53)
      · −3.0% : fill 84% (48/64) · rebond 70% (33/48)
      · −4.0% : fill 76% (41/64) · rebond 72% (30/41)
      · −5.0% : fill 65% (34/64) · rebond 71% (25/34)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 28% (15/72) · rebond 99% (14/15)
      · −2.0% : fill 19% (10/72) · rebond 85% (9/10)
      · −3.0% : fill 14% (7/72) · rebond 66% (5/7)
      · −4.0% : fill 10% (4/72) · rebond 100% (4/4)
      · −5.0% : fill 7% (3/72) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 44% en base · 50% si les 15 1res min sont vertes (79 cas) · 38% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 72% si début vert vs 22% si rouge (base 44% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.96% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.36% → **scale +1.31% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **22%** (continue à baisser 63%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.24%** (au-delà de la MAE q10 -7.24%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-3.01% .. +3.15%] · haut q95 +3.79% · bas q05 -4.8%
   - 60min (n=149) : retour [-3.38% .. +5.47%] · haut q95 +5.95% · bas q05 -5.51%
   - 2h (n=149) : retour [-4.99% .. +5.4%] · haut q95 +8.18% · bas q05 -6.92%
   - 4h (n=149) : retour [-6.72% .. +6.87%] · haut q95 +8.47% · bas q05 -8.22%
   - 6h (n=149) : retour [-8.04% .. +7.63%] · haut q95 +9.38% · bas q05 -9.79%
   - session (n=149) : retour [-7.7% .. +7.99%] · haut q95 +9.38% · bas q05 -9.79%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.0% des séances sont trend-up (mild 0% / strong 6.0%) · base = 9 séances trend-up (n_eff 7.5)
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

- **RSI** : 43.0  _(momentum baissier)_
- **ADX** : 31.7  _(tendance etablie)_
- **MACD** : hist -33424.759  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 58.2%
- **ATR** : 216357.14 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.271  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 44.9  _(transition)_
- **MA** : MA20 1857500.0 · MA50 2164752.66 · MA200 1180549.95  _(prix < MA20)_
- **Dist MA** : MA20 -15.6% · MA50 -27.6% · MA200 +32.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86338 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
