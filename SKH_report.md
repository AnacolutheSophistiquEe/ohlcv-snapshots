# 000660

**Generated** : 2026-07-29T00:12:42.704665+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1550000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩1550000.00 (+20.1% vs entrée) · entrée ₩1291125.75 · stop ₩1226997.62 · T1 ₩1419382.00 · R/R 2.0  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.695 · ¼-Kelly 0.03 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -50 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1265474.50–₩1316777.00 (mid ₩1291125.75)
- Spot actuel : ₩1550000.00 (+20.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1226997.62 (stop swing_plan-based (-20.84%))
- Targets : T1 ₩1419382.00 · R/R 2.0 | T2 ₩1547638.25 · R/R 4.0 | T3 ₩1675894.51 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1226997.62


## Edge, scénarios & sizing

- EV/risk : 0.695 | EV/share : ₩44579.357 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.12 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.6 | bear 62.9 | side 26.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→80% · +2.0%→54% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.26% (p90 11.16%) · excursion haute méd. +2.16% / basse méd. −2.59%
- Profil de vol intra : ouverture 3.025% vs midi 1.253% vs clôture 1.518% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 69% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.905% ; recovery-V 29%
- **σ réalisé intraday** 4.981% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 72% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 1754612.5 (VA 1732012.5–1782862.5 ; dernier close 1820000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 38% · rebond 78% · **stop −7.87%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.33 (high win-rate)
- Gaps overnight (n=144) : méd. 0.0% · baisse 49% (gap-down >1% 34% · >2% 27%)
- Excursion ouverture 5min (n=145) : bas méd −0.64% (p90 −1.83%) · haut méd +0.91% · range méd 1.55%
- Excursion ouverture 15min (n=145) : bas méd −0.79% (p90 −2.72%) · haut méd +1.17% · range méd 2.17%
- Excursion ouverture 30min (n=145) : bas méd −1.3% (p90 −3.48%) · haut méd +1.3% · range méd 2.76%
- Excursion ouverture 60min (n=145) : bas méd −1.34% (p90 −4.01%) · haut méd +1.57% · range méd 3.64%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1820000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (91/144) · gap 41% · délai 0.0min · rebond 56% (48/91) (MFE +1.64%)
   - −1.0% : fill 30min 54% · séance 63% (83/144) · gap 34% · délai 0.0min · rebond 66% (52/83) (MFE +2.12%)
   - −1.5% : fill 30min 49% · séance 59% (74/144) · gap 32% · délai 0.0min · rebond 67% (47/74) (MFE +2.18%)
   - −2.0% : fill 30min 42% · séance 53% (67/144) · gap 27% · délai 0.0min · rebond 65% (44/67) (MFE +2.04%)
   - −3.0% : fill 30min 39% · séance 46% (57/144) · gap 22% · délai 3.0min · rebond 76% (42/57) (MFE +2.56%)
   - −4.0% : fill 30min 29% · séance 38% (44/144) · gap 13% · délai 6.2min · rebond 78% (34/44) (MFE +2.57%)
   - −5.0% : fill 30min 14% · séance 31% (35/144) · gap 10% · délai 30.4min · rebond 76% (27/35) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.5%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.41%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −3.64%) → stop au-delà de −2.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=753 jambes) : jambe baissière méd −1.3% (p90 −3.34%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 98% (60/62) · rebond 53% (32/60)
      · −2.0% : fill 88% (51/62) · rebond 59% (30/51)
      · −3.0% : fill 83% (46/62) · rebond 72% (32/46)
      · −4.0% : fill 74% (39/62) · rebond 75% (29/39)
      · −5.0% : fill 62% (32/62) · rebond 73% (24/32)
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
- **P(clôture VERTE) selon le drive 15min** (n=145) : 46% en base · 51% si les 15 1res min sont vertes (78 cas) · 38% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **1:35** → P(séance verte=clôture>ouverture) 77% si début vert vs 16% si rouge (base 46% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.63% (q20 -4.87%) → **SL/trailing à −4.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.43% → **scale +1.66% / runner +3.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=68) : edge inversé — récupère vert seulement **16%** (continue à baisser 64%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.66%** (au-delà de la MAE q10 -6.66%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-3.01% .. +3.26%] · haut q95 +3.81% · bas q05 -3.77%
   - 60min (n=145) : retour [-3.45% .. +5.58%] · haut q95 +6.47% · bas q05 -5.0%
   - 2h (n=145) : retour [-4.39% .. +5.47%] · haut q95 +8.3% · bas q05 -6.18%
   - 4h (n=145) : retour [-6.46% .. +6.98%] · haut q95 +8.49% · bas q05 -8.08%
   - 6h (n=145) : retour [-6.93% .. +7.71%] · haut q95 +9.59% · bas q05 -8.87%
   - session (n=145) : retour [-7.13% .. +8.05%] · haut q95 +9.59% · bas q05 -8.87%


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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 31.7  _(momentum baissier)_
- **ADX** : 29.4  _(tendance etablie)_
- **MACD** : hist -49362.365  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 56.9%
- **ATR** : 204214.29 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.304  _(distribution)_
- **Vol ratio** : 1.35  _(volume normal)_
- **Choppiness** : 49.3  _(transition)_
- **MA** : MA20 2048200.0 · MA50 2187548.75 · MA200 1157750.18  _(prix < MA20)_
- **Dist MA** : MA20 -24.3% · MA50 -29.1% · MA200 +33.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86381 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
