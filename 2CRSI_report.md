# AL2SI

**Generated** : 2026-07-24T00:09:15.953303+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €26.42  

> 🟡 **WAIT-FOR-DIP** — spot +5.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €26.42 (+5.8% vs entrée) · entrée €24.96 · stop €23.79 · T1 €26.04 · R/R 0.92  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk 0.02 _(réel 5 s)_ (GBM -0.035) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.69% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €24.74–€25.17 (mid €24.96)
- Spot actuel : €26.42 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : €23.79 (stop swing_plan-based (-16.61%))
- Targets : T1 €26.04 · R/R 0.92 | T2 €27.13 · R/R 1.85 | T3 €28.21 · R/R 2.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.79


## Edge, scénarios & sizing

- EV/risk : -0.035 | EV/share : €-0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.091 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.4 | bear 6.9 | side 75.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.542% → cible +4.351% / stop −4.688%, p_fill 52%, n_eff≈19.8) : P(cible|rempli) **32%** · **EV/risk +0.020** (×p_fill ; si rempli +0.18% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→42% · +8.0%→24%
- Range intraday médian 8.82% (p90 22.19%) · excursion haute méd. +4.16% / basse méd. −4.26%
- Profil de vol intra : ouverture 5.915% vs midi 1.738% vs clôture 2.037% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (154 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.028% ; recovery-V 32%
- **σ réalisé intraday** 8.327% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 66% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 28.4945 (VA 28.0095–28.9795 ; dernier close 27.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 88% · **stop −5.92%** sous le fill (sous le bruit) · cible +2.78% · R/R 0.47 (high win-rate)
- Gaps overnight (n=153) : méd. 0.2% · baisse 40% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=154) : bas méd −1.24% (p90 −5.23%) · haut méd +1.04% · range méd 3.08%
- Excursion ouverture 15min (n=154) : bas méd −1.64% (p90 −5.86%) · haut méd +1.55% · range méd 4.51%
- Excursion ouverture 30min (n=154) : bas méd −1.72% (p90 −5.86%) · haut méd +2.42% · range méd 4.97%
- Excursion ouverture 60min (n=154) : bas méd −2.29% (p90 −6.96%) · haut méd +2.74% · range méd 6.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 82% (120/153) · gap 30% · délai 0.3min · rebond 70% (81/120) (MFE +3.35%)
   - −1.0% : fill 30min 63% · séance 81% (115/153) · gap 23% · délai 0.4min · rebond 73% (81/115) (MFE +2.68%)
   - −1.5% : fill 30min 55% · séance 76% (105/153) · gap 15% · délai 1.0min · rebond 74% (71/105) (MFE +2.37%)
   - −2.0% : fill 30min 48% · séance 68% (92/153) · gap 10% · délai 1.4min · rebond 69% (62/92) (MFE +1.94%)
   - −3.0% : fill 30min 35% · séance 58% (75/153) · gap 7% · délai 8.1min · rebond 86% (63/75) (MFE +2.34%)
   - −4.0% : fill 30min 29% · séance 50% (64/153) · gap 4% · délai 19.1min · rebond 74% (49/64) (MFE +2.92%)
   - −5.0% : fill 30min 20% · séance 46% (56/153) · gap 4% · délai 42.4min · rebond 88% (52/56) (MFE +2.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.94% (p90 −5.56%) → stop au-delà de −3.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.25% (p90 −5.57%) → stop au-delà de −4.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −5.64%) → stop au-delà de −3.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1498 jambes) : jambe baissière méd −1.26% (p90 −3.62%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 98% (50/54) · rebond 70% (34/50)
      · −2.0% : fill 88% (43/54) · rebond 60% (27/43)
      · −3.0% : fill 80% (38/54) · rebond 80% (31/38)
      · −4.0% : fill 70% (33/54) · rebond 77% (27/33)
      · −5.0% : fill 63% (30/54) · rebond 83% (27/30)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (66 séances) :
      · −1.0% : fill 64% (39/66) · rebond 69% (26/39)
      · −2.0% : fill 52% (29/66) · rebond 72% (20/29)
      · −3.0% : fill 42% (23/66) · rebond 89% (19/23)
      · −4.0% : fill 37% (18/66) · rebond 64% (11/18)
      · −5.0% : fill 36% (15/66) · rebond 88% (14/15)
- **P(clôture VERTE) selon le drive 15min** (n=154) : 46% en base · 59% si les 15 1res min sont vertes (74 cas) · 36% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=154) : COUDE à **31min** → P(séance verte=clôture>ouverture) 71% si début vert vs 22% si rouge (base 46% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **71%** · continue >prix actuel 53% ; creux résiduel méd -2.68% (q20 -7.48%) → **SL/trailing à −7.48%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +7.4% → **scale +3.7% / runner +7.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=154) : retour [-5.27% .. +6.7%] · haut q95 +8.59% · bas q05 -7.74%
   - 60min (n=154) : retour [-6.0% .. +9.37%] · haut q95 +9.93% · bas q05 -8.22%
   - 2h (n=154) : retour [-6.03% .. +10.08%] · haut q95 +11.38% · bas q05 -8.32%
   - 4h (n=154) : retour [-8.8% .. +10.34%] · haut q95 +12.65% · bas q05 -11.42%
   - 6h (n=154) : retour [-8.59% .. +14.45%] · haut q95 +17.09% · bas q05 -11.59%
   - session (n=154) : retour [-10.06% .. +17.23%] · haut q95 +18.35% · bas q05 -15.74%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.6  _(survente)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -0.028  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 59.2%
- **ATR** : 3.9 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.008  _(neutre)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 30.7 · MA50 38.58 · MA200 24.35  _(prix < MA20)_
- **Dist MA** : MA20 -13.9% · MA50 -31.5% · MA200 +8.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90288 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
