# RHM

**Generated** : 2026-07-01T21:36:12.470950+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1050.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €1050.60 (+6.4% vs entrée) · entrée €987.77 · stop €968.02 · T1 €1015.80 · R/R 1.42  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.024 · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €982.16–€993.38 (mid €987.77)
- Spot actuel : €1050.60 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : €968.02 (stop swing_plan-based (-14.75%))
- Targets : T1 €1015.80 · R/R 1.42 | T2 €1043.84 · R/R 2.84 | T3 €1071.87 · R/R 4.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €968.02


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : €-0.480 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.2 | bear 32.0 | side 58.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→49% · +3.0%→29% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.7%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.559% vs midi 0.904% vs clôture 1.018% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.089 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.619% ; recovery-V 42%
- **σ réalisé intraday** 2.967% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 73% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 983.6662 (VA 971.9913–994.1738 ; dernier close 992.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.35%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.08% · baisse 42% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.73%) · haut méd +0.58% · range méd 1.54%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −1.96%) · haut méd +0.8% · range méd 1.9%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −2.22%) · haut méd +0.98% · range méd 2.15%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.48%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 992.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (119/159) · gap 28% · délai 0.3min · rebond 56% (61/119) (MFE +1.22%)
   - −1.0% : fill 30min 47% · séance 72% (106/159) · gap 17% · délai 5.5min · rebond 61% (60/106) (MFE +1.42%)
   - −1.5% : fill 30min 30% · séance 55% (79/159) · gap 9% · délai 20.0min · rebond 56% (42/79) (MFE +1.24%)
   - −2.0% : fill 30min 23% · séance 46% (69/159) · gap 7% · délai 29.0min · rebond 66% (41/69) (MFE +1.38%)
   - −3.0% : fill 30min 10% · séance 29% (45/159) · gap 4% · délai 122.8min · rebond 65% (30/45) (MFE +1.47%)
   - −4.0% : fill 30min 5% · séance 20% (27/159) · gap 2% · délai 287.1min · rebond 51% (15/27) (MFE +1.05%)
   - −5.0% : fill 30min 2% · séance 11% (16/159) · gap 2% · délai 197.1min · rebond 49% (9/16) (MFE +0.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.38%) → stop au-delà de −1.16% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.63%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=467 jambes) : jambe baissière méd −1.15% (p90 −2.63%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 59% (24/48)
      · −2.0% : fill 80% (38/49) · rebond 72% (25/38)
      · −3.0% : fill 47% (27/49) · rebond 65% (19/27)
      · −4.0% : fill 34% (16/49) · rebond 54% (10/16)
      · −5.0% : fill 19% (10/49) · rebond 70% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 77% (36/50) · rebond 72% (24/36)
      · −2.0% : fill 32% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 19% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (22/60) · rebond 50% (12/22)
      · −2.0% : fill 30% (14/60) · rebond 54% (7/14)
      · −3.0% : fill 21% (8/60) · rebond 83% (6/8)
      · −4.0% : fill 9% (3/60) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/60) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (85 cas) · 33% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 77% si début vert vs 23% si rouge (base 49% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 44% ; creux résiduel méd -1.37% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.89% → **scale +1.19% / runner +1.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.19%** (au-delà de la MAE q10 -5.19%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.18%] · haut q95 +3.85% · bas q05 -3.12%
   - 60min (n=160) : retour [-2.85% .. +2.99%] · haut q95 +4.12% · bas q05 -3.46%
   - 2h (n=160) : retour [-3.41% .. +2.97%] · haut q95 +4.16% · bas q05 -4.0%
   - 4h (n=160) : retour [-3.4% .. +2.9%] · haut q95 +4.47% · bas q05 -4.51%
   - 6h (n=160) : retour [-4.53% .. +2.96%] · haut q95 +4.55% · bas q05 -5.7%
   - session (n=160) : retour [-6.67% .. +3.34%] · haut q95 +4.74% · bas q05 -7.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 31.4  _(tendance etablie)_
- **MACD** : hist -11.751  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 36.8%
- **ATR** : 62.83 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.121  _(distribution)_
- **Vol ratio** : 1.37  _(volume normal)_
- **Choppiness** : 39.6  _(transition)_
- **MA** : MA20 1124.48 · MA50 1206.63 · MA200 1553.9  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -12.9% · MA200 -32.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91459 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
