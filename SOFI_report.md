# SOFI

**Generated** : 2026-07-29T00:31:26.285568+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.74  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — SOFI earnings (J-0 sess · earnings)  
> ↳ spot $16.74 (+1.0% vs entrée) · entrée $16.57 · stop $15.82 · T1 $16.82 · R/R 0.33  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk -0.039 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.048 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.52–$16.62 (mid $16.57)
- Spot actuel : $16.74 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $15.82 (stop swing_plan-based (-3.87%))
- Targets : T1 $16.82 · R/R 0.33 | T2 $17.07 · R/R 0.67 | T3 $17.31 · R/R 0.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.82


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : $-0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 35 % | T3 14 %
- Kelly (position) : f* 0.194 | ¼-Kelly 0.048 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.3 | bear 15.3 | side 64.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.016% → cible +1.496% / stop −4.5%, p_fill 76%, n_eff≈30.5) : P(cible|rempli) **53%** · **EV/risk -0.039** (×p_fill ; si rempli -0.23% du capital)
  - **swing** (entrée dip −2.236% → cible +3.344% / stop −1.672%, p_fill 64%, n_eff≈26.4) : P(cible|rempli) **36%** · **EV/risk +0.000** (×p_fill ; si rempli +0.00% du capital)
  - **deep** (entrée dip −3.457% → cible +4.729% / stop −2.364%, p_fill 59%, n_eff≈22.6) : P(cible|rempli) **34%** · **EV/risk -0.018** (×p_fill ; si rempli -0.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.39% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.17%
- Profil de vol intra : ouverture 3.052% vs midi 0.913% vs clôture 0.996% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 66% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.306% ; recovery-V 20%
- **σ réalisé intraday** 2.899% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 16.96 (VA 16.84–17.0 ; dernier close 16.87)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 50% · rebond 72% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.84% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 46% (gap-down >1% 26% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.68%) · haut méd +0.73% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −1.06% (p90 −2.93%) · haut méd +0.98% · range méd 2.33%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.28%) · haut méd +1.2% · range méd 2.84%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.7%) · haut méd +1.31% · range méd 3.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.87 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (122/159) · gap 32% · délai 0.0min · rebond 55% (66/122) (MFE +1.22%)
   - −1.0% : fill 30min 54% · séance 68% (111/159) · gap 26% · délai 1.0min · rebond 63% (70/111) (MFE +1.34%)
   - −1.5% : fill 30min 48% · séance 64% (101/159) · gap 17% · délai 9.0min · rebond 67% (65/101) (MFE +1.76%)
   - −2.0% : fill 30min 39% · séance 50% (75/159) · gap 11% · délai 4.6min · rebond 72% (51/75) (MFE +1.84%)
   - −3.0% : fill 30min 16% · séance 37% (56/159) · gap 2% · délai 36.8min · rebond 66% (39/56) (MFE +1.48%)
   - −4.0% : fill 30min 8% · séance 22% (38/159) · gap 1% · délai 56.0min · rebond 58% (24/38) (MFE +1.43%)
   - −5.0% : fill 30min 3% · séance 8% (18/159) · gap 1% · délai 58.2min · rebond 48% (10/18) (MFE +0.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.79%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.92%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.99%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=664 jambes) : jambe baissière méd −1.12% (p90 −2.78%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 97% (64/65) · rebond 66% (41/64)
      · −2.0% : fill 83% (52/65) · rebond 74% (38/52)
      · −3.0% : fill 68% (42/65) · rebond 76% (32/42)
      · −4.0% : fill 36% (27/65) · rebond 69% (20/27)
      · −5.0% : fill 18% (13/65) · rebond 47% (8/13)
   - **flat** (24 séances) :
      · −1.0% : fill 48% (14/24) · rebond 30% (7/14)
      · −2.0% : fill 31% (8/24) · rebond 36% (3/8)
      · −3.0% : fill 24% (6/24) · rebond 32% (3/6)
      · −4.0% : fill 17% (4/24) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/24) · rebond 0% (0/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 48% (33/70) · rebond 67% (22/33)
      · −2.0% : fill 25% (15/70) · rebond 78% (10/15)
      · −3.0% : fill 13% (8/70) · rebond 39% (4/8)
      · −4.0% : fill 10% (7/70) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/70) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 53% si les 15 1res min sont vertes (74 cas) · 29% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 76% si début vert vs 11% si rouge (base 41% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.56% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.76% → **scale +1.69% / runner +2.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **11%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.38%** (au-delà de la MAE q10 -3.38%), cible rebond +1.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +3.49%] · haut q95 +3.82% · bas q05 -3.53%
   - 60min (n=160) : retour [-3.16% .. +3.37%] · haut q95 +4.02% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.58% .. +3.62%] · haut q95 +4.55% · bas q05 -4.81%
   - 4h (n=160) : retour [-3.93% .. +4.27%] · haut q95 +5.63% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.63% .. +3.88%] · haut q95 +5.68% · bas q05 -5.09%
   - session (n=160) : retour [-4.55% .. +4.83%] · haut q95 +5.68% · bas q05 -5.3%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — SOFI earnings (J-0 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — SOFI earnings (J-0 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — SOFI earnings (J-0 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 41.8  _(momentum baissier)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -0.18  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 16.5%
- **ATR** : 0.83 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.167  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 17.68 · MA50 17.16 · MA200 21.48  _(prix < MA20)_
- **Dist MA** : MA20 -5.3% · MA50 -2.5% · MA200 -22.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83607 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
