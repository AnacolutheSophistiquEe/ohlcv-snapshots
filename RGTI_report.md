# RGTI

**Generated** : 2026-07-27T00:25:34.342553+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $14.17  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $14.17 (+3.0% vs entrée) · entrée $13.76 · stop $13.44 · T1 $14.41 · R/R 2.03  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.331 _(réel 5 s)_ (GBM 0.175) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.35% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +4.4 % ≠ (strike 15.5 − spot 14.17)/spot = +9.4 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -107 % hors [0,100] (R² max 0.43). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $13.69–$13.83 (mid $13.76)
- Spot actuel : $14.17 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $13.44 (stop swing_plan-based (-8.84%))
- Targets : T1 $14.41 · R/R 2.03 | T2 $14.57 · R/R 2.53 | T3 $14.74 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $13.44


## Edge, scénarios & sizing

- EV/risk : 0.175 | EV/share : $0.057 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.072 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.7 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.894% → cible +4.709% / stop −2.354%, p_fill 44%, n_eff≈19.6) : P(cible|rempli) **4%** · **EV/risk -0.331** (×p_fill ; si rempli -1.77% du capital)
  - **swing** (entrée dip −6.366% → cible +5.284% / stop −2.642%, p_fill 43%, n_eff≈18.5) : P(cible|rempli) **27%** · **EV/risk -0.086** (×p_fill ; si rempli -0.53% du capital)
  - **deep** (entrée dip −9.841% → cible +7.473% / stop −3.737%, p_fill 49%, n_eff≈18.0) : P(cible|rempli) **19%** · **EV/risk -0.184** (×p_fill ; si rempli -1.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→71% · +3.0%→55% · +5.0%→36% · +8.0%→14%
- Range intraday médian 8.01% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.342% vs midi 1.659% vs clôture 1.861% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.018)_ ; drift intra méd. -0.505% ; recovery-V 36%
- **σ réalisé intraday** 4.839% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 59% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 14.4712 (VA 14.3407–14.6762 ; dernier close 14.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 76% · **stop −6.87%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 58% (gap-down >1% 46% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.8%) · haut méd +1.13% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.1%) · haut méd +1.54% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −5.33%) · haut méd +1.95% · range méd 4.65%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.24%) · haut méd +2.23% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.17 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (135/159) · gap 51% · délai 0.0min · rebond 66% (89/135) (MFE +2.29%)
   - −1.0% : fill 30min 71% · séance 82% (131/159) · gap 46% · délai 0.0min · rebond 67% (87/131) (MFE +2.06%)
   - −1.5% : fill 30min 66% · séance 76% (123/159) · gap 40% · délai 0.0min · rebond 66% (82/123) (MFE +2.38%)
   - −2.0% : fill 30min 60% · séance 70% (114/159) · gap 30% · délai 0.0min · rebond 65% (75/114) (MFE +2.44%)
   - −3.0% : fill 30min 53% · séance 62% (97/159) · gap 12% · délai 1.2min · rebond 76% (71/97) (MFE +2.55%)
   - −4.0% : fill 30min 38% · séance 47% (76/159) · gap 4% · délai 5.8min · rebond 75% (55/76) (MFE +2.38%)
   - −5.0% : fill 30min 22% · séance 38% (62/159) · gap 1% · délai 21.6min · rebond 68% (46/62) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.76%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.19% (p90 −3.07%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.07%) → stop au-delà de −2.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.31% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 65% (51/82)
      · −2.0% : fill 88% (77/83) · rebond 65% (52/77)
      · −3.0% : fill 82% (69/83) · rebond 71% (49/69)
      · −4.0% : fill 62% (54/83) · rebond 71% (38/54)
      · −5.0% : fill 53% (46/83) · rebond 66% (35/46)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 55% (36/61) · rebond 64% (25/36)
      · −2.0% : fill 42% (26/61) · rebond 62% (15/26)
      · −3.0% : fill 35% (22/61) · rebond 88% (18/22)
      · −4.0% : fill 22% (16/61) · rebond 83% (13/16)
      · −5.0% : fill 18% (11/61) · rebond 67% (8/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (81 cas) · 34% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 16% si rouge (base 51% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **90%** · continue >prix actuel 53% ; creux résiduel méd -2.08% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.6% / q75 +4.26% → **scale +2.6% / runner +4.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.69%** (au-delà de la MAE q10 -5.69%), cible rebond +2.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.26% .. +4.6%] · haut q95 +6.96% · bas q05 -6.56%
   - 60min (n=160) : retour [-6.03% .. +6.48%] · haut q95 +8.03% · bas q05 -7.05%
   - 2h (n=160) : retour [-7.22% .. +7.71%] · haut q95 +9.18% · bas q05 -8.2%
   - 4h (n=160) : retour [-7.8% .. +6.34%] · haut q95 +9.19% · bas q05 -8.8%
   - 6h (n=160) : retour [-8.41% .. +7.76%] · haut q95 +9.34% · bas q05 -10.19%
   - session (n=160) : retour [-7.51% .. +8.55%] · haut q95 +10.48% · bas q05 -10.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.8  _(survente)_
- **ADX** : 30.4  _(tendance etablie)_
- **MACD** : hist -0.053  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 43.4%
- **ATR** : 1.03 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 16.37 · MA50 19.45 · MA200 22.77  _(prix < MA20)_
- **Dist MA** : MA20 -13.4% · MA50 -27.2% · MA200 -37.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83529 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
