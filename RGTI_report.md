# RGTI

**Generated** : 2026-07-09T00:21:48.727095+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $16.92  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.92 (+1.0% vs entrée) · entrée $16.75 · stop $16.25 · T1 $17.24 · R/R 0.98  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk -0.029 _(réel 5 s)_ (GBM 0.058) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.65–$16.85 (mid $16.75)
- Spot actuel : $16.92 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $16.25 (stop swing_plan-based (-5.4%))
- Targets : T1 $17.24 · R/R 0.98 | T2 $17.72 · R/R 1.94 | T3 $18.21 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.25


## Edge, scénarios & sizing

- EV/risk : 0.058 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.08 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.3 | bear 73.0 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.01% → cible +2.908% / stop −3.0%, p_fill 90%, n_eff≈37.5) : P(cible|rempli) **50%** · **EV/risk -0.029** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.221% → cible +6.503% / stop −3.251%, p_fill 75%, n_eff≈30.9) : P(cible|rempli) **28%** · **EV/risk -0.135** (×p_fill ; si rempli -0.58% du capital)
  - **deep** (entrée dip −3.43% → cible +9.196% / stop −4.598%, p_fill 77%, n_eff≈29.5) : P(cible|rempli) **33%** · **EV/risk -0.053** (×p_fill ; si rempli -0.31% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→82% · +2.0%→69% · +3.0%→55% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.44% / basse méd. −3.0%
- Profil de vol intra : ouverture 5.205% vs midi 1.699% vs clôture 1.958% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 46%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; momentum — autocorr 0.061)_ ; drift intra méd. -0.273% ; recovery-V 46%
- **σ réalisé intraday** 5.492% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 51% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 16.6144 (VA 16.3896–16.8393 ; dernier close 16.565)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 65% · rebond 76% · **stop −7.38%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.57% · baisse 59% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.42% (p90 −2.96%) · haut méd +1.04% · range méd 2.62%
- Excursion ouverture 15min (n=160) : bas méd −1.55% (p90 −4.46%) · haut méd +1.54% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.02%) · haut méd +1.96% · range méd 4.67%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.65%) · haut méd +2.4% · range méd 5.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.565 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 86% (137/159) · gap 52% · délai 0.0min · rebond 69% (91/137) (MFE +2.42%)
   - −1.0% : fill 30min 71% · séance 83% (133/159) · gap 45% · délai 0.0min · rebond 69% (88/133) (MFE +2.06%)
   - −1.5% : fill 30min 65% · séance 78% (124/159) · gap 39% · délai 0.0min · rebond 66% (82/124) (MFE +2.41%)
   - −2.0% : fill 30min 60% · séance 72% (114/159) · gap 30% · délai 0.0min · rebond 65% (74/114) (MFE +2.68%)
   - −3.0% : fill 30min 53% · séance 65% (98/159) · gap 13% · délai 1.3min · rebond 76% (72/98) (MFE +2.67%)
   - −4.0% : fill 30min 38% · séance 49% (78/159) · gap 5% · délai 4.6min · rebond 78% (58/78) (MFE +2.41%)
   - −5.0% : fill 30min 26% · séance 43% (66/159) · gap 2% · délai 19.8min · rebond 69% (50/66) (MFE +1.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.03% (p90 −3.03%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.3% (p90 −4.12%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.3% (p90 −4.26%) → stop au-delà de −2.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1183 jambes) : jambe baissière méd −1.33% (p90 −3.44%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 64% (50/83)
      · −2.0% : fill 90% (78/84) · rebond 66% (52/78)
      · −3.0% : fill 86% (71/84) · rebond 75% (52/71)
      · −4.0% : fill 66% (57/84) · rebond 78% (43/57)
      · −5.0% : fill 58% (50/84) · rebond 69% (40/50)
   - **flat** (15 séances) :
      · −1.0% : fill 89% (13/15) · rebond 88% (11/13)
      · −2.0% : fill 62% (10/15) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 58% (37/60) · rebond 73% (27/37)
      · −2.0% : fill 46% (26/60) · rebond 65% (15/26)
      · −3.0% : fill 36% (22/60) · rebond 83% (17/22)
      · −4.0% : fill 24% (16/60) · rebond 78% (12/16)
      · −5.0% : fill 18% (11/60) · rebond 55% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 64% si les 15 1res min sont vertes (78 cas) · 38% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 16% si rouge (base 52% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **91%** · continue >prix actuel 54% ; creux résiduel méd -2.48% (q20 -3.58%) → **SL/trailing à −3.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +4.34% → **scale +2.95% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.81%** (au-delà de la MAE q10 -5.81%), cible rebond +2.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.71% .. +5.38%] · haut q95 +8.05% · bas q05 -6.98%
   - 60min (n=160) : retour [-6.09% .. +7.16%] · haut q95 +9.53% · bas q05 -7.29%
   - 2h (n=160) : retour [-7.53% .. +8.43%] · haut q95 +9.77% · bas q05 -8.29%
   - 4h (n=160) : retour [-8.76% .. +6.55%] · haut q95 +9.87% · bas q05 -10.48%
   - 6h (n=160) : retour [-8.81% .. +8.51%] · haut q95 +10.55% · bas q05 -10.48%
   - session (n=160) : retour [-7.98% .. +9.86%] · haut q95 +10.98% · bas q05 -10.48%


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.2  _(survente)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.417  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 32.8%
- **ATR** : 1.61 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.218  _(distribution)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 19.57 · MA50 20.15 · MA200 23.8  _(prix < MA20)_
- **Dist MA** : MA20 -13.6% · MA50 -16.0% · MA200 -28.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88448 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
