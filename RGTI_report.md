# RGTI

**Generated** : 2026-07-10T00:28:24.464657+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $16.99  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.99 (+1.1% vs entrée) · entrée $16.80 · stop $16.30 · T1 $17.25 · R/R 0.9  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk -0.028 _(réel 5 s)_ (GBM 0.074) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.71–$16.89 (mid $16.80)
- Spot actuel : $16.99 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $16.30 (stop swing_plan-based (-5.36%))
- Targets : T1 $17.25 · R/R 0.9 | T2 $17.70 · R/R 1.8 | T3 $18.15 · R/R 2.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.30


## Edge, scénarios & sizing

- EV/risk : 0.074 | EV/share : $0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.072 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.2 | bear 72.0 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.103% → cible +2.684% / stop −3.0%, p_fill 84%, n_eff≈36.0) : P(cible|rempli) **52%** · **EV/risk -0.028** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.433% → cible +6.001% / stop −3.0%, p_fill 76%, n_eff≈30.3) : P(cible|rempli) **25%** · **EV/risk -0.190** (×p_fill ; si rempli -0.76% du capital)
  - **deep** (entrée dip −3.767% → cible +8.486% / stop −4.243%, p_fill 78%, n_eff≈29.7) : P(cible|rempli) **31%** · **EV/risk -0.096** (×p_fill ; si rempli -0.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→82% · +2.0%→70% · +3.0%→56% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.55% / basse méd. −3.0%
- Profil de vol intra : ouverture 5.234% vs midi 1.694% vs clôture 1.95% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 46%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; momentum — autocorr 0.054)_ ; drift intra méd. -0.067% ; recovery-V 46%
- **σ réalisé intraday** 5.451% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 49% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 16.807 (VA 16.609–16.915 ; dernier close 16.929)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 64% · rebond 76% · **stop −7.38%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.61% · baisse 60% (gap-down >1% 46% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.35% (p90 −2.96%) · haut méd +1.06% · range méd 2.62%
- Excursion ouverture 15min (n=160) : bas méd −1.54% (p90 −4.44%) · haut méd +1.55% · range méd 3.71%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −6.02%) · haut méd +2.08% · range méd 4.71%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −6.62%) · haut méd +2.48% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.929 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 80% · séance 86% (137/159) · gap 53% · délai 0.0min · rebond 70% (91/137) (MFE +2.46%)
   - −1.0% : fill 30min 72% · séance 84% (133/159) · gap 46% · délai 0.0min · rebond 69% (88/133) (MFE +2.22%)
   - −1.5% : fill 30min 66% · séance 79% (125/159) · gap 40% · délai 0.0min · rebond 67% (83/125) (MFE +2.54%)
   - −2.0% : fill 30min 60% · séance 73% (115/159) · gap 29% · délai 0.0min · rebond 66% (75/115) (MFE +2.72%)
   - −3.0% : fill 30min 52% · séance 64% (98/159) · gap 12% · délai 1.3min · rebond 76% (72/98) (MFE +2.67%)
   - −4.0% : fill 30min 38% · séance 48% (78/159) · gap 5% · délai 4.6min · rebond 78% (58/78) (MFE +2.41%)
   - −5.0% : fill 30min 25% · séance 42% (66/159) · gap 2% · délai 19.8min · rebond 69% (50/66) (MFE +1.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.94% (p90 −2.99%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.29% (p90 −4.08%) → stop au-delà de −2.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.29% (p90 −4.25%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1183 jambes) : jambe baissière méd −1.32% (p90 −3.36%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 98% (84/85) · rebond 65% (51/84)
      · −2.0% : fill 90% (79/85) · rebond 67% (53/79)
      · −3.0% : fill 83% (71/85) · rebond 75% (52/71)
      · −4.0% : fill 64% (57/85) · rebond 78% (43/57)
      · −5.0% : fill 56% (50/85) · rebond 69% (40/50)
   - **flat** (15 séances) :
      · −1.0% : fill 89% (13/15) · rebond 88% (11/13)
      · −2.0% : fill 62% (10/15) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/15) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 58% (36/59) · rebond 73% (26/36)
      · −2.0% : fill 46% (26/59) · rebond 65% (15/26)
      · −3.0% : fill 36% (22/59) · rebond 83% (17/22)
      · −4.0% : fill 24% (16/59) · rebond 78% (12/16)
      · −5.0% : fill 18% (11/59) · rebond 55% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 65% si les 15 1res min sont vertes (79 cas) · 39% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 16% si rouge (base 53% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **91%** · continue >prix actuel 56% ; creux résiduel méd -2.3% (q20 -3.53%) → **SL/trailing à −3.53%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.81% / q75 +4.27% → **scale +2.81% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.81%** (au-delà de la MAE q10 -5.81%), cible rebond +2.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.66% .. +5.26%] · haut q95 +7.96% · bas q05 -6.94%
   - 60min (n=160) : retour [-6.09% .. +7.15%] · haut q95 +9.46% · bas q05 -7.27%
   - 2h (n=160) : retour [-7.51% .. +8.33%] · haut q95 +9.7% · bas q05 -8.26%
   - 4h (n=160) : retour [-8.71% .. +6.55%] · haut q95 +9.73% · bas q05 -10.48%
   - 6h (n=160) : retour [-8.77% .. +8.5%] · haut q95 +10.39% · bas q05 -10.48%
   - session (n=160) : retour [-7.96% .. +9.85%] · haut q95 +10.91% · bas q05 -10.48%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 11% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.86% / p90 2.7%) · ~4.0 replis/séance, durée méd 40.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **93%** (reprise méd 11.1 min, n=44)
   - −1.0% → **90%** (reprise méd 30.5 min, n=27)
   - −1.5% → **81%** (reprise méd 43.22 min, n=12)
   - −2.0% → **70%** (reprise méd 138.94 min, n=8)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.7%** (p90, défaut prudent ; serré/agressif −1.86%) ; extension open→close méd +8.33% (q75 +9.92% / q95 +12.86%), MFE méd +9.1% / q90 +12.37%
   - Échelle scale-out : +9.1% (33%) / +10.39% (33%) / +12.37% (34%)
- **DÉSARMER** : repli > **−2.7%** depuis le plus-haut = décay → P(retournement) **74%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.37% : P(retournement après) 0% (mèche méd 0.52%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.96%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.1  _(momentum baissier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist -0.376  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 35.1%
- **ATR** : 1.56 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.198  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 19.44 · MA50 20.15 · MA200 23.75  _(prix < MA20)_
- **Dist MA** : MA20 -12.6% · MA50 -15.7% · MA200 -28.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88250 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
