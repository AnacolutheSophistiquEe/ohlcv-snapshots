# MSTR

**Generated** : 2026-08-13T00:21:41.029604+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $94.83  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $94.83 (+1.4% vs entrée) · entrée $93.53 · stop $89.79 · T1 $95.35 · R/R 0.49  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk 0.019 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 348 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $93.16–$93.89 (mid $93.53)
- Spot actuel : $94.83 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $89.79 (stop swing_plan-based (-8.57%))
- Targets : T1 $95.35 · R/R 0.49 | T2 $97.17 · R/R 0.97 | T3 $98.99 · R/R 1.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.79


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.116 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 26 % | T3 14 %
- Kelly (position) : f* 0.085 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.4 | bear 10.8 | side 11.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.375% → cible +1.946% / stop −4.0%, p_fill 68%, n_eff≈29.5) : P(cible|rempli) **58%** · **EV/risk +0.019** (×p_fill ; si rempli +0.11% du capital)
  - **swing** (entrée dip −3.03% → cible +4.351% / stop −5.714%, p_fill 56%, n_eff≈26.5) : P(cible|rempli) **61%** · **EV/risk +0.023** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −4.679% → cible +6.153% / stop −8.719%, p_fill 63%, n_eff≈25.8) : P(cible|rempli) **59%** · **EV/risk +0.061** (×p_fill ; si rempli +0.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→59% · +3.0%→40% · +5.0%→14% · +8.0%→6%
- Range intraday médian 5.38% (p90 9.51%) · excursion haute méd. +2.54% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.387% vs midi 1.205% vs clôture 1.315% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.127% ; recovery-V 31%
- **σ réalisé intraday** 3.755% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 80% / bas 61% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 96.1161 (VA 95.3969–96.4244 ; dernier close 96.14)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 54% (gap-down >1% 39% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.0%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.75%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.3% (p90 −3.35%) · haut méd +1.45% · range méd 3.12%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −4.14%) · haut méd +1.85% · range méd 3.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 96.14 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (125/159) · gap 46% · délai 0.0min · rebond 53% (63/125) (MFE +1.3%)
   - −1.0% : fill 30min 63% · séance 75% (120/159) · gap 39% · délai 0.0min · rebond 59% (70/120) (MFE +1.2%)
   - −1.5% : fill 30min 55% · séance 68% (110/159) · gap 32% · délai 0.0min · rebond 58% (64/110) (MFE +1.54%)
   - −2.0% : fill 30min 49% · séance 62% (100/159) · gap 26% · délai 0.0min · rebond 63% (64/100) (MFE +1.39%)
   - −3.0% : fill 30min 34% · séance 49% (78/159) · gap 15% · délai 2.0min · rebond 60% (48/78) (MFE +1.66%)
   - −4.0% : fill 30min 23% · séance 39% (64/159) · gap 5% · délai 12.7min · rebond 64% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 16% · séance 27% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.28%) → stop au-delà de −1.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.73%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.64%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=963 jambes) : jambe baissière méd −1.14% (p90 −2.74%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (76/77) · rebond 53% (39/76)
      · −2.0% : fill 90% (69/77) · rebond 61% (41/69)
      · −3.0% : fill 79% (61/77) · rebond 61% (37/61)
      · −4.0% : fill 64% (50/77) · rebond 67% (33/50)
      · −5.0% : fill 46% (38/77) · rebond 76% (28/38)
   - **flat** (17 séances) :
      · −1.0% : fill 93% (16/17) · rebond 73% (11/16)
      · −2.0% : fill 71% (12/17) · rebond 60% (8/12)
      · −3.0% : fill 30% (6/17) · rebond 57% (4/6)
      · −4.0% : fill 19% (5/17) · rebond 13% (2/5)
      · −5.0% : fill 15% (4/17) · rebond 16% (2/4)
   - **gap-up** (65 séances) :
      · −1.0% : fill 36% (28/65) · rebond 71% (20/28)
      · −2.0% : fill 22% (19/65) · rebond 72% (15/19)
      · −3.0% : fill 15% (11/65) · rebond 56% (7/11)
      · −4.0% : fill 13% (9/65) · rebond 66% (5/9)
      · −5.0% : fill 6% (5/65) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (78 cas) · 39% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 78% si début vert vs 16% si rouge (base 46% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 43% ; creux résiduel méd -1.52% (q20 -3.26%) → **SL/trailing à −3.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.61% / q75 +2.49% → **scale +1.61% / runner +2.49%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **16%** (continue à baisser 61%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.07%** (au-delà de la MAE q10 -5.07%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.46% .. +3.73%] · haut q95 +4.01% · bas q05 -3.96%
   - 60min (n=160) : retour [-4.78% .. +3.5%] · haut q95 +4.98% · bas q05 -5.37%
   - 2h (n=160) : retour [-4.55% .. +5.18%] · haut q95 +5.79% · bas q05 -5.39%
   - 4h (n=160) : retour [-6.03% .. +6.59%] · haut q95 +8.43% · bas q05 -7.05%
   - 6h (n=160) : retour [-5.92% .. +5.44%] · haut q95 +8.43% · bas q05 -7.93%
   - session (n=160) : retour [-5.31% .. +5.77%] · haut q95 +8.43% · bas q05 -7.97%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 51.6  _(neutre)_
- **ADX** : 10.5  _(pas de tendance nette)_
- **MACD** : hist 0.919  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 11.0%
- **ATR** : 5.25 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.013  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 57.1  _(transition)_
- **MA** : MA20 96.46 · MA50 102.9 · MA200 150.04  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 -7.8% · MA200 -36.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87509 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
