# SOI

**Generated** : 2026-07-29T21:44:06.318552+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €96.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €96.20 (+9.1% vs entrée) · entrée €88.20 · stop €83.95 · T1 €96.71 · R/R 2.0  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.061 _(réel 5 s)_ (GBM 0.297) · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -124 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €86.50–€89.90 (mid €88.20)
- Spot actuel : €96.20 (+9.1% au-dessus de la zone — repli à attendre)
- Stop : €83.95 (stop swing_plan-based (-12.73%))
- Targets : T1 €96.71 · R/R 2.0 | T2 €105.21 · R/R 4.0 | T3 €113.72 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €83.95


## Edge, scénarios & sizing

- EV/risk : 0.297 | EV/share : €1.261 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 16 % | T3 12 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.7 | bear 84.1 | side 6.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 96.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.774% → cible +4.312% / stop −3.29%, p_fill 54%, n_eff≈20.9) : P(cible|rempli) **32%** · **EV/risk -0.081** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −8.309% → cible +9.642% / stop −4.821%, p_fill 36%, n_eff≈16.4) : P(cible|rempli) **29%** · **EV/risk -0.061** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −12.848% → cible +13.636% / stop −6.818%, p_fill 38%, n_eff≈14.1) : P(cible|rempli) **38%** · **EV/risk +0.050** (×p_fill ; si rempli +0.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→69% · +3.0%→59% · +5.0%→45% · +8.0%→22%
- Range intraday médian 9.52% (p90 17.62%) · excursion haute méd. +3.82% / basse méd. −3.47%
- Profil de vol intra : ouverture 6.03% vs midi 1.707% vs clôture 2.617% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. -0.804% ; recovery-V 35%
- **σ réalisé intraday** 5.72% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 98.3025 (VA 94.8825–99.7275 ; dernier close 97.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 78% · **stop −7.29%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.38 (high win-rate)
- Gaps overnight (n=141) : méd. 0.02% · baisse 50% (gap-down >1% 33% · >2% 25%)
- Excursion ouverture 5min (n=142) : bas méd −1.27% (p90 −3.84%) · haut méd +1.0% · range méd 3.17%
- Excursion ouverture 15min (n=142) : bas méd −1.55% (p90 −5.22%) · haut méd +1.34% · range méd 3.91%
- Excursion ouverture 30min (n=142) : bas méd −1.75% (p90 −5.67%) · haut méd +1.78% · range méd 4.39%
- Excursion ouverture 60min (n=142) : bas méd −1.85% (p90 −6.06%) · haut méd +1.89% · range méd 4.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (111/141) · gap 40% · délai 0.0min · rebond 64% (72/111) (MFE +1.89%)
   - −1.0% : fill 30min 64% · séance 75% (106/141) · gap 33% · délai 0.1min · rebond 70% (76/106) (MFE +1.83%)
   - −1.5% : fill 30min 60% · séance 72% (97/141) · gap 30% · délai 0.2min · rebond 73% (71/97) (MFE +2.18%)
   - −2.0% : fill 30min 56% · séance 67% (90/141) · gap 25% · délai 0.2min · rebond 76% (71/90) (MFE +2.67%)
   - −3.0% : fill 30min 42% · séance 58% (75/141) · gap 18% · délai 0.4min · rebond 74% (59/75) (MFE +2.8%)
   - −4.0% : fill 30min 34% · séance 50% (61/141) · gap 8% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 25% · séance 46% (53/141) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −3.77%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −3.03%) → stop au-delà de −2.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.19%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1247 jambes) : jambe baissière méd −1.34% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 98% (55/56) · rebond 59% (34/55)
      · −2.0% : fill 94% (53/56) · rebond 71% (41/53)
      · −3.0% : fill 85% (45/56) · rebond 72% (36/45)
      · −4.0% : fill 77% (40/56) · rebond 81% (33/40)
      · −5.0% : fill 70% (35/56) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (34/68) · rebond 85% (28/34)
      · −2.0% : fill 33% (22/68) · rebond 85% (18/22)
      · −3.0% : fill 30% (19/68) · rebond 83% (15/19)
      · −4.0% : fill 22% (13/68) · rebond 55% (9/13)
      · −5.0% : fill 20% (10/68) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 51% en base · 71% si les 15 1res min sont vertes (66 cas) · 30% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=142) : COUDE à **37min** → P(séance verte=clôture>ouverture) 84% si début vert vs 21% si rouge (base 51% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **84%** · continue >prix actuel 61% ; creux résiduel méd -2.14% (q20 -5.51%) → **SL/trailing à −5.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.38% / q75 +5.39% → **scale +3.38% / runner +5.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.77%** (au-delà de la MAE q10 -8.77%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-5.29% .. +7.15%] · haut q95 +7.97% · bas q05 -6.66%
   - 60min (n=142) : retour [-6.0% .. +7.38%] · haut q95 +9.37% · bas q05 -7.18%
   - 2h (n=142) : retour [-6.42% .. +10.06%] · haut q95 +12.62% · bas q05 -8.09%
   - 4h (n=142) : retour [-7.16% .. +10.3%] · haut q95 +14.28% · bas q05 -8.34%
   - 6h (n=142) : retour [-8.33% .. +11.68%] · haut q95 +14.33% · bas q05 -10.2%
   - session (n=142) : retour [-11.65% .. +13.89%] · haut q95 +16.2% · bas q05 -13.95%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.3% des séances sont trend-up (mild 0% / strong 6.3%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 5% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 45.0  _(momentum baissier)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist 1.706  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 38.5%
- **ATR** : 10.15 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.123  _(distribution)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 101.72 · MA50 125.23 · MA200 70.34  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -23.2% · MA200 +36.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98800 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
