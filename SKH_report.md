# 000660

**Generated** : 2026-08-19T00:13:15.803665+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1662000.00  

> 🟡 **WAIT-FOR-DIP** — spot +16.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1662000.00 (+16.0% vs entrée) · entrée ₩1433200.00 · stop ₩1261216.00 · T1 ₩1855000.00 · R/R 2.45  
> ↳ P(T1 av. stop) 6 % · EV/risk 0.236 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1401553.52–₩1464846.48 (mid ₩1433200.00)
- Spot actuel : ₩1662000.00 (+16.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1261216.00 (stop swing_plan-based (-24.11%))
- Targets : T1 ₩1855000.00 · R/R 2.45 | T2 ₩1880729.35 · R/R 2.6 | T3 ₩1906458.69 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1261216.00


## Edge, scénarios & sizing

- EV/risk : 0.295 | EV/share : ₩50680.964 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 3 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.5 | bear 62.8 | side 25.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.259% → cible +8.281% / stop −4.14%, p_fill 33%, n_eff≈14.0) : P(cible|rempli) **8%** · **EV/risk +0.081** (×p_fill ; si rempli +1.00% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→79% · +2.0%→54% · +3.0%→41% · +5.0%→29% · +8.0%→14%
- Range intraday médian 7.15% (p90 11.62%) · excursion haute méd. +2.16% / basse méd. −3.11%
- Profil de vol intra : ouverture 3.361% vs midi 1.447% vs clôture 1.651% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 72% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -1.662% ; recovery-V 27%
- **σ réalisé intraday** 5.022% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 74% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1642387.5 (VA 1635487.5–1656187.5 ; dernier close 1643000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 70% · **stop −8.33%** sous le fill (sous le bruit) · cible +2.6% · R/R 0.31 (high win-rate)
- Gaps overnight (n=158) : méd. 0.59% · baisse 45% (gap-down >1% 34% · >2% 27%)
- Excursion ouverture 5min (n=159) : bas méd −0.79% (p90 −2.13%) · haut méd +0.79% · range méd 1.74%
- Excursion ouverture 15min (n=159) : bas méd −1.01% (p90 −2.79%) · haut méd +1.03% · range méd 2.37%
- Excursion ouverture 30min (n=159) : bas méd −1.57% (p90 −3.77%) · haut méd +1.26% · range méd 2.93%
- Excursion ouverture 60min (n=159) : bas méd −1.75% (p90 −4.93%) · haut méd +1.47% · range méd 3.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1643000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 67% (100/158) · gap 39% · délai 0.0min · rebond 56% (53/100) (MFE +1.23%)
   - −1.0% : fill 30min 51% · séance 63% (92/158) · gap 34% · délai 0.0min · rebond 63% (57/92) (MFE +1.74%)
   - −1.5% : fill 30min 46% · séance 60% (83/158) · gap 32% · délai 0.0min · rebond 67% (53/83) (MFE +2.17%)
   - −2.0% : fill 30min 40% · séance 53% (75/158) · gap 27% · délai 0.0min · rebond 64% (49/75) (MFE +2.04%)
   - −3.0% : fill 30min 38% · séance 48% (65/158) · gap 23% · délai 0.4min · rebond 66% (45/65) (MFE +2.25%)
   - −4.0% : fill 30min 28% · séance 40% (51/158) · gap 14% · délai 3.5min · rebond 72% (38/51) (MFE +2.39%)
   - −5.0% : fill 30min 17% · séance 35% (42/158) · gap 9% · délai 30.4min · rebond 70% (31/42) (MFE +2.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.52%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.75% (p90 −3.04%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −3.79%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=857 jambes) : jambe baissière méd −1.33% (p90 −3.56%) · ~13.0 jambes/séance
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
   - **gap-up** (79 séances) :
      · −1.0% : fill 31% (18/79) · rebond 89% (16/18)
      · −2.0% : fill 21% (12/79) · rebond 90% (11/12)
      · −3.0% : fill 17% (9/79) · rebond 59% (6/9)
      · −4.0% : fill 14% (6/79) · rebond 100% (6/6)
      · −5.0% : fill 12% (5/79) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 42% en base · 50% si les 15 1res min sont vertes (81 cas) · 35% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 42% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **73%** · continue >prix actuel 45% ; creux résiduel méd -1.99% (q20 -6.15%) → **SL/trailing à −6.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +3.31% → **scale +1.32% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **22%** (continue à baisser 61%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.89%** (au-delà de la MAE q10 -6.89%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-3.37% .. +2.9%] · haut q95 +3.67% · bas q05 -4.57%
   - 60min (n=159) : retour [-4.21% .. +5.09%] · haut q95 +5.77% · bas q05 -5.63%
   - 2h (n=159) : retour [-5.07% .. +5.16%] · haut q95 +7.9% · bas q05 -7.37%
   - 4h (n=159) : retour [-6.78% .. +6.48%] · haut q95 +8.34% · bas q05 -8.29%
   - 6h (n=159) : retour [-7.16% .. +7.23%] · haut q95 +8.58% · bas q05 -8.98%
   - session (n=159) : retour [-7.13% .. +7.62%] · haut q95 +8.58% · bas q05 -8.98%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 0% / strong 5.7%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 16% vs absente 1% (base 6%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 54.1  _(neutre)_
- **ADX** : 28.9  _(tendance etablie)_
- **MACD** : hist 34397.881  _(bullish_recent)_
- **BB** : %B 0.58 · largeur 42.1%
- **ATR** : 169285.71 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.233  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 1606450.0 · MA50 2035220.0 · MA200 1235068.99  _(prix > MA20)_
- **Dist MA** : MA20 +3.5% · MA50 -18.3% · MA200 +34.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86266 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
