# SMCI

**Generated** : 2026-07-08T00:14:08.787390+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $26.25  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $26.25 (+0.9% vs entrée) · entrée $26.01 · stop $24.28 · T1 $29.48 · R/R 2.01  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.143 _(réel 5 s)_ (GBM 0.03) · ¼-Kelly 0.067 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −6.67% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $25.78–$26.25 (mid $26.01)
- Spot actuel : $26.25 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $24.28 (stop swing_plan-based (-7.72%))
- Targets : T1 $29.48 · R/R 2.01 | T2 $29.79 · R/R 2.18 | T3 $30.10 · R/R 2.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $24.28


## Edge, scénarios & sizing

- EV/risk : 0.03 | EV/share : $0.052 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.269 | ¼-Kelly 0.067 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.0 | bear 56.2 | side 26.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.902% → cible +13.336% / stop −6.668%, p_fill 76%, n_eff≈30.1) : P(cible|rempli) **2%** · **EV/risk -0.143** (×p_fill ; si rempli -1.26% du capital)
  - **swing** (entrée dip −1.985% → cible +11.703% / stop −5.851%, p_fill 74%, n_eff≈28.6) : P(cible|rempli) **15%** · **EV/risk -0.339** (×p_fill ; si rempli -2.67% du capital)
  - **deep** (entrée dip −2.894% → cible +16.551% / stop −8.275%, p_fill 65%, n_eff≈24.7) : P(cible|rempli) **36%** · **EV/risk -0.009** (×p_fill ; si rempli -0.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→48% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.47% (p90 11.21%) · excursion haute méd. +2.83% / basse méd. −2.66%
- Profil de vol intra : ouverture 3.816% vs midi 1.272% vs clôture 1.504% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.45% ; recovery-V 22%
- **σ réalisé intraday** 4.44% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 69% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 27.3216 (VA 26.9504–27.4701 ; dernier close 27.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 66% · **stop −4.81%** sous le fill (sous le bruit) · cible +1.93% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.31% · baisse 44% (gap-down >1% 30% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.28%) · haut méd +0.91% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −3.24%) · haut méd +1.23% · range méd 2.65%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.8%) · haut méd +1.44% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.54% (p90 −4.38%) · haut méd +1.76% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (125/159) · gap 40% · délai 0.0min · rebond 57% (72/125) (MFE +1.24%)
   - −1.0% : fill 30min 57% · séance 71% (113/159) · gap 30% · délai 0.0min · rebond 58% (64/113) (MFE +1.18%)
   - −1.5% : fill 30min 48% · séance 66% (98/159) · gap 25% · délai 2.7min · rebond 65% (60/98) (MFE +1.48%)
   - −2.0% : fill 30min 43% · séance 57% (87/159) · gap 21% · délai 2.4min · rebond 65% (55/87) (MFE +1.65%)
   - −3.0% : fill 30min 27% · séance 49% (67/159) · gap 16% · délai 13.6min · rebond 59% (40/67) (MFE +1.79%)
   - −4.0% : fill 30min 20% · séance 38% (48/159) · gap 12% · délai 15.4min · rebond 65% (29/48) (MFE +1.48%)
   - −5.0% : fill 30min 17% · séance 31% (39/159) · gap 8% · délai 15.8min · rebond 66% (25/39) (MFE +1.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.42%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −2.74%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.71%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.22% (p90 −2.88%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 97% (66/67) · rebond 53% (37/66)
      · −2.0% : fill 89% (58/67) · rebond 56% (32/58)
      · −3.0% : fill 82% (50/67) · rebond 57% (29/50)
      · −4.0% : fill 70% (39/67) · rebond 67% (24/39)
      · −5.0% : fill 55% (32/67) · rebond 63% (20/32)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 46% (33/76) · rebond 63% (17/33)
      · −2.0% : fill 29% (19/76) · rebond 85% (16/19)
      · −3.0% : fill 26% (15/76) · rebond 60% (9/15)
      · −4.0% : fill 16% (8/76) · rebond 56% (4/8)
      · −5.0% : fill 14% (7/76) · rebond 75% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (72 cas) · 27% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:11** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 46% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.46% (q20 -2.99%) → **SL/trailing à −2.99%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.9% → **scale +1.8% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **15%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.66%** (au-delà de la MAE q10 -6.66%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.68%] · haut q95 +6.06% · bas q05 -4.5%
   - 60min (n=160) : retour [-4.44% .. +5.32%] · haut q95 +6.58% · bas q05 -5.81%
   - 2h (n=160) : retour [-4.9% .. +6.65%] · haut q95 +8.25% · bas q05 -5.85%
   - 4h (n=160) : retour [-6.55% .. +7.42%] · haut q95 +8.67% · bas q05 -7.54%
   - 6h (n=160) : retour [-6.65% .. +7.54%] · haut q95 +9.19% · bas q05 -9.07%
   - session (n=160) : retour [-8.08% .. +8.56%] · haut q95 +9.43% · bas q05 -9.51%


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
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 23.2  _(pas de tendance nette)_
- **MACD** : hist -0.674  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 57.3%
- **ATR** : 2.46 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.133  _(distribution)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 42.0  _(transition)_
- **MA** : MA20 31.21 · MA50 33.41 · MA200 34.84  _(prix < MA20)_
- **Dist MA** : MA20 -15.9% · MA50 -21.4% · MA200 -24.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88318 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
