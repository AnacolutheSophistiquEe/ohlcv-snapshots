# SMCI

**Generated** : 2026-08-07T22:00:19.222264+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $31.13  

> 🟡 **WAIT-FOR-DIP** — spot +4.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $31.13 (+4.7% vs entrée) · entrée $29.73 · stop $28.77 · T1 $31.64 · R/R 1.99  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.019 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.21% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $29.51–$29.94 (mid $29.73)
- Spot actuel : $31.13 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : $28.77 (stop swing_plan-based (-17.98%))
- Targets : T1 $31.64 · R/R 1.99 | T2 $32.30 · R/R 2.68 | T3 $32.97 · R/R 3.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $28.77


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.088 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 66.0 | bear 7.3 | side 26.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 374.0 (= 12 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.511% → cible +6.427% / stop −3.214%, p_fill 30%, n_eff≈13.0) : P(cible|rempli) **0%** · **EV/risk +0.019** (×p_fill ; si rempli +0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→62% · +3.0%→45% · +5.0%→26% · +8.0%→11%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.66%
- Profil de vol intra : ouverture 4.018% vs midi 1.225% vs clôture 1.634% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -0.331% ; recovery-V 22%
- **σ réalisé intraday** 4.096% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 56% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 30.0312 (VA 29.7942–30.4657 ; dernier close 29.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 45% (gap-down >1% 34% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.61%) · haut méd +0.91% · range méd 2.0%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.24%) · haut méd +1.24% · range méd 2.79%
- Excursion ouverture 30min (n=160) : bas méd −1.64% (p90 −3.76%) · haut méd +1.4% · range méd 3.68%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −4.84%) · haut méd +1.65% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 29.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (124/159) · gap 41% · délai 0.0min · rebond 56% (73/124) (MFE +1.29%)
   - −1.0% : fill 30min 57% · séance 72% (114/159) · gap 34% · délai 0.0min · rebond 61% (67/114) (MFE +1.32%)
   - −1.5% : fill 30min 47% · séance 65% (100/159) · gap 24% · délai 0.0min · rebond 63% (62/100) (MFE +1.53%)
   - −2.0% : fill 30min 44% · séance 56% (89/159) · gap 18% · délai 0.8min · rebond 66% (56/89) (MFE +1.68%)
   - −3.0% : fill 30min 32% · séance 51% (74/159) · gap 13% · délai 9.8min · rebond 62% (46/74) (MFE +1.8%)
   - −4.0% : fill 30min 21% · séance 39% (54/159) · gap 8% · délai 21.7min · rebond 70% (34/54) (MFE +1.68%)
   - −5.0% : fill 30min 16% · séance 32% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −2.28%) → stop au-delà de −1.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.15%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.71% (p90 −2.71%) → stop au-delà de −1.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (68/70) · rebond 53% (38/68)
      · −2.0% : fill 87% (61/70) · rebond 60% (35/61)
      · −3.0% : fill 83% (55/70) · rebond 57% (32/55)
      · −4.0% : fill 64% (42/70) · rebond 67% (26/42)
      · −5.0% : fill 55% (35/70) · rebond 76% (24/35)
   - **flat** (13 séances) :
      · −1.0% : fill 97% (12/13) · rebond 90% (9/12)
      · −2.0% : fill 61% (9/13) · rebond 87% (6/9)
      · −3.0% : fill 35% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 30% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 47% (34/76) · rebond 69% (20/34)
      · −2.0% : fill 26% (19/76) · rebond 77% (15/19)
      · −3.0% : fill 24% (16/76) · rebond 70% (11/16)
      · −4.0% : fill 18% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 16% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 70% si les 15 1res min sont vertes (72 cas) · 23% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 82% si début vert vs 6% si rouge (base 44% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **82%** · continue >prix actuel 46% ; creux résiduel méd -1.42% (q20 -3.1%) → **SL/trailing à −3.1%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.85% → **scale +1.59% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **6%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.94%** (au-delà de la MAE q10 -4.94%), cible rebond +1.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.68%] · haut q95 +6.05% · bas q05 -4.49%
   - 60min (n=160) : retour [-4.42% .. +5.38%] · haut q95 +6.58% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.88% .. +6.65%] · haut q95 +7.94% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.5% .. +7.42%] · haut q95 +8.64% · bas q05 -6.92%
   - 6h (n=160) : retour [-6.03% .. +6.84%] · haut q95 +9.07% · bas q05 -7.27%
   - session (n=160) : retour [-7.61% .. +7.84%] · haut q95 +9.41% · bas q05 -8.27%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist 0.536  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 34.4%
- **ATR** : 2.51 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.006  _(neutre)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 28.17 · MA50 31.86 · MA200 32.19  _(prix > MA20)_
- **Dist MA** : MA20 +10.5% · MA50 -2.3% · MA200 -3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91973 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
