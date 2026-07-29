# PRY

**Generated** : 2026-07-29T00:11:29.817810+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €116.55  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €116.55 (+0.5% vs entrée) · entrée €115.97 · stop €113.96 · T1 €120.00 · R/R 2.0  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.28 _(réel 5 s)_ (GBM 0.152) · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -55 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €115.39–€116.55 (mid €115.97)
- Spot actuel : €116.55 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €113.96 (stop swing_plan-based (-2.22%))
- Targets : T1 €120.00 · R/R 2.0 | T2 €124.02 · R/R 4.0 | T3 €128.05 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €113.96


## Edge, scénarios & sizing

- EV/risk : 0.152 | EV/share : €0.306 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.053 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.3 | bear 25.9 | side 40.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.553% / stop −8.0%, p_fill 84%, n_eff≈33.8) : P(cible|rempli) **41%** · **EV/risk -0.093** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −0.492% → cible +3.472% / stop −1.736%, p_fill 77%, n_eff≈32.0) : P(cible|rempli) **23%** · **EV/risk -0.280** (×p_fill ; si rempli -0.63% du capital)
  - **deep** (entrée dip −0.712% → cible +4.91% / stop −2.455%, p_fill 93%, n_eff≈35.9) : P(cible|rempli) **28%** · **EV/risk -0.207** (×p_fill ; si rempli -0.55% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→39% · +3.0%→28% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.88% (p90 6.33%) · excursion haute méd. +1.45% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.269% vs midi 0.792% vs clôture 1.135% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; neutre — autocorr -0.002)_ ; drift intra méd. -0.686% ; recovery-V 16%
- **σ réalisé intraday** 2.595% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 65% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 127.4387 (VA 125.6137–127.6212 ; dernier close 121.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 68% · **stop −2.31%** sous le fill (sous le bruit) · cible +1.31% · R/R 0.57 (high win-rate)
- Gaps overnight (n=140) : méd. 0.29% · baisse 42% (gap-down >1% 19% · >2% 12%)
- Excursion ouverture 5min (n=141) : bas méd −0.71% (p90 −2.07%) · haut méd +0.5% · range méd 1.38%
- Excursion ouverture 15min (n=141) : bas méd −0.91% (p90 −2.34%) · haut méd +0.64% · range méd 1.71%
- Excursion ouverture 30min (n=141) : bas méd −0.93% (p90 −2.94%) · haut méd +0.76% · range méd 1.84%
- Excursion ouverture 60min (n=141) : bas méd −1.18% (p90 −3.15%) · haut méd +0.87% · range méd 2.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 121.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (102/140) · gap 27% · délai 0.2min · rebond 61% (64/102) (MFE +1.23%)
   - −1.0% : fill 30min 50% · séance 63% (86/140) · gap 19% · délai 0.3min · rebond 56% (51/86) (MFE +1.47%)
   - −1.5% : fill 30min 33% · séance 53% (74/140) · gap 16% · délai 4.1min · rebond 46% (39/74) (MFE +0.85%)
   - −2.0% : fill 30min 24% · séance 44% (60/140) · gap 12% · délai 13.0min · rebond 52% (36/60) (MFE +1.14%)
   - −3.0% : fill 30min 14% · séance 36% (44/140) · gap 4% · délai 80.0min · rebond 59% (29/44) (MFE +1.57%)
   - −4.0% : fill 30min 4% · séance 22% (24/140) · gap 2% · délai 206.4min · rebond 68% (17/24) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 14% (16/140) · gap 1% · délai 389.4min · rebond 86% (13/16) (MFE +1.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.28% (p90 −1.61%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.56%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=426 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 89% (45/50) · rebond 46% (25/45)
      · −2.0% : fill 70% (36/50) · rebond 59% (24/36)
      · −3.0% : fill 61% (28/50) · rebond 69% (21/28)
      · −4.0% : fill 37% (15/50) · rebond 60% (10/15)
      · −5.0% : fill 26% (11/50) · rebond 89% (9/11)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (27/64) · rebond 66% (17/27)
      · −2.0% : fill 28% (17/64) · rebond 26% (7/17)
      · −3.0% : fill 21% (11/64) · rebond 48% (6/11)
      · −4.0% : fill 15% (6/64) · rebond 86% (5/6)
      · −5.0% : fill 7% (3/64) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 49% en base · 78% si les 15 1res min sont vertes (65 cas) · 26% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=141) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 86% si début vert vs 20% si rouge (base 49% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **86%** · continue >prix actuel 65% ; creux résiduel méd -1.29% (q20 -2.05%) → **SL/trailing à −2.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.6% → **scale +1.4% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **20%** (continue à baisser 67%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-2.84% .. +2.69%] · haut q95 +3.44% · bas q05 -3.34%
   - 60min (n=141) : retour [-2.9% .. +2.28%] · haut q95 +3.9% · bas q05 -3.47%
   - 2h (n=141) : retour [-3.58% .. +3.28%] · haut q95 +4.11% · bas q05 -3.68%
   - 4h (n=141) : retour [-3.46% .. +3.62%] · haut q95 +4.53% · bas q05 -4.45%
   - 6h (n=141) : retour [-3.71% .. +3.75%] · haut q95 +4.9% · bas q05 -4.61%
   - session (n=141) : retour [-4.92% .. +4.78%] · haut q95 +5.92% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.0% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 31.1  _(tendance etablie)_
- **MACD** : hist -1.27  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 23.3%
- **ATR** : 5.53 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.16  _(distribution)_
- **Vol ratio** : 1.33  _(volume normal)_
- **Choppiness** : 42.2  _(transition)_
- **MA** : MA20 132.55 · MA50 141.65 · MA200 109.95  _(prix < MA20)_
- **Dist MA** : MA20 -12.1% · MA50 -17.7% · MA200 +6.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91209 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
