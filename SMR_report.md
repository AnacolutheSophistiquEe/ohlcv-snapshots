# SMR

**Generated** : 2026-08-01T21:52:10.399262+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $8.42  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $8.42 (+3.7% vs entrée) · entrée $8.12 · stop $7.91 · T1 $8.38 · R/R 1.24  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.048 _(réel 5 s)_ (GBM 0.086) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.53% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.07–$8.17 (mid $8.12)
- Spot actuel : $8.42 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $7.91 (stop swing_plan-based (-16.02%))
- Targets : T1 $8.38 · R/R 1.24 | T2 $8.64 · R/R 2.48 | T3 $8.90 · R/R 3.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.91


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : $0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.115 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.8 | bear 13.9 | side 9.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.595% → cible +3.208% / stop −2.525%, p_fill 48%, n_eff≈19.2) : P(cible|rempli) **34%** · **EV/risk -0.048** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −7.906% → cible +7.173% / stop −8.81%, p_fill 25%, n_eff≈11.0) : P(cible|rempli) **33%** · **EV/risk -0.064** (×p_fill ; si rempli -2.23% du capital)
  - **deep** (entrée dip −12.22% → cible +10.144% / stop −13.865%, p_fill 32%, n_eff≈11.4) : P(cible|rempli) **65%** · **EV/risk +0.032** (×p_fill ; si rempli +1.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→66% · +3.0%→59% · +5.0%→40% · +8.0%→18%
- Range intraday médian 7.8% (p90 12.61%) · excursion haute méd. +3.54% / basse méd. −3.33%
- Profil de vol intra : ouverture 5.08% vs midi 1.563% vs clôture 1.821% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.323% ; recovery-V 36%
- **σ réalisé intraday** 4.89% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 71% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 7.7364 (VA 7.6972–8.0112 ; dernier close 7.58)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 54% · rebond 77% · **stop −5.95%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.75% · baisse 60% (gap-down >1% 44% · >2% 31%)
- Excursion ouverture 5min (n=160) : bas méd −1.07% (p90 −3.21%) · haut méd +1.09% · range méd 2.71%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.69%) · haut méd +1.48% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −4.63%) · haut méd +2.14% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.85%) · haut méd +2.65% · range méd 5.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.58 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (130/159) · gap 52% · délai 0.0min · rebond 67% (80/130) (MFE +1.76%)
   - −1.0% : fill 30min 69% · séance 78% (125/159) · gap 44% · délai 0.0min · rebond 68% (83/125) (MFE +2.09%)
   - −1.5% : fill 30min 64% · séance 76% (119/159) · gap 40% · délai 0.0min · rebond 75% (88/119) (MFE +2.24%)
   - −2.0% : fill 30min 59% · séance 70% (112/159) · gap 31% · délai 0.0min · rebond 69% (82/112) (MFE +2.42%)
   - −3.0% : fill 30min 48% · séance 61% (100/159) · gap 11% · délai 2.0min · rebond 75% (81/100) (MFE +2.59%)
   - −4.0% : fill 30min 36% · séance 54% (84/159) · gap 7% · délai 11.3min · rebond 77% (65/84) (MFE +2.56%)
   - −5.0% : fill 30min 26% · séance 43% (63/159) · gap 3% · délai 19.6min · rebond 71% (46/63) (MFE +2.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.71%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.98%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.02% (p90 −3.62%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1175 jambes) : jambe baissière méd −1.4% (p90 −3.23%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 100% (85/85) · rebond 70% (57/85)
      · −2.0% : fill 94% (81/85) · rebond 75% (62/81)
      · −3.0% : fill 85% (76/85) · rebond 77% (63/76)
      · −4.0% : fill 75% (66/85) · rebond 81% (54/66)
      · −5.0% : fill 60% (48/85) · rebond 74% (37/48)
   - **flat** (13 séances) :
      · −1.0% : fill 80% (10/13) · rebond 53% (6/10)
      · −2.0% : fill 69% (8/13) · rebond 22% (4/8)
      · −3.0% : fill 66% (6/13) · rebond 46% (3/6)
      · −4.0% : fill 66% (6/13) · rebond 56% (3/6)
      · −5.0% : fill 56% (5/13) · rebond 79% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 45% (30/61) · rebond 70% (20/30)
      · −2.0% : fill 32% (23/61) · rebond 66% (16/23)
      · −3.0% : fill 25% (18/61) · rebond 80% (15/18)
      · −4.0% : fill 18% (12/61) · rebond 67% (8/12)
      · −5.0% : fill 13% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (73 cas) · 33% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 84% si début vert vs 13% si rouge (base 46% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **84%** · continue >prix actuel 41% ; creux résiduel méd -2.3% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.19% → **scale +1.66% / runner +3.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **13%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.73%** (au-delà de la MAE q10 -4.73%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.47% .. +4.9%] · haut q95 +6.51% · bas q05 -6.01%
   - 60min (n=160) : retour [-6.43% .. +5.31%] · haut q95 +7.39% · bas q05 -7.73%
   - 2h (n=160) : retour [-7.55% .. +7.42%] · haut q95 +11.04% · bas q05 -8.34%
   - 4h (n=160) : retour [-7.96% .. +7.69%] · haut q95 +11.04% · bas q05 -10.44%
   - 6h (n=160) : retour [-7.92% .. +8.26%] · haut q95 +11.33% · bas q05 -10.41%
   - session (n=160) : retour [-7.88% .. +9.96%] · haut q95 +11.4% · bas q05 -10.71%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 50.6  _(neutre)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist 0.088  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 24.3%
- **ATR** : 0.68 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.04  _(neutre)_
- **Vol ratio** : 1.31  _(volume normal)_
- **Choppiness** : 63.3  _(marche en range (choppy))_
- **MA** : MA20 8.48 · MA50 9.97 · MA200 16.44  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 -15.5% · MA200 -48.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83383 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
