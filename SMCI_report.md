# SMCI

**Generated** : 2026-06-30T00:14:09.193684+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $28.15  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $28.15 (+2.4% vs entrée) · entrée $27.48 · stop $26.37 · T1 $29.48 · R/R 1.8  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.09 _(réel 5 s)_ (GBM 0.082) · ¼-Kelly 0.045 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.02% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $27.18–$27.78 (mid $27.48)
- Spot actuel : $28.15 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $26.37 (stop swing_plan-based (-16.63%))
- Targets : T1 $29.48 · R/R 1.8 | T2 $30.72 · R/R 2.92 | T3 $31.96 · R/R 4.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.37


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : $0.091 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.182 | ¼-Kelly 0.045 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.1 | bear 5.0 | side 73.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.384% → cible +7.301% / stop −4.022%, p_fill 54%, n_eff≈22.2) : P(cible|rempli) **8%** · **EV/risk -0.090** (×p_fill ; si rempli -0.67% du capital)
  - **swing** (entrée dip −5.261% → cible +31.256% / stop −12.0%, p_fill 41%, n_eff≈15.3) : P(cible|rempli) **0%** · **EV/risk -0.067** (×p_fill ; si rempli -1.97% du capital)
  - **deep** (entrée dip −8.122% → cible +17.215% / stop −8.607%, p_fill 43%, n_eff≈13.0) : P(cible|rempli) **27%** · **EV/risk -0.068** (×p_fill ; si rempli -1.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→65% · +3.0%→45% · +5.0%→30% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.75% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.739% vs midi 1.264% vs clôture 1.44% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑0%/↓2% ; spike-down 66% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.155 ; mean-reverting — autocorr -0.034)_ ; drift intra méd. 0.218% ; recovery-V 30%
- **σ réalisé intraday** 4.466% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 64% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 30.7067 (VA 30.4652–31.0862 ; dernier close 30.64)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 62% · **stop −4.73%** sous le fill (sous le bruit) · cible +1.95% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 47% (gap-down >1% 32% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.52%) · haut méd +0.91% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.29%) · haut méd +1.23% · range méd 2.76%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −4.05%) · haut méd +1.42% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −4.31%) · haut méd +1.75% · range méd 4.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 76% (126/159) · gap 42% · délai 0.0min · rebond 58% (73/126) (MFE +1.31%)
   - −1.0% : fill 30min 60% · séance 69% (113/159) · gap 32% · délai 0.0min · rebond 58% (64/113) (MFE +1.34%)
   - −1.5% : fill 30min 50% · séance 64% (98/159) · gap 26% · délai 0.3min · rebond 65% (59/98) (MFE +1.55%)
   - −2.0% : fill 30min 44% · séance 58% (87/159) · gap 21% · délai 1.2min · rebond 68% (54/87) (MFE +1.96%)
   - −3.0% : fill 30min 28% · séance 50% (67/159) · gap 16% · délai 10.8min · rebond 57% (38/67) (MFE +1.8%)
   - −4.0% : fill 30min 21% · séance 39% (49/159) · gap 13% · délai 15.9min · rebond 62% (30/49) (MFE +1.29%)
   - −5.0% : fill 30min 17% · séance 31% (39/159) · gap 8% · délai 15.8min · rebond 62% (25/39) (MFE +1.95%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.04%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.91%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.78%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=819 jambes) : jambe baissière méd −1.22% (p90 −2.76%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (67/68) · rebond 55% (38/67)
      · −2.0% : fill 89% (59/68) · rebond 58% (32/59)
      · −3.0% : fill 82% (51/68) · rebond 60% (29/51)
      · −4.0% : fill 69% (40/68) · rebond 66% (25/40)
      · −5.0% : fill 53% (32/68) · rebond 60% (20/32)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 39% (32/75) · rebond 57% (16/32)
      · −2.0% : fill 27% (18/75) · rebond 95% (15/18)
      · −3.0% : fill 24% (14/75) · rebond 46% (7/14)
      · −4.0% : fill 16% (8/75) · rebond 45% (4/8)
      · −5.0% : fill 13% (7/75) · rebond 69% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 73% si les 15 1res min sont vertes (70 cas) · 30% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 79% si début vert vs 23% si rouge (base 50% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **79%** · continue >prix actuel 57% ; creux résiduel méd -1.09% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.27% / q75 +3.54% → **scale +2.27% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **23%** (continue à baisser 56%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.15%** (au-delà de la MAE q10 -6.15%), cible rebond +1.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.23% .. +4.71%] · haut q95 +6.45% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.53% .. +5.55%] · haut q95 +6.59% · bas q05 -5.44%
   - 2h (n=160) : retour [-5.19% .. +6.66%] · haut q95 +8.38% · bas q05 -5.84%
   - 4h (n=160) : retour [-6.85% .. +7.48%] · haut q95 +8.75% · bas q05 -8.05%
   - 6h (n=160) : retour [-6.47% .. +8.09%] · haut q95 +9.5% · bas q05 -8.09%
   - session (n=160) : retour [-7.07% .. +8.79%] · haut q95 +9.5% · bas q05 -8.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.4 · part idiosyncratique 0.6
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.8  _(survente)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist -0.81  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 83.7%
- **ATR** : 3.68 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.12  _(distribution)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 35.98 · MA50 33.49 · MA200 35.27  _(prix < MA20)_
- **Dist MA** : MA20 -21.8% · MA50 -16.0% · MA200 -20.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91034 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
