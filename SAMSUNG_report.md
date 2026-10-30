# 005930

**Generated** : 2026-10-30T01:16:40.855757+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩221750.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩221750.00 (+1.9% vs entrée) · entrée ₩217674.05 · stop ₩213125.83 · T1 ₩225254.40 · R/R 1.67  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.09% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 221750.0 · ATR Wilder 13600.19 (6.13 %)_
- **Swing** : plage **205409.26 → 195061.09** (-7.37 % a -12.04 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 197981.66-204500.0 (A). stop INDICATIF 182399.9 (-6.49 % sous le bas ; sous le support 189200.0-194183.48 (- 0,5 ATR)).
- **Deep** : plage **195061.09 → 164970.57** (-12.04 % a -25.61 % sous la cloture, 2.21 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 189200.0-194183.48 (A) ; 166770.53-168863.88 (A). stop INDICATIF 141927.71 (-13.97 % sous le bas ; sous le support 148727.8-151120.2 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.25 ATR sous le plus haut 20 s., RSI(2) 28.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 197981.66-204500.0 (A, -7.78 %) ; 189200.0-194183.48 (A, -12.43 %) ; 166770.53-168863.88 (A, -23.85 %) ; 148727.8-151120.2 (B, -31.85 %) ; 141351.23-144042.68 (A, -35.04 %) ; 128093.31-132280.01 (B, -40.35 %)
- Resistances reelles au-dessus : 240000.0-246500.0 (A, 8.23 %) ; 261711.37-267000.0 (A, 18.02 %) ; 276000.0-281500.0 (A, 24.46 %) ; 285500.0-288000.0 (A, 28.75 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.51 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.88 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **0.062 pt plus bas** dans le cas TYPIQUE (médiane), 0.062 au p90, **0.062 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 10.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0001 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.702 % | p01 -4.987 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4218** [0.35 ; 0.4962] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.2913** [0.2453 ; 0.3408] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.24** [0.1973 ; 0.2871] _(largeur 9.0 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.5 pt), deep (26.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.82 %** | CVaR **-9.95 %** | vol 4.88 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.81 % contre 5.76 % aujourd'hui, rapport 0.49)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.8 % vs -7.83 % si l'on extrapolait par √5 _(rapport 0.869 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1821** (β de hausse 1.3422, asymétrie 0.8807) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : ₩-102.278 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 5.6 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 148.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.839% → cible +3.482% / stop −2.089%, p_fill 55%, n_eff≈60.9) : P(cible|rempli) **9%** · **EV/risk -0.202** (×p_fill ; si rempli -0.77% du capital)
  - **swing** (entrée dip −4.043% → cible +13.723% / stop −7.125%, p_fill 44%, n_eff≈52.4) : P(cible|rempli) **12%** · **EV/risk -0.103** (×p_fill ; si rempli -1.65% du capital)
  - **deep** (entrée dip −6.244% → cible +16.399% / stop −10.939%, p_fill 45%, n_eff≈50.7) : P(cible|rempli) **16%** · **EV/risk -0.085** (×p_fill ; si rempli -2.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→47% · +3.0%→34% · +5.0%→18% · +8.0%→3%
- Range intraday médian 5.16% (p90 8.97%) · excursion haute méd. +1.89% / basse méd. −2.23%
- Profil de vol intra : ouverture 2.706% vs midi 1.151% vs clôture 1.316% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.097)_ ; drift intra méd. -0.205% ; recovery-V 27%
- **σ réalisé intraday** 2.986% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 212950.0 (VA 208450.0–215050.0 ; dernier close 215500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 21% · rebond 50% · **stop −6.44%** sous le fill (sous le bruit) · cible +0.92% · R/R 0.14 (high win-rate)
- Gaps overnight (n=152) : méd. 0.09% · baisse 48% (gap-down >1% 32% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.51% (p90 −1.56%) · haut méd +0.59% · range méd 1.29%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.15%) · haut méd +0.77% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.68%) · haut méd +0.98% · range méd 2.36%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.39%) · haut méd +1.18% · range méd 2.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 215500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 69% (98/152) · gap 41% · délai 0.0min · rebond 45% (44/98) (MFE +0.92%)
   - −1.0% : fill 30min 48% · séance 61% (88/152) · gap 32% · délai 0.0min · rebond 58% (46/88) (MFE +1.24%)
   - −1.5% : fill 30min 39% · séance 51% (75/152) · gap 26% · délai 0.0min · rebond 59% (40/75) (MFE +1.15%)
   - −2.0% : fill 30min 32% · séance 46% (70/152) · gap 24% · délai 0.0min · rebond 54% (38/70) (MFE +1.24%)
   - −3.0% : fill 30min 26% · séance 39% (61/152) · gap 23% · délai 0.0min · rebond 50% (32/61) (MFE +1.0%)
   - −4.0% : fill 30min 22% · séance 35% (50/152) · gap 9% · délai 5.7min · rebond 50% (28/50) (MFE +1.06%)
   - −5.0% : fill 30min 12% · séance 21% (35/152) · gap 7% · délai 14.8min · rebond 50% (21/35) (MFE +0.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.78%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.98%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −2.15%) → stop au-delà de −1.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=773 jambes) : jambe baissière méd −1.19% (p90 −2.81%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 98% (58/60) · rebond 58% (27/58)
      · −2.0% : fill 77% (49/60) · rebond 39% (21/49)
      · −3.0% : fill 75% (48/60) · rebond 46% (24/48)
      · −4.0% : fill 68% (41/60) · rebond 45% (22/41)
      · −5.0% : fill 45% (30/60) · rebond 44% (16/30)
   - **flat** (15 séances) :
      · −1.0% : fill 57% (11/15) · rebond 64% (6/11)
      · −2.0% : fill 41% (7/15) · rebond 85% (5/7)
      · −3.0% : fill 18% (4/15) · rebond 18% (1/4)
      · −4.0% : fill 12% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 12% (2/15) · rebond 100% (2/2)
   - **gap-up** (77 séances) :
      · −1.0% : fill 28% (19/77) · rebond 54% (13/19)
      · −2.0% : fill 20% (14/77) · rebond 91% (12/14)
      · −3.0% : fill 12% (9/77) · rebond 85% (7/9)
      · −4.0% : fill 10% (7/77) · rebond 96% (6/7)
      · −5.0% : fill 2% (3/77) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 64% si les 15 1res min sont vertes (79 cas) · 20% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 42% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 77min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 58% ; creux résiduel méd -1.18% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.58% / q75 +2.99% → **scale +1.58% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **8%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.13%** (au-delà de la MAE q10 -5.13%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.52% .. +3.07%] · haut q95 +3.45% · bas q05 -3.33%
   - 60min (n=160) : retour [-2.99% .. +3.07%] · haut q95 +4.3% · bas q05 -3.65%
   - 2h (n=160) : retour [-3.97% .. +4.52%] · haut q95 +5.82% · bas q05 -5.0%
   - 4h (n=160) : retour [-5.32% .. +5.06%] · haut q95 +6.21% · bas q05 -6.7%
   - 6h (n=160) : retour [-5.49% .. +4.64%] · haut q95 +6.65% · bas q05 -7.05%
   - session (n=160) : retour [-5.1% .. +5.3%] · haut q95 +6.65% · bas q05 -7.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 3.02%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.39 · part idiosyncratique 0.61
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 38.8  _(momentum baissier)_
- **ADX** : 23.9  _(pas de tendance nette)_
- **MACD** : hist 914.617  _(bullish_recent)_
- **BB** : %B 0.35 · largeur 39.9%
- **ATR** : 15160.71 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.208  _(distribution)_
- **Vol ratio** : 0.25  _(volume atone)_
- **Choppiness** : 58.4  _(transition)_
- **MA** : MA20 235412.5 · MA50 252025.0 · MA200 237068.63  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -12.0% · MA200 -6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (512767 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
