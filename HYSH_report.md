# 298040

**Generated** : 2026-07-28T21:51:36.733658+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2324000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩2324000.00 (+2.5% vs entrée) · entrée ₩2266800.00 · stop ₩2064700.00 · T1 ₩2671000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.342 _(réel 5 s)_ (GBM 0.121) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -90 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2231119.37–₩2302480.63 (mid ₩2266800.00)
- Spot actuel : ₩2324000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩2064700.00 (stop swing_plan-based (-11.16%))
- Targets : T1 ₩2671000.00 · R/R 2.0 | T2 ₩2735693.79 · R/R 2.32 | T3 ₩2800387.57 · R/R 2.64
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2064700.00


## Edge, scénarios & sizing

- EV/risk : 0.121 | EV/share : ₩24561.480 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 7 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.3 | bear 61.9 | side 17.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.122% → cible +6.014% / stop −3.214%, p_fill 84%, n_eff≈35.3) : P(cible|rempli) **12%** · **EV/risk -0.137** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −2.464% → cible +17.831% / stop −8.916%, p_fill 90%, n_eff≈34.4) : P(cible|rempli) **8%** · **EV/risk -0.342** (×p_fill ; si rempli -3.39% du capital)
  - **deep** (entrée dip −3.803% → cible +11.097% / stop −5.548%, p_fill 89%, n_eff≈33.3) : P(cible|rempli) **31%** · **EV/risk -0.128** (×p_fill ; si rempli -0.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→62% · +2.0%→52% · +3.0%→39% · +5.0%→22% · +8.0%→6%
- Range intraday médian 6.88% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.93%
- Profil de vol intra : ouverture 4.294% vs midi 1.065% vs clôture 1.157% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.103)_ ; drift intra méd. -1.592% ; recovery-V 29%
- **σ réalisé intraday** 5.157% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 66% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 2625012.5 (VA 2583262.5–2629187.5 ; dernier close 2628000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 87% · **stop −5.08%** sous le fill (sous le bruit) · cible +2.39% · R/R 0.47 (high win-rate)
- Gaps overnight (n=140) : méd. 0.7% · baisse 37% (gap-down >1% 23% · >2% 16%)
- Excursion ouverture 5min (n=141) : bas méd −1.29% (p90 −3.44%) · haut méd +0.81% · range méd 2.69%
- Excursion ouverture 15min (n=141) : bas méd −1.95% (p90 −4.5%) · haut méd +1.11% · range méd 3.74%
- Excursion ouverture 30min (n=141) : bas méd −2.46% (p90 −4.91%) · haut méd +1.12% · range méd 4.15%
- Excursion ouverture 60min (n=141) : bas méd −2.58% (p90 −5.29%) · haut méd +1.36% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2628000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 71% (96/140) · gap 31% · délai 0.0min · rebond 62% (60/96) (MFE +1.28%)
   - −1.0% : fill 30min 57% · séance 68% (88/140) · gap 23% · délai 0.8min · rebond 62% (55/88) (MFE +1.56%)
   - −1.5% : fill 30min 49% · séance 60% (79/140) · gap 20% · délai 1.5min · rebond 54% (48/79) (MFE +1.44%)
   - −2.0% : fill 30min 44% · séance 57% (70/140) · gap 16% · délai 4.5min · rebond 52% (38/70) (MFE +1.33%)
   - −3.0% : fill 30min 32% · séance 48% (57/140) · gap 7% · délai 7.9min · rebond 55% (32/57) (MFE +1.27%)
   - −4.0% : fill 30min 21% · séance 43% (49/140) · gap 4% · délai 33.3min · rebond 74% (37/49) (MFE +1.91%)
   - −5.0% : fill 30min 18% · séance 33% (36/140) · gap 4% · délai 28.8min · rebond 87% (30/36) (MFE +2.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.19%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −4.17%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −4.2%) → stop au-delà de −2.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=757 jambes) : jambe baissière méd −1.38% (p90 −3.37%) · ~13.8 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 100% (48/48) · rebond 60% (30/48)
      · −2.0% : fill 87% (40/48) · rebond 54% (22/40)
      · −3.0% : fill 83% (38/48) · rebond 55% (21/38)
      · −4.0% : fill 79% (33/48) · rebond 80% (25/33)
      · −5.0% : fill 66% (27/48) · rebond 90% (22/27)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (76 séances) :
      · −1.0% : fill 44% (29/76) · rebond 63% (17/29)
      · −2.0% : fill 34% (22/76) · rebond 48% (11/22)
      · −3.0% : fill 24% (14/76) · rebond 52% (7/14)
      · −4.0% : fill 19% (11/76) · rebond 76% (9/11)
      · −5.0% : fill 10% (6/76) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 38% en base · 61% si les 15 1res min sont vertes (57 cas) · 27% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 38% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.65% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.18% → **scale +1.7% / runner +3.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **13%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-4.3% .. +4.24%] · haut q95 +6.1% · bas q05 -5.24%
   - 60min (n=141) : retour [-5.25% .. +4.79%] · haut q95 +6.32% · bas q05 -5.57%
   - 2h (n=141) : retour [-7.02% .. +4.44%] · haut q95 +6.75% · bas q05 -8.06%
   - 4h (n=141) : retour [-7.59% .. +5.3%] · haut q95 +7.37% · bas q05 -9.26%
   - 6h (n=141) : retour [-7.46% .. +5.24%] · haut q95 +8.32% · bas q05 -9.31%
   - session (n=141) : retour [-6.67% .. +5.56%] · haut q95 +8.32% · bas q05 -9.39%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 0% / strong 5.7%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 24% vs absente 0% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 36.3  _(momentum baissier)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist -15353.401  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 49.1%
- **ATR** : 246214.29 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 59.9  _(transition)_
- **MA** : MA20 2880250.0 · MA50 3309400.0 · MA200 2632639.59  _(prix < MA20)_
- **Dist MA** : MA20 -19.3% · MA50 -29.8% · MA200 -11.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87883 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
