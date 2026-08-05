# EVT

**Generated** : 2026-08-05T00:04:26.273701+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.46  

> 🟡 **WAIT-FOR-DIP** — spot +2.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.46 (+2.1% vs entrée) · entrée €3.39 · stop €3.27 · T1 €3.50 · R/R 0.92  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk 0.03 _(réel 5 s)_ (GBM -0.0) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.36–€3.41 (mid €3.39)
- Spot actuel : €3.46 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €3.27 (stop swing_plan-based (-8.9%))
- Targets : T1 €3.50 · R/R 0.92 | T2 €3.62 · R/R 1.92 | T3 €3.74 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.27


## Edge, scénarios & sizing

- EV/risk : -0.0 | EV/share : €-0.000 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 8 % | T3 8 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.1 | bear 63.7 | side 6.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.021% → cible +3.497% / stop −3.5%, p_fill 50%, n_eff≈18.3) : P(cible|rempli) **19%** · **EV/risk +0.030** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −4.456% → cible +7.82% / stop −4.652%, p_fill 24%, n_eff≈10.3) : P(cible|rempli) **3%** · **EV/risk -0.128** (×p_fill ; si rempli -2.49% du capital)
  - **deep** (entrée dip −6.883% → cible +11.06% / stop −7.16%, p_fill 27%, n_eff≈10.2) : P(cible|rempli) **2%** · **EV/risk -0.142** (×p_fill ; si rempli -3.75% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→45% · +3.0%→25% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.15% (p90 6.48%) · excursion haute méd. +1.72% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.731% vs midi 1.227% vs clôture 1.238% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.075 ; mean-reverting — autocorr -0.139)_ ; drift intra méd. -0.31% ; recovery-V 34%
- **σ réalisé intraday** 3.393% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 66% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 3.4849 (VA 3.4771–3.5031 ; dernier close 3.478)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 74% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 47% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −2.51%) · haut méd +0.47% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.69%) · haut méd +0.78% · range méd 1.73%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −2.79%) · haut méd +0.91% · range méd 2.05%
- Excursion ouverture 60min (n=160) : bas méd −1.19% (p90 −3.03%) · haut méd +0.94% · range méd 2.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.478 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 84% (133/159) · gap 29% · délai 0.2min · rebond 68% (88/133) (MFE +1.56%)
   - −1.0% : fill 30min 52% · séance 74% (119/159) · gap 21% · délai 0.6min · rebond 67% (77/119) (MFE +1.6%)
   - −1.5% : fill 30min 37% · séance 59% (100/159) · gap 15% · délai 2.5min · rebond 60% (64/100) (MFE +1.33%)
   - −2.0% : fill 30min 27% · séance 46% (80/159) · gap 9% · délai 14.8min · rebond 64% (53/80) (MFE +1.43%)
   - −3.0% : fill 30min 14% · séance 30% (56/159) · gap 5% · délai 30.4min · rebond 68% (42/56) (MFE +1.66%)
   - −4.0% : fill 30min 8% · séance 16% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 9% (17/159) · gap 1% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.52%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.92%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −1.94%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=818 jambes) : jambe baissière méd −1.08% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 95% (59/62) · rebond 71% (36/59)
      · −2.0% : fill 64% (44/62) · rebond 60% (28/44)
      · −3.0% : fill 38% (32/62) · rebond 68% (24/32)
      · −4.0% : fill 26% (20/62) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/62) · rebond 57% (9/13)
   - **flat** (41 séances) :
      · −1.0% : fill 79% (32/41) · rebond 68% (24/32)
      · −2.0% : fill 53% (19/41) · rebond 68% (13/19)
      · −3.0% : fill 40% (12/41) · rebond 73% (9/12)
      · −4.0% : fill 17% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/41) · rebond 27% (1/3)
   - **gap-up** (56 séances) :
      · −1.0% : fill 48% (28/56) · rebond 59% (17/28)
      · −2.0% : fill 23% (17/56) · rebond 70% (12/17)
      · −3.0% : fill 14% (12/56) · rebond 57% (9/12)
      · −4.0% : fill 6% (5/56) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 68% si les 15 1res min sont vertes (75 cas) · 40% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 67% si début vert vs 40% si rouge (base 53% · écart 27 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **67%** · continue >prix actuel 48% ; creux résiduel méd -1.85% (q20 -3.13%) → **SL/trailing à −3.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.17% → **scale +1.35% / runner +2.17%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **40%** (continue à baisser 41%) → **RÉDUIRE ~60%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.53% .. +2.43%] · haut q95 +3.51% · bas q05 -3.43%
   - 60min (n=160) : retour [-3.12% .. +3.15%] · haut q95 +4.38% · bas q05 -3.55%
   - 2h (n=160) : retour [-3.48% .. +3.21%] · haut q95 +4.56% · bas q05 -4.27%
   - 4h (n=160) : retour [-2.94% .. +3.03%] · haut q95 +4.56% · bas q05 -4.69%
   - 6h (n=160) : retour [-3.34% .. +3.25%] · haut q95 +4.79% · bas q05 -5.33%
   - session (n=160) : retour [-4.23% .. +4.09%] · haut q95 +5.95% · bas q05 -5.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.7  _(momentum baissier)_
- **ADX** : 40.8  _(tendance tres forte)_
- **MACD** : hist 0.005  _(bullish_recent)_
- **BB** : %B 0.35 · largeur 67.9%
- **ATR** : 0.15 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.029  _(neutre)_
- **Vol ratio** : 0.3  _(volume atone)_
- **Choppiness** : 71.9  _(marche en range (choppy))_
- **MA** : MA20 3.86 · MA50 4.49 · MA200 5.28  _(prix < MA20)_
- **Dist MA** : MA20 -10.5% · MA50 -23.1% · MA200 -34.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90073 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
