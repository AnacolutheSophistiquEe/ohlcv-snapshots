# ENR

**Generated** : 2026-07-13T00:05:52.316295+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · €152.12  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €152.12 (+0.6% vs entrée) · entrée €151.22 · stop €147.90 · T1 €157.87 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.137 _(réel 5 s)_ (GBM 0.113) · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €150.33–€152.12 (mid €151.22)
- Spot actuel : €152.12 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €147.90 (stop swing_plan-based (-2.78%))
- Targets : T1 €157.87 · R/R 2.0 | T2 €164.53 · R/R 4.01 | T3 €171.18 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €147.90


## Edge, scénarios & sizing

- EV/risk : 0.113 | EV/share : €0.374 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.033 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 12.0 | bear 20.7 | side 67.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 152.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.348% → cible +1.967% / stop −8.0%, p_fill 89%, n_eff≈35.5) : P(cible|rempli) **29%** · **EV/risk -0.084** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −0.594% → cible +4.399% / stop −2.199%, p_fill 85%, n_eff≈34.1) : P(cible|rempli) **30%** · **EV/risk -0.137** (×p_fill ; si rempli -0.35% du capital)
  - **deep** (entrée dip −0.774% → cible +6.221% / stop −3.11%, p_fill 89%, n_eff≈34.8) : P(cible|rempli) **27%** · **EV/risk -0.209** (×p_fill ; si rempli -0.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→61% · +2.0%→46% · +3.0%→24% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.08% (p90 6.09%) · excursion haute méd. +1.53% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.132% vs midi 0.944% vs clôture 1.186% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.498% ; recovery-V 26%
- **σ réalisé intraday** 2.558% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 67% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 153.8465 (VA 152.6475–154.8275 ; dernier close 152.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 67% · **stop −2.92%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 40% (gap-down >1% 21% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.93%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.23%) · haut méd +0.58% · range méd 1.52%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.42%) · haut méd +0.59% · range méd 1.78%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.61% · range méd 1.99%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 152.06 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 72% (114/159) · gap 29% · délai 0.4min · rebond 52% (58/114) (MFE +1.11%)
   - −1.0% : fill 30min 50% · séance 67% (103/159) · gap 21% · délai 1.2min · rebond 56% (60/103) (MFE +1.31%)
   - −1.5% : fill 30min 40% · séance 60% (89/159) · gap 18% · délai 8.5min · rebond 60% (56/89) (MFE +1.48%)
   - −2.0% : fill 30min 25% · séance 45% (65/159) · gap 13% · délai 11.3min · rebond 58% (38/65) (MFE +1.26%)
   - −3.0% : fill 30min 16% · séance 34% (48/159) · gap 6% · délai 112.6min · rebond 63% (34/48) (MFE +1.42%)
   - −4.0% : fill 30min 9% · séance 25% (37/159) · gap 3% · délai 285.2min · rebond 60% (25/37) (MFE +1.23%)
   - −5.0% : fill 30min 3% · séance 16% (21/159) · gap 1% · délai 203.6min · rebond 67% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.85%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.22%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.52%) → stop au-delà de −0.86% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=489 jambes) : jambe baissière méd −1.06% (p90 −2.49%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 96% (45/46) · rebond 51% (25/45)
      · −2.0% : fill 74% (33/46) · rebond 58% (21/33)
      · −3.0% : fill 64% (28/46) · rebond 55% (19/28)
      · −4.0% : fill 49% (23/46) · rebond 55% (16/23)
      · −5.0% : fill 36% (15/46) · rebond 63% (10/15)
   - **flat** (26 séances) :
      · −1.0% : fill 72% (20/26) · rebond 69% (14/20)
      · −2.0% : fill 36% (9/26) · rebond 56% (4/9)
      · −3.0% : fill 18% (5/26) · rebond 80% (3/5)
      · −4.0% : fill 16% (4/26) · rebond 76% (2/4)
      · −5.0% : fill 10% (2/26) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 48% (38/87) · rebond 55% (21/38)
      · −2.0% : fill 30% (23/87) · rebond 60% (13/23)
      · −3.0% : fill 20% (15/87) · rebond 73% (12/15)
      · −4.0% : fill 12% (10/87) · rebond 67% (7/10)
      · −5.0% : fill 6% (4/87) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 86% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 49% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **86%** · continue >prix actuel 72% ; creux résiduel méd -1.09% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.3% → **scale +2.05% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 64%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.92%** (au-delà de la MAE q10 -4.92%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.01%] · haut q95 +2.58% · bas q05 -2.93%
   - 60min (n=160) : retour [-2.28% .. +2.07%] · haut q95 +2.74% · bas q05 -3.19%
   - 2h (n=160) : retour [-2.83% .. +2.39%] · haut q95 +3.11% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.82% .. +2.64%] · haut q95 +4.04% · bas q05 -3.78%
   - 6h (n=160) : retour [-3.13% .. +3.75%] · haut q95 +4.68% · bas q05 -4.43%
   - session (n=160) : retour [-5.24% .. +4.36%] · haut q95 +5.47% · bas q05 -5.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.0  _(momentum baissier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist -0.824  _(bearish_recent)_
- **BB** : %B 0.13 · largeur 15.3%
- **ATR** : 7.74 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.086  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 63.9  _(marche en range (choppy))_
- **MA** : MA20 161.37 · MA50 165.45 · MA200 141.13  _(prix < MA20)_
- **Dist MA** : MA20 -5.7% · MA50 -8.1% · MA200 +7.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92912 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
