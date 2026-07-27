# SMCI

**Generated** : 2026-07-27T00:21:50.280974+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $30.11  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $30.11 (+9.3% vs entrée) · entrée $27.54 · stop $26.53 · T1 $29.56 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % · EV/risk 0.059 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -7.0 % ≠ (strike 29.0 − spot 30.11)/spot = -3.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $27.13–$27.94 (mid $27.54)
- Spot actuel : $30.11 (+9.3% au-dessus de la zone — repli à attendre)
- Stop : $26.53 (stop swing_plan-based (-11.9%))
- Targets : T1 $29.56 · R/R 2.0 | T2 $31.58 · R/R 4.0 | T3 $33.60 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.53


## Edge, scénarios & sizing

- EV/risk : 0.059 | EV/share : $0.060 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 15 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.3 | bear 7.5 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 271.0 (= 9 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.878% → cible +9.117% / stop −4.559%, p_fill 34%, n_eff≈14.5) : P(cible|rempli) **0%** · **EV/risk -0.035** (×p_fill ; si rempli -0.47% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→64% · +3.0%→45% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.14%) · excursion haute méd. +2.57% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.966% vs midi 1.217% vs clôture 1.566% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 67% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.064)_ ; drift intra méd. -0.179% ; recovery-V 20%
- **σ réalisé intraday** 4.169% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 30.3306 (VA 29.7669–30.7919 ; dernier close 30.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 75% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.45% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 45% (gap-down >1% 31% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.06%) · haut méd +1.0% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −3.11%) · haut méd +1.38% · range méd 2.81%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.73%) · haut méd +1.47% · range méd 3.71%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −4.29%) · haut méd +1.66% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (125/159) · gap 40% · délai 0.0min · rebond 58% (73/125) (MFE +1.32%)
   - −1.0% : fill 30min 57% · séance 71% (113/159) · gap 31% · délai 0.0min · rebond 62% (66/113) (MFE +1.36%)
   - −1.5% : fill 30min 45% · séance 62% (96/159) · gap 24% · délai 0.1min · rebond 64% (59/96) (MFE +1.46%)
   - −2.0% : fill 30min 42% · séance 54% (86/159) · gap 19% · délai 0.4min · rebond 65% (54/86) (MFE +1.64%)
   - −3.0% : fill 30min 27% · séance 48% (69/159) · gap 13% · délai 11.8min · rebond 61% (42/69) (MFE +1.72%)
   - −4.0% : fill 30min 21% · séance 38% (51/159) · gap 9% · délai 13.8min · rebond 68% (31/51) (MFE +1.68%)
   - −5.0% : fill 30min 16% · séance 32% (42/159) · gap 6% · délai 23.5min · rebond 75% (29/42) (MFE +2.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.43%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.8%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −3.05%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=851 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 53% (37/67)
      · −2.0% : fill 85% (59/69) · rebond 61% (34/59)
      · −3.0% : fill 80% (52/69) · rebond 58% (30/52)
      · −4.0% : fill 67% (41/69) · rebond 69% (25/41)
      · −5.0% : fill 56% (34/69) · rebond 73% (23/34)
   - **flat** (15 séances) :
      · −1.0% : fill 94% (13/15) · rebond 87% (10/13)
      · −2.0% : fill 43% (8/15) · rebond 76% (5/8)
      · −3.0% : fill 10% (2/15) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/15) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/15) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 47% (33/75) · rebond 71% (19/33)
      · −2.0% : fill 27% (19/75) · rebond 74% (15/19)
      · −3.0% : fill 24% (15/75) · rebond 66% (10/15)
      · −4.0% : fill 16% (9/75) · rebond 65% (5/9)
      · −5.0% : fill 15% (8/75) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 69% si les 15 1res min sont vertes (75 cas) · 22% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 78% si début vert vs 12% si rouge (base 45% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.71% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.94% → **scale +1.68% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **12%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.63%** (au-delà de la MAE q10 -5.63%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.08% .. +5.03%] · haut q95 +6.69% · bas q05 -4.34%
   - 60min (n=160) : retour [-4.14% .. +5.62%] · haut q95 +6.69% · bas q05 -5.42%
   - 2h (n=160) : retour [-4.78% .. +6.74%] · haut q95 +8.51% · bas q05 -5.82%
   - 4h (n=160) : retour [-5.26% .. +7.53%] · haut q95 +8.88% · bas q05 -6.93%
   - 6h (n=160) : retour [-6.46% .. +6.94%] · haut q95 +9.88% · bas q05 -7.95%
   - session (n=160) : retour [-7.17% .. +7.86%] · haut q95 +9.88% · bas q05 -8.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 9% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.2  _(momentum haussier)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist 0.685  _(bullish_recent)_
- **BB** : %B 0.79 · largeur 30.2%
- **ATR** : 1.99 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.18  _(distribution)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 41.9  _(transition)_
- **MA** : MA20 27.67 · MA50 32.74 · MA200 33.47  _(prix > MA20)_
- **Dist MA** : MA20 +8.8% · MA50 -8.0% · MA200 -10.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91627 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
