# SOFI

**Generated** : 2026-07-01T00:23:08.919494+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.93  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $17.93 (+6.7% vs entrée) · entrée $16.81 · stop $16.45 · T1 $17.53 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.072 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 215 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.67–$16.96 (mid $16.81)
- Spot actuel : $17.93 (+6.7% au-dessus de la zone — repli à attendre)
- Stop : $16.45 (stop swing_plan-based (-8.23%))
- Targets : T1 $17.53 · R/R 2.0 | T2 $18.24 · R/R 3.97 | T3 $18.96 · R/R 5.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.45


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : $-0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 18 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 28.2 | bear 30.0 | side 41.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 287.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.832% → cible +1.905% / stop −5.0%, p_fill 43%, n_eff≈16.0) : P(cible|rempli) **64%** · **EV/risk +0.087** (×p_fill ; si rempli +1.02% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→45% · +3.0%→34% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.64%) · excursion haute méd. +1.85% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.972% vs midi 0.932% vs clôture 1.016% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; momentum — autocorr 0.033)_ ; drift intra méd. 0.277% ; recovery-V 32%
- **σ réalisé intraday** 3.215% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 51% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 17.8708 (VA 17.8122–18.1242 ; dernier close 18.18)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 72% · **stop −3.94%** sous le fill (sous le bruit) · cible +2.35% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 50% (gap-down >1% 28% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.89%) · haut méd +0.63% · range méd 1.67%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −3.19%) · haut méd +0.95% · range méd 2.32%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.25%) · haut méd +1.14% · range méd 2.75%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.4%) · haut méd +1.43% · range méd 3.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.18 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (124/159) · gap 35% · délai 0.0min · rebond 63% (71/124) (MFE +1.55%)
   - −1.0% : fill 30min 52% · séance 69% (112/159) · gap 28% · délai 0.1min · rebond 67% (72/112) (MFE +1.56%)
   - −1.5% : fill 30min 44% · séance 63% (101/159) · gap 20% · délai 1.3min · rebond 68% (65/101) (MFE +1.97%)
   - −2.0% : fill 30min 38% · séance 48% (75/159) · gap 11% · délai 1.8min · rebond 72% (52/75) (MFE +2.35%)
   - −3.0% : fill 30min 21% · séance 33% (54/159) · gap 3% · délai 10.5min · rebond 73% (39/54) (MFE +1.64%)
   - −4.0% : fill 30min 10% · séance 22% (38/159) · gap 2% · délai 64.4min · rebond 61% (24/38) (MFE +1.43%)
   - −5.0% : fill 30min 4% · séance 12% (22/159) · gap 1% · délai 59.1min · rebond 48% (12/22) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −1.89%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −1.92%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=676 jambes) : jambe baissière méd −1.11% (p90 −2.76%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 96% (66/68) · rebond 66% (42/66)
      · −2.0% : fill 78% (52/68) · rebond 71% (38/52)
      · −3.0% : fill 62% (41/68) · rebond 74% (30/41)
      · −4.0% : fill 42% (28/68) · rebond 65% (20/28)
      · −5.0% : fill 23% (15/68) · rebond 47% (9/15)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (30/67) · rebond 78% (20/30)
      · −2.0% : fill 20% (14/67) · rebond 82% (9/14)
      · −3.0% : fill 5% (7/67) · rebond 71% (5/7)
      · −4.0% : fill 5% (7/67) · rebond 64% (4/7)
      · −5.0% : fill 3% (5/67) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (72 cas) · 35% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 70% si début vert vs 20% si rouge (base 45% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **70%** · continue >prix actuel 44% ; creux résiduel méd -2.09% (q20 -4.17%) → **SL/trailing à −4.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.43% / q75 +2.41% → **scale +1.43% / runner +2.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **20%** (continue à baisser 51%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.15% .. +3.68%] · haut q95 +4.01% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.25% .. +3.68%] · haut q95 +4.59% · bas q05 -4.22%
   - 2h (n=160) : retour [-3.85% .. +3.87%] · haut q95 +5.18% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.91% .. +4.62%] · haut q95 +5.68% · bas q05 -4.96%
   - 6h (n=160) : retour [-4.27% .. +3.88%] · haut q95 +5.71% · bas q05 -5.53%
   - session (n=160) : retour [-4.04% .. +5.18%] · haut q95 +5.72% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.39 · part idiosyncratique 0.61
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.1  _(momentum haussier)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist 0.1  _(pas de croisement recent)_
- **BB** : %B 0.8 · largeur 15.3%
- **ATR** : 0.91 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.056  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 54.2  _(transition)_
- **MA** : MA20 17.14 · MA50 16.91 · MA200 22.42  _(prix > MA20)_
- **Dist MA** : MA20 +4.6% · MA50 +6.0% · MA200 -20.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89349 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
