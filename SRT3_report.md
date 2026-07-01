# SRT3

**Generated** : 2026-07-01T21:37:49.513138+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €229.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €229.40 (+2.6% vs entrée) · entrée €223.67 · stop €220.18 · T1 €230.64 · R/R 2.0  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk 0.051 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €222.27–€225.06 (mid €223.67)
- Spot actuel : €229.40 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €220.18 (stop swing_plan-based (-4.02%))
- Targets : T1 €230.64 · R/R 2.0 | T2 €237.62 · R/R 4.0 | T3 €244.59 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €220.18


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : €0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.0 | bear 16.9 | side 33.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 459.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.134% → cible +1.395% / stop −3.0%, p_fill 58%, n_eff≈25.4) : P(cible|rempli) **39%** · **EV/risk -0.014** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −2.5% → cible +3.118% / stop −1.559%, p_fill 46%, n_eff≈18.6) : P(cible|rempli) **39%** · **EV/risk +0.051** (×p_fill ; si rempli +0.17% du capital)
  - **deep** (entrée dip −3.86% → cible +4.41% / stop −2.205%, p_fill 46%, n_eff≈17.2) : P(cible|rempli) **24%** · **EV/risk -0.157** (×p_fill ; si rempli -0.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→71% · +2.0%→45% · +3.0%→25% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.59%) · excursion haute méd. +1.84% / basse méd. −1.97%
- Profil de vol intra : ouverture 2.038% vs midi 0.884% vs clôture 1.017% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑1%/↓0% ; spike-down 54% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr 0.014)_ ; drift intra méd. 0.056% ; recovery-V 23%
- **σ réalisé intraday** 2.451% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 62% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 227.6712 (VA 226.9812–228.5337 ; dernier close 227.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 67% · **stop −2.61%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 53% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.81%) · haut méd +0.5% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.52% (p90 −1.89%) · haut méd +0.66% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.03%) · haut méd +0.77% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.41%) · haut méd +0.82% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 227.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 75% (122/159) · gap 28% · délai 0.2min · rebond 51% (57/122) (MFE +1.02%)
   - −1.0% : fill 30min 43% · séance 63% (102/159) · gap 17% · délai 0.6min · rebond 57% (57/102) (MFE +1.15%)
   - −1.5% : fill 30min 32% · séance 58% (90/159) · gap 11% · délai 7.0min · rebond 67% (55/90) (MFE +1.56%)
   - −2.0% : fill 30min 22% · séance 42% (68/159) · gap 6% · délai 19.3min · rebond 59% (43/68) (MFE +1.34%)
   - −3.0% : fill 30min 6% · séance 24% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 13% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.14% (p90 −1.88%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.91%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.18% (p90 −2.2%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=414 jambes) : jambe baissière méd −1.04% (p90 −2.37%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 84% (62/75) · rebond 66% (39/62)
      · −2.0% : fill 59% (42/75) · rebond 62% (28/42)
      · −3.0% : fill 41% (29/75) · rebond 56% (17/29)
      · −4.0% : fill 22% (16/75) · rebond 71% (12/16)
      · −5.0% : fill 11% (7/75) · rebond 92% (6/7)
   - **flat** (36 séances) :
      · −1.0% : fill 59% (20/36) · rebond 40% (9/20)
      · −2.0% : fill 44% (14/36) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/36) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/36) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/36) · rebond 44% (2/3)
   - **gap-up** (48 séances) :
      · −1.0% : fill 39% (20/48) · rebond 52% (9/20)
      · −2.0% : fill 19% (12/48) · rebond 72% (8/12)
      · −3.0% : fill 6% (5/48) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/48) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/48) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 61% si les 15 1res min sont vertes (89 cas) · 42% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 78% si début vert vs 30% si rouge (base 53% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -0.87% (q20 -1.84%) → **SL/trailing à −1.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +2.32% → **scale +1.2% / runner +2.32%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **30%** (continue à baisser 49%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.21% .. +2.11%] · haut q95 +2.65% · bas q05 -2.77%
   - 60min (n=160) : retour [-2.52% .. +2.32%] · haut q95 +2.81% · bas q05 -3.19%
   - 2h (n=160) : retour [-2.27% .. +2.61%] · haut q95 +3.11% · bas q05 -3.25%
   - 4h (n=160) : retour [-2.72% .. +2.68%] · haut q95 +3.3% · bas q05 -3.54%
   - 6h (n=160) : retour [-2.73% .. +3.51%] · haut q95 +4.0% · bas q05 -3.94%
   - session (n=160) : retour [-3.64% .. +4.71%] · haut q95 +5.64% · bas q05 -4.53%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.21%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.0  _(neutre)_
- **ADX** : 13.3  _(pas de tendance nette)_
- **MACD** : hist 0.278  _(bullish_recent)_
- **BB** : %B 0.54 · largeur 16.9%
- **ATR** : 9.77 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.151  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 228.03 · MA50 225.93 · MA200 229.35  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 +1.5% · MA200 +0.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (96126 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
