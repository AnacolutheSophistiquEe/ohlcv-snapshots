# SMCI

**Generated** : 2026-07-24T00:21:14.993299+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $31.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $31.20 (+4.8% vs entrée) · entrée $29.76 · stop $28.85 · T1 $31.58 · R/R 2.0  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.068 _(réel 5 s)_ (GBM 0.053) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.06% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $29.56–$29.95 (mid $29.76)
- Spot actuel : $31.20 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : $28.85 (stop swing_plan-based (-13.45%))
- Targets : T1 $31.58 · R/R 2.0 | T2 $32.13 · R/R 2.6 | T3 $32.68 · R/R 3.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $28.85


## Edge, scénarios & sizing

- EV/risk : 0.053 | EV/share : $0.048 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.102 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.4 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 374.0 (= 12 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.621% → cible +6.119% / stop −3.06%, p_fill 27%, n_eff≈12.3) : P(cible|rempli) **0%** · **EV/risk -0.068** (×p_fill ; si rempli -0.75% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→64% · +3.0%→46% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.14%) · excursion haute méd. +2.68% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.891% vs midi 1.199% vs clôture 1.543% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. -0.234% ; recovery-V 21%
- **σ réalisé intraday** 3.987% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 63% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 30.8595 (VA 30.6775–31.6785 ; dernier close 30.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 73% · **stop −4.4%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 43% (gap-down >1% 31% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.16%) · haut méd +0.92% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −3.21%) · haut méd +1.36% · range méd 2.72%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.78%) · haut méd +1.45% · range méd 3.57%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −4.34%) · haut méd +1.58% · range méd 4.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (125/159) · gap 38% · délai 0.0min · rebond 59% (73/125) (MFE +1.32%)
   - −1.0% : fill 30min 56% · séance 70% (113/159) · gap 31% · délai 0.0min · rebond 59% (64/113) (MFE +1.23%)
   - −1.5% : fill 30min 45% · séance 62% (97/159) · gap 23% · délai 0.5min · rebond 62% (58/97) (MFE +1.42%)
   - −2.0% : fill 30min 41% · séance 54% (87/159) · gap 20% · délai 1.1min · rebond 64% (54/87) (MFE +1.59%)
   - −3.0% : fill 30min 26% · séance 48% (70/159) · gap 13% · délai 18.9min · rebond 59% (42/70) (MFE +1.62%)
   - −4.0% : fill 30min 20% · séance 38% (51/159) · gap 10% · délai 15.8min · rebond 67% (31/51) (MFE +1.62%)
   - −5.0% : fill 30min 17% · séance 32% (42/159) · gap 6% · délai 19.0min · rebond 73% (28/42) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −2.47%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −3.03%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.13%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=840 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 94% (66/68) · rebond 48% (35/66)
      · −2.0% : fill 88% (59/68) · rebond 59% (33/59)
      · −3.0% : fill 82% (52/68) · rebond 56% (30/52)
      · −4.0% : fill 69% (41/68) · rebond 67% (25/41)
      · −5.0% : fill 57% (34/68) · rebond 70% (22/34)
   - **flat** (15 séances) :
      · −1.0% : fill 94% (13/15) · rebond 87% (10/13)
      · −2.0% : fill 43% (8/15) · rebond 76% (5/8)
      · −3.0% : fill 10% (2/15) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/15) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/15) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 47% (34/76) · rebond 71% (19/34)
      · −2.0% : fill 27% (20/76) · rebond 74% (16/20)
      · −3.0% : fill 25% (16/76) · rebond 65% (10/16)
      · −4.0% : fill 16% (9/76) · rebond 65% (5/9)
      · −5.0% : fill 15% (8/76) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 67% si les 15 1res min sont vertes (75 cas) · 23% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 77% si début vert vs 12% si rouge (base 45% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **77%** · continue >prix actuel 47% ; creux résiduel méd -1.68% (q20 -3.04%) → **SL/trailing à −3.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +2.99% → **scale +1.63% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **12%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.1% .. +5.21%] · haut q95 +6.78% · bas q05 -4.35%
   - 60min (n=160) : retour [-4.19% .. +5.65%] · haut q95 +6.78% · bas q05 -5.45%
   - 2h (n=160) : retour [-4.78% .. +6.81%] · haut q95 +8.55% · bas q05 -5.82%
   - 4h (n=160) : retour [-5.36% .. +7.54%] · haut q95 +8.97% · bas q05 -6.94%
   - 6h (n=160) : retour [-6.47% .. +6.97%] · haut q95 +10.09% · bas q05 -8.03%
   - session (n=160) : retour [-7.23% .. +7.86%] · haut q95 +10.09% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.4  _(momentum haussier)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist 0.574  _(bullish_recent)_
- **BB** : %B 0.89 · largeur 31.9%
- **ATR** : 1.91 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.205  _(distribution)_
- **Vol ratio** : 1.75  _(volume au-dessus de la moyenne)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 27.75 · MA50 32.79 · MA200 33.59  _(prix > MA20)_
- **Dist MA** : MA20 +12.4% · MA50 -4.8% · MA200 -7.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91618 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
