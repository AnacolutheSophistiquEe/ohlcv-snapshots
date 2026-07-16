# PLTR

**Generated** : 2026-07-16T22:02:29.656666+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $134.44  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $134.44 (+5.5% vs entrée) · entrée $127.42 · stop $121.05 · T1 $129.88 · R/R 0.39  
> ↳ P(T1 av. stop) 48 % · EV/risk -0.011 · ¼-Kelly 0.042 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $126.93–$127.91 (mid $127.42)
- Spot actuel : $134.44 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : $121.05 (stop swing_plan-based (-13.39%))
- Targets : T1 $129.88 · R/R 0.39 | T2 $132.34 · R/R 0.77 | T3 $134.80 · R/R 1.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $121.05


## Edge, scénarios & sizing

- EV/risk : -0.011 | EV/share : $-0.073 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 12 % | T3 8 %
- Kelly (position) : f* 0.17 | ¼-Kelly 0.042 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.1 | bear 11.2 | side 74.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 134.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→45% · +3.0%→26% · +5.0%→8% · +8.0%→2%
- Range intraday médian 3.91% (p90 7.33%) · excursion haute méd. +1.87% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.952% vs midi 0.733% vs clôture 0.836% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 52% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr 0.018)_ ; drift intra méd. 0.452% ; recovery-V 32%
- **σ réalisé intraday** 2.803% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 54% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 133.615 (VA 133.427–134.085 ; dernier close 133.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 62% · **stop −2.34%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 55% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.94%) · haut méd +0.97% · range méd 1.86%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.79%) · haut méd +1.18% · range méd 2.25%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.47%) · haut méd +1.32% · range méd 2.85%
- Excursion ouverture 60min (n=160) : bas méd −1.32% (p90 −3.89%) · haut méd +1.53% · range méd 3.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 133.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (117/159) · gap 42% · délai 0.0min · rebond 55% (63/117) (MFE +1.14%)
   - −1.0% : fill 30min 56% · séance 66% (106/159) · gap 32% · délai 0.0min · rebond 58% (60/106) (MFE +1.31%)
   - −1.5% : fill 30min 47% · séance 58% (90/159) · gap 24% · délai 0.1min · rebond 64% (55/90) (MFE +1.27%)
   - −2.0% : fill 30min 39% · séance 50% (74/159) · gap 17% · délai 1.8min · rebond 59% (45/74) (MFE +1.36%)
   - −3.0% : fill 30min 21% · séance 34% (53/159) · gap 9% · délai 4.2min · rebond 48% (24/53) (MFE +0.96%)
   - −4.0% : fill 30min 16% · séance 25% (40/159) · gap 4% · délai 10.7min · rebond 53% (20/40) (MFE +1.07%)
   - −5.0% : fill 30min 12% · séance 20% (28/159) · gap 2% · délai 25.4min · rebond 62% (15/28) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.75%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.71%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.49%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.07% (p90 −2.52%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 94% (65/69) · rebond 62% (39/65)
      · −2.0% : fill 78% (53/69) · rebond 57% (34/53)
      · −3.0% : fill 58% (38/69) · rebond 44% (18/38)
      · −4.0% : fill 46% (30/69) · rebond 52% (15/30)
      · −5.0% : fill 41% (23/69) · rebond 64% (13/23)
   - **flat** (31 séances) :
      · −1.0% : fill 75% (24/31) · rebond 40% (12/24)
      · −2.0% : fill 50% (12/31) · rebond 70% (7/12)
      · −3.0% : fill 39% (10/31) · rebond 75% (5/10)
      · −4.0% : fill 20% (7/31) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/31) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/59) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 69% si les 15 1res min sont vertes (82 cas) · 36% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **42min** → P(séance verte=clôture>ouverture) 79% si début vert vs 21% si rouge (base 53% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -1.28% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.16% → **scale +1.18% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **21%** (continue à baisser 50%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.33%** (au-delà de la MAE q10 -3.33%), cible rebond +1.36% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.85% .. +3.69%] · haut q95 +3.97% · bas q05 -4.04%
   - 60min (n=160) : retour [-3.6% .. +3.88%] · haut q95 +4.67% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.86% .. +4.93%] · haut q95 +4.93% · bas q05 -4.52%
   - 4h (n=160) : retour [-4.38% .. +5.63%] · haut q95 +6.11% · bas q05 -5.22%
   - 6h (n=160) : retour [-4.98% .. +5.36%] · haut q95 +6.79% · bas q05 -5.58%
   - session (n=160) : retour [-4.78% .. +4.71%] · haut q95 +6.79% · bas q05 -5.59%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 82.1  _(surachat)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist 1.749  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 27.4%
- **ATR** : 7.15 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.039  _(neutre)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 45.1  _(transition)_
- **MA** : MA20 125.17 · MA50 132.55 · MA200 155.87  _(prix > MA20)_
- **Dist MA** : MA20 +7.4% · MA50 +1.4% · MA200 -13.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91244 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
