# MSTR

**Generated** : 2026-07-10T21:59:48.291091+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $94.64  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $94.64 (+3.5% vs entrée) · entrée $91.43 · stop $86.86 · T1 $94.43 · R/R 0.66  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.088 _(réel 5 s)_ (GBM -0.082) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -55 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.270 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $90.83–$92.03 (mid $91.43)
- Spot actuel : $94.64 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $86.86 (stop swing_plan-based (-10.85%))
- Targets : T1 $94.43 · R/R 0.66 | T2 $97.43 · R/R 1.31 | T3 $100.42 · R/R 1.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $86.86


## Edge, scénarios & sizing

- EV/risk : -0.082 | EV/share : $-0.377 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.0 | bear 81.3 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.39% → cible +3.278% / stop −5.0%, p_fill 39%, n_eff≈16.3) : P(cible|rempli) **24%** · **EV/risk -0.088** (×p_fill ; si rempli -1.14% du capital)
  - **swing** (entrée dip −7.458% → cible +7.331% / stop −3.665%, p_fill 41%, n_eff≈15.4) : P(cible|rempli) **35%** · **EV/risk +0.034** (×p_fill ; si rempli +0.31% du capital)
  - **deep** (entrée dip −11.524% → cible +10.367% / stop −5.184%, p_fill 46%, n_eff≈13.3) : P(cible|rempli) **20%** · **EV/risk -0.189** (×p_fill ; si rempli -2.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→55% · +3.0%→36% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.34% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.84%
- Profil de vol intra : ouverture 3.395% vs midi 1.263% vs clôture 1.288% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.628% ; recovery-V 39%
- **σ réalisé intraday** 4.305% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 64% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 93.9635 (VA 93.1735–94.5165 ; dernier close 93.81)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 68% · **stop −5.2%** sous le fill (sous le bruit) · cible +1.58% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 56% (gap-down >1% 40% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.03% (p90 −2.27%) · haut méd +0.65% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.02%) · haut méd +1.04% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.61%) · haut méd +1.22% · range méd 3.17%
- Excursion ouverture 60min (n=160) : bas méd −1.94% (p90 −4.7%) · haut méd +1.52% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (126/159) · gap 48% · délai 0.0min · rebond 50% (62/126) (MFE +1.17%)
   - −1.0% : fill 30min 65% · séance 76% (120/159) · gap 40% · délai 0.0min · rebond 55% (67/120) (MFE +1.46%)
   - −1.5% : fill 30min 59% · séance 73% (113/159) · gap 30% · délai 0.0min · rebond 56% (67/113) (MFE +1.44%)
   - −2.0% : fill 30min 50% · séance 66% (101/159) · gap 26% · délai 0.2min · rebond 56% (64/101) (MFE +1.32%)
   - −3.0% : fill 30min 36% · séance 55% (78/159) · gap 17% · délai 3.8min · rebond 54% (46/78) (MFE +1.48%)
   - −4.0% : fill 30min 24% · séance 45% (63/159) · gap 8% · délai 23.3min · rebond 56% (37/63) (MFE +1.28%)
   - −5.0% : fill 30min 20% · séance 35% (48/159) · gap 6% · délai 24.2min · rebond 68% (34/48) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.66%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.17% (p90 −2.87%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.36% (p90 −3.07%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=960 jambes) : jambe baissière méd −1.22% (p90 −2.85%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 48% (36/73)
      · −2.0% : fill 90% (66/74) · rebond 50% (38/66)
      · −3.0% : fill 81% (57/74) · rebond 53% (33/57)
      · −4.0% : fill 68% (47/74) · rebond 59% (30/47)
      · −5.0% : fill 56% (38/74) · rebond 70% (28/38)
   - **flat** (18 séances) :
      · −1.0% : fill 88% (17/18) · rebond 82% (11/17)
      · −2.0% : fill 70% (14/18) · rebond 66% (10/14)
      · −3.0% : fill 54% (10/18) · rebond 56% (6/10)
      · −4.0% : fill 34% (7/18) · rebond 12% (2/7)
      · −5.0% : fill 26% (5/18) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (30/67) · rebond 62% (20/30)
      · −2.0% : fill 33% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 22% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 19% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 10% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 52% si les 15 1res min sont vertes (75 cas) · 38% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 73% si début vert vs 21% si rouge (base 44% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -2.31% (q20 -4.04%) → **SL/trailing à −4.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +3.39% → **scale +2.11% / runner +3.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 55%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.48%** (au-delà de la MAE q10 -5.48%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.13%] · haut q95 +5.47% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.0% .. +4.59%] · haut q95 +5.63% · bas q05 -5.45%
   - 2h (n=160) : retour [-4.74% .. +5.69%] · haut q95 +6.85% · bas q05 -5.48%
   - 4h (n=160) : retour [-7.33% .. +8.09%] · haut q95 +9.25% · bas q05 -8.32%
   - 6h (n=160) : retour [-7.05% .. +6.97%] · haut q95 +10.09% · bas q05 -8.32%
   - session (n=160) : retour [-5.91% .. +6.37%] · haut q95 +10.09% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.8  _(momentum baissier)_
- **ADX** : 26.4  _(tendance etablie)_
- **MACD** : hist 1.709  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 54.9%
- **ATR** : 8.8 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.267  _(distribution)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 102.83 · MA50 137.47 · MA200 175.19  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -31.2% · MA200 -46.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90081 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
