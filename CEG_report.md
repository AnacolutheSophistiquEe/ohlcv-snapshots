# CEG

**Generated** : 2026-06-30T00:19:52.407762+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $259.32  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $259.32 (+3.9% vs entrée) · entrée $249.55 · stop $245.31 · T1 $258.02 · R/R 2.0  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.042 _(réel 5 s)_ (GBM 0.098) · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $247.85–$251.24 (mid $249.55)
- Spot actuel : $259.32 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : $245.31 (stop swing_plan-based (-5.4%))
- Targets : T1 $258.02 · R/R 2.0 | T2 $266.49 · R/R 4.0 | T3 $274.96 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $245.31


## Edge, scénarios & sizing

- EV/risk : 0.098 | EV/share : $0.414 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 22 % | T3 11 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 79.6 | bear 7.4 | side 13.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.716% → cible +1.518% / stop −1.5%, p_fill 43%, n_eff≈19.4) : P(cible|rempli) **30%** · **EV/risk -0.035** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −3.767% → cible +3.395% / stop −1.697%, p_fill 37%, n_eff≈19.2) : P(cible|rempli) **32%** · **EV/risk -0.042** (×p_fill ; si rempli -0.19% du capital)
  - **deep** (entrée dip −5.819% → cible +4.801% / stop −2.4%, p_fill 43%, n_eff≈18.6) : P(cible|rempli) **32%** · **EV/risk -0.041** (×p_fill ; si rempli -0.23% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→36% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.5%) · excursion haute méd. +1.5% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.525% vs midi 0.735% vs clôture 0.767% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.078)_ ; drift intra méd. -0.221% ; recovery-V 20%
- **σ réalisé intraday** 2.407% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 264.7539 (VA 262.3586–265.4071 ; dernier close 263.92)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.18% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 43% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.87%) · haut méd +0.78% · range méd 1.7%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.29%) · haut méd +1.0% · range méd 2.08%
- Excursion ouverture 30min (n=160) : bas méd −0.89% (p90 −2.73%) · haut méd +1.08% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −3.07%) · haut méd +1.31% · range méd 2.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 263.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (119/159) · gap 27% · délai 0.0min · rebond 46% (60/119) (MFE +0.93%)
   - −1.0% : fill 30min 52% · séance 64% (104/159) · gap 23% · délai 1.6min · rebond 54% (59/104) (MFE +1.11%)
   - −1.5% : fill 30min 41% · séance 56% (90/159) · gap 12% · délai 3.7min · rebond 55% (51/90) (MFE +1.2%)
   - −2.0% : fill 30min 31% · séance 47% (70/159) · gap 10% · délai 10.0min · rebond 67% (46/70) (MFE +1.18%)
   - −3.0% : fill 30min 11% · séance 27% (43/159) · gap 4% · délai 50.6min · rebond 38% (18/43) (MFE +0.74%)
   - −4.0% : fill 30min 6% · séance 16% (28/159) · gap 2% · délai 37.5min · rebond 47% (14/28) (MFE +0.93%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 6.1min · rebond 61% (10/17) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.42%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.26% (p90 −1.19%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.62%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=479 jambes) : jambe baissière méd −1.07% (p90 −2.58%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 100% (54/54) · rebond 53% (34/54)
      · −2.0% : fill 85% (39/54) · rebond 69% (28/39)
      · −3.0% : fill 53% (24/54) · rebond 42% (10/24)
      · −4.0% : fill 35% (17/54) · rebond 46% (8/17)
      · −5.0% : fill 21% (13/54) · rebond 64% (9/13)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 36% (27/68) · rebond 70% (18/27)
      · −2.0% : fill 22% (17/68) · rebond 75% (12/17)
      · −3.0% : fill 8% (7/68) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 71% si les 15 1res min sont vertes (90 cas) · 20% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 12% si rouge (base 49% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 163min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **83%** · continue >prix actuel 40% ; creux résiduel méd -0.93% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.85% / q75 +1.7% → **scale +0.85% / runner +1.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **12%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.45%** (au-delà de la MAE q10 -2.45%), cible rebond +0.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.33%] · haut q95 +3.13% · bas q05 -3.77%
   - 60min (n=160) : retour [-3.5% .. +3.04%] · haut q95 +3.5% · bas q05 -4.15%
   - 2h (n=160) : retour [-3.76% .. +3.15%] · haut q95 +4.27% · bas q05 -4.74%
   - 4h (n=160) : retour [-3.81% .. +3.35%] · haut q95 +5.28% · bas q05 -5.04%
   - 6h (n=160) : retour [-4.34% .. +3.54%] · haut q95 +5.28% · bas q05 -5.05%
   - session (n=160) : retour [-4.31% .. +3.57%] · haut q95 +5.28% · bas q05 -5.04%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.29% / p90 1.8%) · ~2.0 replis/séance, durée méd 55.87 min. P(nouveau plus-haut après repli) :
   - −0.5% → **60%** (reprise méd 17.23 min, n=23)
   - −1.0% → **42%** (reprise méd 20.49 min, n=9)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.8%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +3.46% (q75 +4.43% / q95 +6.6%), MFE méd +3.74% / q90 +6.4%
   - Échelle scale-out : +3.74% (33%) / +5.32% (33%) / +6.4% (34%)
- **DÉSARMER** : repli > **−1.8%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.4% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 85% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.46 · part idiosyncratique 0.54
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.9  _(momentum haussier)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist 1.3  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 14.4%
- **ATR** : 9.45 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.222  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 43.2  _(transition)_
- **MA** : MA20 262.37 · MA50 281.39 · MA200 317.31  _(prix < MA20)_
- **Dist MA** : MA20 -1.2% · MA50 -7.8% · MA200 -18.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91875 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
