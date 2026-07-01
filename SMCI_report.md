# SMCI

**Generated** : 2026-07-01T21:50:28.813711+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $27.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $27.65 (+2.0% vs entrée) · entrée $27.10 · stop $25.91 · T1 $29.48 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.128 _(réel 5 s)_ (GBM 0.072) · ¼-Kelly 0.052 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.39% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $26.81–$27.39 (mid $27.10)
- Spot actuel : $27.65 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $25.91 (stop swing_plan-based (-15.83%))
- Targets : T1 $29.48 · R/R 2.0 | T2 $30.47 · R/R 2.83 | T3 $31.47 · R/R 3.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $25.91


## Edge, scénarios & sizing

- EV/risk : 0.072 | EV/share : $0.086 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.21 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.1 | bear 5.0 | side 74.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.984% → cible +8.786% / stop −4.393%, p_fill 59%, n_eff≈24.1) : P(cible|rempli) **6%** · **EV/risk -0.128** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −4.352% → cible +32.373% / stop −12.0%, p_fill 49%, n_eff≈18.1) : P(cible|rempli) **0%** · **EV/risk -0.182** (×p_fill ; si rempli -4.42% du capital)
  - **deep** (entrée dip −6.737% → cible +16.969% / stop −8.484%, p_fill 55%, n_eff≈17.9) : P(cible|rempli) **44%** · **EV/risk +0.145** (×p_fill ; si rempli +2.25% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→45% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.17% (p90 11.21%) · excursion haute méd. +2.75% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.784% vs midi 1.267% vs clôture 1.464% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑0%/↓1% ; spike-down 65% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.157 ; mean-reverting — autocorr -0.039)_ ; drift intra méd. -0.071% ; recovery-V 28%
- **σ réalisé intraday** 4.598% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 63% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 29.5794 (VA 29.2374–29.7504 ; dernier close 29.33)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 64% · **stop −5.15%** sous le fill (sous le bruit) · cible +1.84% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 45% (gap-down >1% 30% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.45%) · haut méd +0.91% · range méd 1.93%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −3.28%) · haut méd +1.23% · range méd 2.63%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −4.01%) · haut méd +1.43% · range méd 3.48%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −4.5%) · haut méd +1.75% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 29.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (125/159) · gap 41% · délai 0.0min · rebond 57% (72/125) (MFE +1.24%)
   - −1.0% : fill 30min 60% · séance 68% (112/159) · gap 30% · délai 0.0min · rebond 59% (63/112) (MFE +1.24%)
   - −1.5% : fill 30min 50% · séance 63% (97/159) · gap 25% · délai 0.7min · rebond 66% (59/97) (MFE +1.5%)
   - −2.0% : fill 30min 45% · séance 57% (87/159) · gap 20% · délai 2.4min · rebond 69% (55/87) (MFE +1.92%)
   - −3.0% : fill 30min 27% · séance 50% (67/159) · gap 16% · délai 13.5min · rebond 59% (39/67) (MFE +1.91%)
   - −4.0% : fill 30min 20% · séance 40% (49/159) · gap 12% · délai 22.4min · rebond 64% (30/49) (MFE +1.4%)
   - −5.0% : fill 30min 16% · séance 31% (40/159) · gap 8% · délai 22.0min · rebond 64% (26/40) (MFE +1.84%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.97%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.84%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −2.75%) → stop au-delà de −1.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=819 jambes) : jambe baissière méd −1.22% (p90 −2.79%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 97% (66/67) · rebond 55% (37/66)
      · −2.0% : fill 89% (58/67) · rebond 58% (32/58)
      · −3.0% : fill 82% (50/67) · rebond 60% (29/50)
      · −4.0% : fill 69% (39/67) · rebond 66% (24/39)
      · −5.0% : fill 53% (32/67) · rebond 60% (20/32)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (32/76) · rebond 61% (16/32)
      · −2.0% : fill 29% (19/76) · rebond 95% (16/19)
      · −3.0% : fill 26% (15/76) · rebond 53% (8/15)
      · −4.0% : fill 18% (9/76) · rebond 56% (5/9)
      · −5.0% : fill 16% (8/76) · rebond 76% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 74% si les 15 1res min sont vertes (71 cas) · 29% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 50% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 55% ; creux résiduel méd -1.26% (q20 -3.2%) → **SL/trailing à −3.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.06% / q75 +3.42% → **scale +2.06% / runner +3.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.48%** (au-delà de la MAE q10 -6.48%), cible rebond +1.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.21% .. +4.68%] · haut q95 +6.31% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.5% .. +5.48%] · haut q95 +6.59% · bas q05 -5.82%
   - 2h (n=160) : retour [-5.09% .. +6.65%] · haut q95 +8.38% · bas q05 -5.85%
   - 4h (n=160) : retour [-6.81% .. +7.46%] · haut q95 +8.73% · bas q05 -7.92%
   - 6h (n=160) : retour [-6.86% .. +7.9%] · haut q95 +9.4% · bas q05 -9.62%
   - session (n=160) : retour [-8.68% .. +8.75%] · haut q95 +9.46% · bas q05 -9.91%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 14% vs absente 4% (base 6%)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.8  _(neutre)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist -0.763  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 75.8%
- **ATR** : 2.63 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.137  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 52.0  _(transition)_
- **MA** : MA20 33.97 · MA50 33.48 · MA200 35.11  _(prix < MA20)_
- **Dist MA** : MA20 -18.6% · MA50 -17.4% · MA200 -21.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90806 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
