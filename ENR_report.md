# ENR

**Generated** : 2026-07-01T21:40:57.305757+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €163.34  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €163.34 (+22.0% vs entrée) · entrée €133.90 · stop €130.82 · T1 €140.07 · R/R 2.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.123 · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €132.67–€135.13 (mid €133.90)
- Spot actuel : €163.34 (+22.0% au-dessus de la zone — repli à attendre)
- Stop : €130.82 (stop swing_plan-based (-19.91%))
- Targets : T1 €140.07 · R/R 2.0 | T2 €146.24 · R/R 4.01 | T3 €152.41 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.82


## Edge, scénarios & sizing

- EV/risk : 0.123 | EV/share : €0.380 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 13 % | T3 4 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 45.6 | bear 26.5 | side 27.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 490.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→49% · +3.0%→26% · +5.0%→9% · +8.0%→1%
- Range intraday médian 4.38% (p90 6.09%) · excursion haute méd. +1.69% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.153% vs midi 0.999% vs clôture 1.211% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.288% ; recovery-V 16%
- **σ réalisé intraday** 2.613% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 63% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 165.764 (VA 164.724–165.868 ; dernier close 165.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 75% · **stop −1.46%** sous le fill (sous le bruit) · cible +1.5% · R/R 1.03 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 40% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.62% (p90 −1.82%) · haut méd +0.47% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.41%) · haut méd +0.63% · range méd 1.86%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.79% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 165.98 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 72% (112/159) · gap 27% · délai 0.4min · rebond 49% (55/112) (MFE +0.97%)
   - −1.0% : fill 30min 48% · séance 66% (100/159) · gap 21% · délai 1.4min · rebond 54% (57/100) (MFE +1.09%)
   - −1.5% : fill 30min 37% · séance 60% (87/159) · gap 17% · délai 12.9min · rebond 61% (54/87) (MFE +1.47%)
   - −2.0% : fill 30min 23% · séance 42% (63/159) · gap 11% · délai 16.5min · rebond 58% (37/63) (MFE +1.18%)
   - −3.0% : fill 30min 17% · séance 35% (49/159) · gap 4% · délai 126.0min · rebond 70% (36/49) (MFE +1.61%)
   - −4.0% : fill 30min 8% · séance 26% (37/159) · gap 2% · délai 302.8min · rebond 64% (25/37) (MFE +1.67%)
   - −5.0% : fill 30min 2% · séance 17% (21/159) · gap 1% · délai 378.8min · rebond 75% (14/21) (MFE +1.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.95%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.29%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=498 jambes) : jambe baissière méd −1.06% (p90 −2.53%) · ~7.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 55% (24/44)
      · −2.0% : fill 70% (32/45) · rebond 65% (21/32)
      · −3.0% : fill 63% (28/45) · rebond 67% (20/28)
      · −4.0% : fill 52% (23/45) · rebond 61% (16/23)
      · −5.0% : fill 37% (15/45) · rebond 74% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 67% (19/27) · rebond 63% (13/19)
      · −2.0% : fill 27% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 20% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 17% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 11% (2/27) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 47% (37/87) · rebond 48% (20/37)
      · −2.0% : fill 30% (23/87) · rebond 56% (13/23)
      · −3.0% : fill 23% (16/87) · rebond 74% (13/16)
      · −4.0% : fill 14% (10/87) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/87) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 86% si les 15 1res min sont vertes (79 cas) · 20% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **17min** → P(séance verte=clôture>ouverture) 84% si début vert vs 24% si rouge (base 49% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 244min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 69% ; creux résiduel méd -1.02% (q20 -2.33%) → **SL/trailing à −2.33%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.0% / q75 +3.05% → **scale +2.0% / runner +3.05%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **24%** (continue à baisser 62%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.02%** (au-delà de la MAE q10 -5.02%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.06%] · haut q95 +2.75% · bas q05 -2.73%
   - 60min (n=160) : retour [-2.43% .. +2.23%] · haut q95 +2.89% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.07% .. +2.61%] · haut q95 +3.46% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.03% .. +2.69%] · haut q95 +4.23% · bas q05 -3.89%
   - 6h (n=160) : retour [-3.21% .. +4.05%] · haut q95 +4.86% · bas q05 -4.47%
   - session (n=160) : retour [-4.95% .. +4.44%] · haut q95 +5.79% · bas q05 -6.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.64 · part idiosyncratique 0.36
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.6  _(momentum haussier)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 0.806  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 19.7%
- **ATR** : 7.33 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.096  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 54.2  _(transition)_
- **MA** : MA20 158.5 · MA50 168.15 · MA200 138.85  _(prix > MA20)_
- **Dist MA** : MA20 +3.1% · MA50 -2.9% · MA200 +17.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90798 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
