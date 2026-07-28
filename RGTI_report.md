# RGTI

**Generated** : 2026-07-28T22:02:50.293015+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $14.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $14.52 (+3.6% vs entrée) · entrée $14.02 · stop $13.69 · T1 $14.54 · R/R 1.58  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.305 _(réel 5 s)_ (GBM 0.157) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.35% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -76 % hors [0,100] (R² max 0.42). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $13.95–$14.10 (mid $14.02)
- Spot actuel : $14.52 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : $13.69 (stop swing_plan-based (-10.35%))
- Targets : T1 $14.54 · R/R 1.58 | T2 $14.85 · R/R 2.52 | T3 $15.17 · R/R 3.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $13.69


## Edge, scénarios & sizing

- EV/risk : 0.157 | EV/share : $0.052 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.094 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 15.4 | side 77.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.424% → cible +3.696% / stop −2.346%, p_fill 41%, n_eff≈19.1) : P(cible|rempli) **5%** · **EV/risk -0.305** (×p_fill ; si rempli -1.73% du capital)
  - **swing** (entrée dip −7.535% → cible +6.089% / stop −3.044%, p_fill 35%, n_eff≈15.1) : P(cible|rempli) **30%** · **EV/risk -0.030** (×p_fill ; si rempli -0.27% du capital)
  - **deep** (entrée dip −11.646% → cible +8.611% / stop −4.305%, p_fill 41%, n_eff≈14.6) : P(cible|rempli) **34%** · **EV/risk +0.022** (×p_fill ; si rempli +0.23% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→71% · +3.0%→55% · +5.0%→38% · +8.0%→14%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.396% vs midi 1.672% vs clôture 1.87% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.009)_ ; drift intra méd. -0.334% ; recovery-V 40%
- **σ réalisé intraday** 4.892% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 61% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 15.0804 (VA 15.0496–15.3887 ; dernier close 15.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 61% · rebond 76% · **stop −6.87%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.5% · baisse 57% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.78%) · haut méd +1.22% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.48% (p90 −4.08%) · haut méd +1.55% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.78% (p90 −5.29%) · haut méd +2.0% · range méd 4.68%
- Excursion ouverture 60min (n=160) : bas méd −2.04% (p90 −6.05%) · haut méd +2.39% · range méd 5.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (134/159) · gap 50% · délai 0.0min · rebond 66% (88/134) (MFE +2.29%)
   - −1.0% : fill 30min 69% · séance 80% (130/159) · gap 45% · délai 0.0min · rebond 67% (86/130) (MFE +2.06%)
   - −1.5% : fill 30min 64% · séance 75% (122/159) · gap 40% · délai 0.0min · rebond 66% (81/122) (MFE +2.38%)
   - −2.0% : fill 30min 59% · séance 69% (114/159) · gap 30% · délai 0.0min · rebond 65% (75/114) (MFE +2.44%)
   - −3.0% : fill 30min 52% · séance 61% (97/159) · gap 12% · délai 1.2min · rebond 76% (71/97) (MFE +2.55%)
   - −4.0% : fill 30min 38% · séance 46% (76/159) · gap 4% · délai 5.8min · rebond 75% (55/76) (MFE +2.38%)
   - −5.0% : fill 30min 21% · séance 38% (62/159) · gap 1% · délai 21.6min · rebond 68% (46/62) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.71%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.22% (p90 −2.99%) → stop au-delà de −2.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.06%) → stop au-delà de −2.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.31% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 98% (81/82) · rebond 65% (50/81)
      · −2.0% : fill 88% (77/82) · rebond 65% (52/77)
      · −3.0% : fill 82% (69/82) · rebond 71% (49/69)
      · −4.0% : fill 62% (54/82) · rebond 71% (38/54)
      · −5.0% : fill 53% (46/82) · rebond 66% (35/46)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 52% (36/62) · rebond 64% (25/36)
      · −2.0% : fill 40% (26/62) · rebond 62% (15/26)
      · −3.0% : fill 33% (22/62) · rebond 88% (18/22)
      · −4.0% : fill 21% (16/62) · rebond 83% (13/16)
      · −5.0% : fill 17% (11/62) · rebond 67% (8/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (82 cas) · 34% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 16% si rouge (base 52% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **90%** · continue >prix actuel 55% ; creux résiduel méd -1.97% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.65% / q75 +4.21% → **scale +2.65% / runner +4.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.69%** (au-delà de la MAE q10 -5.69%), cible rebond +2.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +4.97%] · haut q95 +6.95% · bas q05 -6.55%
   - 60min (n=160) : retour [-6.01% .. +6.36%] · haut q95 +7.81% · bas q05 -7.04%
   - 2h (n=160) : retour [-7.15% .. +7.68%] · haut q95 +9.17% · bas q05 -8.19%
   - 4h (n=160) : retour [-7.72% .. +6.33%] · haut q95 +9.19% · bas q05 -9.13%
   - 6h (n=160) : retour [-8.25% .. +7.69%] · haut q95 +9.26% · bas q05 -9.95%
   - session (n=160) : retour [-7.36% .. +8.5%] · haut q95 +10.43% · bas q05 -10.22%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.2  _(momentum baissier)_
- **ADX** : 29.7  _(tendance etablie)_
- **MACD** : hist 0.069  _(bullish_recent)_
- **BB** : %B 0.27 · largeur 39.6%
- **ATR** : 1.1 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.261  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 15.99 · MA50 19.3 · MA200 22.48  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -24.8% · MA200 -35.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83293 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
