# MSTR

**Generated** : 2026-07-22T21:57:30.503653+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $100.01  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $100.01 (+5.8% vs entrée) · entrée $94.52 · stop $91.24 · T1 $101.06 · R/R 1.99  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.137 _(réel 5 s)_ (GBM -0.233) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 144 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $93.21–$95.83 (mid $94.52)
- Spot actuel : $100.01 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : $91.24 (stop swing_plan-based (-8.77%))
- Targets : T1 $101.06 · R/R 1.99 | T2 $107.61 · R/R 3.99 | T3 $114.16 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $91.24


## Edge, scénarios & sizing

- EV/risk : -0.233 | EV/share : $-0.763 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.4 | bear 53.1 | side 24.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 100.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.499% → cible +7.14% / stop −3.57%, p_fill 47%, n_eff≈22.8) : P(cible|rempli) **5%** · **EV/risk -0.061** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −5.496% → cible +6.928% / stop −3.464%, p_fill 43%, n_eff≈18.1) : P(cible|rempli) **21%** · **EV/risk -0.137** (×p_fill ; si rempli -1.11% du capital)
  - **deep** (entrée dip −8.487% → cible +9.798% / stop −4.899%, p_fill 44%, n_eff≈19.4) : P(cible|rempli) **24%** · **EV/risk -0.120** (×p_fill ; si rempli -1.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→75% · +2.0%→61% · +3.0%→40% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.48% (p90 9.85%) · excursion haute méd. +2.63% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.441% vs midi 1.256% vs clôture 1.318% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.256% ; recovery-V 41%
- **σ réalisé intraday** 4.064% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 60% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 101.5091 (VA 100.1321–102.5419 ; dernier close 101.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 68% · **stop −5.19%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 52% (gap-down >1% 39% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.96% (p90 −2.11%) · haut méd +0.76% · range méd 1.76%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −2.89%) · haut méd +1.09% · range méd 2.51%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.47%) · haut méd +1.38% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.8% (p90 −4.23%) · haut méd +1.57% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 101.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (125/159) · gap 46% · délai 0.0min · rebond 52% (61/125) (MFE +1.4%)
   - −1.0% : fill 30min 62% · séance 73% (119/159) · gap 39% · délai 0.0min · rebond 56% (66/119) (MFE +1.36%)
   - −1.5% : fill 30min 55% · séance 67% (110/159) · gap 31% · délai 0.0min · rebond 54% (63/110) (MFE +1.31%)
   - −2.0% : fill 30min 47% · séance 61% (99/159) · gap 26% · délai 0.2min · rebond 60% (63/99) (MFE +1.23%)
   - −3.0% : fill 30min 36% · séance 52% (77/159) · gap 18% · délai 2.0min · rebond 58% (46/77) (MFE +1.52%)
   - −4.0% : fill 30min 24% · séance 44% (64/159) · gap 7% · délai 17.3min · rebond 61% (38/64) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 30% (46/159) · gap 5% · délai 24.1min · rebond 68% (32/46) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.29%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.82%) → stop au-delà de −2.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.15% (p90 −2.79%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=970 jambes) : jambe baissière méd −1.2% (p90 −2.76%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 47% (35/72)
      · −2.0% : fill 91% (65/73) · rebond 56% (38/65)
      · −3.0% : fill 84% (57/73) · rebond 59% (34/57)
      · −4.0% : fill 71% (48/73) · rebond 65% (31/48)
      · −5.0% : fill 50% (36/73) · rebond 70% (26/36)
   - **flat** (18 séances) :
      · −1.0% : fill 90% (17/18) · rebond 84% (11/17)
      · −2.0% : fill 59% (13/18) · rebond 65% (9/13)
      · −3.0% : fill 45% (9/18) · rebond 55% (5/9)
      · −4.0% : fill 29% (7/18) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/18) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 38% (30/68) · rebond 66% (20/30)
      · −2.0% : fill 26% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 17% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 16% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 53% si les 15 1res min sont vertes (74 cas) · 40% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 73% si début vert vs 15% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **73%** · continue >prix actuel 57% ; creux résiduel méd -1.75% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.13% → **scale +1.96% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **15%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.49%** (au-delà de la MAE q10 -5.49%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +3.99%] · haut q95 +4.9% · bas q05 -4.11%
   - 60min (n=160) : retour [-4.9% .. +3.78%] · haut q95 +5.38% · bas q05 -5.2%
   - 2h (n=160) : retour [-4.74% .. +5.6%] · haut q95 +6.51% · bas q05 -5.28%
   - 4h (n=160) : retour [-7.33% .. +7.84%] · haut q95 +8.92% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.61% .. +6.89%] · haut q95 +9.73% · bas q05 -8.32%
   - session (n=160) : retour [-5.87% .. +6.22%] · haut q95 +9.73% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **17%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 6%)
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
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.1  _(momentum haussier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 2.694  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 21.8%
- **ATR** : 6.18 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.141  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 67.0  _(marche en range (choppy))_
- **MA** : MA20 94.59 · MA50 124.47 · MA200 166.07  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 -19.7% · MA200 -39.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92918 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
