# SAF

**Generated** : 2026-06-29T00:06:36.791278+00:00  
**Santé technique** : 10/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €332.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)  
> ↳ spot €332.70 (+7.4% vs entrée) · entrée €309.73 · stop €305.95 · T1 €317.27 · R/R 1.99  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.114 · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 129 % hors [0,100] (R² max 0.19). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 74.9 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €308.22–€311.24 (mid €309.73)
- Spot actuel : €332.70 (+7.4% au-dessus de la zone — repli à attendre)
- Stop : €305.95 (stop swing_plan-based (-8.04%))
- Targets : T1 €317.27 · R/R 1.99 | T2 €324.82 · R/R 3.99 | T3 €332.37 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.95


## Edge, scénarios & sizing

- EV/risk : 0.114 | EV/share : €0.431 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 16 % | T3 10 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 16.2 | bear 39.6 | side 44.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 333.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→60% · +2.0%→35% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.8% (p90 5.22%) · excursion haute méd. +1.21% / basse méd. −1.11%
- Profil de vol intra : ouverture 1.706% vs midi 0.672% vs clôture 0.792% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 36% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.027)_ ; drift intra méd. 0.468% ; recovery-V 17%
- **σ réalisé intraday** 1.953% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 47% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 338.575 (VA 336.575–339.825 ; dernier close 334.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 21% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=136) : méd. -0.06% · baisse 52% (gap-down >1% 15% · >2% 2%)
- Excursion ouverture 5min (n=137) : bas méd −0.37% (p90 −1.46%) · haut méd +0.25% · range méd 0.93%
- Excursion ouverture 15min (n=137) : bas méd −0.44% (p90 −1.66%) · haut méd +0.44% · range méd 1.19%
- Excursion ouverture 30min (n=137) : bas méd −0.51% (p90 −1.92%) · haut méd +0.57% · range méd 1.31%
- Excursion ouverture 60min (n=137) : bas méd −0.69% (p90 −1.98%) · haut méd +0.69% · range méd 1.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 334.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 68% (97/136) · gap 29% · délai 0.2min · rebond 38% (36/97) (MFE +0.74%)
   - −1.0% : fill 30min 41% · séance 50% (69/136) · gap 15% · délai 0.4min · rebond 40% (24/69) (MFE +0.58%)
   - −1.5% : fill 30min 27% · séance 42% (59/136) · gap 6% · délai 6.7min · rebond 35% (19/59) (MFE +0.89%)
   - −2.0% : fill 30min 14% · séance 33% (43/136) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 5% · séance 21% (26/136) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 10% (12/136) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/136) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.95%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=164 jambes) : jambe baissière méd −1.08% (p90 −2.73%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 76% (38/49) · rebond 39% (14/38)
      · −2.0% : fill 56% (27/49) · rebond 51% (13/27)
      · −3.0% : fill 35% (16/49) · rebond 58% (9/16)
      · −4.0% : fill 16% (8/49) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/49) · rebond 0% (0/2)
   - **flat** (36 séances) :
      · −1.0% : fill 45% (15/36) · rebond 55% (7/15)
      · −2.0% : fill 23% (7/36) · rebond 50% (3/7)
      · −3.0% : fill 11% (4/36) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/36) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (51 séances) :
      · −1.0% : fill 24% (16/51) · rebond 26% (3/16)
      · −2.0% : fill 15% (9/51) · rebond 34% (3/9)
      · −3.0% : fill 11% (6/51) · rebond 55% (4/6)
      · −4.0% : fill 8% (3/51) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/51) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 50% en base · 66% si les 15 1res min sont vertes (61 cas) · 34% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=137) : COUDE à **44min** → P(séance verte=clôture>ouverture) 78% si début vert vs 21% si rouge (base 50% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **78%** · continue >prix actuel 61% ; creux résiduel méd -0.57% (q20 -1.5%) → **SL/trailing à −1.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.83% → **scale +1.29% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **21%** (continue à baisser 48%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.53%** (au-delà de la MAE q10 -2.53%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-1.82% .. +1.93%] · haut q95 +2.66% · bas q05 -2.31%
   - 60min (n=137) : retour [-1.83% .. +2.46%] · haut q95 +3.18% · bas q05 -2.63%
   - 2h (n=137) : retour [-2.26% .. +2.39%] · haut q95 +3.39% · bas q05 -2.93%
   - 4h (n=137) : retour [-2.16% .. +2.82%] · haut q95 +3.49% · bas q05 -3.04%
   - 6h (n=137) : retour [-2.27% .. +3.5%] · haut q95 +3.79% · bas q05 -3.18%
   - session (n=137) : retour [-2.99% .. +3.67%] · haut q95 +4.29% · bas q05 -4.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.5% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.77 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 74.9  _(surachat)_
- **ADX** : 27.5  _(tendance etablie)_
- **MACD** : hist 2.183  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 23.1%
- **ATR** : 9.56 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 33.6  _(marche directionnel)_
- **MA** : MA20 313.75 · MA50 294.38 · MA200 299.66  _(prix > MA20)_
- **Dist MA** : MA20 +6.0% · MA50 +13.0% · MA200 +11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93107 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
