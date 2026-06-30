# SRT3

**Generated** : 2026-06-30T00:03:26.286824+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €226.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €226.10 (+0.8% vs entrée) · entrée €224.32 · stop €215.35 · T1 €227.37 · R/R 0.34  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.07 _(réel 5 s)_ (GBM 0.012) · ¼-Kelly 0.079 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €223.71–€224.93 (mid €224.32)
- Spot actuel : €226.10 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €215.35 (stop swing_plan-based (-3.23%))
- Targets : T1 €227.37 · R/R 0.34 | T2 €230.42 · R/R 0.68 | T3 €233.47 · R/R 1.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €215.35


## Edge, scénarios & sizing

- EV/risk : 0.012 | EV/share : €0.108 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 35 % | T3 12 %
- Kelly (position) : f* 0.317 | ¼-Kelly 0.079 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 67.5 | bear 14.9 | side 17.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.792% → cible +1.36% / stop −4.0%, p_fill 67%, n_eff≈26.8) : P(cible|rempli) **37%** · **EV/risk -0.070** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −1.736% → cible +3.041% / stop −1.52%, p_fill 72%, n_eff≈29.3) : P(cible|rempli) **39%** · **EV/risk +0.093** (×p_fill ; si rempli +0.20% du capital)
  - **deep** (entrée dip −2.677% → cible +4.3% / stop −2.15%, p_fill 64%, n_eff≈23.8) : P(cible|rempli) **46%** · **EV/risk +0.217** (×p_fill ; si rempli +0.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→70% · +2.0%→44% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.59%) · excursion haute méd. +1.8% / basse méd. −1.97%
- Profil de vol intra : ouverture 2.052% vs midi 0.894% vs clôture 1.021% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑1%/↓0% ; spike-down 56% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr 0.014)_ ; drift intra méd. -0.002% ; recovery-V 23%
- **σ réalisé intraday** 2.466% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 68% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 224.9712 (VA 223.7862–227.5387 ; dernier close 224.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 60% · rebond 67% · **stop −2.61%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 53% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.26% (p90 −1.82%) · haut méd +0.5% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.93%) · haut méd +0.66% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.51% (p90 −2.07%) · haut méd +0.77% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.64% (p90 −2.5%) · haut méd +0.82% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 224.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 76% (123/159) · gap 28% · délai 0.2min · rebond 49% (57/123) (MFE +1.0%)
   - −1.0% : fill 30min 43% · séance 63% (103/159) · gap 18% · délai 0.7min · rebond 56% (57/103) (MFE +1.15%)
   - −1.5% : fill 30min 33% · séance 60% (91/159) · gap 12% · délai 7.0min · rebond 67% (55/91) (MFE +1.56%)
   - −2.0% : fill 30min 22% · séance 44% (69/159) · gap 7% · délai 19.2min · rebond 60% (44/69) (MFE +1.33%)
   - −3.0% : fill 30min 7% · séance 25% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 13% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.11% (p90 −1.91%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.09% (p90 −1.94%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.18% (p90 −2.2%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=413 jambes) : jambe baissière méd −1.04% (p90 −2.4%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 83% (63/76) · rebond 64% (39/63)
      · −2.0% : fill 61% (43/76) · rebond 62% (29/43)
      · −3.0% : fill 42% (29/76) · rebond 56% (17/29)
      · −4.0% : fill 23% (16/76) · rebond 71% (12/16)
      · −5.0% : fill 12% (7/76) · rebond 92% (6/7)
   - **flat** (36 séances) :
      · −1.0% : fill 59% (20/36) · rebond 40% (9/20)
      · −2.0% : fill 44% (14/36) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/36) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/36) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/36) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 41% (20/47) · rebond 52% (9/20)
      · −2.0% : fill 20% (12/47) · rebond 72% (8/12)
      · −3.0% : fill 7% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 60% si les 15 1res min sont vertes (89 cas) · 39% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 76% si début vert vs 30% si rouge (base 51% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **76%** · continue >prix actuel 54% ; creux résiduel méd -0.93% (q20 -2.17%) → **SL/trailing à −2.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.69% → **scale +1.08% / runner +2.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **30%** (continue à baisser 49%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.25% .. +2.12%] · haut q95 +2.66% · bas q05 -2.77%
   - 60min (n=160) : retour [-2.53% .. +2.32%] · haut q95 +2.83% · bas q05 -3.2%
   - 2h (n=160) : retour [-2.31% .. +2.64%] · haut q95 +3.11% · bas q05 -3.32%
   - 4h (n=160) : retour [-2.73% .. +2.75%] · haut q95 +3.31% · bas q05 -3.56%
   - 6h (n=160) : retour [-2.75% .. +3.53%] · haut q95 +4.05% · bas q05 -4.01%
   - session (n=160) : retour [-3.71% .. +4.77%] · haut q95 +5.65% · bas q05 -4.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.2%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.3  _(momentum baissier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist -0.638  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 18.7%
- **ATR** : 9.99 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.15  _(distribution)_
- **Vol ratio** : 0.42  _(volume atone)_
- **Choppiness** : 52.1  _(transition)_
- **MA** : MA20 229.54 · MA50 226.45 · MA200 228.99  _(prix < MA20)_
- **Dist MA** : MA20 -1.5% · MA50 -0.2% · MA200 -1.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92647 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
