# SOFI

**Generated** : 2026-07-02T22:00:44.131534+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $18.24  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $18.24 (+7.6% vs entrée) · entrée $16.95 · stop $16.64 · T1 $17.58 · R/R 2.03  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.051 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 359 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.82–$17.08 (mid $16.95)
- Spot actuel : $18.24 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : $16.64 (stop swing_plan-based (-8.8%))
- Targets : T1 $17.58 · R/R 2.03 | T2 $18.22 · R/R 4.1 | T3 $18.85 · R/R 6.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.64


## Edge, scénarios & sizing

- EV/risk : -0.051 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 34.2 | bear 26.8 | side 39.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 383.0 (= 21 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.215% → cible +1.668% / stop −4.5%, p_fill 23%, n_eff≈9.5) : P(cible|rempli) **76%** · **EV/risk +0.051** (×p_fill ; si rempli +0.99% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→45% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.37% (p90 6.64%) · excursion haute méd. +1.85% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.951% vs midi 0.943% vs clôture 1.011% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 65% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; neutre — autocorr 0.016)_ ; drift intra méd. 0.288% ; recovery-V 30%
- **σ réalisé intraday** 3.176% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 51% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 18.5397 (VA 18.4322–18.6472 ; dernier close 18.43)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 73% · **stop −3.9%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 51% (gap-down >1% 27% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.89%) · haut méd +0.63% · range méd 1.67%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −3.18%) · haut méd +0.95% · range méd 2.32%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.21%) · haut méd +1.14% · range méd 2.7%
- Excursion ouverture 60min (n=160) : bas méd −1.36% (p90 −3.39%) · haut méd +1.44% · range méd 3.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.43 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (123/159) · gap 34% · délai 0.0min · rebond 62% (70/123) (MFE +1.54%)
   - −1.0% : fill 30min 52% · séance 68% (111/159) · gap 27% · délai 0.3min · rebond 68% (72/111) (MFE +1.46%)
   - −1.5% : fill 30min 44% · séance 62% (100/159) · gap 19% · délai 1.4min · rebond 69% (65/100) (MFE +1.95%)
   - −2.0% : fill 30min 36% · séance 48% (74/159) · gap 11% · délai 1.9min · rebond 73% (51/74) (MFE +2.33%)
   - −3.0% : fill 30min 20% · séance 32% (53/159) · gap 3% · délai 10.4min · rebond 73% (38/53) (MFE +1.66%)
   - −4.0% : fill 30min 9% · séance 22% (37/159) · gap 2% · délai 64.3min · rebond 61% (23/37) (MFE +1.41%)
   - −5.0% : fill 30min 4% · séance 12% (21/159) · gap 1% · délai 58.3min · rebond 47% (11/21) (MFE +0.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −1.87%) → stop au-delà de −1.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.8%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.73%) → stop au-delà de −1.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=671 jambes) : jambe baissière méd −1.11% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 68% (43/67)
      · −2.0% : fill 79% (53/69) · rebond 72% (39/53)
      · −3.0% : fill 59% (41/69) · rebond 74% (30/41)
      · −4.0% : fill 40% (28/69) · rebond 65% (20/28)
      · −5.0% : fill 22% (15/69) · rebond 47% (9/15)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 41% (28/66) · rebond 78% (19/28)
      · −2.0% : fill 19% (12/66) · rebond 81% (7/12)
      · −3.0% : fill 5% (6/66) · rebond 69% (4/6)
      · −4.0% : fill 5% (6/66) · rebond 62% (3/6)
      · −5.0% : fill 3% (4/66) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (72 cas) · 36% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 69% si début vert vs 24% si rouge (base 45% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **69%** · continue >prix actuel 45% ; creux résiduel méd -1.98% (q20 -4.01%) → **SL/trailing à −4.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.54% → **scale +1.55% / runner +2.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **24%** (continue à baisser 50%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.99%** (au-delà de la MAE q10 -2.99%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.01% .. +3.67%] · haut q95 +4.01% · bas q05 -3.95%
   - 60min (n=160) : retour [-3.23% .. +3.67%] · haut q95 +4.54% · bas q05 -4.12%
   - 2h (n=160) : retour [-3.85% .. +3.84%] · haut q95 +5.12% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.83% .. +4.62%] · haut q95 +5.68% · bas q05 -4.95%
   - 6h (n=160) : retour [-4.21% .. +3.88%] · haut q95 +5.71% · bas q05 -5.49%
   - session (n=160) : retour [-4.03% .. +5.17%] · haut q95 +5.71% · bas q05 -6.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 66.1  _(momentum haussier)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist 0.114  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 17.0%
- **ATR** : 0.94 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.02  _(neutre)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 17.26 · MA50 16.87 · MA200 22.33  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 +8.1% · MA200 -18.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88567 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
