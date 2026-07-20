# SOFI

**Generated** : 2026-07-20T00:32:29.033639+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.28  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.28 (+1.8% vs entrée) · entrée $16.97 · stop $16.38 · T1 $17.23 · R/R 0.44  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM 0.007) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -285 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.92–$17.03 (mid $16.97)
- Spot actuel : $17.28 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $16.38 (stop swing_plan-based (-5.53%))
- Targets : T1 $17.23 · R/R 0.44 | T2 $17.49 · R/R 0.88 | T3 $17.75 · R/R 1.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.38


## Edge, scénarios & sizing

- EV/risk : 0.007 | EV/share : $0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 36 % | T3 15 %
- Kelly (position) : f* 0.135 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.5 | bear 17.8 | side 66.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.761% → cible +1.529% / stop −3.5%, p_fill 62%, n_eff≈24.2) : P(cible|rempli) **36%** · **EV/risk -0.079** (×p_fill ; si rempli -0.45% du capital)
  - **swing** (entrée dip −3.886% → cible +3.42% / stop −1.711%, p_fill 35%, n_eff≈12.4) : P(cible|rempli) **51%** · **EV/risk +0.176** (×p_fill ; si rempli +0.85% du capital)
  - **deep** (entrée dip −6.006% → cible +4.837% / stop −2.419%, p_fill 28%, n_eff≈10.4) : P(cible|rempli) **54%** · **EV/risk +0.156** (×p_fill ; si rempli +1.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→70% · +2.0%→50% · +3.0%→38% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.55% (p90 6.91%) · excursion haute méd. +1.97% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.074% vs midi 0.952% vs clôture 0.99% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 66% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.003)_ ; drift intra méd. -0.152% ; recovery-V 28%
- **σ réalisé intraday** 3.103% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 57% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 17.2812 (VA 16.9787–17.5562 ; dernier close 17.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 52% · rebond 73% · **stop −2.97%** sous le fill (sous le bruit) · cible +2.02% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. 0.11% · baisse 47% (gap-down >1% 25% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.76%) · haut méd +0.75% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −3.06%) · haut méd +1.12% · range méd 2.42%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.33%) · haut méd +1.29% · range méd 2.91%
- Excursion ouverture 60min (n=160) : bas méd −1.43% (p90 −3.79%) · haut méd +1.45% · range méd 3.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 76% (123/159) · gap 32% · délai 0.0min · rebond 56% (67/123) (MFE +1.22%)
   - −1.0% : fill 30min 52% · séance 68% (112/159) · gap 25% · délai 0.9min · rebond 64% (71/112) (MFE +1.34%)
   - −1.5% : fill 30min 46% · séance 63% (101/159) · gap 19% · délai 9.1min · rebond 65% (64/101) (MFE +1.76%)
   - −2.0% : fill 30min 39% · séance 52% (77/159) · gap 12% · délai 5.0min · rebond 73% (53/77) (MFE +2.02%)
   - −3.0% : fill 30min 18% · séance 37% (57/159) · gap 3% · délai 30.8min · rebond 63% (39/57) (MFE +1.47%)
   - −4.0% : fill 30min 9% · séance 24% (39/159) · gap 2% · délai 57.4min · rebond 58% (24/39) (MFE +1.41%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 1% · délai 60.7min · rebond 47% (10/19) (MFE +0.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.9%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.05%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −2.08%) → stop au-delà de −1.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=671 jambes) : jambe baissière méd −1.1% (p90 −2.76%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 96% (65/67) · rebond 72% (43/65)
      · −2.0% : fill 82% (52/67) · rebond 77% (39/52)
      · −3.0% : fill 64% (41/67) · rebond 73% (30/41)
      · −4.0% : fill 40% (27/67) · rebond 69% (20/27)
      · −5.0% : fill 19% (13/67) · rebond 47% (8/13)
   - **flat** (24 séances) :
      · −1.0% : fill 55% (15/24) · rebond 31% (8/15)
      · −2.0% : fill 36% (9/24) · rebond 37% (4/9)
      · −3.0% : fill 28% (7/24) · rebond 34% (4/7)
      · −4.0% : fill 20% (4/24) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/24) · rebond 0% (0/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 46% (32/68) · rebond 61% (20/32)
      · −2.0% : fill 29% (16/68) · rebond 77% (10/16)
      · −3.0% : fill 15% (9/68) · rebond 40% (5/9)
      · −4.0% : fill 11% (8/68) · rebond 20% (3/8)
      · −5.0% : fill 2% (4/68) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (72 cas) · 33% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 44% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.55% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.78% → **scale +1.69% / runner +2.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **13%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.02%** (au-delà de la MAE q10 -4.02%), cible rebond +1.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.94% .. +3.59%] · haut q95 +3.93% · bas q05 -3.61%
   - 60min (n=160) : retour [-3.21% .. +3.41%] · haut q95 +4.04% · bas q05 -4.02%
   - 2h (n=160) : retour [-3.73% .. +3.68%] · haut q95 +4.78% · bas q05 -4.98%
   - 4h (n=160) : retour [-4.03% .. +4.44%] · haut q95 +5.67% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.65% .. +3.96%] · haut q95 +5.69% · bas q05 -5.14%
   - session (n=160) : retour [-4.57% .. +4.94%] · haut q95 +5.69% · bas q05 -5.42%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -0.129  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 11.7%
- **ATR** : 0.94 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.062  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 17.91 · MA50 17.02 · MA200 21.82  _(prix < MA20)_
- **Dist MA** : MA20 -3.5% · MA50 +1.5% · MA200 -20.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83640 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
