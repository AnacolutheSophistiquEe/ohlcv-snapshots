# SMR

**Generated** : 2026-07-06T21:56:25.236219+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.61  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.61 (+1.7% vs entrée) · entrée $9.45 · stop $9.18 · T1 $9.66 · R/R 0.78  
> ↳ P(T1 av. stop) 47 % _(réel 5 s)_ · EV/risk -0.048 _(réel 5 s)_ (GBM 0.041) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.89% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.41–$9.50 (mid $9.45)
- Spot actuel : $9.61 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $9.18 (stop swing_plan-based (-12.73%))
- Targets : T1 $9.66 · R/R 0.78 | T2 $10.02 · R/R 2.11 | T3 $10.38 · R/R 3.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.18


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : $0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.085 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.5 | bear 52.8 | side 24.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.631% → cible +2.235% / stop −2.886%, p_fill 65%, n_eff≈26.2) : P(cible|rempli) **47%** · **EV/risk -0.048** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −3.58% → cible +18.981% / stop −9.489%, p_fill 65%, n_eff≈26.6) : P(cible|rempli) **9%** · **EV/risk -0.056** (×p_fill ; si rempli -0.81% du capital)
  - **deep** (entrée dip −5.532% → cible +30.525% / stop −15.262%, p_fill 59%, n_eff≈23.4) : P(cible|rempli) **7%** · **EV/risk +0.004** (×p_fill ; si rempli +0.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→54% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.26% (p90 12.61%) · excursion haute méd. +3.23% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.891% vs midi 1.555% vs clôture 1.771% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr 0.021)_ ; drift intra méd. -0.03% ; recovery-V 18%
- **σ réalisé intraday** 5.245% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 48% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 9.7423 (VA 9.6158–10.0586 ; dernier close 9.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 76% · **stop −6.48%** sous le fill (sous le bruit) · cible +2.81% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.75% · baisse 59% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.33% (p90 −3.45%) · haut méd +1.07% · range méd 2.82%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.96%) · haut méd +1.44% · range méd 3.83%
- Excursion ouverture 30min (n=160) : bas méd −1.9% (p90 −5.4%) · haut méd +1.98% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.04%) · haut méd +2.64% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 82% (131/159) · gap 52% · délai 0.0min · rebond 67% (81/131) (MFE +1.75%)
   - −1.0% : fill 30min 68% · séance 79% (126/159) · gap 42% · délai 0.0min · rebond 67% (83/126) (MFE +1.83%)
   - −1.5% : fill 30min 65% · séance 75% (120/159) · gap 38% · délai 0.0min · rebond 75% (87/120) (MFE +2.22%)
   - −2.0% : fill 30min 61% · séance 69% (114/159) · gap 28% · délai 0.2min · rebond 69% (83/114) (MFE +2.72%)
   - −3.0% : fill 30min 49% · séance 62% (102/159) · gap 13% · délai 2.3min · rebond 76% (83/102) (MFE +2.81%)
   - −4.0% : fill 30min 39% · séance 55% (86/159) · gap 6% · délai 9.3min · rebond 73% (66/86) (MFE +2.7%)
   - −5.0% : fill 30min 25% · séance 42% (63/159) · gap 4% · délai 17.5min · rebond 73% (46/63) (MFE +1.97%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.81%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.05% (p90 −3.26%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.71%) → stop au-delà de −2.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1189 jambes) : jambe baissière méd −1.4% (p90 −3.19%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 72% (55/84)
      · −2.0% : fill 92% (80/84) · rebond 76% (60/80)
      · −3.0% : fill 86% (77/84) · rebond 81% (64/77)
      · −4.0% : fill 76% (66/84) · rebond 79% (54/66)
      · −5.0% : fill 58% (47/84) · rebond 81% (37/47)
   - **flat** (14 séances) :
      · −1.0% : fill 76% (11/14) · rebond 42% (7/11)
      · −2.0% : fill 63% (9/14) · rebond 30% (5/9)
      · −3.0% : fill 60% (7/14) · rebond 29% (4/7)
      · −4.0% : fill 60% (7/14) · rebond 40% (3/7)
      · −5.0% : fill 46% (5/14) · rebond 70% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (31/61) · rebond 64% (21/31)
      · −2.0% : fill 38% (25/61) · rebond 63% (18/25)
      · −3.0% : fill 28% (18/61) · rebond 77% (15/18)
      · −4.0% : fill 24% (13/61) · rebond 67% (9/13)
      · −5.0% : fill 18% (11/61) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 58% si les 15 1res min sont vertes (66 cas) · 35% si rouges (94 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 82% si début vert vs 13% si rouge (base 45% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **82%** · continue >prix actuel 49% ; creux résiduel méd -2.31% (q20 -4.04%) → **SL/trailing à −4.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.27% / q75 +4.31% → **scale +2.27% / runner +4.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.28%** (au-delà de la MAE q10 -6.28%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.68% .. +4.91%] · haut q95 +6.59% · bas q05 -6.75%
   - 60min (n=160) : retour [-6.43% .. +5.84%] · haut q95 +8.45% · bas q05 -7.96%
   - 2h (n=160) : retour [-7.94% .. +9.23%] · haut q95 +11.39% · bas q05 -9.13%
   - 4h (n=160) : retour [-8.84% .. +8.43%] · haut q95 +11.39% · bas q05 -10.75%
   - 6h (n=160) : retour [-8.64% .. +8.76%] · haut q95 +11.62% · bas q05 -10.89%
   - session (n=160) : retour [-8.5% .. +10.88%] · haut q95 +11.74% · bas q05 -10.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0.6% / strong 4.4%) · base = 8 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **12%**. Lecture précoce 30 min : signature présente → 10% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.19% (p75 1.56% / p90 2.99%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=44)
   - −1.0% → **81%** (reprise méd 19.98 min, n=26)
   - −1.5% → **72%** (reprise méd 40.32 min, n=11)
   - −2.0% → **89%** (reprise méd 49.41 min, n=8)
   - −3.0% → **100%** (reprise méd 84.35 min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.99%** (p90, défaut prudent ; serré/agressif −1.56%) ; extension open→close méd +11.04% (q75 +11.76% / q95 +11.9%), MFE méd +12.98% / q90 +13.48%
   - Échelle scale-out : +12.98% (33%) / +13.38% (33%) / +13.48% (34%)
- **DÉSARMER** : repli > **−2.99%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.48% : P(retournement après) 0% (mèche méd 2.37%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 47.7  _(neutre)_
- **ADX** : 11.1  _(pas de tendance nette)_
- **MACD** : hist -0.045  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 22.9%
- **ATR** : 0.91 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.213  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 64.9  _(marche en range (choppy))_
- **MA** : MA20 10.25 · MA50 11.34 · MA200 19.42  _(prix < MA20)_
- **Dist MA** : MA20 -6.2% · MA50 -15.3% · MA200 -50.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89553 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
