# 000660

**Generated** : 2026-07-09T18:29:05.293460+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2190000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2190000.00 (+2.3% vs entrée) · entrée ₩2141166.61 · stop ₩2058730.90 · T1 ₩2227528.24 · R/R 1.05  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.019 _(réel 5 s)_ (GBM 0.104) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.85% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2123894.29–₩2158438.94 (mid ₩2141166.61)
- Spot actuel : ₩2190000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩2058730.90 (stop swing_plan-based (-9.19%))
- Targets : T1 ₩2227528.24 · R/R 1.05 | T2 ₩2313889.86 · R/R 2.1 | T3 ₩2400251.49 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2058730.90


## Edge, scénarios & sizing

- EV/risk : 0.104 | EV/share : ₩8565.467 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.131 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 62.2 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.226% → cible +4.033% / stop −3.85%, p_fill 45%, n_eff≈17.7) : P(cible|rempli) **25%** · **EV/risk -0.019** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −4.902% → cible +9.019% / stop −4.509%, p_fill 32%, n_eff≈10.9) : P(cible|rempli) **6%** · **EV/risk -0.283** (×p_fill ; si rempli -3.97% du capital)
  - **deep** (entrée dip −7.586% → cible +12.755% / stop −6.377%, p_fill 28%, n_eff≈10.4) : P(cible|rempli) **30%** · **EV/risk -0.074** (×p_fill ; si rempli -1.68% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→57% · +3.0%→44% · +5.0%→30% · +8.0%→15%
- Range intraday médian 5.86% (p90 11.41%) · excursion haute méd. +2.33% / basse méd. −1.68%
- Profil de vol intra : ouverture 4.263% vs midi 1.045% vs clôture 0.989% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 60% · range 27% · trend ↑9%/↓4% ; spike-down 53% · recovery-V 34%)_
- **Régime intraday** : **mixte** _(efficiency 0.251 ; mean-reverting — autocorr -0.14)_ ; drift intra méd. 0.913% ; recovery-V 30%
- **σ réalisé intraday** 4.406% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 37% / bas 29% / whipsaw 3%
- POC intraday (dernière séance, temps-au-prix) : 2257462.5 (VA 2238287.5–2269262.5 ; dernier close 2225000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 65% · **stop −6.72%** sous le fill (sous le bruit) · cible +2.52% · R/R 0.38 (high win-rate)
- Gaps overnight (n=135) : méd. -0.03% · baisse 50% (gap-down >1% 18% · >2% 15%)
- Excursion ouverture 5min (n=136) : bas méd −0.46% (p90 −4.24%) · haut méd +1.16% · range méd 2.92%
- Excursion ouverture 15min (n=136) : bas méd −0.83% (p90 −4.4%) · haut méd +1.53% · range méd 3.48%
- Excursion ouverture 30min (n=136) : bas méd −1.31% (p90 −4.62%) · haut méd +1.69% · range méd 3.99%
- Excursion ouverture 60min (n=136) : bas méd −1.31% (p90 −5.04%) · haut méd +1.95% · range méd 4.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2225000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 67% (86/135) · gap 25% · délai 0.2min · rebond 51% (45/86) (MFE +1.06%)
   - −1.0% : fill 30min 52% · séance 58% (74/135) · gap 18% · délai 0.2min · rebond 52% (42/74) (MFE +1.05%)
   - −1.5% : fill 30min 45% · séance 53% (65/135) · gap 16% · délai 0.2min · rebond 60% (39/65) (MFE +1.16%)
   - −2.0% : fill 30min 39% · séance 48% (59/135) · gap 15% · délai 0.2min · rebond 58% (37/59) (MFE +1.58%)
   - −3.0% : fill 30min 36% · séance 40% (49/135) · gap 15% · délai 0.2min · rebond 65% (33/49) (MFE +2.52%)
   - −4.0% : fill 30min 25% · séance 30% (35/135) · gap 9% · délai 0.2min · rebond 60% (24/35) (MFE +1.8%)
   - −5.0% : fill 30min 19% · séance 25% (28/135) · gap 6% · délai 0.2min · rebond 49% (18/28) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.0% (p90 −2.97%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.0% (p90 −2.92%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.0% (p90 −2.75%) → stop au-delà de −1.47% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=573 jambes) : jambe baissière méd −1.18% (p90 −3.34%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (39 séances) :
      · −1.0% : fill 79% (31/39) · rebond 42% (14/31)
      · −2.0% : fill 68% (27/39) · rebond 51% (16/27)
      · −3.0% : fill 64% (24/39) · rebond 55% (15/24)
      · −4.0% : fill 58% (21/39) · rebond 54% (14/21)
      · −5.0% : fill 48% (16/39) · rebond 46% (10/16)
   - **flat** (62 séances) :
      · −1.0% : fill 55% (34/62) · rebond 68% (23/34)
      · −2.0% : fill 43% (25/62) · rebond 68% (16/25)
      · −3.0% : fill 33% (19/62) · rebond 82% (14/19)
      · −4.0% : fill 20% (11/62) · rebond 82% (8/11)
      · −5.0% : fill 14% (9/62) · rebond 61% (6/9)
   - **gap-up** (34 séances) :
      · −1.0% : fill 34% (9/34) · rebond 48% (5/9)
      · −2.0% : fill 26% (7/34) · rebond 55% (5/7)
      · −3.0% : fill 19% (6/34) · rebond 62% (4/6)
      · −4.0% : fill 8% (3/34) · rebond 40% (2/3)
      · −5.0% : fill 8% (3/34) · rebond 40% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 54% en base · 73% si les 15 1res min sont vertes (78 cas) · 28% si rouges (58 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=136) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 90% si début vert vs 18% si rouge (base 61% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **90%** · continue >prix actuel 51% ; creux résiduel méd -1.45% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +4.33% → **scale +1.65% / runner +4.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=53) : edge inversé — récupère vert seulement **18%** (continue à baisser 49%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-4.86% .. +8.61%] · haut q95 +9.62% · bas q05 -6.09%
   - 60min (n=136) : retour [-5.21% .. +8.35%] · haut q95 +9.62% · bas q05 -6.09%
   - 2h (n=136) : retour [-4.89% .. +9.18%] · haut q95 +9.68% · bas q05 -6.41%
   - 4h (n=136) : retour [-5.73% .. +11.26%] · haut q95 +11.89% · bas q05 -7.65%
   - 6h (n=136) : retour [-7.35% .. +11.47%] · haut q95 +12.28% · bas q05 -9.57%
   - session (n=136) : retour [-7.41% .. +11.21%] · haut q95 +12.72% · bas q05 -9.58%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.4% des séances sont trend-up (mild 0.7% / strong 6.6%) · base = 10 séances trend-up (n_eff 9.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 25% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.04% (p75 1.37% / p90 1.86%) · ~2.56 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **79%** (reprise méd 19.25 min, n=30)
   - −1.0% → **66%** (reprise méd 30.0 min, n=17)
   - −1.5% → **100%** (reprise méd 29.63 min, n=6)
   - −2.0% → **100%** (reprise méd 101.08 min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.86%** (p90, défaut prudent ; serré/agressif −1.37%) ; extension open→close méd +8.52% (q75 +12.19% / q95 +16.01%), MFE méd +9.77% / q90 +14.75%
   - Échelle scale-out : +9.77% (33%) / +12.49% (33%) / +14.75% (34%)
- **DÉSARMER** : repli > **−1.86%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.75% : P(retournement après) 0% (mèche méd 0.47%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.08%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -87248.263  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 40.7%
- **ATR** : 274785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 2486750.0 · MA50 2125244.49 · MA200 1066384.77  _(prix < MA20)_
- **Dist MA** : MA20 -11.9% · MA50 +3.0% · MA200 +105.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88513 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
