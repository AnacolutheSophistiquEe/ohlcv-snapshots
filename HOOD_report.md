# HOOD

**Generated** : 2026-07-10T00:32:33.773943+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $115.11  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)  
> ↳ spot $115.11 (+9.5% vs entrée) · entrée $105.15 · stop $102.47 · T1 $110.51 · R/R 2.0  
> ↳ P(T1 av. stop) 32 % · EV/risk -0.005 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $104.08–$106.22 (mid $105.15)
- Spot actuel : $115.11 (+9.5% au-dessus de la zone — repli à attendre)
- Stop : $102.47 (stop swing_plan-based (-10.98%))
- Targets : T1 $110.51 · R/R 2.0 | T2 $115.87 · R/R 4.0 | T3 $121.23 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $102.47


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : $-0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 17 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 30.2 | bear 11.8 | side 58.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 576.0 (= 5 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.928% → cible +6.54% / stop −3.27%, p_fill 20%, n_eff≈10.6) : P(cible|rempli) **7%** · **EV/risk -0.030** (×p_fill ; si rempli -0.51% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→55% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.01% (p90 8.79%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.446% vs midi 1.075% vs clôture 1.055% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 65% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.022)_ ; drift intra méd. 0.936% ; recovery-V 37%
- **σ réalisé intraday** 3.804% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 46% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 111.8168 (VA 109.7003–112.0658 ; dernier close 113.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 85% · **stop −4.78%** sous le fill (sous le bruit) · cible +2.36% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 34% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.85%) · haut méd +0.89% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.84%) · haut méd +1.07% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.51%) · haut méd +1.68% · range méd 3.29%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −3.84%) · haut méd +1.71% · range méd 3.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 113.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (121/159) · gap 41% · délai 0.0min · rebond 57% (61/121) (MFE +1.41%)
   - −1.0% : fill 30min 56% · séance 65% (106/159) · gap 34% · délai 0.0min · rebond 62% (60/106) (MFE +1.32%)
   - −1.5% : fill 30min 48% · séance 60% (98/159) · gap 24% · délai 0.1min · rebond 56% (53/98) (MFE +1.52%)
   - −2.0% : fill 30min 42% · séance 55% (88/159) · gap 15% · délai 0.5min · rebond 65% (52/88) (MFE +1.35%)
   - −3.0% : fill 30min 30% · séance 42% (66/159) · gap 8% · délai 10.7min · rebond 69% (42/66) (MFE +1.81%)
   - −4.0% : fill 30min 18% · séance 31% (50/159) · gap 4% · délai 15.8min · rebond 76% (32/50) (MFE +2.05%)
   - −5.0% : fill 30min 11% · séance 19% (31/159) · gap 1% · délai 22.0min · rebond 85% (25/31) (MFE +2.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.52%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −2.45%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.43%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=750 jambes) : jambe baissière méd −1.16% (p90 −2.66%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 95% (67/71) · rebond 58% (35/67)
      · −2.0% : fill 83% (57/71) · rebond 61% (32/57)
      · −3.0% : fill 70% (46/71) · rebond 66% (28/46)
      · −4.0% : fill 55% (37/71) · rebond 80% (26/37)
      · −5.0% : fill 36% (26/71) · rebond 84% (21/26)
   - **flat** (23 séances) :
      · −1.0% : fill 70% (17/23) · rebond 76% (12/17)
      · −2.0% : fill 54% (12/23) · rebond 59% (7/12)
      · −3.0% : fill 18% (6/23) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/23) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/23) · rebond 82% (2/3)
   - **gap-up** (65 séances) :
      · −1.0% : fill 32% (22/65) · rebond 64% (13/22)
      · −2.0% : fill 26% (19/65) · rebond 82% (13/19)
      · −3.0% : fill 20% (14/65) · rebond 95% (12/14)
      · −4.0% : fill 11% (8/65) · rebond 81% (5/8)
      · −5.0% : fill 4% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (73 cas) · 38% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 83% si début vert vs 21% si rouge (base 52% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 193min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **83%** · continue >prix actuel 61% ; creux résiduel méd -1.26% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.75% / q75 +3.21% → **scale +1.75% / runner +3.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.24%** (au-delà de la MAE q10 -4.24%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +4.77%] · haut q95 +5.23% · bas q05 -4.28%
   - 60min (n=160) : retour [-3.45% .. +4.92%] · haut q95 +6.38% · bas q05 -4.69%
   - 2h (n=160) : retour [-4.05% .. +6.6%] · haut q95 +7.62% · bas q05 -5.35%
   - 4h (n=160) : retour [-4.61% .. +7.55%] · haut q95 +8.53% · bas q05 -6.08%
   - 6h (n=160) : retour [-5.15% .. +7.37%] · haut q95 +8.53% · bas q05 -6.21%
   - session (n=160) : retour [-4.98% .. +7.51%] · haut q95 +8.76% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 10.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **44%**. Lecture précoce 30 min : signature présente → 24% vs absente 5% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.11%) · ~4.0 replis/séance, durée méd 37.3 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.11%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.07% (q75 +9.68% / q95 +13.38%), MFE méd +6.49% / q90 +14.82%
   - Échelle scale-out : +6.49% (33%) / +11.14% (33%) / +14.82% (34%)
- **DÉSARMER** : repli > **−2.11%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=3) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.82% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.6  _(momentum haussier)_
- **ADX** : 28.9  _(tendance etablie)_
- **MACD** : hist 0.919  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 33.8%
- **ATR** : 6.51 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 45.8  _(transition)_
- **MA** : MA20 103.04 · MA50 88.95 · MA200 102.26  _(prix > MA20)_
- **Dist MA** : MA20 +11.7% · MA50 +29.4% · MA200 +12.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91964 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
