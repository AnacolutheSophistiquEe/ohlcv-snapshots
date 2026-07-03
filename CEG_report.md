# CEG

**Generated** : 2026-07-03T21:55:38.404962+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $239.25  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $239.25 (+4.6% vs entrée) · entrée $228.83 · stop $225.40 · T1 $231.91 · R/R 0.9  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.077 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.0 < 20 (tendance pas encore confirmée) alors que Choppiness 37.6 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $228.21–$229.45 (mid $228.83)
- Spot actuel : $239.25 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $225.40 (stop swing_plan-based (-10.08%))
- Targets : T1 $231.91 · R/R 0.9 | T2 $234.99 · R/R 1.8 | T3 $238.08 · R/R 2.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $225.40


## Edge, scénarios & sizing

- EV/risk : -0.077 | EV/share : $-0.265 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 23 % | T3 10 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 75.8 | bear 5.9 | side 18.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→36% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.51%) · excursion haute méd. +1.49% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.566% vs midi 0.738% vs clôture 0.789% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.572% ; recovery-V 16%
- **σ réalisé intraday** 2.457% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 238.6079 (VA 237.7041–240.4154 ; dernier close 239.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 63% · **stop −3.25%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.12% · baisse 44% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.71%) · haut méd +0.79% · range méd 1.71%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.26%) · haut méd +1.0% · range méd 2.13%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.97%) · haut méd +1.08% · range méd 2.34%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.17%) · haut méd +1.3% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 239.17 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (120/159) · gap 27% · délai 0.0min · rebond 44% (59/120) (MFE +0.89%)
   - −1.0% : fill 30min 53% · séance 65% (105/159) · gap 21% · délai 1.6min · rebond 51% (58/105) (MFE +1.06%)
   - −1.5% : fill 30min 41% · séance 56% (91/159) · gap 11% · délai 4.1min · rebond 50% (49/91) (MFE +1.0%)
   - −2.0% : fill 30min 32% · séance 48% (71/159) · gap 9% · délai 9.2min · rebond 63% (45/71) (MFE +1.1%)
   - −3.0% : fill 30min 14% · séance 28% (43/159) · gap 3% · délai 36.6min · rebond 39% (18/43) (MFE +0.74%)
   - −4.0% : fill 30min 6% · séance 18% (29/159) · gap 2% · délai 47.4min · rebond 38% (13/29) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 11% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −1.4%) → stop au-delà de −0.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.15%) → stop au-delà de −0.85% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=474 jambes) : jambe baissière méd −1.09% (p90 −2.65%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 100% (56/56) · rebond 50% (34/56)
      · −2.0% : fill 82% (41/56) · rebond 61% (28/41)
      · −3.0% : fill 55% (26/56) · rebond 43% (11/26)
      · −4.0% : fill 40% (19/56) · rebond 34% (8/19)
      · −5.0% : fill 28% (15/56) · rebond 77% (11/15)
   - **flat** (36 séances) :
      · −1.0% : fill 66% (22/36) · rebond 39% (7/22)
      · −2.0% : fill 40% (13/36) · rebond 48% (5/13)
      · −3.0% : fill 27% (11/36) · rebond 29% (5/11)
      · −4.0% : fill 12% (6/36) · rebond 23% (2/6)
      · −5.0% : fill 4% (3/36) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 38% (27/67) · rebond 63% (17/27)
      · −2.0% : fill 24% (17/67) · rebond 79% (12/17)
      · −3.0% : fill 7% (6/67) · rebond 32% (2/6)
      · −4.0% : fill 4% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 72% si les 15 1res min sont vertes (88 cas) · 18% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 84% si début vert vs 11% si rouge (base 48% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **84%** · continue >prix actuel 37% ; creux résiduel méd -1.0% (q20 -1.91%) → **SL/trailing à −1.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.82% / q75 +1.67% → **scale +0.82% / runner +1.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **11%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.85%** (au-delà de la MAE q10 -2.85%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.3%] · haut q95 +3.02% · bas q05 -3.66%
   - 60min (n=160) : retour [-3.87% .. +2.86%] · haut q95 +3.48% · bas q05 -4.67%
   - 2h (n=160) : retour [-4.19% .. +3.13%] · haut q95 +4.23% · bas q05 -5.3%
   - 4h (n=160) : retour [-4.52% .. +3.35%] · haut q95 +5.28% · bas q05 -5.88%
   - 6h (n=160) : retour [-4.84% .. +3.49%] · haut q95 +5.28% · bas q05 -6.84%
   - session (n=160) : retour [-4.34% .. +3.48%] · haut q95 +5.28% · bas q05 -6.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 11% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.29% / p90 1.8%) · ~2.0 replis/séance, durée méd 55.87 min. P(nouveau plus-haut après repli) :
   - −0.5% → **60%** (reprise méd 17.23 min, n=23)
   - −1.0% → **42%** (reprise méd 20.49 min, n=9)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.8%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +3.46% (q75 +4.43% / q95 +6.6%), MFE méd +3.74% / q90 +6.4%
   - Échelle scale-out : +3.74% (33%) / +5.32% (33%) / +6.4% (34%)
- **DÉSARMER** : repli > **−1.8%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.4% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 85% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.862  _(bearish_recent)_
- **BB** : %B 0.09 · largeur 18.2%
- **ATR** : 10.42 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.239  _(distribution)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 37.6  _(marche directionnel)_
- **MA** : MA20 258.3 · MA50 278.67 · MA200 316.09  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -14.1% · MA200 -24.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89056 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
