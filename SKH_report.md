# 000660

**Generated** : 2026-07-29T21:48:09.566235+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1404000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩1404000.00 (+14.6% vs entrée) · entrée ₩1225425.75 · stop ₩1161590.03 · T1 ₩1348841.76 · R/R 1.93  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.65 · ¼-Kelly 0.029 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -63 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1200742.55–₩1250108.95 (mid ₩1225425.75)
- Spot actuel : ₩1404000.00 (+14.6% au-dessus de la zone — repli à attendre)
- Stop : ₩1161590.03 (stop swing_plan-based (-17.27%))
- Targets : T1 ₩1348841.76 · R/R 1.93 | T2 ₩1472257.77 · R/R 3.87 | T3 ₩1595673.78 · R/R 5.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1161590.03


## Edge, scénarios & sizing

- EV/risk : 0.65 | EV/share : ₩41479.091 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.116 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.7 | bear 62.9 | side 26.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.783% → cible +4.504% / stop −4.826%, p_fill 41%, n_eff≈13.3) : P(cible|rempli) **35%** · **EV/risk +0.068** (×p_fill ; si rempli +0.80% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→79% · +2.0%→54% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.32% (p90 11.16%) · excursion haute méd. +2.16% / basse méd. −2.59%
- Profil de vol intra : ouverture 3.029% vs midi 1.265% vs clôture 1.527% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑2%/↓0% ; spike-down 70% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.02)_ ; drift intra méd. -1.162% ; recovery-V 28%
- **σ réalisé intraday** 4.958% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 73% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 1616500.0 (VA 1577500.0–1637500.0 ; dernier close 1555000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 39% · rebond 74% · **stop −8.92%** sous le fill (sous le bruit) · cible +2.5% · R/R 0.28 (high win-rate)
- Gaps overnight (n=145) : méd. 0.0% · baisse 50% (gap-down >1% 35% · >2% 29%)
- Excursion ouverture 5min (n=146) : bas méd −0.67% (p90 −1.81%) · haut méd +0.9% · range méd 1.59%
- Excursion ouverture 15min (n=146) : bas méd −0.8% (p90 −2.7%) · haut méd +1.14% · range méd 2.24%
- Excursion ouverture 30min (n=146) : bas méd −1.32% (p90 −3.47%) · haut méd +1.27% · range méd 2.84%
- Excursion ouverture 60min (n=146) : bas méd −1.36% (p90 −3.94%) · haut méd +1.56% · range méd 3.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1555000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 69% (92/145) · gap 42% · délai 0.0min · rebond 54% (48/92) (MFE +1.34%)
   - −1.0% : fill 30min 55% · séance 64% (84/145) · gap 35% · délai 0.0min · rebond 64% (52/84) (MFE +1.85%)
   - −1.5% : fill 30min 50% · séance 59% (75/145) · gap 33% · délai 0.0min · rebond 65% (47/75) (MFE +1.84%)
   - −2.0% : fill 30min 43% · séance 54% (68/145) · gap 29% · délai 0.0min · rebond 63% (44/68) (MFE +1.84%)
   - −3.0% : fill 30min 40% · séance 47% (58/145) · gap 24% · délai 0.0min · rebond 73% (42/58) (MFE +2.33%)
   - −4.0% : fill 30min 30% · séance 39% (45/145) · gap 14% · délai 3.4min · rebond 74% (34/45) (MFE +2.5%)
   - −5.0% : fill 30min 15% · séance 32% (36/145) · gap 12% · délai 30.3min · rebond 71% (27/36) (MFE +2.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.5%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.41%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −3.64%) → stop au-delà de −2.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=759 jambes) : jambe baissière méd −1.31% (p90 −3.36%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (61/63) · rebond 51% (32/61)
      · −2.0% : fill 88% (52/63) · rebond 56% (30/52)
      · −3.0% : fill 84% (47/63) · rebond 68% (32/47)
      · −4.0% : fill 75% (40/63) · rebond 71% (29/40)
      · −5.0% : fill 64% (33/63) · rebond 69% (24/33)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (70 séances) :
      · −1.0% : fill 27% (14/70) · rebond 99% (13/14)
      · −2.0% : fill 16% (9/70) · rebond 81% (8/9)
      · −3.0% : fill 11% (6/70) · rebond 91% (5/6)
      · −4.0% : fill 7% (3/70) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/70) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 45% en base · 51% si les 15 1res min sont vertes (78 cas) · 37% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=146) : COUDE à **1:35** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 45% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.63% (q20 -4.87%) → **SL/trailing à −4.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.43% → **scale +1.66% / runner +3.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **15%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.63%** (au-delà de la MAE q10 -6.63%), cible rebond +1.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-3.01% .. +3.2%] · haut q95 +3.81% · bas q05 -3.76%
   - 60min (n=146) : retour [-3.43% .. +5.56%] · haut q95 +6.35% · bas q05 -4.97%
   - 2h (n=146) : retour [-4.35% .. +5.45%] · haut q95 +8.27% · bas q05 -6.1%
   - 4h (n=146) : retour [-6.42% .. +6.95%] · haut q95 +8.49% · bas q05 -8.07%
   - 6h (n=146) : retour [-6.89% .. +7.7%] · haut q95 +9.56% · bas q05 -8.84%
   - session (n=146) : retour [-7.13% .. +8.04%] · haut q95 +9.56% · bas q05 -8.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.4  _(momentum baissier)_
- **ADX** : 30.8  _(tendance etablie)_
- **MACD** : hist -60417.442  _(pas de croisement recent)_
- **BB** : %B -0.0 · largeur 58.2%
- **ATR** : 212785.71 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.306  _(distribution)_
- **Vol ratio** : 1.74  _(volume au-dessus de la moyenne)_
- **Choppiness** : 39.2  _(transition)_
- **MA** : MA20 1985900.0 · MA50 2179254.84 · MA200 1163029.94  _(prix < MA20)_
- **Dist MA** : MA20 -29.3% · MA50 -35.6% · MA200 +20.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86936 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
