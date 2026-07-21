# 267260

**Generated** : 2026-07-21T00:15:17.222140+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩752000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩752000.00 (+0.4% vs entrée) · entrée ₩748648.67 · stop ₩688756.77 · T1 ₩767908.78 · R/R 0.32  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.183 _(réel 5 s)_ (GBM -0.162) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -35 % hors [0,100] (R² max 0.02). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩745297.33–₩752000.00 (mid ₩748648.67)
- Spot actuel : ₩752000.00 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : ₩688756.77 (stop swing_plan-based (-4.0%))
- Targets : T1 ₩767908.78 · R/R 0.32 | T2 ₩787168.90 · R/R 0.64 | T3 ₩806429.02 · R/R 0.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩688756.77


## Edge, scénarios & sizing

- EV/risk : -0.162 | EV/share : ₩-9684.633 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 75.9 | side 17.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.446% → cible +2.573% / stop −8.0%, p_fill 96%, n_eff≈38.8) : P(cible|rempli) **31%** · **EV/risk -0.183** (×p_fill ; si rempli -1.52% du capital)
  - **swing** (entrée dip −0.988% → cible +5.753% / stop −3.042%, p_fill 94%, n_eff≈36.7) : P(cible|rempli) **12%** · **EV/risk -0.615** (×p_fill ; si rempli -2.00% du capital)
  - **deep** (entrée dip −1.451% → cible +8.135% / stop −4.068%, p_fill 92%, n_eff≈35.3) : P(cible|rempli) **22%** · **EV/risk -0.374** (×p_fill ; si rempli -1.66% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→45% · +3.0%→29% · +5.0%→9% · +8.0%→5%
- Range intraday médian 5.91% (p90 10.49%) · excursion haute méd. +1.85% / basse méd. −3.42%
- Profil de vol intra : ouverture 3.944% vs midi 1.038% vs clôture 1.132% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -1.862% ; recovery-V 16%
- **σ réalisé intraday** 4.836% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 79% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 797525.0 (VA 787025.0–797525.0 ; dernier close 796000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 82% · **stop −4.27%** sous le fill (sous le bruit) · cible +1.94% · R/R 0.45 (high win-rate)
- Gaps overnight (n=134) : méd. 1.12% · baisse 37% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=135) : bas méd −1.51% (p90 −3.67%) · haut méd +0.92% · range méd 2.64%
- Excursion ouverture 15min (n=135) : bas méd −1.71% (p90 −4.69%) · haut méd +1.06% · range méd 3.27%
- Excursion ouverture 30min (n=135) : bas méd −2.09% (p90 −4.94%) · haut méd +1.08% · range méd 3.66%
- Excursion ouverture 60min (n=135) : bas méd −2.47% (p90 −5.63%) · haut méd +1.13% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 796000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (95/134) · gap 29% · délai 0.1min · rebond 53% (53/95) (MFE +1.19%)
   - −1.0% : fill 30min 54% · séance 69% (88/134) · gap 21% · délai 0.3min · rebond 53% (51/88) (MFE +1.01%)
   - −1.5% : fill 30min 47% · séance 62% (75/134) · gap 14% · délai 0.6min · rebond 67% (49/75) (MFE +1.28%)
   - −2.0% : fill 30min 42% · séance 58% (68/134) · gap 9% · délai 1.0min · rebond 68% (46/68) (MFE +1.7%)
   - −3.0% : fill 30min 30% · séance 48% (53/134) · gap 7% · délai 5.7min · rebond 75% (36/53) (MFE +1.58%)
   - −4.0% : fill 30min 22% · séance 41% (44/134) · gap 3% · délai 16.6min · rebond 78% (35/44) (MFE +2.23%)
   - −5.0% : fill 30min 12% · séance 33% (34/134) · gap 2% · délai 65.9min · rebond 82% (26/34) (MFE +1.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −3.31%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.56%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −5.2%) → stop au-delà de −3.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=654 jambes) : jambe baissière méd −1.34% (p90 −3.63%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 98% (44/45) · rebond 46% (23/44)
      · −2.0% : fill 90% (37/45) · rebond 62% (22/37)
      · −3.0% : fill 78% (31/45) · rebond 73% (20/31)
      · −4.0% : fill 67% (27/45) · rebond 80% (22/27)
      · −5.0% : fill 55% (20/45) · rebond 81% (15/20)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 49% (30/72) · rebond 64% (21/30)
      · −2.0% : fill 35% (19/72) · rebond 71% (15/19)
      · −3.0% : fill 25% (11/72) · rebond 73% (8/11)
      · −4.0% : fill 23% (10/72) · rebond 82% (8/10)
      · −5.0% : fill 16% (7/72) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 34% en base · 50% si les 15 1res min sont vertes (64 cas) · 22% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=135) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 75% si début vert vs 11% si rouge (base 34% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **75%** · continue >prix actuel 42% ; creux résiduel méd -1.63% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.28% → **scale +1.21% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **11%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.25%** (au-delà de la MAE q10 -5.25%), cible rebond +1.76% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-5.28% .. +3.01%] · haut q95 +4.41% · bas q05 -5.69%
   - 60min (n=135) : retour [-5.61% .. +3.33%] · haut q95 +4.61% · bas q05 -6.04%
   - 2h (n=135) : retour [-7.04% .. +3.67%] · haut q95 +5.69% · bas q05 -7.45%
   - 4h (n=135) : retour [-6.95% .. +3.31%] · haut q95 +5.56% · bas q05 -8.26%
   - 6h (n=135) : retour [-6.97% .. +4.17%] · haut q95 +7.65% · bas q05 -8.87%
   - session (n=135) : retour [-7.16% .. +3.94%] · haut q95 +7.65% · bas q05 -9.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.7  _(momentum baissier)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist -9746.416  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 36.9%
- **ATR** : 75500.0 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.226  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 892600.0 · MA50 1032360.11 · MA200 915203.25  _(prix < MA20)_
- **Dist MA** : MA20 -15.8% · MA50 -27.2% · MA200 -17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84278 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
