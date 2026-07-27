# SOI

**Generated** : 2026-07-27T21:43:56.356010+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €107.05  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €107.05 (+15.0% vs entrée) · entrée €93.09 · stop €81.92 · T1 €117.75 · R/R 2.21  
> ↳ P(T1 av. stop) 14 % · EV/risk 0.169 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -36 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €91.32–€94.85 (mid €93.09)
- Spot actuel : €107.05 (+15.0% au-dessus de la zone — repli à attendre)
- Stop : €81.92 (stop swing_plan-based (-23.48%))
- Targets : T1 €117.75 · R/R 2.21 | T2 €118.64 · R/R 2.29 | T3 €119.52 · R/R 2.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €81.92


## Edge, scénarios & sizing

- EV/risk : 0.169 | EV/share : €1.884 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.2 | bear 82.3 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 321.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.933% → cible +6.521% / stop −3.26%, p_fill 29%, n_eff≈14.8) : P(cible|rempli) **2%** · **EV/risk -0.074** (×p_fill ; si rempli -0.83% du capital)
  - **swing** (entrée dip −13.045% → cible +26.497% / stop −12.0%, p_fill 24%, n_eff≈9.0) : P(cible|rempli) **8%** · **EV/risk +0.087** (×p_fill ; si rempli +4.35% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→70% · +3.0%→59% · +5.0%→45% · +8.0%→22%
- Range intraday médian 9.18% (p90 17.62%) · excursion haute méd. +3.82% / basse méd. −3.36%
- Profil de vol intra : ouverture 5.961% vs midi 1.694% vs clôture 2.599% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑0%/↓1% ; spike-down 76% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.08)_ ; drift intra méd. -0.097% ; recovery-V 39%
- **σ réalisé intraday** 5.588% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 56% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 115.8435 (VA 115.3605–117.7755 ; dernier close 114.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 80% · **stop −7.18%** sous le fill (sous le bruit) · cible +3.02% · R/R 0.42 (high win-rate)
- Gaps overnight (n=139) : méd. 0.03% · baisse 50% (gap-down >1% 32% · >2% 24%)
- Excursion ouverture 5min (n=140) : bas méd −1.27% (p90 −3.74%) · haut méd +1.0% · range méd 3.17%
- Excursion ouverture 15min (n=140) : bas méd −1.55% (p90 −5.04%) · haut méd +1.34% · range méd 3.91%
- Excursion ouverture 30min (n=140) : bas méd −1.75% (p90 −5.36%) · haut méd +1.78% · range méd 4.39%
- Excursion ouverture 60min (n=140) : bas méd −1.85% (p90 −5.86%) · haut méd +1.92% · range méd 4.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 114.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 77% (109/139) · gap 39% · délai 0.0min · rebond 64% (71/109) (MFE +1.89%)
   - −1.0% : fill 30min 62% · séance 74% (104/139) · gap 32% · délai 0.1min · rebond 70% (75/104) (MFE +1.83%)
   - −1.5% : fill 30min 58% · séance 71% (95/139) · gap 30% · délai 0.2min · rebond 74% (70/95) (MFE +2.18%)
   - −2.0% : fill 30min 54% · séance 66% (88/139) · gap 24% · délai 0.2min · rebond 78% (70/88) (MFE +2.67%)
   - −3.0% : fill 30min 42% · séance 57% (73/139) · gap 17% · délai 0.5min · rebond 76% (58/73) (MFE +2.95%)
   - −4.0% : fill 30min 33% · séance 48% (59/139) · gap 7% · délai 1.9min · rebond 76% (47/59) (MFE +2.78%)
   - −5.0% : fill 30min 24% · séance 44% (51/139) · gap 2% · délai 14.4min · rebond 80% (43/51) (MFE +3.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.78%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −3.03%) → stop au-delà de −2.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.19%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1228 jambes) : jambe baissière méd −1.32% (p90 −3.16%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 97% (54/55) · rebond 62% (34/54)
      · −2.0% : fill 94% (52/55) · rebond 74% (41/52)
      · −3.0% : fill 85% (44/55) · rebond 76% (36/44)
      · −4.0% : fill 76% (39/55) · rebond 80% (32/39)
      · −5.0% : fill 68% (34/55) · rebond 86% (29/34)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (67 séances) :
      · −1.0% : fill 44% (33/67) · rebond 84% (27/33)
      · −2.0% : fill 30% (21/67) · rebond 82% (17/21)
      · −3.0% : fill 27% (18/67) · rebond 80% (14/18)
      · −4.0% : fill 18% (12/67) · rebond 68% (9/12)
      · −5.0% : fill 16% (9/67) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 53% en base · 73% si les 15 1res min sont vertes (65 cas) · 31% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=140) : COUDE à **36min** → P(séance verte=clôture>ouverture) 81% si début vert vs 24% si rouge (base 53% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **81%** · continue >prix actuel 62% ; creux résiduel méd -2.55% (q20 -5.44%) → **SL/trailing à −5.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.36% / q75 +5.85% → **scale +3.36% / runner +5.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 63%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.48%** (au-delà de la MAE q10 -8.48%), cible rebond +1.99% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-5.31% .. +7.19%] · haut q95 +8.25% · bas q05 -6.23%
   - 60min (n=140) : retour [-6.04% .. +7.39%] · haut q95 +10.23% · bas q05 -6.74%
   - 2h (n=140) : retour [-6.62% .. +10.11%] · haut q95 +12.67% · bas q05 -8.14%
   - 4h (n=140) : retour [-7.18% .. +10.68%] · haut q95 +14.28% · bas q05 -8.41%
   - 6h (n=140) : retour [-8.52% .. +11.87%] · haut q95 +14.34% · bas q05 -10.35%
   - session (n=140) : retour [-11.78% .. +13.89%] · haut q95 +16.32% · bas q05 -13.97%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 0% / strong 6.4%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 6% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 18.6  _(pas de tendance nette)_
- **MACD** : hist 2.853  _(bullish_recent)_
- **BB** : %B 0.58 · largeur 41.3%
- **ATR** : 9.69 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.122  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 103.64 · MA50 127.34 · MA200 69.77  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 -15.9% · MA200 +53.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98132 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
