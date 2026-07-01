# RGTI

**Generated** : 2026-07-01T21:55:33.513025+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $18.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $18.68 (+3.4% vs entrée) · entrée $18.07 · stop $17.52 · T1 $18.71 · R/R 1.16  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.125 _(réel 5 s)_ (GBM 0.053) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.01% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.94–$18.20 (mid $18.07)
- Spot actuel : $18.68 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $17.52 (stop swing_plan-based (-10.88%))
- Targets : T1 $18.71 · R/R 1.16 | T2 $19.36 · R/R 2.35 | T3 $20.00 · R/R 3.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.52


## Edge, scénarios & sizing

- EV/risk : 0.053 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.2 | bear 72.8 | side 9.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.264% → cible +3.557% / stop −3.014%, p_fill 45%, n_eff≈20.0) : P(cible|rempli) **28%** · **EV/risk -0.125** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −7.189% → cible +7.954% / stop −3.977%, p_fill 41%, n_eff≈15.0) : P(cible|rempli) **20%** · **EV/risk -0.140** (×p_fill ; si rempli -1.35% du capital)
  - **deep** (entrée dip −11.11% → cible +11.249% / stop −5.624%, p_fill 39%, n_eff≈13.4) : P(cible|rempli) **50%** · **EV/risk +0.173** (×p_fill ; si rempli +2.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→52% · +5.0%→36% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.31% / basse méd. −3.0%
- Profil de vol intra : ouverture 5.111% vs midi 1.704% vs clôture 1.962% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 50%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; momentum — autocorr 0.061)_ ; drift intra méd. 0.485% ; recovery-V 56%
- **σ réalisé intraday** 5.734% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 44% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 19.2891 (VA 19.1307–19.4701 ; dernier close 19.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 65% · rebond 78% · **stop −7.4%** sous le fill (sous le bruit) · cible +3.41% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.7% · baisse 59% (gap-down >1% 48% · >2% 31%)
- Excursion ouverture 5min (n=160) : bas méd −1.43% (p90 −2.97%) · haut méd +1.02% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −4.57%) · haut méd +1.54% · range méd 3.53%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.23%) · haut méd +1.89% · range méd 4.61%
- Excursion ouverture 60min (n=160) : bas méd −2.36% (p90 −6.54%) · haut méd +2.21% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 19.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 85% (136/159) · gap 53% · délai 0.0min · rebond 68% (90/136) (MFE +2.32%)
   - −1.0% : fill 30min 72% · séance 82% (132/159) · gap 48% · délai 0.0min · rebond 67% (87/132) (MFE +2.2%)
   - −1.5% : fill 30min 67% · séance 78% (124/159) · gap 41% · délai 0.0min · rebond 68% (83/124) (MFE +2.57%)
   - −2.0% : fill 30min 61% · séance 72% (114/159) · gap 31% · délai 0.0min · rebond 67% (76/114) (MFE +2.79%)
   - −3.0% : fill 30min 56% · séance 65% (99/159) · gap 14% · délai 1.2min · rebond 78% (73/99) (MFE +3.41%)
   - −4.0% : fill 30min 40% · séance 50% (79/159) · gap 6% · délai 3.9min · rebond 76% (59/79) (MFE +2.8%)
   - −5.0% : fill 30min 26% · séance 43% (67/159) · gap 2% · délai 15.1min · rebond 71% (51/67) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.05% (p90 −3.58%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.33% (p90 −4.26%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.44% (p90 −4.46%) → stop au-delà de −2.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1190 jambes) : jambe baissière méd −1.31% (p90 −3.37%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 98% (81/82) · rebond 64% (49/81)
      · −2.0% : fill 92% (77/82) · rebond 67% (52/77)
      · −3.0% : fill 88% (70/82) · rebond 77% (52/70)
      · −4.0% : fill 69% (57/82) · rebond 77% (43/57)
      · −5.0% : fill 60% (50/82) · rebond 74% (41/50)
   - **flat** (14 séances) :
      · −1.0% : fill 86% (12/14) · rebond 84% (10/12)
      · −2.0% : fill 53% (9/14) · rebond 89% (7/9)
      · −3.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −4.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −5.0% : fill 30% (4/14) · rebond 77% (2/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 56% (39/63) · rebond 71% (28/39)
      · −2.0% : fill 44% (28/63) · rebond 62% (17/28)
      · −3.0% : fill 38% (25/63) · rebond 83% (19/25)
      · −4.0% : fill 26% (18/63) · rebond 78% (14/18)
      · −5.0% : fill 20% (13/63) · rebond 54% (8/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 69% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:06** → P(séance verte=clôture>ouverture) 91% si début vert vs 20% si rouge (base 55% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 108min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **91%** · continue >prix actuel 58% ; creux résiduel méd -2.45% (q20 -3.7%) → **SL/trailing à −3.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.93% / q75 +4.91% → **scale +2.93% / runner +4.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **20%** (continue à baisser 49%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.69%** (au-delà de la MAE q10 -6.69%), cible rebond +2.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-6.16% .. +6.18%] · haut q95 +8.48% · bas q05 -7.12%
   - 60min (n=160) : retour [-6.11% .. +7.45%] · haut q95 +9.82% · bas q05 -7.34%
   - 2h (n=160) : retour [-7.69% .. +9.32%] · haut q95 +10.11% · bas q05 -8.42%
   - 4h (n=160) : retour [-8.95% .. +9.07%] · haut q95 +10.3% · bas q05 -10.51%
   - 6h (n=160) : retour [-8.84% .. +8.63%] · haut q95 +11.14% · bas q05 -10.51%
   - session (n=160) : retour [-8.06% .. +9.98%] · haut q95 +11.45% · bas q05 -10.51%


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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.7  _(neutre)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist -0.371  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 32.2%
- **ATR** : 1.82 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.262  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 20.64 · MA50 20.17 · MA200 23.89  _(prix < MA20)_
- **Dist MA** : MA20 -9.5% · MA50 -7.4% · MA200 -21.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91041 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
