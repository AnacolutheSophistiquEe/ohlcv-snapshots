# SOI

**Generated** : 2026-08-07T00:08:43.127595+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €120.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €120.40 (+0.7% vs entrée) · entrée €119.60 · stop €115.40 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.183 _(réel 5 s)_ (GBM 0.089) · ¼-Kelly 0.049 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.51% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -244 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €118.80–€120.40 (mid €119.60)
- Spot actuel : €120.40 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €115.40 (stop swing_plan-based (-10.32%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €130.78 · R/R 2.66 | T3 €133.57 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €115.40


## Edge, scénarios & sizing

- EV/risk : 0.089 | EV/share : €0.372 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 40 % | T3 40 %
- Kelly (position) : f* 0.195 | ¼-Kelly 0.049 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.3 | bear 69.4 | side 25.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 361.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.662% → cible +7.022% / stop −3.511%, p_fill 86%, n_eff≈36.0) : P(cible|rempli) **13%** · **EV/risk -0.183** (×p_fill ; si rempli -0.74% du capital)
  - **swing** (entrée dip −1.469% → cible +14.724% / stop −8.983%, p_fill 86%, n_eff≈35.0) : P(cible|rempli) **29%** · **EV/risk -0.064** (×p_fill ; si rempli -0.67% du capital)
  - **deep** (entrée dip −2.143% → cible +12.308% / stop −13.568%, p_fill 88%, n_eff≈36.9) : P(cible|rempli) **32%** · **EV/risk -0.323** (×p_fill ; si rempli -5.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→57% · +5.0%→42% · +8.0%→21%
- Range intraday médian 9.43% (p90 16.36%) · excursion haute méd. +3.69% / basse méd. −3.82%
- Profil de vol intra : ouverture 5.919% vs midi 1.692% vs clôture 2.601% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.111)_ ; drift intra méd. -0.357% ; recovery-V 36%
- **σ réalisé intraday** 5.698% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 62% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 123.2062 (VA 120.3007–124.1003 ; dernier close 117.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 78% · **stop −7.29%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.38 (high win-rate)
- Gaps overnight (n=147) : méd. 0.13% · baisse 46% (gap-down >1% 31% · >2% 22%)
- Excursion ouverture 5min (n=148) : bas méd −1.16% (p90 −3.77%) · haut méd +1.0% · range méd 2.94%
- Excursion ouverture 15min (n=148) : bas méd −1.42% (p90 −5.07%) · haut méd +1.56% · range méd 3.8%
- Excursion ouverture 30min (n=148) : bas méd −1.58% (p90 −5.42%) · haut méd +1.91% · range méd 4.33%
- Excursion ouverture 60min (n=148) : bas méd −1.75% (p90 −5.87%) · haut méd +1.92% · range méd 4.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 117.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 79% (116/147) · gap 37% · délai 0.0min · rebond 63% (75/116) (MFE +1.93%)
   - −1.0% : fill 30min 58% · séance 74% (110/147) · gap 31% · délai 0.2min · rebond 70% (79/110) (MFE +1.83%)
   - −1.5% : fill 30min 55% · séance 71% (101/147) · gap 29% · délai 0.2min · rebond 73% (74/101) (MFE +2.17%)
   - −2.0% : fill 30min 51% · séance 64% (92/147) · gap 22% · délai 0.2min · rebond 77% (73/92) (MFE +2.82%)
   - −3.0% : fill 30min 38% · séance 54% (76/147) · gap 16% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 30% · séance 45% (61/147) · gap 8% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 22% · séance 41% (53/147) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.8%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −3.56%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.83% (p90 −3.05%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1297 jambes) : jambe baissière méd −1.32% (p90 −3.15%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 98% (56/57) · rebond 61% (35/56)
      · −2.0% : fill 94% (54/57) · rebond 72% (42/54)
      · −3.0% : fill 86% (46/57) · rebond 74% (37/46)
      · −4.0% : fill 74% (40/57) · rebond 81% (33/40)
      · −5.0% : fill 67% (35/57) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (73 séances) :
      · −1.0% : fill 49% (37/73) · rebond 81% (30/37)
      · −2.0% : fill 30% (23/73) · rebond 87% (19/23)
      · −3.0% : fill 24% (19/73) · rebond 83% (15/19)
      · −4.0% : fill 18% (13/73) · rebond 55% (9/13)
      · −5.0% : fill 16% (10/73) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 51% en base · 68% si les 15 1res min sont vertes (70 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=148) : COUDE à **47min** → P(séance verte=clôture>ouverture) 80% si début vert vs 27% si rouge (base 51% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **80%** · continue >prix actuel 60% ; creux résiduel méd -2.57% (q20 -5.59%) → **SL/trailing à −5.59%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.16% / q75 +4.82% → **scale +3.16% / runner +4.82%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **27%** (continue à baisser 55%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.5%** (au-delà de la MAE q10 -8.5%), cible rebond +2.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-5.23% .. +7.02%] · haut q95 +7.84% · bas q05 -6.58%
   - 60min (n=148) : retour [-5.94% .. +7.13%] · haut q95 +9.22% · bas q05 -7.01%
   - 2h (n=148) : retour [-6.04% .. +9.94%] · haut q95 +12.43% · bas q05 -7.71%
   - 4h (n=148) : retour [-6.9% .. +10.25%] · haut q95 +14.14% · bas q05 -8.17%
   - 6h (n=148) : retour [-7.75% .. +10.88%] · haut q95 +14.28% · bas q05 -9.7%
   - session (n=148) : retour [-11.25% .. +13.79%] · haut q95 +15.76% · bas q05 -13.01%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.1% des séances sont trend-up (mild 0% / strong 6.1%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 5% vs absente 5% (base 6%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.8  _(momentum haussier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist 3.548  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 41.6%
- **ATR** : 10.66 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.011  _(neutre)_
- **Vol ratio** : 0.26  _(volume atone)_
- **Choppiness** : 44.3  _(transition)_
- **MA** : MA20 103.2 · MA50 119.88 · MA200 72.22  _(prix > MA20)_
- **Dist MA** : MA20 +16.7% · MA50 +0.4% · MA200 +66.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98880 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
