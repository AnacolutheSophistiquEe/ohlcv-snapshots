# IONQ

**Generated** : 2026-06-26T21:51:36.875527+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $49.31  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $49.31 (+2.9% vs entrée) · entrée $47.92 · stop $46.30 · T1 $49.47 · R/R 0.96  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.021 _(réel 5 s)_ (GBM -0.015) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $47.61–$48.23 (mid $47.92)
- Spot actuel : $49.31 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $46.30 (stop swing_plan-based (-9.59%))
- Targets : T1 $49.47 · R/R 0.96 | T2 $51.02 · R/R 1.91 | T3 $52.58 · R/R 2.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $46.30


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : $-0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 18 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 11.2 | side 80.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.813% → cible +3.237% / stop −3.393%, p_fill 58%, n_eff≈22.1) : P(cible|rempli) **46%** · **EV/risk -0.021** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −6.195% → cible +7.239% / stop −3.619%, p_fill 41%, n_eff≈15.8) : P(cible|rempli) **29%** · **EV/risk -0.089** (×p_fill ; si rempli -0.78% du capital)
  - **deep** (entrée dip −9.571% → cible +10.237% / stop −5.119%, p_fill 36%, n_eff≈13.0) : P(cible|rempli) **31%** · **EV/risk -0.044** (×p_fill ; si rempli -0.63% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→57% · +5.0%→31% · +8.0%→18%
- Range intraday médian 7.63% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.78%
- Profil de vol intra : ouverture 4.783% vs midi 1.617% vs clôture 1.663% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 75% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; momentum — autocorr 0.037)_ ; drift intra méd. 0.042% ; recovery-V 44%
- **σ réalisé intraday** 5.519% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 51% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 50.8324 (VA 50.4656–51.1991 ; dernier close 50.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 85% · **stop −4.75%** sous le fill (sous le bruit) · cible +3.44% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.29% · baisse 52% (gap-down >1% 37% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.31% (p90 −3.12%) · haut méd +0.98% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.87% (p90 −4.0%) · haut méd +1.31% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −2.14% (p90 −5.35%) · haut méd +1.73% · range méd 4.38%
- Excursion ouverture 60min (n=160) : bas méd −2.53% (p90 −6.06%) · haut méd +1.98% · range méd 5.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 50.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (133/159) · gap 47% · délai 0.0min · rebond 72% (94/133) (MFE +2.14%)
   - −1.0% : fill 30min 73% · séance 81% (126/159) · gap 37% · délai 0.0min · rebond 76% (93/126) (MFE +2.5%)
   - −1.5% : fill 30min 69% · séance 78% (120/159) · gap 29% · délai 0.0min · rebond 72% (84/120) (MFE +2.48%)
   - −2.0% : fill 30min 59% · séance 72% (113/159) · gap 19% · délai 0.4min · rebond 72% (80/113) (MFE +2.69%)
   - −3.0% : fill 30min 50% · séance 61% (91/159) · gap 12% · délai 6.0min · rebond 76% (68/91) (MFE +3.35%)
   - −4.0% : fill 30min 32% · séance 48% (73/159) · gap 6% · délai 15.8min · rebond 81% (56/73) (MFE +2.75%)
   - −5.0% : fill 30min 21% · séance 42% (65/159) · gap 3% · délai 29.0min · rebond 85% (56/65) (MFE +3.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.9%) → stop au-delà de −2.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.14% (p90 −3.71%) → stop au-delà de −2.68% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.28% (p90 −3.75%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1116 jambes) : jambe baissière méd −1.37% (p90 −3.34%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 100% (70/70) · rebond 75% (52/70)
      · −2.0% : fill 92% (65/70) · rebond 78% (51/65)
      · −3.0% : fill 82% (55/70) · rebond 75% (43/55)
      · −4.0% : fill 63% (43/70) · rebond 80% (35/43)
      · −5.0% : fill 56% (38/70) · rebond 80% (32/38)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 81% (9/14)
      · −2.0% : fill 60% (13/17) · rebond 49% (7/13)
      · −3.0% : fill 45% (10/17) · rebond 52% (6/10)
      · −4.0% : fill 40% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/17) · rebond 91% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 58% (42/72) · rebond 77% (32/42)
      · −2.0% : fill 50% (35/72) · rebond 64% (22/35)
      · −3.0% : fill 40% (26/72) · rebond 85% (19/26)
      · −4.0% : fill 30% (23/72) · rebond 88% (18/23)
      · −5.0% : fill 25% (20/72) · rebond 97% (18/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 63% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 85% si début vert vs 24% si rouge (base 51% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -2.17% (q20 -3.45%) → **SL/trailing à −3.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.23% / q75 +3.4% → **scale +2.23% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **24%** (continue à baisser 49%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +2.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.22% .. +7.18%] · haut q95 +8.32% · bas q05 -6.23%
   - 60min (n=160) : retour [-5.32% .. +7.67%] · haut q95 +11.21% · bas q05 -6.82%
   - 2h (n=160) : retour [-6.64% .. +9.55%] · haut q95 +11.83% · bas q05 -7.67%
   - 4h (n=160) : retour [-7.74% .. +9.69%] · haut q95 +12.74% · bas q05 -8.69%
   - 6h (n=160) : retour [-7.74% .. +7.65%] · haut q95 +12.88% · bas q05 -10.19%
   - session (n=160) : retour [-7.63% .. +9.69%] · haut q95 +12.92% · bas q05 -10.19%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist -1.653  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 44.0%
- **ATR** : 5.42 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.271  _(distribution)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 58.7  _(transition)_
- **MA** : MA20 59.68 · MA50 54.51 · MA200 49.58  _(prix < MA20)_
- **Dist MA** : MA20 -17.4% · MA50 -9.5% · MA200 -0.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (68638 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
