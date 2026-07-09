# PLTR

**Generated** : 2026-07-09T00:19:03.443542+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $132.22  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $132.22 (+5.1% vs entrée) · entrée $125.76 · stop $118.21 · T1 $128.30 · R/R 0.34  
> ↳ P(T1 av. stop) 42 % · EV/risk -0.025 · ¼-Kelly 0.045 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −6.0% cohérent avec le bruit 5 s (EV-optimal ≈ −6.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $125.25–$126.27 (mid $125.76)
- Spot actuel : $132.22 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : $118.21 (stop swing_plan-based (-12.77%))
- Targets : T1 $128.30 · R/R 0.34 | T2 $130.83 · R/R 0.67 | T3 $133.37 · R/R 1.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $118.21


## Edge, scénarios & sizing

- EV/risk : -0.025 | EV/share : $-0.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 11 % | T3 8 %
- Kelly (position) : f* 0.178 | ¼-Kelly 0.045 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.0 | bear 9.8 | side 73.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 132.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→42% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.91% (p90 7.17%) · excursion haute méd. +1.85% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.929% vs midi 0.744% vs clôture 0.824% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 52% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.002)_ ; drift intra méd. 0.086% ; recovery-V 26%
- **σ réalisé intraday** 2.817% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 55% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 138.5644 (VA 135.0731–138.7481 ; dernier close 134.36)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 49% · **stop −2.91%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 56% (gap-down >1% 30% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.95% · range méd 1.81%
- Excursion ouverture 15min (n=160) : bas méd −0.89% (p90 −2.79%) · haut méd +1.18% · range méd 2.25%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.41%) · haut méd +1.32% · range méd 2.69%
- Excursion ouverture 60min (n=160) : bas méd −1.32% (p90 −3.83%) · haut méd +1.53% · range méd 3.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 134.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (116/159) · gap 41% · délai 0.0min · rebond 57% (64/116) (MFE +1.14%)
   - −1.0% : fill 30min 55% · séance 66% (105/159) · gap 30% · délai 0.0min · rebond 62% (62/105) (MFE +1.39%)
   - −1.5% : fill 30min 46% · séance 57% (87/159) · gap 21% · délai 0.5min · rebond 66% (54/87) (MFE +1.54%)
   - −2.0% : fill 30min 38% · séance 48% (71/159) · gap 14% · délai 4.2min · rebond 61% (44/71) (MFE +1.43%)
   - −3.0% : fill 30min 18% · séance 32% (51/159) · gap 4% · délai 21.0min · rebond 45% (23/51) (MFE +0.85%)
   - −4.0% : fill 30min 12% · séance 22% (37/159) · gap 3% · délai 28.5min · rebond 41% (17/37) (MFE +0.82%)
   - −5.0% : fill 30min 9% · séance 16% (25/159) · gap 2% · délai 25.8min · rebond 49% (12/25) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.71%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.6%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.54%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=539 jambes) : jambe baissière méd −1.06% (p90 −2.58%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 94% (63/67) · rebond 66% (39/63)
      · −2.0% : fill 75% (51/67) · rebond 61% (34/51)
      · −3.0% : fill 52% (36/67) · rebond 38% (17/36)
      · −4.0% : fill 40% (27/67) · rebond 37% (12/27)
      · −5.0% : fill 33% (20/67) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 74% (25/33) · rebond 41% (13/25)
      · −2.0% : fill 49% (12/33) · rebond 70% (7/12)
      · −3.0% : fill 38% (10/33) · rebond 75% (5/10)
      · −4.0% : fill 19% (7/33) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/33) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 28% (17/59) · rebond 73% (10/17)
      · −2.0% : fill 13% (8/59) · rebond 42% (3/8)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 3% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (82 cas) · 34% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:06** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 52% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 149min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **86%** · continue >prix actuel 41% ; creux résiduel méd -1.03% (q20 -1.51%) → **SL/trailing à −1.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.87% / q75 +1.61% → **scale +0.87% / runner +1.61%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **10%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.64%** (au-delà de la MAE q10 -2.64%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.94% .. +3.37%] · haut q95 +3.77% · bas q05 -4.13%
   - 60min (n=160) : retour [-3.33% .. +3.59%] · haut q95 +4.5% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.6% .. +4.46%] · haut q95 +4.76% · bas q05 -4.49%
   - 4h (n=160) : retour [-4.37% .. +4.91%] · haut q95 +5.59% · bas q05 -5.33%
   - 6h (n=160) : retour [-5.03% .. +4.6%] · haut q95 +5.59% · bas q05 -5.6%
   - session (n=160) : retour [-4.93% .. +4.47%] · haut q95 +5.59% · bas q05 -5.62%


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.1  _(neutre)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist 2.126  _(bullish_recent)_
- **BB** : %B 0.7 · largeur 27.3%
- **ATR** : 7.02 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.079  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 41.9  _(transition)_
- **MA** : MA20 125.24 · MA50 133.82 · MA200 157.33  _(prix > MA20)_
- **Dist MA** : MA20 +5.6% · MA50 -1.2% · MA200 -16.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91263 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
