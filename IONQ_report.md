# IONQ

**Generated** : 2026-07-08T00:16:58.091051+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $45.36  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $45.36 (+2.4% vs entrée) · entrée $44.28 · stop $42.77 · T1 $47.30 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk 0.07 _(réel 5 s)_ (GBM 0.003) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -48 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $43.67–$44.88 (mid $44.28)
- Spot actuel : $45.36 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $42.77 (stop swing_plan-based (-5.72%))
- Targets : T1 $47.30 · R/R 2.0 | T2 $50.33 · R/R 4.01 | T3 $53.35 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $42.77


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : $0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 20 % | T3 10 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.2 | bear 22.5 | side 60.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.089% → cible +3.054% / stop −3.004%, p_fill 81%, n_eff≈33.6) : P(cible|rempli) **47%** · **EV/risk -0.044** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −2.387% → cible +6.829% / stop −3.415%, p_fill 75%, n_eff≈31.1) : P(cible|rempli) **36%** · **EV/risk +0.070** (×p_fill ; si rempli +0.32% du capital)
  - **deep** (entrée dip −3.689% → cible +9.658% / stop −4.829%, p_fill 81%, n_eff≈30.2) : P(cible|rempli) **44%** · **EV/risk +0.225** (×p_fill ; si rempli +1.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→70% · +3.0%→64% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.82% (p90 12.54%) · excursion haute méd. +3.78% / basse méd. −2.66%
- Profil de vol intra : ouverture 4.944% vs midi 1.604% vs clôture 1.683% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; momentum — autocorr 0.046)_ ; drift intra méd. -0.122% ; recovery-V 38%
- **σ réalisé intraday** 5.233% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 61% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 49.4038 (VA 48.9663–50.7163 ; dernier close 48.86)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 86% · **stop −4.72%** sous le fill (sous le bruit) · cible +3.12% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 54% (gap-down >1% 38% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.99%) · haut méd +1.03% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −3.9%) · haut méd +1.34% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.85% (p90 −5.19%) · haut méd +2.0% · range méd 4.44%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −5.86%) · haut méd +2.65% · range méd 5.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 48.86 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (133/159) · gap 48% · délai 0.0min · rebond 73% (94/133) (MFE +2.32%)
   - −1.0% : fill 30min 71% · séance 80% (125/159) · gap 38% · délai 0.0min · rebond 79% (93/125) (MFE +2.76%)
   - −1.5% : fill 30min 68% · séance 77% (120/159) · gap 31% · délai 0.0min · rebond 75% (85/120) (MFE +2.79%)
   - −2.0% : fill 30min 57% · séance 70% (112/159) · gap 20% · délai 0.2min · rebond 75% (80/112) (MFE +2.85%)
   - −3.0% : fill 30min 47% · séance 59% (90/159) · gap 10% · délai 5.0min · rebond 75% (67/90) (MFE +3.43%)
   - −4.0% : fill 30min 28% · séance 45% (72/159) · gap 5% · délai 18.5min · rebond 79% (55/72) (MFE +2.48%)
   - −5.0% : fill 30min 19% · séance 39% (63/159) · gap 3% · délai 31.2min · rebond 86% (55/63) (MFE +3.12%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.89%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.46%) → stop au-delà de −2.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.13% (p90 −3.49%) → stop au-delà de −2.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1115 jambes) : jambe baissière méd −1.34% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 100% (71/71) · rebond 78% (53/71)
      · −2.0% : fill 94% (67/71) · rebond 82% (53/67)
      · −3.0% : fill 81% (57/71) · rebond 74% (44/57)
      · −4.0% : fill 61% (44/71) · rebond 76% (35/44)
      · −5.0% : fill 52% (38/71) · rebond 81% (32/38)
   - **flat** (17 séances) :
      · −1.0% : fill 64% (13/17) · rebond 83% (9/13)
      · −2.0% : fill 48% (12/17) · rebond 48% (6/12)
      · −3.0% : fill 36% (9/17) · rebond 50% (5/9)
      · −4.0% : fill 33% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 33% (7/17) · rebond 91% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 57% (41/71) · rebond 78% (31/41)
      · −2.0% : fill 45% (33/71) · rebond 64% (21/33)
      · −3.0% : fill 36% (24/71) · rebond 86% (18/24)
      · −4.0% : fill 27% (21/71) · rebond 89% (17/21)
      · −5.0% : fill 22% (18/71) · rebond 98% (17/18)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 55% si les 15 1res min sont vertes (80 cas) · 41% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 54% ; creux résiduel méd -2.22% (q20 -4.24%) → **SL/trailing à −4.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +3.36% → **scale +1.91% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 53%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.43%** (au-delà de la MAE q10 -5.43%), cible rebond +2.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.11% .. +7.16%] · haut q95 +8.02% · bas q05 -5.87%
   - 60min (n=160) : retour [-5.19% .. +6.08%] · haut q95 +9.9% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.61% .. +8.49%] · haut q95 +10.65% · bas q05 -7.54%
   - 4h (n=160) : retour [-7.66% .. +7.69%] · haut q95 +11.99% · bas q05 -8.49%
   - 6h (n=160) : retour [-7.51% .. +7.64%] · haut q95 +12.32% · bas q05 -9.26%
   - session (n=160) : retour [-7.36% .. +9.38%] · haut q95 +12.33% · bas q05 -8.88%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.6)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.24% (p75 1.9% / p90 2.72%) · ~4.11 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=44)
   - −1.0% → **74%** (reprise méd 20.47 min, n=27)
   - −1.5% → **60%** (reprise méd 38.13 min, n=14)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.72%** (p90, défaut prudent ; serré/agressif −1.9%) ; extension open→close méd +7.82% (q75 +12.53% / q95 +18.2%), MFE méd +9.35% / q90 +18.66%
   - Échelle scale-out : +9.35% (33%) / +13.03% (33%) / +18.66% (34%)
- **DÉSARMER** : repli > **−2.72%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.66% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.5  _(survente)_
- **ADX** : 20.8  _(pas de tendance nette)_
- **MACD** : hist -1.262  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 32.7%
- **ATR** : 4.49 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.331  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 47.5  _(transition)_
- **MA** : MA20 54.6 · MA50 55.02 · MA200 49.43  _(prix < MA20)_
- **Dist MA** : MA20 -16.9% · MA50 -17.6% · MA200 -8.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88573 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
