# IONQ

**Generated** : 2026-07-01T00:16:30.896550+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $53.26  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $53.26 (+5.5% vs entrée) · entrée $50.46 · stop $48.61 · T1 $54.16 · R/R 2.0  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.029 · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.67% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $50.11–$50.81 (mid $50.46)
- Spot actuel : $53.26 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : $48.61 (stop swing_plan-based (-14.97%))
- Targets : T1 $54.16 · R/R 2.0 | T2 $54.91 · R/R 2.41 | T3 $55.66 · R/R 2.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $48.61


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : $-0.053 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.112 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.2 | bear 55.5 | side 27.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 266.0 (= 5 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.262% → cible +7.343% / stop −3.671%, p_fill 27%, n_eff≈11.6) : P(cible|rempli) **2%** · **EV/risk -0.059** (×p_fill ; si rempli -0.79% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→57% · +5.0%→32% · +8.0%→18%
- Range intraday médian 7.68% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.73%
- Profil de vol intra : ouverture 4.825% vs midi 1.605% vs clôture 1.691% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 76% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; momentum — autocorr 0.041)_ ; drift intra méd. 0.291% ; recovery-V 45%
- **σ réalisé intraday** 5.469% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 55% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 53.1141 (VA 52.0949–54.1334 ; dernier close 53.91)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 85% · **stop −4.75%** sous le fill (sous le bruit) · cible +3.44% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 52% (gap-down >1% 38% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.31% (p90 −3.05%) · haut méd +0.97% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.84% (p90 −3.95%) · haut méd +1.29% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.95% (p90 −5.3%) · haut méd +1.79% · range méd 4.37%
- Excursion ouverture 60min (n=160) : bas méd −2.44% (p90 −5.97%) · haut méd +2.22% · range méd 5.6%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 53.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (132/159) · gap 47% · délai 0.0min · rebond 72% (93/132) (MFE +2.26%)
   - −1.0% : fill 30min 72% · séance 80% (125/159) · gap 38% · délai 0.0min · rebond 77% (92/125) (MFE +2.71%)
   - −1.5% : fill 30min 68% · séance 77% (120/159) · gap 30% · délai 0.0min · rebond 72% (84/120) (MFE +2.53%)
   - −2.0% : fill 30min 59% · séance 71% (113/159) · gap 18% · délai 0.3min · rebond 73% (80/113) (MFE +2.71%)
   - −3.0% : fill 30min 50% · séance 61% (92/159) · gap 11% · délai 5.3min · rebond 77% (69/92) (MFE +3.43%)
   - −4.0% : fill 30min 30% · séance 48% (74/159) · gap 6% · délai 17.6min · rebond 82% (57/74) (MFE +2.56%)
   - −5.0% : fill 30min 21% · séance 41% (65/159) · gap 3% · délai 29.0min · rebond 85% (56/65) (MFE +3.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.89%) → stop au-delà de −2.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.14% (p90 −3.63%) → stop au-delà de −2.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.28% (p90 −3.68%) → stop au-delà de −2.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1115 jambes) : jambe baissière méd −1.35% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 100% (69/69) · rebond 76% (51/69)
      · −2.0% : fill 93% (65/69) · rebond 79% (51/65)
      · −3.0% : fill 82% (56/69) · rebond 76% (44/56)
      · −4.0% : fill 64% (44/69) · rebond 81% (36/44)
      · −5.0% : fill 55% (38/69) · rebond 80% (32/38)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 81% (9/14)
      · −2.0% : fill 60% (13/17) · rebond 49% (7/13)
      · −3.0% : fill 45% (10/17) · rebond 52% (6/10)
      · −4.0% : fill 40% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/17) · rebond 91% (6/7)
   - **gap-up** (73 séances) :
      · −1.0% : fill 55% (42/73) · rebond 77% (32/42)
      · −2.0% : fill 48% (35/73) · rebond 64% (22/35)
      · −3.0% : fill 38% (26/73) · rebond 85% (19/26)
      · −4.0% : fill 29% (23/73) · rebond 88% (18/23)
      · −5.0% : fill 24% (20/73) · rebond 97% (18/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 62% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 82% si début vert vs 24% si rouge (base 51% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **82%** · continue >prix actuel 57% ; creux résiduel méd -2.16% (q20 -3.55%) → **SL/trailing à −3.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.25% / q75 +3.46% → **scale +2.25% / runner +3.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **24%** (continue à baisser 49%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +2.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.19% .. +7.17%] · haut q95 +8.21% · bas q05 -6.11%
   - 60min (n=160) : retour [-5.29% .. +6.46%] · haut q95 +10.9% · bas q05 -6.8%
   - 2h (n=160) : retour [-6.64% .. +8.8%] · haut q95 +11.43% · bas q05 -7.63%
   - 4h (n=160) : retour [-7.68% .. +8.74%] · haut q95 +12.45% · bas q05 -8.64%
   - 6h (n=160) : retour [-7.67% .. +7.64%] · haut q95 +12.78% · bas q05 -10.1%
   - session (n=160) : retour [-7.55% .. +9.59%] · haut q95 +12.8% · bas q05 -10.1%


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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.1  _(momentum baissier)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -1.166  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 38.4%
- **ATR** : 4.62 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.315  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 55.2  _(transition)_
- **MA** : MA20 57.96 · MA50 54.84 · MA200 49.66  _(prix < MA20)_
- **Dist MA** : MA20 -8.1% · MA50 -2.9% · MA200 +7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93464 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
