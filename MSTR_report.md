# MSTR

**Generated** : 2026-07-07T21:47:20.903511+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $97.36  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $97.36 (+4.2% vs entrée) · entrée $93.47 · stop $89.27 · T1 $96.72 · R/R 0.77  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.124 _(réel 5 s)_ (GBM -0.075) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -41 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $92.82–$94.12 (mid $93.47)
- Spot actuel : $97.36 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $89.27 (stop swing_plan-based (-12.33%))
- Targets : T1 $96.72 · R/R 0.77 | T2 $99.97 · R/R 1.55 | T3 $103.22 · R/R 2.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.27


## Edge, scénarios & sizing

- EV/risk : -0.075 | EV/share : $-0.315 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.021 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.3 | bear 16.8 | side 76.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.989% → cible +3.476% / stop −4.5%, p_fill 32%, n_eff≈14.2) : P(cible|rempli) **1%** · **EV/risk -0.124** (×p_fill ; si rempli -1.75% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→55% · +3.0%→38% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.31% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.84%
- Profil de vol intra : ouverture 3.37% vs midi 1.236% vs clôture 1.276% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.51% ; recovery-V 43%
- **σ réalisé intraday** 4.339% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 65% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 101.5081 (VA 99.7879–102.2454 ; dernier close 100.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 67% · **stop −5.27%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.28 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 56% (gap-down >1% 40% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.28%) · haut méd +0.65% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.02%) · haut méd +1.04% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.39% (p90 −3.64%) · haut méd +1.22% · range méd 3.17%
- Excursion ouverture 60min (n=160) : bas méd −1.87% (p90 −4.85%) · haut méd +1.63% · range méd 3.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 100.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (126/159) · gap 48% · délai 0.0min · rebond 51% (63/126) (MFE +1.23%)
   - −1.0% : fill 30min 64% · séance 75% (120/159) · gap 40% · délai 0.0min · rebond 56% (68/120) (MFE +1.46%)
   - −1.5% : fill 30min 57% · séance 72% (112/159) · gap 30% · délai 0.0min · rebond 56% (67/112) (MFE +1.45%)
   - −2.0% : fill 30min 50% · séance 64% (100/159) · gap 25% · délai 0.2min · rebond 57% (64/100) (MFE +1.32%)
   - −3.0% : fill 30min 36% · séance 53% (77/159) · gap 16% · délai 4.0min · rebond 55% (46/77) (MFE +1.49%)
   - −4.0% : fill 30min 23% · séance 45% (62/159) · gap 8% · délai 29.6min · rebond 55% (36/62) (MFE +1.08%)
   - −5.0% : fill 30min 18% · séance 34% (47/159) · gap 6% · délai 27.3min · rebond 67% (33/47) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.9% (p90 −2.7%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.15% (p90 −2.81%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.36% (p90 −3.07%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=962 jambes) : jambe baissière méd −1.23% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 50% (37/73)
      · −2.0% : fill 90% (66/74) · rebond 53% (39/66)
      · −3.0% : fill 81% (57/74) · rebond 56% (34/57)
      · −4.0% : fill 66% (46/74) · rebond 56% (29/46)
      · −5.0% : fill 55% (37/74) · rebond 68% (27/37)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 53% si les 15 1res min sont vertes (74 cas) · 39% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 46% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 210min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -2.31% (q20 -4.04%) → **SL/trailing à −4.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +3.39% → **scale +2.11% / runner +3.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.66%** (au-delà de la MAE q10 -5.66%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.22%] · haut q95 +5.54% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.04% .. +4.76%] · haut q95 +5.74% · bas q05 -5.49%
   - 2h (n=160) : retour [-4.74% .. +5.71%] · haut q95 +6.98% · bas q05 -5.51%
   - 4h (n=160) : retour [-7.33% .. +8.1%] · haut q95 +9.3% · bas q05 -8.32%
   - 6h (n=160) : retour [-7.14% .. +6.98%] · haut q95 +10.1% · bas q05 -8.32%
   - session (n=160) : retour [-5.94% .. +6.4%] · haut q95 +10.1% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
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

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.5  _(survente)_
- **ADX** : 28.5  _(tendance etablie)_
- **MACD** : hist 1.297  _(bullish_recent)_
- **BB** : %B 0.34 · largeur 55.9%
- **ATR** : 9.65 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.272  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 37.7  _(marche directionnel)_
- **MA** : MA20 106.68 · MA50 141.94 · MA200 178.93  _(prix < MA20)_
- **Dist MA** : MA20 -8.7% · MA50 -31.4% · MA200 -45.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87897 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
