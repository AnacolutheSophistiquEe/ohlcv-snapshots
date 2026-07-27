# 000660

**Generated** : 2026-07-27T00:12:24.242170+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1759000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩1759000.00 (+2.3% vs entrée) · entrée ₩1719407.38 · stop ₩1569194.46 · T1 ₩2019833.22 · R/R 2.0  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.219 _(réel 5 s)_ (GBM 0.439) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1687569.81–₩1751244.96 (mid ₩1719407.38)
- Spot actuel : ₩1759000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩1569194.46 (stop swing_plan-based (-10.79%))
- Targets : T1 ₩2019833.22 · R/R 2.0 | T2 ₩2107678.53 · R/R 2.58 | T3 ₩2195523.83 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1569194.46


## Edge, scénarios & sizing

- EV/risk : 0.439 | EV/share : ₩65989.688 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 12 % | T3 6 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.7 | bear 62.9 | side 22.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.02% → cible +6.548% / stop −3.627%, p_fill 83%, n_eff≈31.6) : P(cible|rempli) **14%** · **EV/risk -0.235** (×p_fill ; si rempli -1.03% du capital)
  - **swing** (entrée dip −2.25% → cible +17.473% / stop −8.736%, p_fill 75%, n_eff≈28.6) : P(cible|rempli) **14%** · **EV/risk -0.219** (×p_fill ; si rempli -2.55% du capital)
  - **deep** (entrée dip −3.48% → cible +13.054% / stop −6.527%, p_fill 75%, n_eff≈25.6) : P(cible|rempli) **21%** · **EV/risk -0.338** (×p_fill ; si rempli -2.93% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→81% · +2.0%→55% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.23% (p90 11.16%) · excursion haute méd. +2.24% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.006% vs midi 1.241% vs clôture 1.511% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (144 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 68% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.963% ; recovery-V 25%
- **σ réalisé intraday** 4.97% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 71% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 1784475.0 (VA 1757675.0–1824675.0 ; dernier close 1759000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 39% · rebond 78% · **stop −7.87%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.33 (high win-rate)
- Gaps overnight (n=143) : méd. -0.01% · baisse 50% (gap-down >1% 35% · >2% 28%)
- Excursion ouverture 5min (n=144) : bas méd −0.58% (p90 −1.76%) · haut méd +0.92% · range méd 1.53%
- Excursion ouverture 15min (n=144) : bas méd −0.79% (p90 −2.48%) · haut méd +1.18% · range méd 2.14%
- Excursion ouverture 30min (n=144) : bas méd −1.28% (p90 −3.04%) · haut méd +1.3% · range méd 2.75%
- Excursion ouverture 60min (n=144) : bas méd −1.34% (p90 −4.09%) · haut méd +1.6% · range méd 3.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1759000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 67% (90/143) · gap 41% · délai 0.0min · rebond 54% (47/90) (MFE +1.34%)
   - −1.0% : fill 30min 55% · séance 63% (82/143) · gap 35% · délai 0.0min · rebond 64% (51/82) (MFE +1.85%)
   - −1.5% : fill 30min 50% · séance 58% (73/143) · gap 32% · délai 0.0min · rebond 66% (46/73) (MFE +1.84%)
   - −2.0% : fill 30min 42% · séance 52% (66/143) · gap 28% · délai 0.0min · rebond 64% (43/66) (MFE +1.85%)
   - −3.0% : fill 30min 40% · séance 47% (57/143) · gap 22% · délai 3.0min · rebond 76% (42/57) (MFE +2.56%)
   - −4.0% : fill 30min 29% · séance 39% (44/143) · gap 13% · délai 6.2min · rebond 78% (34/44) (MFE +2.57%)
   - −5.0% : fill 30min 14% · séance 31% (35/143) · gap 10% · délai 30.4min · rebond 76% (27/35) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.5%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.41%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −3.64%) → stop au-delà de −2.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=744 jambes) : jambe baissière méd −1.31% (p90 −3.34%) · ~13.0 jambes/séance
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
   - **gap-up** (69 séances) :
      · −1.0% : fill 24% (13/69) · rebond 98% (12/13)
      · −2.0% : fill 13% (8/69) · rebond 75% (7/8)
      · −3.0% : fill 11% (6/69) · rebond 91% (5/6)
      · −4.0% : fill 7% (3/69) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=144) : 45% en base · 51% si les 15 1res min sont vertes (78 cas) · 36% si rouges (66 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=144) : COUDE à **1:35** → P(séance verte=clôture>ouverture) 77% si début vert vs 12% si rouge (base 45% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.63% (q20 -4.87%) → **SL/trailing à −4.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.43% → **scale +1.66% / runner +3.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **12%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.68%** (au-delà de la MAE q10 -6.68%), cible rebond +1.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=144) : retour [-3.01% .. +3.32%] · haut q95 +3.86% · bas q05 -3.64%
   - 60min (n=144) : retour [-3.46% .. +5.61%] · haut q95 +6.6% · bas q05 -5.03%
   - 2h (n=144) : retour [-4.43% .. +5.48%] · haut q95 +8.31% · bas q05 -5.99%
   - 4h (n=144) : retour [-6.5% .. +7.0%] · haut q95 +8.5% · bas q05 -8.08%
   - 6h (n=144) : retour [-6.98% .. +7.73%] · haut q95 +9.62% · bas q05 -8.89%
   - session (n=144) : retour [-7.13% .. +8.06%] · haut q95 +9.62% · bas q05 -8.89%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 9 séances trend-up (n_eff 7.5)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 30.2  _(momentum baissier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist -49784.22  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 58.2%
- **ATR** : 210500.0 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.282  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 2144950.0 · MA50 2199135.56 · MA200 1144375.75  _(prix < MA20)_
- **Dist MA** : MA20 -18.0% · MA50 -20.0% · MA200 +53.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87237 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
