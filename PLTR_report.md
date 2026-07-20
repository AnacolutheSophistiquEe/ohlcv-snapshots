# PLTR

**Generated** : 2026-07-20T22:01:04.167047+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $134.85  

> 🟡 **WAIT-FOR-DIP** — spot +5.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $134.85 (+5.6% vs entrée) · entrée $127.73 · stop $121.34 · T1 $130.18 · R/R 0.38  
> ↳ P(T1 av. stop) 50 % · EV/risk 0.003 · ¼-Kelly 0.046 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $127.24–$128.22 (mid $127.73)
- Spot actuel : $134.85 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : $121.34 (stop swing_plan-based (-13.51%))
- Targets : T1 $130.18 · R/R 0.38 | T2 $132.64 · R/R 0.77 | T3 $135.09 · R/R 1.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $121.34


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : $0.021 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 12 % | T3 8 %
- Kelly (position) : f* 0.183 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.8 | bear 11.0 | side 75.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 270.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→48% · +3.0%→26% · +5.0%→8% · +8.0%→2%
- Range intraday médian 3.96% (p90 7.33%) · excursion haute méd. +1.9% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.969% vs midi 0.753% vs clôture 0.85% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 54% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.022)_ ; drift intra méd. 0.476% ; recovery-V 41%
- **σ réalisé intraday** 2.794% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 49% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 131.9054 (VA 130.6521–133.4371 ; dernier close 132.34)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 62% · **stop −2.34%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 57% (gap-down >1% 33% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.97%) · haut méd +0.95% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.79%) · haut méd +1.17% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.46%) · haut méd +1.31% · range méd 2.85%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.83%) · haut méd +1.47% · range méd 3.2%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.34 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (118/159) · gap 43% · délai 0.0min · rebond 55% (64/118) (MFE +1.14%)
   - −1.0% : fill 30min 58% · séance 67% (107/159) · gap 33% · délai 0.0min · rebond 60% (61/107) (MFE +1.31%)
   - −1.5% : fill 30min 49% · séance 60% (92/159) · gap 25% · délai 0.1min · rebond 66% (57/92) (MFE +1.57%)
   - −2.0% : fill 30min 41% · séance 52% (76/159) · gap 17% · délai 1.8min · rebond 62% (47/76) (MFE +1.43%)
   - −3.0% : fill 30min 24% · séance 36% (55/159) · gap 8% · délai 4.2min · rebond 53% (26/55) (MFE +1.13%)
   - −4.0% : fill 30min 17% · séance 26% (41/159) · gap 4% · délai 15.3min · rebond 57% (21/41) (MFE +1.31%)
   - −5.0% : fill 30min 11% · séance 19% (28/159) · gap 2% · délai 25.4min · rebond 62% (15/28) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −2.07%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.49%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.07% (p90 −2.53%) · ~7.1 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 95% (67/71) · rebond 65% (41/67)
      · −2.0% : fill 79% (55/71) · rebond 61% (36/55)
      · −3.0% : fill 61% (40/71) · rebond 50% (20/40)
      · −4.0% : fill 47% (31/71) · rebond 56% (16/31)
      · −5.0% : fill 38% (23/71) · rebond 64% (13/23)
   - **flat** (29 séances) :
      · −1.0% : fill 75% (23/29) · rebond 40% (11/23)
      · −2.0% : fill 51% (12/29) · rebond 70% (7/12)
      · −3.0% : fill 39% (10/29) · rebond 75% (5/10)
      · −4.0% : fill 20% (7/29) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/29) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/59) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 69% si les 15 1res min sont vertes (80 cas) · 40% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **42min** → P(séance verte=clôture>ouverture) 79% si début vert vs 27% si rouge (base 55% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -1.28% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.16% → **scale +1.18% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 46%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.25%** (au-delà de la MAE q10 -3.25%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.82% .. +3.67%] · haut q95 +3.95% · bas q05 -4.0%
   - 60min (n=160) : retour [-3.58% .. +3.88%] · haut q95 +4.63% · bas q05 -4.45%
   - 2h (n=160) : retour [-3.85% .. +4.81%] · haut q95 +4.81% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.37% .. +5.63%] · haut q95 +6.0% · bas q05 -5.15%
   - 6h (n=160) : retour [-4.96% .. +5.26%] · haut q95 +6.77% · bas q05 -5.56%
   - session (n=160) : retour [-4.72% .. +4.69%] · haut q95 +6.77% · bas q05 -5.58%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 74.9  _(surachat)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist 1.474  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 28.3%
- **ATR** : 7.07 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.012  _(neutre)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 53.2  _(transition)_
- **MA** : MA20 125.57 · MA50 132.5 · MA200 155.4  _(prix > MA20)_
- **Dist MA** : MA20 +7.4% · MA50 +1.8% · MA200 -13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91077 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
