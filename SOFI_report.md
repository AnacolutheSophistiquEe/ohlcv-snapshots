# SOFI

**Generated** : 2026-06-29T00:22:31.169077+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.88  

> 🟡 **WAIT-FOR-DIP** — spot +3.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $17.88 (+3.1% vs entrée) · entrée $17.35 · stop $16.13 · T1 $18.35 · R/R 0.82  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.075 _(réel 5 s)_ (GBM -0.014) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −7.0% cohérent avec le bruit 5 s (EV-optimal ≈ −7.0%)  

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

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.27–$17.42 (mid $17.35)
- Spot actuel : $17.88 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $16.13 (stop swing_plan-based (-12.29%))
- Targets : T1 $18.35 · R/R 0.82 | T2 $18.40 · R/R 0.86 | T3 $18.44 · R/R 0.89
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.13


## Edge, scénarios & sizing

- EV/risk : -0.014 | EV/share : $-0.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.085 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.2 | bear 27.0 | side 53.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 393.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.989% → cible +5.814% / stop −7.0%, p_fill 35%, n_eff≈14.5) : P(cible|rempli) **0%** · **EV/risk +0.075** (×p_fill ; si rempli +1.48% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→70% · +2.0%→46% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.64%) · excursion haute méd. +1.89% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.991% vs midi 0.933% vs clôture 1.025% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 65% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; momentum — autocorr 0.044)_ ; drift intra méd. 0.296% ; recovery-V 34%
- **σ réalisé intraday** 3.209% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 49% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 17.8105 (VA 17.5575–17.9485 ; dernier close 17.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 71% · **stop −3.95%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 52% (gap-down >1% 28% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.9%) · haut méd +0.64% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −3.19%) · haut méd +0.96% · range méd 2.34%
- Excursion ouverture 30min (n=160) : bas méd −1.18% (p90 −3.27%) · haut méd +1.15% · range méd 2.81%
- Excursion ouverture 60min (n=160) : bas méd −1.41% (p90 −3.38%) · haut méd +1.44% · range méd 3.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (124/159) · gap 36% · délai 0.0min · rebond 62% (70/124) (MFE +1.54%)
   - −1.0% : fill 30min 53% · séance 68% (112/159) · gap 28% · délai 0.1min · rebond 66% (71/112) (MFE +1.46%)
   - −1.5% : fill 30min 45% · séance 62% (101/159) · gap 20% · délai 1.2min · rebond 68% (65/101) (MFE +1.95%)
   - −2.0% : fill 30min 38% · séance 47% (75/159) · gap 11% · délai 1.7min · rebond 71% (52/75) (MFE +2.23%)
   - −3.0% : fill 30min 21% · séance 34% (55/159) · gap 4% · délai 10.6min · rebond 73% (40/55) (MFE +1.66%)
   - −4.0% : fill 30min 10% · séance 23% (39/159) · gap 2% · délai 64.3min · rebond 62% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 5% · séance 12% (22/159) · gap 1% · délai 59.1min · rebond 48% (12/22) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −1.89%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −1.92%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=682 jambes) : jambe baissière méd −1.12% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 66% (42/67)
      · −2.0% : fill 78% (53/69) · rebond 71% (39/53)
      · −3.0% : fill 62% (42/69) · rebond 74% (31/42)
      · −4.0% : fill 42% (29/69) · rebond 65% (21/29)
      · −5.0% : fill 23% (15/69) · rebond 47% (9/15)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (72 cas) · 36% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 68% si début vert vs 26% si rouge (base 46% · écart 42 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **68%** · continue >prix actuel 43% ; creux résiduel méd -2.12% (q20 -4.06%) → **SL/trailing à −4.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.45% / q75 +2.64% → **scale +1.45% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **26%** (continue à baisser 50%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.0%** (au-delà de la MAE q10 -3.0%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.22% .. +3.69%] · haut q95 +4.01% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.25% .. +3.68%] · haut q95 +4.62% · bas q05 -4.26%
   - 2h (n=160) : retour [-3.86% .. +3.89%] · haut q95 +5.21% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.93% .. +4.62%] · haut q95 +5.68% · bas q05 -4.96%
   - 6h (n=160) : retour [-4.3% .. +3.89%] · haut q95 +5.71% · bas q05 -5.55%
   - session (n=160) : retour [-4.05% .. +5.18%] · haut q95 +5.72% · bas q05 -6.16%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 66.8  _(momentum haussier)_
- **ADX** : 20.9  _(pas de tendance nette)_
- **MACD** : hist 0.077  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 16.6%
- **ATR** : 0.97 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.028  _(neutre)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 56.6  _(transition)_
- **MA** : MA20 17.18 · MA50 16.95 · MA200 22.49  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +5.5% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89563 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
