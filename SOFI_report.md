# SOFI

**Generated** : 2026-06-26T21:58:45.381862+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.88  

> 🟡 **WAIT-FOR-DIP** — spot +3.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $17.88 (+3.1% vs entrée) · entrée $17.35 · stop $16.84 · T1 $18.35 · R/R 1.96  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.174 _(réel 5 s)_ (GBM -0.023) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 165 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.27–$17.42 (mid $17.35)
- Spot actuel : $17.88 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $16.84 (stop swing_plan-based (-12.29%))
- Targets : T1 $18.35 · R/R 1.96 | T2 $18.40 · R/R 2.06 | T3 $18.44 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.84


## Edge, scénarios & sizing

- EV/risk : -0.023 | EV/share : $-0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 19.2 | bear 27.0 | side 53.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 393.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.99% → cible +5.814% / stop −2.907%, p_fill 37%, n_eff≈14.5) : P(cible|rempli) **0%** · **EV/risk +0.174** (×p_fill ; si rempli +1.36% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→70% · +2.0%→46% · +3.0%→35% · +5.0%→9% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.64%) · excursion haute méd. +1.89% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.991% vs midi 0.939% vs clôture 1.014% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓1% ; spike-down 67% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; momentum — autocorr 0.044)_ ; drift intra méd. 0.062% ; recovery-V 34%
- **σ réalisé intraday** 3.217% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 51% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 17.3942 (VA 17.2647–17.4312 ; dernier close 17.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 71% · **stop −3.95%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 51% (gap-down >1% 27% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.9%) · haut méd +0.63% · range méd 1.67%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.19%) · haut méd +0.95% · range méd 2.36%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.28%) · haut méd +1.14% · range méd 2.84%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.39%) · haut méd +1.43% · range méd 3.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (124/159) · gap 34% · délai 0.0min · rebond 61% (69/124) (MFE +1.47%)
   - −1.0% : fill 30min 52% · séance 68% (112/159) · gap 27% · délai 0.1min · rebond 65% (71/112) (MFE +1.46%)
   - −1.5% : fill 30min 44% · séance 62% (101/159) · gap 19% · délai 1.3min · rebond 67% (65/101) (MFE +1.93%)
   - −2.0% : fill 30min 39% · séance 48% (76/159) · gap 11% · délai 1.7min · rebond 71% (53/76) (MFE +2.24%)
   - −3.0% : fill 30min 22% · séance 34% (56/159) · gap 4% · délai 10.6min · rebond 73% (41/56) (MFE +1.67%)
   - −4.0% : fill 30min 10% · séance 23% (40/159) · gap 2% · délai 64.4min · rebond 62% (26/40) (MFE +1.49%)
   - −5.0% : fill 30min 5% · séance 13% (22/159) · gap 1% · délai 59.1min · rebond 48% (12/22) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −1.91%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.98%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.85%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=684 jambes) : jambe baissière méd −1.12% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 65% (42/67)
      · −2.0% : fill 81% (54/69) · rebond 71% (40/54)
      · −3.0% : fill 64% (43/69) · rebond 74% (32/43)
      · −4.0% : fill 44% (30/69) · rebond 65% (22/30)
      · −5.0% : fill 24% (15/69) · rebond 47% (9/15)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 41% (29/66) · rebond 75% (19/29)
      · −2.0% : fill 17% (13/66) · rebond 76% (8/13)
      · −3.0% : fill 5% (7/66) · rebond 71% (5/7)
      · −4.0% : fill 5% (7/66) · rebond 64% (4/7)
      · −5.0% : fill 4% (5/66) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 54% si les 15 1res min sont vertes (72 cas) · 36% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 68% si début vert vs 21% si rouge (base 44% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **68%** · continue >prix actuel 42% ; creux résiduel méd -2.13% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +2.25% → **scale +1.28% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **21%** (continue à baisser 53%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.1%** (au-delà de la MAE q10 -3.1%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.29% .. +3.7%] · haut q95 +4.01% · bas q05 -3.98%
   - 60min (n=160) : retour [-3.26% .. +3.68%] · haut q95 +4.78% · bas q05 -4.29%
   - 2h (n=160) : retour [-3.86% .. +3.93%] · haut q95 +5.27% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.94% .. +4.43%] · haut q95 +5.66% · bas q05 -4.96%
   - 6h (n=160) : retour [-4.33% .. +3.91%] · haut q95 +5.7% · bas q05 -5.57%
   - session (n=160) : retour [-4.05% .. +4.65%] · haut q95 +5.72% · bas q05 -6.16%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.37 · part idiosyncratique 0.63
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 66.8  _(momentum haussier)_
- **ADX** : 20.9  _(pas de tendance nette)_
- **MACD** : hist 0.077  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 16.6%
- **ATR** : 0.97 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.029  _(neutre)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 56.6  _(transition)_
- **MA** : MA20 17.18 · MA50 16.95 · MA200 22.49  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +5.5% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (71997 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
