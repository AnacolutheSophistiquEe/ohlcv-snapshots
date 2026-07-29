# EVT

**Generated** : 2026-07-29T00:04:17.569539+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.51  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €3.51 (+2.6% vs entrée) · entrée €3.42 · stop €3.31 · T1 €3.55 · R/R 1.18  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk 0.002 _(réel 5 s)_ (GBM 0.016) · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.40–€3.45 (mid €3.42)
- Spot actuel : €3.51 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €3.31 (stop swing_plan-based (-8.96%))
- Targets : T1 €3.55 · R/R 1.18 | T2 €3.67 · R/R 2.27 | T3 €3.79 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.31


## Edge, scénarios & sizing

- EV/risk : 0.016 | EV/share : €0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.1 | bear 69.9 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.362% → cible +3.539% / stop −3.501%, p_fill 35%, n_eff≈15.1) : P(cible|rempli) **25%** · **EV/risk +0.002** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −5.209% → cible +7.915% / stop −3.957%, p_fill 22%, n_eff≈8.4) : P(cible|rempli) **2%** · **EV/risk -0.122** (×p_fill ; si rempli -2.22% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→28% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.36% (p90 7.64%) · excursion haute méd. +1.87% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.852% vs midi 1.193% vs clôture 1.28% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.077 ; mean-reverting — autocorr -0.128)_ ; drift intra méd. -0.135% ; recovery-V 40%
- **σ réalisé intraday** 3.563% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 67% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 3.4693 (VA 3.4494–3.4921 ; dernier close 3.454)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 75% · rebond 68% · **stop −3.19%** sous le fill (sous le bruit) · cible +1.67% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.73%) · haut méd +0.68% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.81%) · haut méd +0.85% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.83%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −3.19%) · haut méd +0.98% · range méd 2.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.454 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 84% (133/159) · gap 32% · délai 0.2min · rebond 66% (88/133) (MFE +1.57%)
   - −1.0% : fill 30min 55% · séance 75% (120/159) · gap 22% · délai 0.4min · rebond 68% (79/120) (MFE +1.67%)
   - −1.5% : fill 30min 40% · séance 61% (99/159) · gap 16% · délai 1.2min · rebond 63% (64/99) (MFE +1.49%)
   - −2.0% : fill 30min 29% · séance 49% (79/159) · gap 10% · délai 14.3min · rebond 63% (52/79) (MFE +1.42%)
   - −3.0% : fill 30min 16% · séance 33% (56/159) · gap 5% · délai 30.4min · rebond 68% (42/56) (MFE +1.66%)
   - −4.0% : fill 30min 8% · séance 18% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 6% · séance 9% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −2.56%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.95%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −1.97%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=814 jambes) : jambe baissière méd −1.07% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 95% (60/63) · rebond 71% (37/60)
      · −2.0% : fill 64% (44/63) · rebond 60% (28/44)
      · −3.0% : fill 38% (32/63) · rebond 68% (24/32)
      · −4.0% : fill 26% (20/63) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/63) · rebond 57% (9/13)
   - **flat** (42 séances) :
      · −1.0% : fill 84% (34/42) · rebond 68% (26/34)
      · −2.0% : fill 56% (19/42) · rebond 68% (13/19)
      · −3.0% : fill 42% (12/42) · rebond 73% (9/12)
      · −4.0% : fill 18% (5/42) · rebond 20% (1/5)
      · −5.0% : fill 9% (3/42) · rebond 27% (1/3)
   - **gap-up** (54 séances) :
      · −1.0% : fill 41% (26/54) · rebond 56% (16/26)
      · −2.0% : fill 22% (16/54) · rebond 61% (11/16)
      · −3.0% : fill 17% (12/54) · rebond 57% (9/12)
      · −4.0% : fill 7% (5/54) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 68% si les 15 1res min sont vertes (77 cas) · 44% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 70% si début vert vs 43% si rouge (base 56% · écart 27 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **70%** · continue >prix actuel 50% ; creux résiduel méd -1.84% (q20 -2.74%) → **SL/trailing à −2.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.39% / q75 +2.38% → **scale +1.39% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **43%** (continue à baisser 39%) → **RÉDUIRE ~57%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.89%** (au-delà de la MAE q10 -4.89%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.77% .. +2.53%] · haut q95 +3.51% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.21% .. +3.33%] · haut q95 +4.53% · bas q05 -3.78%
   - 2h (n=160) : retour [-3.49% .. +3.25%] · haut q95 +4.63% · bas q05 -4.36%
   - 4h (n=160) : retour [-3.16% .. +3.33%] · haut q95 +4.63% · bas q05 -5.72%
   - 6h (n=160) : retour [-3.54% .. +3.34%] · haut q95 +5.2% · bas q05 -5.58%
   - session (n=160) : retour [-4.45% .. +4.18%] · haut q95 +6.35% · bas q05 -6.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 15.1  _(survente)_
- **ADX** : 38.3  _(tendance etablie)_
- **MACD** : hist -0.06  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 75.1%
- **ATR** : 0.3 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.064  _(accumulation)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 29.1  _(marche directionnel)_
- **MA** : MA20 4.19 · MA50 4.62 · MA200 5.34  _(prix < MA20)_
- **Dist MA** : MA20 -16.4% · MA50 -24.1% · MA200 -34.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90356 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
