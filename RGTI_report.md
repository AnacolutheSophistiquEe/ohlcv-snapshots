# RGTI

**Generated** : 2026-08-01T20:22:03.054673+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $14.95  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $14.95 (+0.7% vs entrée) · entrée $14.85 · stop $14.12 · T1 $16.30 · R/R 1.99  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.176 _(réel 5 s)_ (GBM 0.019) · ¼-Kelly 0.046 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.89% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.75–$14.95 (mid $14.85)
- Spot actuel : $14.95 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : $14.12 (stop swing_plan-based (-10.01%))
- Targets : T1 $16.30 · R/R 1.99 | T2 $16.31 · R/R 2.0 | T3 $16.32 · R/R 2.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.12


## Edge, scénarios & sizing

- EV/risk : 0.019 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.183 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.2 | side 76.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.682% → cible +9.781% / stop −4.891%, p_fill 86%, n_eff≈36.3) : P(cible|rempli) **5%** · **EV/risk -0.176** (×p_fill ; si rempli -1.00% du capital)
  - **swing** (entrée dip −1.505% → cible +17.271% / stop −8.635%, p_fill 88%, n_eff≈36.2) : P(cible|rempli) **4%** · **EV/risk -0.443** (×p_fill ; si rempli -4.35% du capital)
  - **deep** (entrée dip −2.331% → cible +27.458% / stop −13.729%, p_fill 90%, n_eff≈34.4) : P(cible|rempli) **3%** · **EV/risk -0.683** (×p_fill ; si rempli -10.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→71% · +3.0%→55% · +5.0%→38% · +8.0%→14%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.385% vs midi 1.676% vs clôture 1.907% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr 0.015)_ ; drift intra méd. -0.803% ; recovery-V 36%
- **σ réalisé intraday** 4.915% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 64% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 13.5331 (VA 13.4686–13.7911 ; dernier close 13.22)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 48% · rebond 73% · **stop −6.42%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.58% · baisse 59% (gap-down >1% 47% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.75%) · haut méd +1.1% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.49% (p90 −4.29%) · haut méd +1.54% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −5.79%) · haut méd +1.91% · range méd 4.68%
- Excursion ouverture 60min (n=160) : bas méd −2.08% (p90 −6.5%) · haut méd +2.22% · range méd 5.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 13.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (134/159) · gap 52% · délai 0.0min · rebond 62% (86/134) (MFE +1.99%)
   - −1.0% : fill 30min 71% · séance 81% (130/159) · gap 47% · délai 0.0min · rebond 64% (84/130) (MFE +1.91%)
   - −1.5% : fill 30min 66% · séance 76% (123/159) · gap 40% · délai 0.0min · rebond 63% (80/123) (MFE +2.19%)
   - −2.0% : fill 30min 60% · séance 70% (115/159) · gap 30% · délai 0.0min · rebond 64% (76/115) (MFE +1.78%)
   - −3.0% : fill 30min 54% · séance 63% (98/159) · gap 13% · délai 1.2min · rebond 72% (71/98) (MFE +2.47%)
   - −4.0% : fill 30min 40% · séance 48% (77/159) · gap 4% · délai 5.8min · rebond 73% (56/77) (MFE +2.32%)
   - −5.0% : fill 30min 22% · séance 40% (63/159) · gap 1% · délai 21.5min · rebond 67% (47/63) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.72%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.22% (p90 −2.99%) → stop au-delà de −2.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.24% (p90 −4.06%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.32% (p90 −3.34%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 61% (50/83)
      · −2.0% : fill 89% (79/84) · rebond 64% (53/79)
      · −3.0% : fill 84% (71/84) · rebond 66% (49/71)
      · −4.0% : fill 65% (56/84) · rebond 69% (39/56)
      · −5.0% : fill 56% (48/84) · rebond 64% (36/48)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 52% (34/60) · rebond 63% (23/34)
      · −2.0% : fill 40% (25/60) · rebond 63% (15/25)
      · −3.0% : fill 33% (21/60) · rebond 89% (18/21)
      · −4.0% : fill 21% (15/60) · rebond 85% (13/15)
      · −5.0% : fill 17% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 67% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 15% si rouge (base 50% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **90%** · continue >prix actuel 55% ; creux résiduel méd -1.98% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.65% / q75 +4.22% → **scale +2.65% / runner +4.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +2.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.48% .. +4.97%] · haut q95 +6.89% · bas q05 -6.53%
   - 60min (n=160) : retour [-5.95% .. +6.06%] · haut q95 +7.24% · bas q05 -7.03%
   - 2h (n=160) : retour [-7.02% .. +7.63%] · haut q95 +9.15% · bas q05 -8.13%
   - 4h (n=160) : retour [-7.69% .. +6.31%] · haut q95 +9.19% · bas q05 -8.89%
   - 6h (n=160) : retour [-8.03% .. +7.61%] · haut q95 +9.24% · bas q05 -9.49%
   - session (n=160) : retour [-7.69% .. +8.4%] · haut q95 +10.34% · bas q05 -10.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 48.1  _(neutre)_
- **ADX** : 29.1  _(tendance etablie)_
- **MACD** : hist 0.136  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 31.2%
- **ATR** : 1.17 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 61.4  _(transition)_
- **MA** : MA20 15.34 · MA50 19.15 · MA200 21.97  _(prix < MA20)_
- **Dist MA** : MA20 -2.6% · MA50 -21.9% · MA200 -31.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82627 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
