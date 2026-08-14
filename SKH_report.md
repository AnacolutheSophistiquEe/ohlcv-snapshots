# 000660

**Generated** : 2026-08-14T00:12:21.063960+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1593000.00  

> 🟡 **WAIT-FOR-DIP** — spot +5.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1593000.00 (+5.8% vs entrée) · entrée ₩1506250.00 · stop ₩1400812.50 · T1 ₩1687013.42 · R/R 1.71  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk 0.065 _(réel 5 s)_ (GBM -0.057) · ¼-Kelly 0.049 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −7.0% cohérent avec le bruit 5 s (EV-optimal ≈ −7.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1490788.67–₩1521711.33 (mid ₩1506250.00)
- Spot actuel : ₩1593000.00 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1400812.50 (stop swing_plan-based (-22.54%))
- Targets : T1 ₩1687013.42 · R/R 1.71 | T2 ₩1712240.30 · R/R 1.95 | T3 ₩1737467.19 · R/R 2.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1400812.50


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : ₩-6025.000 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 28 % | T3 28 %
- Kelly (position) : f* 0.195 | ¼-Kelly 0.049 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.4 | bear 62.2 | side 30.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.441% → cible +12.001% / stop −7.0%, p_fill 47%, n_eff≈17.9) : P(cible|rempli) **7%** · **EV/risk +0.065** (×p_fill ; si rempli +0.98% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→52% · +3.0%→40% · +5.0%→28% · +8.0%→14%
- Range intraday médian 7.08% (p90 11.62%) · excursion haute méd. +2.08% / basse méd. −3.11%
- Profil de vol intra : ouverture 3.347% vs midi 1.429% vs clôture 1.627% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (156 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑2%/↓0% ; spike-down 75% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. -1.913% ; recovery-V 25%
- **σ réalisé intraday** 5.292% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 80% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 1431000.0 (VA 1409000.0–1449000.0 ; dernier close 1430000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 70% · **stop −8.33%** sous le fill (sous le bruit) · cible +2.6% · R/R 0.31 (high win-rate)
- Gaps overnight (n=155) : méd. 0.04% · baisse 48% (gap-down >1% 36% · >2% 29%)
- Excursion ouverture 5min (n=156) : bas méd −0.74% (p90 −2.13%) · haut méd +0.8% · range méd 1.75%
- Excursion ouverture 15min (n=156) : bas méd −0.97% (p90 −2.85%) · haut méd +1.05% · range méd 2.42%
- Excursion ouverture 30min (n=156) : bas méd −1.57% (p90 −3.87%) · haut méd +1.23% · range méd 2.94%
- Excursion ouverture 60min (n=156) : bas méd −1.78% (p90 −4.93%) · haut méd +1.42% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1430000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 71% (100/155) · gap 41% · délai 0.0min · rebond 56% (53/100) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 67% (92/155) · gap 36% · délai 0.0min · rebond 63% (57/92) (MFE +1.74%)
   - −1.5% : fill 30min 48% · séance 63% (83/155) · gap 34% · délai 0.0min · rebond 67% (53/83) (MFE +2.17%)
   - −2.0% : fill 30min 42% · séance 56% (75/155) · gap 29% · délai 0.0min · rebond 64% (49/75) (MFE +2.04%)
   - −3.0% : fill 30min 40% · séance 51% (65/155) · gap 24% · délai 0.4min · rebond 66% (45/65) (MFE +2.25%)
   - −4.0% : fill 30min 30% · séance 43% (51/155) · gap 15% · délai 3.5min · rebond 72% (38/51) (MFE +2.39%)
   - −5.0% : fill 30min 18% · séance 37% (42/155) · gap 10% · délai 30.4min · rebond 70% (31/42) (MFE +2.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.61%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −3.08%) → stop au-delà de −2.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −3.9%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=844 jambes) : jambe baissière méd −1.33% (p90 −3.58%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 98% (65/67) · rebond 51% (34/65)
      · −2.0% : fill 90% (56/67) · rebond 55% (32/56)
      · −3.0% : fill 86% (51/67) · rebond 65% (34/51)
      · −4.0% : fill 74% (43/67) · rebond 65% (30/43)
      · −5.0% : fill 65% (36/67) · rebond 62% (25/36)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (76 séances) :
      · −1.0% : fill 35% (18/76) · rebond 89% (16/18)
      · −2.0% : fill 23% (12/76) · rebond 90% (11/12)
      · −3.0% : fill 19% (9/76) · rebond 59% (6/9)
      · −4.0% : fill 16% (6/76) · rebond 100% (6/6)
      · −5.0% : fill 14% (5/76) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=156) : 41% en base · 48% si les 15 1res min sont vertes (80 cas) · 34% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=156) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 41% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.96% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.36% → **scale +1.31% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **20%** (continue à baisser 62%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.13%** (au-delà de la MAE q10 -7.13%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=156) : retour [-3.48% .. +2.98%] · haut q95 +3.68% · bas q05 -4.65%
   - 60min (n=156) : retour [-4.29% .. +5.23%] · haut q95 +5.8% · bas q05 -5.72%
   - 2h (n=156) : retour [-5.72% .. +5.25%] · haut q95 +7.95% · bas q05 -7.4%
   - 4h (n=156) : retour [-6.79% .. +6.68%] · haut q95 +8.43% · bas q05 -8.32%
   - 6h (n=156) : retour [-7.39% .. +7.45%] · haut q95 +8.82% · bas q05 -9.07%
   - session (n=156) : retour [-7.27% .. +7.81%] · haut q95 +8.82% · bas q05 -9.07%


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

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 31.7  _(tendance etablie)_
- **MACD** : hist 13401.981  _(bullish_recent)_
- **BB** : %B 0.46 · largeur 44.3%
- **ATR** : 178142.86 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.24  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 1621400.0 · MA50 2056440.0 · MA200 1223320.92  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -22.5% · MA200 +30.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85912 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
