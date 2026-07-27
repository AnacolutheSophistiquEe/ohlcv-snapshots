# SMR

**Generated** : 2026-07-27T00:27:57.424692+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $8.10 (+6.4% vs entrée) · entrée $7.61 · stop $7.40 · T1 $8.03 · R/R 2.0  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.15 _(réel 5 s)_ (GBM -0.192) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.2 % ≠ (strike 9.0 − spot 8.10)/spot = +11.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $7.53–$7.70 (mid $7.61)
- Spot actuel : $8.10 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : $7.40 (stop swing_plan-based (-8.66%))
- Targets : T1 $8.03 · R/R 2.0 | T2 $8.46 · R/R 4.05 | T3 $8.88 · R/R 6.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.40


## Edge, scénarios & sizing

- EV/risk : -0.192 | EV/share : $-0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 17 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 70.6 | bear 17.6 | side 11.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.746% → cible +2.491% / stop −2.441%, p_fill 46%, n_eff≈20.5) : P(cible|rempli) **22%** · **EV/risk -0.172** (×p_fill ; si rempli -0.92% du capital)
  - **swing** (entrée dip −6.044% → cible +5.569% / stop −2.784%, p_fill 48%, n_eff≈18.1) : P(cible|rempli) **24%** · **EV/risk -0.150** (×p_fill ; si rempli -0.87% du capital)
  - **deep** (entrée dip −9.341% → cible +7.875% / stop −3.937%, p_fill 37%, n_eff≈13.5) : P(cible|rempli) **6%** · **EV/risk -0.298** (×p_fill ; si rempli -3.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→65% · +3.0%→57% · +5.0%→40% · +8.0%→18%
- Range intraday médian 7.8% (p90 12.61%) · excursion haute méd. +3.54% / basse méd. −3.09%
- Profil de vol intra : ouverture 5.088% vs midi 1.539% vs clôture 1.783% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. -0.251% ; recovery-V 30%
- **σ réalisé intraday** 4.798% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 67% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 8.3329 (VA 8.1879–8.4597 ; dernier close 8.09)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 53% · rebond 75% · **stop −6.04%** sous le fill (sous le bruit) · cible +2.36% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. -0.63% · baisse 59% (gap-down >1% 43% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.25%) · haut méd +1.07% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.46% (p90 −3.78%) · haut méd +1.41% · range méd 3.5%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.69%) · haut méd +1.97% · range méd 4.32%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −5.95%) · haut méd +2.63% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.09 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (131/159) · gap 51% · délai 0.0min · rebond 68% (82/131) (MFE +1.75%)
   - −1.0% : fill 30min 69% · séance 79% (125/159) · gap 43% · délai 0.0min · rebond 69% (84/125) (MFE +2.09%)
   - −1.5% : fill 30min 64% · séance 76% (119/159) · gap 38% · délai 0.0min · rebond 76% (88/119) (MFE +2.23%)
   - −2.0% : fill 30min 59% · séance 70% (112/159) · gap 29% · délai 0.2min · rebond 70% (81/112) (MFE +2.39%)
   - −3.0% : fill 30min 46% · séance 61% (100/159) · gap 10% · délai 2.9min · rebond 73% (81/100) (MFE +2.57%)
   - −4.0% : fill 30min 36% · séance 53% (84/159) · gap 5% · délai 11.2min · rebond 75% (64/84) (MFE +2.36%)
   - −5.0% : fill 30min 25% · séance 41% (62/159) · gap 3% · délai 19.7min · rebond 68% (45/62) (MFE +1.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.69%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.71%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −2.85%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1178 jambes) : jambe baissière méd −1.39% (p90 −3.22%) · ~14.6 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 71% (57/84)
      · −2.0% : fill 94% (80/84) · rebond 77% (61/80)
      · −3.0% : fill 84% (75/84) · rebond 75% (62/75)
      · −4.0% : fill 73% (65/84) · rebond 80% (53/65)
      · −5.0% : fill 57% (46/84) · rebond 71% (35/46)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (11/14) · rebond 54% (7/11)
      · −2.0% : fill 69% (9/14) · rebond 22% (4/9)
      · −3.0% : fill 66% (7/14) · rebond 47% (4/7)
      · −4.0% : fill 66% (7/14) · rebond 55% (3/7)
      · −5.0% : fill 56% (6/14) · rebond 80% (5/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 47% (30/61) · rebond 70% (20/30)
      · −2.0% : fill 34% (23/61) · rebond 66% (16/23)
      · −3.0% : fill 26% (18/61) · rebond 80% (15/18)
      · −4.0% : fill 19% (12/61) · rebond 67% (8/12)
      · −5.0% : fill 14% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 60% si les 15 1res min sont vertes (72 cas) · 30% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 67% si début vert vs 16% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **67%** · continue >prix actuel 42% ; creux résiduel méd -3.01% (q20 -5.01%) → **SL/trailing à −5.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.24% / q75 +4.03% → **scale +2.24% / runner +4.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.87%** (au-delà de la MAE q10 -6.87%), cible rebond +1.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.49% .. +4.91%] · haut q95 +6.56% · bas q05 -6.02%
   - 60min (n=160) : retour [-6.47% .. +5.54%] · haut q95 +7.8% · bas q05 -7.81%
   - 2h (n=160) : retour [-7.66% .. +7.64%] · haut q95 +11.12% · bas q05 -8.68%
   - 4h (n=160) : retour [-8.37% .. +7.77%] · haut q95 +11.1% · bas q05 -10.59%
   - 6h (n=160) : retour [-8.05% .. +8.4%] · haut q95 +11.36% · bas q05 -10.71%
   - session (n=160) : retour [-8.0% .. +10.19%] · haut q95 +11.49% · bas q05 -10.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.8  _(momentum baissier)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist 0.048  _(bullish_recent)_
- **BB** : %B 0.25 · largeur 36.6%
- **ATR** : 0.64 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.052  _(distribution)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 8.93 · MA50 10.26 · MA200 17.24  _(prix < MA20)_
- **Dist MA** : MA20 -9.3% · MA50 -21.0% · MA200 -53.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84055 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
