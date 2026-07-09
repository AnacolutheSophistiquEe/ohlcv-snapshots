# 000660

**Generated** : 2026-07-09T18:51:11.808118+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2190000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2190000.00 (+2.3% vs entrée) · entrée ₩2141166.61 · stop ₩2058730.90 · T1 ₩2227528.24 · R/R 1.05  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.164 _(réel 5 s)_ (GBM 0.068) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.85% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2123894.29–₩2158438.94 (mid ₩2141166.61)
- Spot actuel : ₩2190000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩2058730.90 (stop swing_plan-based (-9.19%))
- Targets : T1 ₩2227528.24 · R/R 1.05 | T2 ₩2313889.86 · R/R 2.1 | T3 ₩2400251.49 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2058730.90


## Edge, scénarios & sizing

- EV/risk : 0.068 | EV/share : ₩5561.131 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.102 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 62.2 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.226% → cible +4.033% / stop −3.85%, p_fill 64%, n_eff≈21.8) : P(cible|rempli) **27%** · **EV/risk -0.164** (×p_fill ; si rempli -0.99% du capital)
  - **swing** (entrée dip −4.902% → cible +9.019% / stop −4.509%, p_fill 43%, n_eff≈13.6) : P(cible|rempli) **23%** · **EV/risk -0.162** (×p_fill ; si rempli -1.69% du capital)
  - **deep** (entrée dip −7.586% → cible +12.755% / stop −6.377%, p_fill 36%, n_eff≈12.1) : P(cible|rempli) **45%** · **EV/risk +0.099** (×p_fill ; si rempli +1.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→72% · +2.0%→60% · +3.0%→48% · +5.0%→32% · +8.0%→16%
- Range intraday médian 6.7% (p90 12.2%) · excursion haute méd. +2.79% / basse méd. −2.1%
- Profil de vol intra : ouverture 4.522% vs midi 1.168% vs clôture 1.166% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (129 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 73% · range 23% · trend ↑4%/↓0% ; spike-down 61% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.158 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. 0.517% ; recovery-V 32%
- **σ réalisé intraday** 5.874% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 58% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 2160975.0 (VA 2112025.0–2214375.0 ; dernier close 2199000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 47% · rebond 84% · **stop −7.86%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.34 (high win-rate)
- Gaps overnight (n=128) : méd. -0.08% · baisse 54% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=129) : bas méd −0.46% (p90 −4.25%) · haut méd +1.16% · range méd 2.94%
- Excursion ouverture 15min (n=129) : bas méd −0.83% (p90 −4.4%) · haut méd +1.54% · range méd 3.48%
- Excursion ouverture 30min (n=129) : bas méd −1.3% (p90 −4.65%) · haut méd +1.69% · range méd 4.0%
- Excursion ouverture 60min (n=129) : bas méd −1.34% (p90 −5.19%) · haut méd +1.93% · range méd 4.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2199000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 70% (84/128) · gap 21% · délai 0.2min · rebond 60% (47/84) (MFE +1.72%)
   - −1.0% : fill 30min 56% · séance 63% (73/128) · gap 11% · délai 0.3min · rebond 67% (46/73) (MFE +1.82%)
   - −1.5% : fill 30min 49% · séance 58% (66/128) · gap 10% · délai 0.3min · rebond 69% (42/66) (MFE +1.84%)
   - −2.0% : fill 30min 40% · séance 52% (59/128) · gap 5% · délai 0.4min · rebond 67% (39/59) (MFE +1.91%)
   - −3.0% : fill 30min 38% · séance 47% (51/128) · gap 5% · délai 5.9min · rebond 84% (39/51) (MFE +2.67%)
   - −4.0% : fill 30min 25% · séance 37% (38/128) · gap 4% · délai 12.1min · rebond 77% (29/38) (MFE +2.71%)
   - −5.0% : fill 30min 11% · séance 28% (30/128) · gap 3% · délai 32.3min · rebond 74% (23/30) (MFE +2.41%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.0% (p90 −2.99%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.0% (p90 −3.7%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.0% (p90 −3.94%) → stop au-delà de −2.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=651 jambes) : jambe baissière méd −1.28% (p90 −3.47%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (39 séances) :
      · −1.0% : fill 81% (31/39) · rebond 59% (17/31)
      · −2.0% : fill 67% (26/39) · rebond 60% (16/26)
      · −3.0% : fill 62% (23/39) · rebond 86% (18/23)
      · −4.0% : fill 57% (21/39) · rebond 74% (16/21)
      · −5.0% : fill 49% (17/39) · rebond 79% (14/17)
   - **flat** (56 séances) :
      · −1.0% : fill 56% (31/56) · rebond 72% (21/31)
      · −2.0% : fill 44% (24/56) · rebond 64% (15/24)
      · −3.0% : fill 37% (19/56) · rebond 82% (14/19)
      · −4.0% : fill 23% (11/56) · rebond 82% (8/11)
      · −5.0% : fill 16% (9/56) · rebond 61% (6/9)
   - **gap-up** (33 séances) :
      · −1.0% : fill 48% (11/33) · rebond 77% (8/11)
      · −2.0% : fill 40% (9/33) · rebond 87% (8/9)
      · −3.0% : fill 40% (9/33) · rebond 82% (7/9)
      · −4.0% : fill 29% (6/33) · rebond 83% (5/6)
      · −5.0% : fill 15% (4/33) · rebond 67% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=129) : 53% en base · 69% si les 15 1res min sont vertes (73 cas) · 32% si rouges (56 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=129) : COUDE à **1:57** → P(séance verte=clôture>ouverture) 88% si début vert vs 7% si rouge (base 53% · écart 81 pts) ; prédictivité sature ensuite (plafond brut 147min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **88%** · continue >prix actuel 55% ; creux résiduel méd -1.32% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +3.88% → **scale +1.46% / runner +3.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=57) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.73%** (au-delà de la MAE q10 -6.73%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=129) : retour [-4.86% .. +8.7%] · haut q95 +9.63% · bas q05 -6.13%
   - 60min (n=129) : retour [-5.54% .. +7.73%] · haut q95 +9.63% · bas q05 -6.85%
   - 2h (n=129) : retour [-5.29% .. +9.18%] · haut q95 +9.68% · bas q05 -7.25%
   - 4h (n=129) : retour [-7.63% .. +11.41%] · haut q95 +11.9% · bas q05 -9.49%
   - 6h (n=129) : retour [-9.45% .. +12.13%] · haut q95 +14.41% · bas q05 -10.76%
   - session (n=129) : retour [-8.93% .. +11.5%] · haut q95 +14.5% · bas q05 -10.88%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.4% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -87248.263  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 40.7%
- **ATR** : 274785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 2486750.0 · MA50 2125244.49 · MA200 1066384.77  _(prix < MA20)_
- **Dist MA** : MA20 -11.9% · MA50 +3.0% · MA200 +105.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83577 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
