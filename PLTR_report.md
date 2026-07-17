# PLTR

**Generated** : 2026-07-17T22:03:01.283722+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $132.38  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot $132.38 (+12.1% vs entrée) · entrée $118.07 · stop $115.54 · T1 $123.15 · R/R 2.01  
> ↳ P(T1 av. stop) 29 % · EV/risk -0.067 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $117.06–$119.09 (mid $118.07)
- Spot actuel : $132.38 (+12.1% au-dessus de la zone — repli à attendre)
- Stop : $115.54 (stop swing_plan-based (-12.72%))
- Targets : T1 $123.15 · R/R 2.01 | T2 $128.23 · R/R 4.02 | T3 $133.30 · R/R 6.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.54


## Edge, scénarios & sizing

- EV/risk : -0.067 | EV/share : $-0.169 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 15 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.0 | bear 16.4 | side 60.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 132.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→46% · +3.0%→26% · +5.0%→8% · +8.0%→2%
- Range intraday médian 3.94% (p90 7.33%) · excursion haute méd. +1.88% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.975% vs midi 0.742% vs clôture 0.85% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓1% ; spike-down 53% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr 0.025)_ ; drift intra méd. 0.479% ; recovery-V 36%
- **σ réalisé intraday** 2.814% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 51% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 133.725 (VA 132.647–134.341 ; dernier close 134.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 62% · **stop −2.34%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 56% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.96% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.79%) · haut méd +1.18% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.46%) · haut méd +1.32% · range méd 2.87%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.86%) · haut méd +1.52% · range méd 3.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 134.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (118/159) · gap 42% · délai 0.0min · rebond 56% (64/118) (MFE +1.15%)
   - −1.0% : fill 30min 57% · séance 67% (107/159) · gap 32% · délai 0.0min · rebond 59% (61/107) (MFE +1.32%)
   - −1.5% : fill 30min 48% · séance 59% (91/159) · gap 24% · délai 0.2min · rebond 65% (56/91) (MFE +1.37%)
   - −2.0% : fill 30min 40% · séance 51% (75/159) · gap 17% · délai 1.9min · rebond 61% (46/75) (MFE +1.38%)
   - −3.0% : fill 30min 22% · séance 35% (54/159) · gap 9% · délai 5.9min · rebond 51% (25/54) (MFE +1.0%)
   - −4.0% : fill 30min 16% · séance 25% (40/159) · gap 4% · délai 10.7min · rebond 53% (20/40) (MFE +1.07%)
   - −5.0% : fill 30min 12% · séance 20% (28/159) · gap 2% · délai 25.4min · rebond 62% (15/28) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.99%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.12%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.49%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.06% (p90 −2.53%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 94% (66/70) · rebond 64% (40/66)
      · −2.0% : fill 79% (54/70) · rebond 59% (35/54)
      · −3.0% : fill 59% (39/70) · rebond 47% (19/39)
      · −4.0% : fill 45% (30/70) · rebond 52% (15/30)
      · −5.0% : fill 39% (23/70) · rebond 64% (13/23)
   - **flat** (30 séances) :
      · −1.0% : fill 75% (24/30) · rebond 40% (12/24)
      · −2.0% : fill 50% (12/30) · rebond 70% (7/12)
      · −3.0% : fill 39% (10/30) · rebond 75% (5/10)
      · −4.0% : fill 20% (7/30) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/30) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/59) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 69% si les 15 1res min sont vertes (81 cas) · 38% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **42min** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 54% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -1.28% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.16% → **scale +1.18% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **24%** (continue à baisser 48%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.84% .. +3.68%] · haut q95 +3.96% · bas q05 -4.02%
   - 60min (n=160) : retour [-3.59% .. +3.88%] · haut q95 +4.65% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.86% .. +4.87%] · haut q95 +4.86% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.37% .. +5.63%] · haut q95 +6.06% · bas q05 -5.18%
   - 6h (n=160) : retour [-4.97% .. +5.31%] · haut q95 +6.78% · bas q05 -5.57%
   - session (n=160) : retour [-4.75% .. +4.7%] · haut q95 +6.78% · bas q05 -5.58%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 75.1  _(surachat)_
- **ADX** : 13.4  _(pas de tendance nette)_
- **MACD** : hist 1.526  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 27.6%
- **ATR** : 7.17 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.016  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 125.25 · MA50 132.48 · MA200 155.64  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 -0.1% · MA200 -14.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90619 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
