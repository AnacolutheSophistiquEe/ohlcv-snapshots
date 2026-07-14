# MSTR

**Generated** : 2026-07-14T00:22:27.414337+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $92.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $92.10 (+2.9% vs entrée) · entrée $89.53 · stop $82.37 · T1 $92.41 · R/R 0.4  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.037 _(réel 5 s)_ (GBM -0.081) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -69 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $88.95–$90.10 (mid $89.53)
- Spot actuel : $92.10 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $82.37 (stop swing_plan-based (-9.52%))
- Targets : T1 $92.41 · R/R 0.4 | T2 $95.29 · R/R 0.8 | T3 $98.17 · R/R 1.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $82.37


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : $-0.581 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.0 | bear 83.5 | side 10.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.793% → cible +3.218% / stop −8.0%, p_fill 49%, n_eff≈21.6) : P(cible|rempli) **29%** · **EV/risk -0.037** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −6.144% → cible +7.195% / stop −3.597%, p_fill 41%, n_eff≈17.8) : P(cible|rempli) **29%** · **EV/risk -0.048** (×p_fill ; si rempli -0.42% du capital)
  - **deep** (entrée dip −9.496% → cible +10.175% / stop −5.087%, p_fill 53%, n_eff≈18.2) : P(cible|rempli) **21%** · **EV/risk -0.210** (×p_fill ; si rempli -2.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→71% · +2.0%→55% · +3.0%→35% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.36% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.84%
- Profil de vol intra : ouverture 3.392% vs midi 1.261% vs clôture 1.298% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.006)_ ; drift intra méd. -0.775% ; recovery-V 35%
- **σ réalisé intraday** 4.231% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 94.6587 (VA 93.8262–94.9917 ; dernier close 94.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 68% · **stop −5.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 54% (gap-down >1% 39% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.03% (p90 −2.25%) · haut méd +0.62% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.0%) · haut méd +1.07% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.55%) · haut méd +1.32% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.94% (p90 −4.55%) · haut méd +1.52% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (127/159) · gap 47% · délai 0.0min · rebond 53% (64/127) (MFE +1.42%)
   - −1.0% : fill 30min 65% · séance 75% (120/159) · gap 39% · délai 0.0min · rebond 57% (68/120) (MFE +1.47%)
   - −1.5% : fill 30min 57% · séance 70% (112/159) · gap 29% · délai 0.0min · rebond 56% (67/112) (MFE +1.45%)
   - −2.0% : fill 30min 48% · séance 63% (100/159) · gap 25% · délai 0.2min · rebond 56% (64/100) (MFE +1.32%)
   - −3.0% : fill 30min 35% · séance 53% (77/159) · gap 16% · délai 4.0min · rebond 54% (46/77) (MFE +1.49%)
   - −4.0% : fill 30min 23% · séance 44% (62/159) · gap 8% · délai 24.4min · rebond 56% (36/62) (MFE +1.27%)
   - −5.0% : fill 30min 19% · séance 34% (47/159) · gap 6% · délai 24.8min · rebond 68% (33/47) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.52%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.2% (p90 −2.84%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.35% (p90 −3.08%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=965 jambes) : jambe baissière méd −1.21% (p90 −2.84%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 48% (36/72)
      · −2.0% : fill 90% (65/73) · rebond 50% (38/65)
      · −3.0% : fill 81% (56/73) · rebond 54% (33/56)
      · −4.0% : fill 68% (46/73) · rebond 59% (29/46)
      · −5.0% : fill 56% (37/73) · rebond 70% (27/37)
   - **flat** (19 séances) :
      · −1.0% : fill 90% (18/19) · rebond 85% (12/18)
      · −2.0% : fill 60% (14/19) · rebond 66% (10/14)
      · −3.0% : fill 46% (10/19) · rebond 56% (6/10)
      · −4.0% : fill 29% (7/19) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/19) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 41% (30/67) · rebond 62% (20/30)
      · −2.0% : fill 31% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 21% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 18% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 9% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 50% si les 15 1res min sont vertes (76 cas) · 36% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 70% si début vert vs 20% si rouge (base 43% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **70%** · continue >prix actuel 51% ; creux résiduel méd -2.3% (q20 -3.69%) → **SL/trailing à −3.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.34% → **scale +2.14% / runner +3.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 56%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.39%** (au-delà de la MAE q10 -5.39%), cible rebond +1.85% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.07%] · haut q95 +5.39% · bas q05 -4.18%
   - 60min (n=160) : retour [-4.98% .. +4.42%] · haut q95 +5.54% · bas q05 -5.42%
   - 2h (n=160) : retour [-4.74% .. +5.68%] · haut q95 +6.72% · bas q05 -5.44%
   - 4h (n=160) : retour [-7.33% .. +8.08%] · haut q95 +9.2% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.96% .. +6.96%] · haut q95 +10.07% · bas q05 -8.32%
   - session (n=160) : retour [-5.9% .. +6.34%] · haut q95 +10.07% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 9% vs absente 3% (base 6%)
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
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 1.685  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 54.0%
- **ATR** : 8.22 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.291  _(distribution)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 101.42 · MA50 136.15 · MA200 174.01  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -32.4% · MA200 -47.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90245 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
