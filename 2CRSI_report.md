# AL2SI

**Generated** : 2026-07-15T00:11:08.176847+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €28.22  

> 🟡 **WAIT-FOR-DIP** — spot +7.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €28.22 (+7.3% vs entrée) · entrée €26.31 · stop €24.20 · T1 €30.80 · R/R 2.13  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk 0.006 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.085 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.55). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €25.98–€26.64 (mid €26.31)
- Spot actuel : €28.22 (+7.3% au-dessus de la zone — repli à attendre)
- Stop : €24.20 (stop swing_plan-based (-25.13%))
- Targets : T1 €30.80 · R/R 2.13 | T2 €33.02 · R/R 3.18 | T3 €33.14 · R/R 3.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.20


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 40 % | T3 40 %
- Kelly (position) : f* 0.342 | ¼-Kelly 0.085 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.0 | bear 5.9 | side 75.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.782% → cible +17.08% / stop −8.0%, p_fill 44%, n_eff≈14.3) : P(cible|rempli) **5%** · **EV/risk +0.006** (×p_fill ; si rempli +0.10% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→75% · +3.0%→64% · +5.0%→41% · +8.0%→22%
- Range intraday médian 8.29% (p90 20.17%) · excursion haute méd. +4.16% / basse méd. −3.43%
- Profil de vol intra : ouverture 5.719% vs midi 1.676% vs clôture 1.993% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓1% ; spike-down 75% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.157 ; neutre — autocorr -0.025)_ ; drift intra méd. 0.006% ; recovery-V 28%
- **σ réalisé intraday** 8.432% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 69% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 31.0117 (VA 30.5437–31.1288 ; dernier close 30.72)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 90% · **stop −6.54%** sous le fill (sous le bruit) · cible +2.82% · R/R 0.43 (high win-rate)
- Gaps overnight (n=145) : méd. 0.25% · baisse 35% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=146) : bas méd −1.12% (p90 −5.17%) · haut méd +1.04% · range méd 3.08%
- Excursion ouverture 15min (n=146) : bas méd −1.6% (p90 −6.03%) · haut méd +1.54% · range méd 4.45%
- Excursion ouverture 30min (n=146) : bas méd −1.72% (p90 −6.68%) · haut méd +2.03% · range méd 4.96%
- Excursion ouverture 60min (n=146) : bas méd −2.29% (p90 −7.35%) · haut méd +2.53% · range méd 5.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 80% (112/145) · gap 27% · délai 0.3min · rebond 67% (74/112) (MFE +3.01%)
   - −1.0% : fill 30min 59% · séance 78% (107/145) · gap 20% · délai 0.4min · rebond 70% (74/107) (MFE +2.55%)
   - −1.5% : fill 30min 50% · séance 72% (97/145) · gap 12% · délai 1.5min · rebond 71% (64/97) (MFE +1.71%)
   - −2.0% : fill 30min 43% · séance 64% (84/145) · gap 8% · délai 3.1min · rebond 71% (57/84) (MFE +1.88%)
   - −3.0% : fill 30min 31% · séance 54% (68/145) · gap 6% · délai 9.0min · rebond 83% (56/68) (MFE +2.37%)
   - −4.0% : fill 30min 26% · séance 46% (58/145) · gap 5% · délai 19.0min · rebond 76% (45/58) (MFE +2.92%)
   - −5.0% : fill 30min 20% · séance 41% (50/145) · gap 5% · délai 31.0min · rebond 90% (47/50) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −5.58%) → stop au-delà de −3.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −5.66%) → stop au-delà de −4.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −3.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1391 jambes) : jambe baissière méd −1.25% (p90 −3.48%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (46/50) · rebond 68% (31/46)
      · −2.0% : fill 85% (39/50) · rebond 56% (24/39)
      · −3.0% : fill 82% (35/50) · rebond 76% (28/35)
      · −4.0% : fill 69% (30/50) · rebond 71% (24/30)
      · −5.0% : fill 60% (27/50) · rebond 77% (24/27)
   - **flat** (30 séances) :
      · −1.0% : fill 81% (23/30) · rebond 79% (18/23)
      · −2.0% : fill 64% (17/30) · rebond 86% (13/17)
      · −3.0% : fill 42% (11/30) · rebond 92% (10/11)
      · −4.0% : fill 42% (11/30) · rebond 94% (10/11)
      · −5.0% : fill 34% (9/30) · rebond 100% (9/9)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 48% en base · 69% si les 15 1res min sont vertes (69 cas) · 33% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=146) : COUDE à **31min** → P(séance verte=clôture>ouverture) 76% si début vert vs 24% si rouge (base 48% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 59% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.09% → **scale +3.7% / runner +6.09%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **24%** (continue à baisser 60%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −12.35%** (au-delà de la MAE q10 -12.35%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-5.56% .. +8.27%] · haut q95 +9.37% · bas q05 -7.81%
   - 60min (n=146) : retour [-6.07% .. +9.99%] · haut q95 +10.1% · bas q05 -8.86%
   - 2h (n=146) : retour [-6.13% .. +10.32%] · haut q95 +10.34% · bas q05 -9.2%
   - 4h (n=146) : retour [-11.52% .. +11.57%] · haut q95 +13.39% · bas q05 -12.89%
   - 6h (n=146) : retour [-10.44% .. +14.99%] · haut q95 +20.14% · bas q05 -14.94%
   - session (n=146) : retour [-10.63% .. +21.08%] · haut q95 +21.95% · bas q05 -16.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 52.8  _(neutre)_
- **ADX** : 22.3  _(pas de tendance nette)_
- **MACD** : hist -0.097  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 73.3%
- **ATR** : 4.15 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.017  _(neutre)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 31.31 · MA50 40.16 · MA200 23.88  _(prix < MA20)_
- **Dist MA** : MA20 -9.9% · MA50 -29.7% · MA200 +18.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90214 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
