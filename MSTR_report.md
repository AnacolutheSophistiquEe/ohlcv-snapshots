# MSTR

**Generated** : 2026-07-23T21:56:06.325546+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $93.63  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot $93.63 (+2.2% vs entrée) · entrée $91.64 · stop $88.61 · T1 $97.71 · R/R 2.0  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.154 _(réel 5 s)_ (GBM -0.188) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $90.43–$92.86 (mid $91.64)
- Spot actuel : $93.63 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $88.61 (stop swing_plan-based (-5.36%))
- Targets : T1 $97.71 · R/R 2.0 | T2 $103.78 · R/R 4.01 | T3 $109.85 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $88.61


## Edge, scénarios & sizing

- EV/risk : -0.188 | EV/share : $-0.572 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 10 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 32.0 | bear 40.6 | side 27.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.964% → cible +2.962% / stop −3.5%, p_fill 86%, n_eff≈37.3) : P(cible|rempli) **49%** · **EV/risk +0.092** (×p_fill ; si rempli +0.37% du capital)
  - **swing** (entrée dip −2.119% → cible +6.623% / stop −3.312%, p_fill 74%, n_eff≈32.7) : P(cible|rempli) **29%** · **EV/risk -0.154** (×p_fill ; si rempli -0.69% du capital)
  - **deep** (entrée dip −3.28% → cible +9.367% / stop −4.683%, p_fill 78%, n_eff≈30.0) : P(cible|rempli) **28%** · **EV/risk -0.213** (×p_fill ; si rempli -1.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→61% · +3.0%→40% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.48% (p90 9.85%) · excursion haute méd. +2.63% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.419% vs midi 1.25% vs clôture 1.318% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.101 ; neutre — autocorr -0.019)_ ; drift intra méd. -0.248% ; recovery-V 39%
- **σ réalisé intraday** 3.999% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 62% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 100.0662 (VA 99.4188–100.3438 ; dernier close 99.93)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 68% · **stop −5.19%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 53% (gap-down >1% 40% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.09%) · haut méd +0.78% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −2.87%) · haut méd +1.07% · range méd 2.48%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.46%) · haut méd +1.37% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −4.23%) · haut méd +1.67% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 99.93 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (125/159) · gap 47% · délai 0.0min · rebond 51% (61/125) (MFE +1.32%)
   - −1.0% : fill 30min 63% · séance 73% (119/159) · gap 40% · délai 0.0min · rebond 57% (67/119) (MFE +1.24%)
   - −1.5% : fill 30min 56% · séance 67% (110/159) · gap 32% · délai 0.0min · rebond 55% (64/110) (MFE +1.45%)
   - −2.0% : fill 30min 48% · séance 61% (99/159) · gap 25% · délai 0.2min · rebond 61% (63/99) (MFE +1.32%)
   - −3.0% : fill 30min 35% · séance 53% (77/159) · gap 18% · délai 3.9min · rebond 60% (46/77) (MFE +1.56%)
   - −4.0% : fill 30min 23% · séance 43% (63/159) · gap 7% · délai 17.0min · rebond 61% (37/63) (MFE +1.65%)
   - −5.0% : fill 30min 16% · séance 29% (45/159) · gap 5% · délai 24.3min · rebond 68% (31/45) (MFE +1.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.28%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.82%) → stop au-delà de −2.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.15% (p90 −2.79%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=963 jambes) : jambe baissière méd −1.2% (p90 −2.8%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 49% (36/72)
      · −2.0% : fill 92% (65/73) · rebond 58% (38/65)
      · −3.0% : fill 84% (57/73) · rebond 61% (34/57)
      · −4.0% : fill 69% (47/73) · rebond 65% (30/47)
      · −5.0% : fill 48% (35/73) · rebond 70% (25/35)
   - **flat** (18 séances) :
      · −1.0% : fill 90% (17/18) · rebond 84% (11/17)
      · −2.0% : fill 59% (13/18) · rebond 65% (9/13)
      · −3.0% : fill 45% (9/18) · rebond 55% (5/9)
      · −4.0% : fill 29% (7/18) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/18) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 38% (30/68) · rebond 66% (20/30)
      · −2.0% : fill 26% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 17% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 16% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 51% si les 15 1res min sont vertes (75 cas) · 40% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 73% si début vert vs 15% si rouge (base 45% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **73%** · continue >prix actuel 57% ; creux résiduel méd -1.75% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.13% → **scale +1.96% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **15%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.36%** (au-delà de la MAE q10 -5.36%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.75% .. +3.98%] · haut q95 +4.81% · bas q05 -4.1%
   - 60min (n=160) : retour [-4.9% .. +3.7%] · haut q95 +5.36% · bas q05 -5.17%
   - 2h (n=160) : retour [-4.74% .. +5.59%] · haut q95 +6.5% · bas q05 -5.28%
   - 4h (n=160) : retour [-7.33% .. +7.77%] · haut q95 +8.88% · bas q05 -8.31%
   - 6h (n=160) : retour [-6.6% .. +6.88%] · haut q95 +9.67% · bas q05 -8.32%
   - session (n=160) : retour [-5.87% .. +6.19%] · haut q95 +9.67% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **17%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 6%)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.9  _(momentum baissier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 2.245  _(pas de croisement recent)_
- **BB** : %B 0.45 · largeur 21.8%
- **ATR** : 5.96 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 65.7  _(marche en range (choppy))_
- **MA** : MA20 94.57 · MA50 122.43 · MA200 164.78  _(prix < MA20)_
- **Dist MA** : MA20 -1.0% · MA50 -23.5% · MA200 -43.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89882 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
