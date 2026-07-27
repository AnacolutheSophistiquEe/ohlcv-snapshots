# EVT

**Generated** : 2026-07-27T21:38:41.497062+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.42  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €3.42 (+1.8% vs entrée) · entrée €3.36 · stop €3.24 · T1 €3.48 · R/R 1.0  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.032 _(réel 5 s)_ (GBM 0.055) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.34–€3.39 (mid €3.36)
- Spot actuel : €3.42 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €3.24 (stop swing_plan-based (-7.75%))
- Targets : T1 €3.48 · R/R 1.0 | T2 €3.60 · R/R 2.0 | T3 €3.72 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.24


## Edge, scénarios & sizing

- EV/risk : 0.055 | EV/share : €0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.047 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.0 | bear 68.9 | side 9.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.813% → cible +3.513% / stop −3.501%, p_fill 50%, n_eff≈18.6) : P(cible|rempli) **20%** · **EV/risk -0.032** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −3.979% → cible +7.854% / stop −3.927%, p_fill 33%, n_eff≈11.6) : P(cible|rempli) **9%** · **EV/risk -0.150** (×p_fill ; si rempli -1.80% du capital)
  - **deep** (entrée dip −6.16% → cible +11.107% / stop −5.552%, p_fill 31%, n_eff≈12.1) : P(cible|rempli) **6%** · **EV/risk -0.098** (×p_fill ; si rempli -1.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→31% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.47% (p90 7.64%) · excursion haute méd. +1.87% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.861% vs midi 1.173% vs clôture 1.269% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.085 ; mean-reverting — autocorr -0.114)_ ; drift intra méd. -0.167% ; recovery-V 39%
- **σ réalisé intraday** 3.601% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 61% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 3.4529 (VA 3.444–3.4706 ; dernier close 3.424)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 62% · rebond 66% · **stop −3.05%** sous le fill (sous le bruit) · cible +1.78% · R/R 0.58 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 53% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −2.78%) · haut méd +0.56% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.83%) · haut méd +0.83% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −2.83%) · haut méd +0.94% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.23%) · haut méd +0.95% · range méd 2.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.424 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 85% (134/159) · gap 32% · délai 0.2min · rebond 64% (89/134) (MFE +1.49%)
   - −1.0% : fill 30min 56% · séance 78% (122/159) · gap 22% · délai 0.4min · rebond 67% (81/122) (MFE +1.6%)
   - −1.5% : fill 30min 42% · séance 62% (100/159) · gap 17% · délai 1.1min · rebond 66% (66/100) (MFE +1.78%)
   - −2.0% : fill 30min 31% · séance 51% (80/159) · gap 11% · délai 14.4min · rebond 63% (53/80) (MFE +1.42%)
   - −3.0% : fill 30min 17% · séance 34% (57/159) · gap 6% · délai 30.8min · rebond 68% (43/57) (MFE +1.66%)
   - −4.0% : fill 30min 9% · séance 19% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 6% · séance 10% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.72%) → stop au-delà de −1.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.04%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −1.97%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=807 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 95% (62/65) · rebond 70% (39/62)
      · −2.0% : fill 67% (45/65) · rebond 60% (29/45)
      · −3.0% : fill 40% (33/65) · rebond 69% (25/33)
      · −4.0% : fill 27% (20/65) · rebond 56% (14/20)
      · −5.0% : fill 17% (13/65) · rebond 57% (9/13)
   - **flat** (41 séances) :
      · −1.0% : fill 90% (34/41) · rebond 68% (26/34)
      · −2.0% : fill 60% (19/41) · rebond 68% (13/19)
      · −3.0% : fill 45% (12/41) · rebond 73% (9/12)
      · −4.0% : fill 19% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 10% (3/41) · rebond 27% (1/3)
   - **gap-up** (53 séances) :
      · −1.0% : fill 44% (26/53) · rebond 56% (16/26)
      · −2.0% : fill 24% (16/53) · rebond 61% (11/16)
      · −3.0% : fill 18% (12/53) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/53) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 68% si les 15 1res min sont vertes (76 cas) · 44% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 70% si début vert vs 43% si rouge (base 56% · écart 27 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **70%** · continue >prix actuel 52% ; creux résiduel méd -1.75% (q20 -3.02%) → **SL/trailing à −3.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.53% → **scale +1.29% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **43%** (continue à baisser 39%) → **RÉDUIRE ~57%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.88%** (au-delà de la MAE q10 -4.88%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.66%] · haut q95 +3.52% · bas q05 -4.29%
   - 60min (n=160) : retour [-3.24% .. +3.33%] · haut q95 +4.59% · bas q05 -4.3%
   - 2h (n=160) : retour [-3.49% .. +3.27%] · haut q95 +4.63% · bas q05 -4.64%
   - 4h (n=160) : retour [-3.21% .. +3.5%] · haut q95 +4.63% · bas q05 -6.35%
   - 6h (n=160) : retour [-3.69% .. +3.44%] · haut q95 +5.21% · bas q05 -6.34%
   - session (n=160) : retour [-4.57% .. +4.29%] · haut q95 +6.57% · bas q05 -6.77%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 10.5  _(survente)_
- **ADX** : 37.4  _(tendance etablie)_
- **MACD** : hist -0.085  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 74.0%
- **ATR** : 0.3 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.054  _(accumulation)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 29.9  _(marche directionnel)_
- **MA** : MA20 4.27 · MA50 4.65 · MA200 5.36  _(prix < MA20)_
- **Dist MA** : MA20 -19.8% · MA50 -26.3% · MA200 -36.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90103 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
