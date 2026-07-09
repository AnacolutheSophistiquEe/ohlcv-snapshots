# HOOD

**Generated** : 2026-07-09T00:25:50.584679+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $113.53  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $113.53 (+8.7% vs entrée) · entrée $104.44 · stop $101.74 · T1 $109.84 · R/R 2.0  
> ↳ P(T1 av. stop) 32 % · EV/risk -0.021 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $103.36–$105.52 (mid $104.44)
- Spot actuel : $113.53 (+8.7% au-dessus de la zone — repli à attendre)
- Stop : $101.74 (stop swing_plan-based (-10.38%))
- Targets : T1 $109.84 · R/R 2.0 | T2 $115.23 · R/R 4.0 | T3 $120.63 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $101.74


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : $-0.056 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 16 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 36.0 | bear 14.0 | side 50.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 568.0 (= 5 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.639% → cible +2.311% / stop −3.0%, p_fill 26%, n_eff≈12.8) : P(cible|rempli) **50%** · **EV/risk +0.041** (×p_fill ; si rempli +0.47% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→54% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.01% (p90 8.79%) · excursion haute méd. +2.11% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.422% vs midi 1.07% vs clôture 1.048% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑1%/↓0% ; spike-down 64% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; momentum — autocorr 0.035)_ ; drift intra méd. 0.862% ; recovery-V 33%
- **σ réalisé intraday** 3.791% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 48% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 115.2301 (VA 113.5369–115.3604 ; dernier close 112.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 85% · **stop −4.76%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.86%) · haut méd +0.94% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.05% (p90 −2.89%) · haut méd +1.05% · range méd 2.54%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.55%) · haut méd +1.61% · range méd 3.26%
- Excursion ouverture 60min (n=160) : bas méd −1.56% (p90 −3.84%) · haut méd +1.71% · range méd 3.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 76% (121/159) · gap 40% · délai 0.0min · rebond 56% (61/121) (MFE +1.39%)
   - −1.0% : fill 30min 56% · séance 64% (106/159) · gap 32% · délai 0.0min · rebond 61% (60/106) (MFE +1.28%)
   - −1.5% : fill 30min 47% · séance 60% (98/159) · gap 23% · délai 0.2min · rebond 55% (53/98) (MFE +1.37%)
   - −2.0% : fill 30min 40% · séance 54% (88/159) · gap 16% · délai 0.6min · rebond 64% (52/88) (MFE +1.31%)
   - −3.0% : fill 30min 29% · séance 40% (66/159) · gap 8% · délai 10.8min · rebond 67% (42/66) (MFE +1.74%)
   - −4.0% : fill 30min 19% · séance 32% (51/159) · gap 4% · délai 15.4min · rebond 76% (33/51) (MFE +2.06%)
   - −5.0% : fill 30min 11% · séance 19% (32/159) · gap 2% · délai 21.5min · rebond 85% (26/32) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.54%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.46%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.43%) → stop au-delà de −1.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=749 jambes) : jambe baissière méd −1.16% (p90 −2.71%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 95% (67/71) · rebond 56% (35/67)
      · −2.0% : fill 82% (57/71) · rebond 59% (32/57)
      · −3.0% : fill 69% (46/71) · rebond 63% (28/46)
      · −4.0% : fill 58% (38/71) · rebond 80% (27/38)
      · −5.0% : fill 38% (27/71) · rebond 84% (22/27)
   - **flat** (23 séances) :
      · −1.0% : fill 70% (17/23) · rebond 76% (12/17)
      · −2.0% : fill 54% (12/23) · rebond 59% (7/12)
      · −3.0% : fill 18% (6/23) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/23) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/23) · rebond 82% (2/3)
   - **gap-up** (65 séances) :
      · −1.0% : fill 32% (22/65) · rebond 64% (13/22)
      · −2.0% : fill 26% (19/65) · rebond 82% (13/19)
      · −3.0% : fill 20% (14/65) · rebond 95% (12/14)
      · −4.0% : fill 11% (8/65) · rebond 81% (5/8)
      · −5.0% : fill 4% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (73 cas) · 38% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 84% si début vert vs 18% si rouge (base 51% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -1.26% (q20 -2.85%) → **SL/trailing à −2.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +3.47% → **scale +1.0% / runner +3.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **18%** (continue à baisser 61%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.05%** (au-delà de la MAE q10 -4.05%), cible rebond +1.58% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +4.82%] · haut q95 +5.26% · bas q05 -4.32%
   - 60min (n=160) : retour [-3.46% .. +4.93%] · haut q95 +6.38% · bas q05 -4.71%
   - 2h (n=160) : retour [-4.06% .. +6.61%] · haut q95 +7.62% · bas q05 -5.4%
   - 4h (n=160) : retour [-4.62% .. +7.6%] · haut q95 +8.55% · bas q05 -6.09%
   - 6h (n=160) : retour [-5.2% .. +7.47%] · haut q95 +8.55% · bas q05 -6.29%
   - session (n=160) : retour [-5.0% .. +7.58%] · haut q95 +8.76% · bas q05 -6.62%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 10.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **44%**. Lecture précoce 30 min : signature présente → 24% vs absente 5% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.11%) · ~4.0 replis/séance, durée méd 37.3 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.11%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.07% (q75 +9.68% / q95 +13.38%), MFE méd +6.49% / q90 +14.82%
   - Échelle scale-out : +6.49% (33%) / +11.14% (33%) / +14.82% (34%)
- **DÉSARMER** : repli > **−2.11%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=3) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.82% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.4  _(momentum haussier)_
- **ADX** : 28.2  _(tendance etablie)_
- **MACD** : hist 1.009  _(pas de croisement recent)_
- **BB** : %B 0.83 · largeur 36.3%
- **ATR** : 7.15 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.011  _(neutre)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 49.3  _(transition)_
- **MA** : MA20 101.48 · MA50 88.33 · MA200 102.31  _(prix > MA20)_
- **Dist MA** : MA20 +11.9% · MA50 +28.5% · MA200 +11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92437 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
