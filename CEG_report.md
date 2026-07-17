# CEG

**Generated** : 2026-07-17T00:30:26.533470+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $251.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $251.77 (+1.5% vs entrée) · entrée $248.14 · stop $244.42 · T1 $251.21 · R/R 0.83  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.071 _(réel 5 s)_ (GBM -0.038) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $247.53–$248.75 (mid $248.14)
- Spot actuel : $251.77 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $244.42 (stop swing_plan-based (-4.51%))
- Targets : T1 $251.21 · R/R 0.83 | T2 $254.28 · R/R 1.65 | T3 $257.34 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $244.42


## Edge, scénarios & sizing

- EV/risk : -0.038 | EV/share : $-0.141 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 26 % | T3 8 %
- Kelly (position) : f* 0.038 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.4 | bear 6.3 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.442% → cible +1.236% / stop −1.5%, p_fill 42%, n_eff≈20.4) : P(cible|rempli) **36%** · **EV/risk -0.071** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −3.171% → cible +2.765% / stop −1.382%, p_fill 35%, n_eff≈18.3) : P(cible|rempli) **11%** · **EV/risk -0.254** (×p_fill ; si rempli -1.00% du capital)
  - **deep** (entrée dip −4.901% → cible +3.91% / stop −1.955%, p_fill 53%, n_eff≈20.7) : P(cible|rempli) **17%** · **EV/risk -0.279** (×p_fill ; si rempli -1.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→39% · +3.0%→21% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.44% (p90 5.5%) · excursion haute méd. +1.51% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.568% vs midi 0.738% vs clôture 0.751% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. -0.168% ; recovery-V 12%
- **σ réalisé intraday** 2.312% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 257.379 (VA 255.881–259.947 ; dernier close 258.15)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 43% · rebond 60% · **stop −3.2%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.12% · baisse 45% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.57%) · haut méd +0.85% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −0.64% (p90 −2.17%) · haut méd +1.01% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.71%) · haut méd +1.09% · range méd 2.26%
- Excursion ouverture 60min (n=160) : bas méd −0.93% (p90 −3.01%) · haut méd +1.37% · range méd 2.64%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 258.15 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 70% (119/159) · gap 26% · délai 0.0min · rebond 45% (59/119) (MFE +0.93%)
   - −1.0% : fill 30min 49% · séance 60% (103/159) · gap 20% · délai 1.5min · rebond 51% (57/103) (MFE +1.06%)
   - −1.5% : fill 30min 37% · séance 50% (89/159) · gap 10% · délai 3.9min · rebond 52% (48/89) (MFE +1.05%)
   - −2.0% : fill 30min 27% · séance 43% (69/159) · gap 8% · délai 10.2min · rebond 60% (42/69) (MFE +1.08%)
   - −3.0% : fill 30min 12% · séance 26% (43/159) · gap 3% · délai 42.3min · rebond 36% (17/43) (MFE +0.79%)
   - −4.0% : fill 30min 5% · séance 16% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 10% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.21%) → stop au-delà de −0.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.21% (p90 −1.02%) → stop au-delà de −0.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.59%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.08% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 95% (55/56) · rebond 50% (33/55)
      · −2.0% : fill 75% (40/56) · rebond 57% (26/40)
      · −3.0% : fill 52% (27/56) · rebond 39% (11/27)
      · −4.0% : fill 34% (19/56) · rebond 34% (8/19)
      · −5.0% : fill 24% (15/56) · rebond 77% (11/15)
   - **flat** (35 séances) :
      · −1.0% : fill 60% (21/35) · rebond 40% (7/21)
      · −2.0% : fill 36% (12/35) · rebond 48% (4/12)
      · −3.0% : fill 25% (10/35) · rebond 28% (4/10)
      · −4.0% : fill 11% (5/35) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/35) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 32% (27/68) · rebond 63% (17/27)
      · −2.0% : fill 21% (17/68) · rebond 79% (12/17)
      · −3.0% : fill 6% (6/68) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 69% si les 15 1res min sont vertes (91 cas) · 21% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 50% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **81%** · continue >prix actuel 42% ; creux résiduel méd -1.06% (q20 -1.9%) → **SL/trailing à −1.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.75% / q75 +1.36% → **scale +0.75% / runner +1.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **12%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.61%** (au-delà de la MAE q10 -2.61%), cible rebond +0.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.36%] · haut q95 +2.81% · bas q05 -3.5%
   - 60min (n=160) : retour [-3.68% .. +2.73%] · haut q95 +3.4% · bas q05 -4.33%
   - 2h (n=160) : retour [-3.9% .. +3.01%] · haut q95 +4.21% · bas q05 -5.01%
   - 4h (n=160) : retour [-3.99% .. +3.32%] · haut q95 +4.93% · bas q05 -5.52%
   - 6h (n=160) : retour [-4.75% .. +3.28%] · haut q95 +5.19% · bas q05 -5.74%
   - session (n=160) : retour [-4.33% .. +3.31%] · haut q95 +5.19% · bas q05 -5.74%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **24%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.33% / p90 1.7%) · ~1.3 replis/séance, durée méd 60.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 22.57 min, n=22)
   - −1.0% → **58%** (reprise méd 114.96 min, n=10)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.7%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.24% (q75 +3.91% / q95 +6.6%), MFE méd +3.42% / q90 +5.81%
   - Échelle scale-out : +3.42% (33%) / +5.29% (33%) / +5.81% (34%)
- **DÉSARMER** : repli > **−1.7%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.81% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.7  _(momentum baissier)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist 1.537  _(bullish_recent)_
- **BB** : %B 0.4 · largeur 18.6%
- **ATR** : 9.41 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.202  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 256.36 · MA50 268.82 · MA200 312.54  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -6.3% · MA200 -19.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89255 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
