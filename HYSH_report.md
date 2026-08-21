# 298040

**Generated** : 2026-08-21T21:54:05.817299+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2721000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2721000.00 (+1.6% vs entrée) · entrée ₩2678535.04 · stop ₩2485535.04 · T1 ₩2963223.90 · R/R 1.48  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.059 _(réel 5 s)_ (GBM 0.201) · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2636070.09–₩2721000.00 (mid ₩2678535.04)
- Spot actuel : ₩2721000.00 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : ₩2485535.04 (stop swing_plan-based (-8.65%))
- Targets : T1 ₩2963223.90 · R/R 1.48 | T2 ₩3247912.76 · R/R 2.95 | T3 ₩3532601.62 · R/R 4.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2485535.04


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.96 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.65 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **3.036 pt plus bas** dans le cas TYPIQUE (médiane), 3.036 au p90, **3.036 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 8.65 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0025 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.437 % | p01 -4.603 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2948** [0.2307 ; 0.3657] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.4767** [0.4244 ; 0.5294] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4892** [0.4368 ; 0.5418] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (30.2 pt), deep (30.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.91 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.66 % contre 6.04 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.9 % vs -12.54 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0848** (β de hausse 0.9655, asymétrie 1.1235) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.201 | EV/share : ₩38730.374 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 8 % | T3 2 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.2 | bear 47.3 | side 31.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.707% → cible +12.652% / stop −8.0%, p_fill 96%, n_eff≈38.8) : P(cible|rempli) **3%** · **EV/risk -0.144** (×p_fill ; si rempli -1.20% du capital)
  - **swing** (entrée dip −1.557% → cible +10.629% / stop −7.205%, p_fill 96%, n_eff≈38.8) : P(cible|rempli) **25%** · **EV/risk -0.059** (×p_fill ; si rempli -0.44% du capital)
  - **deep** (entrée dip −2.26% → cible +15.031% / stop −10.886%, p_fill 98%, n_eff≈38.7) : P(cible|rempli) **26%** · **EV/risk -0.266** (×p_fill ; si rempli -2.96% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→60% · +2.0%→51% · +3.0%→39% · +5.0%→22% · +8.0%→6%
- Range intraday médian 7.04% (p90 10.6%) · excursion haute méd. +2.13% / basse méd. −4.19%
- Profil de vol intra : ouverture 4.535% vs midi 1.156% vs clôture 1.224% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -1.49% ; recovery-V 27%
- **σ réalisé intraday** 4.682% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 60% / whipsaw 7%
- POC intraday (dernière séance, temps-au-prix) : 2863687.5 (VA 2850937.5–2870062.5 ; dernier close 2858000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 82% · **stop −5.6%** sous le fill (sous le bruit) · cible +2.31% · R/R 0.41 (high win-rate)
- Gaps overnight (n=157) : méd. 0.96% · baisse 35% (gap-down >1% 24% · >2% 16%)
- Excursion ouverture 5min (n=158) : bas méd −1.47% (p90 −3.44%) · haut méd +0.78% · range méd 2.65%
- Excursion ouverture 15min (n=158) : bas méd −1.92% (p90 −4.33%) · haut méd +0.92% · range méd 3.38%
- Excursion ouverture 30min (n=158) : bas méd −2.47% (p90 −4.91%) · haut méd +0.99% · range méd 4.15%
- Excursion ouverture 60min (n=158) : bas méd −2.54% (p90 −5.32%) · haut méd +1.37% · range méd 4.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2858000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 66% (105/157) · gap 31% · délai 0.0min · rebond 55% (63/105) (MFE +1.26%)
   - −1.0% : fill 30min 54% · séance 62% (96/157) · gap 24% · délai 0.4min · rebond 59% (59/96) (MFE +1.48%)
   - −1.5% : fill 30min 48% · séance 57% (87/157) · gap 20% · délai 1.6min · rebond 53% (52/87) (MFE +1.45%)
   - −2.0% : fill 30min 44% · séance 54% (78/157) · gap 16% · délai 4.5min · rebond 55% (43/78) (MFE +1.37%)
   - −3.0% : fill 30min 31% · séance 46% (64/157) · gap 8% · délai 9.9min · rebond 57% (36/64) (MFE +1.38%)
   - −4.0% : fill 30min 23% · séance 41% (55/157) · gap 6% · délai 24.9min · rebond 69% (40/55) (MFE +1.94%)
   - −5.0% : fill 30min 19% · séance 34% (42/157) · gap 6% · délai 25.4min · rebond 82% (34/42) (MFE +2.31%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.16%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −3.28%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.47%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=855 jambes) : jambe baissière méd −1.4% (p90 −3.48%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 100% (53/53) · rebond 60% (33/53)
      · −2.0% : fill 90% (45/53) · rebond 50% (24/45)
      · −3.0% : fill 87% (43/53) · rebond 57% (24/43)
      · −4.0% : fill 84% (38/53) · rebond 75% (28/38)
      · −5.0% : fill 74% (32/53) · rebond 81% (25/32)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (88 séances) :
      · −1.0% : fill 38% (32/88) · rebond 56% (18/32)
      · −2.0% : fill 31% (25/88) · rebond 62% (14/25)
      · −3.0% : fill 21% (16/88) · rebond 52% (8/16)
      · −4.0% : fill 15% (12/88) · rebond 64% (9/12)
      · −5.0% : fill 9% (7/88) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 34% en base · 53% si les 15 1res min sont vertes (63 cas) · 25% si rouges (95 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=158) : COUDE à **46min** → P(séance verte=clôture>ouverture) 74% si début vert vs 14% si rouge (base 34% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **74%** · continue >prix actuel 46% ; creux résiduel méd -1.83% (q20 -3.92%) → **SL/trailing à −3.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +3.91% → **scale +1.78% / runner +3.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **14%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.98%** (au-delà de la MAE q10 -5.98%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-4.33% .. +4.26%] · haut q95 +6.12% · bas q05 -5.34%
   - 60min (n=158) : retour [-5.25% .. +4.83%] · haut q95 +6.61% · bas q05 -6.06%
   - 2h (n=158) : retour [-7.07% .. +4.51%] · haut q95 +6.91% · bas q05 -8.11%
   - 4h (n=158) : retour [-7.63% .. +5.31%] · haut q95 +7.61% · bas q05 -9.27%
   - 6h (n=158) : retour [-7.6% .. +5.24%] · haut q95 +8.35% · bas q05 -9.32%
   - session (n=158) : retour [-7.62% .. +5.59%] · haut q95 +8.35% · bas q05 -9.39%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.1% des séances sont trend-up (mild 0% / strong 5.1%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **54%**. Lecture précoce 30 min : signature présente → 20% vs absente 0% (base 5%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 58.9  _(momentum haussier)_
- **ADX** : 9.9  _(pas de tendance nette)_
- **MACD** : hist 34734.786  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 47.3%
- **ATR** : 193000.0 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.136  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 56.3  _(transition)_
- **MA** : MA20 2686000.0 · MA50 2996480.0 · MA200 2726853.63  _(prix > MA20)_
- **Dist MA** : MA20 +1.3% · MA50 -9.2% · MA200 -0.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (611454 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
