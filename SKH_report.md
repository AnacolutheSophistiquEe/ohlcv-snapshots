# 000660

**Generated** : 2026-07-23T21:47:12.963573+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1919000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩1919000.00 (+0.9% vs entrée) · entrée ₩1902700.15 · stop ₩1834364.44 · T1 ₩2019833.22 · R/R 1.71  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk -0.269 _(réel 5 s)_ (GBM -0.007) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.59% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1886400.30–₩1919000.00 (mid ₩1902700.15)
- Spot actuel : ₩1919000.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩1834364.44 (stop swing_plan-based (-13.65%))
- Targets : T1 ₩2019833.22 · R/R 1.71 | T2 ₩2085367.62 · R/R 2.67 | T3 ₩2150902.01 · R/R 3.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1834364.44


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : ₩-488.847 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.088 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.5 | bear 62.2 | side 29.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.849% → cible +6.156% / stop −3.592%, p_fill 82%, n_eff≈31.9) : P(cible|rempli) **16%** · **EV/risk -0.269** (×p_fill ; si rempli -1.18% du capital)
  - **swing** (entrée dip −1.875% → cible +27.826% / stop −12.0%, p_fill 78%, n_eff≈28.5) : P(cible|rempli) **0%** · **EV/risk -0.312** (×p_fill ; si rempli -4.80% du capital)
  - **deep** (entrée dip −2.84% → cible +13.75% / stop −6.875%, p_fill 75%, n_eff≈25.9) : P(cible|rempli) **26%** · **EV/risk -0.249** (×p_fill ; si rempli -2.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→81% · +2.0%→56% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.23% (p90 11.16%) · excursion haute méd. +2.25% / basse méd. −2.5%
- Profil de vol intra : ouverture 3.012% vs midi 1.236% vs clôture 1.508% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 17% · trend ↑2%/↓0% ; spike-down 67% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.695% ; recovery-V 28%
- **σ réalisé intraday** 5.054% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 68% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 1981075.0 (VA 1937575.0–1998475.0 ; dernier close 1836000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 79% · **stop −8.68%** sous le fill (sous le bruit) · cible +2.69% · R/R 0.31 (high win-rate)
- Gaps overnight (n=141) : méd. -0.01% · baisse 50% (gap-down >1% 36% · >2% 29%)
- Excursion ouverture 5min (n=142) : bas méd −0.58% (p90 −1.75%) · haut méd +0.96% · range méd 1.53%
- Excursion ouverture 15min (n=142) : bas méd −0.79% (p90 −2.41%) · haut méd +1.18% · range méd 2.14%
- Excursion ouverture 30min (n=142) : bas méd −1.28% (p90 −3.02%) · haut méd +1.36% · range méd 2.75%
- Excursion ouverture 60min (n=142) : bas méd −1.34% (p90 −3.76%) · haut méd +1.7% · range méd 3.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1836000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (89/141) · gap 41% · délai 0.0min · rebond 56% (47/89) (MFE +1.63%)
   - −1.0% : fill 30min 55% · séance 63% (81/141) · gap 36% · délai 0.0min · rebond 66% (51/81) (MFE +2.11%)
   - −1.5% : fill 30min 50% · séance 58% (72/141) · gap 34% · délai 0.0min · rebond 68% (46/72) (MFE +2.18%)
   - −2.0% : fill 30min 42% · séance 52% (65/141) · gap 29% · délai 0.0min · rebond 66% (43/65) (MFE +2.04%)
   - −3.0% : fill 30min 39% · séance 47% (56/141) · gap 23% · délai 0.0min · rebond 79% (42/56) (MFE +2.69%)
   - −4.0% : fill 30min 28% · séance 38% (43/141) · gap 13% · délai 3.5min · rebond 77% (33/43) (MFE +2.78%)
   - −5.0% : fill 30min 14% · séance 30% (34/141) · gap 10% · délai 30.4min · rebond 74% (26/34) (MFE +2.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.51%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.41%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −3.64%) → stop au-delà de −2.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=728 jambes) : jambe baissière méd −1.31% (p90 −3.32%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (59/61) · rebond 55% (32/59)
      · −2.0% : fill 87% (50/61) · rebond 62% (30/50)
      · −3.0% : fill 82% (45/61) · rebond 76% (32/45)
      · −4.0% : fill 72% (38/61) · rebond 73% (28/38)
      · −5.0% : fill 60% (31/61) · rebond 71% (23/31)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 25% (13/68) · rebond 98% (12/13)
      · −2.0% : fill 13% (8/68) · rebond 75% (7/8)
      · −3.0% : fill 12% (6/68) · rebond 91% (5/6)
      · −4.0% : fill 7% (3/68) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/68) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 46% en base · 53% si les 15 1res min sont vertes (77 cas) · 37% si rouges (65 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 74% si début vert vs 22% si rouge (base 46% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **74%** · continue >prix actuel 46% ; creux résiduel méd -1.64% (q20 -6.25%) → **SL/trailing à −6.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +3.41% → **scale +1.37% / runner +3.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.23%** (au-delà de la MAE q10 -7.23%), cible rebond +1.84% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-2.79% .. +3.44%] · haut q95 +4.08% · bas q05 -3.66%
   - 60min (n=142) : retour [-3.49% .. +5.67%] · haut q95 +6.71% · bas q05 -5.09%
   - 2h (n=142) : retour [-4.52% .. +5.55%] · haut q95 +8.32% · bas q05 -6.23%
   - 4h (n=142) : retour [-5.64% .. +7.06%] · haut q95 +8.51% · bas q05 -8.09%
   - 6h (n=142) : retour [-7.06% .. +7.76%] · haut q95 +9.69% · bas q05 -8.94%
   - session (n=142) : retour [-7.07% .. +8.08%] · haut q95 +9.69% · bas q05 -8.94%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.3% des séances sont trend-up (mild 0% / strong 6.3%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.4  _(momentum baissier)_
- **ADX** : 28.1  _(tendance etablie)_
- **MACD** : hist -52740.324  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 62.2%
- **ATR** : 227785.71 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 2202850.0 · MA50 2200649.42 · MA200 1137363.38  _(prix < MA20)_
- **Dist MA** : MA20 -12.9% · MA50 -12.8% · MA200 +68.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88085 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
