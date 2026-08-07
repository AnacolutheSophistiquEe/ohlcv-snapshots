# 298040

**Generated** : 2026-08-07T21:53:04.240688+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2832000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩2832000.00 (+3.2% vs entrée) · entrée ₩2743450.00 · stop ₩2460235.71 · T1 ₩3058141.05 · R/R 1.11  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.298 _(réel 5 s)_ (GBM 0.136) · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2680511.79–₩2806388.21 (mid ₩2743450.00)
- Spot actuel : ₩2832000.00 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : ₩2460235.71 (stop swing_plan-based (-13.13%))
- Targets : T1 ₩3058141.05 · R/R 1.11 | T2 ₩3372832.11 · R/R 2.22 | T3 ₩3687523.16 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2460235.71


## Edge, scénarios & sizing

- EV/risk : 0.136 | EV/share : ₩38481.397 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 7 % | T3 3 %
- Kelly (position) : f* 0.054 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.2 | bear 67.0 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.421% → cible +8.905% / stop −4.452%, p_fill 89%, n_eff≈35.7) : P(cible|rempli) **4%** · **EV/risk -0.247** (×p_fill ; si rempli -1.24% du capital)
  - **swing** (entrée dip −3.13% → cible +11.471% / stop −10.323%, p_fill 81%, n_eff≈33.7) : P(cible|rempli) **27%** · **EV/risk -0.298** (×p_fill ; si rempli -3.81% du capital)
  - **deep** (entrée dip −4.829% → cible +43.703% / stop −18.0%, p_fill 81%, n_eff≈32.7) : P(cible|rempli) **0%** · **EV/risk -0.460** (×p_fill ; si rempli -10.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→64% · +2.0%→54% · +3.0%→40% · +5.0%→24% · +8.0%→8%
- Range intraday médian 7.06% (p90 10.6%) · excursion haute méd. +2.21% / basse méd. −4.19%
- Profil de vol intra : ouverture 4.545% vs midi 1.178% vs clôture 1.191% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 72% · range 27% · trend ↑0%/↓1% ; spike-down 80% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.152 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. -1.936% ; recovery-V 28%
- **σ réalisé intraday** 5.364% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 64% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 2762387.5 (VA 2710337.5–2814437.5 ; dernier close 2712000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 80% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.36 (high win-rate)
- Gaps overnight (n=148) : méd. 0.71% · baisse 37% (gap-down >1% 25% · >2% 15%)
- Excursion ouverture 5min (n=149) : bas méd −1.37% (p90 −3.44%) · haut méd +0.81% · range méd 2.72%
- Excursion ouverture 15min (n=149) : bas méd −2.09% (p90 −4.72%) · haut méd +1.11% · range méd 3.72%
- Excursion ouverture 30min (n=149) : bas méd −2.52% (p90 −5.13%) · haut méd +1.12% · range méd 4.28%
- Excursion ouverture 60min (n=149) : bas méd −2.84% (p90 −5.38%) · haut méd +1.37% · range méd 4.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2712000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (100/148) · gap 32% · délai 0.0min · rebond 61% (62/100) (MFE +1.28%)
   - −1.0% : fill 30min 56% · séance 65% (92/148) · gap 25% · délai 0.4min · rebond 60% (57/92) (MFE +1.56%)
   - −1.5% : fill 30min 49% · séance 59% (83/148) · gap 20% · délai 1.5min · rebond 53% (50/83) (MFE +1.45%)
   - −2.0% : fill 30min 43% · séance 56% (74/148) · gap 15% · délai 4.5min · rebond 52% (40/74) (MFE +1.25%)
   - −3.0% : fill 30min 33% · séance 48% (61/148) · gap 8% · délai 11.4min · rebond 51% (33/61) (MFE +1.0%)
   - −4.0% : fill 30min 24% · séance 44% (53/148) · gap 6% · délai 27.3min · rebond 67% (38/53) (MFE +1.78%)
   - −5.0% : fill 30min 18% · séance 36% (40/148) · gap 5% · délai 30.3min · rebond 80% (32/40) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.45%) → stop au-delà de −2.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.69%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −3.77%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.44% (p90 −3.56%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 100% (51/51) · rebond 61% (32/51)
      · −2.0% : fill 89% (43/51) · rebond 50% (23/43)
      · −3.0% : fill 86% (41/51) · rebond 51% (22/41)
      · −4.0% : fill 82% (36/51) · rebond 72% (26/36)
      · −5.0% : fill 71% (30/51) · rebond 78% (23/30)
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
- **P(clôture VERTE) selon le drive 15min** (n=149) : 36% en base · 58% si les 15 1res min sont vertes (61 cas) · 24% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **57min** → P(séance verte=clôture>ouverture) 78% si début vert vs 14% si rouge (base 36% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -2.2% (q20 -4.69%) → **SL/trailing à −4.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.71% → **scale +1.96% / runner +3.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **14%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.9%** (au-delà de la MAE q10 -5.9%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-4.64% .. +4.37%] · haut q95 +6.21% · bas q05 -5.39%
   - 60min (n=149) : retour [-5.54% .. +5.08%] · haut q95 +7.21% · bas q05 -6.09%
   - 2h (n=149) : retour [-7.48% .. +4.66%] · haut q95 +7.65% · bas q05 -8.39%
   - 4h (n=149) : retour [-7.98% .. +5.44%] · haut q95 +8.31% · bas q05 -10.05%
   - 6h (n=149) : retour [-7.8% .. +5.58%] · haut q95 +8.88% · bas q05 -10.05%
   - session (n=149) : retour [-8.14% .. +5.83%] · haut q95 +8.88% · bas q05 -10.05%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.2  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 76128.733  _(bullish_recent)_
- **BB** : %B 0.7 · largeur 43.0%
- **ATR** : 283214.29 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.063  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 2610400.0 · MA50 3107740.0 · MA200 2675250.45  _(prix > MA20)_
- **Dist MA** : MA20 +8.5% · MA50 -8.9% · MA200 +5.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88125 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
