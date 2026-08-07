# IONQ

**Generated** : 2026-08-07T22:03:31.954517+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $44.43  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $44.43 (+1.0% vs entrée) · entrée $43.98 · stop $43.10 · T1 $45.46 · R/R 1.68  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM 0.092) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $43.68–$44.27 (mid $43.98)
- Spot actuel : $44.43 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $43.10 (stop swing_plan-based (-8.82%))
- Targets : T1 $45.46 · R/R 1.68 | T2 $46.93 · R/R 3.35 | T3 $48.41 · R/R 5.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $43.10


## Edge, scénarios & sizing

- EV/risk : 0.092 | EV/share : $0.081 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.105 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.3 | bear 17.7 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 400.0 (= 9 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.012% → cible +3.357% / stop −1.998%, p_fill 80%, n_eff≈34.4) : P(cible|rempli) **25%** · **EV/risk -0.079** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −2.229% → cible +7.508% / stop −6.741%, p_fill 87%, n_eff≈35.5) : P(cible|rempli) **48%** · **EV/risk +0.032** (×p_fill ; si rempli +0.24% du capital)
  - **deep** (entrée dip −3.443% → cible +10.618% / stop −10.24%, p_fill 94%, n_eff≈36.3) : P(cible|rempli) **38%** · **EV/risk -0.223** (×p_fill ; si rempli -2.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→61% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.64% (p90 12.22%) · excursion haute méd. +3.69% / basse méd. −3.16%
- Profil de vol intra : ouverture 5.183% vs midi 1.51% vs clôture 1.708% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.007)_ ; drift intra méd. -0.423% ; recovery-V 23%
- **σ réalisé intraday** 4.835% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 67% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 40.2839 (VA 40.0669–40.8264 ; dernier close 39.67)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 54% (gap-down >1% 39% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.84%) · haut méd +1.2% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.65% (p90 −4.14%) · haut méd +1.35% · range méd 3.7%
- Excursion ouverture 30min (n=160) : bas méd −1.89% (p90 −5.23%) · haut méd +1.93% · range méd 4.49%
- Excursion ouverture 60min (n=160) : bas méd −2.27% (p90 −5.9%) · haut méd +2.33% · range méd 5.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.67 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (133/159) · gap 45% · délai 0.0min · rebond 66% (91/133) (MFE +1.88%)
   - −1.0% : fill 30min 68% · séance 76% (125/159) · gap 39% · délai 0.0min · rebond 75% (93/125) (MFE +2.35%)
   - −1.5% : fill 30min 65% · séance 74% (120/159) · gap 33% · délai 0.0min · rebond 68% (83/120) (MFE +2.52%)
   - −2.0% : fill 30min 57% · séance 66% (110/159) · gap 18% · délai 0.2min · rebond 68% (76/110) (MFE +2.54%)
   - −3.0% : fill 30min 46% · séance 56% (91/159) · gap 9% · délai 7.0min · rebond 73% (67/91) (MFE +2.77%)
   - −4.0% : fill 30min 30% · séance 44% (72/159) · gap 5% · délai 15.4min · rebond 74% (55/72) (MFE +2.39%)
   - −5.0% : fill 30min 18% · séance 36% (61/159) · gap 2% · délai 31.1min · rebond 83% (53/61) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.83% (p90 −2.91%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.14%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −2.85%) → stop au-delà de −2.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1127 jambes) : jambe baissière méd −1.31% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 75% (57/75)
      · −2.0% : fill 96% (71/75) · rebond 73% (54/71)
      · −3.0% : fill 81% (60/75) · rebond 72% (45/60)
      · −4.0% : fill 62% (45/75) · rebond 71% (35/45)
      · −5.0% : fill 52% (38/75) · rebond 77% (31/38)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (37/68) · rebond 71% (27/37)
      · −2.0% : fill 33% (27/68) · rebond 52% (16/27)
      · −3.0% : fill 28% (22/68) · rebond 79% (17/22)
      · −4.0% : fill 23% (19/68) · rebond 79% (16/19)
      · −5.0% : fill 20% (16/68) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 54% si les 15 1res min sont vertes (80 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 77% si début vert vs 17% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -2.22% (q20 -3.52%) → **SL/trailing à −3.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.86% / q75 +2.64% → **scale +1.86% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **17%** (continue à baisser 55%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.06%** (au-delà de la MAE q10 -4.06%), cible rebond +1.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +7.17%] · haut q95 +8.09% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.09% .. +6.59%] · haut q95 +8.99% · bas q05 -6.5%
   - 2h (n=160) : retour [-6.33% .. +8.5%] · haut q95 +10.68% · bas q05 -7.18%
   - 4h (n=160) : retour [-7.23% .. +7.66%] · haut q95 +11.93% · bas q05 -8.18%
   - 6h (n=160) : retour [-7.44% .. +7.74%] · haut q95 +11.95% · bas q05 -8.43%
   - session (n=160) : retour [-7.25% .. +8.36%] · haut q95 +11.95% · bas q05 -8.43%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 2.08% / p90 3.34%) · ~3.45 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=44)
   - −1.0% → **72%** (reprise méd 49.72 min, n=27)
   - −1.5% → **56%** (reprise méd 81.24 min, n=14)
   - −2.0% → **51%** (reprise méd 175.66 min, n=10)
   - −3.0% → **62%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.34%** (p90, défaut prudent ; serré/agressif −2.08%) ; extension open→close méd +7.78% (q75 +8.69% / q95 +17.35%), MFE méd +9.24% / q90 +13.41%
   - Échelle scale-out : +9.24% (33%) / +12.23% (33%) / +13.41% (34%)
- **DÉSARMER** : repli > **−3.34%** depuis le plus-haut = décay → P(retournement) **44%** (préavis méd 168.41 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.41% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 75% du temps (retour médian dernière heure +0.28%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.6  _(momentum haussier)_
- **ADX** : 28.7  _(tendance etablie)_
- **MACD** : hist 1.637  _(pas de croisement recent)_
- **BB** : %B 1.1 · largeur 34.6%
- **ATR** : 2.93 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.182  _(distribution)_
- **Vol ratio** : 1.29  _(volume normal)_
- **Choppiness** : 44.1  _(transition)_
- **MA** : MA20 36.78 · MA50 48.68 · MA200 45.63  _(prix > MA20)_
- **Dist MA** : MA20 +20.8% · MA50 -8.7% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92521 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
