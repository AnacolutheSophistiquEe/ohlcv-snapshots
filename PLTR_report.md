# PLTR

**Generated** : 2026-07-07T00:15:14.600474+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $132.54  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $132.54 (+5.2% vs entrée) · entrée $126.00 · stop $118.44 · T1 $128.61 · R/R 0.35  
> ↳ P(T1 av. stop) 39 % · EV/risk -0.031 · ¼-Kelly 0.04 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −6.0% cohérent avec le bruit 5 s (EV-optimal ≈ −6.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $125.48–$126.52 (mid $126.00)
- Spot actuel : $132.54 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $118.44 (stop swing_plan-based (-12.93%))
- Targets : T1 $128.61 · R/R 0.35 | T2 $131.22 · R/R 0.69 | T3 $133.83 · R/R 1.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $118.44


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.232 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 9 % | T3 6 %
- Kelly (position) : f* 0.16 | ¼-Kelly 0.04 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.3 | bear 9.7 | side 73.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→72% · +2.0%→41% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.83% (p90 7.17%) · excursion haute méd. +1.81% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.89% vs midi 0.735% vs clôture 0.813% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 52% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.13% ; recovery-V 21%
- **σ réalisé intraday** 2.76% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 55% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 130.9267 (VA 129.3798–131.4793 ; dernier close 129.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 49% · **stop −2.91%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 56% (gap-down >1% 29% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.93% · range méd 1.77%
- Excursion ouverture 15min (n=160) : bas méd −0.89% (p90 −2.79%) · haut méd +1.18% · range méd 2.25%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.51%) · haut méd +1.32% · range méd 2.69%
- Excursion ouverture 60min (n=160) : bas méd −1.32% (p90 −3.83%) · haut méd +1.53% · range méd 3.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.17 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 72% (115/159) · gap 41% · délai 0.0min · rebond 55% (63/115) (MFE +1.11%)
   - −1.0% : fill 30min 55% · séance 66% (105/159) · gap 29% · délai 0.0min · rebond 61% (62/105) (MFE +1.32%)
   - −1.5% : fill 30min 46% · séance 57% (87/159) · gap 20% · délai 0.9min · rebond 64% (54/87) (MFE +1.37%)
   - −2.0% : fill 30min 39% · séance 49% (72/159) · gap 14% · délai 4.2min · rebond 61% (45/72) (MFE +1.43%)
   - −3.0% : fill 30min 18% · séance 33% (52/159) · gap 4% · délai 20.9min · rebond 45% (24/52) (MFE +0.85%)
   - −4.0% : fill 30min 12% · séance 23% (37/159) · gap 3% · délai 28.5min · rebond 41% (17/37) (MFE +0.82%)
   - −5.0% : fill 30min 9% · séance 17% (25/159) · gap 2% · délai 25.8min · rebond 49% (12/25) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.7%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.38%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.37%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=538 jambes) : jambe baissière méd −1.08% (p90 −2.66%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 93% (63/67) · rebond 64% (39/63)
      · −2.0% : fill 78% (52/67) · rebond 61% (35/52)
      · −3.0% : fill 55% (37/67) · rebond 38% (18/37)
      · −4.0% : fill 41% (27/67) · rebond 37% (12/27)
      · −5.0% : fill 34% (20/67) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 74% (25/33) · rebond 41% (13/25)
      · −2.0% : fill 49% (12/33) · rebond 70% (7/12)
      · −3.0% : fill 38% (10/33) · rebond 75% (5/10)
      · −4.0% : fill 19% (7/33) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/33) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 73% (10/17)
      · −2.0% : fill 13% (8/59) · rebond 42% (3/8)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 3% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 66% si les 15 1res min sont vertes (82 cas) · 31% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:06** → P(séance verte=clôture>ouverture) 85% si début vert vs 10% si rouge (base 50% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 149min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **85%** · continue >prix actuel 44% ; creux résiduel méd -1.03% (q20 -1.52%) → **SL/trailing à −1.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.84% / q75 +1.54% → **scale +0.84% / runner +1.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **10%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.64%** (au-delà de la MAE q10 -2.64%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.97% .. +2.55%] · haut q95 +3.44% · bas q05 -4.16%
   - 60min (n=160) : retour [-3.39% .. +3.66%] · haut q95 +4.08% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.63% .. +3.57%] · haut q95 +4.41% · bas q05 -4.5%
   - 4h (n=160) : retour [-4.43% .. +5.02%] · haut q95 +5.63% · bas q05 -5.36%
   - 6h (n=160) : retour [-5.04% .. +4.72%] · haut q95 +5.77% · bas q05 -5.61%
   - session (n=160) : retour [-4.98% .. +4.54%] · haut q95 +5.77% · bas q05 -5.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.6%) · ~3.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 24.87 min, n=29)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.6%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.37% (q75 +5.17% / q95 +7.65%), MFE méd +5.25% / q90 +8.69%
   - Échelle scale-out : +5.25% (33%) / +7.16% (33%) / +8.69% (34%)
- **DÉSARMER** : repli > **−1.6%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.69% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 72% du temps (retour médian dernière heure +0.21%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.7 · part idiosyncratique 0.3
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.8  _(neutre)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 1.329  _(bullish_recent)_
- **BB** : %B 0.7 · largeur 28.2%
- **ATR** : 6.79 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.142  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 44.1  _(transition)_
- **MA** : MA20 125.51 · MA50 134.18 · MA200 157.73  _(prix > MA20)_
- **Dist MA** : MA20 +5.6% · MA50 -1.2% · MA200 -16.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91889 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
