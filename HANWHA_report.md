# 012450

**Generated** : 2026-07-09T19:17:21.334148+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩957000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩957000.00 (+3.4% vs entrée) · entrée ₩925486.26 · stop ₩896625.59 · T1 ₩983207.61 · R/R 2.0  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.124 _(réel 5 s)_ (GBM 0.141) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩913941.99–₩937030.53 (mid ₩925486.26)
- Spot actuel : ₩957000.00 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : ₩896625.59 (stop swing_plan-based (-6.31%))
- Targets : T1 ₩983207.61 · R/R 2.0 | T2 ₩1040928.95 · R/R 4.0 | T3 ₩1098650.29 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩896625.59


## Edge, scénarios & sizing

- EV/risk : 0.141 | EV/share : ₩4066.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 5 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 32.6 | bear 15.9 | side 51.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.5% → cible +2.789% / stop −8.0%, p_fill 86%, n_eff≈33.4) : P(cible|rempli) **30%** · **EV/risk -0.090** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −3.294% → cible +6.237% / stop −3.118%, p_fill 71%, n_eff≈28.0) : P(cible|rempli) **28%** · **EV/risk -0.124** (×p_fill ; si rempli -0.54% du capital)
  - **deep** (entrée dip −5.084% → cible +8.82% / stop −4.41%, p_fill 75%, n_eff≈27.7) : P(cible|rempli) **21%** · **EV/risk -0.306** (×p_fill ; si rempli -1.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→59% · +2.0%→41% · +3.0%→22% · +5.0%→11% · +8.0%→2%
- Range intraday médian 5.59% (p90 8.18%) · excursion haute méd. +1.75% / basse méd. −3.37%
- Profil de vol intra : ouverture 4.13% vs midi 1.032% vs clôture 0.989% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (129 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓2% ; spike-down 80% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.03)_ ; drift intra méd. -1.994% ; recovery-V 16%
- **σ réalisé intraday** 4.568% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 30% / bas 65% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 956775.0 (VA 931575.0–972525.0 ; dernier close 952000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 80% · **stop −4.17%** sous le fill (sous le bruit) · cible +2.44% · R/R 0.59 (high win-rate)
- Gaps overnight (n=128) : méd. 0.41% · baisse 31% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=129) : bas méd −1.64% (p90 −4.06%) · haut méd +0.73% · range méd 2.68%
- Excursion ouverture 15min (n=129) : bas méd −1.91% (p90 −4.87%) · haut méd +0.85% · range méd 3.45%
- Excursion ouverture 30min (n=129) : bas méd −2.53% (p90 −5.33%) · haut méd +0.86% · range méd 4.22%
- Excursion ouverture 60min (n=129) : bas méd −2.58% (p90 −5.67%) · haut méd +1.12% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 952000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (94/128) · gap 17% · délai 0.6min · rebond 47% (47/94) (MFE +0.73%)
   - −1.0% : fill 30min 56% · séance 72% (90/128) · gap 11% · délai 1.2min · rebond 56% (53/90) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 66% (83/128) · gap 5% · délai 3.3min · rebond 58% (46/83) (MFE +1.26%)
   - −2.0% : fill 30min 44% · séance 57% (68/128) · gap 4% · délai 5.2min · rebond 63% (41/68) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 46% (49/128) · gap 2% · délai 15.5min · rebond 70% (33/49) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 33% (37/128) · gap 2% · délai 14.4min · rebond 80% (30/37) (MFE +2.13%)
   - −5.0% : fill 30min 10% · séance 26% (28/128) · gap 2% · délai 49.5min · rebond 80% (23/28) (MFE +2.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.19%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.89%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.39%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=607 jambes) : jambe baissière méd −1.3% (p90 −3.46%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (23 séances) :
      · −1.0% : fill 98% (22/23) · rebond 50% (12/22)
      · −2.0% : fill 81% (17/23) · rebond 54% (9/17)
      · −3.0% : fill 70% (14/23) · rebond 67% (9/14)
      · −4.0% : fill 57% (12/23) · rebond 86% (10/12)
      · −5.0% : fill 47% (9/23) · rebond 76% (7/9)
   - **flat** (35 séances) :
      · −1.0% : fill 87% (30/35) · rebond 49% (16/30)
      · −2.0% : fill 72% (23/35) · rebond 66% (14/23)
      · −3.0% : fill 56% (15/35) · rebond 62% (9/15)
      · −4.0% : fill 56% (15/35) · rebond 68% (10/15)
      · −5.0% : fill 43% (11/35) · rebond 78% (9/11)
   - **gap-up** (70 séances) :
      · −1.0% : fill 55% (38/70) · rebond 65% (25/38)
      · −2.0% : fill 42% (28/70) · rebond 66% (18/28)
      · −3.0% : fill 32% (20/70) · rebond 80% (15/20)
      · −4.0% : fill 13% (10/70) · rebond 100% (10/10)
      · −5.0% : fill 11% (8/70) · rebond 92% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=129) : 31% en base · 60% si les 15 1res min sont vertes (44 cas) · 15% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=129) : COUDE à **54min** → P(séance verte=clôture>ouverture) 75% si début vert vs 9% si rouge (base 31% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 52min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=43) : tient le vert **75%** · continue >prix actuel 49% ; creux résiduel méd -2.29% (q20 -3.6%) → **SL/trailing à −3.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +2.15% → **scale +1.19% / runner +2.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **9%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.47%** (au-delà de la MAE q10 -4.47%), cible rebond +1.69% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=129) : retour [-4.75% .. +4.55%] · haut q95 +5.73% · bas q05 -6.05%
   - 60min (n=129) : retour [-5.27% .. +4.58%] · haut q95 +6.56% · bas q05 -6.59%
   - 2h (n=129) : retour [-7.27% .. +4.25%] · haut q95 +6.74% · bas q05 -8.0%
   - 4h (n=129) : retour [-7.06% .. +5.54%] · haut q95 +7.08% · bas q05 -8.22%
   - 6h (n=129) : retour [-7.15% .. +4.51%] · haut q95 +7.13% · bas q05 -8.63%
   - session (n=129) : retour [-7.23% .. +4.75%] · haut q95 +7.13% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -27.399  _(bearish_recent)_
- **BB** : %B 0.0 · largeur 25.5%
- **ATR** : 89357.14 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.146  _(distribution)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 1096400.0 · MA50 1181480.0 · MA200 1147817.86  _(prix < MA20)_
- **Dist MA** : MA20 -12.7% · MA50 -19.0% · MA200 -16.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84418 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
