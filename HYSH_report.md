# 298040

**Generated** : 2026-08-06T21:53:15.563712+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2737000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩2737000.00 (+1.8% vs entrée) · entrée ₩2688065.86 · stop ₩2397208.72 · T1 ₩2993538.63 · R/R 1.05  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.383 _(réel 5 s)_ (GBM 0.106) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2639131.73–₩2737000.00 (mid ₩2688065.86)
- Spot actuel : ₩2737000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2397208.72 (stop swing_plan-based (-12.41%))
- Targets : T1 ₩2993538.63 · R/R 1.05 | T2 ₩3299011.40 · R/R 2.1 | T3 ₩3604484.18 · R/R 3.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2397208.72


## Edge, scénarios & sizing

- EV/risk : 0.106 | EV/share : ₩30796.618 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 7 % | T3 3 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.7 | bear 65.7 | side 12.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.804% → cible +11.988% / stop −5.994%, p_fill 93%, n_eff≈37.4) : P(cible|rempli) **4%** · **EV/risk -0.213** (×p_fill ; si rempli -1.38% du capital)
  - **swing** (entrée dip −1.783% → cible +11.364% / stop −10.82%, p_fill 93%, n_eff≈37.5) : P(cible|rempli) **23%** · **EV/risk -0.383** (×p_fill ; si rempli -4.45% du capital)
  - **deep** (entrée dip −2.599% → cible +16.071% / stop −16.366%, p_fill 94%, n_eff≈36.2) : P(cible|rempli) **18%** · **EV/risk -0.474** (×p_fill ; si rempli -8.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→62% · +2.0%→52% · +3.0%→39% · +5.0%→24% · +8.0%→8%
- Range intraday médian 7.04% (p90 10.49%) · excursion haute méd. +2.14% / basse méd. −4.06%
- Profil de vol intra : ouverture 4.473% vs midi 1.169% vs clôture 1.179% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 73% · range 26% · trend ↑0%/↓1% ; spike-down 80% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.076)_ ; drift intra méd. -1.63% ; recovery-V 29%
- **σ réalisé intraday** 5.361% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 63% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 2997868.75 (VA 2927343.75–3012981.25 ; dernier close 2999000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 84% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.37 (high win-rate)
- Gaps overnight (n=147) : méd. 0.89% · baisse 36% (gap-down >1% 23% · >2% 16%)
- Excursion ouverture 5min (n=148) : bas méd −1.47% (p90 −3.44%) · haut méd +0.81% · range méd 2.73%
- Excursion ouverture 15min (n=148) : bas méd −2.19% (p90 −4.75%) · haut méd +1.03% · range méd 3.77%
- Excursion ouverture 30min (n=148) : bas méd −2.52% (p90 −5.13%) · haut méd +1.11% · range méd 4.26%
- Excursion ouverture 60min (n=148) : bas méd −2.69% (p90 −5.41%) · haut méd +1.34% · range méd 4.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2999000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 67% (99/147) · gap 31% · délai 0.0min · rebond 60% (61/99) (MFE +1.27%)
   - −1.0% : fill 30min 55% · séance 64% (91/147) · gap 23% · délai 0.6min · rebond 59% (56/91) (MFE +1.55%)
   - −1.5% : fill 30min 48% · séance 58% (82/147) · gap 21% · délai 1.3min · rebond 52% (49/82) (MFE +1.29%)
   - −2.0% : fill 30min 42% · séance 55% (73/147) · gap 16% · délai 4.2min · rebond 54% (40/73) (MFE +1.29%)
   - −3.0% : fill 30min 32% · séance 47% (60/147) · gap 8% · délai 10.1min · rebond 53% (33/60) (MFE +1.03%)
   - −4.0% : fill 30min 22% · séance 43% (52/147) · gap 6% · délai 26.4min · rebond 65% (37/52) (MFE +1.62%)
   - −5.0% : fill 30min 19% · séance 34% (39/147) · gap 5% · délai 28.8min · rebond 84% (32/39) (MFE +2.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.51%) → stop au-delà de −2.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.77% (p90 −3.82%) → stop au-delà de −2.49% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.83% (p90 −4.03%) → stop au-delà de −2.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=804 jambes) : jambe baissière méd −1.43% (p90 −3.56%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 59% (31/50)
      · −2.0% : fill 89% (42/50) · rebond 54% (23/42)
      · −3.0% : fill 85% (40/50) · rebond 54% (22/40)
      · −4.0% : fill 81% (35/50) · rebond 70% (25/35)
      · −5.0% : fill 69% (29/50) · rebond 84% (23/29)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (81 séances) :
      · −1.0% : fill 40% (30/81) · rebond 58% (17/30)
      · −2.0% : fill 32% (23/81) · rebond 53% (12/23)
      · −3.0% : fill 23% (15/81) · rebond 45% (7/15)
      · −4.0% : fill 19% (12/81) · rebond 64% (9/12)
      · −5.0% : fill 12% (7/81) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 37% en base · 62% si les 15 1res min sont vertes (60 cas) · 24% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=148) : COUDE à **57min** → P(séance verte=clôture>ouverture) 78% si début vert vs 14% si rouge (base 37% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -2.2% (q20 -4.69%) → **SL/trailing à −4.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.71% → **scale +1.96% / runner +3.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **14%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.78%** (au-delà de la MAE q10 -5.78%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-4.66% .. +4.44%] · haut q95 +6.23% · bas q05 -5.4%
   - 60min (n=148) : retour [-5.54% .. +5.15%] · haut q95 +7.27% · bas q05 -6.09%
   - 2h (n=148) : retour [-7.5% .. +4.68%] · haut q95 +7.72% · bas q05 -8.48%
   - 4h (n=148) : retour [-7.99% .. +5.45%] · haut q95 +8.32% · bas q05 -10.09%
   - 6h (n=148) : retour [-7.86% .. +5.65%] · haut q95 +8.91% · bas q05 -10.09%
   - session (n=148) : retour [-6.99% .. +5.85%] · haut q95 +8.91% · bas q05 -10.09%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.4% des séances sont trend-up (mild 0% / strong 5.4%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 20% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.1  _(neutre)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist 67152.044  _(bullish_recent)_
- **BB** : %B 0.61 · largeur 42.8%
- **ATR** : 290857.14 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.061  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 45.6  _(transition)_
- **MA** : MA20 2608750.0 · MA50 3125300.0 · MA200 2669400.44  _(prix > MA20)_
- **Dist MA** : MA20 +4.9% · MA50 -12.4% · MA200 +2.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87948 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
