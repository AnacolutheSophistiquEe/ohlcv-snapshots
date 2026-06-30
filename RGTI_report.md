# RGTI

**Generated** : 2026-06-30T00:18:24.651787+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $19.44  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $19.44 (+2.6% vs entrée) · entrée $18.94 · stop $18.32 · T1 $19.63 · R/R 1.11  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.279 _(réel 5 s)_ (GBM 0.007) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.28% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $18.80–$19.08 (mid $18.94)
- Spot actuel : $19.44 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : $18.32 (stop swing_plan-based (-9.51%))
- Targets : T1 $19.63 · R/R 1.11 | T2 $20.32 · R/R 2.23 | T3 $21.01 · R/R 3.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $18.32


## Edge, scénarios & sizing

- EV/risk : 0.007 | EV/share : $0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.9 | bear 72.8 | side 9.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.581% → cible +3.645% / stop −3.284%, p_fill 56%, n_eff≈23.4) : P(cible|rempli) **19%** · **EV/risk -0.279** (×p_fill ; si rempli -1.64% du capital)
  - **swing** (entrée dip −5.665% → cible +8.151% / stop −4.076%, p_fill 57%, n_eff≈21.5) : P(cible|rempli) **46%** · **EV/risk +0.205** (×p_fill ; si rempli +1.47% du capital)
  - **deep** (entrée dip −8.761% → cible +11.527% / stop −5.764%, p_fill 47%, n_eff≈17.0) : P(cible|rempli) **27%** · **EV/risk -0.089** (×p_fill ; si rempli -1.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→51% · +5.0%→36% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.19% / basse méd. −3.11%
- Profil de vol intra : ouverture 5.069% vs midi 1.702% vs clôture 1.972% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 48%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; momentum — autocorr 0.054)_ ; drift intra méd. 0.268% ; recovery-V 51%
- **σ réalisé intraday** 5.851% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 44% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 18.6241 (VA 18.2573–18.8075 ; dernier close 18.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 66% · rebond 77% · **stop −7.41%** sous le fill (sous le bruit) · cible +2.85% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. -0.69% · baisse 59% (gap-down >1% 47% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.47% (p90 −2.97%) · haut méd +1.02% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −4.57%) · haut méd +1.54% · range méd 3.54%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.33%) · haut méd +1.8% · range méd 4.62%
- Excursion ouverture 60min (n=160) : bas méd −2.36% (p90 −6.57%) · haut méd +2.16% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 80% · séance 86% (137/159) · gap 54% · délai 0.0min · rebond 67% (91/137) (MFE +2.42%)
   - −1.0% : fill 30min 73% · séance 83% (133/159) · gap 47% · délai 0.0min · rebond 67% (88/133) (MFE +2.06%)
   - −1.5% : fill 30min 68% · séance 79% (124/159) · gap 40% · délai 0.0min · rebond 67% (83/124) (MFE +2.54%)
   - −2.0% : fill 30min 62% · séance 72% (113/159) · gap 30% · délai 0.0min · rebond 66% (75/113) (MFE +2.73%)
   - −3.0% : fill 30min 56% · séance 66% (98/159) · gap 14% · délai 1.3min · rebond 77% (72/98) (MFE +2.85%)
   - −4.0% : fill 30min 41% · séance 52% (79/159) · gap 6% · délai 3.9min · rebond 76% (59/79) (MFE +2.8%)
   - −5.0% : fill 30min 27% · séance 45% (67/159) · gap 2% · délai 15.1min · rebond 71% (51/67) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.05% (p90 −3.82%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.44% (p90 −4.3%) → stop au-delà de −2.7% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.52% (p90 −4.55%) → stop au-delà de −2.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1200 jambes) : jambe baissière méd −1.31% (p90 −3.36%) · ~15.6 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 98% (81/82) · rebond 63% (49/81)
      · −2.0% : fill 92% (76/82) · rebond 66% (51/76)
      · −3.0% : fill 87% (69/82) · rebond 76% (51/69)
      · −4.0% : fill 71% (57/82) · rebond 77% (43/57)
      · −5.0% : fill 62% (50/82) · rebond 74% (41/50)
   - **flat** (14 séances) :
      · −1.0% : fill 86% (12/14) · rebond 84% (10/12)
      · −2.0% : fill 53% (9/14) · rebond 89% (7/9)
      · −3.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −4.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −5.0% : fill 30% (4/14) · rebond 77% (2/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 59% (40/63) · rebond 71% (29/40)
      · −2.0% : fill 46% (28/63) · rebond 62% (17/28)
      · −3.0% : fill 40% (25/63) · rebond 83% (19/25)
      · −4.0% : fill 27% (18/63) · rebond 78% (14/18)
      · −5.0% : fill 21% (13/63) · rebond 54% (8/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 67% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 12% si rouge (base 53% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **90%** · continue >prix actuel 56% ; creux résiduel méd -2.31% (q20 -3.32%) → **SL/trailing à −3.32%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.96% / q75 +4.44% → **scale +2.96% / runner +4.44%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.12%** (au-delà de la MAE q10 -6.12%), cible rebond +1.53% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-6.33% .. +6.58%] · haut q95 +8.63% · bas q05 -7.15%
   - 60min (n=160) : retour [-6.14% .. +7.68%] · haut q95 +9.92% · bas q05 -7.34%
   - 2h (n=160) : retour [-7.75% .. +9.46%] · haut q95 +10.23% · bas q05 -8.46%
   - 4h (n=160) : retour [-9.08% .. +9.81%] · haut q95 +10.4% · bas q05 -10.52%
   - 6h (n=160) : retour [-8.85% .. +8.64%] · haut q95 +11.36% · bas q05 -10.52%
   - session (n=160) : retour [-8.08% .. +9.99%] · haut q95 +11.59% · bas q05 -10.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 14% vs absente 2% (base 6%)
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

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -0.446  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 43.0%
- **ATR** : 2.07 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.136  _(distribution)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 60.7  _(transition)_
- **MA** : MA20 21.36 · MA50 20.2 · MA200 23.88  _(prix < MA20)_
- **Dist MA** : MA20 -9.0% · MA50 -3.7% · MA200 -18.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90992 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
