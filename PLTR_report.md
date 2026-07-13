# PLTR

**Generated** : 2026-07-13T22:02:03.788291+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $130.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $130.04 (+4.8% vs entrée) · entrée $124.12 · stop $116.68 · T1 $126.64 · R/R 0.34  
> ↳ P(T1 av. stop) 43 % · EV/risk -0.028 · ¼-Kelly 0.046 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −6.0% cohérent avec le bruit 5 s (EV-optimal ≈ −6.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $123.62–$124.63 (mid $124.12)
- Spot actuel : $130.04 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : $116.68 (stop swing_plan-based (-12.05%))
- Targets : T1 $126.64 · R/R 0.34 | T2 $129.16 · R/R 0.68 | T3 $131.68 · R/R 1.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $116.68


## Edge, scénarios & sizing

- EV/risk : -0.028 | EV/share : $-0.208 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 11 % | T3 8 %
- Kelly (position) : f* 0.183 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.8 | bear 9.9 | side 73.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 130.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→44% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.96% (p90 7.17%) · excursion haute méd. +1.81% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.957% vs midi 0.737% vs clôture 0.826% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 55% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr 0.005)_ ; drift intra méd. 0.023% ; recovery-V 34%
- **σ réalisé intraday** 2.78% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 126.5473 (VA 126.0958–127.1492 ; dernier close 126.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 58% · **stop −2.51%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 56% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.96%) · haut méd +0.94% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.79%) · haut méd +1.17% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −3.48%) · haut méd +1.26% · range méd 2.79%
- Excursion ouverture 60min (n=160) : bas méd −1.36% (p90 −3.97%) · haut méd +1.43% · range méd 3.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 126.79 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (117/159) · gap 43% · délai 0.0min · rebond 53% (63/117) (MFE +1.07%)
   - −1.0% : fill 30min 57% · séance 68% (106/159) · gap 32% · délai 0.0min · rebond 57% (60/106) (MFE +1.29%)
   - −1.5% : fill 30min 47% · séance 59% (89/159) · gap 24% · délai 0.2min · rebond 63% (54/89) (MFE +1.22%)
   - −2.0% : fill 30min 39% · séance 50% (73/159) · gap 16% · délai 2.4min · rebond 58% (44/73) (MFE +1.33%)
   - −3.0% : fill 30min 20% · séance 34% (52/159) · gap 7% · délai 5.7min · rebond 45% (23/52) (MFE +0.85%)
   - −4.0% : fill 30min 15% · séance 25% (39/159) · gap 3% · délai 14.8min · rebond 50% (19/39) (MFE +0.98%)
   - −5.0% : fill 30min 10% · séance 19% (27/159) · gap 2% · délai 25.9min · rebond 58% (14/27) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.85%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.77%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.54%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=540 jambes) : jambe baissière méd −1.07% (p90 −2.57%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 94% (64/68) · rebond 60% (38/64)
      · −2.0% : fill 77% (52/68) · rebond 55% (33/52)
      · −3.0% : fill 56% (37/68) · rebond 39% (17/37)
      · −4.0% : fill 44% (29/68) · rebond 48% (14/29)
      · −5.0% : fill 38% (22/68) · rebond 61% (12/22)
   - **flat** (33 séances) :
      · −1.0% : fill 74% (25/33) · rebond 41% (13/25)
      · −2.0% : fill 49% (12/33) · rebond 70% (7/12)
      · −3.0% : fill 38% (10/33) · rebond 75% (5/10)
      · −4.0% : fill 19% (7/33) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/33) · rebond 57% (2/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 32% (17/58) · rebond 61% (9/17)
      · −2.0% : fill 17% (9/58) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/58) · rebond 15% (1/5)
      · −4.0% : fill 3% (3/58) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/58) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (82 cas) · 37% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 77% si début vert vs 24% si rouge (base 52% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **77%** · continue >prix actuel 54% ; creux résiduel méd -1.35% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.3% / q75 +2.16% → **scale +1.3% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **24%** (continue à baisser 47%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.22%** (au-delà de la MAE q10 -3.22%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.9% .. +3.37%] · haut q95 +3.73% · bas q05 -4.09%
   - 60min (n=160) : retour [-3.61% .. +3.24%] · haut q95 +4.49% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.87% .. +4.41%] · haut q95 +4.73% · bas q05 -4.59%
   - 4h (n=160) : retour [-4.39% .. +4.86%] · haut q95 +5.55% · bas q05 -5.32%
   - 6h (n=160) : retour [-5.01% .. +4.42%] · haut q95 +5.55% · bas q05 -5.59%
   - session (n=160) : retour [-4.86% .. +4.47%] · haut q95 +5.55% · bas q05 -5.6%


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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.5  _(momentum haussier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist 1.599  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 26.7%
- **ATR** : 6.75 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.048  _(neutre)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 40.4  _(transition)_
- **MA** : MA20 124.87 · MA50 133.09 · MA200 156.54  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 -2.3% · MA200 -16.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91704 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
