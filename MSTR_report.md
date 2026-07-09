# MSTR

**Generated** : 2026-07-09T00:16:12.177764+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $93.87  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $93.87 (+3.3% vs entrée) · entrée $90.86 · stop $83.59 · T1 $93.93 · R/R 0.42  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.037 _(réel 5 s)_ (GBM -0.079) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -57 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.280 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $90.24–$91.47 (mid $90.86)
- Spot actuel : $93.87 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : $83.59 (stop swing_plan-based (-10.58%))
- Targets : T1 $93.93 · R/R 0.42 | T2 $97.00 · R/R 0.84 | T3 $100.08 · R/R 1.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $83.59


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : $-0.574 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.12 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.0 | bear 80.7 | side 11.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.207% → cible +3.384% / stop −8.0%, p_fill 45%, n_eff≈17.5) : P(cible|rempli) **29%** · **EV/risk -0.037** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −7.064% → cible +7.567% / stop −3.783%, p_fill 43%, n_eff≈15.5) : P(cible|rempli) **35%** · **EV/risk +0.036** (×p_fill ; si rempli +0.32% du capital)
  - **deep** (entrée dip −10.924% → cible +10.701% / stop −5.35%, p_fill 46%, n_eff≈13.7) : P(cible|rempli) **5%** · **EV/risk -0.359** (×p_fill ; si rempli -4.16% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→55% · +3.0%→36% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.34% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.381% vs midi 1.26% vs clôture 1.287% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.656% ; recovery-V 41%
- **σ réalisé intraday** 4.345% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 67% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 97.8892 (VA 97.3987–100.9958 ; dernier close 97.36)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 67% · **stop −5.27%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.28 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 55% (gap-down >1% 39% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.03% (p90 −2.28%) · haut méd +0.66% · range méd 1.89%
- Excursion ouverture 15min (n=160) : bas méd −1.27% (p90 −3.02%) · haut méd +1.05% · range méd 2.59%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.63%) · haut méd +1.26% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −4.78%) · haut méd +1.57% · range méd 3.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (126/159) · gap 48% · délai 0.0min · rebond 52% (63/126) (MFE +1.32%)
   - −1.0% : fill 30min 65% · séance 76% (120/159) · gap 39% · délai 0.0min · rebond 57% (68/120) (MFE +1.47%)
   - −1.5% : fill 30min 58% · séance 72% (113/159) · gap 29% · délai 0.0min · rebond 57% (68/113) (MFE +1.52%)
   - −2.0% : fill 30min 49% · séance 65% (101/159) · gap 25% · délai 0.2min · rebond 58% (65/101) (MFE +1.36%)
   - −3.0% : fill 30min 35% · séance 54% (78/159) · gap 16% · délai 5.7min · rebond 56% (47/78) (MFE +1.52%)
   - −4.0% : fill 30min 22% · séance 44% (62/159) · gap 8% · délai 29.6min · rebond 55% (36/62) (MFE +1.08%)
   - −5.0% : fill 30min 18% · séance 34% (47/159) · gap 6% · délai 27.3min · rebond 67% (33/47) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.68%) → stop au-delà de −1.88% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.18% (p90 −2.86%) → stop au-delà de −2.32% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.36% (p90 −3.07%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=959 jambes) : jambe baissière méd −1.23% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 50% (37/73)
      · −2.0% : fill 90% (66/74) · rebond 53% (39/66)
      · −3.0% : fill 81% (57/74) · rebond 56% (34/57)
      · −4.0% : fill 66% (46/74) · rebond 56% (29/46)
      · −5.0% : fill 55% (37/74) · rebond 68% (27/37)
   - **flat** (18 séances) :
      · −1.0% : fill 88% (17/18) · rebond 82% (11/17)
      · −2.0% : fill 70% (14/18) · rebond 66% (10/14)
      · −3.0% : fill 54% (10/18) · rebond 56% (6/10)
      · −4.0% : fill 34% (7/18) · rebond 12% (2/7)
      · −5.0% : fill 26% (5/18) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (30/67) · rebond 62% (20/30)
      · −2.0% : fill 33% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 22% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 19% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 10% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 52% si les 15 1res min sont vertes (75 cas) · 39% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 45% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 210min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **73%** · continue >prix actuel 53% ; creux résiduel méd -2.31% (q20 -4.04%) → **SL/trailing à −4.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +3.39% → **scale +2.11% / runner +3.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.57%** (au-delà de la MAE q10 -5.57%), cible rebond +2.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.17%] · haut q95 +5.5% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.02% .. +4.68%] · haut q95 +5.68% · bas q05 -5.47%
   - 2h (n=160) : retour [-4.74% .. +5.7%] · haut q95 +6.92% · bas q05 -5.49%
   - 4h (n=160) : retour [-7.33% .. +8.1%] · haut q95 +9.27% · bas q05 -8.32%
   - 6h (n=160) : retour [-7.1% .. +6.97%] · haut q95 +10.1% · bas q05 -8.32%
   - session (n=160) : retour [-5.91% .. +6.38%] · haut q95 +10.1% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 31.3  _(momentum baissier)_
- **ADX** : 28.0  _(tendance etablie)_
- **MACD** : hist 1.411  _(bullish_recent)_
- **BB** : %B 0.31 · largeur 54.6%
- **ATR** : 9.39 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.279  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 41.8  _(transition)_
- **MA** : MA20 105.02 · MA50 140.4 · MA200 177.65  _(prix < MA20)_
- **Dist MA** : MA20 -10.6% · MA50 -33.1% · MA200 -47.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90129 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
