# IONQ

**Generated** : 2026-07-02T00:18:09.083277+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $51.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $51.40 (+11.1% vs entrée) · entrée $46.26 · stop $44.50 · T1 $49.78 · R/R 2.0  
> ↳ P(T1 av. stop) 33 % · EV/risk -0.003 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $45.55–$46.96 (mid $46.26)
- Spot actuel : $51.40 (+11.1% au-dessus de la zone — repli à attendre)
- Stop : $44.50 (stop swing_plan-based (-13.43%))
- Targets : T1 $49.78 · R/R 2.0 | T2 $53.29 · R/R 3.99 | T3 $56.81 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $44.50


## Edge, scénarios & sizing

- EV/risk : -0.003 | EV/share : $-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 17 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 16.4 | bear 22.9 | side 60.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 257.0 (= 5 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.546% → cible +3.401% / stop −3.0%, p_fill 36%, n_eff≈15.4) : P(cible|rempli) **38%** · **EV/risk -0.045** (×p_fill ; si rempli -0.38% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→59% · +5.0%→32% · +8.0%→18%
- Range intraday médian 7.68% (p90 12.54%) · excursion haute méd. +3.64% / basse méd. −2.73%
- Profil de vol intra : ouverture 4.818% vs midi 1.602% vs clôture 1.682% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; momentum — autocorr 0.045)_ ; drift intra méd. 0.331% ; recovery-V 45%
- **σ réalisé intraday** 5.364% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 53% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 53.2797 (VA 52.9288–53.6893 ; dernier close 53.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 85% · **stop −4.75%** sous le fill (sous le bruit) · cible +3.44% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.33% · baisse 53% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.3% (p90 −3.03%) · haut méd +0.99% · range méd 2.55%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −3.94%) · haut méd +1.33% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.92% (p90 −5.27%) · haut méd +1.81% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.36% (p90 −5.93%) · haut méd +2.37% · range méd 5.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 53.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (132/159) · gap 48% · délai 0.0min · rebond 73% (94/132) (MFE +2.24%)
   - −1.0% : fill 30min 73% · séance 80% (125/159) · gap 39% · délai 0.0min · rebond 77% (93/125) (MFE +2.75%)
   - −1.5% : fill 30min 69% · séance 77% (120/159) · gap 31% · délai 0.0min · rebond 73% (84/120) (MFE +2.61%)
   - −2.0% : fill 30min 60% · séance 72% (113/159) · gap 20% · délai 0.2min · rebond 74% (80/113) (MFE +2.87%)
   - −3.0% : fill 30min 49% · séance 60% (91/159) · gap 11% · délai 5.2min · rebond 77% (68/91) (MFE +3.45%)
   - −4.0% : fill 30min 30% · séance 47% (74/159) · gap 6% · délai 17.6min · rebond 82% (57/74) (MFE +2.56%)
   - −5.0% : fill 30min 20% · séance 40% (65/159) · gap 3% · délai 29.0min · rebond 85% (56/65) (MFE +3.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.89%) → stop au-delà de −2.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −3.59%) → stop au-delà de −2.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.22% (p90 −3.64%) → stop au-delà de −2.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1112 jambes) : jambe baissière méd −1.35% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 100% (70/70) · rebond 77% (52/70)
      · −2.0% : fill 93% (66/70) · rebond 80% (52/66)
      · −3.0% : fill 80% (56/70) · rebond 76% (44/56)
      · −4.0% : fill 62% (44/70) · rebond 81% (36/44)
      · −5.0% : fill 53% (38/70) · rebond 80% (32/38)
   - **flat** (16 séances) :
      · −1.0% : fill 78% (13/16) · rebond 83% (9/13)
      · −2.0% : fill 59% (12/16) · rebond 48% (6/12)
      · −3.0% : fill 44% (9/16) · rebond 50% (5/9)
      · −4.0% : fill 40% (7/16) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/16) · rebond 91% (6/7)
   - **gap-up** (73 séances) :
      · −1.0% : fill 55% (42/73) · rebond 77% (32/42)
      · −2.0% : fill 48% (35/73) · rebond 64% (22/35)
      · −3.0% : fill 38% (26/73) · rebond 85% (19/26)
      · −4.0% : fill 29% (23/73) · rebond 88% (18/23)
      · −5.0% : fill 24% (20/73) · rebond 97% (18/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 63% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 24% si rouge (base 52% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **83%** · continue >prix actuel 58% ; creux résiduel méd -2.09% (q20 -3.48%) → **SL/trailing à −3.48%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.15% / q75 +3.43% → **scale +2.15% / runner +3.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **24%** (continue à baisser 49%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +2.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +7.17%] · haut q95 +8.17% · bas q05 -6.05%
   - 60min (n=160) : retour [-5.27% .. +6.16%] · haut q95 +10.71% · bas q05 -6.79%
   - 2h (n=160) : retour [-6.64% .. +8.57%] · haut q95 +11.29% · bas q05 -7.62%
   - 4h (n=160) : retour [-7.68% .. +8.44%] · haut q95 +12.36% · bas q05 -8.61%
   - 6h (n=160) : retour [-7.63% .. +7.64%] · haut q95 +12.69% · bas q05 -10.05%
   - session (n=160) : retour [-7.51% .. +9.56%] · haut q95 +12.71% · bas q05 -10.05%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.91% / p90 2.69%) · ~4.38 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=47)
   - −1.0% → **74%** (reprise méd 20.0 min, n=29)
   - −1.5% → **60%** (reprise méd 36.27 min, n=15)
   - −2.0% → **52%** (reprise méd 29.52 min, n=9)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.69%** (p90, défaut prudent ; serré/agressif −1.91%) ; extension open→close méd +7.85% (q75 +12.44% / q95 +18.2%), MFE méd +9.42% / q90 +18.49%
   - Échelle scale-out : +9.42% (33%) / +13.0% (33%) / +18.49% (34%)
- **DÉSARMER** : repli > **−2.69%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.49% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +1.02%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.6  _(momentum baissier)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -1.096  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 33.4%
- **ATR** : 4.56 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.362  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 54.7  _(transition)_
- **MA** : MA20 56.96 · MA50 54.9 · MA200 49.64  _(prix < MA20)_
- **Dist MA** : MA20 -9.8% · MA50 -6.4% · MA200 +3.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92603 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
