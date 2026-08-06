# RHM

**Generated** : 2026-08-06T00:01:53.966417+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · €1198.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1198.80 (+1.4% vs entrée) · entrée €1182.75 · stop €1159.10 · T1 €1199.28 · R/R 0.7  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.151 _(réel 5 s)_ (GBM 0.046) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 241 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1179.44–€1186.06 (mid €1182.75)
- Spot actuel : €1198.80 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €1159.10 (stop swing_plan-based (-6.59%))
- Targets : T1 €1199.28 · R/R 0.7 | T2 €1215.81 · R/R 1.4 | T3 €1232.34 · R/R 2.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1159.10


## Edge, scénarios & sizing

- EV/risk : 0.046 | EV/share : €1.101 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 32 % | T3 10 %
- Kelly (position) : f* 0.088 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 65.5 | bear 5.0 | side 29.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.337% → cible +1.398% / stop −2.0%, p_fill 47%, n_eff≈23.3) : P(cible|rempli) **37%** · **EV/risk -0.151** (×p_fill ; si rempli -0.64% du capital)
  - **swing** (entrée dip −2.942% → cible +3.125% / stop −3.759%, p_fill 33%, n_eff≈16.0) : P(cible|rempli) **47%** · **EV/risk -0.051** (×p_fill ; si rempli -0.57% du capital)
  - **deep** (entrée dip −4.547% → cible +4.42% / stop −5.733%, p_fill 41%, n_eff≈18.4) : P(cible|rempli) **37%** · **EV/risk -0.141** (×p_fill ; si rempli -1.98% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→50% · +3.0%→29% · +5.0%→2% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.65%) · excursion haute méd. +2.05% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.503% vs midi 0.894% vs clôture 1.091% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; neutre — autocorr -0.017)_ ; drift intra méd. 0.141% ; recovery-V 49%
- **σ réalisé intraday** 2.879% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 77% / bas 57% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 1182.4625 (VA 1166.2775–1189.9325 ; dernier close 1176.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 38% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.75%) · haut méd +0.65% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.02%) · haut méd +0.72% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.75%) · haut méd +0.88% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −3.05%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1176.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 73% (118/159) · gap 25% · délai 0.3min · rebond 59% (63/118) (MFE +1.34%)
   - −1.0% : fill 30min 44% · séance 64% (107/159) · gap 11% · délai 4.3min · rebond 61% (63/107) (MFE +1.4%)
   - −1.5% : fill 30min 29% · séance 52% (81/159) · gap 6% · délai 18.2min · rebond 55% (43/81) (MFE +1.14%)
   - −2.0% : fill 30min 21% · séance 43% (71/159) · gap 4% · délai 30.4min · rebond 64% (44/71) (MFE +1.38%)
   - −3.0% : fill 30min 9% · séance 27% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 19% (27/159) · gap 1% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 9% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −1.73%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.5% (p90 −1.77%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −1.94%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=483 jambes) : jambe baissière méd −1.07% (p90 −2.55%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (48/50) · rebond 63% (28/48)
      · −2.0% : fill 78% (38/50) · rebond 64% (25/38)
      · −3.0% : fill 50% (26/50) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/50) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/50) · rebond 76% (6/8)
   - **flat** (48 séances) :
      · −1.0% : fill 67% (35/48) · rebond 69% (23/35)
      · −2.0% : fill 29% (17/48) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/48) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/48) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/48) · rebond 22% (1/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 41% (24/61) · rebond 49% (12/24)
      · −2.0% : fill 28% (16/61) · rebond 62% (9/16)
      · −3.0% : fill 15% (9/61) · rebond 66% (6/9)
      · −4.0% : fill 8% (4/61) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 72% si les 15 1res min sont vertes (82 cas) · 43% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 82% si début vert vs 30% si rouge (base 56% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **82%** · continue >prix actuel 53% ; creux résiduel méd -0.92% (q20 -2.1%) → **SL/trailing à −2.1%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.44% / q75 +2.24% → **scale +1.44% / runner +2.24%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **30%** (continue à baisser 54%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.52%** (au-delà de la MAE q10 -4.52%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +2.91%] · haut q95 +3.63% · bas q05 -3.47%
   - 60min (n=160) : retour [-3.04% .. +2.87%] · haut q95 +3.69% · bas q05 -4.4%
   - 2h (n=160) : retour [-3.42% .. +2.97%] · haut q95 +4.0% · bas q05 -4.64%
   - 4h (n=160) : retour [-3.8% .. +3.13%] · haut q95 +4.56% · bas q05 -4.98%
   - 6h (n=160) : retour [-4.37% .. +3.6%] · haut q95 +4.56% · bas q05 -5.59%
   - session (n=160) : retour [-6.16% .. +4.38%] · haut q95 +4.81% · bas q05 -6.28%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 90.0  _(surachat)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist 27.745  _(pas de croisement recent)_
- **BB** : %B 0.96 · largeur 30.5%
- **ATR** : 43.74 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 27.5  _(marche directionnel)_
- **MA** : MA20 1050.02 · MA50 1106.95 · MA200 1453.63  _(prix > MA20)_
- **Dist MA** : MA20 +14.2% · MA50 +8.3% · MA200 -17.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92080 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
