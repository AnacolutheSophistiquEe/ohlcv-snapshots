# 298040

**Generated** : 2026-07-27T00:15:49.512952+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2681000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩2681000.00 (+0.9% vs entrée) · entrée ₩2656696.49 · stop ₩2556208.80 · T1 ₩2857671.87 · R/R 2.0  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.332 _(réel 5 s)_ (GBM 0.341) · ¼-Kelly 0.021 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.100 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2632392.99–₩2681000.00 (mid ₩2656696.49)
- Spot actuel : ₩2681000.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩2556208.80 (stop swing_plan-based (-4.65%))
- Targets : T1 ₩2857671.87 · R/R 2.0 | T2 ₩3058647.25 · R/R 4.0 | T3 ₩3259622.63 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2556208.80


## Edge, scénarios & sizing

- EV/risk : 0.341 | EV/share : ₩34257.220 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 20 % | T3 5 %
- Kelly (position) : f* 0.085 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.6 | bear 61.4 | side 17.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.49% → cible +3.383% / stop −2.824%, p_fill 96%, n_eff≈38.8) : P(cible|rempli) **31%** · **EV/risk -0.221** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −0.902% → cible +7.565% / stop −3.782%, p_fill 96%, n_eff≈38.1) : P(cible|rempli) **23%** · **EV/risk -0.332** (×p_fill ; si rempli -1.31% du capital)
  - **deep** (entrée dip −1.226% → cible +10.698% / stop −5.349%, p_fill 94%, n_eff≈35.8) : P(cible|rempli) **19%** · **EV/risk -0.441** (×p_fill ; si rempli -2.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→64% · +2.0%→54% · +3.0%→40% · +5.0%→22% · +8.0%→6%
- Range intraday médian 6.88% (p90 9.73%) · excursion haute méd. +2.21% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.289% vs midi 1.052% vs clôture 1.157% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.1)_ ; drift intra méd. -1.467% ; recovery-V 30%
- **σ réalisé intraday** 5.181% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 64% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 2691787.5 (VA 2643987.5–2733612.5 ; dernier close 2685000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 87% · **stop −5.08%** sous le fill (sous le bruit) · cible +2.39% · R/R 0.47 (high win-rate)
- Gaps overnight (n=139) : méd. 0.6% · baisse 38% (gap-down >1% 23% · >2% 16%)
- Excursion ouverture 5min (n=140) : bas méd −1.28% (p90 −3.44%) · haut méd +0.84% · range méd 2.68%
- Excursion ouverture 15min (n=140) : bas méd −1.93% (p90 −4.6%) · haut méd +1.12% · range méd 3.65%
- Excursion ouverture 30min (n=140) : bas méd −2.4% (p90 −4.91%) · haut méd +1.15% · range méd 4.14%
- Excursion ouverture 60min (n=140) : bas méd −2.54% (p90 −5.29%) · haut méd +1.43% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2685000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 70% (95/139) · gap 32% · délai 0.0min · rebond 61% (59/95) (MFE +1.31%)
   - −1.0% : fill 30min 56% · séance 67% (87/139) · gap 23% · délai 0.6min · rebond 60% (54/87) (MFE +1.64%)
   - −1.5% : fill 30min 48% · séance 60% (78/139) · gap 20% · délai 1.3min · rebond 52% (47/78) (MFE +1.29%)
   - −2.0% : fill 30min 43% · séance 56% (69/139) · gap 16% · délai 4.1min · rebond 51% (37/69) (MFE +1.08%)
   - −3.0% : fill 30min 33% · séance 47% (56/139) · gap 7% · délai 6.8min · rebond 54% (31/56) (MFE +1.03%)
   - −4.0% : fill 30min 22% · séance 42% (48/139) · gap 4% · délai 26.4min · rebond 73% (36/48) (MFE +1.89%)
   - −5.0% : fill 30min 18% · séance 34% (36/139) · gap 4% · délai 28.8min · rebond 87% (30/36) (MFE +2.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.19%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −4.17%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −4.2%) → stop au-delà de −2.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=748 jambes) : jambe baissière méd −1.4% (p90 −3.39%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 100% (48/48) · rebond 60% (30/48)
      · −2.0% : fill 87% (40/48) · rebond 54% (22/40)
      · −3.0% : fill 83% (38/48) · rebond 55% (21/38)
      · −4.0% : fill 79% (33/48) · rebond 80% (25/33)
      · −5.0% : fill 66% (27/48) · rebond 90% (22/27)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (75 séances) :
      · −1.0% : fill 42% (28/75) · rebond 59% (16/28)
      · −2.0% : fill 32% (21/75) · rebond 42% (10/21)
      · −3.0% : fill 21% (13/75) · rebond 43% (6/13)
      · −4.0% : fill 16% (10/75) · rebond 71% (8/10)
      · −5.0% : fill 11% (6/75) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 39% en base · 61% si les 15 1res min sont vertes (57 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 78% si début vert vs 14% si rouge (base 39% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.65% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.18% → **scale +1.7% / runner +3.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **14%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.92%** (au-delà de la MAE q10 -4.92%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-4.34% .. +4.25%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=140) : retour [-5.25% .. +4.82%] · haut q95 +6.37% · bas q05 -5.57%
   - 2h (n=140) : retour [-7.08% .. +4.51%] · haut q95 +6.85% · bas q05 -8.11%
   - 4h (n=140) : retour [-7.64% .. +5.31%] · haut q95 +7.53% · bas q05 -9.29%
   - 6h (n=140) : retour [-7.48% .. +5.24%] · haut q95 +8.34% · bas q05 -9.32%
   - session (n=140) : retour [-6.67% .. +5.58%] · haut q95 +8.34% · bas q05 -9.39%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 0% / strong 5.7%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 24% vs absente 0% (base 6%)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.2  _(momentum baissier)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -434.626  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 45.1%
- **ATR** : 251142.86 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.104  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 49.8  _(transition)_
- **MA** : MA20 2951650.0 · MA50 3374860.0 · MA200 2621242.37  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -20.6% · MA200 +2.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88431 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
