# SOI

**Generated** : 2026-08-19T21:43:59.641421+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €109.15  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €109.15 (+1.4% vs entrée) · entrée €107.65 · stop €97.48 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk 0.152 _(réel 5 s)_ (GBM 0.245) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 138 % hors [0,100] (R² max 0.65). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €106.15–€109.15 (mid €107.65)
- Spot actuel : €109.15 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €97.48 (stop swing_plan-based (-10.7%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €136.10 · R/R 2.8 | T3 €136.89 · R/R 2.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €97.48


## Edge, scénarios & sizing

- EV/risk : 0.245 | EV/share : €2.495 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 15 % | T3 14 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 56.0 | bear 26.3 | side 17.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 437.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.621% → cible +8.552% / stop −4.276%, p_fill 90%, n_eff≈36.3) : P(cible|rempli) **5%** · **EV/risk -0.065** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −1.379% → cible +18.903% / stop −9.451%, p_fill 82%, n_eff≈34.4) : P(cible|rempli) **19%** · **EV/risk +0.152** (×p_fill ; si rempli +1.76% du capital)
  - **deep** (entrée dip −1.995% → cible +27.233% / stop −13.616%, p_fill 87%, n_eff≈36.5) : P(cible|rempli) **26%** · **EV/risk -0.077** (×p_fill ; si rempli -1.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→68% · +3.0%→54% · +5.0%→38% · +8.0%→15%
- Range intraday médian 8.76% (p90 15.19%) · excursion haute méd. +3.5% / basse méd. −3.33%
- Profil de vol intra : ouverture 5.489% vs midi 1.534% vs clôture 2.399% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.032% ; recovery-V 39%
- **σ réalisé intraday** 5.019% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 57% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 131.955 (VA 131.297–132.519 ; dernier close 130.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 61% · rebond 79% · **stop −8.26%** sous le fill (sous le bruit) · cible +2.71% · R/R 0.33 (high win-rate)
- Gaps overnight (n=154) : méd. 0.51% · baisse 44% (gap-down >1% 31% · >2% 20%)
- Excursion ouverture 5min (n=155) : bas méd −1.14% (p90 −3.53%) · haut méd +0.98% · range méd 2.77%
- Excursion ouverture 15min (n=155) : bas méd −1.42% (p90 −4.89%) · haut méd +1.38% · range méd 3.48%
- Excursion ouverture 30min (n=155) : bas méd −1.52% (p90 −5.17%) · haut méd +1.68% · range méd 3.98%
- Excursion ouverture 60min (n=155) : bas méd −1.65% (p90 −5.61%) · haut méd +1.86% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 130.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 78% (121/154) · gap 36% · délai 0.0min · rebond 65% (79/121) (MFE +2.02%)
   - −1.0% : fill 30min 58% · séance 74% (115/154) · gap 31% · délai 0.2min · rebond 74% (84/115) (MFE +1.87%)
   - −1.5% : fill 30min 52% · séance 68% (104/154) · gap 25% · délai 0.3min · rebond 75% (77/104) (MFE +2.22%)
   - −2.0% : fill 30min 47% · séance 61% (95/154) · gap 20% · délai 0.4min · rebond 79% (76/95) (MFE +2.71%)
   - −3.0% : fill 30min 33% · séance 47% (76/154) · gap 14% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 26% · séance 39% (61/154) · gap 7% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 20% · séance 36% (53/154) · gap 1% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −3.71%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.96%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.46%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1337 jambes) : jambe baissière méd −1.29% (p90 −3.08%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 98% (58/59) · rebond 64% (37/58)
      · −2.0% : fill 95% (56/59) · rebond 75% (44/56)
      · −3.0% : fill 78% (46/59) · rebond 74% (37/46)
      · −4.0% : fill 67% (40/59) · rebond 81% (33/40)
      · −5.0% : fill 61% (35/59) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (78 séances) :
      · −1.0% : fill 51% (40/78) · rebond 84% (33/40)
      · −2.0% : fill 29% (24/78) · rebond 88% (20/24)
      · −3.0% : fill 20% (19/78) · rebond 83% (15/19)
      · −4.0% : fill 15% (13/78) · rebond 55% (9/13)
      · −5.0% : fill 13% (10/78) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 51% en base · 68% si les 15 1res min sont vertes (73 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=155) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 27% si rouge (base 51% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 60% ; creux résiduel méd -2.6% (q20 -5.46%) → **SL/trailing à −5.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.54% / q75 +5.1% → **scale +3.54% / runner +5.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **27%** (continue à baisser 64%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.82%** (au-delà de la MAE q10 -8.82%), cible rebond +2.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-5.22% .. +6.8%] · haut q95 +7.84% · bas q05 -6.37%
   - 60min (n=155) : retour [-5.8% .. +6.86%] · haut q95 +8.59% · bas q05 -6.77%
   - 2h (n=155) : retour [-5.93% .. +7.3%] · haut q95 +12.04% · bas q05 -7.31%
   - 4h (n=155) : retour [-6.6% .. +9.81%] · haut q95 +13.11% · bas q05 -7.96%
   - 6h (n=155) : retour [-7.38% .. +10.25%] · haut q95 +13.97% · bas q05 -9.31%
   - session (n=155) : retour [-10.35% .. +13.13%] · haut q95 +14.84% · bas q05 -12.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.5% des séances sont trend-up (mild 0% / strong 6.5%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 11% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 58.6  _(momentum haussier)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist 0.149  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 40.0%
- **ATR** : 8.69 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.13  _(distribution)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 41.8  _(transition)_
- **MA** : MA20 116.0 · MA50 113.48 · MA200 75.93  _(prix < MA20)_
- **Dist MA** : MA20 -5.9% · MA50 -3.8% · MA200 +43.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98687 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
