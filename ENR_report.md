# ENR

**Generated** : 2026-08-13T21:40:26.472416+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €160.72  

> 🟡 **WAIT-FOR-DIP** — spot +3.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €160.72 (+3.2% vs entrée) · entrée €155.78 · stop €148.25 · T1 €167.54 · R/R 1.56  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk 0.028 _(réel 5 s)_ (GBM 0.08) · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €154.58–€156.98 (mid €155.78)
- Spot actuel : €160.72 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : €148.25 (stop swing_plan-based (-7.76%))
- Targets : T1 €167.54 · R/R 1.56 | T2 €170.64 · R/R 1.97 | T3 €173.74 · R/R 2.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €148.25


## Edge, scénarios & sizing

- EV/risk : 0.08 | EV/share : €0.603 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 15 % | T3 8 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.5 | bear 21.2 | side 64.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 321.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.401% → cible +1.718% / stop −1.5%, p_fill 59%, n_eff≈25.2) : P(cible|rempli) **30%** · **EV/risk -0.140** (×p_fill ; si rempli -0.35% du capital)
  - **swing** (entrée dip −3.075% → cible +7.551% / stop −4.834%, p_fill 58%, n_eff≈22.4) : P(cible|rempli) **31%** · **EV/risk +0.028** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −4.752% → cible +5.434% / stop −7.378%, p_fill 63%, n_eff≈24.2) : P(cible|rempli) **51%** · **EV/risk -0.025** (×p_fill ; si rempli -0.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→44% · +3.0%→25% · +5.0%→9% · +8.0%→1%
- Range intraday médian 4.19% (p90 6.72%) · excursion haute méd. +1.53% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.166% vs midi 0.988% vs clôture 1.153% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑2%/↓0% ; spike-down 58% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.28% ; recovery-V 17%
- **σ réalisé intraday** 2.788% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 72% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 155.6055 (VA 155.0975–157.7645 ; dernier close 158.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 62% · rebond 69% · **stop −4.23%** sous le fill (sous le bruit) · cible +1.88% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 36% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.77%) · haut méd +0.48% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.7% (p90 −2.23%) · haut méd +0.67% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.79% (p90 −2.3%) · haut méd +0.67% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.57%) · haut méd +0.79% · range méd 2.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 158.56 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 70% (114/159) · gap 28% · délai 0.3min · rebond 57% (65/114) (MFE +1.22%)
   - −1.0% : fill 30min 46% · séance 67% (106/159) · gap 20% · délai 2.4min · rebond 66% (65/106) (MFE +1.63%)
   - −1.5% : fill 30min 36% · séance 62% (94/159) · gap 17% · délai 13.4min · rebond 69% (62/94) (MFE +1.88%)
   - −2.0% : fill 30min 21% · séance 47% (72/159) · gap 11% · délai 50.2min · rebond 64% (45/72) (MFE +1.51%)
   - −3.0% : fill 30min 13% · séance 30% (51/159) · gap 4% · délai 204.5min · rebond 62% (35/51) (MFE +1.53%)
   - −4.0% : fill 30min 6% · séance 20% (38/159) · gap 2% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 2% · séance 14% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.19%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −2.13%) → stop au-delà de −0.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.0%) → stop au-delà de −0.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=536 jambes) : jambe baissière méd −1.07% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (48/49) · rebond 62% (27/48)
      · −2.0% : fill 74% (38/49) · rebond 58% (24/38)
      · −3.0% : fill 58% (31/49) · rebond 50% (20/31)
      · −4.0% : fill 44% (25/49) · rebond 53% (17/25)
      · −5.0% : fill 35% (17/49) · rebond 59% (11/17)
   - **flat** (25 séances) :
      · −1.0% : fill 62% (19/25) · rebond 77% (13/19)
      · −2.0% : fill 33% (10/25) · rebond 69% (5/10)
      · −3.0% : fill 12% (5/25) · rebond 80% (3/5)
      · −4.0% : fill 10% (4/25) · rebond 76% (2/4)
      · −5.0% : fill 6% (2/25) · rebond 74% (1/2)
   - **gap-up** (85 séances) :
      · −1.0% : fill 50% (39/85) · rebond 67% (25/39)
      · −2.0% : fill 35% (24/85) · rebond 71% (16/24)
      · −3.0% : fill 19% (15/85) · rebond 81% (12/15)
      · −4.0% : fill 8% (9/85) · rebond 69% (7/9)
      · −5.0% : fill 4% (4/85) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 77% si les 15 1res min sont vertes (77 cas) · 25% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 85% si début vert vs 26% si rouge (base 50% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **85%** · continue >prix actuel 58% ; creux résiduel méd -1.05% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.04% / q75 +2.63% → **scale +2.04% / runner +2.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **26%** (continue à baisser 52%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.28%** (au-delà de la MAE q10 -4.28%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.16% .. +1.94%] · haut q95 +2.5% · bas q05 -2.7%
   - 60min (n=160) : retour [-2.48% .. +2.32%] · haut q95 +2.64% · bas q05 -3.23%
   - 2h (n=160) : retour [-2.96% .. +2.64%] · haut q95 +2.9% · bas q05 -4.12%
   - 4h (n=160) : retour [-3.65% .. +2.62%] · haut q95 +3.81% · bas q05 -4.45%
   - 6h (n=160) : retour [-3.97% .. +3.72%] · haut q95 +4.68% · bas q05 -5.03%
   - session (n=160) : retour [-5.23% .. +4.36%] · haut q95 +5.47% · bas q05 -6.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 15% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 61.4  _(momentum haussier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist 2.037  _(pas de croisement recent)_
- **BB** : %B 0.87 · largeur 17.5%
- **ATR** : 7.53 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.114  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 44.5  _(transition)_
- **MA** : MA20 151.05 · MA50 155.36 · MA200 146.7  _(prix > MA20)_
- **Dist MA** : MA20 +6.4% · MA50 +3.5% · MA200 +9.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98219 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
