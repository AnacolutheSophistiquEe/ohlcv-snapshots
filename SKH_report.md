# 000660

**Generated** : 2026-07-17T21:49:35.443983+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩1842000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1842000.00 (+2.1% vs entrée) · entrée ₩1803929.36 · stop ₩1727922.22 · T1 ₩1855000.00 · R/R 0.67  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.132 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
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

- EV/risk : -0.016 | EV/share : ₩-1245.859 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.6 | bear 62.3 | side 29.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.064% → cible +2.831% / stop −4.213%, p_fill 73%, n_eff≈26.3) : P(cible|rempli) **33%** · **EV/risk -0.132** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −4.55% → cible +14.878% / stop −7.439%, p_fill 57%, n_eff≈19.1) : P(cible|rempli) **18%** · **EV/risk -0.209** (×p_fill ; si rempli -2.75% du capital)
  - **deep** (entrée dip −7.024% → cible +40.55% / stop −18.0%, p_fill 46%, n_eff≈14.5) : P(cible|rempli) **5%** · **EV/risk -0.210** (×p_fill ; si rempli -8.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→82% · +2.0%→57% · +3.0%→39% · +5.0%→24% · +8.0%→12%
- Range intraday médian 6.1% (p90 11.16%) · excursion haute méd. +2.33% / basse méd. −2.45%
- Profil de vol intra : ouverture 2.912% vs midi 1.202% vs clôture 1.47% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑3%/↓0% ; spike-down 66% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.578% ; recovery-V 27%
- **σ réalisé intraday** 5.005% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 71% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1847200.0 (VA 1832800.0–1864000.0 ; dernier close 1840000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 48% · rebond 78% · **stop −8.8%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.29 (high win-rate)
- Gaps overnight (n=137) : méd. -0.14% · baisse 52% (gap-down >1% 37% · >2% 29%)
- Excursion ouverture 5min (n=138) : bas méd −0.56% (p90 −1.67%) · haut méd +0.99% · range méd 1.51%
- Excursion ouverture 15min (n=138) : bas méd −0.79% (p90 −2.15%) · haut méd +1.18% · range méd 2.05%
- Excursion ouverture 30min (n=138) : bas méd −1.28% (p90 −3.03%) · haut méd +1.36% · range méd 2.73%
- Excursion ouverture 60min (n=138) : bas méd −1.34% (p90 −3.83%) · haut méd +1.7% · range méd 3.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1840000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 66% (85/137) · gap 42% · délai 0.0min · rebond 54% (44/85) (MFE +1.29%)
   - −1.0% : fill 30min 55% · séance 62% (78/137) · gap 37% · délai 0.0min · rebond 63% (48/78) (MFE +1.64%)
   - −1.5% : fill 30min 50% · séance 59% (70/137) · gap 34% · délai 0.0min · rebond 66% (44/70) (MFE +1.79%)
   - −2.0% : fill 30min 41% · séance 52% (63/137) · gap 29% · délai 0.0min · rebond 63% (41/63) (MFE +1.67%)
   - −3.0% : fill 30min 40% · séance 48% (55/137) · gap 23% · délai 2.7min · rebond 78% (41/55) (MFE +2.57%)
   - −4.0% : fill 30min 29% · séance 39% (42/137) · gap 12% · délai 6.0min · rebond 76% (32/42) (MFE +2.57%)
   - −5.0% : fill 30min 13% · séance 31% (33/137) · gap 9% · délai 30.4min · rebond 72% (25/33) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.6%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.44%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.5% (p90 −3.71%) → stop au-delà de −2.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=692 jambes) : jambe baissière méd −1.3% (p90 −3.39%) · ~12.0 jambes/séance
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
   - **gap-up** (66 séances) :
      · −1.0% : fill 22% (12/66) · rebond 98% (11/12)
      · −2.0% : fill 14% (8/66) · rebond 75% (7/8)
      · −3.0% : fill 12% (6/66) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/66) · rebond 100% (3/3)
      · −5.0% : fill 5% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 46% en base · 55% si les 15 1res min sont vertes (74 cas) · 34% si rouges (64 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=138) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 74% si début vert vs 18% si rouge (base 46% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -1.56% (q20 -6.57%) → **SL/trailing à −6.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.41% → **scale +1.31% / runner +3.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=63) : edge inversé — récupère vert seulement **18%** (continue à baisser 62%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.8%** (au-delà de la MAE q10 -6.8%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-2.87% .. +3.0%] · haut q95 +3.68% · bas q05 -3.69%
   - 60min (n=138) : retour [-3.55% .. +5.74%] · haut q95 +5.81% · bas q05 -5.17%
   - 2h (n=138) : retour [-4.68% .. +5.71%] · haut q95 +7.96% · bas q05 -6.69%
   - 4h (n=138) : retour [-5.87% .. +7.16%] · haut q95 +8.52% · bas q05 -8.11%
   - 6h (n=138) : retour [-7.28% .. +7.81%] · haut q95 +9.81% · bas q05 -9.03%
   - session (n=138) : retour [-6.65% .. +8.13%] · haut q95 +9.81% · bas q05 -9.03%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87416 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
