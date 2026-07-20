# 000660

**Generated** : 2026-07-20T00:13:19.406408+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩1842000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1842000.00 (+2.1% vs entrée) · entrée ₩1803929.36 · stop ₩1727922.22 · T1 ₩1855000.00 · R/R 0.67  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.139 _(réel 5 s)_ (GBM -0.037) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.21% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1793715.23–₩1814143.49 (mid ₩1803929.36)
- Spot actuel : ₩1842000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1727922.22 (stop swing_plan-based (-11.65%))
- Targets : T1 ₩1855000.00 · R/R 0.67 | T2 ₩2019833.22 · R/R 2.84 | T3 ₩2052864.76 · R/R 3.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1727922.22


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : ₩-2786.982 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.07 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.6 | bear 62.3 | side 29.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.064% → cible +2.831% / stop −4.213%, p_fill 75%, n_eff≈26.8) : P(cible|rempli) **31%** · **EV/risk -0.139** (×p_fill ; si rempli -0.79% du capital)
  - **swing** (entrée dip −4.55% → cible +14.878% / stop −7.439%, p_fill 59%, n_eff≈19.7) : P(cible|rempli) **16%** · **EV/risk -0.244** (×p_fill ; si rempli -3.08% du capital)
  - **deep** (entrée dip −7.024% → cible +40.55% / stop −18.0%, p_fill 48%, n_eff≈15.1) : P(cible|rempli) **4%** · **EV/risk -0.247** (×p_fill ; si rempli -9.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→81% · +2.0%→56% · +3.0%→38% · +5.0%→24% · +8.0%→12%
- Range intraday médian 6.1% (p90 11.16%) · excursion haute méd. +2.25% / basse méd. −2.5%
- Profil de vol intra : ouverture 2.93% vs midi 1.208% vs clôture 1.489% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (139 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑3%/↓0% ; spike-down 67% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.707% ; recovery-V 26%
- **σ réalisé intraday** 5.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 73% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 1847200.0 (VA 1832800.0–1864000.0 ; dernier close 1840000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 78% · **stop −8.8%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.29 (high win-rate)
- Gaps overnight (n=138) : méd. -0.04% · baisse 50% (gap-down >1% 36% · >2% 29%)
- Excursion ouverture 5min (n=139) : bas méd −0.56% (p90 −1.64%) · haut méd +0.94% · range méd 1.51%
- Excursion ouverture 15min (n=139) : bas méd −0.79% (p90 −2.14%) · haut méd +1.17% · range méd 2.03%
- Excursion ouverture 30min (n=139) : bas méd −1.3% (p90 −3.03%) · haut méd +1.34% · range méd 2.74%
- Excursion ouverture 60min (n=139) : bas méd −1.34% (p90 −3.81%) · haut méd +1.67% · range méd 3.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1840000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 66% (86/138) · gap 42% · délai 0.0min · rebond 55% (45/86) (MFE +1.35%)
   - −1.0% : fill 30min 54% · séance 63% (79/138) · gap 36% · délai 0.0min · rebond 64% (49/79) (MFE +1.8%)
   - −1.5% : fill 30min 49% · séance 58% (70/138) · gap 34% · délai 0.0min · rebond 66% (44/70) (MFE +1.79%)
   - −2.0% : fill 30min 41% · séance 51% (63/138) · gap 29% · délai 0.0min · rebond 63% (41/63) (MFE +1.67%)
   - −3.0% : fill 30min 40% · séance 47% (55/138) · gap 23% · délai 2.7min · rebond 78% (41/55) (MFE +2.57%)
   - −4.0% : fill 30min 28% · séance 39% (42/138) · gap 12% · délai 6.0min · rebond 76% (32/42) (MFE +2.57%)
   - −5.0% : fill 30min 13% · séance 30% (33/138) · gap 9% · délai 30.4min · rebond 72% (25/33) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.6%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.44%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.5% (p90 −3.71%) → stop au-delà de −2.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=704 jambes) : jambe baissière méd −1.3% (p90 −3.38%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (58/60) · rebond 53% (31/58)
      · −2.0% : fill 87% (49/60) · rebond 60% (29/49)
      · −3.0% : fill 82% (44/60) · rebond 74% (31/44)
      · −4.0% : fill 71% (37/60) · rebond 72% (27/37)
      · −5.0% : fill 59% (30/60) · rebond 69% (22/30)
   - **flat** (11 séances) :
      · −1.0% : fill 88% (8/11) · rebond 81% (6/8)
      · −2.0% : fill 70% (6/11) · rebond 80% (5/6)
      · −3.0% : fill 60% (5/11) · rebond 100% (5/5)
      · −4.0% : fill 31% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 14% (1/11) · rebond 100% (1/1)
   - **gap-up** (67 séances) :
      · −1.0% : fill 26% (13/67) · rebond 98% (12/13)
      · −2.0% : fill 14% (8/67) · rebond 75% (7/8)
      · −3.0% : fill 12% (6/67) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/67) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=139) : 45% en base · 53% si les 15 1res min sont vertes (75 cas) · 34% si rouges (64 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=139) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 74% si début vert vs 17% si rouge (base 45% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -1.56% (q20 -6.57%) → **SL/trailing à −6.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.41% → **scale +1.31% / runner +3.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=64) : edge inversé — récupère vert seulement **17%** (continue à baisser 63%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.75%** (au-delà de la MAE q10 -6.75%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=139) : retour [-2.85% .. +2.98%] · haut q95 +3.68% · bas q05 -3.68%
   - 60min (n=139) : retour [-3.53% .. +5.73%] · haut q95 +5.8% · bas q05 -5.16%
   - 2h (n=139) : retour [-4.64% .. +5.67%] · haut q95 +7.95% · bas q05 -6.58%
   - 4h (n=139) : retour [-5.82% .. +7.13%] · haut q95 +8.52% · bas q05 -8.11%
   - 6h (n=139) : retour [-7.22% .. +7.8%] · haut q95 +9.78% · bas q05 -9.01%
   - session (n=139) : retour [-6.56% .. +8.12%] · haut q95 +9.78% · bas q05 -9.01%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.5% des séances sont trend-up (mild 0% / strong 6.5%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 20% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.7  _(survente)_
- **ADX** : 27.3  _(tendance etablie)_
- **MACD** : hist -84253.399  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 57.1%
- **ATR** : 253357.14 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.185  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 45.6  _(transition)_
- **MA** : MA20 2378350.0 · MA50 2190066.62 · MA200 1107604.31  _(prix < MA20)_
- **Dist MA** : MA20 -22.6% · MA50 -15.9% · MA200 +66.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87423 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
