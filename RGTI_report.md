# RGTI

**Generated** : 2026-08-20T20:16:56.450073+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.97  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.97 (+3.4% vs entrée) · entrée $15.44 · stop $14.33 · T1 $17.27 · R/R 1.65  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.016 _(réel 5 s)_ (GBM -0.038) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.8 % ≠ (strike 17.0 − spot 15.97)/spot = +6.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $15.20–$15.67 (mid $15.44)
- Spot actuel : $15.97 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $14.33 (stop swing_plan-based (-10.22%))
- Targets : T1 $17.27 · R/R 1.65 | T2 $18.08 · R/R 2.38 | T3 $18.90 · R/R 3.12
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.33


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.22 %)** : le gap seul le franchit 0.797 % des séances ; quand il le franchit, l'exécution est **4.782 points plus bas** → perte réelle **15.002 %** _(et non 10.22 %)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.083 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2923** [0.2284 ; 0.3631] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.5522** [0.4995 ; 0.604] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5576** [0.5049 ; 0.6093] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.2 pt), swing (36.9 pt), deep (34.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.8 %** | CVaR **-10.8 %** | vol 6.84 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 16.36 % contre 6.37 % aujourd'hui, rapport 2.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8385** (β de hausse 1.9817, asymétrie 0.9277) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.665× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.038 | EV/share : $-0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.5 | bear 27.8 | side 66.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 10 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.507% → cible +3.659% / stop −2.105%, p_fill 65%, n_eff≈28.4) : P(cible|rempli) **23%** · **EV/risk -0.014** (×p_fill ; si rempli -0.04% du capital)
  - **swing** (entrée dip −3.31% → cible +11.866% / stop −7.147%, p_fill 52%, n_eff≈25.7) : P(cible|rempli) **27%** · **EV/risk -0.016** (×p_fill ; si rempli -0.22% du capital)
  - **deep** (entrée dip −5.119% → cible +25.528% / stop −12.764%, p_fill 61%, n_eff≈28.8) : P(cible|rempli) **18%** · **EV/risk -0.009** (×p_fill ; si rempli -0.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→80% · +2.0%→74% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.46%
- Profil de vol intra : ouverture 5.491% vs midi 1.576% vs clôture 1.842% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.325% ; recovery-V 33%
- **σ réalisé intraday** 4.584% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 45% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 16.9713 (VA 16.777–17.2488 ; dernier close 17.01)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 43% · rebond 77% · **stop −6.3%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 42% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.9%) · haut méd +1.28% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.99%) · haut méd +1.87% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.77%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.02%) · haut méd +2.53% · range méd 5.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 78% · séance 84% (135/159) · gap 48% · délai 0.0min · rebond 66% (88/135) (MFE +2.44%)
   - −1.0% : fill 30min 68% · séance 76% (127/159) · gap 42% · délai 0.0min · rebond 69% (83/127) (MFE +2.02%)
   - −1.5% : fill 30min 60% · séance 69% (120/159) · gap 36% · délai 0.0min · rebond 69% (80/120) (MFE +2.24%)
   - −2.0% : fill 30min 56% · séance 63% (112/159) · gap 29% · délai 0.0min · rebond 70% (76/112) (MFE +2.48%)
   - −3.0% : fill 30min 50% · séance 56% (98/159) · gap 13% · délai 1.2min · rebond 76% (72/98) (MFE +2.48%)
   - −4.0% : fill 30min 36% · séance 43% (77/159) · gap 5% · délai 5.6min · rebond 77% (57/77) (MFE +2.32%)
   - −5.0% : fill 30min 19% · séance 34% (63/159) · gap 3% · délai 21.6min · rebond 70% (48/63) (MFE +1.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.21%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −2.69%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.93%) → stop au-delà de −2.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.29% (p90 −3.09%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 95% (82/84) · rebond 64% (50/82)
      · −2.0% : fill 85% (77/84) · rebond 69% (52/77)
      · −3.0% : fill 80% (71/84) · rebond 71% (50/71)
      · −4.0% : fill 65% (57/84) · rebond 75% (41/57)
      · −5.0% : fill 52% (48/84) · rebond 69% (37/48)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 95% (13/15)
      · −2.0% : fill 71% (12/16) · rebond 85% (10/12)
      · −3.0% : fill 48% (7/16) · rebond 90% (5/7)
      · −4.0% : fill 32% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 20% (5/16) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 43% (30/59) · rebond 67% (20/30)
      · −2.0% : fill 30% (23/59) · rebond 63% (14/23)
      · −3.0% : fill 25% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 16% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 13% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 70% si les 15 1res min sont vertes (80 cas) · 30% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 88% si début vert vs 16% si rouge (base 52% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **88%** · continue >prix actuel 50% ; creux résiduel méd -2.39% (q20 -3.58%) → **SL/trailing à −3.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.34% / q75 +5.27% → **scale +2.34% / runner +5.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.37%** (au-delà de la MAE q10 -5.37%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.24% .. +4.96%] · haut q95 +6.51% · bas q05 -6.36%
   - 60min (n=160) : retour [-5.57% .. +6.41%] · haut q95 +6.71% · bas q05 -6.86%
   - 2h (n=160) : retour [-5.84% .. +7.05%] · haut q95 +9.14% · bas q05 -7.6%
   - 4h (n=160) : retour [-7.26% .. +7.22%] · haut q95 +9.18% · bas q05 -7.88%
   - 6h (n=160) : retour [-7.5% .. +8.25%] · haut q95 +9.43% · bas q05 -8.66%
   - session (n=160) : retour [-7.39% .. +8.56%] · haut q95 +10.21% · bas q05 -8.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.69% / p90 2.67%) · ~4.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 13.25 min, n=41)
   - −1.0% → **77%** (reprise méd 55.8 min, n=26)
   - −1.5% → **78%** (reprise méd 94.96 min, n=15)
   - −2.0% → **79%** (reprise méd 109.11 min, n=8)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.69%) ; extension open→close méd +7.29% (q75 +9.11% / q95 +9.99%), MFE méd +9.12% / q90 +10.34%
   - Échelle scale-out : +9.12% (33%) / +10.23% (33%) / +10.34% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **33%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.34% : P(retournement après) 0% (mèche méd 1.02%)
- **CONTEXTE** : la dernière heure tient les gains 59% du temps (retour médian dernière heure +0.5%)


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 55.5  _(momentum haussier)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist 0.053  _(pas de croisement recent)_
- **BB** : %B 0.4 · largeur 40.1%
- **ATR** : 1.1 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.005  _(neutre)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 16.65 · MA50 17.46 · MA200 20.15  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -8.5% · MA200 -20.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (410887 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
