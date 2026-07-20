# SOI

**Generated** : 2026-07-20T00:09:27.825688+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €87.34  

> 🟡 **WAIT-FOR-DIP** — spot +6.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €87.34 (+6.8% vs entrée) · entrée €81.80 · stop €79.12 · T1 €84.77 · R/R 1.11  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.025 · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.27% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -428 % hors [0,100] (R² max 0.63). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €81.20–€82.39 (mid €81.80)
- Spot actuel : €87.34 (+6.8% au-dessus de la zone — repli à attendre)
- Stop : €79.12 (stop swing_plan-based (-17.46%))
- Targets : T1 €84.77 · R/R 1.11 | T2 €87.74 · R/R 2.22 | T3 €90.71 · R/R 3.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €79.12


## Edge, scénarios & sizing

- EV/risk : 0.025 | EV/share : €0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.0 | bear 39.4 | side 52.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 87.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.346% → cible +3.633% / stop −3.272%, p_fill 29%, n_eff≈11.7) : P(cible|rempli) **12%** · **EV/risk -0.112** (×p_fill ; si rempli -1.25% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→68% · +3.0%→56% · +5.0%→42% · +8.0%→21%
- Range intraday médian 9.09% (p90 17.62%) · excursion haute méd. +3.52% / basse méd. −3.47%
- Profil de vol intra : ouverture 5.776% vs midi 1.717% vs clôture 2.563% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. -0.744% ; recovery-V 40%
- **σ réalisé intraday** 5.574% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 67% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 84.4035 (VA 83.6085–85.3575 ; dernier close 87.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 78% · **stop −7.28%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.38 (high win-rate)
- Gaps overnight (n=134) : méd. 0.08% · baisse 48% (gap-down >1% 33% · >2% 24%)
- Excursion ouverture 5min (n=135) : bas méd −1.24% (p90 −3.56%) · haut méd +1.11% · range méd 3.18%
- Excursion ouverture 15min (n=135) : bas méd −1.53% (p90 −4.95%) · haut méd +1.39% · range méd 4.05%
- Excursion ouverture 30min (n=135) : bas méd −1.71% (p90 −5.49%) · haut méd +1.96% · range méd 4.42%
- Excursion ouverture 60min (n=135) : bas méd −1.91% (p90 −5.88%) · haut méd +1.97% · range méd 4.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 87.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (106/134) · gap 41% · délai 0.0min · rebond 62% (68/106) (MFE +1.93%)
   - −1.0% : fill 30min 62% · séance 76% (101/134) · gap 33% · délai 0.2min · rebond 68% (72/101) (MFE +1.8%)
   - −1.5% : fill 30min 58% · séance 72% (92/134) · gap 30% · délai 0.1min · rebond 72% (67/92) (MFE +2.14%)
   - −2.0% : fill 30min 53% · séance 66% (85/134) · gap 24% · délai 0.2min · rebond 76% (67/85) (MFE +2.65%)
   - −3.0% : fill 30min 40% · séance 57% (70/134) · gap 18% · délai 0.8min · rebond 73% (55/70) (MFE +2.72%)
   - −4.0% : fill 30min 32% · séance 47% (56/134) · gap 8% · délai 2.1min · rebond 72% (44/56) (MFE +2.23%)
   - −5.0% : fill 30min 25% · séance 44% (49/134) · gap 2% · délai 14.4min · rebond 78% (41/49) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −3.79%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −3.31%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.21%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1183 jambes) : jambe baissière méd −1.34% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 97% (52/53) · rebond 58% (32/52)
      · −2.0% : fill 93% (50/53) · rebond 72% (39/50)
      · −3.0% : fill 83% (42/53) · rebond 74% (34/42)
      · −4.0% : fill 74% (37/53) · rebond 77% (30/37)
      · −5.0% : fill 70% (33/53) · rebond 85% (28/33)
   - **flat** (16 séances) :
      · −1.0% : fill 100% (16/16) · rebond 76% (13/16)
      · −2.0% : fill 96% (14/16) · rebond 80% (11/14)
      · −3.0% : fill 64% (10/16) · rebond 59% (7/10)
      · −4.0% : fill 50% (7/16) · rebond 54% (5/7)
      · −5.0% : fill 50% (7/16) · rebond 70% (6/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 48% (33/65) · rebond 84% (27/33)
      · −2.0% : fill 33% (21/65) · rebond 82% (17/21)
      · −3.0% : fill 29% (18/65) · rebond 80% (14/18)
      · −4.0% : fill 20% (12/65) · rebond 68% (9/12)
      · −5.0% : fill 18% (9/65) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 52% en base · 70% si les 15 1res min sont vertes (62 cas) · 34% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=135) : COUDE à **36min** → P(séance verte=clôture>ouverture) 78% si début vert vs 26% si rouge (base 52% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **78%** · continue >prix actuel 57% ; creux résiduel méd -2.59% (q20 -5.61%) → **SL/trailing à −5.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.46% / q75 +5.79% → **scale +2.46% / runner +5.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **26%** (continue à baisser 64%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.84%** (au-delà de la MAE q10 -8.84%), cible rebond +2.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-5.35% .. +6.87%] · haut q95 +7.24% · bas q05 -6.41%
   - 60min (n=135) : retour [-6.15% .. +7.55%] · haut q95 +8.85% · bas q05 -6.79%
   - 2h (n=135) : retour [-6.89% .. +10.22%] · haut q95 +12.14% · bas q05 -8.24%
   - 4h (n=135) : retour [-7.23% .. +11.69%] · haut q95 +13.5% · bas q05 -8.57%
   - 6h (n=135) : retour [-8.76% .. +12.21%] · haut q95 +14.34% · bas q05 -10.54%
   - session (n=135) : retour [-12.18% .. +13.93%] · haut q95 +16.6% · bas q05 -13.98%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.9% des séances sont trend-up (mild 0% / strong 5.9%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.19% (p75 2.41% / p90 3.18%) · ~5.56 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **91%** (reprise méd 20.0 min, n=51)
   - −1.0% → **89%** (reprise méd 25.0 min, n=30)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.41%) ; extension open→close méd +13.56% (q75 +14.42% / q95 +17.52%), MFE méd +14.58% / q90 +18.51%
   - Échelle scale-out : +14.58% (33%) / +17.98% (33%) / +18.51% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.51% : P(retournement après) 0% (mèche méd 1.28%)
- **CONTEXTE** : la dernière heure tient les gains 91% du temps (retour médian dernière heure +3.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.2  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -1.174  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 41.5%
- **ATR** : 8.92 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.12  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 40.6  _(transition)_
- **MA** : MA20 107.69 · MA50 133.05 · MA200 68.01  _(prix < MA20)_
- **Dist MA** : MA20 -18.9% · MA50 -34.4% · MA200 +28.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98183 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
