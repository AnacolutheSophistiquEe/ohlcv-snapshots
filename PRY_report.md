# PRY

**Generated** : 2026-08-12T00:10:46.634081+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €127.95  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €127.95 (+2.1% vs entrée) · entrée €125.34 · stop €119.18 · T1 €129.59 · R/R 0.69  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.347 _(réel 5 s)_ (GBM -0.021) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €124.49–€126.19 (mid €125.34)
- Spot actuel : €127.95 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €119.18 (stop swing_plan-based (-6.86%))
- Targets : T1 €129.59 · R/R 0.69 | T2 €133.85 · R/R 1.38 | T3 €138.10 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €119.18


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : €-0.132 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 20 % | T3 6 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.6 | bear 51.1 | side 24.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 384.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.924% → cible +1.519% / stop −8.0%, p_fill 84%, n_eff≈31.9) : P(cible|rempli) **52%** · **EV/risk -0.042** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −2.045% → cible +3.395% / stop −4.915%, p_fill 73%, n_eff≈26.5) : P(cible|rempli) **30%** · **EV/risk -0.347** (×p_fill ; si rempli -2.33% du capital)
  - **deep** (entrée dip −3.158% → cible +4.802% / stop −7.458%, p_fill 68%, n_eff≈25.2) : P(cible|rempli) **17%** · **EV/risk -0.422** (×p_fill ; si rempli -4.65% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→65% · +2.0%→41% · +3.0%→29% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.35% (p90 6.51%) · excursion haute méd. +1.5% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.433% vs midi 0.859% vs clôture 1.202% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.849% ; recovery-V 27%
- **σ réalisé intraday** 2.912% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 68% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 126.647 (VA 125.321–127.055 ; dernier close 126.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=149) : méd. 0.35% · baisse 40% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=150) : bas méd −0.79% (p90 −2.34%) · haut méd +0.43% · range méd 1.5%
- Excursion ouverture 15min (n=150) : bas méd −1.0% (p90 −2.91%) · haut méd +0.62% · range méd 1.8%
- Excursion ouverture 30min (n=150) : bas méd −1.04% (p90 −3.18%) · haut méd +0.72% · range méd 1.99%
- Excursion ouverture 60min (n=150) : bas méd −1.23% (p90 −3.37%) · haut méd +0.86% · range méd 2.23%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 126.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 71% (108/149) · gap 26% · délai 0.2min · rebond 62% (68/108) (MFE +1.27%)
   - −1.0% : fill 30min 48% · séance 64% (92/149) · gap 19% · délai 0.3min · rebond 61% (56/92) (MFE +1.57%)
   - −1.5% : fill 30min 35% · séance 55% (80/149) · gap 15% · délai 2.0min · rebond 53% (44/80) (MFE +1.14%)
   - −2.0% : fill 30min 25% · séance 46% (65/149) · gap 10% · délai 5.4min · rebond 61% (41/65) (MFE +1.34%)
   - −3.0% : fill 30min 13% · séance 35% (47/149) · gap 4% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 20% (25/149) · gap 1% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 1% · séance 13% (17/149) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.02%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −2.07%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −2.02%) → stop au-delà de −1.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=474 jambes) : jambe baissière méd −1.07% (p90 −2.61%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (27 séances) :
      · −1.0% : fill 69% (15/27) · rebond 71% (10/15)
      · −2.0% : fill 45% (8/27) · rebond 86% (6/8)
      · −3.0% : fill 22% (5/27) · rebond 40% (2/5)
      · −4.0% : fill 10% (3/27) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/27) · rebond 25% (1/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 45% (30/70) · rebond 74% (20/30)
      · −2.0% : fill 29% (19/70) · rebond 43% (9/19)
      · −3.0% : fill 23% (13/70) · rebond 63% (8/13)
      · −4.0% : fill 12% (6/70) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/70) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 48% en base · 70% si les 15 1res min sont vertes (69 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=150) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 25% si rouge (base 48% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **83%** · continue >prix actuel 64% ; creux résiduel méd -1.32% (q20 -2.06%) → **SL/trailing à −2.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.41% / q75 +2.58% → **scale +1.41% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 65%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-2.96% .. +2.77%] · haut q95 +3.47% · bas q05 -3.41%
   - 60min (n=150) : retour [-3.39% .. +2.21%] · haut q95 +3.97% · bas q05 -3.59%
   - 2h (n=150) : retour [-3.69% .. +2.46%] · haut q95 +4.1% · bas q05 -4.82%
   - 4h (n=150) : retour [-3.67% .. +3.21%] · haut q95 +4.42% · bas q05 -4.94%
   - 6h (n=150) : retour [-3.75% .. +3.69%] · haut q95 +4.69% · bas q05 -5.57%
   - session (n=150) : retour [-4.56% .. +4.37%] · haut q95 +5.7% · bas q05 -6.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 31.9  _(tendance etablie)_
- **MACD** : hist 1.214  _(bullish_recent)_
- **BB** : %B 0.61 · largeur 17.8%
- **ATR** : 6.16 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.037  _(neutre)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 54.6  _(transition)_
- **MA** : MA20 125.42 · MA50 136.92 · MA200 111.53  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -6.5% · MA200 +14.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94451 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
