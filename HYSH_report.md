# 298040

**Generated** : 2026-08-10T00:16:50.127625+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2832000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩2832000.00 (+3.2% vs entrée) · entrée ₩2743450.00 · stop ₩2460235.71 · T1 ₩3058141.05 · R/R 1.11  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.243 _(réel 5 s)_ (GBM 0.137) · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

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

- EV/risk : 0.137 | EV/share : ₩38751.605 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 7 % | T3 3 %
- Kelly (position) : f* 0.054 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.2 | bear 67.0 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.421% → cible +8.905% / stop −4.452%, p_fill 90%, n_eff≈35.9) : P(cible|rempli) **4%** · **EV/risk -0.225** (×p_fill ; si rempli -1.11% du capital)
  - **swing** (entrée dip −3.13% → cible +11.471% / stop −10.323%, p_fill 82%, n_eff≈33.8) : P(cible|rempli) **31%** · **EV/risk -0.243** (×p_fill ; si rempli -3.07% du capital)
  - **deep** (entrée dip −4.829% → cible +43.703% / stop −18.0%, p_fill 82%, n_eff≈32.8) : P(cible|rempli) **0%** · **EV/risk -0.484** (×p_fill ; si rempli -10.66% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→64% · +2.0%→54% · +3.0%→40% · +5.0%→24% · +8.0%→8%
- Range intraday médian 7.06% (p90 10.6%) · excursion haute méd. +2.21% / basse méd. −4.19%
- Profil de vol intra : ouverture 4.574% vs midi 1.186% vs clôture 1.2% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 72% · range 27% · trend ↑0%/↓1% ; spike-down 81% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.145 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. -1.855% ; recovery-V 26%
- **σ réalisé intraday** 5.309% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 66% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 2826800.0 (VA 2801600.0–2841200.0 ; dernier close 2836000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 80% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.36 (high win-rate)
- Gaps overnight (n=149) : méd. 0.89% · baisse 36% (gap-down >1% 24% · >2% 15%)
- Excursion ouverture 5min (n=150) : bas méd −1.47% (p90 −3.44%) · haut méd +0.84% · range méd 2.7%
- Excursion ouverture 15min (n=150) : bas méd −2.08% (p90 −4.61%) · haut méd +1.12% · range méd 3.62%
- Excursion ouverture 30min (n=150) : bas méd −2.52% (p90 −5.11%) · haut méd +1.17% · range méd 4.26%
- Excursion ouverture 60min (n=150) : bas méd −2.69% (p90 −5.37%) · haut méd +1.37% · range méd 4.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2836000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 66% (100/149) · gap 32% · délai 0.0min · rebond 61% (62/100) (MFE +1.28%)
   - −1.0% : fill 30min 55% · séance 64% (92/149) · gap 24% · délai 0.4min · rebond 60% (57/92) (MFE +1.56%)
   - −1.5% : fill 30min 48% · séance 58% (83/149) · gap 20% · délai 1.5min · rebond 53% (50/83) (MFE +1.45%)
   - −2.0% : fill 30min 42% · séance 55% (74/149) · gap 15% · délai 4.5min · rebond 52% (40/74) (MFE +1.25%)
   - −3.0% : fill 30min 32% · séance 47% (61/149) · gap 8% · délai 11.4min · rebond 51% (33/61) (MFE +1.0%)
   - −4.0% : fill 30min 23% · séance 43% (53/149) · gap 5% · délai 27.3min · rebond 67% (38/53) (MFE +1.78%)
   - −5.0% : fill 30min 18% · séance 35% (40/149) · gap 5% · délai 30.3min · rebond 80% (32/40) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.39%) → stop au-delà de −2.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.69%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −3.77%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=817 jambes) : jambe baissière méd −1.43% (p90 −3.58%) · ~14.0 jambes/séance
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
   - **gap-up** (82 séances) :
      · −1.0% : fill 38% (30/82) · rebond 58% (17/30)
      · −2.0% : fill 30% (23/82) · rebond 53% (12/23)
      · −3.0% : fill 22% (15/82) · rebond 45% (7/15)
      · −4.0% : fill 18% (12/82) · rebond 64% (9/12)
      · −5.0% : fill 12% (7/82) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 36% en base · 58% si les 15 1res min sont vertes (61 cas) · 23% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **32min** → P(séance verte=clôture>ouverture) 73% si début vert vs 15% si rouge (base 36% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **73%** · continue >prix actuel 52% ; creux résiduel méd -2.06% (q20 -4.0%) → **SL/trailing à −4.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.64% / q75 +4.02% → **scale +2.64% / runner +4.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.45%** (au-delà de la MAE q10 -6.45%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-4.63% .. +4.33%] · haut q95 +6.19% · bas q05 -5.38%
   - 60min (n=150) : retour [-5.54% .. +5.04%] · haut q95 +7.15% · bas q05 -6.08%
   - 2h (n=150) : retour [-7.46% .. +4.63%] · haut q95 +7.58% · bas q05 -8.31%
   - 4h (n=150) : retour [-7.98% .. +5.44%] · haut q95 +8.31% · bas q05 -9.98%
   - 6h (n=150) : retour [-7.74% .. +5.5%] · haut q95 +8.85% · bas q05 -9.95%
   - session (n=150) : retour [-8.11% .. +5.8%] · haut q95 +8.85% · bas q05 -9.99%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.3% des séances sont trend-up (mild 0% / strong 5.3%) · base = 8 séances trend-up (n_eff 5.4)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88250 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
