# RHM

**Generated** : 2026-08-06T21:36:07.601996+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · €1159.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €1159.00 (+1.2% vs entrée) · entrée €1145.58 · stop €1094.74 · T1 €1179.52 · R/R 0.67  
> ↳ P(T1 av. stop) 68 % _(réel 5 s)_ · EV/risk 0.094 _(réel 5 s)_ (GBM -0.054) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 217 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €1138.79–€1152.37 (mid €1145.58)
- Spot actuel : €1159.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €1094.74 (stop swing_plan-based (-5.54%))
- Targets : T1 €1179.52 · R/R 0.67 | T2 €1213.45 · R/R 1.33 | T3 €1247.39 · R/R 2.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1094.74


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : €-2.740 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 31 % | T3 18 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 41.0 | bear 5.0 | side 54.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.531% → cible +1.325% / stop −2.0%, p_fill 84%, n_eff≈35.7) : P(cible|rempli) **53%** · **EV/risk +0.058** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −1.154% → cible +2.962% / stop −4.438%, p_fill 66%, n_eff≈30.9) : P(cible|rempli) **68%** · **EV/risk +0.094** (×p_fill ; si rempli +0.64% du capital)
  - **deep** (entrée dip −1.791% → cible +4.19% / stop −6.699%, p_fill 66%, n_eff≈29.5) : P(cible|rempli) **59%** · **EV/risk -0.044** (×p_fill ; si rempli -0.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→49% · +3.0%→29% · +5.0%→2% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.65%) · excursion haute méd. +1.98% / basse méd. −1.58%
- Profil de vol intra : ouverture 2.529% vs midi 0.892% vs clôture 1.111% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; neutre — autocorr -0.016)_ ; drift intra méd. 0.055% ; recovery-V 46%
- **σ réalisé intraday** 2.807% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 80% / bas 57% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 1226.6125 (VA 1222.9925–1229.3275 ; dernier close 1198.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 36% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.74% (p90 −1.74%) · haut méd +0.58% · range méd 1.35%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −2.0%) · haut méd +0.68% · range méd 1.83%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.75%) · haut méd +0.88% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.96%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1198.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 70% (116/159) · gap 24% · délai 0.3min · rebond 59% (63/116) (MFE +1.34%)
   - −1.0% : fill 30min 43% · séance 62% (105/159) · gap 10% · délai 4.1min · rebond 61% (61/105) (MFE +1.4%)
   - −1.5% : fill 30min 28% · séance 50% (81/159) · gap 5% · délai 18.2min · rebond 55% (43/81) (MFE +1.14%)
   - −2.0% : fill 30min 20% · séance 42% (71/159) · gap 4% · délai 30.4min · rebond 64% (44/71) (MFE +1.38%)
   - −3.0% : fill 30min 9% · séance 26% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 19% (27/159) · gap 1% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 9% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.73% (p90 −1.69%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.5% (p90 −1.77%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −1.94%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=488 jambes) : jambe baissière méd −1.06% (p90 −2.53%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (48/50) · rebond 63% (28/48)
      · −2.0% : fill 78% (38/50) · rebond 64% (25/38)
      · −3.0% : fill 50% (26/50) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/50) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/50) · rebond 76% (6/8)
   - **flat** (46 séances) :
      · −1.0% : fill 67% (33/46) · rebond 69% (21/33)
      · −2.0% : fill 29% (17/46) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/46) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/46) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/46) · rebond 22% (1/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 38% (24/63) · rebond 49% (12/24)
      · −2.0% : fill 26% (16/63) · rebond 62% (9/16)
      · −3.0% : fill 14% (9/63) · rebond 66% (6/9)
      · −4.0% : fill 8% (4/63) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/63) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 67% si les 15 1res min sont vertes (82 cas) · 43% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 76% si début vert vs 30% si rouge (base 54% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **76%** · continue >prix actuel 50% ; creux résiduel méd -0.97% (q20 -2.2%) → **SL/trailing à −2.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +2.17% → **scale +1.28% / runner +2.17%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **30%** (continue à baisser 54%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.52%** (au-delà de la MAE q10 -4.52%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +2.87%] · haut q95 +3.58% · bas q05 -3.41%
   - 60min (n=160) : retour [-2.99% .. +2.84%] · haut q95 +3.54% · bas q05 -4.35%
   - 2h (n=160) : retour [-3.38% .. +2.93%] · haut q95 +3.98% · bas q05 -4.63%
   - 4h (n=160) : retour [-3.79% .. +3.07%] · haut q95 +4.55% · bas q05 -4.94%
   - 6h (n=160) : retour [-4.35% .. +3.57%] · haut q95 +4.55% · bas q05 -5.53%
   - session (n=160) : retour [-6.03% .. +4.33%] · haut q95 +4.79% · bas q05 -6.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 81.8  _(surachat)_
- **ADX** : 26.0  _(tendance etablie)_
- **MACD** : hist 23.704  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 31.8%
- **ATR** : 50.84 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.019  _(neutre)_
- **Vol ratio** : 2.19  _(volume au-dessus de la moyenne)_
- **Choppiness** : 32.7  _(marche directionnel)_
- **MA** : MA20 1055.12 · MA50 1105.51 · MA200 1451.2  _(prix > MA20)_
- **Dist MA** : MA20 +9.8% · MA50 +4.8% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91470 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
