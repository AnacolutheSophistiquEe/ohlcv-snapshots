# CEG

**Generated** : 2026-07-22T00:28:09.541837+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $262.22  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $262.22 (+2.4% vs entrée) · entrée $255.98 · stop $252.14 · T1 $259.23 · R/R 0.85  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk -0.032 _(réel 5 s)_ (GBM -0.049) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $255.33–$256.63 (mid $255.98)
- Spot actuel : $262.22 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $252.14 (stop swing_plan-based (-6.59%))
- Targets : T1 $259.23 · R/R 0.85 | T2 $262.49 · R/R 1.7 | T3 $265.74 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $252.14


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : $-0.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 24 % | T3 8 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.3 | bear 6.9 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.386% → cible +1.272% / stop −1.5%, p_fill 24%, n_eff≈12.8) : P(cible|rempli) **26%** · **EV/risk -0.032** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −5.243% → cible +2.843% / stop −1.422%, p_fill 17%, n_eff≈8.9) : P(cible|rempli) **11%** · **EV/risk -0.121** (×p_fill ; si rempli -1.00% du capital)
  - **deep** (entrée dip −8.092% → cible +4.021% / stop −2.01%, p_fill 25%, n_eff≈10.5) : P(cible|rempli) **12%** · **EV/risk -0.172** (×p_fill ; si rempli -1.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→38% · +3.0%→20% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.4% (p90 5.5%) · excursion haute méd. +1.51% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.516% vs midi 0.731% vs clôture 0.751% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.049)_ ; drift intra méd. -0.182% ; recovery-V 10%
- **σ réalisé intraday** 2.243% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 62% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 254.2537 (VA 253.4767–254.7717 ; dernier close 253.58)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 64% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.1% · baisse 46% (gap-down >1% 21% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.71%) · haut méd +0.84% · range méd 1.63%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.09%) · haut méd +1.0% · range méd 2.0%
- Excursion ouverture 30min (n=160) : bas méd −0.84% (p90 −2.6%) · haut méd +1.07% · range méd 2.25%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.97%) · haut méd +1.32% · range méd 2.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 253.58 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 70% (118/159) · gap 27% · délai 0.0min · rebond 45% (58/118) (MFE +0.93%)
   - −1.0% : fill 30min 50% · séance 60% (102/159) · gap 21% · délai 1.0min · rebond 51% (56/102) (MFE +1.06%)
   - −1.5% : fill 30min 39% · séance 51% (89/159) · gap 11% · délai 3.4min · rebond 52% (48/89) (MFE +1.05%)
   - −2.0% : fill 30min 30% · séance 44% (70/159) · gap 7% · délai 8.6min · rebond 64% (44/70) (MFE +1.15%)
   - −3.0% : fill 30min 11% · séance 26% (43/159) · gap 3% · délai 55.1min · rebond 34% (16/43) (MFE +0.77%)
   - −4.0% : fill 30min 5% · séance 15% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 9% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.18%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −1.01%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.59%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=480 jambes) : jambe baissière méd −1.07% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 96% (56/57) · rebond 50% (33/56)
      · −2.0% : fill 78% (42/57) · rebond 62% (28/42)
      · −3.0% : fill 52% (28/57) · rebond 36% (11/28)
      · −4.0% : fill 31% (19/57) · rebond 34% (8/19)
      · −5.0% : fill 22% (15/57) · rebond 77% (11/15)
   - **flat** (34 séances) :
      · −1.0% : fill 60% (20/34) · rebond 39% (6/20)
      · −2.0% : fill 36% (11/34) · rebond 48% (4/11)
      · −3.0% : fill 24% (9/34) · rebond 26% (3/9)
      · −4.0% : fill 11% (5/34) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/34) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 31% (26/68) · rebond 64% (17/26)
      · −2.0% : fill 20% (17/68) · rebond 79% (12/17)
      · −3.0% : fill 6% (6/68) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 69% si les 15 1res min sont vertes (89 cas) · 23% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 75% si début vert vs 17% si rouge (base 49% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -1.08% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.09% / q75 +1.85% → **scale +1.09% / runner +1.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **17%** (continue à baisser 67%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.41%** (au-delà de la MAE q10 -3.41%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.99% .. +2.35%] · haut q95 +2.79% · bas q05 -3.48%
   - 60min (n=160) : retour [-3.65% .. +2.63%] · haut q95 +3.37% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.83% .. +2.96%] · haut q95 +4.21% · bas q05 -4.88%
   - 4h (n=160) : retour [-3.91% .. +3.29%] · haut q95 +4.76% · bas q05 -5.18%
   - 6h (n=160) : retour [-4.59% .. +3.09%] · haut q95 +5.04% · bas q05 -5.22%
   - session (n=160) : retour [-4.33% .. +3.27%] · haut q95 +5.04% · bas q05 -5.22%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.33% / p90 1.7%) · ~1.3 replis/séance, durée méd 60.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 22.57 min, n=22)
   - −1.0% → **58%** (reprise méd 114.96 min, n=10)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.7%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.24% (q75 +3.91% / q95 +6.6%), MFE méd +3.42% / q90 +5.81%
   - Échelle scale-out : +3.42% (33%) / +5.29% (33%) / +5.81% (34%)
- **DÉSARMER** : repli > **−1.7%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.81% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 1.929  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 15.5%
- **ATR** : 8.79 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.147  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 45.2  _(transition)_
- **MA** : MA20 253.93 · MA50 265.12 · MA200 311.33  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 -1.1% · MA200 -15.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89664 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
