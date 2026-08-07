# SOFI

**Generated** : 2026-08-07T00:32:45.577585+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $18.10 (+7.1% vs entrée) · entrée $16.90 · stop $15.98 · T1 $18.75 · R/R 2.01  
> ↳ P(T1 av. stop) 23 % · EV/risk -0.012 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.72–$17.08 (mid $16.90)
- Spot actuel : $18.10 (+7.1% au-dessus de la zone — repli à attendre)
- Stop : $15.98 (stop swing_plan-based (-11.74%))
- Targets : T1 $18.75 · R/R 2.01 | T2 $19.16 · R/R 2.46 | T3 $19.57 · R/R 2.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.98


## Edge, scénarios & sizing

- EV/risk : -0.123 | EV/share : $-0.114 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 9 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 43.0 | bear 25.3 | side 31.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 272.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.016% → cible +4.627% / stop −2.314%, p_fill 30%, n_eff≈14.5) : P(cible|rempli) **14%** · **EV/risk +0.138** (×p_fill ; si rempli +1.07% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→69% · +2.0%→49% · +3.0%→35% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.41% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.05% vs midi 0.906% vs clôture 1.011% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 16% · trend ↑2%/↓0% ; spike-down 65% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.363% ; recovery-V 20%
- **σ réalisé intraday** 2.901% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 58% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 18.4664 (VA 18.3139–18.6036 ; dernier close 18.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 69% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.84% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.22% · baisse 43% (gap-down >1% 26% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.74%) · haut méd +0.74% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.95%) · haut méd +0.99% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.33%) · haut méd +1.16% · range méd 2.82%
- Excursion ouverture 60min (n=160) : bas méd −1.49% (p90 −3.78%) · haut méd +1.3% · range méd 3.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (122/159) · gap 32% · délai 0.0min · rebond 52% (65/122) (MFE +1.18%)
   - −1.0% : fill 30min 54% · séance 67% (112/159) · gap 26% · délai 1.0min · rebond 62% (70/112) (MFE +1.27%)
   - −1.5% : fill 30min 47% · séance 63% (102/159) · gap 18% · délai 9.0min · rebond 64% (64/102) (MFE +1.51%)
   - −2.0% : fill 30min 38% · séance 51% (78/159) · gap 11% · délai 4.8min · rebond 69% (53/78) (MFE +1.84%)
   - −3.0% : fill 30min 18% · séance 38% (58/159) · gap 4% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 11% · séance 22% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 4% · séance 9% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.98%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −1.81%) → stop au-delà de −1.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=656 jambes) : jambe baissière méd −1.12% (p90 −2.79%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 97% (64/65) · rebond 60% (40/64)
      · −2.0% : fill 85% (54/65) · rebond 71% (39/54)
      · −3.0% : fill 71% (44/65) · rebond 73% (33/44)
      · −4.0% : fill 42% (29/65) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/65) · rebond 38% (8/14)
   - **flat** (23 séances) :
      · −1.0% : fill 55% (14/23) · rebond 46% (7/14)
      · −2.0% : fill 40% (8/23) · rebond 58% (4/8)
      · −3.0% : fill 34% (6/23) · rebond 57% (3/6)
      · −4.0% : fill 14% (3/23) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/23) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 45% (34/71) · rebond 70% (23/34)
      · −2.0% : fill 26% (16/71) · rebond 66% (10/16)
      · −3.0% : fill 11% (8/71) · rebond 39% (4/8)
      · −4.0% : fill 8% (7/71) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/71) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 58% si les 15 1res min sont vertes (72 cas) · 29% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 43% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **78%** · continue >prix actuel 57% ; creux résiduel méd -1.48% (q20 -2.95%) → **SL/trailing à −2.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +2.89% → **scale +1.91% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.11%** (au-delà de la MAE q10 -3.11%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.89% .. +3.67%] · haut q95 +4.01% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.12% .. +3.67%] · haut q95 +4.48% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.85%] · haut q95 +5.12% · bas q05 -4.6%
   - 4h (n=160) : retour [-3.8% .. +4.92%] · haut q95 +5.77% · bas q05 -5.05%
   - 6h (n=160) : retour [-4.6% .. +4.59%] · haut q95 +6.6% · bas q05 -5.08%
   - session (n=160) : retour [-4.53% .. +5.69%] · haut q95 +6.72% · bas q05 -5.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.8  _(neutre)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist 0.16  _(bullish_recent)_
- **BB** : %B 0.7 · largeur 21.4%
- **ATR** : 0.86 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.094  _(distribution)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 17.37 · MA50 17.39 · MA200 21.13  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 +4.1% · MA200 -14.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84997 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
