# MSTR

**Generated** : 2026-07-22T00:21:35.246445+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $101.95  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $101.95 (+3.0% vs entrée) · entrée $98.97 · stop $94.51 · T1 $104.47 · R/R 1.23  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk -0.038 _(réel 5 s)_ (GBM -0.039) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $98.34–$99.59 (mid $98.97)
- Spot actuel : $101.95 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $94.51 (stop swing_plan-based (-9.74%))
- Targets : T1 $104.47 · R/R 1.23 | T2 $106.40 · R/R 1.67 | T3 $108.33 · R/R 2.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $94.51


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : $-0.172 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.2 | bear 64.4 | side 26.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 102.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.922% → cible +5.565% / stop −4.5%, p_fill 40%, n_eff≈19.7) : P(cible|rempli) **17%** · **EV/risk -0.038** (×p_fill ; si rempli -0.43% du capital)
  - **swing** (entrée dip −6.44% → cible +7.054% / stop −3.527%, p_fill 39%, n_eff≈17.4) : P(cible|rempli) **34%** · **EV/risk +0.004** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −9.948% → cible +9.976% / stop −4.988%, p_fill 38%, n_eff≈16.7) : P(cible|rempli) **18%** · **EV/risk -0.189** (×p_fill ; si rempli -2.50% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→75% · +2.0%→60% · +3.0%→39% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.61% (p90 9.85%) · excursion haute méd. +2.54% / basse méd. −2.64%
- Profil de vol intra : ouverture 3.423% vs midi 1.286% vs clôture 1.317% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.297% ; recovery-V 38%
- **σ réalisé intraday** 4.099% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 59% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 99.6006 (VA 97.2766–100.6174 ; dernier close 97.81)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 68% · **stop −5.19%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 53% (gap-down >1% 40% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.12%) · haut méd +0.76% · range méd 1.79%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −2.9%) · haut méd +1.12% · range méd 2.53%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.48%) · haut méd +1.37% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.85% (p90 −4.23%) · haut méd +1.5% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (126/159) · gap 47% · délai 0.0min · rebond 52% (62/126) (MFE +1.41%)
   - −1.0% : fill 30min 63% · séance 74% (120/159) · gap 40% · délai 0.0min · rebond 56% (67/120) (MFE +1.36%)
   - −1.5% : fill 30min 56% · séance 68% (111/159) · gap 32% · délai 0.0min · rebond 54% (64/111) (MFE +1.32%)
   - −2.0% : fill 30min 48% · séance 62% (100/159) · gap 26% · délai 0.2min · rebond 60% (64/100) (MFE +1.23%)
   - −3.0% : fill 30min 37% · séance 53% (78/159) · gap 18% · délai 2.0min · rebond 58% (47/78) (MFE +1.52%)
   - −4.0% : fill 30min 24% · séance 44% (64/159) · gap 7% · délai 17.3min · rebond 61% (38/64) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 30% (46/159) · gap 5% · délai 24.1min · rebond 68% (32/46) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.29%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.16% (p90 −2.82%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.26% (p90 −2.81%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=968 jambes) : jambe baissière méd −1.2% (p90 −2.78%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 47% (35/72)
      · −2.0% : fill 91% (65/73) · rebond 56% (38/65)
      · −3.0% : fill 84% (57/73) · rebond 59% (34/57)
      · −4.0% : fill 71% (48/73) · rebond 65% (31/48)
      · −5.0% : fill 50% (36/73) · rebond 70% (26/36)
   - **flat** (19 séances) :
      · −1.0% : fill 90% (18/19) · rebond 85% (12/18)
      · −2.0% : fill 60% (14/19) · rebond 66% (10/14)
      · −3.0% : fill 46% (10/19) · rebond 56% (6/10)
      · −4.0% : fill 29% (7/19) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/19) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 40% (30/67) · rebond 66% (20/30)
      · −2.0% : fill 28% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 18% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 16% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 53% si les 15 1res min sont vertes (74 cas) · 38% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 72% si début vert vs 15% si rouge (base 45% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **72%** · continue >prix actuel 59% ; creux résiduel méd -1.73% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +3.15% → **scale +2.01% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **15%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.49%** (au-delà de la MAE q10 -5.49%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +4.0%] · haut q95 +4.99% · bas q05 -4.13%
   - 60min (n=160) : retour [-4.9% .. +3.87%] · haut q95 +5.41% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.74% .. +5.62%] · haut q95 +6.54% · bas q05 -5.28%
   - 4h (n=160) : retour [-7.33% .. +7.91%] · haut q95 +9.02% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.66% .. +6.9%] · haut q95 +9.78% · bas q05 -8.32%
   - session (n=160) : retour [-5.87% .. +6.24%] · haut q95 +9.78% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 10% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.3  _(momentum haussier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 2.662  _(pas de croisement recent)_
- **BB** : %B 0.83 · largeur 22.9%
- **ATR** : 6.79 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.176  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 61.8  _(marche en range (choppy))_
- **MA** : MA20 94.79 · MA50 126.22 · MA200 167.33  _(prix > MA20)_
- **Dist MA** : MA20 +7.6% · MA50 -19.2% · MA200 -39.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93095 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
