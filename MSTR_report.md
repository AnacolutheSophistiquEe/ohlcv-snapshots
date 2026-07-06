# MSTR

**Generated** : 2026-07-06T21:47:12.416414+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $100.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $100.77 (+4.9% vs entrée) · entrée $96.03 · stop $88.35 · T1 $104.17 · R/R 1.06  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.034 _(réel 5 s)_ (GBM -0.079) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $95.35–$96.71 (mid $96.03)
- Spot actuel : $100.77 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : $88.35 (stop swing_plan-based (-13.9%))
- Targets : T1 $104.17 · R/R 1.06 | T2 $105.21 · R/R 1.2 | T3 $106.24 · R/R 1.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $88.35


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : $-0.606 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.07 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.0 | bear 76.6 | side 7.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.707% → cible +8.477% / stop −8.0%, p_fill 30%, n_eff≈12.0) : P(cible|rempli) **0%** · **EV/risk -0.034** (×p_fill ; si rempli -0.88% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→54% · +3.0%→36% · +5.0%→12% · +8.0%→6%
- Range intraday médian 5.25% (p90 9.51%) · excursion haute méd. +2.38% / basse méd. −2.84%
- Profil de vol intra : ouverture 3.316% vs midi 1.239% vs clôture 1.265% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.82% ; recovery-V 43%
- **σ réalisé intraday** 4.308% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 100.1667 (VA 99.5327–101.4347 ; dernier close 100.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 65% · **stop −5.32%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.23 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 55% (gap-down >1% 39% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −1.02% (p90 −2.28%) · haut méd +0.63% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.27% (p90 −3.02%) · haut méd +0.98% · range méd 2.54%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.64%) · haut méd +1.19% · range méd 3.14%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −4.92%) · haut méd +1.57% · range méd 3.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 100.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (126/159) · gap 48% · délai 0.0min · rebond 49% (62/126) (MFE +0.97%)
   - −1.0% : fill 30min 63% · séance 75% (120/159) · gap 39% · délai 0.0min · rebond 55% (67/120) (MFE +1.39%)
   - −1.5% : fill 30min 57% · séance 71% (112/159) · gap 28% · délai 0.0min · rebond 55% (66/112) (MFE +1.37%)
   - −2.0% : fill 30min 49% · séance 64% (100/159) · gap 24% · délai 0.2min · rebond 55% (63/100) (MFE +1.23%)
   - −3.0% : fill 30min 35% · séance 53% (77/159) · gap 14% · délai 5.7min · rebond 53% (46/77) (MFE +1.43%)
   - −4.0% : fill 30min 21% · séance 44% (62/159) · gap 7% · délai 36.2min · rebond 53% (36/62) (MFE +1.05%)
   - −5.0% : fill 30min 17% · séance 33% (47/159) · gap 4% · délai 29.7min · rebond 65% (33/47) (MFE +1.25%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.71%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.18% (p90 −2.82%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.42% (p90 −3.13%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=963 jambes) : jambe baissière méd −1.24% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 48% (36/73)
      · −2.0% : fill 90% (66/74) · rebond 50% (38/66)
      · −3.0% : fill 80% (57/74) · rebond 54% (34/57)
      · −4.0% : fill 65% (46/74) · rebond 54% (29/46)
      · −5.0% : fill 53% (37/74) · rebond 66% (27/37)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 43% (31/68) · rebond 62% (21/31)
      · −2.0% : fill 33% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 22% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 19% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 10% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 52% si les 15 1res min sont vertes (73 cas) · 39% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 72% si début vert vs 22% si rouge (base 45% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 210min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **72%** · continue >prix actuel 51% ; creux résiduel méd -2.3% (q20 -4.16%) → **SL/trailing à −4.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +3.15% → **scale +2.03% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.66%** (au-delà de la MAE q10 -5.66%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +3.89%] · haut q95 +4.28% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.05% .. +3.47%] · haut q95 +5.28% · bas q05 -5.5%
   - 2h (n=160) : retour [-4.74% .. +5.55%] · haut q95 +6.09% · bas q05 -5.53%
   - 4h (n=160) : retour [-7.36% .. +7.2%] · haut q95 +8.69% · bas q05 -8.32%
   - 6h (n=160) : retour [-7.15% .. +6.49%] · haut q95 +9.11% · bas q05 -8.34%
   - session (n=160) : retour [-5.98% .. +6.41%] · haut q95 +9.11% · bas q05 -8.34%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.5  _(momentum baissier)_
- **ADX** : 29.4  _(tendance etablie)_
- **MACD** : hist 0.86  _(bullish_recent)_
- **BB** : %B 0.38 · largeur 55.7%
- **ATR** : 10.05 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.226  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 36.0  _(marche directionnel)_
- **MA** : MA20 107.84 · MA50 143.44 · MA200 180.09  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -29.7% · MA200 -44.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88875 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
