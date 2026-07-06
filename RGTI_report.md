# RGTI

**Generated** : 2026-07-06T21:53:26.360606+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.96  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.96 (+2.5% vs entrée) · entrée $17.53 · stop $17.00 · T1 $18.12 · R/R 1.11  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.248 _(réel 5 s)_ (GBM 0.078) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.03% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.41–$17.65 (mid $17.53)
- Spot actuel : $17.96 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $17.00 (stop swing_plan-based (-8.84%))
- Targets : T1 $18.12 · R/R 1.11 | T2 $18.71 · R/R 2.23 | T3 $19.30 · R/R 3.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.00


## Edge, scénarios & sizing

- EV/risk : 0.078 | EV/share : $0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.109 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.6 | bear 72.6 | side 8.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.396% → cible +3.372% / stop −3.027%, p_fill 65%, n_eff≈25.4) : P(cible|rempli) **25%** · **EV/risk -0.248** (×p_fill ; si rempli -1.15% du capital)
  - **swing** (entrée dip −5.269% → cible +7.54% / stop −3.77%, p_fill 58%, n_eff≈23.1) : P(cible|rempli) **31%** · **EV/risk -0.073** (×p_fill ; si rempli -0.48% du capital)
  - **deep** (entrée dip −8.153% → cible +10.663% / stop −5.332%, p_fill 50%, n_eff≈18.1) : P(cible|rempli) **19%** · **EV/risk -0.205** (×p_fill ; si rempli -2.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→54% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.21% (p90 13.36%) · excursion haute méd. +3.37% / basse méd. −3.0%
- Profil de vol intra : ouverture 5.156% vs midi 1.685% vs clôture 1.948% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 47%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; momentum — autocorr 0.051)_ ; drift intra méd. -0.052% ; recovery-V 48%
- **σ réalisé intraday** 5.63% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 51% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 17.8415 (VA 17.6295–18.3185 ; dernier close 17.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 65% · rebond 79% · **stop −7.38%** sous le fill (sous le bruit) · cible +2.74% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.57% · baisse 57% (gap-down >1% 45% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.42% (p90 −2.97%) · haut méd +1.04% · range méd 2.62%
- Excursion ouverture 15min (n=160) : bas méd −1.55% (p90 −4.51%) · haut méd +1.54% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.05%) · haut méd +1.96% · range méd 4.67%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −6.5%) · haut méd +2.4% · range méd 5.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 86% (137/159) · gap 52% · délai 0.0min · rebond 70% (92/137) (MFE +2.41%)
   - −1.0% : fill 30min 70% · séance 83% (133/159) · gap 45% · délai 0.0min · rebond 70% (89/133) (MFE +2.06%)
   - −1.5% : fill 30min 66% · séance 79% (125/159) · gap 38% · délai 0.0min · rebond 68% (84/125) (MFE +2.53%)
   - −2.0% : fill 30min 60% · séance 73% (115/159) · gap 29% · délai 0.0min · rebond 67% (76/115) (MFE +2.72%)
   - −3.0% : fill 30min 53% · séance 65% (99/159) · gap 13% · délai 1.4min · rebond 79% (74/99) (MFE +2.74%)
   - −4.0% : fill 30min 38% · séance 49% (78/159) · gap 5% · délai 5.4min · rebond 77% (58/78) (MFE +2.5%)
   - −5.0% : fill 30min 25% · séance 43% (66/159) · gap 2% · délai 16.6min · rebond 72% (51/66) (MFE +2.34%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.04% (p90 −3.18%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.31% (p90 −4.15%) → stop au-delà de −2.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.31% (p90 −4.26%) → stop au-delà de −2.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1187 jambes) : jambe baissière méd −1.34% (p90 −3.44%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 65% (50/82)
      · −2.0% : fill 92% (78/83) · rebond 68% (53/78)
      · −3.0% : fill 88% (71/83) · rebond 78% (53/71)
      · −4.0% : fill 67% (57/83) · rebond 77% (43/57)
      · −5.0% : fill 58% (50/83) · rebond 74% (41/50)
   - **flat** (15 séances) :
      · −1.0% : fill 89% (13/15) · rebond 88% (11/13)
      · −2.0% : fill 62% (10/15) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/15) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 58% (38/61) · rebond 73% (28/38)
      · −2.0% : fill 46% (27/61) · rebond 65% (16/27)
      · −3.0% : fill 36% (23/61) · rebond 83% (18/23)
      · −4.0% : fill 24% (16/61) · rebond 78% (12/16)
      · −5.0% : fill 18% (11/61) · rebond 55% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 62% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 17% si rouge (base 52% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **91%** · continue >prix actuel 57% ; creux résiduel méd -2.3% (q20 -3.25%) → **SL/trailing à −3.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.96% / q75 +4.43% → **scale +2.96% / runner +4.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 55%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.82%** (au-delà de la MAE q10 -5.82%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.89% .. +5.6%] · haut q95 +8.23% · bas q05 -7.05%
   - 60min (n=160) : retour [-5.87% .. +7.16%] · haut q95 +9.64% · bas q05 -7.32%
   - 2h (n=160) : retour [-7.6% .. +8.62%] · haut q95 +9.91% · bas q05 -8.33%
   - 4h (n=160) : retour [-8.86% .. +6.69%] · haut q95 +10.15% · bas q05 -10.49%
   - 6h (n=160) : retour [-8.82% .. +8.57%] · haut q95 +10.8% · bas q05 -10.49%
   - session (n=160) : retour [-8.0% .. +9.93%] · haut q95 +11.23% · bas q05 -10.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.86% / p90 2.67%) · ~4.0 replis/séance, durée méd 36.72 min. P(nouveau plus-haut après repli) :
   - −0.5% → **93%** (reprise méd 13.54 min, n=48)
   - −1.0% → **90%** (reprise méd 30.0 min, n=29)
   - −1.5% → **82%** (reprise méd 45.0 min, n=13)
   - −2.0% → **70%** (reprise méd 125.91 min, n=9)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.86%) ; extension open→close méd +8.41% (q75 +9.94% / q95 +11.6%), MFE méd +9.22% / q90 +12.07%
   - Échelle scale-out : +9.22% (33%) / +10.54% (33%) / +12.07% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **74%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.07% : P(retournement après) 0% (mèche méd 0.62%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.98%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.2  _(momentum baissier)_
- **ADX** : 15.8  _(pas de tendance nette)_
- **MACD** : hist -0.372  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 27.1%
- **ATR** : 1.77 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.248  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 53.6  _(transition)_
- **MA** : MA20 20.02 · MA50 20.15 · MA200 23.87  _(prix < MA20)_
- **Dist MA** : MA20 -10.3% · MA50 -10.9% · MA200 -24.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89200 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
