# SMCI

**Generated** : 2026-07-09T22:02:22.611088+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $28.24  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $28.24 (+2.5% vs entrée) · entrée $27.55 · stop $26.58 · T1 $29.48 · R/R 1.99  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.146 _(réel 5 s)_ (GBM 0.086) · ¼-Kelly 0.045 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.52% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $27.26–$27.83 (mid $27.55)
- Spot actuel : $28.24 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $26.58 (stop swing_plan-based (-16.76%))
- Targets : T1 $29.48 · R/R 1.99 | T2 $30.68 · R/R 3.23 | T3 $31.87 · R/R 4.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.58


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : $0.084 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.182 | ¼-Kelly 0.045 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.6 | bear 55.7 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.457% → cible +7.038% / stop −3.519%, p_fill 58%, n_eff≈22.4) : P(cible|rempli) **1%** · **EV/risk -0.146** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −5.409% → cible +31.057% / stop −12.0%, p_fill 51%, n_eff≈18.7) : P(cible|rempli) **0%** · **EV/risk -0.196** (×p_fill ; si rempli -4.57% du capital)
  - **deep** (entrée dip −8.363% → cible +16.537% / stop −8.269%, p_fill 45%, n_eff≈14.7) : P(cible|rempli) **26%** · **EV/risk -0.141** (×p_fill ; si rempli -2.58% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→49% · +5.0%→32% · +8.0%→12%
- Range intraday médian 6.69% (p90 11.21%) · excursion haute méd. +2.92% / basse méd. −2.66%
- Profil de vol intra : ouverture 3.868% vs midi 1.285% vs clôture 1.519% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓1% ; spike-down 67% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. -0.102% ; recovery-V 20%
- **σ réalisé intraday** 4.381% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 67% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 26.7955 (VA 26.7425–27.5905 ; dernier close 28.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 68% · **stop −4.65%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 46% (gap-down >1% 31% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.14%) · haut méd +0.92% · range méd 1.96%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −3.16%) · haut méd +1.33% · range méd 2.65%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.74%) · haut méd +1.47% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −4.4%) · haut méd +1.76% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.17 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 77% (126/159) · gap 40% · délai 0.0min · rebond 56% (72/126) (MFE +1.23%)
   - −1.0% : fill 30min 57% · séance 70% (113/159) · gap 31% · délai 0.0min · rebond 57% (63/113) (MFE +1.14%)
   - −1.5% : fill 30min 48% · séance 65% (99/159) · gap 26% · délai 1.1min · rebond 63% (60/99) (MFE +1.45%)
   - −2.0% : fill 30min 44% · séance 57% (88/159) · gap 22% · délai 1.1min · rebond 66% (56/88) (MFE +1.59%)
   - −3.0% : fill 30min 28% · séance 50% (68/159) · gap 16% · délai 18.8min · rebond 57% (40/68) (MFE +1.77%)
   - −4.0% : fill 30min 20% · séance 39% (49/159) · gap 11% · délai 22.8min · rebond 67% (30/49) (MFE +1.49%)
   - −5.0% : fill 30min 16% · séance 32% (40/159) · gap 7% · délai 22.7min · rebond 68% (26/40) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.3%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.72%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.68%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=816 jambes) : jambe baissière méd −1.22% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 93% (67/69) · rebond 51% (37/67)
      · −2.0% : fill 86% (59/69) · rebond 58% (33/59)
      · −3.0% : fill 80% (51/69) · rebond 55% (29/51)
      · −4.0% : fill 68% (40/69) · rebond 69% (25/40)
      · −5.0% : fill 55% (33/69) · rebond 66% (21/33)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 46% (32/74) · rebond 62% (16/32)
      · −2.0% : fill 29% (19/74) · rebond 85% (16/19)
      · −3.0% : fill 26% (15/74) · rebond 60% (9/15)
      · −4.0% : fill 16% (8/74) · rebond 56% (4/8)
      · −5.0% : fill 14% (7/74) · rebond 75% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 67% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:11** → P(séance verte=clôture>ouverture) 78% si début vert vs 14% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 53% ; creux résiduel méd -1.47% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.81% / q75 +2.99% → **scale +1.81% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.52%** (au-delà de la MAE q10 -6.52%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +4.68%] · haut q95 +6.05% · bas q05 -4.48%
   - 60min (n=160) : retour [-4.4% .. +5.23%] · haut q95 +6.58% · bas q05 -5.81%
   - 2h (n=160) : retour [-4.87% .. +6.65%] · haut q95 +7.97% · bas q05 -5.84%
   - 4h (n=160) : retour [-6.44% .. +7.42%] · haut q95 +8.64% · bas q05 -7.37%
   - 6h (n=160) : retour [-6.57% .. +7.38%] · haut q95 +9.08% · bas q05 -8.85%
   - session (n=160) : retour [-7.83% .. +8.42%] · haut q95 +9.41% · bas q05 -9.33%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 12% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.1  _(neutre)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist -0.325  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 31.7%
- **ATR** : 2.41 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.13  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 41.2  _(transition)_
- **MA** : MA20 29.8 · MA50 33.4 · MA200 34.66  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -15.5% · MA200 -18.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88712 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
