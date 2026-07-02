# PLTR

**Generated** : 2026-07-02T21:51:20.215733+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $129.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $129.30 (+4.6% vs entrée) · entrée $123.57 · stop $113.68 · T1 $126.09 · R/R 0.25  
> ↳ P(T1 av. stop) 38 % · EV/risk -0.031 · ¼-Kelly 0.049 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $123.06–$124.07 (mid $123.57)
- Spot actuel : $129.30 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $113.68 (stop swing_plan-based (-11.81%))
- Targets : T1 $126.09 · R/R 0.25 | T2 $128.61 · R/R 0.51 | T3 $131.13 · R/R 0.76
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.68


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.307 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 10 % | T3 6 %
- Kelly (position) : f* 0.195 | ¼-Kelly 0.049 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.8 | bear 9.8 | side 72.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 129.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→39% · +3.0%→21% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.86% (p90 7.17%) · excursion haute méd. +1.77% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.848% vs midi 0.73% vs clôture 0.805% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 54% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.158% ; recovery-V 21%
- **σ réalisé intraday** 2.668% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 51% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 127.46 (VA 126.58–127.68 ; dernier close 125.69)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 49% · **stop −2.9%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 56% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −1.97%) · haut méd +0.9% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −2.79%) · haut méd +1.15% · range méd 2.22%
- Excursion ouverture 30min (n=160) : bas méd −1.14% (p90 −3.53%) · haut méd +1.3% · range méd 2.62%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.86%) · haut méd +1.48% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 125.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (115/159) · gap 43% · délai 0.0min · rebond 54% (63/115) (MFE +1.07%)
   - −1.0% : fill 30min 57% · séance 69% (106/159) · gap 30% · délai 0.0min · rebond 61% (63/106) (MFE +1.32%)
   - −1.5% : fill 30min 48% · séance 59% (88/159) · gap 21% · délai 1.0min · rebond 64% (55/88) (MFE +1.37%)
   - −2.0% : fill 30min 40% · séance 51% (73/159) · gap 15% · délai 4.2min · rebond 61% (46/73) (MFE +1.43%)
   - −3.0% : fill 30min 19% · séance 35% (53/159) · gap 4% · délai 21.0min · rebond 45% (25/53) (MFE +0.85%)
   - −4.0% : fill 30min 13% · séance 24% (38/159) · gap 3% · délai 28.5min · rebond 42% (18/38) (MFE +0.83%)
   - −5.0% : fill 30min 10% · séance 18% (26/159) · gap 2% · délai 26.1min · rebond 49% (13/26) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −1.72%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.38%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.38%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=540 jambes) : jambe baissière méd −1.06% (p90 −2.71%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 93% (63/67) · rebond 64% (39/63)
      · −2.0% : fill 78% (52/67) · rebond 61% (35/52)
      · −3.0% : fill 55% (37/67) · rebond 38% (18/37)
      · −4.0% : fill 41% (27/67) · rebond 37% (12/27)
      · −5.0% : fill 34% (20/67) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (59 séances) :
      · −1.0% : fill 31% (17/59) · rebond 73% (10/17)
      · −2.0% : fill 14% (8/59) · rebond 42% (3/8)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 3% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 63% si les 15 1res min sont vertes (81 cas) · 31% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:30** → P(séance verte=clôture>ouverture) 91% si début vert vs 11% si rouge (base 48% · écart 80 pts) ; prédictivité sature ensuite (plafond brut 149min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **91%** · continue >prix actuel 48% ; creux résiduel méd -0.73% (q20 -1.52%) → **SL/trailing à −1.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.82% / q75 +1.42% → **scale +0.82% / runner +1.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **11%** (continue à baisser 50%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.0% .. +2.92%] · haut q95 +3.44% · bas q05 -4.19%
   - 60min (n=160) : retour [-3.44% .. +3.72%] · haut q95 +4.13% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.7% .. +3.65%] · haut q95 +4.47% · bas q05 -4.5%
   - 4h (n=160) : retour [-4.46% .. +5.16%] · haut q95 +5.67% · bas q05 -5.53%
   - 6h (n=160) : retour [-5.06% .. +4.82%] · haut q95 +5.99% · bas q05 -5.62%
   - session (n=160) : retour [-4.98% .. +4.61%] · haut q95 +5.99% · bas q05 -5.64%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.6%) · ~3.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 24.87 min, n=29)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.6%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.37% (q75 +5.17% / q95 +7.65%), MFE méd +5.25% / q90 +8.69%
   - Échelle scale-out : +5.25% (33%) / +7.16% (33%) / +8.69% (34%)
- **DÉSARMER** : repli > **−1.6%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.69% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 72% du temps (retour médian dernière heure +0.21%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.68 · part idiosyncratique 0.32
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist 0.503  _(bullish_recent)_
- **BB** : %B 0.59 · largeur 30.0%
- **ATR** : 6.59 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.198  _(distribution)_
- **Vol ratio** : 1.38  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 125.97 · MA50 134.58 · MA200 157.91  _(prix > MA20)_
- **Dist MA** : MA20 +2.6% · MA50 -3.9% · MA200 -18.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92921 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
