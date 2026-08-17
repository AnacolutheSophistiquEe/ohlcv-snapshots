# 298040

**Generated** : 2026-08-17T00:16:48.858596+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2954000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2954000.00 (+5.6% vs entrée) · entrée ₩2798350.00 · stop ₩2532921.43 · T1 ₩3107611.73 · R/R 1.17  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.007 _(réel 5 s)_ (GBM 0.164) · ¼-Kelly 0.016 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2736497.65–₩2860202.35 (mid ₩2798350.00)
- Spot actuel : ₩2954000.00 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : ₩2532921.43 (stop swing_plan-based (-14.25%))
- Targets : T1 ₩3107611.73 · R/R 1.17 | T2 ₩3416873.47 · R/R 2.33 | T3 ₩3726135.20 · R/R 3.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2532921.43


## Edge, scénarios & sizing

- EV/risk : 0.164 | EV/share : ₩43485.301 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 8 % | T3 2 %
- Kelly (position) : f* 0.064 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.0 | bear 20.1 | side 54.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.391% → cible +5.449% / stop −8.0%, p_fill 73%, n_eff≈32.4) : P(cible|rempli) **11%** · **EV/risk -0.064** (×p_fill ; si rempli -0.70% du capital)
  - **swing** (entrée dip −5.264% → cible +11.052% / stop −9.485%, p_fill 64%, n_eff≈24.7) : P(cible|rempli) **30%** · **EV/risk -0.007** (×p_fill ; si rempli -0.10% du capital)
  - **deep** (entrée dip −8.146% → cible +42.885% / stop −18.0%, p_fill 60%, n_eff≈24.6) : P(cible|rempli) **7%** · **EV/risk -0.268** (×p_fill ; si rempli -8.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→60% · +2.0%→50% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 7.04% (p90 10.6%) · excursion haute méd. +1.99% / basse méd. −4.2%
- Profil de vol intra : ouverture 4.59% vs midi 1.151% vs clôture 1.203% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 24% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -1.734% ; recovery-V 20%
- **σ réalisé intraday** 4.848% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 69% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 2912387.5 (VA 2891537.5–2933237.5 ; dernier close 2953000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 81% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.38 (high win-rate)
- Gaps overnight (n=154) : méd. 1.15% · baisse 35% (gap-down >1% 24% · >2% 16%)
- Excursion ouverture 5min (n=155) : bas méd −1.37% (p90 −3.5%) · haut méd +0.81% · range méd 2.67%
- Excursion ouverture 15min (n=155) : bas méd −1.85% (p90 −4.38%) · haut méd +1.11% · range méd 3.42%
- Excursion ouverture 30min (n=155) : bas méd −2.5% (p90 −4.92%) · haut méd +1.12% · range méd 4.19%
- Excursion ouverture 60min (n=155) : bas méd −2.57% (p90 −5.33%) · haut méd +1.36% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2953000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 64% (102/154) · gap 30% · délai 0.0min · rebond 57% (62/102) (MFE +1.27%)
   - −1.0% : fill 30min 53% · séance 62% (94/154) · gap 24% · délai 0.4min · rebond 60% (58/94) (MFE +1.53%)
   - −1.5% : fill 30min 47% · séance 56% (85/154) · gap 20% · délai 1.6min · rebond 53% (51/85) (MFE +1.46%)
   - −2.0% : fill 30min 42% · séance 54% (76/154) · gap 16% · délai 4.5min · rebond 52% (41/76) (MFE +1.27%)
   - −3.0% : fill 30min 31% · séance 46% (63/154) · gap 7% · délai 11.5min · rebond 55% (35/63) (MFE +1.29%)
   - −4.0% : fill 30min 23% · séance 41% (54/154) · gap 5% · délai 25.8min · rebond 68% (39/54) (MFE +1.89%)
   - −5.0% : fill 30min 18% · séance 34% (41/154) · gap 4% · délai 28.7min · rebond 81% (33/41) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.26%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.78% (p90 −3.56%) → stop au-delà de −2.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −3.77%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=836 jambes) : jambe baissière méd −1.43% (p90 −3.56%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 58% (32/52)
      · −2.0% : fill 90% (44/52) · rebond 47% (23/44)
      · −3.0% : fill 87% (42/52) · rebond 54% (23/42)
      · −4.0% : fill 83% (37/52) · rebond 73% (27/37)
      · −5.0% : fill 73% (31/52) · rebond 79% (24/31)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (86 séances) :
      · −1.0% : fill 37% (31/86) · rebond 62% (18/31)
      · −2.0% : fill 30% (24/86) · rebond 58% (13/24)
      · −3.0% : fill 23% (16/86) · rebond 52% (8/16)
      · −4.0% : fill 16% (12/86) · rebond 64% (9/12)
      · −5.0% : fill 10% (7/86) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 32% en base · 53% si les 15 1res min sont vertes (63 cas) · 21% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=155) : COUDE à **46min** → P(séance verte=clôture>ouverture) 71% si début vert vs 14% si rouge (base 32% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **71%** · continue >prix actuel 46% ; creux résiduel méd -1.95% (q20 -3.95%) → **SL/trailing à −3.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +3.64% → **scale +1.78% / runner +3.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.03%** (au-delà de la MAE q10 -6.03%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-4.48% .. +4.3%] · haut q95 +6.12% · bas q05 -5.35%
   - 60min (n=155) : retour [-5.34% .. +4.92%] · haut q95 +6.71% · bas q05 -6.07%
   - 2h (n=155) : retour [-7.31% .. +4.54%] · haut q95 +7.21% · bas q05 -8.18%
   - 4h (n=155) : retour [-7.85% .. +5.36%] · haut q95 +8.06% · bas q05 -9.55%
   - 6h (n=155) : retour [-7.6% .. +5.24%] · haut q95 +8.43% · bas q05 -9.36%
   - session (n=155) : retour [-8.0% .. +5.68%] · haut q95 +8.43% · bas q05 -9.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.2% des séances sont trend-up (mild 0% / strong 5.2%) · base = 8 séances trend-up (n_eff 5.4)
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

- **RSI** : 56.1  _(momentum haussier)_
- **ADX** : 11.5  _(pas de tendance nette)_
- **MACD** : hist 83469.652  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 46.3%
- **ATR** : 265428.57 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.107  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 2645600.0 · MA50 3036680.0 · MA200 2707286.66  _(prix > MA20)_
- **Dist MA** : MA20 +11.7% · MA50 -2.7% · MA200 +9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87201 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
