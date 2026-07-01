# SOFI

**Generated** : 2026-07-01T22:02:14.819343+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.44  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $18.44 (+3.6% vs entrée) · entrée $17.80 · stop $16.56 · T1 $18.75 · R/R 0.77  
> ↳ P(T1 av. stop) 10 % · EV/risk -0.014 · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −7.0% cohérent avec le bruit 5 s (EV-optimal ≈ −7.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 329 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.74–$17.87 (mid $17.80)
- Spot actuel : $18.44 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : $16.56 (stop swing_plan-based (-13.2%))
- Targets : T1 $18.75 · R/R 0.77 | T2 $18.77 · R/R 0.78 | T3 $18.79 · R/R 0.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.56


## Edge, scénarios & sizing

- EV/risk : -0.014 | EV/share : $-0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.0 | bear 16.7 | side 53.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→45% · +3.0%→34% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.37% (p90 6.64%) · excursion haute méd. +1.85% / basse méd. −2.15%
- Profil de vol intra : ouverture 2.953% vs midi 0.946% vs clôture 1.012% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 67% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; neutre — autocorr 0.025)_ ; drift intra méd. 0.225% ; recovery-V 30%
- **σ réalisé intraday** 3.181% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 53% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 18.0451 (VA 17.8539–18.0834 ; dernier close 17.93)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 73% · **stop −3.91%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 52% (gap-down >1% 27% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.89%) · haut méd +0.63% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.18%) · haut méd +0.94% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.23%) · haut méd +1.12% · range méd 2.72%
- Excursion ouverture 60min (n=160) : bas méd −1.41% (p90 −3.39%) · haut méd +1.34% · range méd 3.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.93 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (124/159) · gap 34% · délai 0.0min · rebond 62% (70/124) (MFE +1.54%)
   - −1.0% : fill 30min 53% · séance 70% (112/159) · gap 27% · délai 0.2min · rebond 68% (72/112) (MFE +1.46%)
   - −1.5% : fill 30min 45% · séance 64% (101/159) · gap 19% · délai 1.5min · rebond 69% (65/101) (MFE +1.95%)
   - −2.0% : fill 30min 37% · séance 49% (75/159) · gap 11% · délai 1.9min · rebond 73% (52/75) (MFE +2.33%)
   - −3.0% : fill 30min 20% · séance 32% (54/159) · gap 3% · délai 10.5min · rebond 73% (39/54) (MFE +1.64%)
   - −4.0% : fill 30min 9% · séance 22% (38/159) · gap 2% · délai 64.4min · rebond 61% (24/38) (MFE +1.43%)
   - −5.0% : fill 30min 4% · séance 12% (22/159) · gap 1% · délai 59.1min · rebond 48% (12/22) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −1.88%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −1.92%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=673 jambes) : jambe baissière méd −1.11% (p90 −2.75%) · ~9.0 jambes/séance
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
      · −1.0% : fill 43% (29/66) · rebond 78% (19/29)
      · −2.0% : fill 20% (13/66) · rebond 81% (8/13)
      · −3.0% : fill 5% (7/66) · rebond 71% (5/7)
      · −4.0% : fill 5% (7/66) · rebond 64% (4/7)
      · −5.0% : fill 3% (5/66) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (72 cas) · 34% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 68% si début vert vs 24% si rouge (base 44% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **68%** · continue >prix actuel 43% ; creux résiduel méd -2.12% (q20 -4.06%) → **SL/trailing à −4.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.45% / q75 +2.64% → **scale +1.45% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **24%** (continue à baisser 50%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.99%** (au-delà de la MAE q10 -2.99%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +3.68%] · haut q95 +4.01% · bas q05 -3.96%
   - 60min (n=160) : retour [-3.24% .. +3.67%] · haut q95 +4.57% · bas q05 -4.17%
   - 2h (n=160) : retour [-3.85% .. +3.86%] · haut q95 +5.15% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.88% .. +4.62%] · haut q95 +5.68% · bas q05 -4.96%
   - 6h (n=160) : retour [-4.24% .. +3.88%] · haut q95 +5.71% · bas q05 -5.52%
   - session (n=160) : retour [-4.04% .. +5.18%] · haut q95 +5.71% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 73.4  _(surachat)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist 0.122  _(pas de croisement recent)_
- **BB** : %B 0.95 · largeur 16.4%
- **ATR** : 0.91 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.039  _(neutre)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 17.18 · MA50 16.89 · MA200 22.38  _(prix > MA20)_
- **Dist MA** : MA20 +7.3% · MA50 +9.2% · MA200 -17.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89522 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
