# 298040

**Generated** : 2026-08-13T21:53:25.175841+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2956000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2956000.00 (+2.5% vs entrée) · entrée ₩2884750.00 · stop ₩2804864.29 · T1 ₩3040348.84 · R/R 1.95  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.192 _(réel 5 s)_ (GBM -0.178) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.77% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.170 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2856227.58–₩2913272.42 (mid ₩2884750.00)
- Spot actuel : ₩2956000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩2804864.29 (stop swing_plan-based (-14.31%))
- Targets : T1 ₩3040348.84 · R/R 1.95 | T2 ₩3175819.34 · R/R 3.64 | T3 ₩3311289.83 · R/R 5.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2804864.29


## Edge, scénarios & sizing

- EV/risk : -0.178 | EV/share : ₩-14184.183 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 23 % | T3 23 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.1 | bear 74.0 | side 16.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.407% → cible +5.394% / stop −2.769%, p_fill 79%, n_eff≈32.4) : P(cible|rempli) **10%** · **EV/risk -0.192** (×p_fill ; si rempli -0.68% du capital)
  - **swing** (entrée dip −5.302% → cible +11.021% / stop −9.513%, p_fill 64%, n_eff≈24.0) : P(cible|rempli) **36%** · **EV/risk -0.025** (×p_fill ; si rempli -0.38% du capital)
  - **deep** (entrée dip −8.195% → cible +42.87% / stop −18.0%, p_fill 68%, n_eff≈24.6) : P(cible|rempli) **7%** · **EV/risk -0.307** (×p_fill ; si rempli -8.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→62% · +2.0%→52% · +3.0%→40% · +5.0%→24% · +8.0%→8%
- Range intraday médian 7.06% (p90 10.6%) · excursion haute méd. +2.14% / basse méd. −4.2%
- Profil de vol intra : ouverture 4.627% vs midi 1.19% vs clôture 1.206% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 26% · trend ↑0%/↓1% ; spike-down 82% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -1.761% ; recovery-V 24%
- **σ réalisé intraday** 5.178% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 64% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 2839875.0 (VA 2836625.0–2865875.0 ; dernier close 2845000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 81% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.38 (high win-rate)
- Gaps overnight (n=151) : méd. 0.89% · baisse 37% (gap-down >1% 25% · >2% 16%)
- Excursion ouverture 5min (n=152) : bas méd −1.47% (p90 −3.54%) · haut méd +0.84% · range méd 2.7%
- Excursion ouverture 15min (n=152) : bas méd −2.08% (p90 −4.44%) · haut méd +1.12% · range méd 3.62%
- Excursion ouverture 30min (n=152) : bas méd −2.52% (p90 −5.08%) · haut méd +1.16% · range méd 4.26%
- Excursion ouverture 60min (n=152) : bas méd −2.69% (p90 −5.35%) · haut méd +1.37% · range méd 4.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2845000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 66% (101/151) · gap 32% · délai 0.0min · rebond 59% (62/101) (MFE +1.27%)
   - −1.0% : fill 30min 55% · séance 64% (93/151) · gap 25% · délai 0.1min · rebond 59% (57/93) (MFE +1.55%)
   - −1.5% : fill 30min 48% · séance 57% (84/151) · gap 21% · délai 1.3min · rebond 52% (50/84) (MFE +1.28%)
   - −2.0% : fill 30min 43% · séance 55% (75/151) · gap 16% · délai 4.1min · rebond 50% (40/75) (MFE +1.01%)
   - −3.0% : fill 30min 33% · séance 47% (62/151) · gap 7% · délai 10.0min · rebond 53% (34/62) (MFE +1.03%)
   - −4.0% : fill 30min 24% · séance 44% (54/151) · gap 5% · délai 25.8min · rebond 68% (39/54) (MFE +1.89%)
   - −5.0% : fill 30min 19% · séance 35% (41/151) · gap 4% · délai 28.7min · rebond 81% (33/41) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.33%) → stop au-delà de −2.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.69%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −3.77%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=827 jambes) : jambe baissière méd −1.43% (p90 −3.56%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 58% (32/52)
      · −2.0% : fill 90% (44/52) · rebond 47% (23/44)
      · −3.0% : fill 87% (42/52) · rebond 54% (23/42)
      · −4.0% : fill 83% (37/52) · rebond 73% (27/37)
      · −5.0% : fill 73% (31/52) · rebond 79% (24/31)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 37% (30/83) · rebond 58% (17/30)
      · −2.0% : fill 30% (23/83) · rebond 53% (12/23)
      · −3.0% : fill 22% (15/83) · rebond 45% (7/15)
      · −4.0% : fill 18% (12/83) · rebond 64% (9/12)
      · −5.0% : fill 11% (7/83) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 34% en base · 56% si les 15 1res min sont vertes (62 cas) · 23% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **32min** → P(séance verte=clôture>ouverture) 73% si début vert vs 14% si rouge (base 34% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **73%** · continue >prix actuel 52% ; creux résiduel méd -2.06% (q20 -4.0%) → **SL/trailing à −4.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.64% / q75 +4.02% → **scale +2.64% / runner +4.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **14%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.43%** (au-delà de la MAE q10 -6.43%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-4.6% .. +4.32%] · haut q95 +6.15% · bas q05 -5.37%
   - 60min (n=152) : retour [-5.48% .. +4.99%] · haut q95 +6.96% · bas q05 -6.08%
   - 2h (n=152) : retour [-7.41% .. +4.58%] · haut q95 +7.42% · bas q05 -8.26%
   - 4h (n=152) : retour [-7.97% .. +5.41%] · haut q95 +8.29% · bas q05 -9.81%
   - 6h (n=152) : retour [-7.61% .. +5.35%] · haut q95 +8.74% · bas q05 -9.7%
   - session (n=152) : retour [-8.07% .. +5.75%] · haut q95 +8.74% · bas q05 -9.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.3% des séances sont trend-up (mild 0% / strong 5.3%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 20% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 55.3  _(momentum haussier)_
- **ADX** : 12.0  _(pas de tendance nette)_
- **MACD** : hist 84457.407  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 45.0%
- **ATR** : 266285.71 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.166  _(distribution)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 42.2  _(transition)_
- **MA** : MA20 2634300.0 · MA50 3046140.0 · MA200 2700779.92  _(prix > MA20)_
- **Dist MA** : MA20 +12.2% · MA50 -3.0% · MA200 +9.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88169 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
