# PLTR

**Generated** : 2026-07-09T22:04:05.962319+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $129.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $129.04 (+10.7% vs entrée) · entrée $116.57 · stop $113.96 · T1 $121.79 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.036 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $115.53–$117.61 (mid $116.57)
- Spot actuel : $129.04 (+10.7% au-dessus de la zone — repli à attendre)
- Stop : $113.96 (stop swing_plan-based (-11.68%))
- Targets : T1 $121.79 · R/R 2.0 | T2 $127.00 · R/R 4.0 | T3 $132.22 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.96


## Edge, scénarios & sizing

- EV/risk : -0.036 | EV/share : $-0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 26.1 | bear 15.8 | side 58.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 129.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→44% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.94% (p90 7.17%) · excursion haute méd. +1.85% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.934% vs midi 0.74% vs clôture 0.829% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 53% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr -0.004)_ ; drift intra méd. 0.18% ; recovery-V 32%
- **σ réalisé intraday** 2.814% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 52% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 128.3544 (VA 126.8006–129.9081 ; dernier close 132.22)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 54% · **stop −2.71%** sous le fill (sous le bruit) · cible +1.09% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 57% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.96% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.79%) · haut méd +1.18% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.31%) · haut méd +1.32% · range méd 2.78%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.83%) · haut méd +1.52% · range méd 3.2%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 74% (116/159) · gap 43% · délai 0.0min · rebond 56% (63/116) (MFE +1.14%)
   - −1.0% : fill 30min 56% · séance 66% (105/159) · gap 31% · délai 0.0min · rebond 60% (61/105) (MFE +1.32%)
   - −1.5% : fill 30min 47% · séance 58% (88/159) · gap 23% · délai 0.2min · rebond 63% (54/88) (MFE +1.37%)
   - −2.0% : fill 30min 39% · séance 48% (72/159) · gap 15% · délai 1.9min · rebond 58% (44/72) (MFE +1.38%)
   - −3.0% : fill 30min 19% · séance 33% (52/159) · gap 6% · délai 11.7min · rebond 48% (24/52) (MFE +0.96%)
   - −4.0% : fill 30min 14% · séance 24% (38/159) · gap 3% · délai 26.3min · rebond 46% (18/38) (MFE +0.88%)
   - −5.0% : fill 30min 11% · séance 18% (26/159) · gap 2% · délai 25.4min · rebond 54% (13/26) (MFE +1.09%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.71%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.77%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.54%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=539 jambes) : jambe baissière méd −1.06% (p90 −2.54%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 94% (64/68) · rebond 63% (39/64)
      · −2.0% : fill 76% (52/68) · rebond 58% (34/52)
      · −3.0% : fill 54% (37/68) · rebond 43% (18/37)
      · −4.0% : fill 42% (28/68) · rebond 43% (13/28)
      · −5.0% : fill 36% (21/68) · rebond 56% (11/21)
   - **flat** (33 séances) :
      · −1.0% : fill 74% (25/33) · rebond 41% (13/25)
      · −2.0% : fill 49% (12/33) · rebond 70% (7/12)
      · −3.0% : fill 38% (10/33) · rebond 75% (5/10)
      · −4.0% : fill 19% (7/33) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/33) · rebond 57% (2/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 28% (16/58) · rebond 73% (9/16)
      · −2.0% : fill 13% (8/58) · rebond 42% (3/8)
      · −3.0% : fill 4% (5/58) · rebond 15% (1/5)
      · −4.0% : fill 3% (3/58) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/58) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 67% si les 15 1res min sont vertes (82 cas) · 36% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:06** → P(séance verte=clôture>ouverture) 86% si début vert vs 14% si rouge (base 53% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **86%** · continue >prix actuel 41% ; creux résiduel méd -1.03% (q20 -1.51%) → **SL/trailing à −1.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.87% / q75 +1.61% → **scale +0.87% / runner +1.61%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **14%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.6%** (au-delà de la MAE q10 -2.6%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.93% .. +3.37%] · haut q95 +3.76% · bas q05 -4.12%
   - 60min (n=160) : retour [-3.31% .. +3.51%] · haut q95 +4.5% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.6% .. +4.44%] · haut q95 +4.75% · bas q05 -4.49%
   - 4h (n=160) : retour [-4.33% .. +4.89%] · haut q95 +5.58% · bas q05 -5.33%
   - 6h (n=160) : retour [-5.03% .. +4.54%] · haut q95 +5.58% · bas q05 -5.6%
   - session (n=160) : retour [-4.91% .. +4.47%] · haut q95 +5.58% · bas q05 -5.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 15% vs absente 3% (base 6%)
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

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.6  _(neutre)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist 1.964  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 27.0%
- **ATR** : 7.11 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.042  _(neutre)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 42.4  _(transition)_
- **MA** : MA20 125.09 · MA50 133.54 · MA200 157.07  _(prix > MA20)_
- **Dist MA** : MA20 +3.2% · MA50 -3.4% · MA200 -17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91162 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
