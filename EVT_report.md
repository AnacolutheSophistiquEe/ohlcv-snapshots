# EVT

**Generated** : 2026-07-22T00:04:22.586612+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €3.56 (+2.9% vs entrée) · entrée €3.46 · stop €3.34 · T1 €3.59 · R/R 1.08  
> ↳ P(T1 av. stop) 26 % · EV/risk 0.085 · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.44–€3.49 (mid €3.46)
- Spot actuel : €3.56 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €3.34 (stop swing_plan-based (-9.71%))
- Targets : T1 €3.59 · R/R 1.08 | T2 €3.71 · R/R 2.08 | T3 €3.84 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.34


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : €0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.051 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 23.2 | bear 67.6 | side 9.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.695% → cible +3.588% / stop −3.499%, p_fill 30%, n_eff≈11.8) : P(cible|rempli) **27%** · **EV/risk -0.021** (×p_fill ; si rempli -0.24% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→75% · +2.0%→49% · +3.0%→31% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.43% (p90 7.64%) · excursion haute méd. +1.98% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.898% vs midi 1.201% vs clôture 1.272% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.084 ; mean-reverting — autocorr -0.113)_ ; drift intra méd. 0.044% ; recovery-V 44%
- **σ réalisé intraday** 3.642% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 57% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 3.641 (VA 3.5894–3.6474 ; dernier close 3.592)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 76% · rebond 68% · **stop −3.22%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.07% · baisse 53% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.83%) · haut méd +0.63% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.83%) · haut méd +0.85% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −2.83%) · haut méd +0.96% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.27%) · haut méd +0.97% · range méd 2.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.592 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 85% (133/159) · gap 33% · délai 0.2min · rebond 65% (89/133) (MFE +1.49%)
   - −1.0% : fill 30min 55% · séance 76% (120/159) · gap 22% · délai 0.6min · rebond 68% (80/120) (MFE +1.6%)
   - −1.5% : fill 30min 40% · séance 61% (98/159) · gap 18% · délai 1.6min · rebond 63% (64/98) (MFE +1.78%)
   - −2.0% : fill 30min 30% · séance 49% (78/159) · gap 11% · délai 14.3min · rebond 64% (52/78) (MFE +1.42%)
   - −3.0% : fill 30min 17% · séance 32% (55/159) · gap 6% · délai 3.8min · rebond 64% (41/55) (MFE +1.66%)
   - −4.0% : fill 30min 9% · séance 20% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 6% · séance 10% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.28%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.04%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −1.97%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=806 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 95% (62/65) · rebond 70% (39/62)
      · −2.0% : fill 67% (45/65) · rebond 60% (29/45)
      · −3.0% : fill 40% (33/65) · rebond 69% (25/33)
      · −4.0% : fill 27% (20/65) · rebond 56% (14/20)
      · −5.0% : fill 17% (13/65) · rebond 57% (9/13)
   - **flat** (41 séances) :
      · −1.0% : fill 88% (32/41) · rebond 71% (25/32)
      · −2.0% : fill 53% (17/41) · rebond 73% (12/17)
      · −3.0% : fill 37% (10/41) · rebond 62% (7/10)
      · −4.0% : fill 22% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 11% (3/41) · rebond 27% (1/3)
   - **gap-up** (53 séances) :
      · −1.0% : fill 44% (26/53) · rebond 56% (16/26)
      · −2.0% : fill 24% (16/53) · rebond 61% (11/16)
      · −3.0% : fill 18% (12/53) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/53) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 58% en base · 68% si les 15 1res min sont vertes (77 cas) · 48% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 70% si début vert vs 46% si rouge (base 58% · écart 24 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **70%** · continue >prix actuel 52% ; creux résiduel méd -1.71% (q20 -3.01%) → **SL/trailing à −3.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.53% → **scale +1.29% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **46%** (continue à baisser 39%) → **RÉDUIRE ~54%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.04%** (au-delà de la MAE q10 -5.04%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.22% .. +2.83%] · haut q95 +3.54% · bas q05 -4.59%
   - 60min (n=160) : retour [-3.81% .. +3.33%] · haut q95 +4.63% · bas q05 -5.37%
   - 2h (n=160) : retour [-3.88% .. +3.28%] · haut q95 +4.64% · bas q05 -5.4%
   - 4h (n=160) : retour [-3.22% .. +3.6%] · haut q95 +4.64% · bas q05 -6.71%
   - 6h (n=160) : retour [-3.73% .. +3.49%] · haut q95 +5.21% · bas q05 -6.92%
   - session (n=160) : retour [-4.6% .. +4.36%] · haut q95 +6.62% · bas q05 -7.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : extreme
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

- **RSI** : 13.3  _(survente)_
- **ADX** : 31.6  _(tendance etablie)_
- **MACD** : hist -0.157  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 60.4%
- **ATR** : 0.31 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.149  _(accumulation)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 28.4  _(marche directionnel)_
- **MA** : MA20 4.56 · MA50 4.74 · MA200 5.42  _(prix < MA20)_
- **Dist MA** : MA20 -21.9% · MA50 -24.9% · MA200 -34.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90538 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
