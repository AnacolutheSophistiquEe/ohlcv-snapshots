# SMCI

**Generated** : 2026-06-30T21:49:36.688432+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $29.33  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $29.33 (+3.4% vs entrée) · entrée $28.36 · stop $27.37 · T1 $29.48 · R/R 1.13  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk -0.124 _(réel 5 s)_ (GBM 0.047) · ¼-Kelly 0.035 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.51% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $28.14–$28.59 (mid $28.36)
- Spot actuel : $29.33 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $27.37 (stop swing_plan-based (-18.39%))
- Targets : T1 $29.48 · R/R 1.13 | T2 $31.25 · R/R 2.92 | T3 $33.03 · R/R 4.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.37


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : $0.047 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.139 | ¼-Kelly 0.035 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.6 | bear 13.5 | side 78.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.299% → cible +3.953% / stop −3.507%, p_fill 42%, n_eff≈15.3) : P(cible|rempli) **17%** · **EV/risk -0.124** (×p_fill ; si rempli -1.03% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→64% · +3.0%→44% · +5.0%→30% · +8.0%→12%
- Range intraday médian 6.17% (p90 11.21%) · excursion haute méd. +2.65% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.751% vs midi 1.263% vs clôture 1.46% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓2% ; spike-down 67% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.158 ; neutre — autocorr -0.03)_ ; drift intra méd. -0.23% ; recovery-V 28%
- **σ réalisé intraday** 4.629% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 66% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 30.0291 (VA 29.0914–31.1374 ; dernier close 28.13)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 64% · **stop −5.15%** sous le fill (sous le bruit) · cible +1.84% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 46% (gap-down >1% 31% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.46%) · haut méd +0.91% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.28%) · haut méd +1.21% · range méd 2.71%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −4.03%) · haut méd +1.38% · range méd 3.47%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.53%) · haut méd +1.67% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.13 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (126/159) · gap 41% · délai 0.0min · rebond 57% (72/126) (MFE +1.23%)
   - −1.0% : fill 30min 61% · séance 70% (113/159) · gap 31% · délai 0.0min · rebond 59% (64/113) (MFE +1.23%)
   - −1.5% : fill 30min 50% · séance 64% (98/159) · gap 26% · délai 0.8min · rebond 66% (59/98) (MFE +1.5%)
   - −2.0% : fill 30min 45% · séance 58% (88/159) · gap 21% · délai 2.5min · rebond 69% (55/88) (MFE +1.92%)
   - −3.0% : fill 30min 27% · séance 50% (68/159) · gap 16% · délai 13.8min · rebond 59% (39/68) (MFE +1.89%)
   - −4.0% : fill 30min 20% · séance 40% (50/159) · gap 13% · délai 22.7min · rebond 64% (31/50) (MFE +1.41%)
   - −5.0% : fill 30min 16% · séance 32% (40/159) · gap 8% · délai 22.0min · rebond 64% (26/40) (MFE +1.84%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.04%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.91%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.78%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=820 jambes) : jambe baissière méd −1.22% (p90 −2.83%) · ~11.8 jambes/séance
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
      · −1.0% : fill 41% (32/75) · rebond 61% (16/32)
      · −2.0% : fill 30% (19/75) · rebond 95% (16/19)
      · −3.0% : fill 27% (15/75) · rebond 53% (8/15)
      · −4.0% : fill 19% (9/75) · rebond 56% (5/9)
      · −5.0% : fill 17% (8/75) · rebond 76% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 73% si les 15 1res min sont vertes (70 cas) · 29% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 79% si début vert vs 22% si rouge (base 49% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **79%** · continue >prix actuel 57% ; creux résiduel méd -1.09% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.27% / q75 +3.54% → **scale +2.27% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.48%** (au-delà de la MAE q10 -6.48%), cible rebond +1.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.22% .. +4.68%] · haut q95 +6.38% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.52% .. +5.51%] · haut q95 +6.59% · bas q05 -5.82%
   - 2h (n=160) : retour [-5.16% .. +6.66%] · haut q95 +8.38% · bas q05 -5.85%
   - 4h (n=160) : retour [-6.84% .. +7.47%] · haut q95 +8.74% · bas q05 -7.99%
   - 6h (n=160) : retour [-6.9% .. +7.99%] · haut q95 +9.44% · bas q05 -9.72%
   - session (n=160) : retour [-8.73% .. +8.77%] · haut q95 +9.47% · bas q05 -9.98%


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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.42 · part idiosyncratique 0.58
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.9  _(momentum baissier)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist -0.744  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 82.1%
- **ATR** : 3.32 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 61.8  _(marche en range (choppy))_
- **MA** : MA20 35.1 · MA50 33.51 · MA200 35.19  _(prix < MA20)_
- **Dist MA** : MA20 -16.4% · MA50 -12.5% · MA200 -16.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90264 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
